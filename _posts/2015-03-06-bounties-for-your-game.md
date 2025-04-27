---
layout: post
title: "Bounties for your game"
date: 2015-03-06
comments: true
---

Many open source projects are supported by bounties - cash rewards for specific work done. Have you ever wondered about doing so for games? Well I did, and tried it with [C-Dogs SDL](http://cxong.github.io/cdogs-sdl/), and it was _awesome_.

## The Bounty

A month or so ago I looked into open source bounties. I knew that for very popular projects, businesses used bounties to fund the development of features. The sum of self-interested funding improved the overall project, benefiting all users.

But not all projects are in this enviable place. Open source projects, like many things, follow a [power law distribution](https://en.wikipedia.org/wiki/Power_law): there are a few that get outsize attention, and a vast majority of mediocre ones languishing in one form or another. C-Dogs SDL is one of them, which gets a few drive-by contributions, but is mostly worked on by me alone. Will bounties help here, by attracting eyeballs, or even contributors who get things done?

<!--more-->

I found out more after settling on [Bountysource](https://www.bountysource.com/) as the funding platform. A first look confirmed my suspicions: most of the funding were for super-popular projects (like Firefox) or those that had strong commercial ties. For games this was even more stark; the only project bothering seems to be [OpenRA](http://www.openra.net/), one of the top open source games and much more notable than C-Dogs SDL. Either bounties just didn't work for small projects, or they do but most people either don't bother, or do it via other channels. I hoped it was the latter.

In the end I chose this task for the bounty: [**deploy binaries via Travis CI**](https://github.com/cxong/cdogs-sdl/issues/290). There were [plenty to choose from](https://github.com/cxong/cdogs-sdl/issues), but most weren't suitable; they were wishlist tasks that didn't have a clear scope, or required deep knowledge of the game code. This one however was almost perfect; it was small and required no code changes. Build and CI procedures were already set up and [well documented](https://github.com/cxong/cdogs-sdl/wiki#developers), so in theory it is just researching [Travis CI](https://travis-ci.org) docs and setting up config files. I posted a modest bounty, and waited.

The bounty languished in obscurity.

## The Contributor

One nice thing about GitHub is lots of analytics, including one for [traffic](https://github.com/cxong/cdogs-sdl/graphs/traffic), which shows how many views and clones you're getting, and from where. There were hardly any from Bountysource.

Enter [**William "meZee"**](https://github.com/meZee). After more than a month of inactivity, he got in touch out of the blue, when I had all but forgotten about the bounty. "Excellent!" I thought; it seems that bounties don't bring in visitors, except the ones that count: contributors.

And then, radio silence.

Open source development is a lonely endeavour. The freedom that authors grant to users contributes to this, since people can use, hack, extend, even fork without bothering the authors. Most work is done by unpaid volunteers, who pick up and drop projects on a whim. Did meZee just take a break? Silently drop the task because it was too hard, not worth it, or too boring? I had no way to tell.

One week later, a flurry of activity! It turns out that getting two cloud services (GitHub and Travis CI) to talk to each other can be fiddly - who knew! - but the task was done in short order. I got an annoying task done, meZee got some cash and knowledge, and he even wished to contribute more! I couldn't have wished for a better outcome.

## Do they work?

This was an excellent experience, if a bit belated. It is still early days though, but overall I'm very satisfied and will try bounties again. Time will tell whether bounties:

- attract other contributors, not just those motivated by the money
- attract users in general, by signalling that there is real dedication in a project
- discourage volunteer contributors, since they may as well wait for bounties to be posted

I believe that a lot of potential contributions are held back by small barriers, and most contributions are from extremely motivated and knowledgeable people. Perhaps in this case, the small bounty was enough to nudge one person into becoming a contributor, and that alone is worth the price. Bounties may have a long history but they still have a ways to go, as evidenced by the sparse project selection in Bountysource. But if more people jumped in, it has the potential to become a powerful form of crowdfunding. Is there a feature you want or an issue fixed in an open source project? Post a bounty; you may be pleasantly surprised.

## Lessons

- Open source projects progress at their own pace, as unpaid volunteers work from their free time, so _be patient_.
- If you want contributors, break down all the barriers, and even more! No one wants to spend days setting things up, learning a code base, and contributing changes, with no guarantee of it being accepted, so why should your potential contributors? Everyone wants to start small and test the waters, so place a high priority on removing barriers.
