---
layout: post
title: Big Without Scale
date: 2023-11-14
comments: true
published: true
---

Having big and interesting game worlds has been a holy grail of games since the beginning. In the early years, technical constraints meant that big worlds were simply infeasible, without heavy use of procedural generation - [*Elite*](https://en.wikipedia.org/wiki/Elite_(video_game)) in 1984 for example boasted thousands of planets - but nowadays, the main constraint is dev effort. Put simply, to create lots of interesting content, you need to put in lots of work.

But that doesn't mean we can't use clever techniques to get the most bang for buck.

![Elite](https://upload.wikimedia.org/wikipedia/en/3/31/Arcelite_through_vipers.jpg)

# Bigger is not Better

When we look at lists of [biggest game worlds](https://www.reddit.com/r/Games/comments/ehwyj8/sizes_of_the_largest_open_world_video_game_maps/), space games like [*Elite Dangerous*](https://en.wikipedia.org/wiki/Elite_Dangerous) and [*Starfield*](https://en.wikipedia.org/wiki/Starfield_(video_game)) dominate, but that's not particularly insightful when you consider they are mostly empty space. A bit lower in the rankings you'll find [*Daggerfall*](https://en.wikipedia.org/wiki/The_Elder_Scrolls_II:_Daggerfall), which dwarfs other *Elder Scrolls* game worlds while being much older than them - notably having "the size of Great Britain" - but again, isn't interesting as most of the game is empty wilderness, sparsely filled with randomly generated towns.

<iframe width="560" height="315" src="https://www.youtube.com/embed/UvFdMax3wlA?si=WiYpCwuiHphb-vk2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Another mistake that some games make is by increasing the scale of their game worlds without maintaining the density of content, which makes things feel sparse. During the release of [*GTA San Andreas*](https://en.wikipedia.org/wiki/Grand_Theft_Auto%3A_San_Andreas), there was some hype about being able to enter lots of buildings, and while the game did make many improvements in density over its predecessors, most buildings were still off bounds or limited in interactivity, making the game feel less like a huge living city and still like a playground for driving cars around.

So when it comes to feeling big, the raw numbers don't tell the whole story. Bigger is not better if it is just sparse, more is not better if it is small variations of the same stuff. To truly feel big, we need things like variety, complexity, and content.

# PCG is not a Panacea

Over the years various people have touted procedural content generation as the killer technology that will enable big and interesting game worlds on the cheap. In recent years, [*No Man's Sky*](https://en.wikipedia.org/wiki/No_Man's_Sky) suffered bad reviews due to not being able to live up to its hype; boasting quintillions of playable worlds, a press largely unfamiliar with PCG helped blow things out of proportion. The reality is that, although PCG is great for some things, it is no replacement for hand-crafted content in the same quantity; quintillions of worlds created by competent human artists (if such a thing were possible) would be so much more compelling than any algorithm could, and equating the two was ridiculous.

More recently, generative AI has caused much disruption and threatened to replace human artists in many domains. It is still early days, but indications so far suggest that they cannot fully replace all human artists, but may be useful in some mundane tasks, provided we can sort out the legal issues.

I view PCG and generative AI similarly - they are useful in limited areas, and work best when complementing hand-crafted art, as additional tools in an artist's toolset. PCG for example works well in roguelikes or game randomisers to improve replayability, but still requires a great deal of effort and care in creating those worlds in the first place, and tuning the generators for the task. Generative AI has already proven useful in areas like prototyping and as filler content, but requires a lot of resources to train and tune, and cannot be the whole content pipeline alone.

So although technology will make work easier, you still need to put in the work. But where do we focus our work on?

# A World that Feels Alive

Stepping back a bit, we want big worlds they are immersive. When we reach the end of a small world, the illusion is shattered and we are rudely reminded of the artifice of the game, but if the world was big enough, we could continue to pretend that this was a virtual reality we could inhabit indefinitely.

But we can do better than focusing solely on scale. By taking cities as an example, what makes a city feel "big" isn't its geographic size; instead it's:

- **complexity**
- **density**
- **specialisation**

By focusing on these, we can achieve worlds that feel big without excess effort, and avoid common pitfalls that make some worlds feel wrong.

## Complexity

Real life big cities are incredibly complex places. They are where people live, work, play; where industry and commerce and many different sectors coexist in symbiotic ways. Lots of infrastructure and services are needed to keep it all working - transportation, sanitation, health, construction, emergency services, education, on and on. This amount of complexity really resists procedural generation, and a simulation approach would also be very difficult. Any given part of a city will contain amenities of different types, like religious temples mixed in between residential buildings. Cities resist uniformity, and this makes them endlessly interesting.

<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/stairwell_jinja.jpeg"
    data-fancybox="gallery-complex"
    data-caption="When space is at a premium but there's a need for certain amenities, any tiny bit of free space is fair game. Here is a Japanese Shinto shrine tucked underneath a stairwell.">
![Sendai Station](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/stairwell_jinja_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/mitsumine.jpeg"
    data-fancybox="gallery-complex"
    data-caption="Another Shinto shrine sandwiched by apartment buildings.">
![Mitsumine Shrine](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/mitsumine_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/shingen-ji.jpeg"
    data-fancybox="gallery-complex"
    data-caption="Religious buildings like this temple are used by the local residents who live nearby, but the architectural style is completely different.">
![Shingen-ji](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/shingen-ji_th.jpeg)
</a>

Cities are sometimes designed, but often organic entities, and this makes it resistant to clean delineations. Buildings are not simply just an "office building", blocks are not simply a "commercial block". Buildings can be owned by a single business, or multiple businesses. Successful businesses can expand to encompass multiple, adjacent buildings, connecting them so that when you enter them, you can seamlessly travel from one building to another as if it were a single building. Dominant businesses can buy up buildings in the same area - the Japanese electronics retailer [Yodobashi Camera](https://en.wikipedia.org/wiki/Yodobashi_Camera) owns a whopping [13 "pavilions" (buildings)](https://www.shinjukustation.com/yodobashi-camera-shinjuku/) in the [West Shinjuku district](https://en.wikipedia.org/wiki/Nishi-Shinjuku) of Tokyo alone.

A city's appearance reflects its history and culture. As a city grows, newer areas and buildings will have a different style than older areas. The distribution of businesses can also follow opposing dynamics. Recall what I wrote about cities not being uniform? Sometimes businesses cluster and you'll find single buildings filled with the same type of business, shopping streets, or department stores designed to capture a specific type of clientele. Just as businesses and amenities may need to spread out to capture geographically dispersed users, they can also [cluster to capture users who are shopping around](https://en.wikipedia.org/wiki/Hotelling%27s_law).

## Density

Cities are much more than just villages or towns but extended out. Because of how desirable they are to be in, space becomes a premium and this drives up density. This can do some weird things - streets become narrower, buildings get higher. A newbie trap is to make everything bigger in cities, including streets, but density will lead to them becoming smaller, unless there are other forces at play.

An example of where things aren't quite right is [EarthBound's](https://en.wikipedia.org/wiki/EarthBound) [Twoson Department Store](https://wikibound.info/wiki/Twoson#Department_store). Although it does contain different shops on each level, which is realistic, it does two things wrong: 1. the slow escalators between each floor make it less convenient, and 2. the shops don't actually have better selections than [other towns](https://wikibound.info/wiki/Onett#Businesses). In reality, big city department stores should be more convenient and have better item selections.

![Twoson Department Store](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/twoson.png)

Compare this with Pokemon's [Celadon Department Store](https://bulbapedia.bulbagarden.net/wiki/Celadon_Department_Store). It has great item selection and its stairs and elevators are quite convenient.

One consequence of extreme density and verticality is that it turns the space from 2D into 3D, which [humans have trouble navigating](http://cxong.github.io/2022/12/2d-vs-3d). Underground spaces lack [weenies](https://theoryofthemeparks.blogspot.com/2015/08/wayfinding-in-themed-design-weenie.html), and claustrophobic spaces limit sight lines. This all makes dense spaces incredibly hard to navigate, so there's an over-reliance on signage, providing sensory overload.

<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sendai.jpeg"
    data-fancybox="gallery-dense"
    data-caption="In very busy locations like major stations, the infrastructure needs to support multiple modes of transportation. Elevated walkways like this can help separate pedestrian traffic from road vehicles, and opens up more levels for shop fronts.">
![Sendai Station](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sendai_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/panda_bridge.jpeg"
    data-fancybox="gallery-dense"
    data-caption="Multi-level pedestrian walkways and bridges effectively turns outdoor urban spaces into multi-level spaces too.">
![Panda Bridge](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/panda_bridge_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/namba_walk.jpeg"
    data-fancybox="gallery-dense"
    data-caption="This underground walkway stretches almost a kilometre long. Originating as a pedestrian connection between two stations, commerce can easily develop and turn utilitarian spaces like this into destinations.">
![Namba Walk](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/namba_walk_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/dotonbori.jpeg"
    data-fancybox="gallery-dense"
    data-caption="Density forces 3-dimensional spaces. Not just the fact that multi-level buildings exist, but vertical signage dominates the view, advertising businesses at different levels in each building.">
![Dotonbori](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/dotonbori_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/multilevel.jpeg"
    data-fancybox="gallery-dense"
    data-caption="An example of what extreme density can do: tiny multi-level buildings where each level contains a different, related business.">
![Multilevel business building](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/multilevel_th.jpeg)
</a>


## Specialisation

When population density is high enough, more and more niches become viable, and here's where we see lots of specialisation. Specialty stores in big cities sell all sorts of weird items for tiny interest groups, that are often baffling for lay people. Unique buildings, people of all sorts of subcultures comingle like colourful animals in a thick urban jungle. Cities are anything but boring and uniform.

Recall Pokemon's Celadon Department Store? It sells a lot of unique items, including strange ones like [Fresh Water](https://bulbapedia.bulbagarden.net/wiki/Fresh_Water), a healing item can only be bought at a vending machine one at a time, it does exactly the same thing as the [Super Potion](https://bulbapedia.bulbagarden.net/wiki/Super_Potion), yet it is much cheaper. In gameplay terms this makes little sense, but I love how items like this give the game extra life. You get the sense that this item was not made for the player, that the game's world was inhabited by all sorts of different people who use this item for different purposes, and it just so happens to be useful to the player too.

<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/toshima.jpeg"
    data-fancybox="gallery-special"
    data-caption="Big cities have big infrastructure needs. This colossal chimney belongs to the Toshima Incineration Plant, located right next to a busy train station. Its size is required to clear the local skyscrapers.">
![Toshima Incineration Plant](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/toshima_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sennichimae.jpeg"
    data-fancybox="gallery-special"
    data-caption="Big cities also have small infrastructure. This bustling shopping street is criss-crossed with phone lines, an reminder of the dense webs and networks that power the city.">
![Saita Building](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/sennichimae_th.jpeg)
</a>
<a
    href="https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/saita_building.jpeg"
    data-fancybox="gallery-special"
    data-caption="We like to think that cities have a look, but its buildings are often distinctive. Prefabs and McMansions are for the suburbs.">
![Saita Building](https://raw.githubusercontent.com/cxong/cxong.github.io/master/_posts/saita_building_th.jpeg)
</a>

# Making Big Worlds is Hard

This is basically what I wanted to say with this post: making big worlds is hard, and you can't cheat your way by copy-pasting content or using procedural generation. However by focusing on three elements: **complexity**, **density** and **specialisation**, you can make the most of your efforts - some games do this well by making some locations feel bigger without actually being geographically bigger.

This post does not cover exactly *how* to go about building big worlds - this is a far too broad subject - but here's a random list of items to consider:

- Historical layering, old/new regions: tell the history of the world via the environment
- Show construction: real cities/worlds are organic and always a work-in-progress
- Unique landmarks: gives a place character, as well as aiding navigation
- Multiple transportation modes
- Specialty stores selling unique items
- Content that is only tangentially useful for gameplay, but which make sense for the world
- Verticality: undergrounds, overpasses
- Mixed use buildings and districts: don't use only single-use architecture!
- Infrastructure: real cities can't exist without it. Don't completely forget the aqueducts, waste management plants, power lines!
- Confusing navigation: in moderation, but dense cities are confusing places, so don't be afraid to lean into it

As well as a few excellent reading materials:

- [A Beginner’s Guide To Crafting Video Game Cities](https://www.gamedeveloper.com/design/a-beginner-s-guide-to-crafting-video-game-cities) - argues that one should take a world-building approach to building cities. Make a realistic city first, then adapt it for the game: *it is, after all, not its size that differentiates a city from a village, but its functions*
- [Urban Design and the Creation of Videogame Cities](https://www.gamedeveloper.com/design/urban-design-and-the-creation-of-videogame-cities) - contains lots of pointers on how to make great cities. *Game cities must always make sense*
