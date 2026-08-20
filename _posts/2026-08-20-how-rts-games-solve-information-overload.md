---
layout: post
title: How RTS Games Solve Information Overload
date: 2026-08-20
comments: true
published: true
---

![RTS UI collage](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rtsui.jpg)

For the past few years I've been working on [reverse engineering and remaking an almost 40 year old DOS game](https://congusbongus.itch.io/opencrystalcaves). Despite its age, I'm often surprised by the complexity and little tricks the game used, one of which is _sound priority_.

Here's the deal: the game, [_Crystal Caves_](https://en.wikipedia.org/wiki/Crystal_Caves), uses [PC speaker audio](https://en.wikipedia.org/wiki/PC_speaker), an extremely primitive, single-channel technology that was mostly used for simple beeps and boops. In practice this meant you could only play one sound at a time. So what happens if two sound-emitting events happen together, like jumping while a rocket hits an enemy?

Well, every sound in _Crystal Caves_ has a [priority field](https://moddingwiki.shikadi.net/wiki/Crystal_Caves_Sound_format), a number representing its relative importance. A sound will [interrupt another that's already playing](https://flukz.org/devlog/audio-mixing-voice-stealing-shmup/) only if its priority is higher. Simple and effective, and the player barely notices that only one sound is playing at a time.

Fast forward to 2006's _Company of Heroes_, an RTS that boasts 128 "voices" (depending on game settings), and many sound emitters: infantry rifle cracks, tracked vehicle rumbles, unit shouts, distant artillery rumbles, rocket screeches, all on top of music and UI noises. With dozens of units possible onscreen and more offscreen, this can easily become an overwhelming cacophony, and yet the game's audio is designed so that the player never misses the most important audio cues.

There's an entire field of study on how this is made possible.

<!--more-->

# The Bandwidth Limit

In 1956 [George Miller](https://en.wikipedia.org/wiki/George_Armitage_Miller), a founder of cognitive psychology, found that most people were "severely limited in terms of the amount of information \[they\] can receive, process, and remember". This includes responding to a number of different signals, or remembering a sequence. Around about 7, performance rapidly broke down. This was published in [_The Magical Number Seven, Plus or Minus Two_](https://en.wikipedia.org/wiki/The_Magical_Number_Seven,_Plus_or_Minus_Two), one of the most highly cited papers in psychology.

Now the limit wasn't absolute, and with training and mnemonic devices, [amazing feats of memorisation](https://en.wikipedia.org/wiki/World_Memory_Championships) are possible. But the fact that there's such a consistent range for untrained individuals (below which we use to [screen for cognitive impairments](https://knowyourmeme.com/memes/person-woman-man-camera-tv)), hints at a fundamental human cognitive limitation. We simply cannot simultaneously process too many pieces of information. When there are too many signals to react to, **prioritisation is key**, and choosing what _not_ to present is even more important.

> ![Eisenhower matrix](https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Eisenhower_matrix.svg/250px-Eisenhower_matrix.svg.png)
>
> The [Eisenhower matrix](https://en.wikipedia.org/wiki/Time_management#Eisenhower_method)'s ELIMINATE quadrant seems harsh but it is key, to allow one to focus on the important, urgent tasks.

# Information Overload

At 4:00 a.m. on March 28, 1979, feedwater pumps at the Three Mile Island nuclear power plant failed, the start of a series of failures that eventually led to the [Three Mile Island accident](https://en.wikipedia.org/wiki/Three_Mile_Island_accident), the worst accident in U.S. commercial nuclear power plant history. While the cause of the accident was ultimately due to multiple failures in a complex system, or what's termed a ["normal accident"](https://en.wikipedia.org/wiki/System_accident), there were key failures in the user interface that added to operator confusion and prevented a timely, effective response:

- Emergency pumps were working but operators did not notice that valves that would have let feedwater into the system were closed. One indicator light was "covered by a yellow maintenance tag", while the other was missed likely due to "[the operator's] own large belly [hiding] it from his view"
- The light indicating a key valve's status was labelled "Light on - RC-RV2 open", and when the light went out operators thought it meant the valve was closed. In fact it only indicated that the valve was powered, not that it was open.
- A downstream temperature indicator would have indicated a problem as well, but it wasn't considered important by the designers - it was effectively placed out of sight, behind the main instrument panel - and personnel were not trained to use it

That is, the problem wasn't that operators missed important information. The interface was so poorly designed, that the operators couldn't tell which were important.

> ![Three Mile Island control panels](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/3mi.jpg)
>
> https://www.wvia.org/news/pennsylvania-news/2024-10-29/nuclear-boosters-skeptics-eyeing-three-mile-island-restart

# How RTS Games Solve the Problem

RTS games are uniquely situated to tackle the information triage problem, as they combine the complexity of strategy games with the intensity of real-time action games: relevant information needs to be presented to the player promptly, from many sources, without overwhelming the player. At first glance the classic RTS UX seemingly hasn't changed a lot, but dig under the surface and there are numerous tweaks and developments made.

At the top level there's the minimap - a view of the entire battlespace at a glance, providing overview and context, with the main view focussing on a player-chosen area of the action. The interface is highly contextual - selecting different units presents different status info and unit-specific commands. Sometimes there's fixed HUD buttons for common, time-critical actions, such as selecting key units, building and training, or activating special abilities. This is all well and good - what's on screen is what the player is focused on, and therefore the most important - but a lot of key things happen off-screen, which would otherwise be easily missed. How do RTS games handle this?

<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_ping.jpeg"
    data-fancybox="gallery-rts"
    data-caption="Minimap pings show where the alert came from, giving the player context so they can focus on it when they are ready, without interrupting what the player is currently doing. These are often coupled with audio alerts and camera-jump shortcut so players can quickly react and focus on the alert">
![Minimap ping](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_ping_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_spacial.jpeg"
    data-fancybox="gallery-rts"
    data-caption="Adapted from FPS games, screen edge indicators show where an attack is coming from relative to the current viewport. This is less precise but allows rapid response, and helps the player maintain spacial awareness without having to glance at a minimap">
![Screen edge indicators](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_spacial_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_msg.jpeg"
    data-fancybox="gallery-rts"
    data-caption="Alerts that are not specific to a location can be indicated with a text notification. These form a first-in-first-out queue, useful for time-critical alerts">
![Notification messages](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_msg_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_superweapon.jpeg"
    data-fancybox="gallery-rts"
    data-caption="Some alerts are important but not time critical; these are shown as a persistent message so they can be acted upon at a later time">
![Persistent message](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_superweapon_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_coh.jpeg"
    data-fancybox="gallery-rts"
    data-caption="Games like Company of Heroes use a suite of audio techniques to provide additional context. Weapons like artillery sound different depending on whether they are on-screen or off-screen, and 3D audio allows players to estimate where they are coming from. Artillery also takes some time to land so the sound gives the player time to react effectively">
![Company of Heroes](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rts_coh_th.jpeg)
</a>

As a rough guide, RTS alerts follow these rules:

- Both important and urgent: audio+visual alerts (base under attack)
- Urgent but not important: audio only (unit completed)
- Important but not urgent: persistent visual (superweapon ready)

# How Not to Solve the Problem

We've shown how RTS games elegantly solve the information triage problem. You're probably familiar with how _not_ to solve this problem. Take a look at this:

![screenshot of phone with overwhelming notifications](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/phonenotifs.jpeg)

A sea of unopened notifications. How do you know which ones are important, which ones are urgent? You can't. This is because although the phone maker has designed the OS, no one has designed the entire ecosystem as a whole. As a result, every app developer is competing for your attention. An important work email needs to compete with dozens of other apps - games, social media, instant messaging, and so on - [for your engagement](https://en.wikipedia.org/wiki/Attention_economy). Each app maker tries to shout louder at you since it's in their best interest to get your attention, but when every app does the same, you - the user - lose, either by being overwhelmed, or being addicted to the phone. Hot take: we wouldn't need [digital detoxes](https://en.wikipedia.org/wiki/Digital_detox) at all if only these digital devices had well-designed information systems, that surface important information and suppress addiction mechanisms.

![Email inbox](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/emailinbox.png)

Speaking of email, it also has the same problem. Important emails compete with spammers, marketers and over-eager notifications, flooding your inbox with hundreds of emails a day. Methods like [Inbox Zero](https://www.techtarget.com/whatis/definition/inbox-zero) try to address this but still require work on your part, and in any case highlights that there's a problem. What makes the email situation pernicious is that many email senders are actively hostile, trying to spam or scam you, whereas apps are at worst parasites, who don't want to kill their host.

![Slack channels](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/blog-slack-triage-thumb.png)

But even if the message senders weren't actively malicious, the fact that the message content isn't under control still leads to information overload. Consider instant messaging like Slack. Over the years they've released numerous features to help you manage notifications: you can highlight or mute channels, mark certain users as VIP, temp mutes, per-channel notification settings, thread follow/unfollow, channel keywords, notification schedules and VIP overrides. It's great that Slack gives you such fine control, but you have to manually set this all up. Every additional setting makes the out-of-the-box experience worse. It would be great if there were some sort of algorithm that could manage it for you...

![Shrimp Jesus](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cc/Facebook_AI_slop%2C_%22Shrimp_Jesus%22_1.jpg/330px-Facebook_AI_slop%2C_%22Shrimp_Jesus%22_1.jpg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=thumbnail)

Speaking of algorithms, now we come to the worst offender of all: social media. Here we have the classic problem of numerous content creators adversarially competing for your attention, but most users can't be expected to fine tune their recommendations to the level of the average Slack user. Typically you would subscribe to certain topics or creators, but this system is imperfect: in addition to the overload problem (if you're subscribed to too many things), there's the discoverability problem (if you're not subscribed to things that would interest you). To tackle this, social media platforms deploy sophisticated algorithms to show you a personalised feed, using as many signals as they can get their grubby hands on: what you've seen (and how long) and interacted with (likes, comments), subtle signals like view and pause time, your demographic, interests, followed/followers, DMs, even your interactions off-site.

Now that alone might work well (and is a bit creepy), but the real kicker is that the algorithm isn't on your side; it's there to keep you engaged. Even if you get addicted, even if it makes you miserable, even if it leads to [all sorts of real-life evils](https://en.wikipedia.org/wiki/Criticism_of_Facebook). For this reason, there's a small but growing [movement away from algorithmic control](https://collaborate.princeton.edu/en/publications/understanding-decentralized-social-feed-curation-on-mastodon/).

# Take-Aways

The reason why RTS games can solve information overload so well is because it has complete control over the ecosystem (everything that happens is within the game, under the control of the game designers), whereas other platforms may not have that luxury. Putting this together:

| Platform            | Problem                                         | RTS games are better because             |
| ------------------- | ----------------------------------------------- | ---------------------------------------- |
| Phone notifications | Prioritisation between different sources (apps) | No competition between different sources |
| Email               | Adversarial messages                            | Nothing is adversarial                   |
| IM                  | Unpredictable message importance                | Deterministic message importance         |
| Social Media        | Optimising for engagement                       | Optimising for player enjoyment          |

So the next time you build an information platform - a dashboard, UI, message feed, or what have you - keep this in mind:

- Determine which are important, which are urgent, both, or neither
- Prioritise! Make sure the messages that are important and/or urgent are never hidden by those that are not
- Beware of unpredictable message importance/urgency. Things could be unpredictable if they are user-generated, randomly-generated, or highly contextual
- Guard against adversarial messages (e.g. users who are spammers)
- Last but not least, make sure it serves your users' interest!
