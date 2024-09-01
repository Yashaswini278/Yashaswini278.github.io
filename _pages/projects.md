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
<div class="projects-container">
  <div class="projects-sidebar">
    <h2>Projects</h2>
    <ul>
      {%- assign sorted_projects = site.projects | sort: "importance" -%}
      {%- for project in sorted_projects -%}
        <li><a href="#{{ project.title | slugify }}">{{ project.title }}</a></li>
      {%- endfor %}
    </ul>
  </div>

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
</div>

<!-- Add CSS to control the layout -->
<style>
.projects-container {
  display: flex;
  align-items: flex-start;
}

.projects-sidebar {
  width: 20%;
  background-color: #f4f4f4;
  padding: 20px;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
}

.projects-content {
  width: 80%;
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
