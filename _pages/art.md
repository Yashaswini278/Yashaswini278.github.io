---
layout: page
title: art
permalink: /art/
description: I started doing art in the summer of 2023. It gave me an incredible opportunity to see the world around me in detail. 
<br> These are some of my work. 
nav: true
nav_order: 4
#display_categories: [work, fun]
images:
  - image_path: assets/img/art/starry_night.jpg
    title: Starry Night
  - image_path: assets/img/art/flower.jpg
    title: Flower
---

<ul class="art">
  {% for image in page.images %}
    <li><img src="{{ image.image_path }}" alt="{{ image.title}}"/></li>
  {% endfor %}
</ul>

