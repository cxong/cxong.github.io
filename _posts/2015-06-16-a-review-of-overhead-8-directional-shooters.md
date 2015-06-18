---
layout: post
title: "A Review of Overhead 8-Directional Shooters"
date: 2015-06-16
comments: true
published: false
---

I'm a big believer in learning from others' examples, especially for games: to make better games, you can look for similar games to your own (and not just the same genre!), and see what worked and what didn't. The game I'm making is [C-Dogs SDL](cxong.github.io/cdogs-sdl/), an **overhead 8-directional shoot-em-up**. A while ago I [started looking for similar games](https://github.com/cxong/cdogs-sdl/issues/80), looking for cool features I can steal, but also looking for places where they weren't fun, and *why*. [**Bertram25**](https://github.com/Bertram25) (of [*Valyria Tear*](valyriatear.blogspot.com) and [*OpenDungeons*](http://opendungeons.github.io/)) encouraged me to elaborate on some of my conclusions in a blog post, so here it is :smile:!

## What are Overhead 8-Directional Shoot-em-ups?

TODO: 8-directional compass thingy

What a mouthful! It's a genre (or sub-genre) that doesn't get mentioned a lot. In a nutshell, it is where you can **move and shoot in 8 directions, from an overhead perspective**. Sounds awfully specific, and in practice people simply describe these games as *top-down shooters* or *2D shooters*, which lumps them together with other sub-genres like *twin-stick shooters* ([*Geometry Wars*](https://en.wikipedia.org/wiki/Geometry_Wars)), *scrolling shooters* ([*Gradius*](https://en.wikipedia.org/wiki/Gradius), most of the [*Touhou games*](https://en.wikipedia.org/wiki/Touhou_Project)), *run-and-guns* ([*Contra*](https://en.wikipedia.org/wiki/Contra_(video_game))), even games like [*Asteroids*](https://en.wikipedia.org/wiki/Asteroids_(video_game)) (whose sub-genre's name I don't know, but would include the [*Strike series*](https://en.wikipedia.org/wiki/Strike_series) or even the on-foot sections of [*2D GTA*](https://en.wikipedia.org/wiki/Grand_Theft_Auto_(video_game))). Fans of those sub-genres will understand how different they are; it's somewhat like lumping *Snakes and Ladders* with *Monopoly* together, because both are board games where pieces are moved using dice.

This is because *small differences in game mechanics can mean big changes in gameplay*. I think overhead 8-directional shoot-em-ups strikes a sweet balance between **movement** and **shooting** that creates an even mix of tactical play and arcade action. The 8 directions means some, but not complete, freedom in engaging enemies around you. As a player, you will:

1. **Move** into an ideal firing line
1. **Shoot** in one of the 8 directions

But also:

1. Make **tactical decisions** whether to stay back and shoot in one direction, or charge in and shoot in many directions
1. You can freely move to **dodge** incoming fire, but doing so will **affect your line of fire**

It is this close relation between moving and shooting, and limitations in both, that creates very dynamic gameplay. Great games in this genre understand this, and design the rest of the game to take advantage of this, from *map design*, to *weapons*, to *enemy AI*.

How exactly does this unique sub-genre affect game design? Let's compare with its sibling sub-genres and see:

- **Twin-stick shooters**: here you can aim in any direction, instead of only 8 directions. This means that movement is much less important, since you can shoot at any target from any position. The implication is, for 8-directionals, indirect-fire weapons like *shotguns* and *seeking weapons* are much more powerful. The limits in aiming also has an effect on map design; maps with walls that aren't in the 8 directions are more awkward for 8-directionals.
  TODO: crimsonland screenshot
  Because twin-stick shooters often use analog sticks for aiming, they are imprecise over long range, and often feature *auto-aim*. Some twin-stick shooters use the mouse to aim, which is extremely precise, and instead feature *recoil*. This means that twin-stick shooters' primary tactical consideration is *range*. For 8-directionals, there's a greater emphasis on *positioning*; range can also be a factor, but often produced by *projectile speed*. Recoil and auto-aim are less important.
- **Scrolling shooters**: only being able to shoot in one direction has a huge effect on game design. Map design is minimal; many scrolling shooters have no walls or obstacles at all. Instead, it's all about *enemy design*, including their *movement patterns*, *firing patterns* and so on. The challenge is to shoot at enemies moving and firing unpredictably before they overwhelm the player.
  TODO: smash tv screenshot
  A lot of 8-directionals go the tactical, emergent gameplay route, where AI is relatively simple and independent. This has its perks, for example you can play with crowd control with simple, predictable AI, but scrolling shooter's patterns have a lot to offer too. Bosses really benefit from complex firing patterns.
- **4-directional shooters**: the most similar to 8-directionals. What does the lack of diagonal directions mean? More movement, faster action, and enemies that can shoot in the 4 directions are much more dangerous. Weapons that can shoot diagonally or seek are much more powerful.
