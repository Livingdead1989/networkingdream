---
layout: default
title: Tags
permalink: /tags/
---

<main>
  <h1>Tags</h1>

  <ul class="tag-list">
    {% assign all_tags = "" | split: "" %}

    {% for post in site.posts %}
      {% for tag in post.tags %}
        {% assign all_tags = all_tags | push: tag %}
      {% endfor %}
    {% endfor %}

    {% for project in site.projects %}
      {% for tag in project.tags %}
        {% assign all_tags = all_tags | push: tag %}
      {% endfor %}
    {% endfor %}

    {% assign all_tags = all_tags | uniq | sort %}

    {% for tag in all_tags %}
      <li>
        <a href="{{ '/tags/' | append: tag | append: '/' | relative_url }}">
          {{ tag }}
        </a>
      </li>
    {% endfor %}
  </ul>
</main>
