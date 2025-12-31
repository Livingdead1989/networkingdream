---
layout: default
title: Blog
permalink: /blog/
---

<main>
  <h1>Blog</h1>

  <div class="cards">
    {% for post in site.posts %}
      <a class="card hover-raise" href="{{ post.url | relative_url }}">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </a>
    {% endfor %}
  </div>
</main>
