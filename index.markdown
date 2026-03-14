---
layout: home
---

<section class="home-hero">
  <div class="profile-pic">
    {% if site.profile_image %}
    <img src="{{ site.profile_image | relative_url }}" alt="{{ site.author_name | default: site.title }} profile picture">
    {% else %}
    <div class="profile-pic-placeholder">{{ site.author_name | default: site.title | slice: 0 }}</div>
    {% endif %}
  </div>
  <div>
    <span class="eyebrow">About, projects, and writing</span>
    <h1>Personal portfolio and interests</h1>
    <p class="home-lead">
      A collection of projects, reflections, and ideas from a data driven, technical guy eager to learn.
    </p>
    <div class="hero-actions">
      <a class="button-link button-link-primary" href="/about/">Read About</a>
      <a class="button-link" href="/projects/">View Projects</a>
      <a class="button-link" href="/posts/">Browse Posts</a>
    </div>
  </div>
</section>

<section class="section-header">
  <div>
    <h2>Start here</h2>
    <p>Three clear entry points: who you are, what you build, and what you write.</p>
  </div>
</section>

<section class="home-grid">
  <article class="panel">
    <h2><a href="/about/">About</a></h2>
    <p>
      Use this section for your background, current work, interests, and a short personal introduction.
    </p>
  </article>
  <article class="panel">
    <h2><a href="/projects/">Projects</a></h2>
    <p>
      Showcase bigger efforts, ongoing builds, and portfolio work with room for status, stack, and links.
    </p>
  </article>
  <article class="panel">
    <h2><a href="/posts/">Posts</a></h2>
    <p>
      Keep smaller reflections, progress notes, updates, and essays organized in one clean archive.
    </p>
  </article>
</section>
