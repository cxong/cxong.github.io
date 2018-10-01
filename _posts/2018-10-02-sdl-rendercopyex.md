---
layout: post
title: "SDL_RenderCopyEx"
date: 2018-10-02
comments: true
---

SDL_RenderCopyEx is a function in SDL2 that allows you to rotate, scale and flip sprites. But how do you use it? I was wondering the same as I wanted to add [bullet trails to C-Dogs SDL](https://github.com/cxong/cdogs-sdl/issues/47). The [official documentation](https://wiki.libsdl.org/SDL_RenderCopyEx) tells you what parameters to use but not how they will look. So I just tried it out myself:

## [sdl2-rendercopyex-demo](https://github.com/cxong/sdl2-rendercopyex-demo)

This is a simple demo project which uses SDL_RenderCopyEx to rotate, scale and flip a sprite. There's also a `center` parameter which controls the center of rotation, which defaults to the center of the sprite you are rendering.

![sdl2-rendercopyex-demo](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sdl-rendercopyex.png)

Pretty simple, although you'll probably want some boilerplate code like I did:

	int render(
		SDL_Renderer *renderer, SDL_Surface *s, SDL_Texture *t,
		int x, int y, double angle, double sx, double sy, SDL_RendererFlip flip)
	{
		SDL_Rect dst;
		int res;
		dst.x = x - (s->w * sx) / 2;
		dst.y = y - (s->h * sy) / 2;
		dst.w = (int)(s->w * sx);
		dst.h = (int)(s->h * sy);
		return SDL_RenderCopyEx(renderer, t, NULL, &dst, angle, NULL, flip);
	}

Source code here: [https://github.com/cxong/sdl2-rendercopyex-demo/blob/master/main.c]