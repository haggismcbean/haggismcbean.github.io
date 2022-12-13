---
layout: post
title:  "Christmas Update"
date:   2022-12-13 12:42:16
---

Yo ho ho to all the good people of the internet. I'm sure you've all been asking yourselves what the latest progress is with Settle Gliese so here I am to provide you with an update.

## Descriptions

I had a great time twiddling around with some openAI text generation and have generated a huge amount of descriptions for all the plants and animals in the game. I have ambitions to extend these to man-made items as well - anything that you can add a description to can have an auto-generated description if you are lacking the inspiration or imagination to come up with your own.

<img src="/images/camel.png" />

> A friendly camel

<img src="/images/night-stalker.png" />

> A typically voluptuous beast

## Culture specific items

All kinds of things now look differently depending on which of the eight cultures you are a part of. If you want the cool pot of the desert people but you are but a lowly swamp person, you'll have no choice but to trade for it or steal it.

<img src="/images/polar-community.png" />

> A polar community

## Tents

For any people that want to be nomads, there are a number of interesting tents and temporary structures they can utilise. Animals will not enter a tent so you can camp out in one safely as night falls. They can be taken down and carried on the back of a person or beast of burden.

<img src="/images/tent.png" />

> A traditional goati tent

## Tech Tree

I've 'finalised' the tech tree for now and added recipes and workshops for every item in the game. There's a bunch of cool things in there such as special pots which can imbue your food with powers, brainchip enhancements, wagonways, sailing boats, guard houses, vending machines, and more.

## Performance

I've improved the performance of the game by reducing the amount of data that needs to be saved and sent when you're walking around the world. There's still plenty of work to be done but I managed to reduce the database size by a factor of ten in the last couple of months.

<img src="/images/riverside.png" />

An unoptimised river 

```
[
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' },
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' },
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' },
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'RIVER' }, { tileType: 'RIVER' }, { tileType: 'NONE' },
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'NONE' },
    { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'NONE' }, { tileType: 'RIVER' }, { tileType: 'NONE' },
]
```

Converts nicely into an array of ones and zeros

```
[
    0, 0, 0, 1, 0, 0, 0,
    0, 0, 0, 1, 0, 0, 0,
    0, 0, 0, 1, 0, 0, 0,
    0, 0, 0, 1, 1, 1, 0,
    0, 0, 0, 0, 0, 1, 0,
    0, 0, 0, 0, 0, 1, 0,
]
```

Which can be converted to a binary number `000100000010000001000000111000000100000010`

Which can be converted to a hex number `4081038102`

Which takes up a lot less space.

## What's Next?

The trailer will be out soon. Most of the major features in the game have been implemented (to a more- or less-buggy state), now the job is to go back and fix most of the bugs, and add minor features such as individual item behaviours. I'm really enjoying the ride so far and it's really exciting being able to see the rough outline of what the game is going to be! Hopefully we'll be ready for some early beta testers early next year some time
