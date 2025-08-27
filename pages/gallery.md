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
