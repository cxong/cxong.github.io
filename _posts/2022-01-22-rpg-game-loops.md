---
layout: post
title: "RPG Game Loops"
date: 2022-01-22
comments: true
published: true
---
Role playing games come in many different flavours but the game loop is a common element in all of them. Whether the game is combat oriented, or it focuses on stats and progression, exploration, or story telling, almost all RPGs follow this simple loop:

![rpg loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/rpg_loop.jpg)

The terms and mechanics may differ between games but the loop is the same. The dungeon may not be a literal dungeon, but a forest, ruins or wilderness.

What's interesting is how different RPGs use mechanics to compel players through this loop. Let's look at a few classic mechanics:

# Quests ❗️

Perhaps there wouldn't be much of a game if there no reason to enter the dungeon where you can get killed. Most RPGs would have a main quest, the [call to adventure](https://en.wikipedia.org/wiki/Hero%27s_journey#The_Call_to_Adventure) that compels the player to venture forth.

![yendor](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/yendor.jpg)

But RPGs, especially Western ones, have lots of side quests, big and small, which give players a more immediate reason for fighting. They could be as mundane as killing 20 rats, or as involved as pulling off a heist.

> ![the ultimate heist](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/the_ultimate_heist.png)
> 
> In Oblivion, The Ultimate Heist is a [7-part quest](https://en.uesp.net/wiki/Oblivion:The_Ultimate_Heist) that involves stealing a unique item from the most heavily guarded location in the game.

Quests are extremely flexible and are only limited by the quest designer's imagination. They can direct the player to arbitrary places and perform arbitrary tasks, thereby showing parts of the game that the designer wants. In return, players want the quests to make sense in the game world, and reward them with game lore in addition to mechanical rewards. Players tend to look down on lazy, highly mechanical quests such as "kill X creatures" or "fetch some item".

Once quests are complete, the prospect of returning to the quest giver to collect the reward can be an incentive to return to town, so quests can work in both directions in the game loop.

# Energy 💚🏥

This is where dungeon fighting consumes a form of energy, which is replenished back in town. The most common is **health** or HP; fighting almost inevitably involves getting hurt, and the most effective way of getting healed is returning to town. A great example is in *Final Fantasy*: although alternate healing methods exist, resting at the town inn is always the cheapest option, by far. **Pokemon** takes this even further, with its free healing Pokemon-centers.

![ff4 hp](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/ff4_hp.jpg)

Health is an unforgiving energy system because the penalties for losing it are harsh - your party dies and you lose the game! But it is not the only type of energy, and the penalties don't need to be as harsh for it to work. **Mana**, or MP, is also common. For magic-focused characters, fighting without mana is much harder, which is a strong incentive for returning to town.

A side note on restoration items: they can alleviate the harshness of energy penalties, but usually they are expensive, so that they don't completely overwhelm the energy system.

# Encumbrance 🧳

Loot is a big part of many RPGs. Many older RPGs had limits on how many things a character could carry, due to technical constraints. But others set limits deliberately, so that characters could not loot items indefinitely, and must return to town to sell excess loot.

*Diablo*, more than any other RPG, [focuses on inventory management and looting](https://www.gamedeveloper.com/design/a-night-with-the-devil) to drive its game loop. A typical dungeon run will have the player pick up mostly useless items, return to town to sell them off, and only occasionally do other things typically done in RPG towns - heal and recover, buy restoration items, upgrade equipment. This focus on looting was done to focus the game on the excitement of finding rare items.

![loot loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/loot_loop.jpg)

Other RPGs, like *Fallout*, *The Elder Scrolls* and various *Dungeons and Dragons*-themed CRPGs use weight limits, coupled with the fact that stronger characters can carry more items, for more flavour.

Compared to energy systems, encumbrance has the advantage of not harshly penalising the player, but still simulating the fatigue of adventuring that feels thematically apt. The obvious downside is that the encumbrance system needs to be designed just right - the game must not give the player too much or too few loot items - otherwise, in the case of too much loot, it can push players to return to town too often to avoid missing out on selling loot.

# Crafting and Identification 🔨

Crafting is a game mechanic that has grown popular in RPGs over time. It adds flavour to the game world, but also acts as an additional force on the RPG game loop, by making loot more valuable if it is taken outside the dungeon.

Consider in [*The Witcher*](https://witcher.fandom.com/wiki/The_Witcher_alchemy), where alchemical ingredients are usually harvested in the wilderness, but the player must [return to a safe resting zone](https://witcher.fandom.com/wiki/Meditation) in order to make potions, oils or bombs.

![craft loop](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/craft_loop.jpg)

As a general rule, crafting ingredients are virtually useless on their own, but are also hard to gather unless the player travels to many different locations. This creates a weak, bi-directional pull in the game loop - players are encouraged to return to town to create useful crafting items, but also to travel to different locations to gather more ingredients.

Incidentally, [item identification](https://tvtropes.org/pmwiki/pmwiki.php/Main/UnknownItemIdentification) - with roots going all the way back to table-top RPGs - is somewhat similar to crafting, in the sense that unidentified items are useless, giving an incentive to return to town to identify them and make them useful.

Compared to energy systems and encumbrance, the influence of crafting on player behaviour is very weak, since crafting ingredients are usually very lightweight, meaning players are free to hoard them and not go back to town just to consume those ingredients. Many crafting systems are secondary in nature, so that players can often ignore crafting altogether.

# Afterthoughts

After examining these different mechanics, all designed to keep players in a hamster-wheel-like loop of town-dungeon-town-dungeon, it may seem arbitrary and player-hostile. Indeed, many RPGs have added quality-of-life conveniences designed to shorten this loop, reduce its urgency, or in some cases to skip it altogether. These include things such as:

- Fast travel / [town portals](https://diablo.fandom.com/wiki/Town_Portal)
- [*Torchlight's* pets](https://torchlight.fandom.com/wiki/Pets_(T1)) who can return to town to sell loot and buy potions on your behalf
- Item stashes, [pack mules](https://dungeonsiege.fandom.com/wiki/Pack_mule) to carry more loot
- Special items that replace town functions (full-healing items, identify scrolls)

So why do we even need this loop, why not keep the player in combat the whole time, and allow them to do everything there?

## Delayed Gratification

A lot of the "pull"-type mechanics give the player something to look forward to, by delaying the immediate reward. Items that must be crafted elsewhere, rare items that need to be fixed or unlocked, completed quest rewards that need to be completed, these all act as mini-cliffhangers, something to keep the player in the game, or for them to look forward to once they return.

## Pacing

Games need a regular pacing in order to keep the player engaged, without being bored or fatigued.

> [pacing in games fills] a very important role: it helps the player stay in "the flow". ...
> The clear [rhythm] it gives to the game helps [players] learn to anticipate challenges and get ready right on time. Providing relief in regular intervals prevents players from getting tired too quickly. Sudden surges of intensity supply them with adrenaline rushes, and the increasing wave structure makes sure they have time to recover afterwards.
>
> [Beyond Pacing: Games Aren't Hollywood](https://www.gamasutra.com/view/feature/4032/beyond_pacing_games_arent_.php?print=1)

Towns in RPGs are an effective way to serve as lulls in the action, so the player can mentally take a break, reflect, and prepare for the next surge in action.

## Composite Game Design

RPGs can be seen as an example of a [composite game](http://thegamedesignforum.com/features/GDH_2.html), a combination of story-telling and turn-based combat. It is therefore important to have different sections that showcase one or the other.

Indeed, the grandfather of RPGs, [Dungeons & Dragons](https://en.wikipedia.org/wiki/Dungeons_%26_Dragons) had [roots in wargames](https://en.wikipedia.org/wiki/Chainmail_(game)), and was created by adding role-playing elements like character creation and storytelling to wargames.

> ![wargames](https://jdglasco.files.wordpress.com/2014/04/polemosiln1888.jpg)
>
> D&D's combat was based off a medieval wargame. Wargames have a rich and long history, going back centuries as [a tool to train officers](https://en.wikipedia.org/wiki/Kriegsspiel). Some have kept this tradition by focusing on realism. Others streamlined the mechanics to make it more fun and interesting, for example by adding fantasy elements.

Just as in composite games where lessons learned from one genre can be used to solve problems in the other, RPGs often use story-telling elements to influence combat, and vice versa, to create a genre that is greater than the sum of its parts. Great RPGs often have superb examples of this inter-dependence of genres. New items, mechanics or characters are introduced via the story. Players in turn can often influence the story or game world by taking on different quests, representing different combat encounters, or sometimes even by performing combat in different ways. This way, players engage with the game on multiple levels.

> ![FF4 Cecil](https://lparchive.org/Final-Fantasy-IV/Update%2011/19-image022.png)
>
> In Final Fantasy 4, the main character undergoes a permanent class change as part of a key story arc, tying his character's moral redemption to a big change in gameplay.

The separation of town and dungeon segments becomes clear. It is hard to tell an engaging story while the player is focused on combat. RPGs therefore need a safe, slow-paced town segment to develop and engage with the story, such as taking on quests and tweaking their characters, and a dangerous, fast-paced dungeon segment to fully explore the combat impacts of their choices.