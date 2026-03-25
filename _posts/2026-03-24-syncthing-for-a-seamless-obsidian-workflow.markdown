---
layout: post
title: "Syncthing for a Seamless Obsidian Workflow"
date: 2026-03-24 13:56:00 -0400
categories:
  - obsidian
  - syncthing
excerpt: "A quick look at how Syncthing and Obsidian can work together to create a seamless cloud-like workflow while staying 100% local."
---

## Context

In a time where cloud solutions, SaaS, and subscriptions are exploding in popularity, it's almost a given that an app or tool will store your data on the cloud. This is super convenient most of the time, but inevitably that service will cost, whether it's immediately communicated upfront or not.

I love the idea of a local-first philosophy for personal projects and small scale workflows, where cloud collaboration isn't a necessity. Working on home lab projects, I always prioritize local first tools. One tool I will be making a lot more use of is [Syncthing](https://syncthing.net/).

## Details

Syncthing is an open source tool that keeps folders synced across devices using the local network. That's really all there is to it, and I had dabbled with it in the past as a way to move files from one device to another without directly using something like a Samba share or other FTP service. I didn't really think much of it until I started unraveling all this incredible freedom I had with Android and Termux. 

Switching from Notion to Obsidian really only had one immediate downfall in my eyes: I couldn't seamlessly work on my PC and phone out of the box. Well, I am pleased to write that this problem is solved by Syncthing. No cost at all, seamless syncing across devices, and it does it all in the background... LOCALLY.

Now, local only does mean that it will not sync unless both devices are on the same network, but for a simple solo workflow, this is fine. I'll never be doing both at the same time in different places, so that limitation doesn't negatively impact my workflow at all.

To wrap this up, I just want to reinforce how seamless this really is. I can have the same note open on both devices and edit on one device, then by the time I look at the note on the other device, it's already updated. Awesome tool, highly recommend.

## More Potential Uses

Some ideas I have for this in the future:
- Business simulation running on my phone with synced postgres to my PC for analytics processing
- Syncing hledger files to manage finances on both devices
- Getting Syncthing on my wife's phone to enable us to have a shared Obsidian Vault for shopping lists, etc
