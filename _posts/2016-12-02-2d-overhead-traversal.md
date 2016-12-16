---
layout: post
title: "2D Overhead Traversal"
date: 2016-12-02
comments: true
published: false
---

Why are open world games so fun? A lot of reasons: a huge, interesting world, lots of things to see and do. But one important mechanic that support this, and which pops up a lot when people talk about open world games, is **traversal**. What's that?

In a nutshell, it's the way the player moves around the world, getting from A to B. This sounds (and often is) mundane, which would be a problem for open world games with huge worlds, which is why these games often have *interesting*, *advanced techniques* to get around. You see this a lot on 3D open world games.

When it comes to *great traversal mechanics*, two games  often get mentioned: **Spiderman 2** and **Just Cause 2**. In the former, you use your web to swing around the city, and in the latter, a unique combination of paraglide and grappling hook lets you fly around quickly. Both take some skill to pick up, but the result is a fast and cool way to get around their game worlds.

> TODO: screenshots

Other games also get mentioned, but I've noticed that *they are all 3D games*, and the traversal mechanics described are *3D mechanics*. I've been thinking about how traversal might work in a [top-down 2D game](http://cxong.github.io/cdogs-sdl); a lot of the things that work in 3D simply aren't there. Like:

- **Great views**: open world games are fun because they have great scenery to enjoy. Many open world gamers have anecdotes of climbing up that big mountain to get a spectacular view, or seeing majestic buildings and landscapes in the distance. In a top-down 2D game this simply isn't possible.

  > TODO: screenshots

- **Vertical movement**: lots of traversal is about cool ways to navigate the environment, the vertical axis in particular. Jumping, climbing, spelunking, grappling, gliding, these are all things that are really awkward if not impossible to pull off in top-down 2D. Incidentally, these things are possible in 2D platformers, which is why the 2D platformer equivalent of open world games - *Metroidvania* - all feature novel movement mechanics, and not just the jump.

  > TODO: screenshots

- **An extra dimension for navigation**: seems obvious, but let's look at an example of a house. In 2D, usually you can just walk in, out, and around it. But in 3D, you could climb up the walls over it, jump off the roof to the ground, maybe go under it through a tunnel or basement, and so on. For multi-storey buildings or more complex architecture, 3D has even more options. You can fake these things in 2D but in 3D it is much more natural. This means that you can more easily pack in a very content-rich area in a small space, and have the player easily and quickly navigate it. Platforms, lifts, stairs, balconies, trap doors - all very easy to do.

  > TODO: screenshots, quake 2

So is it possible to create immersive, rich open worlds in 2D overhead, just like the 3D ones? If it's possible it's certainly a lot harder. Let's go back to first principles: *what makes traversal fun*? There's a great article called [*Traversal Level Design Principles*](http://www.gamasutra.com/blogs/TravisHoffstetter/20160107/263175/Traversal_Level_Design_Principles.php), which covers lots of the points:

- **Fun to get around**
  - **Interesting mechanics**: if getting around is trivial, it's not very interesting. But make it mechanically challenging, and getting around becomes a game of its own.
  - **Lots of ways to traverse**. Variety is the spice of life; if there's just one path from A to B then it's not very interesting. But what if there's a bunch of detours, shortcuts, maybe even secret paths? That's interesting.
  - **Make the journey interesting**. You know road trips? [Hours of driving through featureless terrain](https://en.wikipedia.org/wiki/Penn_%26_Teller's_Smoke_and_Mirrors#Desert_Bus) isn't most people's idea of fun. But what about a road trip with friends? It makes all the difference. As I've mentioned, 3D games make the journey interesting by having spectacular views, which is hard to pull off in 2D, but there are many other methods to try, like filler content (think about car radios, for example).
- **Fast travel**. Sometimes the trip is just too dull, and most players would rather skip the tedium. That's ok; having either instant travel or faster travel is a great way to skip the boring bits, [especially when you're backtracking](http://gamedev.stackexchange.com/q/83893/26250).

Once we start thinking about the principles behind traversal and what makes it fun, it's easy to see a lot of common techniques already in use, many of which are applicable to 2D overhead as well!

- **Vehicles**, which are both more challenging to use and faster than regular movement.

> TODO: screenshots, FF airships, GTA cars

- **Shortcuts**. Things like portals and secret passageways are already common in 2D overhead games. One very subtle yet clever implementation is the [ledges in Pokemon games](http://bulbapedia.bulbagarden.net/wiki/Ledge), which are one-way obstacles, strategically placed so that during your first trip you cannot pass through them, but on your way back you can jump over them. This removes the tedium of backtracking without compromising the experience when you are first exploring an area.

> TODO: screenshot pokemon ledge
