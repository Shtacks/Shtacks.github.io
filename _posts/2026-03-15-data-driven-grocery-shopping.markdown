---
layout: post
title: "Data-Driven Grocery Shopping"
date: 2026-03-15 00:01:00 -0400
categories:
  - obsidian
  - productivity
excerpt: "A quick look at how I set up an Obsidian Base to manage my grocery list with simple, data-driven sorting."
---

## Context

I had a setup in Notion that worked well, but I have been experimenting with Obsidian and really like its local-first design. Seeing Notion's "you've used all free blocks, upgrade now" message while I was working on my grocery list pushed me to revisit the idea and rebuild the system somewhere else.

## Main Takeaways

- Obsidian offers enough structure to support lightweight database-style workflows
- Grocery lists should be simple and easy to use, not overloaded with detail

## Details

Getting that upgrade message from Notion while making my grocery list made me wonder whether Obsidian could do what Notion did for me first: provide enough flexibility to design a grocery list "app" the way I wanted. A grocery list is a simple thing, just a list of items to buy. The one feature I think really matters is logical sorting that matches the layout of the store.

Sure, manually grouping items is not hard, but it is also not something I want to keep doing. An automatically sorted list is not difficult in theory. All it really needs is a small amount of metadata attached to each item: the store section. In my experience, that is enough. So I set out to see whether it would be that simple in practice, and it was.

Obsidian made it easy to add a `section` property to my items:

![Obsidian grocery item section property](/assets/posts/data-driven-grocery-shopping/Screenshot_20260315_000102_Obsidian.jpg)

And of course the sections themselves had to be data-driven too, so they became their own files:

![Obsidian grocery section files](/assets/posts/data-driven-grocery-shopping/Screenshot_20260315_000145_Obsidian.jpg)

That led to the actual list creation.

I now have a Base with two views. One lists all store items, and the other functions as the grocery list itself. Marking an item as bought removes it from the shopping list, and unchecking `Have` on the ingredients list adds it back to the shopping list. It is simple, but effective. As I add more items over time, they remain available in the underlying "database" for easy reuse.

![Obsidian grocery list base view](/assets/posts/data-driven-grocery-shopping/Screenshot_20260315_001551_Obsidian.jpg)

Locally stored, no limits, simple to build, and simple to use. Obsidian wins here in my book.

## Next Steps

To bring this up to the level of my previous Notion version, I want to add recipe integration. The idea is for recipes to contain ingredients that can be added to the list with one tap. Beyond that, I would like to layer in light meal planning and generative AI for recipe generation. At that point, this may turn into a larger standalone project.
