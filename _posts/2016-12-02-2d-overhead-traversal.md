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
