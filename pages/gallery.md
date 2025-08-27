---
layout: single
title: "Gallery"
permalink: /gallery/
classes: wide       
author_profile: true
---


<div class="gallery-grid">
{% assign pics = site.static_files | where_exp: "f", "f.path contains '/assets/gallery/'" | sort: "path" %}
{% for f in pics %}
  <a href="{{ f.path }}" class="gallery-item">
    <img src="{{ f.path }}" 
     alt="{{ f.name | split: '.' | first }}" 
     loading="lazy">
  </a>
{% endfor %}
</div>
