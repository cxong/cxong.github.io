---
layout: post
title: "Useful Gamedev Articles"
date: 2019-02-16
comments: true
published: true
---

Over the years I've found myself referring back to the same handful of gamedev articles, because their advice is useful and timeless. I've decided to collect them here in one place for easy reference. Hope you enjoy!

### [Reducing Visual Confusion In Your Game](https://icewyrmgames.github.io/research/reducing-visual-confusion-in-your-game/) by Peter Angstadt

![Side-by-side screenshot of DoTA 2 with a greyscale vs full colour version, with the greyscale image showing the important visual elements like characters and UI](https://icewyrmgames.github.io/research/reducing-visual-confusion-in-your-game/dota2.jpg)

A lot of game devs know how to make good-looking screenshots but the game itself is unreadable because everything looks too busy, too dark or too washed out. This article goes into the visual design theory of why, and really easy ways of improving the readability of your game.

<!--more-->

### [The Theory and Practice of Cameras in Side-Scrollers](https://docs.google.com/document/d/1iNSQIyNpVGHeak6isbP6AHdHD50gs8MNXF1GCf08efg/pub?embedded=true) by Itay Keren

![Animation of Super Mario World, with guide lines overlaid showing the boundaries of camera movement. The camera follows Mario at an anchor point and shifts to a different anchor point as he turns and runs.](https://lh5.googleusercontent.com/S_XlJsuKm5nDiihKatCTyZm6l7nXSBlEro2HadFE5OT1K9Odddzso7Yl1rIkfiefn-ItoodGuJ7wGUOIjS7nVtix9DbKFCt0Mkl2nTYlciXnUzptfMgCHNd4xTmx0xn2gcq0CTA)

This article contains an encyclopaedic list of 2D side-scroller cameras, many of which can also be applied to 2D games in general. Essential reading for anyone making a 2D camera.

### adventures in level design: Wolfenstein 3D ([1](http://ellaguro.blogspot.com/2012/05/adventures-in-level-design-wolfenstein.html), [2](http://ellaguro.blogspot.com/2012/04/adventures-in-level-design-wolfenstein_27.html), [3](http://ellaguro.blogspot.com/2012/04/adventures-in-level-design-wolfenstein.html)) by Liz Ryerson

![A screenshot of Wolfenstein 3D showing a barrel blocking an exit elevator](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/liz_barrel.png)

This series of blog posts dissecting a few Wolfenstein 3D levels contains surprising insights, covering not just the classic level design goal of pacing, but also narrative and the surprising effect of confusing map layouts and what that says about an ultimately ridiculous game setting.

### [Traversal Level Design Principles](https://www.gamedeveloper.com/design/traversal-level-design-principles) by Travis Hoffstetter

![A rough sketch of a building exterior, with many arrows and labelled points illustrating traversal actions such as climbing up/down, entering/exit points, and going over/across the building.](https://eu-images.contentstack.com/v3/assets/blt740a130ae3c5d529/bltce32f2d33ea440be/650ec2d4c6498b7459fe4d16/CabinPic.PNG/?width=541&auto=webp&quality=80&disable=upscale)

Traversal is an oft-overlooked but key component of open-world games. Great traversal means it's fun to get around in the game, and this is just as important as having an interesting world. Good reference article for anyone making a game that involves travelling across a world.

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

> **Splitter** The enemy can split into multiple other enemies while destroying itself. Examples: Rogue Legacy's Slimes, Legend of Zelda's Vire and Biri.
>
> **Cloner** The enemy can duplicate itself. Often, the duplicate is an exact clone, but sometimes, the duplicate is very slightly modified (such as having reduced health, or being faster). The enemy that does the cloning is not destroyed. Example: Zelda's Ghini

### [Miyamoto on World 1-1: How Nintendo made Mario's most iconic level](https://youtu.be/zRGRJRUWafY)

[![Miyamoto on World 1-1: How Nintendo made Mario's most iconic level](https://img.youtube.com/vi/zRGRJRUWafY/0.jpg)](https://www.youtube.com/watch?v=zRGRJRUWafY)

This short (~15min) video by Eurogamer analyses Super Mario Bro's world 1-1 with its creators including Miyamoto. In it he explains how they designed the level to teach players the fundamentals of playing platformer games, using escalating challenges and sequences. It's a powerful technique and a superior alternative to overt tutorials and manual instructions.

The same idea has been explored in other places, but this video is a great, concise introduction to the concept.

### [Reverse Design articles by The Game Design Forum](http://thegamedesignforum.com/features/featureshome.html)

![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tgdf_smw.png)

These are really quality design analyses of classic games. All of them are very good but of particular use are:

- [Final Fantasy 6](http://thegamedesignforum.com/features/reverse_design_ff6_1.html) and the special way it's designed around the dungeon as the unit of content, and how that influences everything from battle durations and how to balance those pesky RPG curves.
- [Super Mario World](http://thegamedesignforum.com/features/RD_SMW_1.html) is a masterclass in cadence design - how to ramp up difficulty in a challenging yet pleasing way.

### [The guide to implementing 2D platformers](http://higherorderfun.com/blog/2012/05/20/the-guide-to-implementing-2d-platformers/)

![Screenshot of Megaman X with Megaman standing on a sloped surface, a hitbox shown and arrows following the sloped surface](https://uploads.gamedev.net/monthly_06_2012/ccs-5-0-34367600-1338602309.png)

An invaluable resource for platformer devs, and also a great article to show people who underestimate the amount of work required for this genre. It even covers tricky cases like slopes, moving platforms, stairs and more.
