---
layout: page
title: projects
permalink: /projects/
description: Some of my personal projects.
nav: true
nav_order: 2
horizontal: true
---

<!-- pages/projects.md -->
<div class="projects-content">
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  {%- for project in sorted_projects -%}
  <div class="project" id="{{ project.title | slugify }}">
    <div class="project-box">
      <img src="{{ project.image }}" alt="{{ project.title }}">
    </div>
    <div class="project-description">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
  </div>
  {%- endfor %}
</div>

<!-- Add CSS to control the layout -->
<style>
.projects-content {
  padding: 20px;
}

.project {
  display: flex;
  margin-bottom: 20px;
}

.project-box {
  width: 30%;
  margin-right: 20px;
}

.project-box img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.project-description {
  width: 70%;
}
</style>
