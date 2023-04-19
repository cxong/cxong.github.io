---
layout: post
title: "Level Design Patterns in 2D Games"
date: 2019-10-26
comments: true
published: true
---
I'm a sucker for level design and design patterns, so when I came across this [article](https://www.gamasutra.com/blogs/AhmedKhalifa/20190610/344344/Level_Design_Patterns_in_2D_Games.php) (and [paper](http://akhalifa.com/documents/level-design-patterns.pdf)) called ["Level Design Patterns in 2D games"](https://www.gamasutra.com/blogs/AhmedKhalifa/20190610/344344/Level_Design_Patterns_in_2D_Games.php), I had to read it! Unfortunately it's a bit wordy, so I thought I'd summarise it and throw in a bunch of pictures! Enjoy!

> It's taken a surprising amount of effort to gather these examples. If you know of any please let me know so I can add more!

# Guidance

Guide the player through the path they need to take.

1. Level shape

    | Super Mario Bros. | Super Meat Boy |
    | ------------- | ------------- |
    | ![Super Mario Bros. stairs to flagpole](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smb.png "testing") | ![Super Meat Boy hills](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/super_meat_boy.png) |
    {:.table-bordered}

2. Collectibles (a.k.a. *breadcrumbing*)

    | Donkey Kong Country 2 | Granny Smith |
    | ------------- | ------------- |
    | ![Donkey Kong Country 2 bananas](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/dkc2.jpg) | ![Granny Smith apples](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/granny_smith.png) |
    {:.table-bordered}

3. Enemies

    | Super Mario Bros. 3 | Sonic 3 |
    | ------------- | ------------- |
    | ![Super Mario Bros. 3 flying shells](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smb3.jpg) | ![Sonic 3 monkey and collectible on tree](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sonic3.png) |
    {:.table-bordered}

4. Environmental cues

    | The Legend of Zelda: A Link to the Past| Pokemon |
    | ------------- | ------------- |
    | ![The Legend of Zelda: A Link to the Past bombable walls](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loz_lttp.png) | ![Pokemon hidden items in conspicuous rocks](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon.png) |
    {:.table-bordered}

# Safe Zone

Give the players a place safe from hazards so they can stop and think.

| Contra | The Legend of Zelda |
| ------------- | ------------- |
| ![Contra energy zone flames](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/contra.png) | ![The Legend of Zelda safe doorways in dungeons](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/zelda.gif) |
{:.table-bordered}

# Foreshadowing

Partially introduce something new to the player, only to fully reveal it later. This can serve to teach the player, or encourage exploration.

1. New hazard that's out of reach

    | Bare Knuckle III | Golden Axe |
    | ------------- | ------------- |
    | ![Bare Knuckle III boss in boat](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/bareknuckle.png) | ![Golden Axe bad brothers](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/goldenaxe_bad.png) |
    {:.table-bordered}

2. New enemy that foreshadows a boss

    | Megaman | Contra |
    | ------------- | ------------- |
    | ![Megaman enemy using Cutman weapon](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman.jpeg)![Megaman Cutman boss fight](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman_cut.jpeg) | ![Contra bugger before boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/contra.jpeg) |
    {:.table-bordered}

3. New objects / obstacles that cannot be used until later, to encourage exploration.

    | Chrono Trigger | Pokemon |
    | ------------- | ------------- |
    | ![Chrono Trigger sealed chests](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/chrono_trigger.png) | ![Pokemon tree](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon_tree.png) |
    {:.table-bordered}

# Layering

Combining multiple objects to create new experiences, like a harder challenge.

1. Multiples of the same object

    | Raiden 2 | Streets of Rage 3 |
    | ------------- | ------------- |
    | ![Raiden 2 multiple enemies](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/raiden2.png) | ![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sor3.png) |
    {:.table-bordered}

2. Different objects

    | Jackal | Super Mario World |
    | ------------- | ------------- |
    | ![Jackal level 5 boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/jackal_boss.png) | ![Super Mario World Banzai Bill and Goombas](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smw.jpg) |
    {:.table-bordered}

# Branching

Giving the player different choices.

1. Branching with no restrictions - gives the feeling of exploration

    | Binding of Isaac: Rebirth | Final Fantasy IV |
    | ------------- | ------------- |
    | ![Binding of Isaac: Rebirth branching map](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/boi_map.png) | ![Final Fantasy IV airship](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ff4.jpeg) |
    {:.table-bordered}

2. Conditional branching - stimulates curiosity and may require backtracking

    | Super Metroid | The Legend of Zelda: A Link to the Past |
    | ------------- | ------------- |
    | ![Super Metroid coloured doors](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/super_metroid.gif) | ![The Legend of Zelda: A Link to the Past locked doors](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loz.png) |
    {:.table-bordered}

3. Risk-reward branches - encourages players to invest more time in the game by rewarding skill

    | Excitebike | Sonic 3 |
    | ------------- | ------------- |
    | ![Excitebike branching paths](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/excitebike.gif) | ![Sonic 3 extra life](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/s3.png) |
    {:.table-bordered}

# Pace Breaking

Dramatically changing the pacing of the game - higher or lower tension.

1. Introduce difficulty (e.g. bosses) to increase tension

    | Lifeforce | 1943 |
    | ------------- | ------------- |
    | ![Lifeforce first boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/lifeforce.png) | ![1943 boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/1943.png) |
    {:.table-bordered}

2. Decrease tension to let players enjoy other parts of the game, or learn a new mechanic

    | Mappy | Street Fighter 2 |
    | ------------- | ------------- |
    | ![Mappy bonus round](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/mappy.png) | ![Street Fighter 2 car](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sf2.jpg) |
    {:.table-bordered}

3. Decrease tension to set up for a more dramatic increase later (e.g. just before a boss fight)

    | Megaman 2 | Chrono Trigger |
    | ------------- | ------------- |
    | ![Megaman 2 boss corridor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman2.png) | ![Chrono Trigger Magus's Lair](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ctmagus.jpg) |
    {:.table-bordered}

4. Controlling tension through level design

    | Jackal | Gradius 2 |
    | ------------- | ------------- |
    | ![Jackal lasers](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/jackal_laser.png) | ![Gradius 2 flares](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/gradius2.png) |
    {:.table-bordered}
