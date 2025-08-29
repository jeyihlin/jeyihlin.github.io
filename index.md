---
layout: default
title: Home
---

# Welcome

This is your new blog on **GitHub Pages**. Create posts in the `_posts/` folder using the format `YYYY-MM-DD-title.md`.

- Edit this page in `index.md`.
- Add an About page in `about.md`.
- Write your first post in `_posts/`.

Below is a list of your posts:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span style="color: gray; font-size: 0.9em;">— {{ post.date | date: "%Y-%m-%d" }}</span>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

nav: 
  - name: Gallery
    link: /gallery/
