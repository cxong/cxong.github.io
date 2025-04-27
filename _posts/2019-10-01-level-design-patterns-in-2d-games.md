---
layout: post
title: "Level Design Patterns in 2D Games"
date: 2019-10-26
comments: true
published: true
---

I'm a sucker for level design and design patterns, so when I came across this [article](https://www.gamasutra.com/blogs/AhmedKhalifa/20190610/344344/Level_Design_Patterns_in_2D_Games.php) (and [paper](http://akhalifa.com/documents/level-design-patterns.pdf)) called ["Level Design Patterns in 2D games"](https://www.gamasutra.com/blogs/AhmedKhalifa/20190610/344344/Level_Design_Patterns_in_2D_Games.php), I had to read it! Unfortunately it's a bit wordy, so I thought I'd summarise it and throw in a bunch of pictures! Enjoy!

> Hover over the images to read an explanation for each example!

# Guidance

Guide the player through the path they need to take.

1.  Level shape

        | Super Mario Bros. | Super Meat Boy |
        | ------------- | ------------- |
        | ![Super Mario Bros. stairs to flagpole](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smb.png "The upward shape of the staircase encourages players to hit the flagpole as high as possible, achieving a greater score") | ![Super Meat Boy hills](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/super_meat_boy.png "The goal is to reach the pink character on the middle platform, but it's impossible to jump here from the starting location directly. Instead the gentle staircase-like level layout hints at the solution - move to the right side of the level, then jump left onto the middle platform.") |
        {:.table-bordered}

    <!--more-->

2.  Collectibles (a.k.a. _breadcrumbing_)

    | Donkey Kong Country 2                                                                                                                                                                   | Granny Smith                                                                                                                                                                                           |
    | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | ![Donkey Kong Country 2 bananas](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/dkc2.jpg "Collect the trail of bananas and you'll hit the target at the bottom") | ![Granny Smith apples](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/granny_smith.png "The trail of coins shows the ideal arc in order to catch the trapeze bar on the right") |

    {:.table-bordered}

3.  Enemies

    | Super Mario Bros. 3                                                                                                                                                                               | Sonic 3                                                                                                                                                                                                                        |
    | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | ![Super Mario Bros. 3 flying shells](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smb3.jpg "Mario can jump on the procession of flying Para-Beetles to clear the chasm") | ![Sonic 3 monkey and collectible on tree](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sonic3.png "By attacking the Monkey Dude, the player will find a hidden Super Ring video monitor in the tree") |

    {:.table-bordered}

4.  Environmental cues

    | The Legend of Zelda: A Link to the Past                                                                                                                                                                              | Pokemon                                                                                                                                                                             |
    | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ![The Legend of Zelda: A Link to the Past bombable walls](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loz_lttp.png "subtly different cave texture hints at a location that can be bombed") | ![Pokemon hidden items in conspicuous rocks](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon.png "suspicious looking boulder contains a hidden item") |

    {:.table-bordered}

# Safe Zone

Give the players a place safe from hazards so they can stop and think.

| Contra                                                                                                                                                                                               | The Legend of Zelda                                                                                                                                                                                                             |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![Contra energy zone flames](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/contra.png "The player can wait on this platform to safely contemplate the next flame challenge") | ![The Legend of Zelda safe doorways in dungeons](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/zelda.gif "Link is often safe at the entrance of new rooms, giving the player time to examine the room") |

{:.table-bordered}

# Foreshadowing

Partially introduce something new to the player, only to fully reveal it later. This can serve to teach the player, or encourage exploration.

1. New hazard that's out of reach

   | Bare Knuckle III                                                                                                                                                                                                              | Golden Axe                                                                                                                                                                                                                                                      |
   | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Bare Knuckle III boss in boat](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/bareknuckle.png "Ash, the level boss, initially drives the boat and ferries goons, being inaccessible until the end.") | ![Golden Axe bad brothers](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/goldenaxe_bad.png "Two giants with huge hammers stand menacingly yet inactive. They wake up once you defeat all the other enemies, starting the boss battle.") |

   {:.table-bordered}

2. New enemy that foreshadows a boss

   | Megaman                                                                                                                                                                                                                                                                                                                                                                                                                                | Contra                                                                                                                                                                                                                            |
   | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Megaman enemy using Cutman weapon](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman.jpeg "Before encountering Cut Man, his Rolling Cutter scissors appears as an enemy, foreshadowing what the boss fight will be like")![Megaman Cutman boss fight](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman_cut.jpeg "Cut Man using the same Rolling Cutter attack seen before") | ![Contra bugger before boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/contra.jpeg "The appearance of scorpion-like Buggers signals the boss is close - which includes eggs that hatch more Buggers") |

   {:.table-bordered}

3. New objects / obstacles that cannot be used until later, to encourage exploration.

   | Chrono Trigger                                                                                                                                                                                                                                                                                   | Pokemon                                                                                                                                                                                                |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   | ![Chrono Trigger sealed chests](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/chrono_trigger.png "Magically sealed chests are found throughout the game, before obtaining the magic pendant that unlocks them. Collecting all the chests requires lots of backtracking") | ![Pokemon tree](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/pokemon_tree.png "Various trees block key paths in the game, which can be cut after obtaining a key item later") |

   {:.table-bordered}

# Layering

Combining multiple objects to create new experiences, like a harder challenge.

1. Multiples of the same object

   | Raiden 2                                                                                                                                                                                                     | Streets of Rage 3                                                                                                                                                                           |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Raiden 2 multiple enemies](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/raiden2.png "Multiple tanks and Lasercopters presents a tougher challenge than encountering them singly") | ![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sor3.png "Mona and Lisa, two identical fighters, presents a much tougher challenge, and have unique combo moves") |

   {:.table-bordered}

2. Different objects

   | Jackal                                                                                                                                                                                           | Super Mario World                                                                                                                                                                                                          |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Jackal level 5 boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/jackal_boss.png "The combination of turrets and tank spawners leads to an overwhelming boss fight") | ![Super Mario World Banzai Bill and Goombas](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/smw.jpg "Banzai Bills are normally easy to jump over, but blocks above Mario make this a tense moment") |

   {:.table-bordered}

# Branching

Giving the player different choices.

1. Branching with no restrictions - gives the feeling of exploration

   | Binding of Isaac: Rebirth                                                                                                                                                                                                                                                     | Final Fantasy IV                                                                                                                                                                                                                                                  |
   | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Binding of Isaac: Rebirth branching map](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/boi_map.png "The player can freely choose the next room to go to, even though the map is unexplored, giving the illusion of choice in a fairly linear game") | ![Final Fantasy IV airship](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ff4.jpeg "Getting the airship is a pivotal moment in the game - the player can both revisit past locations, go to new locations, and even find hidden islands") |

   {:.table-bordered}

2. Conditional branching - stimulates curiosity and may require backtracking

   | Super Metroid                                                                                                                                                                                             | The Legend of Zelda: A Link to the Past                                                                                                                                                                                                                 |
   | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Super Metroid coloured doors](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/super_metroid.gif "Special doors require special weapons to open, and often requires backtracking") | ![The Legend of Zelda: A Link to the Past locked doors](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loz.png "Locked doors often appear before the keys to open them are found, leading to a maze-like dungeoning experience") |

   {:.table-bordered}

3. Risk-reward branches - encourages players to invest more time in the game by rewarding skill

   | Excitebike                                                                                                                                                                        | Sonic 3                                                                                                                                                                              |
   | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   | ![Excitebike branching paths](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/excitebike.gif "There are often faster paths which are trickier to navigate") | ![Sonic 3 extra life](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/s3.png "Powerful items like extra lives are often well hidden, and off the beaten path") |

   {:.table-bordered}

# Pace Breaking

Dramatically changing the pacing of the game - higher or lower tension.

1. Introduce difficulty (e.g. bosses) to increase tension

   | Lifeforce                                                                                                                                                           | 1943                                                                                                                                                                                    |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Lifeforce first boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/lifeforce.png "Bosses are preceeded by an eerie, enemy-less section") | ![1943 boss](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/1943.png "Before bosses, the music changes, and the waters visibly change and become deathly-still") |

   {:.table-bordered}

2. Decrease tension to let players enjoy other parts of the game, or learn a new mechanic

   | Mappy                                                                                                                                                                                                                                                              | Street Fighter 2                                                                                                                                                                                                                                               |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Mappy bonus round](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/mappy.png "Bonus levels with no enemies break up the tension, but to get a perfect score the player needs to use new techniques like quickly breaking the trampolines") | ![Street Fighter 2 car](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sf2.jpg "The goal of destroying the car as quickly as possible lets players experiment with different moves and learn their relative strengths in a safe space") |

   {:.table-bordered}

3. Decrease tension to set up for a more dramatic increase later (e.g. just before a boss fight)

   | Megaman 2                                                                                                                                                                                                                       | Chrono Trigger                                                                                                                                                                                                                         |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | ![Megaman 2 boss corridor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/megaman2.png "Boss battles are proceeded by a short passage with no enemies, mentally gearing the player for the fight ahead") | ![Chrono Trigger Magus's Lair](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ctmagus.jpg "The iconic approach sequence to Magus has scripted fires appear around the player, dramatically upping the tension") |

   {:.table-bordered}

4. Controlling tension through level design

   | Jackal                                                                                                                                                                               | Gradius 2                                                                                                                                                                            |
   | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   | ![Jackal lasers](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/jackal_laser.png "These timed lasers force the player to stop moving and approach carefully") | ![Gradius 2 flares](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/gradius2.png "occasional flares appear from off screen, keeping the player on their toes") |

   {:.table-bordered}
