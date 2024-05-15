---
layout: post
title:  "Orders, Zones, and Schedules"
date:   2024-05-15 13:27:44
---

It has come to my attention that there are as many as four or even five people who occasionally wonder about how that Settle Gliese game is getting along. Well, exactly a year since the last blog post seems like as good a time as any to fill you curious folks in.

I've taken the game in a decidedly more dwarf-fortress direction. Rather than having direct control of a character's movements, players assign 'orders' to characters, which the characters then do their best to fulfill. It isn't quite as zoomed out as dwarf fortress, but more zoomed out than a typical single-character roguelike. Somewhere in the middle of the two. Let me show you what I mean

## Move

Perhaps the most fundamental of the new orders is the move order. Press 'm', then select a square on the map. Your character will figure out the best path to that square and walk there. They will walk quickly on roads, and slower over undeveloped terrain. You can tell them to move multiple panels in a certain direction, as well.

<img src="/images/move.gif" />

## Gather

Press 'g' to choose what item you want your character to gather. As you can see, not all of these instructions really fit under the conventional definition of the word gather. We have 'fuel light', 'bury body', and 'dig irrigation channel' in here, too. It's possible these actions will be moved out of this menu in the near future. Or maybe not. When constructing menus for my game I don't like to be constrained by things like the actual meanings of words.

<img src="/images/gather.gif" />

## Haul

Once you've gathered some items, you'll want to bring them back to a stockpile you created earlier.

<img src="/images/gathering.gif" />

## Build

And then build a nice big wall around your stockpile to stop any would-be thieves from taking your supplies.

<img src="/images/build.gif" />

## Fight

And naturally, characters will be able to fight each other and all of the various creatures of the planet to their heart's content.

<img src="/images/fight.gif" />

## Schedule

All of these orders can be scheduled to repeat daily or repeat infinitely over a day. You can also queue orders up and then use this menu to see what your character is currently working on.

<img src="/images/scheduler.png" />

## Organisations

To give orders to another character, they'll need to belong to the same organisation as you. Organisations also own 'stockpiles', so if you want to access the wealth of an organisation you'll typically need to become a member.

<img src="/images/organisation.png" />

## Zones

Zones can either belong to a character or an organisation. They are used for defining stockpiles, and also general 'home' areas.

<img src="/images/zones.png" />

## Ordering Other Characters About

Characters can now give orders to all of their little friends through the conversation tree.

<img src="/images/ordering-about.png"/>

## Multiple Characters

A single account can now have multiple users. I haven't decided at the moment what the limit of characters to an account will be, but I like the idea of players making little dynasties and interlocking family trees. I think each account will be given a 'surname' so you will quickly be able to see which characters are played by the same user.

<img src="/images/character-select.png"/>

## The Big Flat Now

The more perceptive of you will have noticed that none of this stuff is what I wrote about in the last article. A year ago, I wrote about how I was going to use Async conversations, Events, and Quests to make the game feel more alive. Well, yes. To make a long story short, I decided on a different direction. I tried a few things out and the game didn't feel like it was heading in the right direction. It took a bit of soul searching but eventually I realised this 'orders' system was a different approach to making the game feel more alive and giving you things to check back in on. It's an approach that feels like it has more potential to me - I hope you agree and are as excited about this next stage of Settle Gliese as I am!