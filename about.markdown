---
layout: page
title: About
permalink: /about/
---

<section class="about-intro">
  <div class="profile-pic">
    {% if site.profile_image %}
    <img src="{{ site.profile_image | relative_url }}" alt="{{ site.author_name | default: site.title }} profile picture">
    {% else %}
    <div class="profile-pic-placeholder">{{ site.author_name | default: site.title | slice: 0 }}</div>
    {% endif %}
  </div>
  <div>
    <span class="eyebrow">About</span>
    <h1 class="about-name">{{ site.author_name }}</h1>
    <p class="about-summary">Use this page to introduce who you are, what kind of work interests you, and what visitors can expect from the rest of the site.</p>
  </div>
</section>

## Overview

Write a short personal introduction here. This should be the quickest summary of your background, your interests, and what kind of technical work or learning you focus on.

## What I Do

Use this section for your current work, areas of study, technical strengths, or the kinds of problems you like to solve.

## Interests

Add a short section about the topics you care about most. This could include data, analytics, software, automation, learning, or anything else you want your site to reflect.

## Current Focus

Describe what you are building, studying, or improving right now. This works well as a bridge between the About page and your Projects section.

## What You Will Find Here

- `Projects` for larger builds, portfolio work, and things in progress
- `Posts` for reflections, updates, lessons learned, and smaller write-ups

## Contact

You can close with a short note about how people can reach you or where they can follow your work.
