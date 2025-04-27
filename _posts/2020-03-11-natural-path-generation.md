---
layout: post
title: "Natural Path Generation"
date: 2020-03-11
comments: true
published: true
---

Random level generators are great fun to make; there's nothing quite like coding an algorithm that creates endless variations of maps and dungeons.

A typical random map generator might place rooms randomly around the place and connect them with corridors. Then the map might be filled randomly with inhabitants - monsters, treasure, NPCs and so on. This is simple and effective, giving players unpredictable yet interesting encounters in games. It's an evergreen approach starting from [rogue (1980)](<https://en.wikipedia.org/wiki/Rogue_(video_game)>) all the way up to the latest indie dungeon crawlers.

[![Rooms and Mazes](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rooms_and_mazes.gif)](http://journal.stuffwithstuff.com/2014/12/21/rooms-and-mazes/)

This can seem backwards though. One problem is that the layout often seems artificial; there's not much reason or purpose for the rooms and the connecting corridors. Real locales would be filled with inhabitants, with paths connecting important destinations together. The paths are like arteries; they are inextricably linked to the design of the whole place.

So I thought a fun experiment would be to make a random level generator that builds such a map via simulation: fill it with virtual inhabitants, who need to go from A to B, find out what paths they need via pathfinding, and create the paths based on travel patterns. Let's see how this goes!

First, I start with a simple "village" generator - just a bunch of buildings scattered randomly around the place.

> ![village](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village.png)

<!--more-->

Before we place paths to connect these buildings, we need to think about how these buildings will be used. Some - shops, inns - will be more important than others - private residences. Let's express that by making some buildings important, giving them a different appearance, and populating them with more NPCs.

> ![village with NPCs](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village_npc.png)

Now to connect the buildings, by taking random pairs of them, then using pathfinding to draw a path between each pair, with two conditions:

- the more important the building, the more we use it as a path destination;
- make sure all buildings have at least one path

> ![village with paths](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village_paths.png)

This seems ok but now the village is overrun with paths. Some are obviously more well travelled than others. What if we showed that by using different tile types? From tree (no wear), grass (light wear), dirt road (moderate wear), stone road (heavy wear):

> ![village with varied paths](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village_varied_paths.png)

Now it's starting to look nice! But there are still a few problems: there's a lot of grass, representing lightly travelled paths, and odd patches of stone/dirt roads, right next to each other.

It turns out we could make one more improvement: when there's an existing path, it would make more sense to reuse it, even if it's slightly out of the way, rather than cutting through untravelled roads. This makes sense and it's what real travellers do. So let's modify our pathfinder, so that it favours well-travelled tiles, and see what we get:

> ![village with shared paths](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village_shared.png)

Nice! Now we see some clear heavily-travelled avenues. By observing the paths, we can also make sense of where the important locations are. Cool huh?

You can find this map generator here: <https://github.com/cxong/gomapgen> under the `village` option. It's also where I make lots of different map generators for fun.

Hope you enjoy!

> ![village animation](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/village.gif)
