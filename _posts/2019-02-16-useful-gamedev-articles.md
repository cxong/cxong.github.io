---
layout: post
title: "Useful Gamedev Articles"
date: 2019-02-16
comments: true
published: true
---

Over the years I've found myself referring back to the same handful of gamedev articles, because their advice is useful and timeless. I've decided to collect them here in one place for easy reference. Hope you enjoy!

### [How to Reduce Visual Confusion in Your Game](https://www.gamasutra.com/blogs/PeterAngstadt/20150312/238446/How_to_Reduce_Visual_Confusion_in_Your_Game.php?print=1) by Peter Angstadt

![](https://images-blogger-opensocial.googleusercontent.com/gadgets/proxy?url=http%3A%2F%2F2.bp.blogspot.com%2F-Edl9e31jHDg%2FVPutq6pwcjI%2FAAAAAAAAAcc%2Ffl1Hc8RDPRc%2Fs1600%2Fdotavalues.png&container=blogger&gadget=a&rewriteMime=image%2F*)

A lot of game devs know how to make good-looking screenshots but the game itself is unreadable because everything looks too busy, too dark or too washed out. This article goes into the visual design theory of why, and really easy ways of improving the readability of your game.

<div style="overflow: auto;">

### [The Theory and Practice of Cameras in Side-Scrollers](https://docs.google.com/document/d/1iNSQIyNpVGHeak6isbP6AHdHD50gs8MNXF1GCf08efg/pub?embedded=true) by Itay Keren

<img style="float: right;" src="https://lh5.googleusercontent.com/S_XlJsuKm5nDiihKatCTyZm6l7nXSBlEro2HadFE5OT1K9Odddzso7Yl1rIkfiefn-ItoodGuJ7wGUOIjS7nVtix9DbKFCt0Mkl2nTYlciXnUzptfMgCHNd4xTmx0xn2gcq0CTA">

This article contains an encyclopaedic list of 2D side-scroller cameras, many of which can also be applied to 2D games in general. Essential reading for anyone making a 2D camera.
</div>

<div style="overflow: auto;">

### adventures in level design: Wolfenstein 3D ([1](http://ellaguro.blogspot.com/2012/05/adventures-in-level-design-wolfenstein.html), [2](http://ellaguro.blogspot.com/2012/04/adventures-in-level-design-wolfenstein_27.html), [3](http://ellaguro.blogspot.com/2012/04/adventures-in-level-design-wolfenstein.html)) by Liz Ryerson

<img style="float: left;" src="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/liz_barrel.png">

This series of blog posts dissecting a few Wolfenstein 3D levels contains surprising insights, covering not just the classic level design goal of pacing, but also narrative and the surprising effect of confusing map layouts and what that says about an ultimately ridiculous game setting.
</div>

<div style="overflow: auto;">

### [Traversal Level Design Principles](http://gamasutra.com/blogs/TravisHoffstetter/20160107/263175/Traversal_Level_Design_Principles.php?print=1) by Travis Hoffstetter

<img style="float: right;" src="https://www.gamasutra.com/db_area/images/blog/263175/LongLedgeBreakdown.PNG">

Traversal is an oft-overlooked but key component of open-world games. Great traversal means it's fun to get around in the game, and this is just as important as having an interesting world. Good reference article for anyone making a game that involves travelling across a world.
</div>

### [Fix Your Timestep!](https://gafferongames.com/post/fix_your_timestep/) by Glenn Fiedler (Gaffer On Games)

Normally I'd recommend game devs use a good engine, so you won't need to write a game loop. But for the stubborn engine developers, or just the morbidly curious, this is a really good article on why your homebrew game loop probably sucks. At least you'll know what the heck delta time means.

```cpp
        while ( accumulator >= dt )
        {
            previousState = currentState;
            integrate( currentState, t, dt );
            t += dt;
            accumulator -= dt;
        }
```

### [Build a Bad Guy Workshop - Designing enemies for retro games](http://www.gamasutra.com/blogs/GarretBright/20140422/215978/Build_a_Bad_Guy_Workshop__Designing_enemies_for_retro_games.php?print=1)

A big list of retro enemy behaviours. Really great reference for retro game devs.

> **Splitter**	The enemy can split into multiple other enemies while destroying itself. Examples: Rogue Legacy's Slimes, Legend of Zelda's Vire and Biri.
> 
> **Cloner**	The enemy can duplicate itself. Often, the duplicate is an exact clone, but sometimes, the duplicate is very slightly modified (such as having reduced health, or being faster). The enemy that does the cloning is not destroyed. Example: Zelda's Ghini

### [Miyamoto on World 1-1: How Nintendo made Mario's most iconic level](https://youtu.be/zRGRJRUWafY)

[![Miyamoto on World 1-1: How Nintendo made Mario's most iconic level](https://img.youtube.com/vi/zRGRJRUWafY/0.jpg)](https://www.youtube.com/watch?v=zRGRJRUWafY)

This short (~15min) video by Eurogamer analyses Super Mario Bro's world 1-1 with its creators including Miyamoto. In it he explains how they designed the level to teach players the fundamentals of playing platformer games, using escalating challenges and sequences. It's a powerful technique and a superior alternative to overt tutorials and manual instructions.

The same idea has been explored in other places, but this video is a great, concise introduction to the concept.

<div style="overflow: auto;">

### [Reverse Design articles by The Game Design Forum](http://thegamedesignforum.com/features/featureshome.html)

<img style="float: left;" src="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tgdf_smw.png">

These are really quality design analyses of classic games. All of them are very good but of particular use are:

- [Final Fantasy 6](http://thegamedesignforum.com/features/reverse_design_ff6_1.html) and the special way it's designed around the dungeon as the unit of content, and how that influences everything from battle durations and how to balance those pesky RPG curves.
- [Super Mario World](http://thegamedesignforum.com/features/RD_SMW_1.html) is a masterclass in cadence design - how to ramp up difficulty in a challenging yet pleasing way.
</div>
