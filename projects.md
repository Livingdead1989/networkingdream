---
layout: default
title: Projects
permalink: /projects/
---

<main>
  <h1>Projects</h1>

  <div class="cards">
    {% for project in site.projects %}
      <a class="card hover-raise" href="{{ project.url | relative_url }}">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
      </a>
    {% endfor %}
  </div>
</main>