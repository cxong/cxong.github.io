---
layout: post
title: "Game Framework Tier List"
date: 2022-08-21
comments: true
published: true
---

To expand on some of the thoughts from my [previous rant on nim](http://cxong.github.io/2022/07/why-i-gave-up-on-nim), here's a tier list I made. Yep, it's going to be my garbage opinions! But it also includes my (admittedly subjective) first-hand experience with using these frameworks. I've used some for years, others just a week. And it includes a few engines and not just frameworks. So there 🧐

## Criteria

How can you judge anything without clear criteria? Mine are quite specific; I am interested in making 2D games, for both jams and long-term hobby projects, so the results will seem heavily skewed if you have different needs. I have made [3D games](http://cxong.github.io/games.html) in the past, but it's not my cup of tea. I may expand on why I'm not interested in a future post. I'm also really keen on frameworks that are great for game jams - [I've written about that in the past](http://cxong.github.io/2020/06/fantasy-consoles-for-jams). In no particular order here are things I look for:

- Learning curve
- Quality of documentation and examples, ease of troubleshooting in general
- How easy it is to package, including web export
- How fun it is to use, vs. fighting with instability and quirks
- How powerful and flexible it is

Also, some of these frameworks are super-specialised. I try to be fair here, for example if a framework is specifically made for VN games, I'm only going to judge it by how it can make a VN game.

Last but not least, I only list frameworks which I've at least attempted to make a game with.

## The List

[![Tier list](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/game-frameworks.png)](https://tiermaker.com/list/video-games/game-frameworks-15282244/2400244)

<!--more-->

- **Phaser**: this was my go-to jam engine and I've used this for many years. The [examples website](https://phaser.io/examples) is excellent, and being a web framework, is great for jams. I stopped using it only because I found [something even better for jams](http://cxong.github.io/2020/06/fantasy-consoles-for-jams), and for other purposes, a web-only framework isn't ideal. Still for what it is, it's great.
- **TIC-80**: my weapon of choice for game jams. The limitations are perfect for jams as it's insanely easy and fast to get something playable, and with the cheap pro version, collaboration is also easy. It's so nice for jams that I wrote [a whole post about it](http://cxong.github.io/2020/06/fantasy-consoles-for-jams).
- **Love2D**: on the surface this seems like a bog-standard 2D game framework, but being Lua, a scripting language, the packaging is genius - you can put your code in a `.love` file, and it can run on any machine easily. It also has a pretty big and dedicated community, with extensions for doing a lot of things. I take marks off because of Lua, a weird (in a bad way) language, and a lack of native support for web export, crucial for jams. However on those fronts, I've been looking into using MoonScript + a web export pipeline, which could make this an awesome option.
- **Unity**: credit must be given for how insanely popular Unity is, which gives it a huge community, lots of resources for learning, and people to work with. Unfortunately it's also very buggy, plugins randomly break with new versions, webGL export is always a pain, and wants to force you to do things a certain way.
- **SDL2**: so lightweight calling it a "game framework" is a bit too charitable, but there's no denying the large number of games, especially retro games, that have been modernised thanks to this library. I've made a few simple 2D games from scratch using this, and that's pretty much all it's good for, when it comes to making a new game.
- **MonoGame**: I used this for a major project more than a decade ago (when it was XNA). At the time it was fantastic, as there was nothing quite like it - a simple yet powerful framework, that could target both PC and console, and supported by a large company that makes games. These days it's still decent, with some good games still using it, but it does not offer any large advantages for the newcomer.
- **OpenFL**: I must admit I've never actually managed to make anything with OpenFL, but I really wanted to get into it. There are some really nice games made with this and Haxe, but the dev environment is not easy at all to set up. Back in the day, the promise of having a single language that transpiled to C++ for efficiency and JavaScript for web was really enticing, but now emscripten is so widespread that most good game frameworks support web export as a first class feature. I don't really have a good reason to revisit this platform anymore.
- **SFML**: I consider this SDL-for-C++, although it's a bit better and a bit worse. Better because it provides a few more nice features than SDL, worse because it's not as well designed and built, and in the end you will still need to write most of your game yourself. Even if you need to use C++, there are better options out there for making games.
- **Cocos2d**: I've only used this briefly in a prototype, but nothing really stood out. Doesn't seem that popular these days, so there are much better options out there.
- **Pygame**: Python is a fantastic language but its games offerings are woeful, due in large part to pygame. It's quite easy to get into thanks to Python, and there are nice resources out there to get started, but it's after the initial experiments where things fall apart - the terrible deployment process, lack of serious extensions or 3rd party games libraries, and until recent years, pygame was still based on SDL 1.x which could not do high definition at all. Don't be fooled by how easy this framework is to pick up - it's not much more than a nice wrapper around SDL.
- **libGDX**: this framework has been around for a while, and sure, it seems decent and is mature. I have no interest in coding in Java however.
- **nico**: [I wrote more extensively](http://cxong.github.io/2022/07/why-i-gave-up-on-nim) about this game framework before, the tl;dr version is that this seems nice, but is very niche, and given the niche nim language and lack of maintenance activity, it's hard to recommend this to anyone.
- **Your own engine**: almost a joke option, but it's here because I've done this before. [Just don't do it](https://seanmiddleditch.github.io/makes-games-not-engines-to-learn-engines/).
- **Construct2**: I briefly tried this framework out to make a prototype, and discovered this kind of drag-and-drop game making is totally not for me. I would much rather code games myself, since I know how and it's way more flexible. In theory you could make great games with it but judging from the typical Construct game (i.e. made by non-programmers), they're nothing special.

## Honorable Mentions

I haven't tried the following frameworks but they are interesting and I would definitely give them a go if I had the opportunity.

### General Purpose Frameworks / Engines

- **Python Arcade**: I came across this while looking for an alternative python framework than pygame, and was impressed by how [it seemed to do everything right](https://api.arcade.academy/en/latest/pygame_comparison.html). The framework is well designed as a games framework first, with useful libraries like tilemap support, rather than a thin wrapper around SDL. Two reasons made it less enticing for me: it is still python which means it doesn't package well, and pygame 2 adds SDL2 support which finally made it performant on HD resolutions. But if I had to make a game in python this would be my first choice. **Possible Tier A**
- **Godot**: When this first came out there was a lot of fanfare about how this would be the open source Unity-killer. Years later Unity is still going strong, and Godot has a (relatively) small but healthy community, and is a regular choice among game jam entries. I'm not so interested in using its GDScript language, nor in learning a game engine, but otherwise this seems like a solid choice. **Tier A-B, depending on how it compares to Unity**
- **GameMaker**: This popular and venerable 2D game engine seems like a totally legit choice for making games, with scripting ability so you're not so limited to what the engine itself can support. Two reasons why I haven't looked into it: it's paid and not open-source, and its scripting language is proprietary. Still, recently it has started to offer a free version, so it could be worth looking into. **Tier B probably**
- **Unreal Engine**: Never had an interest in this, as it seemed to heavy to get into. Plus it's like 12GB, so no thanks. **Tier D, not for me**
- **Allegro**: This is an old 2D games framework, originally designed for the Atari ST, but later being ported to modern platforms. It is pretty niche these days but there are a fair few quality games from the 90's and early 00's that use this library. It's not bad as a 2D games framework, so I'm open to learning more about it if I ever decide to tinker on one of these older games. **Tier B, only good for old games**
- **PICO-8**: The biggest fantasy console, with a community that dwarfs its rivals. It's pretty good, although personally I prefer the open-source TIC-80, but if I had to work on a team that uses PICO-8, I wouldn't mind learning about it. **Tier S-A, I just prefer TIC-80**

### Genre-Specific Frameworks / Engines

- **Solarus**: An engine specifically designed for Zelda-style action RPGs. For such a specific purpose, this engine is surprisingly polished and active, with several [great-looking games](https://www.solarus-games.org/en/games) made with it. I love seeing bespoke engines and frameworks like this, as it gives you a huge leg up over a general-purpose framework. If I had to make an action RPG, this would be one of my top choices.
- **Ren'Py**: This VN framework is proof that you can get great results if you focus on doing one thing and one thing well. Many successful projects use this framework, and although I haven't used it directly, I have worked on [teams that used it](https://ldjam.com/events/ludum-dare/49/home-tripper-1), and it seems really easy to use. Unfortunately VNs are not for me, but I have no reservations about recommending this.
- **OpenRA**: Red Alert has a huge following, but the makers of this open-source remake had the foresight to make the engine generic so that it can support many other RTS games. Now OpenRA drives many mods including [KKND](https://github.com/IceReaper/OpenKrush), Dune 2000, Tiberian Sun and Red Alert 2. Having tried my hand at making RTS games before, I know how much work there is in making a playable game in this genre, so OpenRA does most of the hard work for you.
- **RPGMaker**: For making a retro RPG game there is no better way. Similar to making RTS games, there is a surprising amount of work in making the basic mechanics, so a tool like RPGMaker lets you focus on the fun parts - character design, story writing, map editing - than the mechanics and UI. I've seen alternatives but none approach the quality of RPGMaker. I'm not really interested in making RPGs myself but if I were, this would be a solid choice.

I have no experience with these frameworks but if they work as well as they seem, they could all be Tier S or A.

## Final Thoughts

Game frameworks have come a long way and yet in many ways still have a long way to go. On the one hand there are lots of cool specialty frameworks making it easier to make certain types of games than ever before. On the other, industry-stalwarts like Unity are still a bug-ridden mess to use, which is very disappointing given how popular they are and how much better they could be.

New tech is always hype-y but the game dev world seems particularly bad; new frameworks and engines that over-promise but then can't do really basic things is an evergreen meme. I am cautiously optimistic that, in the long run, the wheat will separate from the chaff and we'll get some truly outstanding options in 10 years time. Here's to hoping!
