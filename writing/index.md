---
title: Writing
---

Essays and reflections on technology, leadership, scaling SaaS, and building sustainably.

## Guides (practical & evergreen)

Guides are structured resources drawn from real experience building and scaling software teams and products.

- → [Browse Guides](/guides/)

## Essays

<ul class="list">
  {% for post in site.posts %}
    <li>
      <a class="title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div class="meta">
        {{ post.date | date: "%B %-d, %Y" }}
        {% if post.category %}<span class="dot">•</span>{{ post.category }}{% endif %}
        {% if post.reading_time %}<span class="dot">•</span>{{ post.reading_time }}{% endif %}
      </div>
      {% if post.excerpt %}
        <div class="meta">{{ post.excerpt | strip_html | truncate: 160 }}</div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
