---
layout: page
title: Beyond Academia
permalink: /beyondacademia/
description: I am a seasoned professional who combines academic rigor with deep sectoral experience to drive innovation and entrepreneurship. My journey spans managing innovation projects at HAVELSAN, leading digital transformation efforts, and spearheading corporate entrepreneurship programs. Through prestigious programs like the Hamdi Ulukaya Initiative and the Entrepreneurship Foundation, I have sharpened my skills and expanded my networks, resulting in impactful ventures, including securing investment in Zorlu Holding's Corporate Entrepreneurship Competition and founding startups in the gig economy and education technology sectors. As a mentor and board member for blockchain and SaaS startups, I am committed to nurturing entrepreneurial thinking in the next generation of business leaders. As a Future Innovation Leaders fellow, I continue to push the boundaries of what's possible in the innovation ecosystem.
nav: true
nav_order: 3
display_categories: [work, media]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
