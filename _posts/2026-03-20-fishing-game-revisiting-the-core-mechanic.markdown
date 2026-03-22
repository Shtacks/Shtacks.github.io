---
layout: post
title: "Fishing Game - Revisiting the Core Mechanic"
date: 2026-03-20 21:25:00 -0400
project: fishing-game
categories:
excerpt: "A dev log in which I revisit the fishing mini game in my fishing game."
---

## Intro

In a game about fishing, the fishing has to be engaging. I did some research recently to see what fishing mini games existed in other games and how people felt about them. As I watched these videos and reflected on my own game, I started to see flaws. 

Particularly, the waiting for a fish to bite portion in my game is boring. It's just waiting with very little to no engagement. With my game being terminal based with ascii graphics, there's no beautiful scenery to be immersed in. The mini game must engage the player 100% from start to finish to be effective for my game. It needs to feel rewarding and fair, be real time based, and still embody a low stress experience.

## The Current System

The current mini game is a 2 part system: waiting for a fish to bite and hooking it, then reeling it in. I felt pretty good about the system as it felt reasonably parallel to real life. Waiting for a bite is just waiting and reeling is the fun part, but I found that this wasn't very engaging. The first red flag was how quickly I added a dev option to skip the mini game completely and just roll the fish on a key press.

The waiting portion was the true downfall. The way it worked is it had a progressive output of symbols to indicate how close a fish was to biting, then a 2 second window to hook the fish once you saw "HOOK NOW!". The downtime just wasn't fun.

The second phase, reeling, was actually pretty clever I think. A series of arrows appeared and you had to enter the arrows in order correctly using arrow keys. I liked this as I felt it paralleled well with similar fish fighting mechanics in other games, while fitting the terminal aesthetic and limitations. Still, though, it had very little visual flair and wasn't interesting to interact with beyond the sequence input.

I had upgrades mapped out for this system and they will need refactoring for the new system. Lot's of percentage roll type upgrades, like multi fish catching, will become interactive rather than passive.

### The waiting game
![Fishing game waiting phase](/assets/posts/fishing-game-revisiting-the-core-mechanic/20260321-2029-08.8996167.gif)
(This could last up to a minute)

### The reeling phase
![Fishing game reeling phase](/assets/posts/fishing-game-revisiting-the-core-mechanic/20260321-2030-53.6519939.gif)

## The New System

The new system keeps the player engaged throught the entire process. Still a two part system, but no waiting and to top it off, some visual flair. I envisioned a claw machine esque game where you're trying to drop the hook onto a moving fish. That's how it started, but then I ported over the sequence part of my previous system, creating the two phase mini game that I have now.

It's still somewhat a work in progress and I plan to add more mechanics and upgrade systems that play into this gameplay, but I feel confident this is a solid foundation to build on. I found myself genuinely enjoying the mini game, and even added a streak mechanic to reward consistent catches with an XP multiplier. 

Anyways, here's what the revised mini game looks like (at least for now):

### New mini game
![Fishing game revised core mechanic](/assets/posts/fishing-game-revisiting-the-core-mechanic/20260321-2037-09.2347959.gif)
