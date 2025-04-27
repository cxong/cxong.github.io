---
layout: post
title: "2D Overhead Traversal"
date: 2016-12-02
comments: true
published: true
---

Why are open world games so fun? A lot of reasons: a huge, interesting world, lots of things to see and do. But one important mechanic that support this, and which pops up a lot when people talk about open world games, is **traversal**. What's that?

In a nutshell, it's the way the player moves around the world, getting from A to B. This sounds (and often is) mundane, which would be a problem for open world games with huge worlds, which is why these games often have _interesting_, _advanced techniques_ to get around. You see this a lot on 3D open world games.

When it comes to _great traversal mechanics_, two games often get mentioned: **Spiderman 2** and **Just Cause 2**. In the former, you use your web to swing around the city, and in the latter, a unique combination of paraglide and grappling hook lets you fly around quickly. Both take some skill to pick up, but the result is a fast and cool way to get around their game worlds.

> ![spiderman 2](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/spiderman2.jpg)![just cause 2](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/justcause2.jpg)

Other games also get mentioned, but I've noticed that _they are all 3D games_, and the traversal mechanics described are _3D mechanics_. I've been thinking about how traversal might work in a [top-down 2D game](http://cxong.github.io/cdogs-sdl); a lot of the things that work in 3D simply aren't there. Like:

- **Great views**: open world games are fun because they have great scenery to enjoy. Many open world gamers have anecdotes of climbing up that big mountain to get a spectacular view, or seeing majestic buildings and landscapes in the distance. In a top-down 2D game this simply isn't possible.

  > ![oblivion](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/oblivion.jpg)![arkham knight](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/arkhamknight.jpeg)

  <!--more-->

- **Vertical movement**: lots of traversal is about cool ways to navigate the environment, the vertical axis in particular. Jumping, climbing, spelunking, grappling, gliding, these are all things that are really awkward if not impossible to pull off in top-down 2D. Incidentally, these things are possible in 2D platformers, which is why the 2D platformer equivalent of open world games - _Metroidvania_ - all feature novel movement mechanics, and not just the jump.

  > ![metroid bomb jump](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/metroid_bombjump.jpg)![worms ninja rope](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/worms_ninja_rope.png)

- **An extra dimension for navigation**: seems obvious, but let's look at an example of a house. In 2D, usually you can just walk in, out, and around it. But in 3D, you could climb up the walls over it, jump off the roof to the ground, maybe go under it through a tunnel or basement, and so on. For multi-storey buildings or more complex architecture, 3D has even more options. You can fake these things in 2D but in 3D it is much more natural. This means that you can more easily pack in a very content-rich area in a small space, and have the player easily and quickly navigate it. Platforms, lifts, stairs, balconies, trap doors - all very easy to do.

  > ![quake 2](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/quake2.jpg)![minecraft caves](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/minecraft_caves.jpg)

So is it possible to create immersive, rich open worlds in 2D overhead, just like the 3D ones? If it's possible it's certainly a lot harder. Let's go back to first principles: _what makes traversal fun_? There's a great article called [_Traversal Level Design Principles_](http://www.gamasutra.com/blogs/TravisHoffstetter/20160107/263175/Traversal_Level_Design_Principles.php), which covers lots of the points:

- **Fun to get around**
  - **Interesting mechanics**: if getting around is trivial, it's not very interesting. But make it mechanically challenging, and getting around becomes a game of its own.
  - **Lots of ways to traverse**. Variety is the spice of life; if there's just one path from A to B then it's not very interesting. But what if there's a bunch of detours, shortcuts, maybe even secret paths? That's interesting.
  - **Make the journey interesting**. You know road trips? [Hours of driving through featureless terrain](https://en.wikipedia.org/wiki/Penn_%26_Teller's_Smoke_and_Mirrors#Desert_Bus) isn't most people's idea of fun. But what about a road trip with friends? It makes all the difference. As I've mentioned, 3D games make the journey interesting by having spectacular views, which is hard to pull off in 2D, but there are many other methods to try, like filler content (think about car radios, for example).
- **Fast travel**. Sometimes the trip is just too dull, and most players would rather skip the tedium. That's ok; having either instant travel or faster travel is a great way to skip the boring bits, [especially when you're backtracking](http://gamedev.stackexchange.com/q/83893/26250).

Once we start thinking about the principles behind traversal and what makes it fun, it's easy to see a lot of common techniques already in use, many of which are applicable to 2D overhead as well!

- **Vehicles**, which are both more challenging to use and faster than regular movement.

> ![final fantasy airships](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/final_fantasy_airships.png)![gta](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/gta.jpg)

- **Shortcuts**. Things like portals and secret passageways are already common in 2D overhead games. One very subtle yet clever implementation is the [ledges in Pokemon games](http://bulbapedia.bulbagarden.net/wiki/Ledge), which are one-way obstacles, strategically placed so that during your first trip you cannot pass through them, but on your way back you can jump over them. This removes the tedium of backtracking without compromising the experience when you are first exploring an area.

> ![pokemon ledge](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon_ledge.png)

- **Multi-storey Levels**. 2D overhead can do multi-storey architecture, even though it doesn't do it quite as well. Still, it's a great way to pack lots of content in a limited amount of space, which makes it very useful for 2D overhead where the viewport is constrained. Separate storeys can be linked with portal techniques disguised as stairs, elevators or sometimes even holes.

> ![earthbound stairs](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/earthbound_stairs.png)![figaro castle](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/figaro_castle.png)

- [**Overworld**](https://en.wikipedia.org/wiki/Overworld). 2D overhead games have actually portrayed huge worlds for a long time, using an old trick: the overworld. That is, when travelling between key locations, the game scales all the way out, representing vast distances in a small space. The player gets a sense of the size of the world, even though it's smoke-and-mirrors, and very little of that world is actually fleshed out. A very well established hack!

> ![ultima overworld](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ultima_overworld.png)![final fantasy overworld](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/final_fantasy_overworld.png)![chrono trigger overworld](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/chrono_trigger_overworld.png)

- **Signposts**. One of the most un-fun ways to traverse is when you are lost, so signposts help prevent that. Not just literal signposts though; in Final Fantasy 6, [Game Design Forum's Reverse Design](http://thegamedesignforum.com/features/reverse_design_ff6_5.html) shows how the game cleverly uses its NPCs to give direct, subtle, even ironic directions to its game world and plot. It also helps engender a [sense of place](http://venturebeat.com/community/2012/05/30/games-need-more-place/) - the sense that this place is a living, breathing and self-consistent entity which has complex relations between itself and the player.

> ![pokemon signposts](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon_signpost.png)![final fantasy 6 NPC directions](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/final_fantasy_6_allusion.png)

- **Traversal tools**. Who says 2D overhead games can't have awesome traversal tools? It's not common but there are examples of special tools that are either challenging to use or get the player to inaccessible places. Adding places that are out-of-the-way, hard to reach makes it all the more rewarding to actually get there, and makes it all the more fun to explore the world.

> ![zelda hookshot](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/zelda_hookshot.png)![pokemon acro bike](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon_acro_bike.png)![chocobo in shallows](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/final_fantasy_chocobo.jpg)

With all these techniques, it should be possible to create open-world 2D overhead games with great traversal mechanics. As I've said before, it always pays to study how games have approached these design problems, and it really helps you make better games!
