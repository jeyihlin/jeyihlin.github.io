---
layout: default
title: Art Gallery
permalink: /gallery/
images:
  - src: /assets/art/work1.jpg
    title: "Forest Reflection"
    desc: "Oil on canvas, 2025"
  - src: /assets/art/work2.jpg
    title: "Blue Pond"
    desc: "Ghibli-style watercolor"
  - src: /assets/art/work3.jpg
    title: "Autumn Leaves"
    desc: "Study in brown tones"
---

<style>
  body {
    background: linear-gradient(135deg, #0033cc 0%, #0099ff 55%, #00ccff 100%);
    color: #f7fbff;
  }
  .page-content, .page, .wrapper { background: transparent !important; }
  .gallery-title { text-align: center; margin: 2rem 0 1rem 0; letter-spacing: 0.02em; }
  .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
                  gap: 18px; margin: 0 auto 4rem auto; max-width: 1200px; padding: 0 1rem; }
  .card { background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.15);
          border-radius: 12px; overflow: hidden; box-shadow: 0 10px 24px rgba(0,0,0,0.18);
          transition: transform .2s ease, box-shadow .2s ease; }
  .card:hover { transform: translateY(-4px); box-shadow: 0 14px 30px rgba(0,0,0,0.28); }
  .card img { display: block; width: 100%; height: 260px; object-fit: contain; background: rgba(0,0,0,0.12); }
  .card figcaption { padding: 12px 14px 16px 14px; color: #ecf6ff; }
  .card figcaption h3 { margin: 0 0 6px 0; font-size: 1.05rem; line-height: 1.3; }
  .card figcaption p { margin: 0; opacity: 0.9; font-size: 0.95rem; }
  @media (max-width: 420px) { .card img { height: 200px; } }
</style>

<h1 class="gallery-title">Art Gallery</h1>

<div class="gallery-grid">
  {% for item in page.images %}
  <figure class="card">
    <img src="{{ item.src | relative_url }}" alt="{{ item.title | escape }}">
    <figcaption>
      <h3>{{ item.title }}</h3>
      <p>{{ item.desc }}</p>
    </figcaption>
  </figure>
  {% endfor %}
</div>
