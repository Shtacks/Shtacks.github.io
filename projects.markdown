---
layout: page
title: Projects
permalink: /projects/
---

<span class="eyebrow">Projects</span>

Browse larger efforts, completed builds, and things still in progress.

{% assign sorted_projects = site.projects | sort: "order" %}
{% if sorted_projects.size > 0 %}
<ul class="post-list project-list">
  {% for project in sorted_projects %}
  <li>
    <div class="post-date-block">{{ project.status | default: "Project" }}</div>
    <div>
      <h3 class="post-card-title">
        <a class="post-link" href="{{ project.url | relative_url }}">{{ project.title | escape }}</a>
      </h3>
      {% if project.summary or project.excerpt %}
      <p class="post-card-excerpt">{{ project.summary | default: project.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
      {% if project.stack %}
      <p class="project-card-meta">{{ project.stack | join: " / " }}</p>
      {% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
<div class="empty-state">
  <h2>No projects published yet.</h2>
  <p>Add Markdown files to <code>_projects/</code> to showcase current work and finished builds.</p>
</div>
{% endif %}
