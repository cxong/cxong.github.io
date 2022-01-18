---
layout: post
title: "RPG Game Loops"
date: 2022-01-16
comments: true
published: false
---
Role playing games come in many different flavours but the game loop is a common element in all of them. Whether the game is combat oriented, or it focuses on stats and progression, exploration, or story telling, almost all RPGs follow this simple loop:

![rpg loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rpg_loop.jpg)

The terms and mechanics may differ between games but the loop is the same. The dungeon may not be a literal dungeon, but a forest, ruins or wilderness.

What's interesting is how different RPGs use mechanics to compel players through this loop. Let's look at a few classic mechanics:

# Quests

Perhaps there wouldn't be much of a game if there no reason to enter the dungeon where you can get killed. Most RPGs would have a main quest, the [call to adventure](https://en.wikipedia.org/wiki/Hero%27s_journey#The_Call_to_Adventure) that compels the player to venture forth.

![yendor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/yendor.jpg)

But RPGs, especially Western ones, had lots of side quests, big and small, which give players a more immediate reason for fighting. They could be as mundane as killing 20 rats, or as involved as pulling off a heist.

> ![the ultimate heist](https://static.wikia.nocookie.net/elderscrolls/images/c/c0/The_Ultimate_Heist_Elder_Scroll.png/revision/latest/scale-to-width-down/699?cb=20130925090055)
> 
> In Oblivion, The Ultimate Heist is a [7-part quest](https://en.uesp.net/wiki/Oblivion:The_Ultimate_Heist) that involves stealing a unique item from the most heavily guarded location in the game.

Quests are extremely flexible and are only limited by the quest writer's imagination. They can direct the player to arbitrary places and perform arbitrary tasks, thereby showing parts of the game that the designer wants. In return, players want the quests to make sense in the game world, and reward them with game lore in addition to mechanical rewards. Players tend to look down on lazy, highly mechanical quests such as "kill X creatures" or "fetch some item".

Once quests are complete, the prospect of returning to the quest giver to collect the reward can be an incentive to return to town, so quests can work in both directions in the game loop.

# Energy

This is where dungeon fighting consumes a form of energy, which is replenished back in town. The most common is **health** or HP; fighting almost inevitably involves getting hurt, and the most effective way of getting healed is returning to town. A great example is in *Final Fantasy*: although alternate healing methods exist, resting at the town inn is always the cheapest option, by far. **Pokemon** takes this even further, with its free healing Pokemon-centers.

![ff4 hp](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ff4_hp.jpg)

Health is a great energy system because the penalties for losing it are harsh - your party dies and you lose the game! But it is not the only type of energy, and the penalties don't need to be as harsh for it to work. **Mana**, or MP, is also common. For magic-focused characters, fighting without mana is much harder, which is a strong incentive for returning to town.

# Encumbrance

Loot is a big part of many RPGs. Many older RPGs had limits on how many things a character to carry, due to technical constraints. But others had limits deliberately, so that characters could not loot items indefinitely, and must return to town to sell excess loot.

*Diablo*, more than any other RPG, [focuses on inventory management and looting](https://www.gamedeveloper.com/design/a-night-with-the-devil) to drive its game loop. A typical dungeon run will have the player pick up mostly useless items, return to town to sell them off, and only occasionally do other things typically done in RPG towns - heal and recover, buy restoration items, upgrade equipment. This focus on items was done to focus the game on the excitement of finding rare items.

![loot loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loot_loop.jpg)

Other RPGs, like *Fallout*, *The Elder Scrolls* and various *Dungeons and Dragons*-themed CRPGs use weight limits, coupled with the fact that stronger characters can carry more items, for more flavour.

As an alternative to energy systems, encumbrance has the advantage of not harshly penalising the player, but still simulating the fatigue of adventuring that feels thematically apt. The obvious downside is that the encumbrance system needs to be designed just right - the game must not give the player too much or too few loot items - otherwise, in the case of too much loot, it can make players feel obligated to return to town prematurely to avoid missing out on selling loot.

# Crafting and Identification

Crafting is a game mechanic that has grown popular in RPGs over time. It adds flavour to the game world, but also acts as an additional force on the RPG game loop, by making loot more valuable if it is taken outside the dungeon.

Consider in [*The Witcher*](https://witcher.fandom.com/wiki/The_Witcher_alchemy), where alchemical ingredients are usually harvested in the wilderness, but the player must [return to a safe resting zone](https://witcher.fandom.com/wiki/Meditation) in order to make potions, oils or bombs.

![craft loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/craft_loop.jpg)

As a general rule, crafting ingredients are virtually useless on their own, but are also hard to gather unless the player travels to many different locations. This creates a weak, bi-directional pull in the game loop - players are encouraged to return to town to create useful crafting items, but also to travel to different locations to gather more ingredients.

Incidentally, [item identification](https://tvtropes.org/pmwiki/pmwiki.php/Main/UnknownItemIdentification) - with roots going all the way back to table-top RPGs - is somewhat similar to crafting, in the sense that unidentified items are useless, giving an incentive to return to town to identify them and make them useful.

Compared to energy systems and encumbrance, the influence of crafting on player behaviour is very weak, since crafting ingredients are usually very lightweight, meaning players are free to hoard them and not go back to town just to consume those ingredients. Many crafting systems are secondary in nature, so that players can often ignore crafting altogether.

# Afterthoughts

After examining these different mechanics, all designed to keep players in a hamster-wheel-like loop of town-dungeon-town-dungeon, it may seen very arbitrary. Indeed, many RPGs have added quality-of-life conveniences designed to shorten this loop, reduce its urgency, or in some cases to skip it altogether. These include things such as:

- Fast travel / [town portals](https://diablo.fandom.com/wiki/Town_Portal)
- [*Torchlight's* pets](https://torchlight.fandom.com/wiki/Pets_(T1)) who can return to town to sell loot and buy potions on your behalf
- Item stashes, [pack mules](https://dungeonsiege.fandom.com/wiki/Pack_mule) to carry more loot
- Special items that replace town functions (full-healing items, identify scrolls)
