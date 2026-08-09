---
layout: page
title: "Research Projects"
permalink: /projects/
---

Below are summaries of my active and past projects.

<div class="project-list">
  {% assign sorted_projects = site.pages | where_exp: "item", "item.path contains 'projects/'" | where_exp: "item", "item.path != 'projects/index.md'" %}
  
  {% for project in sorted_projects %}
    <div class="project-card" style="margin-bottom: 2rem;">
      <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
      <p>{{ project.description }}</p>
      <a href="{{ project.url | relative_url }}" class="btn">Read More &rarr;</a>
    </div>
  {% endfor %}
</div>