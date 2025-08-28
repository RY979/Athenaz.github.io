---
layout: single
title: "Gallery"
permalink: /gallery/
classes: wide
author_profile: true
---

<div class="gallery-grid">

  <!-- First 9 manually ordered -->
  <div class="gallery-item"><img src="/assets/gallery/DSC02842 copy Large.jpeg" alt="DSC02842"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02795 Large.jpeg" alt="DSC02795"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02770 Large.jpeg" alt="DSC02770"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC00047 Large.jpeg" alt="DSC00047"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSCF0423 Large.jpeg" alt="DSCF0423"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC01944 Large.jpeg" alt="DSC01944"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC01232 Large.jpeg" alt="DSC01232"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC00743 Large.jpeg" alt="DSC00743"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02187 Large.jpeg" alt="DSC02187"></div>

 <!-- Rest of gallery (excluding the featured 9) -->
  {% assign pics = site.static_files | where_exp: "f", "f.path contains '/assets/gallery/'" %}
  {% for f in pics %}
    {% unless f.path contains 'DSC02744 copy Large.jpeg'
          or f.path contains 'DSC02795 Large.jpeg'
          or f.path contains 'DSC02770 Large.jpeg'
          or f.path contains 'DSC00047 Large.jpeg'
          or f.path contains 'DSC0423 copy Large.jpeg'
          or f.path contains 'DSC01944 Large.jpeg'
          or f.path contains 'DSC01232 Large.jpeg'
          or f.path contains 'DSC00743 Large.jpeg'
          or f.path contains 'DSC02187 Large.jpeg' %}
      <div class="gallery-item"><img src="{{ f.path | relative_url }}" alt="{{ f.name }}" loading="lazy"></div>
    {% endunless %}
  {% endfor %}

</div>
