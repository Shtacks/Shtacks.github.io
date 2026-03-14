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
    <h1 class="about-name">{{ site.author_name | default: "Your Name" }}</h1>
    <p class="about-summary">Use this page as the main introduction to who you are, what you are building, and what readers should expect from this site.</p>
  </div>
</section>

Suggested sections

- what you do
- what you care about
- what this site is for

Keep it short and personal. A few paragraphs is enough, especially on mobile.

Example

I write about projects, ideas, and the work I am learning through. This page is the quick overview, and the posts section is where the longer-form writing lives.
