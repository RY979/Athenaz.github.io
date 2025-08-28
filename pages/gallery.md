---
layout: single
title: "Gallery"
permalink: /gallery/
classes: wide
author_profile: true
---

<div class="gallery-grid">

  <!-- First 9 manually ordered -->
  <div class="gallery-item"><img src="/assets/gallery/DSC02744 copy Large.jpeg" alt="DSC02744"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02795 Large.jpeg" alt="DSC02795"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02770 Large.jpeg" alt="DSC02770"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC00047 Large.jpeg" alt="DSC00047"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSCF0423 Large.jpeg" alt="DSCF0423"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC01944 Large.jpeg" alt="DSC01944"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC01232 Large.jpeg" alt="DSC01232"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC00743 Large.jpeg" alt="DSC00743"></div>
  <div class="gallery-item"><img src="/assets/gallery/DSC02187 Large.jpeg" alt="DSC02187"></div>

  <!-- Rest auto-loaded -->
  {% for f in site.static_files %}
    {% if f.path contains 'assets/gallery' %}
      {% unless f.path contains 'DSC02744' or f.path contains 'DSC02795' or f.path contains 'DSC02770' or f.path contains 'DSC00047' or f.path contains 'DSC0423' or f.path contains 'DSC01944' or f.path contains 'DSC01232' or f.path contains 'DSC00743' or f.path contains 'DSC02187' %}
        <div class="gallery-item"><img src="{{ f.path }}" alt="{{ f.name }}"></div>
      {% endunless %}
    {% endif %}
  {% endfor %}

</div>
