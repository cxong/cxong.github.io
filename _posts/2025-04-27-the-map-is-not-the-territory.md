---
layout: post
title: The Map Is Not the Territory
date: 2025-04-27
comments: true
published: true
---

Everyone loves game maps. Especially when it comes to [large game worlds](https://cxong.github.io/2023/11/big-without-scale), there's nothing quite like looking at a mesmerising map filled with awesome detail, and imagine (re)inhabiting parts of this virtual world. When studying a map of a game that I've spent dozens if not hundreds of hours in, I often get a sense of both familiarity and strangeness. It's not just that the map shows a different perspective of the same world I experienced as a game avatar, but that the map misrepresents the player experience world in fundamental ways.

<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/magus_map_drawn.jpg"
    data-fancybox="gallery-map">
![Magus game map, drawn](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/magus_map_drawn_th.jpg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/MagusPreservation/master/map.png"
    data-fancybox="gallery-map">
![Magus game map](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/magus_map_th.png)
</a>

> My love of game maps drove me to hand-draw this map of the obscure DOS roguelike _Magus_ recently. From <https://mastodon.gamedev.place/@congusbongus/111900901099931635>

# 🇯🇵

There are two good reasons why almost all travel itineraries for first-time visits to Japan will involve Tokyo and Osaka: they are very well served by high speed rail, and both are large cities with lots of things to see and do. While starting a tour in Tokyo makes sense, there are many good travel locations much closer to Tokyo - in Greater Tokyo or not far out - that often get neglected. This discrepancy becomes apparent when you start looking at a map of Japan. Of course, the reason is obvious when you consider transit, and the personal experience of actually doing the travelling, but the map won't make this apparent at all.

> <a href="https://www.voyagedmagazine.com/wp-content/uploads/2015/07/Japan-Itinerary-Map.jpeg.webp"><img src="https://www.voyagedmagazine.com/wp-content/uploads/2015/07/Japan-Itinerary-Map.jpeg.webp" alt="Japan travel itinerary map" width="400px" /></a>
>
> With few exceptions, first-time Japan travel itineraries will include the Tokyo-Osaka rail corridor, occasionally including day trips from either city. Destinations outside these areas sadly get neglected. From: <https://www.voyagedmagazine.com/how-to-plan-your-first-trip-to-japan-travel-guide-itinerary/>

<!--more-->

You can try this exercise with any new location, like a country or a city. Look at a map and it can seem like a wealth of possible destinations spread out across the area, but when it comes down to the practical, travel-time realities, the place starts looking entirely different. Some places will start feeling closer than they appear on the map, while others, appearing close together, may feel very remote. (This phenomenon is properly visualised by an [isochrone map](https://en.wikipedia.org/wiki/Isochrone_map))

# 🏙️

Chances are, you live in a [monocentric city](https://planningtank.com/settlement-geography/the-monocentric-city) or something close to it - where most people work in a central district but commute from outside it, and whose transit radiates from the centre. By living in such a space, your mental image of the city and its space probably differs quite a lot from the map. Two facts will hold true for you at the same time:

1. There are far away locations that you have visited often, because they are easy to travel to
2. There are nearby locations that you have never visited, because they are very difficult to travel to

Chicago is a poster child of this kind of city; its mass transit mostly radiates from a [core downtown area](https://en.wikipedia.org/wiki/Core_city). Travelling to and from downtown is easy, but travelling between the "branches" is so difficult that the best option is usually to transfer via downtown.

<a href="https://www.chicago-l.org/maps/route/maps/2003elevated.jpg"><img src="https://www.chicago-l.org/maps/route/maps/2003elevated.jpg" alt="Chicago L map, 2003" width="400px" /></a>

That's the gist; unless you can fly like a bird, your experience of navigating the world will not resemble the map.

# 🌎

More than any other development, [railroads made modern USA](https://en.wikipedia.org/wiki/First_transcontinental_railroad). By shrinking transcontinental travel from weeks to days, it linked the coasts, tamed the West, and made it a breadbasket. It turned the continent into a single economic zone, culture, and national identity.

[![Rates of travel in America](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Rates_of_travel_in_America%2C_1800_to_1930.png/330px-Rates_of_travel_in_America%2C_1800_to_1930.png)](https://upload.wikimedia.org/wikipedia/commons/a/a5/Rates_of_travel_in_America%2C_1800_to_1930.png)

When mass air travel first appeared, it made the world smaller. It did for the world what railroads did for USA. The fact that people, goods and military forces could travel from one end of the world to the other in days or less meant that no one on this world was truly out of reach; we could not ignore each other, and could not avoid being influenced by global events. Geographic scale did not change, but the psychological impact of fast travel had irrevocably changed the nature of the world.

# 🎮

What's true for the world also applies to video games. When we find new waypoints in Diablo, we bend the geometry of the world, and we feel like we are conquering the wilderness. When we find a new tool that allows us to backtrack efficiently in a [Metroidvania](https://en.wikipedia.org/wiki/Metroidvania), we shrink the size of the world and we feel powerful.

![Diablo 2 waypoint](https://diablo2.diablowiki.net/images/d/d2/Waypoint1.gif)

A great case study of how different modes of travel fundamentally changes gameplay is [Stratego](https://en.wikipedia.org/wiki/Stratego) vs [Luzhanqi](https://en.wikipedia.org/wiki/Luzhanqi). The two games are extremely similar, but where Stratego pieces can only move one square at a time, those in Luzhanqi have a range of options based on the terrain - they can move unlimited spaces along a railroad, and there are well-connected campsites which are safe from attack. The result is a much faster-paced game, with the game board feeling much smaller due to the railroads, where most of the action takes place, filled with opportunity and danger.

> ![Luzhanqi](https://i0.wp.com/ulises.blogia.com/upload/20060502191234-luzhanqi66.jpg)
>
> The 4 player (2v2) variant for Luzhanqi is especially popular

So how do you use this knowledge to design better games? There are lots of possibilities:

- Giving the player a fast travel mechanism (a shortcut, or [fast-traversal vehicle](https://cxong.github.io/2016/12/2d-overhead-traversal)) makes them feel more powerful, and the world feel smaller. It's a psychologically impactful way of granting a reward, aside from plainly buffing their stats or giving them a powerful item.

<a href="https://vgkami.com/wp-content/uploads/2023/04/The-Airship-in-Final-Fantasy-1.jpg.webp"><img src="https://vgkami.com/wp-content/uploads/2023/04/The-Airship-in-Final-Fantasy-1.jpg.webp" alt="Final Fantasy 4 airship" width="400px" /></a>

- Distance is not so much a function of space, but time and effort taken to travel to a location. If a destination involves a long and dangerous journey away from a safe hub, it can feel especially remote. Consider placing big rewards or secrets in such locations - finding them can feel especially rewarding.

![Freelancer neutron star in Omega-41 system](https://fl-guide.de/graph/systems/omega41.png)

- Letting the player unlock more paths (in the form of waypoints or shortcuts) is an interesting way to provide a sense of progress. It gives the player the feeling of reshaping the world for their convenience, giving them a sense of belonging to the world.

![Pokemon HeartGold/SoulSilver cutting a tree](https://static.pokemoncoders.com/wp-content/uploads/2025/06/get-cut-in-pokemon-hg-ss-getting-cut.jpg)
