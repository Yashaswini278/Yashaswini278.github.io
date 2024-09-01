---
layout: page
title: projects
permalink: /projects/
description: Some of my personal projects.
nav: true
nav_order: 2
#display_categories: [work, fun]
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
    {%- if site.enable_project_categories and page.display_categories %}
      <!-- Display categorized projects -->
      {%- for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {%- assign categorized_projects = site.projects | where: "category", category -%}
      {%- assign sorted_projects = categorized_projects | sort: "importance" %}
      <div class="project-list">
        {%- for project in sorted_projects -%}
        <div class="project" id="{{ project.title | slugify }}">
          {% include projects_horizontal.html %}
        </div>
        {%- endfor %}
      </div>
      {% endfor %}
    {%- else -%}
      <!-- Display projects without categories -->
      {%- assign sorted_projects = site.projects | sort: "importance" -%}
      <div class="project-list">
        {%- for project in sorted_projects -%}
        <div class="project" id="{{ project.title | slugify }}">
          {% include projects_horizontal.html %}
        </div>
        {%- endfor %}
      </div>
    {%- endif -%}
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

.project-list .project {
  margin-bottom: 20px;
}
</style>
