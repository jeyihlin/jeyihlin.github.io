---
layout: default
title: Home
---

# Welcome

This is your new blog on **GitHub Pages**. Create posts in the `_posts/` folder using the format `YYYY-MM-DD-title.md`.

- Edit this page in `index.md`.
- Add an About page in `about.md`.
- Write your first post in `_posts/`.

<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> {{ post.excerpt }}</li>
  {% endfor %}
</ul>
