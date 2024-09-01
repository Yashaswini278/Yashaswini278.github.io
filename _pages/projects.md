---
layout: page
title: projects
permalink: /projects/
description: Some of my relevant personal projects, completed as part of coursework or out of personal interest
nav: true
nav_order: 2
---

<!-- pages/projects.md -->
<div class="projects-content">
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  {%- for project in sorted_projects -%}
  <div class="project" id="{{ project.title | slugify }}">
    <div class="project-details">
      <div class="project-box">
        <img src="{{ project.img | relative_url }}" alt="{{ project.title }}">
        <h3>{{ project.title }}</h3>
      </div>
      <div class="project-description">
        <p>{{ project.description }}</p>
        <a href="{{ project.redirect }}" target="_blank">View Project</a>
      </div>
    </div>
  </div>
  {%- endfor %}
</div>

<style>
.projects-content {
  padding: 20px;
}
.project {
  display: flex;
  margin-bottom: 40px;
  border-bottom: 1px solid #ccc;
  padding-bottom: 20px;
}
.project-details {
  display: flex;
  align-items: flex-start;
}
.project-box {
  width: 30%;
  margin-right: 20px;
  text-align: center;
}
.project-box img {
  width: 100%;
  height: auto;
  object-fit: cover;
  margin-bottom: 10px;
}
.project-box h3 {
  font-size: 1.2em;
  margin: 0;
}
.project-description {
  width: 70%;
}
.project-description p {
  margin-bottom: 10px;
}
</style>