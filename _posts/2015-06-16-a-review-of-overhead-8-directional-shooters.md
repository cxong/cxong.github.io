---
layout: post
title: "A Review of Overhead 8-Directional Shooters"
date: 2015-06-16
comments: true
published: false
---

To make better games, one can look for similar games (not only in the same genre), and see what worked and what didn't. One game I'm making is [C-Dogs SDL](cxong.github.io/cdogs-sdl/), an **overhead 8-directional shoot-em-up**. A while ago I [started looking for similar games](https://github.com/cxong/cdogs-sdl/issues/80), looking for cool features I can steal, but also for where they weren't fun, and *why*. [**Bertram25**](https://github.com/Bertram25) (of [*Valyria Tear*](valyriatear.blogspot.com) and [*OpenDungeons*](http://opendungeons.github.io/)) encouraged me to elaborate on some of my conclusions in a blog post, so here it is :smile:!

## What are Overhead 8-Directional Shoot-em-ups?

TODO: 8-directional compass thingy

This mouthful of a sub-genre doesn't get mentioned a lot. In a nutshell, it's where you can **move and shoot in 8 directions, from an overhead perspective**. Sounds awfully specific, so people simply describe these games as *top-down shooters* or *2D shooters*, which lumps them together with other sub-genres like *twin-stick shooters* ([*Geometry Wars*](https://en.wikipedia.org/wiki/Geometry_Wars)), *scrolling shooters* ([*Gradius*](https://en.wikipedia.org/wiki/Gradius), most of the [*Touhou games*](https://en.wikipedia.org/wiki/Touhou_Project)), *run-and-guns* ([*Contra*](https://en.wikipedia.org/wiki/Contra_(video_game))), even games like [*Asteroids*](https://en.wikipedia.org/wiki/Asteroids_(video_game)) (which have tank-controls, and includes the [*Strike series*](https://en.wikipedia.org/wiki/Strike_series) or even the on-foot sections of [*2D GTA*](https://en.wikipedia.org/wiki/Grand_Theft_Auto_(video_game))). Fans of those sub-genres will understand how different they are; each has different design lessons to learn.

*Small differences in game mechanics can mean big changes in gameplay*. I think overhead 8-directional shoot-em-ups strikes a sweet balance between **movement** and **shooting**, between tactical play and arcade action. The 8 directions means some, but not complete, freedom in engaging enemies around you. As a player, you will:

1. **Move** into an ideal firing line
1. **Shoot** in one of the 8 directions

But also:

1. Make **tactical decisions** whether to stay back and shoot in one direction, or charge in and shoot in many directions
1. You can freely move to **dodge** incoming fire, but doing so will **affect your line of fire**

It is this close relation between moving and shooting, and limitations in both, that creates very dynamic gameplay. Great games in this sub-genre understand this, and design accordingly: *map design*, to *weapons*, to *enemy AI*. Let's compare with its sibling sub-genres:

- **Twin-stick shooters**: here you can aim in any direction, not just 8. Movement is much less important, since you can shoot at any target from any position. The implication is, for 8-directionals, indirect-fire weapons like *shotguns* and *seeking weapons* are much more powerful. The limits in aiming also affects map design; maps with walls that aren't in the 8 directions are more awkward for 8-directionals.
  TODO: crimsonland screenshot
  Because twin-stick shooters often use analog sticks for aiming, they are imprecise over long range, and often feature *auto-aim*. Some twin-stick shooters use the mouse to aim, which is extremely precise, and instead feature *recoil*. This means that twin-stick shooters' primary tactical consideration is *range*. For 8-directionals, there's a greater emphasis on *positioning*; range can also be a factor, but often produced by *projectile speed*. Recoil and auto-aim are less important.
- **Scrolling shooters**: only being able to shoot in one direction has a huge effect on game design. Map design is minimal; many scrolling shooters have no walls or obstacles at all. Instead, it's all about *enemy design*, including their *movement patterns*, *firing patterns* and so on. The challenge is to shoot at enemies moving and firing unpredictably before they overwhelm the player.
  TODO: xevious screenshot
  A lot of 8-directionals go the tactical, emergent gameplay route, where AI is relatively simple and independent. This has its perks, for example you can play with crowd control with simple, predictable AI, but scrolling shooter's patterns have a lot to offer too. Bosses really benefit from complex firing patterns.
- **4-directional shooters**: the most similar to 8-directionals. What does the lack of diagonal directions mean? More movement, faster action, and enemies that can shoot in the 4 directions are much more dangerous. Weapons that can shoot diagonally or seek are much more powerful.

## Super Contra and Jackal

TODO: screenshots

This duo of Konami-made classic NES games share many similarities, and are distinctive, quality entries in the subgenre. Not only are these games heaps of fun, they are also super polished, with **great music** as evidenced in the covers and remixes for Konami games in general.

These games really do a lot with the subgenre, with a great variety in enemies, powerups and weapons:

- Enemies include weak-and-slow infantry (that, in Jackal, can be run over!), fixed turrets, vehicles of various speeds and strength, even fixed-path planes. This gives the player a lot of **choice in how to engage**. The action is frantic so making these choices really puts pressure on the player.
- The weapons that both you and the enemies use are interesting. There are slow-moving but accurate bullets, faster but fixed-axis bullets, indirect-fire grenades, spread shots, even homing missiles. Some of these **keep you away**, some **keep you moving**, some force you to **stop and evade**. The games are at their hardest when **multiple bullet types are in play**, where multiple bullets of different types can conspire together to kill you off.

One downside, especially compared to their contemporaries, is that the pace is *slow*. Since both games have 1-hit-kills, stray bullets often send the player running in the opposite direction. Two possible improvements are: auto scroll, and removing 1-hit-kills.

## Crimsonland

TODO: screenshots

Coming after an era of gory shooters, Crimsonland plays like an unpretentious distillation of late-90's game design sensibilities. It's a twin-stick shooter with tons of everything: weapons, powerups, simple swarm enemies, an interesting perk system, and lots of blood decals. It's great fun and uneven too, and it offers plenty of lessons:

- Overhead shooters are **fun**! The huge range of weapons, explosions and sounds make shooting endless zombies satisfying, all the time.
- There are so many weapons and they are unique. From the standard shotguns and machine guns, to rockets with explosions, homing weapons, piercing weapons, even ones that bounce around. Crimsonland proves that 2D shooters have the prettiest and most interesting weapons, because you can see and appreciate all the bullet patterns. Balance is very poor though.
- The powerups, even though they are even more unbalanced than the weapons, are lots of fun, and are at the core of its gameplay. Once players have mastered the basic game, it becomes more about desperately negotiating overwhelming swarms of enemies to get to crucial, game-changing powerups, only to die inches from them. Critics say this makes the game luck-based, but there's no denying its excitement.
- Unfortunately, the game is severely lacking in content. Its huge range of weapons, powerups, perks and enemies serves as its content, via its quest mode, and while that's lots of fun, after the whole game is unlocked there's not much else to do. To me this proves that there's only so much you can do with shooting things in an open arena; you really need **content** in the form of **maps** to create interesting spaces for unique gameplay.

Ultimately, I think Crimsonland is a great case-study on how **less-is-more**, at least for balance. There are so many weapons, powerups, perks and enemies that balance is simply impossible. Games that don't rely on the number of weapons for content would do well with less, if they want to be balanced, for example. One type of game that thrives on variety however is roguelikes, and sadly Crimsonland missed this boat on becoming a game like *Binding of Isaac* or *Nuclear Throne*.
