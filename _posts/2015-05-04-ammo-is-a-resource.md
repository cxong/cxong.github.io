---
layout: post
title: "Ammo is a Resource"
date: 2015-05-04
comments: true
published: false
---

The [latest release of C-Dogs SDL](http://cxong.github.io/cdogs-sdl/progress/2015/05/03/deathmatch.html) is ostensibly about the addition of *deathmatch* mode, and although it was the original goal and most notable feature, development took twice as long as previous releases, and largely for one reason: **ammo**. Before this, C-Dogs didn't have ammo, or in other words, C-Dogs had infinite ammo. *How could ammo be that hard to implement; surely it's just an extra counter?* I though the same, but I soon realised this:

**Ammo is a resource.**

And that leads to a heap of things related to *resource management*. The player must now contend with many more decisions:

- Which gun should I use? (some guns have rarer ammo)
- How should I engage enemies? (close-up saves ammo but is riskier; farther is safer but wastes ammo)
- Should I run away altogether and save ammo?
- Should I explore, and gamble on finding more ammo or having to use it up on new enemies?

And as a designer, you now have to contend with:

- Making sure the player is not too starved, or over-supplied
- Resetting the player with the right amount of ammo at key points
- Being careful not to railroad the player into a few play styles due to ammo supply

Of course there are great rewards for implementing ammo. It adds a layer of depth via the decision-making. It gives players an incentive to use different guns, as overusing their favourites will make them run out of ammo. But it's also an entire *game mechanic*, and for one that's so old and common, it's surprisingly hard to get right.

## Cyberdogs had ammo!

Fortunately, ammo in games is older than dirt, so there's plenty of examples of how ammo can work, when it doesn't, and what to watch out for. Most C-Dogs fans know that the game is actually a sequel to the very similar **Cyberdogs**, and it had ammo! But the two also play differently. Cyberdogs is slow, tense and methodical; enemies are very dangerous up close, pop out unexpectedly and you had to make your shots count. C-Dogs is sometimes like this too, but it is also fast and frantic, owing to new mechanics like sliding, open spaces, and of course - no ammo. Many players prefer Cyberdogs over C-Dogs for this reason.

TODO: insert screenshots here

How does Cyberdogs solve the ammo resource problem, that is, make sure the player's getting enough ammo, and not too much? **Armoury**. In between levels, the player can spend cash to buy guns and ammo, cash that is earned from completing objectives and killing enemies in the previous level. In a way it is an elegant solution, by fobbing off the problem to the player, who is now responsible for how much ammo to buy. This also acts as a meta-game: too little ammo is dangerous, but too much and you don't have enough cash to buy the goodies like extra lives and bigger guns. This mechanic is quite widespread too, from **shops in RPGs** to **loadout screens in mech games**.

But herein lies the problem: we're attempting to balance one mechanic by piling on more mechanics! Wasn't the point to make sure the player gets the right amount of ammo? Now we've added a *store*, *buying/selling*, *cash* and maybe more. Wouldn't this just make things more complex and hard to balance? Let's look at the ammo resource cycle here:

- Use ammo to kill enemies
- Kills earn cash
- Use cash to buy ammo

Can't we just cut out the middleman - cash - and keep things simple?

## Sources and Sinks

Not quite. The cycle misses some important details: you can *earn more money* by completing more objectives, and you can also *spend money on (expensive) guns*. These are crucial to keeping the Cyberdogs ammo/cash system balanced. In other words, *sources* make sure the economy is never low on cash since players can always go out of their way to obtain more, and *sinks* make sure there's never an overabundance of cash, by having big expensive items that the player can save up towards.

Once again, we can find examples in other genres, notably in RPGs, where there are plenty of sources and sinks to keep the cash economy healthy. If the player is short on cash, she can always farm for more gold, or explore dungeons more thoroughly to find expensive loot to sell. Many RPGs also have inventory limitations, which limits the amount of loot you can carry back to a store and sell; if the player is low on cash then she could make repeated trips to sell all the loot. On the other hand, if the player has too much cash, she could upgrade her equipment, which tends to be quite expensive. Most RPGs also feature magical or rare equipment that is obscenely expensive but provide marginal improvements over regular equipment. [This Gamasutra article on Diablo's item system](http://gamasutra.com/blogs/RadekKoncewicz/20141229/233271/A_Night_With_the_Devil.php) shows how all these aspects work together to create a sophisticated economy. In particular, most of your gear was from loot, shop equipment was extremely expensive, but still worthwhile since the loot was random and often made the player miss out on a particular kind of equipment.

So it is important to have multiple sources and sinks in your economy, and also to make these alternates less desirable, otherwise they distract from the main game. For example, grinding, farming and shuttling loot are reliable money-makers but they are often tedious and less fun than fighting enemies or completing objectives.

There's another lesson from RPGs too, and that is to **grow prices superlinearly**. That is, for bigger and better items, increase their price much more than usual. Ever wonder why the wooden sword costs 10G, the iron sword 100G, and the silver sword 1000G, even though each one is only a little better than the last? This is to stop players from hoarding cash and making later segments of the game too easy because they can buy the best gear in one go. It's a neat trick to prevent snowballing and make balancing much easier, by making those upgrades reliable sinks.
