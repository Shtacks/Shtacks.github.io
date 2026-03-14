---
layout: page
title: Posts
permalink: /posts/
---

<span class="eyebrow">Posts</span>

Browse recent writing below.

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <div class="post-date-block">{{ post.date | date: "%b %-d, %Y" }}</div>
    <div>
    <h3 class="post-card-title">
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    </h3>
    {% if post.excerpt %}
    <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 140 }}</p>
    {% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No posts yet.</p>
{% endif %}
