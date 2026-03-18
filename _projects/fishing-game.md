---
title: "Fishing Game"
status: In Progress
summary: "An ASCII fishing game blending traditional roguelike aesthetics with a more relaxed, fishing-focused experience."
stack:
  - Python
  - JSON
  - Tcod
  - Curses
  - Git
  - Codex
project_url: ""
repo_url: ""
timeline: 3 weeks
order: 10
---

# Background

Ever since my freshman year of college, I've always wanted to make a video game. Back then, I had just started my first computer science class learning the basics of Java. I remember trying to build a mobile game using MIT App Inventor 2. That software used code blocks with a drag and drop canvas, but I had something going with one of my roommates. Development halted when I hit the 5 megabyte project size limit. It hurt to realize there was no real way around it.

A couple years later, again I tried with Android Studio this time. I was using a first party tool to create a native application, but the lack of game engine features was ultimately the end of that project.

I tried many times to start video game projects, with engines, without engines, with art, without art. It's always ended the same way; i realize the scope of the game is way too wide for me to realistically ever finish it in an amount of time that would feel rewarding to me.

I've always wanted to capture something that I've seen with games like Caves of Qud or Cataclysm's various forks or even classic ADOM. I wanted a simple looking game, something people look at and assume is surface level with a lack of depth, only to find that despite the simple aesthetic, has incredible depth and complexity. I've wanted to make deep, intricate systems that all play into one another and feed a satisfying progression where the player could do "anything" they want. I've wanted to surprise players at what was possible in the game. These big ideas required more commitment than I could afford to give, but I've always felt they were good ideas.

Now I'm here with my latest attempt at a game dev project, but this time I'm setting aside my huge ambition to try and create a focused experience. Still, with the ascii old school look, partly because I love the aesthetic and partly because I don't enjoy spending time on art. What I'm going for is a relaxing, low stress game where the entire experience revolves around fishing. No combat or peripheral systems that don't feed back into that task. Everything goes into fishing. Now, that doesn't mean there isn't depth, but the depth is much easier to manage when it's not also breadth.

## Approach

The approach I'm taking with this project is quite simple: keep the scope tight, and the design data-driven. Simply put, only focus on fishing as the core loop of the game and write the game in a way where all the data is defined in json, with the logic in Python. The UI uses a dual front-end currently where I started with curses for a true CLI game and added tcod for a few modern features. Tcod will be my main front-end as it creates an OS window and gives more flexibility with how exactly the game looks when drawn on the screen.

## AI Involvement

I am making heavy use of Codex CLI to develop this project. I know the world is quite divided on this topic, but I'm making this for me at the end of the day, and I want to actually finish the project. AI empowers me to create at *at least* 10x the speed I would otherwise. Does the quality of the game suffer from this? Frankly, I don't think so. I put care and attention into how I'm designing the systems and UX. AI may be writing the code, but I'm steering the ship very carefully.

Also, Codex CLI, Termux, Git, and Python mean I can work on this on my phone as well. That's *incredibly convenient*.

## Features and Mechanics

#### Fishing 
For a fishing game, it's important to have a well thought out fishing mechanic. This game being ascii based, and the goal being a relaxing experience, I didn't want the mini game to be too difficult, so I prioritized rewarding high skill rather than penalizing low skill. What this looks like in the game is exp bonuses for quick completion of inputs, but no time limits to worry about other than the "hook window". The way the mini game works is in 2 stages: 
1. The waiting game: wait until the fish bites, then hook the fish within the hook window (about 2 seconds). This window is not stressful, just enough to require some engagement from the player.
2. The reeling phase: input a sequence of directional key presses using arrow keys. The number of inputs it determined by a multitude of factors, but the main idea is to accurately input the sequence. There is no time limit, however there is bonus exp on the table for quickly finishing the sequence. One incorrect key press loses the fish. I like this design as there's no way the player would ever feel cheated out of a catch because they aren't good at the mini game. It's purely a balance of knowing about the extra exp and knowing one error results in failure.
#### Fish 
The second most important thing are the fish themselves. They need to be exciting to catch. The way I approached the fish was, firstly, to define their data via json. Fish can be added to the game without touching any core code as they aren't hardcoded. As for retention inspiring mechanics, the fish have a few variables: rarity, weight, and an extra rare "shiny" variant. Coupled with that is a collection log to keep track of which ones the player has and how many are left to find.
#### Upgrades
This game originally was meant to be an idle game, however I kind of shifted my focus a bit to make it more of a collection-progression game. With that being said, the game will still make use of interesting upgrades that introduce new mechanics and ways of playing the game, alongside smaller incremental stat upgrades.
#### Quests
Quests come in the form of NPC requests. I want to have a substantial enough questing system to handle multi stage quests with unlocks and state changes to map entities. In short, I want to open the door to systems via quests to introduce them gradually and effectively. 
#### NPCs 
The aforementioned NPCs will be moving map entities. They will path around the map and offer dialogue and quests to the player. NPC movement is mainly for flavor to make the world feel less static. More on that implementation later.
#### Bounties
Another retention mechanic will be Bounties. This should be simple catch requests, but they act as daily and weekly goals. My vision is that the player will choose one of each daily and weekly bounty to accept, progress towards completion of the bounty, and if complete withing the day or week, a double exp reward is granted. Double exp is a banked pool of double exp points that deplete as exp rewards are doubled. It's essentially a gradual drip feed of extra exp rather than a large dump of exp. I believe this adds variety and encourages play beyond just completing daily and weekly tasks.
#### Events
Events should serve as an opportunity for the player to mix up a repetitive playing pattern. Events will be fish frenzies (high catch rate nodes), weather changes, holidays, tournaments, etc. They should be varied and exciting enough that the player gravitates towards participating rather than continuing their current activity in most cases.
