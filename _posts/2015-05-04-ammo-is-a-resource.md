---
layout: post
title: "Ammo is a Resource"
date: 2015-05-04
comments: true
published: false
---

The [latest release of C-Dogs SDL](http://cxong.github.io/cdogs-sdl/progress/2015/05/03/deathmatch.html) is ostensibly about the addition of *deathmatch* mode, and although it was the original goal and most notable feature of this release, development took twice as long as previous releases, and largely for one reason: **ammo**. Before this release, C-Dogs didn't have ammo, or in other words, C-Dogs had infinite ammo. *How could ammo be that hard to implement; surely it's just an extra counter?* I though the same, but I soon realised this:

**Ammo is a resource.**

And that leads to a heap of things related to *resource management*. The player must now contend with many more decisions:

- Which gun should I use? (some guns have rarer ammo)
- How should I engage enemies? (close-up saves ammo but is riskier; farther is safer but wastes ammo)
- Should I run away altogether and save ammo?

And as a designer, you now have to contend with:

- Making sure the player is not too starved, or over-supplied
- Resetting the player with the right amount of ammo at key points
- Being careful not to railroad the player into a few play styles due to ammo supply

Of course there are great rewards for implementing ammo. It adds a layer of depth via the decision-making. It gives players an incentive to use different guns, as overusing their favourites will make them run out of ammo. But it's also an entire *game mechanic*, and for one that's so old and common, it's surprisingly hard to get it right.
