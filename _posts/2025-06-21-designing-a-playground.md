---
layout: post
title: Designing a Great FPS Playground
date: 2025-06-21
comments: true
published: true
---

<style>
table, th, td {
  border: 1px solid black;
}
</style>

Back in the day I played a lot of online FPS games, but one really stuck with me and earned most of my devotion: [Enemy Territory](https://en.wikipedia.org/wiki/Wolfenstein:_Enemy_Territory), the free (and now open source) team, class and objective-based game. I remember during a late night session, one of my clan-mates said:

> congusbongus always goes for the objectives eh?

It was the first time I really thought about how people play the same game in different ways, and enjoy different aspects of it. Later I would learn about [Bartle's player types](https://en.wikipedia.org/wiki/Bartle_taxonomy_of_player_types) and how that applies to all sorts of multiplayer games, and mechanics like different player classes or even weapon types clearly caters to different kinds of players. But herein lies a problem: how do you get different kinds of players to come together and interact, instead of running off doing their own thing? Players like me would do the objectives because that's the goal of the game, after all, but what about players who don't care about that, and instead might grief, camp or just mess around?

Plenty of mechanics prevent the most antisocial of behaviours. Spawn protection prevents the worst kinds of spawn camping, and limited ammo prevents players from camping advantageous terrain indefinitely. But I want to look at how map design can focus the action, provide good pacing, and enable dynamic gameplay so different kinds of players can shine and enjoy the game in their own ways. For that we need to first look at the classic Enemy Territory map [Supply Depot](https://et.trackbase.net/map/8/).

<!--more-->

<hr>

<a
    href="https://et.trackbase.net/img/etmap/thumb/8supply_cc_thumb.jpg"
    data-fancybox="gallery-supply"
    data-caption="The overhead map of Supply Depot. The Allies start in the west building and attack up the road to a roadblock on the north. Then they continue South to a large walled complex, to steal gold and take it back up the road and escape to the east.">
![Command Map](https://et.trackbase.net/img/etmap/thumb/8supply_cc_thumb.jpg)
</a>
<a
    href="https://et.trackbase.net/img/etmap/8supply1.jpg"
    data-fancybox="gallery-supply"
    data-caption="The Allies start with their truck (right), and attack a bunker gate (left). They must plant dynamite to blow the gate open, but the bunker provides great protection and firing lines for the defending Axis.">
![First Gate](https://et.trackbase.net/img/etmap/thumb/8supply1_thumb.jpg)
</a>
<a
    href="https://et.trackbase.net/img/etmap/8supply2.jpg"
    data-fancybox="gallery-supply"
    data-caption="After the bunker gate (right), the Allies continue up the road and must blow up a second, depot gate (left, behind trees). Like the bunker, the depot walls provide great firing positions for the defenders.">
![Depot Gate](https://et.trackbase.net/img/etmap/thumb/8supply2_thumb.jpg)
</a>
<a
    href="https://et.trackbase.net/img/etmap/8supply3.jpg"
    data-fancybox="gallery-supply"
    data-caption="The Allies then bring the truck to the back of the depot and load the gold into the truck using the crane. However the crane controls are deep within the depot building, which is easily defensible by the Axis.">
![Depot crane](https://et.trackbase.net/img/etmap/thumb/8supply3_thumb.jpg)
</a>

Supply Depot is perhaps the most popular competition map, and certainly the [most popular custom map](https://et.trackbase.net/maplist/). It is played with an attacking team (Allies) and a defending team (Axis). The Allies must escort a truck - which moves on a pre-defined route - through first a bunker gate, then a depot gate, steal gold crates from the depot and load them into the truck, and finally escort the truck back out and to the escape point. This multi-stage structure gives the game a series of [rising-and-falling action points](https://www.masterclass.com/articles/freytags-pyramid) that keep the game moving in a very exciting way. Objectives in Enemy Territory aren't usually straightforward: for example, to blow up a gate, the players must first plant dynamite, but then guard it for 30 seconds lest it is defused. Thus we have the following dramatic structure:

1. Allies face a heavily-defended bunker gate (exposition)
2. Allies beat back the Axis and plant dynamite at the bunker gate (rising action)
3. Allies defend the dynamite as the Axis fights to push them back (climax)
4. The dynamite explodes, opening the way to the next area (falling action)
5. The Axis fall back to defend the depot gate (denouement)

And this structure repeats twice more, at the depot gate and crane controls, and to a lesser extent the final chase of the truck as it reaches the exit.

From what I've described, you'd think that this map is fantastic and provides exciting gameplay all the time. This is simply not true. While it is a great _competition_ map, as a public map it is one of the less popular, for two main reasons:

- The objectives require a high level of teamwork at personal risk
- Going alone and taking your own non-objective tasks is ineffective

So as an individual player, your experience is likely to be: go for the objective, at great personal risk, and fail miserably, or try taking a very long sneaky path, but you don't achieve much besides get a few extra kills, and it feels boring to do so. The map is not well designed for less skilled, individual players, who need to be able to enjoy the game in their own way. The map is more like a (team) obstacle course, instead of a playground.

<hr>

Let's look at a pair of maps to see a different way whereby a map can produce dynamic gameplay, from [Counter-Strike](https://en.wikipedia.org/wiki/Counter-Strike): [de_dust](https://counterstrike.fandom.com/wiki/Dust) and [de_dust2](https://counterstrike.fandom.com/wiki/Dust_II).

<a
    href="http://games.parsons.edu/wp-content/uploads/2012/04/dust_floorplan.jpg"
    data-fancybox="gallery-dust"
    data-caption="Overhead map of de_dust. Terrorists spawn in the left courtyard, and Counter-Terrorists spawn in the right, with bomb site A in the north and B right where CTs spawn. It soon becomes apparent that the two choke points are the dark corridors in the middle and the underpass in the south.">
![de_dust floorplan](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/de_dust-overview_th.jpg)
</a>
<a
    href="https://games.parsons.edu/wp-content/uploads/2012/04/dust1.jpg"
    data-fancybox="gallery-dust"
    data-caption="Entrance to the underpass in de_dust. Millions of hours were spent slaughtering virtual players in this tiny map.">
![de_dust underpass entrance](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/dust1_th.jpg)
</a>

Dust 2 needs no introduction, being one of the most popular maps in one of the most popular FPS game franchises. Its predecessor Dust 1 (a.k.a. de_dust) was also notorious in its day, also one of the most popular (and often most hated) maps in the game's early years. [If you've played it you'll know this well](https://games.parsons.edu/de_dust/), but even if not, a little study of the floor plan will reveal why it is so controversial: the map design forces players into two easily defensible chokepoints, and unless there's a spirited assault with a generous amount of luck, the game devolves into a spammy, chaotic mess of a firefight, with little teamwork to speak of and random deaths galore. In other words, it forces players to play in one specific way, and even if you're not on the receiving end of the meat grinder, the game quickly becomes monotonous.

Contrast this with de_dust2, which has an ingenious map layout. [As with most bomb defuse maps](https://www.gamedeveloper.com/design/a-cs-go-level-design-concept-the-pathways), there are two bomb sites where the Terrorists (T) can plant a bomb to win, but the Counter-Terrorists (CT) have the advantage of being closer to the bomb sites, and can set up a defense ahead of time. The one tactical edge Ts have is they can all attack one site, whereas CTs need to potentially split their players among two, unless they read their opponents correctly. In game-theoretic terms we have this payoff matrix:

| CT / T                   | All attack A    | All attack B    | Attack opportunistically |
| ------------------------ | --------------- | --------------- | ------------------------ |
| All defend A             | CT wins         | CT loses        | Outcome uncertain        |
| All defend B             | CT loses        | CT wins         | Outcome uncertain        |
| Defend opportunistically | CT disadvantage | CT disadvantage | CT wins                  |

> [RUSH B](https://knowyourmeme.com/memes/rush-b)

In other words for either team there is no [dominant strategy](https://en.wikipedia.org/wiki/Strategic_dominance) as the payoff is roughly equal no matter what they do. They can both gamble and go to one bomb site, and win/lose based on what the other team did, or they can try to hedge their bets and try to defend both (or some variant like try to control the middle ground), which is harder to do and puts them at a disadvantage if the other team was more decisive. So the game has a rock-paper-scissors like nature, and every round can be different than the last, keeping things fresh and dynamic.

Of course the devil is in the details, as a lot of the payoff values depend on things like how quickly can teams go from one bomb site to the other (rotation time), how defensible each site is, how easy it is to scout what the other team is doing, how effective delay or denial mechanics like smoke grenades are in the map and so on. Small factors can easily tip the balance of the map, changing the effective strategies and making the game less fun.

<hr>

A game like Counter-Strike is in some ways easy to design for, since the game is constrained both in space (small maps, one objective) and time (short time limit per round). In more complex games, with larger maps, multiple objectives and stages, and long round times, it can be hard to prevent players running off doing their own thing, while still letting them play the game in their own play-style.

Enter Team Fortress 2's [payload game mode](https://wiki.teamfortress.com/wiki/Payload). This game, perhaps more than any other, set the blueprint for how the combination of [hero shooter](https://en.wikipedia.org/wiki/Hero_shooter) + well designed map mechanics can focus gameplay into one main battleground, while still spanning a large total space. For those uninitiated, in the payload game mode, the attacking team must escort a slow-moving vehicle past a series of checkpoints, and the defending team have a defender's advantage, especially when it comes to the "payload", where escorts are particularly vulnerable to being shot at from all directions. The payload is the natural focal point of the game, even as it traverses the length of the level.

<a
    href="https://www.escapistmagazine.com/wp-content/uploads/2023/07/Team-Fortress-2-Best-Payload-Maps-Badwater-Basin.jpg?w=1024&resize=1024%2C576"
    data-fancybox="gallery-payload"
    data-caption="Screenshot of Badwater Basin, perhaps the best payload map in TF2.">
![Badwater Basin](https://www.escapistmagazine.com/wp-content/uploads/2023/07/Team-Fortress-2-Best-Payload-Maps-Badwater-Basin.jpg?w=1024&resize=400%2C240)
</a>
<a
    href="https://www.escapistmagazine.com/wp-content/uploads/2023/07/Team-Fortress-2-Best-Payload-Maps-Gold-Rush.jpg?w=1024&resize=1024%2C576"
    data-fancybox="gallery-payload"
    data-caption="Screenshot of Gold Rush, one of the first payload maps in the game. TF2 did not come out with payload maps but added it soon after, and Gold Rush remained a favourite as it went through many changes.">
![Gold Rush](https://www.escapistmagazine.com/wp-content/uploads/2023/07/Team-Fortress-2-Best-Payload-Maps-Gold-Rush.jpg?w=1024&resize=400%2C240)
</a>

Despite being a natural meat-grinder, how does the game encourage players to jump in? In a number of clever ways:

- The payload itself slowly replenishes attackers standing next to it, making it a natural place to hang out
- The payload stops moving if a defender is next to it, which means the fastest way to stop it is for a defender to jump into the fray
- Multiple attackers can push the payload faster, encouraging more players to gather around it
- If left unattended, the payload rolls slowly backwards, encouraging attackers not to neglect it

Furthermore, the distinctive player characters have clear strengths and weaknesses, which encourages teammates to stick together, even if they are not explicitly a support class. The game is extremely sticky in this way, bringing players together into a chaotic arena.

<hr>

Across games and generations, one challenge has remained constant: how do you design maps and mechanics that cater to many kinds of players, while still keeping them in the same game? Great competitive maps like Supply Depot reward tight teamwork but can alienate casual or solo players. Maps like de_dust2 embrace unpredictability, creating freshness through tactical ambiguity. And TF2’s payload mode shows that, with the right incentives, even chaos can be fun and focused.

Whether you’re designing a symmetrical shooter or a hero-based brawler, the goal should be the same: build a playground where every kind of player feels they can contribute - and where the game naturally pulls them toward each other.
