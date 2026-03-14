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
    <h2>Recent Activity</h2>
    <p>The latest projects and posts from across the site.</p>
  </div>
</section>

<section class="home-grid">
  <article class="panel">
    <h2><a href="/projects/">Latest Projects</a></h2>
    {% if site.projects.size > 0 %}
    <ul class="feed-list">
      {% assign latest_projects = site.projects | sort: "order" %}
      {% for project in latest_projects limit: 3 %}
      <li>
        <a class="feed-link" href="{{ project.url | relative_url }}">{{ project.title | escape }}</a>
        {% if project.summary or project.excerpt %}
        <p>{{ project.summary | default: project.excerpt | strip_html | truncate: 110 }}</p>
        {% endif %}
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p>No projects published yet. Add entries to start building your project archive.</p>
    {% endif %}
  </article>
  <article class="panel">
    <h2><a href="/posts/">Latest Posts</a></h2>
    {% if site.posts.size > 0 %}
    <ul class="feed-list">
      {% for post in site.posts limit: 3 %}
      <li>
        <span class="feed-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <a class="feed-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncate: 110 }}</p>
        {% endif %}
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p>No posts published yet.</p>
    {% endif %}
  </article>
</section>
