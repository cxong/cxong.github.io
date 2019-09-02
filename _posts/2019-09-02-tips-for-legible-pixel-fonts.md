---
layout: post
title: "3 Tips for Super Legible Pixel Fonts"
date: 2019-09-02
comments: true
published: true
---

Recently I restored the font used in [C-Dogs SDL](https://cxong.github.io/cdogs-sdl/) to the one used in the original [C-Dogs](https://en.wikipedia.org/wiki/C-Dogs). The reason why they were replaced in the first place was because the original graphics weren't open source, so I was looking for alternatives. A few years back [the author of C-Dogs agreed to open source the original graphics](https://cxong.github.io/cdogs-sdl/news/2016/05/07/c-dogs-is-now-free.html), and I've only just gotten around to restoring the font.

But that's not what this post is about! I want you to take a look at the [C-Dogs font](https://opengameart.org/content/c-dogs-font-3x5):

![](https://opengameart.org/sites/default/files/Screen%20Shot%202016-11-03%20at%2010.36.00%20PM.png)

It's actually a pretty neat font. Most of the letters are just 3x5 pixels (some wider or taller), but with a few tricks they look super legible for their size. Here I'll show you some of the tricks used to make pixel fonts really legible.

## Tom Thumb

Let's back up a bit. While I was looking for a free font, I had some tough requirements. The font couldn't be bigger than 3x5 pixels,  otherwise the UI in the game will break. That's a really small size to work with, and most pixel fonts struggle at that size.

> ![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/bitmap_fonts.png)
> Most [pixel fonts](https://opengameart.org/content/fonts-0) are around the 8x8 size

I managed to find a contender in a surprising place; someone made some 3x5 fonts for use on [PDAs](https://en.wikipedia.org/wiki/PalmPilot), where screens could be 160x160 pixels total. The font was jokingly called ["Tom Thumb"](https://robey.lag.net/2010/01/23/tiny-monospace-font.html):

![](https://robey.lag.net/images/tom-thumb-new.png)

![](https://robey.lag.net/images/tom-thumb-comparison.png)

This was the right size, but it's not nearly as legible as the C-Dogs font. Some letters are so compressed it's hard to tell what they are without context (take a look at "M" and "N" for example). Tom Thumb, being made for a terminal, strictly needed to be monospace whereas with C-Dogs SDL we could have variable-width fonts. Here's some tricks we used to enhance Tom Thumb:

## Add Outlines

For games, you don't really know where your text could end up. It could be over a dark or light background, coloured, or with a bunch of busy game objects moving in the background. A plain-white text will get lost over a bright background and so forth.

A really cheap solution is to just add an outline! And if you overlap the outline it doesn't even need to add to the width of your font.

![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/font_outline.png)

## Use Greys

Before the proliferation of 4k displays, folks have come up with some clever ways to make screen fonts legible. Here's a simple approach using antialiasing:

![](https://www.nomensa.com/blog/sites/default/files/blog/assets/uploads/2011/03/img-2.jpg)

We can copy the same idea on pixel fonts and use some greys in the font to hint at curves.

![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/font_greys.png)

Look at how the "o"s become much rounder, and the "W"'s shape is much improved.

## Make it Proportional

We didn't get to this point with Tom Thumb, but since C-Dogs SDL can handle proportional fonts, why not use the extra horizontal space available? It can really improve wide letters like "W" and "M".

![](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/font_proportional.png)

Here I've just replaced the "w" with one from C-Dogs. Doesn't it look great?

If you're interested in Tom Thumb, both the original and our enhanced version, you can find it [here on OGA](https://opengameart.org/content/tom-thumb-tiny-ascii-font-3x5).
It's got a great range actually, with lots of [Latin1 characters](https://en.wikipedia.org/wiki/ISO/IEC_8859-1).

And if you're making pixel fonts yourself, why not use some of these tips?