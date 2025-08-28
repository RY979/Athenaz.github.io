---
layout: single
title: "Gallery"
permalink: /gallery/
classes: wide
author_profile: true
---

<div class="gallery-grid">

  <!-- Featured 9 -->
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC02842 copy Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC02744 copy Large.jpeg' | relative_url }}" alt="DSC02842" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC02795 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC02795 Large.jpeg' | relative_url }}" alt="DSC02795" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC02770 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC02770 Large.jpeg' | relative_url }}" alt="DSC02770" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC00047 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC00047 Large.jpeg' | relative_url }}" alt="DSC00047" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSCF0423 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC0423 copy Large.jpeg' | relative_url }}" alt="DSCF0423" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC01944 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC01944 Large.jpeg' | relative_url }}" alt="DSC01944" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC01232 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC01232 Large.jpeg' | relative_url }}" alt="DSC01232" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC00743 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC00743 Large.jpeg' | relative_url }}" alt="DSC00743" loading="lazy">
  </a>
  <a class="gallery-item glightbox" href="{{ '/assets/gallery/DSC02187 Large.jpeg' | relative_url }}" data-gallery="athena">
    <img src="{{ '/assets/gallery/DSC02187 Large.jpeg' | relative_url }}" alt="DSC02187" loading="lazy">
  </a>

  <!-- Rest (exclude the featured 9 so they don't repeat) -->
  {% assign pics = site.static_files | where_exp: "f", "f.path contains '/assets/gallery/'" %}
  {% for f in pics %}
    {% unless f.path contains 'DSC02842 copy Large.jpeg'
          or f.path contains 'DSC02795 Large.jpeg'
          or f.path contains 'DSC02770 Large.jpeg'
          or f.path contains 'DSC00047 Large.jpeg'
          or f.path contains 'DSCF0423 Large.jpeg'
          or f.path contains 'DSC01944 Large.jpeg'
          or f.path contains 'DSC01232 Large.jpeg'
          or f.path contains 'DSC00743 Large.jpeg'
          or f.path contains 'DSC02187 Large.jpeg' %}
      <a class="gallery-item glightbox" href="{{ f.path | relative_url }}" data-gallery="athena">
        <img src="{{ f.path | relative_url }}" alt="{{ f.name }}" loading="lazy">
      </a>
    {% endunless %}
  {% endfor %}
</div>
