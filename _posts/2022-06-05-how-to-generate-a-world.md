---
layout: post
title:  "How to Generate a World"
date:   2022-06-05 12:56:46
---

## This Week's Update

Hello friends. This week has been a pretty exciting time for the project.

First but by no means least, after some months of paperwork ping pong I have received the contract for the funding application, so fingers crossed I might actually receive the first installment some time soon.

For most of the week I've been working on the prologue, which has involved building a terminal emulator, and building a sort of 'staged scene' in the game world. There's still plenty of work to do here but it's been fun getting my hands dirty. I'll try not to show too many spoilers, but here's one little screen shot which doesn't give too much away.

<img src="/images/terminal.png" width="100%" />
> Now you too, can be a hacker

## Pixel Art

<img src="/images/warmup-septembitchall.png" height="300" />
> Some pink items

<img src="/images/warmup-froggypractice.png" height="192" />
> Various frogs of different types

Auilix, the pixel artist (follow them [here](https://twitter.com/auilix)), started off the week getting into pixel art. Drawing on a small top-down scale with a limited palette is more puzzle working and problem solving than illustration usually is, so warm ups are necessary. Saultoon's excellent [channel](https://www.youtube.com/c/saultoons) and [Septembit challenge](https://twitter.com/septembit) were a perfect jumping-off point and check out these 16 x 16 frogs as a bonus.

After some design exploration and palette building, we decided to go with a rectangular 16 x 24 pixel tile over the 16 x 16 tiles we used in the alpha for Settle Gliese. A vertical rectangle shape is more ‘human’ shaped than a square, and I think it makes the sprites seem more mature and less potato shaped.

<img src="/images/pixelexperiments1a.png" width="100%" />
> Potato people and square objects

<img src="/images/pixelexperiments2a.png" width="100%" />
> Long graceful, people-shaped people

As a consequence there will be more tiles on a panel, which I don't think is a bad thing. Let me know what you think!

And for all you dead by daylight fans, here is some dead by daylight fan art in the new style:

<img src="/images/lildbd.png" height="72" />
> Coming soon to a screen near you - Dead By Daylight the Roguelike

## Game Design

I've also been working a lot on the game design and have made some pretty big decisions that I think will improve how the game plays. There's still a lot that will go into this and everything's a work in progress. If you have any thoughts or suggestions about these feel free to share in the [discord](https://discord.gg/h9sCtUfhhW)

## Mountains into Mazes

Mountains represented a serious barrier for early humans, and impeded migration to such an extent that in some places different cultures, languages, and even races would develop on either side of the mountain range. Pretty cool, right? I want this to arise in the game, but how to achieve this in an interesting way? We could always force characters to move very slowly through mountain regions, or add a chance of them dying, but I wanted characters to feel that desperation of being lost and stuck halfway up a mountain and these options didn't quite give that feeling. But I had another idea - we could turn the mountains into huge multi-panel mazes.

<img src="/images/maze-mountain.png" height="400" />
> What a maze looks like

In this way players can cross if they're really desperate, brave, or foolish, but I hope most players will be sufficiently put off. Hopefully this is a nice way of translating a real world problem into a 'game-like' problem.

## Mines into Dungeons

Mines were also very dangerous places back in the day, so much so that the best way to get rich from mining was to persuade someone else to do it for you. In the alpha of the game mining was simply a case of walking up to a deposit of some stone or ore, and clicking the 'gather' button.

<img src="/images/alpha-mine.png" height="150" />
> An familiar scene

I wanted it to be more dangerous, to force players to make the same kind of risk reward calculations that early humans must have considered when entering a mine. My first idea was to make players 'dig' a mine, and on each dig there was a percentage chance of the mine collapsing and the player dying. Then I realised what countless other game designers must have realised before me, we can represent the danger of a mine in a much more entertaining way by turning them into dungeons.

<img src="/images/mock-mine.png" height="400" />
> A very bare bones mock up of a mine-dungeon

A player can enter a mine and battle their way through monsters if they want to find the riches buried therein. Or if they value their life, they can persuade other players to explore the mines for them. I hope this will be a nice system for giving newspawns a fun task, as town leaders can persuade them to go spelunking on their behalf.

## Multiple Metals

A final problem I had with the alpha was that once you had discovered bronze and made all bronze items, there wasn't much further tech tree to go, but before you discovered bronze there also wasn't much to do. My first thought was to simply make discovering bronze harder and expand the early game tech tree.

<img src="/images/scrap-metal.jpeg" height="300" />
> A bunch of useless metal

But I think a better solution is to have multiple new metals made up of two or more ores, with varying rarity. The rarer metals will of course produce to stronger weapons, armour, and tools. This I think should be a lot easier to balance than the 'just bronze' route, and with the best of metals only available if you mine ores coming from opposite sides of the planet, it will strongly incentivise long trade routes.

## Apothecaries and Brainchip Upgrades

As well as metals, we can apply a similar principle to the creation of tonics and the upgrading of brainchips. Local plants or rare minerals can provide small upgrades, but for the most powerful effects you'll need to swap plants that only occur on the other side of the planet. With plants, players will need 'local knowledge' - you can only harvest the valuable parts of the plant if you were born in that region. In this way long distance trade or tyranical empires will be the only methods of obtaining the most powerful in game items.

## How to Generate a Planet

Some of you may be interested in how the planet Gliese was generated, so I will add a quick lowdown of how I did it here. In summary - someone else did it for me. I used the brilliant open source project [Mindwerks WorldEngine](https://github.com/Mindwerks/worldengine), which generates a full little world.

<img src="/images/ancient_map_seed1.png" height="400" />

The worlds are generated using plate techtonics, erosion, rain shadows, holdridge life zone models (whatever they are) and more.  I generated a number of little worlds until I found one I liked the look of. You choose the size of the world, and it generates elevation, precipitation, temperature, biome, and ocean maps as images. I then wrote a small program which reads each of these images and saves the data into a database. Not sure what I mean by that? Take for example this heat map

<img src="/images/heat-map.png" height="400" />
> The average temperatures of a generated planet

There are seven colours on this map which represent seven temperatures. My program would look at each pixel, convert its colour into the temperature range (from 1-7), and save this data under the pixel's position. Once I'd done this for every pixel, I had the full world in a database. Each of those pixels is one panel in Settle Gliese. Generating the terrain for the panels, including cliffs, rivers, and coastlines, was a little more complicated. Maybe I'll write some more about that another time.

Thanks for reading, I'll see you again next week!