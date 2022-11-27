---
layout: post
title: "Fantasy Consoles for Jams"
date: 2020-06-27
comments: true
published: true
---
I've done a lot of game jams and have used many engines and frameworks in these jams. They all have pros and cons, but lately, I've been using fantasy consoles as my platform of choice, and I think you should too - they are fantastic for game jams.

What are [fantasy consoles](https://www.gamefromscratch.com/post/2017/06/01/Fantasy-Console-Development.aspx)? In short, they are virtual consoles that mimic retro computers and their limitations, but also provide a complete game development environment. Within the same application, you can draw simple sprites, compose chiptune music and sound effects, and write code using a limited API. Its severe limitations are also its appeal; it's not only a piece of cake to pick up and learn, but the limitations encourage creativity. [PICO-8](https://www.lexaloffle.com/pico-8.php) is the most popular, but there are [many others to choose from](https://paladin-t.github.io/fantasy/index).

![PICO-8](https://www.lexaloffle.com/gfx/jelpi_demo.gif)

One of the most important factors when choosing a platform for jams is development speed. You want to be able to put something playable together as quickly as possible, as time is *the* scarce resource. Here the popular engines do very well; Unity, for example, has a lot of functionality built-in, or easily accessed via its asset store, so you can quickly piece something rough together.

Fantasy consoles represent an alternate approach - with limitations and fewer tools at your disposal, there is less time wasted in choosing how to make your game and more time on focusing on gameplay and making something fun. It's easy and quick to put together something playable, so you can start iterating and polishing on top of a solid base.

Here I'll show you my weapon-of-choice: [TIC-80](https://tic80.com).  It's very similar to other popular fantasy consoles, so the experience is transferrable. Within the same tool, you can:

- Code in [Lua*](# "TIC-80 supports a few other languages, like JavaScript, Moonscript, Wren and Fennel"), against a simple sprite-and-tile based 2D API
- Draw sprites and tiles using a 16-colour palette
- Create chiptune sound effects and music with up to 4 channels in a simple tracker
- Edit tilemaps
- Export to HTML

![TIC-80](https://user-images.githubusercontent.com/1101448/29687467-3ddc432e-8925-11e7-8156-5cec3700cc04.gif)

## Coding

![TIC-80 code editor](https://raw.githubusercontent.com/wiki/nesbox/tic.computer/images/code.gif)

TIC-80 primarily uses Lua for coding, but you get other language choices - Moonscript, JavaScript, Wren and Fennel. I like Moonscript the best because it's like Lua without the bad parts. Its class syntax is excellent, something that sucks in Lua.

As a fantasy console, the editor window is tiny. While charming, I highly recommend getting the pro version for $5, which lets you code using any text editor.

This way, the entire game fits in a single text file, even graphics and sound, which is great for version control and collaboration between your artists and musicians. No more headaches from merging everyone's work - it's just lines of code in a file!

![TIC-80 pro code](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tic80_pro_code.png)

## Graphics

TIC-80 has a mainly sprite-based 2D API, with built-in sprite editor and tilemap editor. They're nothing to write home about, and get the job done.

![TIC-80 sprite editor](https://raw.githubusercontent.com/wiki/nesbox/tic.computer/images/sprite.gif)

Worth mentioning are the shape drawing functions available. In addition to the expected lines, rectangles and circles, you can also draw textured triangles, and which some enterprising folks have made 3D engines out of this. Not that you should do this for your jams, but they're nifty tools to have. Check out the [API](https://github.com/nesbox/TIC-80/wiki#functions) for more details.

![TIC-80 sprite rotation](https://user-images.githubusercontent.com/1101448/31165848-44de7a8a-a8f5-11e7-9832-da9b7ce4d8f1.gif)

## Sound & Music
Sound and music work differently in TIC-80 than you might be used to, but in a way that makes it quite fun to use. In essence, you build these up in layers:
- Create **waveforms** - you get 16 of these. You get the standard square, triangle, sawtooth and noise waves, but you can also draw your own, something which few other tools let you do.

  ![TIC-80 waveform editor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tic80_waveform.png)
- Edit **envelopes** - these are the sound effects, defined as four parameters: waveform, volume, arpeggio, and pitch. It's a bit hard to explain, but here are some examples of things you can do:
  - Create a plucked-instrument with a sharp attack, by starting with  a noise wave
  - Fade in or out using the volume envelope
  - Create a melodic chime with the arpeggio envelope
  - Create a vibrato effect with the pitch envelope

  ![TIC-80 envelope editor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tic80_envelope.png)
- Edit **music**. Here the editor is a more conventional tracker - you use instruments (which are the sound effects created earlier) and lay notes on patterns. Patterns are per-channel and can be reused, which is handy because you only get 60 of them.

  ![TIC-80 music editor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/tic80_music.png)

I've found it handy to keep a notebook of all the sound effects and pattern numbers used, as this is perhaps the clunkiest part of TIC-80.

## Exporting
Exporting is probably the best part of TIC-80 for jams - how easy it is to export games from it. You can:

- Save the game as a `.tic` cartridge, loadable by anyone running TIC-80
- Export to a single `.html` file using `export html`
- Export to an executable using `export native`
- Take a screenshot using <kbd>F8</kbd>
- Record a gif using <kbd>F9</kbd>

So preparing a jam submission is a cinch. What might take an hour messing around with screen recorders, exporters and so on, take only minutes with TIC-80. Take screenshots and gifs early and often and tweet/blog your progress!

## Try it out!
That's it! Fantasy consoles are so simple to learn, use, and are perfect for jams. Here are some games I've made with TIC-80:

- [Dunkman](https://tic80.com/play?cart=1179)
- [Grow Quickly](https://tic80.com/play?cart=964)

And you can even take a look at the source code and how the game was put together - these fantasy consoles are editor-and-player all-in-one.

Try it out and happy jamming!