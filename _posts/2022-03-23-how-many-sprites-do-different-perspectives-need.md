---
layout: post
title: "How may sprites do different perspectives need?"
date: 2022-03-23
comments: true
published: true
---
I love 2D sprite-based games; they are easy to read and a great way to showcase beautiful art and character designs. A major downside is that drawing each sprite is a significant amount of work, and it can grow exponentially depending on the [game perspective](https://tvtropes.org/pmwiki/pmwiki.php/Main/VariousVideoGameViews)!

Choosing the right game perspective has a big impact on your game's art budget. Here's a rundown of different 2D game perspectives and how many different sprites you need to budget for.

# Summary

| Perspective | Sprites Needed | Genres | Examples |
| --- | --- | --- | --- |
| Top-down (vertical) | 1x | action, arcade, puzzle, vertical scrollers | ![Galaxian][7] ![[Centipede][8]](https://tvtropes.org/pmwiki/pmwiki.php/VideoGame/Centipede) [![GTA 2][1]][2] |
| Side view | 1-1.5x | beat-em-up, fighting, infinite runner, metroidvania, platformer, run-and-gun, side-scrolling | [![Knytt][12]][13] ![Mighty Final Fight](https://upload.wikimedia.org/wikipedia/en/1/15/Mighty_Final_Fight_gameplay.png) ![Flashback](https://upload.wikimedia.org/wikipedia/en/6/6e/Flashback_-_The_Quest_for_Identity.png) |
| Isometric (4 directions) | 2-2.5x | business simulation, turn based strategy, turn based tactics | ![Super Mario RPG][11] ![Theme Hospital][14] ![Tactics Ogre](https://upload.wikimedia.org/wikipedia/en/0/09/SFC_Tactics_Ogre_-_Let_Us_Cling_Together.png) |
| Oblique | 3-3.5x | action RPG, overhead shooter, RPG, RTS | [![Seiken Densetsu 3][9]][10] ![Z](https://upload.wikimedia.org/wikipedia/en/1/14/Linux.Debian.ZED.0.1.jpg) ![Zelda Four Swords](https://images.gnwcdn.com/articles/a/5/7/6/8/7/1.jpg/EG11/resize/270x-1/quality/75/format/jpg) |
| 8-directional | 5-5.5x | 8-directional shooter, real time tactics | ![Gauntlet 2][17] [![Super Contra][15]][16] ![Syndicate][20] |

# Top-down: 1x

Games with a perfectly vertical perspective are the cheapest to create sprites for. You only need to create one set of sprites, and even if you need characters to face different directions, you can let your rendering software rotate the sprites. A lot of simple or retro game genres use this economical perspective - **arcade games**, top-down **action games**, **puzzle games** and so on.

> ![Galaxian][7]

The downside is that it's not a very flattering perspective. Characters can't show off their face, only the tops of their heads. Buildings only show their roofs, which are rarely shown in real life, plus it's hard to show important parts like doors.

On the other hand, cars and other vehicles look perfectly fine in this perspective. This is why games like top-down **vertically scrolling shooters** use airplanes or spaceships instead of human characters.

> [![GTA 2][1]][2]
>
> Grand Theft Auto 1 and 2 used a top-down perspective for its human characters and cars. The cars look great; the human characters less so.

# Side view: 1-1.5x

[Side view](https://tvtropes.org/pmwiki/pmwiki.php/Main/SideView) games are also very cheap to draw for. Compared with top-down games, it shows off characters and scenery much better. Because of this ability to intimately show off characters, it's popular in **fighting games** and **metroidvanias**.

> [![Knytt][12]][13]

Games like **infinite runners** only have one fixed view of the characters; even if you allow the characters to move left and right, as in **platformers**, **side-scrollers** or **run-and-gun** games, you can mirror the sprite, which is very cheap to do.

> [![contra sprites][3]][4]
>
> Contra sprites are simply mirrored, which makes the character's handedness change. But it's so fast-paced that most people don't notice.

One caveat is if the characters are handed, [it can look odd when they are simply mirrored](https://tvtropes.org/pmwiki/pmwiki.php/Main/AmbidextrousSprite). Sometimes you can get away with it; if not or if you care about it enough, it can take some time to rework to mirror the sprites.

> [![dragon quest sprites][5]][6]
>
> Dragon Quest, like many JRPGs, have the player look at the character sprites for long periods of time, so it pays off to make sure they are holding their swords and shields on the correct sides, no matter which way they are facing.

# Isometric (4 directions): 2-2.5x

[Isometric games](https://tvtropes.org/pmwiki/pmwiki.php/Main/IsometricProjection) combine the advantages of the freedom of movement of top-down games with the attractiveness of side-scrolling games. If you limit movement to the four diagonal directions, you can get away with only creating 4 sets of sprites: front-facing and back-facing, with the other two directions simply mirrored!

> ![Super Mario RPG][11]
>
> In Super Mario RPG, although the main characters can be viewed in 8 directions, most characters are only shown in the 4 isometric directions.

Similar to the side-scrolling perspective, if your characters are handed, you may need to slightly rework sprites when they are mirrored.

Because not being able to move vertically or horizontally feels unnatural for action games, this perspective finds more use in slower-paced genres like **turn based tactics** and **turn based strategy** games.

> ![Theme Hospital][14]
>
> In the business simulation game Theme Hospital, players build out rooms in their hospital while managing staff and incoming patients. The isometric view helps show off the rooms and quirky characters.

# Oblique: 3-3.5x

[3/4 oblique perspective](https://tvtropes.org/pmwiki/pmwiki.php/Main/ThreeQuartersView) is a highly versatile perspective. It can show off characters and scenery well, as well as feeling natural for players to move around in, so it can be used for a lot of genres. **Overhead shooters**, **RPGs**, **RTS** games, **ARPGs**, as well as genres that work with the other top-down-style perspectives... oblique perspective can handle them all.

> [![Seiken Densetsu 3][9]][10]

The cost is that the sprite work required is substantial: you need at the very least 3 sets of sprites: side view (mirrored for left/right), front view and back view. Again, if your characters are handed, you may need to rework the side view sprites too. For this reason oblique view sprites tend to be simpler compared to side-scrolling games.

> [![Super Contra][15]][16]
>
> Super Contra has overhead shooting sections where the player can face many directions. Its iconic, set-piece bosses however are fixed in one perspective, so the artists can afford to put extra effort into them.

# 8-directional: 5-5.5x

If you want to draw characters moving in 8 directions, the amount of sprites required approaches the limit of what's sensible for hand-drawn sprites. You must draw at least 5 sets of sprites: in addition to the 3 sets for the cardinal directions, you also need 2 sets for the diagonals.

> ![Gauntlet 2][17]
>
> Gauntlet 2, a fast-paced shooting game, being able to move and shoot in 8 directions is crucial, so the sprites are drawn in all 8 directions.

The substantial artwork cost means you should carefully consider workarounds:

1. Allow players to move diagonally, but only draw 4 directions

> <iframe src="https://assets.pinterest.com/ext/embed.html?id=60446819988701257" height="336" width="236" frameborder="0" scrolling="no" ></iframe>

2. Use the perfectly vertical top-down perspective, letting your renderer or image editor do the rotation for you

> [![Alien Breed][18]][19]

3. Use 3D-rendered sprites, which also lets you add arbitrary number of angles

> ![Diablo](https://upload.wikimedia.org/wikipedia/en/2/20/Diabloscreen.jpg)

This perspective only makes sense for games where showing the 8 directions is really important, like **8-directional shooters**.

You can use either oblique or isometric perspectives for buildings; oblique may be easier to navigate but isometric shows off more sides for buildings.

> ![Syndicate][20]

[1]: https://www.mobygames.com/images/shots/s/230627-grand-theft-auto-2-playstation-screenshot-trying-to-escape.jpg
[2]: https://www.mobygames.com/images/shots/l/230627-grand-theft-auto-2-playstation-screenshot-trying-to-escape.jpg
[3]: https://i.pinimg.com/564x/71/2a/e7/712ae791b5d530c8f390265987376769.jpg
[4]: https://pin.it/3RBN50A
[5]: https://i.pinimg.com/564x/69/b3/52/69b352f309089cfc90b53db325697171.jpg
[6]: https://pin.it/5i8n9Ae
[7]: https://upload.wikimedia.org/wikipedia/en/0/09/Galaxian.png
[8]: https://static.tvtropes.org/pmwiki/pub/images/centipede.png
[9]: https://www.fantasyanime.com/mana/screenshots/som2shot11.png
[10]: https://www.fantasyanime.com/mana/som2shots.htm
[11]: https://i0.wp.com/mediianews.com/wp-content/uploads/2022/02/Now-is-the-perfect-time-to-complete-Super-Mario-RPG.jpg?zoom=1&resize=280,160&ssl=1
[12]: https://static.wikia.nocookie.net/nifflas/images/5/5b/Knytt.png/revision/latest?cb=20140831104006
[13]: https://nifflas.fandom.com/wiki/Knytt
[14]: https://upload.wikimedia.org/wikipedia/en/a/a3/ThemeHospital.gif
[15]: https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/a59423b1-d1a3-4776-a3e4-5ffe0bfc77bf/d793d5w-99b034d3-0fd9-4d14-94e8-781502d4d20c.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2E1OTQyM2IxLWQxYTMtNDc3Ni1hM2U0LTVmZmUwYmZjNzdiZlwvZDc5M2Q1dy05OWIwMzRkMy0wZmQ5LTRkMTQtOTRlOC03ODE1MDJkNGQyMGMucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.n1Cp8rcx1DvM9AYWMzHU11u-OVCbOoyFtwozBNkaVFc
[16]: https://www.deviantart.com/luis-mortalkombat14/art/super-contra-2D-6-boss-438536804
[17]: https://upload.wikimedia.org/wikipedia/en/5/55/ARC_Gauntlet_II.png?1648037058741
[18]: https://t.gamesnostalgia.com/screenshots/a/l/alien-breed/21591_small.jpg
[19]: https://gamesnostalgia.com/screenshot/alien-breed/21591
[20]: https://upload.wikimedia.org/wikipedia/en/3/3d/Syndicate.png