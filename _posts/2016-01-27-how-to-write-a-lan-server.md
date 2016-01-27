---
layout: post
title: "How to Write a LAN Server"
date: 2016-01-27
comments: true
---

Recently I had to write a LAN game server/client for [C-Dogs SDL](http://cxong.github.io/cdogs-sdl/). I was surprised at how little information was available, so I thought I might document my solution here.

## The Problem: Which IP to connect to?

Most people who have made, or attempted to make, network-multiplayer games will know that there are two ways to get two game instances to connect to each other:

1. Directly, by entering the **IP address** of the other game instance, or
2. Using an online "**server list**", which is basically a list of IP addresses constantly updated

Most "game server browsers" actually download lists from several known locations, a fancy way of doing no. 2. But no. 2 boils down to picking an IP from a list, which the game then uses to connect to directly anyway - no. 1. The point is: to connect two games, you need the **IP address**.

<sub>In ages past there were dial-up modems where you could connect using *phone numbers*, or IPX which is similar to IP but has different addresses. The protocols have changed but the problem is the same.</sub>

But how do games see each other on a LAN? Somehow many LAN-enabled games can scan and find servers running on a LAN, and avoid having to enter IP addresses manually. They also do this without having to access a remote server list.

## Broadcast Address

Fortunately, the solution is provided by the network itself: in IP networks, you can send messages to the [broadcast address](https://en.wikipedia.org/wiki/Broadcast_address) (255.255.255.255) and the network will pass the message on to all hosts on the network, that is, the LAN. Servers that understand the broadcast message can then reply back, alerting the broadcaster to their presence and address.

This is very simple in concept but takes a surprising amount of code to implement; IP broadcasts are only available for *connectionless, datagram sockets*, and most game network services either use TCP or a connection-based scheme to make things easier, so chances are you can't just shoehorn the broadcast functionality into your existing network handler. Therefore, the LAN "scanner" service will have to run on a different port, using UDP. The procedure is this:

1. The game server itself runs on port *A*, but a "listen" socket runs on a *fixed port B*.
2. The client scans for LAN servers by *broadcasting a UDP packet* on port *B*.
3. Servers receiving the broadcast scan reply back, optionally including the information that a game server is running on port *A*.
4. The client, upon receiving the reply, connects normally to the IP and on port *A*.

<sub>Full credit for [this solution](http://lists.cubik.org/pipermail/enet-discuss/2009-March/001072.html) goes to [Lee Salzman](http://sauerbraten.org/lee/), of Sauerbraten and ENet.</sub>

To illustrate, I'll provide a code walkthrough by implementing a basic chat service using C and ENet, an excellent cross-platform game networking library. But the same approach will work for your chosen language/framework, because we're dealing with socket networking for the most part. A full working server/client code example is available here: https://github.com/cxong/ENetLANChatServer

## The Server

The chat server will run the following:

1. Bind a UDP port for listening to broadcast scans
2. Bind another socket for the chat server itself
3. In a loop, we'll check for:
   - Scans: we'll reply with the chat server port
   - Chat server events: as we're a chat server, we'll just resend the text message to all clients

First, the initialisation:

```c
enet_initialize();
```

A common mistake is to forget to initialise ENet itself; you'll run into mysterious errors with the other ENet functions if you forget. Of course, like a good programmer you should *always* check your error values, but I'm omitting those in this post for brevity.

Next, start the listening socket, on port `34567` (pick any port that is likely to be unused):

```c
ENetSocket listen = enet_socket_create(ENET_SOCKET_TYPE_DATAGRAM);
// Allow the port to be reused by other applications - this means we can run several servers at once
enet_socket_set_option(listen, ENET_SOCKOPT_REUSEADDR, 1);
ENetAddress addr;
addr.host = ENET_HOST_ANY;
addr.port = 34567;
enet_socket_bind(listen, &listenaddr);
```

Now start the chat server itself (supporting up to `16` clients):

```c
ENetAddress addr;
addr.host = ENET_HOST_ANY;
addr.port = 0;  // let the OS choose a free port for us
ENetHost *host = enet_host_create(&addr, 16, 2, 0, 0);
```

Finally, in a loop, check for scans and also perform chat server logic. First the listener: since we're dealing with raw sockets, we're using the old `select()`/`recv()` combo to do non-blocking I/O.

```c
// The following code belongs in a function; we're using return to step out

// Use select to see if there is data to read
ENetSocketSet set;
ENET_SOCKETSET_EMPTY(set);
ENET_SOCKETSET_ADD(set, listen);
if (enet_socketset_select(listen, &set, NULL, 0) <= 0) return;

// Construct a data buffer (ENetBuffer) to receive the data
// Because we know exactly how big the scan packets will be (1 byte),
// we'll only set aside enough memory for that.
// If you want bigger payloads, adjust this to suit.
// If you want dynamic payloads, or you want to receive any payload just for the heck of it,
// use a suitably big buffer.
ENetAddress addr;
char buf;
ENetBuffer recvbuf;
recvbuf.data = &buf;
recvbuf.dataLength = 1;
if (enet_socket_receive(listen, &addr, &recvbuf, 1) <= 0) return;
// At this point we've received a packet; it would be a good idea to check its contents
// to make sure it's what we're looking for (like a magic number) and not random data,
// but all we're doing is sending a small reply so let's just do it, hooray for laziness!
// Reply to scanner client with the port of the server host
// We know the client address from the enet_socket_receive function
ENetBuffer replybuf;
replybuf.data = &host->address.port;
replybuf.dataLength = sizeof host->address.port;
enet_socket_send(listen, &addr, &replybuf, 1);
```

Then the chat server itself; as we're going for maximum <s>laziness</s> simplicity, we'll just broadcast the client's data packet right back at all clients. Since there's no validation or bounds checking, in a production environment this would be a gaping security hole :smile:

```c
ENetEvent event;
if (enet_host_service(host, &event, 0) > 0)
{
	// Whenever a client connects or disconnects, broadcast a message
	// Whenever a client says something, broadcast it including
	// which client it was from
	char buf[256];
	switch (event.type)
	{
		case ENET_EVENT_TYPE_CONNECT:
			send_string(host, "New client connected!");
			break;
		case ENET_EVENT_TYPE_RECEIVE:
			sprintf(buf, "Client says: %s", event.packet->data);
			send_string(server.host, buf);
			break;
		case ENET_EVENT_TYPE_DISCONNECT:
			send_string(host, "Client disconnected :(");
			break;
		default:
			break;
	}
}
```

Don't forget the helper function, `send_string()`:

```c
void send_string(ENetHost *host, char *s)
{
    // +1 for the null-terminator
	ENetPacket *packet = enet_packet_create(s, strlen(s) + 1, ENET_PACKET_FLAG_RELIABLE);
	enet_host_broadcast(host, 0, packet);
}
```

Finally, don't forget to tear everything down at the end:

```c
enet_socket_shutdown(listen, ENET_SOCKET_SHUTDOWN_READ_WRITE);
enet_socket_destroy(listen);
enet_host_destroy(host);
enet_deinitialize();
```

# The Client

The client is conceptually simple:

1. Send UDP broadcast scans to look for servers
2. Once we've received a reply, connect to that IP as a normal ENetHost
3. In a loop:
   - Get keys typed by the user; when they press enter send what they typed
   - Check for messages from the server; if there's any print them out

It turns out that getting keyboard input and performing network I/O together is pretty hard; we'll use [rlutil](https://github.com/tapio/rlutil), a sweet header file that contains some utility functions for console programs. We'll only be using `nb_getch()`, to get keyboard hits in a non-blocking manner.

First, as always, initialisation:

```c
enet_initialize();
```

Scan for the server, on port `34567` (where the server is listening)...

```c
ENetSocket scanner = enet_socket_create(ENET_SOCKET_TYPE_DATAGRAM);
// We need to set a socket option in order to send to the broadcast address
enet_socket_set_option(scanner, ENET_SOCKOPT_BROADCAST, 1);
ENetAddress addr;
addr.host = ENET_HOST_BROADCAST;
addr.port = 34567;
// Send a dummy payload; you can make your own (larger) payload
// but make sure to update the server code if you do
char data = 42;
ENetBuffer sendbuf;
sendbuf.data = &data;
sendbuf.dataLength = 1;
enet_socket_send(scanner, &addr, &sendbuf, 1);
```

...and wait for the reply:

```c
// Note that enet_socket_receive is blocking;
// for a non-blocking version use enet_socketset_select to check before receiving
ENetAddress addr;
enet_uint16 server_port;
ENetBuffer recvbuf;
recvbuf.data = &server_port;
recvbuf.dataLength = sizeof server_port;
enet_socket_receive(scanner, &addr, &recvbuf, 1);
// If the message is correct, we should have received sizeof(enet_uint16) worth of data
// Once again, error checking would be nice here, but omitted for brevity
addr.port = server_port;
// Now addr holds the exact host/port to connect to

// But first, shut down the scanner because we're done with it
enet_socket_shutdown(scanner, ENET_SOCKET_SHUTDOWN_READ_WRITE);
enet_socket_destroy(scanner);
```

Now that we have the server's address (`addr`), start our chat client host:

```c
ENetHost *host = enet_host_create(NULL, 1, 2, 0, 0);
ENetPeer *peer = enet_host_connect(host, &addr, 2, 0);
// Wait for 5 seconds for connection to succeed
ENetEvent event;
if (enet_host_service(host, &event, 5000) > 0 && event.type == ENET_EVENT_TYPE_CONNECT)
{
	printf("Connected\n");
}
```

The chat client is now connected; in a loop, check for the user's typed input, collecting the keys and sending them off on enter/return:

```c
// Keep a keyboard buffer outside the main loop
char buf[256];

// ... inside the loop

int k = nb_getch();
if (k == KEY_ENTER || k == '\r')
{
	// If we have something to say, say it to the server
	if (strlen(buf) > 0)
	{
		send_string(peer, buf);
	}
	memset(buf, 0, sizeof buf);
	printf("\n");
}
else if (k > 0 && strlen(buf) < 255)
{
	// Hold on to our message until we press enter
	buf[strlen(buf)] = (char)k;
	// Print the typed character out; otherwise the user doesn't know what was typed
	printf("%c", k);
}
```

The `send_string()` helper function is different for the client because we're only sending to the server, but otherwise it's exactly the same:

```c
void send_string(ENetPeer *peer, char *s)
{
	ENetPacket *packet = enet_packet_create(s, strlen(s) + 1, ENET_PACKET_FLAG_RELIABLE);
	enet_peer_send(peer, 0, packet);
}
```

We also need to check for server messages, and print whatever we get:

```c
ENetEvent event;
if (enet_host_service(host, &event, 0) > 0 && event.type == ENET_EVENT_TYPE_RECEIVE)
{
	printf("%s\n", event.packet->data);
}
```

Don't forget to tear down everything at the end:

```c
enet_peer_disconnect_now(peer, 0);
enet_host_destroy(host);
enet_deinitialize();
```

## The End

Phew! Hope that all makes sense. As I've said, the concept is simple but the code is verbose because we're pretty deep into socket code, with all the `select()`s, `recv()`s and socket options, thinly wrapped in ENet which makes it slightly less verbose. There's a [working server/client project available here](https://github.com/cxong/ENetLANChatServer), with the proper error checking mess for you to get started. Good luck!
