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
    <p class="about-summary">I work in Business Intelligence and enjoy building clear systems, structured data models, and practical technical solutions.</p>
  </div>
</section>

## Overview

I'm a technically minded individual with a Bachelor of Science in Computer Science. I've always had a creative side, and I enjoy creating something new or designing efficient systems. I have worked in the Business Intelligence field for more than six years, where I put that technical mindset to practical use. In my free time, I like experimenting with new tools and building systems for myself.

## What I Do

My professional career has centered on Business Intelligence, with Power BI, SQL, and Excel as my primary tools, along with some Python, R, and other Microsoft technologies. In my current role, I manage everything related to our Power BI reporting environment on my own. That includes ETL, semantic modeling, report and dashboard development, requirements gathering, row-level and object-level security, data governance, DAX, M, and more.

I also work heavily with SQL to validate source data against the reporting layer, design tables and views for Power BI, and keep data structured and reliable. One principle I value highly is structured data, rather than what I often think of as the "wild west" approach that can happen when Excel becomes the default system for data management.

## Interests

My interests include:

- systems design
- data modeling
- reporting, especially financial reporting
- effective use of AI tools
- learning through experimentation
- swing dancing

## Current Focus

My current focus is on AI tooling, especially identifying useful applications and building some of them myself. AI has changed the way we think about technical work, and I believe it can be extremely valuable when used to enhance or support a workflow. Through my personal projects, I want to show practical ways AI can be used well and reflect how I like to work with it.

## What You Will Find Here

- **Projects:** a collection of projects I have worked on or am currently building
- **Posts:** smaller-scope reflections, ideas, updates, and thoughts that do not need to become full project pages

## Contact

The best way to contact me is by email at [{{ site.email }}](mailto:{{ site.email }}).
