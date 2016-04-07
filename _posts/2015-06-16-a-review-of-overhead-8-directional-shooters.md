---
layout: post
title: "A Review of Overhead 8-Directional Shooters"
date: 2016-04-07
comments: true
published: true
---

To make better games, one can look for similar games (not only in the same genre), and see what worked and what didn't. One game I'm making is [C-Dogs SDL](cxong.github.io/cdogs-sdl/), an **overhead 8-directional shoot-em-up**. A while ago I [started looking for similar games](https://github.com/cxong/cdogs-sdl/issues/80), looking for cool features I can steal, but also for where they weren't fun, and *why*. [**Bertram25**](https://github.com/Bertram25) (of [*Valyria Tear*](valyriatear.blogspot.com) and [*OpenDungeons*](http://opendungeons.github.io/)) encouraged me to elaborate on some of my conclusions in a blog post, so here it is :smile:!

## What are Overhead 8-Directional Shoot-em-ups?

> ![8-way](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/8-way.png)

This mouthful of a sub-genre doesn't get mentioned a lot. In a nutshell, it's where you can **move and shoot in 8 directions, from an overhead perspective**. Sounds awfully specific, so people simply describe these games as *top-down shooters* or *2D shooters*, which lumps them together with other sub-genres like *twin-stick shooters* ([*Geometry Wars*](https://en.wikipedia.org/wiki/Geometry_Wars)), *scrolling shooters* ([*Gradius*](https://en.wikipedia.org/wiki/Gradius), most of the [*Touhou games*](https://en.wikipedia.org/wiki/Touhou_Project)), *run-and-guns* ([*Contra*](https://en.wikipedia.org/wiki/Contra_(video_game))), even games like [*Asteroids*](https://en.wikipedia.org/wiki/Asteroids_(video_game)) (which have tank-controls, and includes the [*Strike series*](https://en.wikipedia.org/wiki/Strike_series) or even the on-foot sections of [*2D GTA*](https://en.wikipedia.org/wiki/Grand_Theft_Auto_(video_game))). Fans of those sub-genres will understand how different they are; each has different design lessons to learn.

*Small differences in game mechanics can mean big changes in gameplay*. I think overhead 8-directional shoot-em-ups strikes a sweet balance between **movement** and **shooting**, between tactical play and arcade action. The 8 directions means some, but not complete, freedom in engaging enemies around you. As a player, you will:

1. **Move** into an ideal firing line
1. **Shoot** in one of the 8 directions

But also:

1. Make **tactical decisions** whether to stay back and shoot in one direction, or charge in and shoot in many directions
1. You can freely move to **dodge** incoming fire, but doing so will **affect your line of fire**

It is this close relation between moving and shooting, and limitations in both, that creates very dynamic gameplay. Great games in this sub-genre understand this, and design accordingly: *map design*, to *weapons*, to *enemy AI*. Let's compare with its sibling sub-genres:

- **Twin-stick shooters**: here you can aim in any direction, not just 8. Movement is much less important, since you can shoot at any target from any position. The implication is, for 8-directionals, indirect-fire weapons like *shotguns* and *seeking weapons* are much more powerful. The limits in aiming also affects map design; maps with walls that aren't in the 8 directions are more awkward for 8-directionals.

  > ![crimsonland](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/crimsonland.png)

  Because twin-stick shooters often use analog sticks for aiming, they are imprecise over long range, and often feature *auto-aim*. Some twin-stick shooters use the mouse to aim, which is extremely precise, and instead feature *recoil*. This means that twin-stick shooters' primary tactical consideration is *range*. For 8-directionals, there's a greater emphasis on *positioning*; range can also be a factor, but often produced by *projectile speed*. Recoil and auto-aim are less important.
- **Scrolling shooters**: only being able to shoot in one direction has a huge effect on game design. Map design is minimal; many scrolling shooters have no walls or obstacles at all. Instead, it's all about *enemy design*, including their *movement patterns*, *firing patterns* and so on. The challenge is to shoot at enemies moving and firing unpredictably before they overwhelm the player.

  > ![xevious](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/xevious.gif)
  
  A lot of 8-directionals go the tactical, emergent gameplay route, where AI is relatively simple and independent. This has its perks, for example you can play with crowd control with simple, predictable AI, but scrolling shooter's patterns have a lot to offer too. Bosses really benefit from complex firing patterns.
- **4-directional shooters**: the most similar to 8-directionals. What does the lack of diagonal directions mean? More movement, faster action, and enemies that can shoot in the 4 directions are much more dangerous. Weapons that can shoot diagonally or seek are much more powerful.

## Early arcade/console games

Overhead shooters have a long heritage; one of the first arcade games ever, [Gun Fight](http://www.arcade-museum.com/game_detail.php?game_id=8039), had players duelling with a two-stick control scheme - one to move, the other to aim and shoot. Through the 80's game makers added features - powerups, different weapons - and tweaked game mechanics, learning valuable design lessons.

### [Front Line](http://www.mobygames.com/game/front-line)

> ![Front Line](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/front_line.png)

An early Taito game, this is a really underrated one with some neat ideas. You play as a soldier who can shoot a gun or throw grenades, the animations are hilarious, and you can even drive tanks! Nevertheless, it has significant flaws too:

- Bullets come out of your gun barrel on your right hand, which makes sense but makes aiming really hard, especially since enemies can come from all around
- Enemies are really hard to pre-empt. This is long before game designers learned to use [antics](http://johnkstuff.blogspot.com.au/2009/02/anticipations.html). Instead, the enemy AI literally performs actions at random, including shooting at you.
- There's not enough meaningful difference between the gun and grenade; most of the time they are both useful. I think shmups with their screen-clearing "bombs" got it right.
 
Some of these flaws may be intentional, given that it's a quarter-munching game at heart. It seems that the arcade version is much more superior to the NES port. The pacing in the NES port is really slow too.

### [Super Contra](http://contra.kontek.net/games/supercnes/supercnes.htm) and [Jackal](http://www.hardcoregaming101.net/jackal/jackal.htm)

> ![Super Contra](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/super_contra.png)
> ![Jackal](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/jackal.png)

This duo of Konami-made classic NES games share many similarities, and are distinctive, quality entries in the subgenre. Not only are these games heaps of fun, they are also super polished, with **great music** as evidenced in the covers and remixes for Konami games in general.

These games really do a lot with the subgenre, with a great variety in enemies, powerups and weapons:

- Enemies include weak-and-slow infantry (that, in Jackal, can be run over!), fixed turrets, vehicles of various speeds and strength, even fixed-path planes. This gives the player a lot of **choice in how to engage**. The action is frantic so making these choices really puts pressure on the player.
- The weapons that both you and the enemies use are interesting. There are slow-moving but accurate bullets, faster but fixed-axis bullets, indirect-fire grenades, spread shots, even homing missiles. Some of these **keep you away**, some **keep you moving**, some force you to **stop and evade**. The games are at their hardest when **multiple bullet types are in play**, where their combination is much more lethal.

One downside, especially compared to their contemporaries, is that the pace is *slow*. Since both games have 1-hit-kills, stray bullets often send the player running in the opposite direction. Two possible improvements are: auto scroll, and removing 1-hit-kills.

Another significant flaw is that your player is quite close to the direction of scrolling, making you vulnerable to new enemies that appear suddenly. This is especially a problem in Jackal. Perhaps this is due to the arcade heritage (cheap, sudden deaths means more quarters), or to the NES's low resolution.

### [Heavy Barrel](http://videogamecritic.com/nesfh.htm)

> ![Heavy Barrel](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/heavy_barrel.png)

A late NES game, less well known but not for its quality, because it's really awesome. Coming after seminal titles like the aforementioned Konami games and the influential [Commando](https://en.wikipedia.org/wiki/Commando_(video_game)), Heavy Barrel benefited from the design lessons from those games. As a result this game sports many cool and powerful weapons, virtually all accessible in the first level. In fact the first level is a real tour-de-force demonstration of how awesome shooters can be.

- Less than half a minute into the first level, you are accosted by two enemies: fixed machine gunners and fast-running soldiers. This sets up an interesting tactical challenge, as the machine gunners **zone you out**, whereas the fast runners can **approach and threaten you**. There are at least two ways to deal with this: quickly take out the machine gunners so you have space to evade the runners, or patiently take out the runners while staying out of the machine gunners' zones.
- All weapon pickups in the game (including grenades, which are cool in theory but overshadowed by the main weapons) have a fixed amount of ammo (think Metal Slug). It's an effective system that discourages player spamming, and keeps them moving with the promise of more ammo.

### [Mercs](https://en.wikipedia.org/wiki/Mercs)

> ![Mercs](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/mercs.png)

This game is basically a more polished version of the earlier Commando game (and similar ones like Ikari Warriors and Gun.Smoke). As a result it's pretty straightforward and repetitive: lots of enemies, lots of shooting. A few points are worth mentioning:

- 3 player co-op. Shooters, especially multi-directional ones, are great for co-op because you can help each other out by shooting at enemies threatening the other players - that's more ways to interact and co-op.
- Lots of enemies use grenades. Grenades are interesting weapons - because they take time to land and explode, they give the player a bit of time to react thoughtfully, keeping them on the move and the pace of the game up.

## 90's Innovation

Overhead shooters really blossomed in this era. Enabled by technical advancements and more discerning players, game makers looked for all kinds of ways to enhance shooters, taking ideas from other genres and games, as well as simply adding more polish to what's become an established genre.

Meanwhile in PC land, shooters saw lots of innovation from diverse game makers. Not only were these shooters creative, many were made with loving care; games like C-Dogs and its ilk were made by people who grew up with and genuinely adored these games.

### [Smash TV](http://www.mobygames.com/game/smash-tv)

> ![Smash TV](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smash_tv.png)

Perhaps the quintessential 8-directional twin-stick shooter; this enhanced remake of Robotron: 2084 distils everything great about overhead shooters into a no-nonsense, crazy-hectic arena shooter with a fantastically-absurd premise. Shoot endless hordes of enemies, get big powerups, fight ridiculous bosses, collect unending piles of cash. It's simple and unsophisticated: the weapon selection is pretty standard, the enemies even more so - there are ones that run towards you, ones that run towards you faster, some that occasionally shoot you, others that run towards you in funny patterns.

Unfortunately the game suffers from a big flaw: **uneven pacing**. In between the ceaseless enemies and unpredictable powerups, it's very hard to control difficulty and player experience. Sometimes normal levels with unfortunate powerup placement can be way more brutal than boss fights. This is a problem we'll see again in a closely related game: Crimsonland. I think the game could really benefit from something like the [AI Director](http://left4dead.wikia.com/wiki/The_Director); unfortunately this wouldn't be developed until a decade later.

### [Tapan Kaikki](http://everything2.com/title/Tapan+Kaikki) + [Assault Trooper](http://www.abandonia.com/games/486)

> ![Tapan Kaikki](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tapan_kaikki.jpg)
> ![Assault Trooper](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/assault_trooper.png)

These two games share more than a few things in common. They were both made by Finns, were released around the same time (1995, 1997), have tank controls, and are chock full of 90's shooter goodies. Tapan Kaikki has some of the most elaborate gore effects of any game: enemies explode in gibs, which leave blood trails, which you can kick (and leave more blood trails), and did I mention you can get your feet covered and leave bloody footprints? Assault Trooper on the other hand is full of interactivity and cool ideas; everything's destructible, even the trees and walls. Both are very interesting examples to study.

Both games are unfortunately hampered by their tank controls - that is, players mainly move forward and rotate via keyboard controls. Both have strafing functions but they are quite awkward to use. Like other games with tank controls, **aiming, especially at far targets, is challenging**. **Navigating twisty passages is likewise difficult**. Both games feature lots of tight, indoor areas which are bad with tank controls; I remember dying endlessly in Assault Trooper because my grenade didn't go where I wanted it to, and bounced back from a corner. My opinion is that tank controls should be avoided in indoor, fast-paced shooters for these reasons.

But don't let that colour your perception of these games; they are flawed gems that are seriously underappreciated.

### [Strike Series](http://www.mobygames.com/game-group/electronic-arts-strike-series) + [Fire Fight](http://www.old-games.com/download/2146/fire-fight)

> ![Strike Series](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/strike.gif)
> ![Fire Fight](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/fire_fight.jpg)

Compared to the last two games, these adapt well to tank controls. Recall that the two problems with tank controls are **moving around in tight spaces** and **aiming at far targets**. Both are about flying aircraft in wide-open spaces, rather than tight indoors. Both also solve the problem of low accuracy with interesting weapons and mechanics. In Strike's case, there is a limited amount of **auto-aim**, which is cleverly explaned as having a "gunner". In Fire Fight, there's the cool "swarmer" weapon which fires a spread salvo of **homing missiles**.

Strike also has the interesting fuel mechanic, which is basically a draining health meter and you must scour the map for extra fuel to stay alive. It's a good way of countering an otherwise slow-paced game, but this sort of [resource mechanic has its problems too](http://cxong.github.io/2015/05/ammo-is-a-resource).

### [Crimsonland](http://www.crimsonland.com/)

> ![Crimsonland](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/crimsonland_large.png)

Coming after an era of gory shooters, Crimsonland plays like an unpretentious distillation of late-90's game design sensibilities. It's a twin-stick shooter with tons of everything: weapons, powerups, simple swarm enemies, an interesting perk system, and lots of blood decals. It's great fun and uneven too, and it offers plenty of lessons:

- Overhead shooters are **fun**! The huge range of weapons, explosions and sounds make shooting endless zombies satisfying, all the time.
- There are so many weapons and they are unique. From the standard shotguns and machine guns, to rockets with explosions, homing weapons, piercing weapons, even ones that bounce around. Crimsonland proves that 2D shooters have the prettiest and most interesting weapons, because you can see and appreciate all the bullet patterns. Balance is very poor though.
- The powerups, even though they are even more unbalanced than the weapons, are lots of fun, and are at the core of its gameplay. Once players have mastered the basic game, it becomes more about desperately negotiating overwhelming swarms of enemies to get to crucial, game-changing powerups, only to die inches from them. Critics say this makes the game luck-based, but there's no denying its excitement.
- Unfortunately, the game is severely lacking in content. Its huge range of weapons, powerups, perks and enemies serves as its content, via its quest mode, and while that's lots of fun, after the whole game is unlocked there's not much else to do. To me this proves that there's only so much you can do with shooting things in an open arena; you really need **content** in the form of **maps** to create interesting spaces for unique gameplay.

Ultimately, I think Crimsonland is a great case-study on how **less-is-more**, at least for balance. There are so many weapons, powerups, perks and enemies that balance is simply impossible. Games that don't rely on the number of weapons for content would do well with less, if they want to be balanced, for example. One type of game that thrives on variety however is roguelikes, and sadly Crimsonland missed this boat on becoming a game like *Binding of Isaac* or *Nuclear Throne*.

## Modern Overhead Shooters

The core design of overhead shooters has been rather stagnant after the 90's. There has been a lot of innovation at the fringes, like cinematic plots, but the basic mechanics are much the same. Titles like [*Alien Shooter*](http://www.mobygames.com/game-group/alien-shooter-series), [*Shadowgrounds*](https://en.wikipedia.org/wiki/Shadowgrounds_(series)), and the recent [*Helldivers*](http://arrowheadgamestudios.com/games/helldivers/) are all great, polished games, but their gameplay is often considered "retro", and in many ways are less ambitious in their design as some of the creative entries from the 90's.

### [Binding of Isaac](http://bindingofisaac.com/) + [Nuclear Throne](http://nuclearthrone.com/)

> ![Binding of Isaac](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/boi.png)
> ![Nuclear Throne](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/nuclear_throne.png)

One exception is the games that marry overhead shooting action within a rogue-like framework. Exemplified by Binding of Isaac, but in this regard surpassed by Nuclear Throne, the marriage does a lot of justice to shooters - the **myriad combinations of weapons and enemies** typically seen in roguelikes makes these shooters more enjoyable than many traditional shooters, much as *Crimsonland*'s numerous weapons had.

This mixed-genre benefits the rogue-like aspect too; just as different weapons and enemies forces you to play the game differently, each run-through is a unique experience due to the items and powerups you happen to get.

## The Future?

I believe we'll continue to see a steady trickle of great overhead shooters, because the genre is simple unadulterated fun. But there'll always be room for innovation, whether that's taking ideas from other, even unrelated genres, but also revisiting old games that had neat ideas but didn't explore them to their fullest, or for whatever reason weren't influential.

The same could be said for any genre, really. We ought to look back on games from the past, because they have a lot of lessons to teach, both what to do and what not to do.
