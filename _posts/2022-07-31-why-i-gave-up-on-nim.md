---
layout: post
title: "Why I gave up on Nim"
date: 2022-07-31
comments: true
published: true
---

For a number of years, I've been looking for a great new programming language to make games with. When I came across [nim](https://nim-lang.org), it felt like a breath of fresh air and my search seemed to be over. However, after trying it for a month or so, I have sadly concluded that it's not the right language for me.

# Disclaimer

Nim is a great language, in fact out of the languages that have come onto the scene in the last decade or so, nim is one of the more promising. This is not meant as a critique of the language overall, only that in its current state, and for my purposes, it is not the right choice.

<!--more-->

# Why look for a new language?

When it comes to making games, I'm a bit of an all-rounder these days, but I'm still a programmer by trade, and it's what I'm best at. Writing code is what I do, and care most about, and the current state of game programming leaves a lot to be desired:

- Good, established game frameworks often use old languages like C/C++, which lack modern features or aren't as nice to work with
- Python, arguably the most popular language and which is fun and productive, but [cross platform deployment](https://packaging.python.org/en/latest/overview/#bringing-your-own-python-executable) is still an afterthought, with no standard, battle-tested method
- Modern JavaScript / TypeScript are also nice to work with, but is browser-first, and on desktop tends to be laggy and bloated
- Unity, the [800-pound gorilla of game engines](https://www.gamedeveloper.com/business/game-engines-on-steam-the-definitive-breakdown), uses C# which is a good language. But the experience of making games in Unity is very much about wrangling with an engine, rather than coding in C#.

This leaves a family of less-popular game frameworks for all sorts of languages, including libGDX for Java, XNA for C#, OpenFL for Haxe, Love2D for Lua and so on. Because their userbases are much smaller, they tend to be less polished and capable, but at least there's usually one for your favourite language.

Thus the choice for me boils down to:

- A good framework that uses an old language
- A good engine that is highly opinionated and frustrating to work with
- A good framework that is suboptimal
- A suboptimal framework in a good language

As a programmer, I could deal with the last option the best, and this is where nim fits.

# Nim for Games

![nim](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/nim.png)

Nim is a great language, at least on paper. It is compiled making it fast, but also borrows great features from languages such as Python, making it a nice language to work with too. It can even compile to a JavaScript backend, which means it supports the web as a first-class platform.

In practice it is a bit quirky and has a learning curve. It uses `var`, `let` and `const`, but in ways that are quite different from what you might expect if you came from say, JavaScript. Its documentation is reminiscent of early-2000s-era language docs, and representation on stackoverflow is sorely lacking. Its choice to take features from Ada/Modula, two very uncommon languages, seems arbitrary and will trip up most learners, for example in its `case`/`of` statements instead of the more well known `switch`/`case`. And its pass-by-value/pass-by-reference system is something I still haven't gotten the hang of. But overall I still found it good, and most of these issues are nitpicks and quite understandable for a new language, and would probably be easy to overcome once one becomes familiar. I certainly found it faster to learn than golang, which is much more opinionated and arbitrary.

One key shortcoming is the lack of IDE support for debugging. For simple projects, you can get away with no debugging or just occasional print-statement debugging. Fantasy consoles don't have debugging but they are still [excellent for making small games](http://cxong.github.io/2020/06/fantasy-consoles-for-jams). But for anything more complex, a good debugger can often overcome an otherwise bad coding experience. For example, even though memory bugs are common in C, I've been able to work around them with conditional break statements in [my C games](https://github.com/cxong/cdogs-sdl). And the ability to modify values at runtime with dynamic languages is such a powerful debugging tool. Sadly this isn't available in nim. If nim were otherwise a pleasure to work with, this could be overlooked to a degree.

The big disappointment however is with the lack of a good game framework in nim. As of writing, the [list of game frameworks and engines for nim](https://github.com/ringabout/awesome-nim#game-frameworks) is a modest collection of barely-actively-maintained wrappers around SDL. This is ok for my purposes since I'm interested in 2D game development, and SDL is mostly fine. The standout in this list is [nico](https://github.com/ftsf/nico), a PICO-8 inspired engine, and this piqued my interest.

As previously mentioned, I'm a big fan of fantasy consoles. Their limitations also make them easy to pick up and learn, and limitations drive creativity. Nico not only couples a nice language with a great API, it is cross platform, including for the web, out of the box. Its feature list contains all the nice things that make fantasy consoles great.

Unfortunately it is not actively maintained, despite plenty of community interest. As of writing I still have several [pull requests](https://github.com/ftsf/nico/pulls) that have stayed open for months. Being far from mature, a lack of maintenance is a critical flaw. I want to [make games, not engines](https://seanmiddleditch.github.io/makes-games-not-engines-to-learn-engines/), which means fixing the issues myself is out of the question. Given that I was still learning the ropes with nim, this is an extra headache I did not need.

# What's Next

For now I'll be taking a short break in my quest to find the perfect games programming language. Plenty of options exist no matter your favourite language, although you'll be putting up with some limitations. I've been looking into [MoonScript](https://moonscript.org) + love2D lately. Coupling a cool language made by a [game dev's game dev](https://leafo.net), with a venerable 2D games framework, this makes a promising combo. A lot of features are missing however, so I'm not diving in head first. If I do ever jump into a new language, I'll be sure to keep my experiences with nim in mind, now that I have a better idea of what makes or breaks a language for games programming.
