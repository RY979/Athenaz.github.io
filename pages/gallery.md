---
layout: single
title: "Gallery"
permalink: /gallery/
author_profile: true
---

<div class="gallery-grid">
{% assign pics = site.static_files | where_exp: "f", "f.path contains '/assets/gallery/'" | sort: "path" %}
{% for f in pics %}
  <a href="{{ f.path }}" class="gallery-item">
    <img src="{{ f.path }}" alt="{{ f.name | split: '.' | first }}">
  </a>
{% endfor %}
</div>
/* --- gallery grid --- */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  gap: 12px;
}
.gallery-item img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 8px;
  display: block;
}
.gallery-item:hover img { opacity: .9; }
