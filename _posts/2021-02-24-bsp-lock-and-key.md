---
layout: post
title: "BSP Lock and Key"
date: 2021-02-24
comments: true
published: true
---

I've been working on [C-Dogs SDL](https://cxong.github.io/cdogs-sdl/) lately, and one thing that often bothered me about that game is that its default random map generator provides an uneven experience. It's exciting at the start when everything's unexplored and there are many corridors and rooms to visit, but in the late stage when you are hunting for keys and objectives, backtracking all over the map, it can be quite tedious.

C-Dogs's map generator is quite configurable and produces a wide variety of maps, but at its core [it's pretty simple](https://github.com/cxong/cdogs-sdl/wiki/Classic-Maps):

- Start with an open area
- Randomly place rooms around the place
- Randomly lock some rooms, and place keys in the rooms

![C-Dogs map](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/cdogs_map.gif)

The lock-and-key system is in series: the yellow key is in an unlocked room, the green key is in a room locked with the yellow key, the blue key is in a room locked with the green key and so on. Here's a tree to illustrate this simple structure:

![C-Dogs map graph](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/cdogs_map_graph.png)

Because the keys (and objectives) could be in any one of several randomly placed rooms, you may need to criss-cross the map many times to collect them all. That's a lot of backtracking! Another issue is the structure - rooms are isolated from each other, all leading outside. This gives all maps a similar feel. What if there were a map generator that could:

- Provide a more interesting structure
- Feel more like an indoors experience, like a building interior or dungeon?

I was first inspired by **sauer2**, maker of many C-Dogs SDL custom campaigns, which often take place indoors. These have cool features like:

- Corridors linking many rooms
- Rooms connected directly to each other
- Locks separating entire sections of the map at a time
- Branching pathways
- Minimal required backtracking

![Space Pirates map](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/space_pirates_map.png)

Searching online, I came across a neat technique that uses [binary space partitioning to generate a building interior](https://gamedev.stackexchange.com/a/48216/26250). The algorithm recursively splits the area in half, placing a corridor at the split, and continues splitting (while alternating horizontal/vertical splits). Areas left unsplit are then filled with rooms. It's a simple yet flexible technique.

![BSP algo](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/bsp_algo.gif)

As the structure of the map is a deeper tree, by finding a critical path that starts and ends at leaf nodes but passes through the root, we can get a fairly long main path, with shorter branches along the way. Here's what that looks like, [in my initial adaptation](https://github.com/cxong/gomapgen#--algobspinterior---corridorwidth2):

![BSP interior demo](https://raw.githubusercontent.com/cxong/gomapgen/master/examples/bspinterior.gif)

<!--more-->

Here's where lock-and-key systems come in. Many games, including turn-based RPGs and action games, employ a [lock and key puzzle system](https://tvtropes.org/pmwiki/pmwiki.php/Main/LockAndKeyPuzzle) to get the player to explore and provide a sense of progress. Games like The Legend of Zelda do this particularly well - an analysis of the dungeons shows that most dungeons are quite linear, with few and shallow side branches, but the clever placement of locks and keys makes the dungeons feel more complex. The key to this is the placement of locks before the key that opens them, which provides foreshadowing.

![Zelda dungeon](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/first-zelda-dungeon.png)

It was quite easy to adapt this to the BSP map. As the critical path starts at a leaf node, goes up through parent nodes to the root, then down through child nodes to another leaf node, we can place locks in the intermediate parent nodes, and place keys somewhere in the sibling hierarchy.

![C-Dogs BSP path](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/cdogs_bsp_path.png)

Not only do players encounter the locks before keys, because of needing to sidetrack to find the key and then return to the lock, but the map is also made to feel bigger and more complex than otherwise.

![C-Dogs BSP graph](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/cdogs_bsp_graph.png)

Finishing touches like removed rooms, locked rooms where hidden objectives or powerups are placed, are then added.

![C-Dogs BSP demo](https://user-images.githubusercontent.com/1083215/108699978-154ff480-755a-11eb-9ea4-184aeab888ed.gif)

It's a simple and effective technique!

For more reading about this kind of technique, also visit [Mechanic #004 - Environment Tree](http://www.squidi.net/three/entry.php?id=4)
