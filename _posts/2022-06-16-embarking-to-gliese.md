---
layout: post
title:  "Journeying to Gliese"
date:   2022-06-16 10:20:37
---

## Let's Journey Together

Hello again friends. This week work continued on the tutorial. I hope to have most of the functionality finished by the end of next week so I can start on the fun stuff - generating the beautiful new biomes, animals, and tech tree.

## Graceful Long Potato Shaped People

One important but slightly problematic task I did this week was converting the current game engine from 16px square tiles to 16px x 24px rectangles. Unfortunately I'm still loading in the old tileset because the new one is not ready, which has lead to this interesting 'stretched potato person' effect. 

<img src="/images/stretched-potato.png" />

> "Is it just me or is something strange happening?"

## Space tiles

Next week I will try to replace these glorious stretched potatos with something from the new artwork. Check out these tiles we've been creating

<img src="/images/walls.png" width="200"/>

> Walls of various sorts

The space station will be owned and operated by a mega corporation, who are sadistically sending you to the planet for their latest reality TV show. We want the space station to strike a balance between 'futuristic cutting-edge technology' and 'shabby souless corporate office'.

<img src="/images/tileset-ship.png" width="220"/>

> Space walls and silhouetted space station parts

## Draggable Grid Layout

<img src="/images/transport-tycoon.jpeg" width="500"/>

> Transport tycoon was an early adopter of this revolutionary layout style

I am toying with the idea of making the various screens in the game draggable, resizable, and hide-able. Depending on what is happening in the game you might want a few different menus up. When in a deep conversation, for example, you might want a small game screen and an enlarged dialogue screen; when you're crafting it can be helpful to have your inventory and the crafting screen both showing; and so on. Let me know what you think of this idea in the discord.

<img src="/images/draggable-grid.gif" />

> A draggable grid offers the most layout flexibility

## Conversation Trees

When you first arrive on the space station orbiting the planet Gliese, you have a conversation with the captain, who fills you in on what you'll be getting up to when you arrive on the planet. We need more versatile ways for characters to communicate asyncronously, and allowing players to create their own dialogue trees would be one way to accomplish this, so this dialogue tree might screen be used for more than just the tutorial. In the future I will remove the purple and orange boxes from the dialogue and go with a more dignified white-on-black design. Adding some logic to convert \*asterisks\* to *italic* would be a nice improvement as well.

<img src="/images/dialogue-tree.gif" />

> A conversation between a new recruit and the captain of the space station

## Generated Embark Lobby

Once a character has been introduced to the world by the captain of the space station, they will be sent off to either join an existing group of established settlers or, if they are feeling particularly reckless, a new group. Rather than displaying a static menu showing which groups are available, I thought it would be more fun to generate rooms for the player to join. There will be a control panel in each room that will show a descripition of the group you are considering joining, and some furniture and decorations. The rooms will be sized according to how many players are currently in the group. Players on the planet will be able to edit their control panel.

<img src="/images/embark-lobby.png" height="650"/>

> This wooden space station with beautiful sand flooring is only temporary

## Embark Options

If a character is ambitious, the option is open for them to create their own embark group. The creator will have the chance to choose the biome the embark group joins, and give a brief description in which they can describe their goals for the group. It would also be useful for the creator to specify how close to other groups they would like to be - some groups might like the challenge of being completely isolated, whereas others will aim to establish relationships with nearby groups as quickly as possible.

<img src="/images/create-embark-group.png" />

> A new embark group form

Another option is to show the user the full map of the planet and highlight which areas fit their current search parameters - if that's done, users could even choose a specific place to embark to. I'm a little reluctant to do that, however, because the idea of players not knowing the world map and having to discover it as a player group appeals to me. It would also be open to abuse from griefers and metagamers. Let me know what you would rather have in the discord channel.

Thanks for reading folks, I'll see you again next week!