---
layout: default
title: Showcase
navbar_title: Showcase
container_class: container-xl
---

<h1>Showcase</h1>

<!-- Badges bölümü -->
{% include widgets/badges.html %}

<!-- Collections bölümü -->
{% assign collections = site.showcase | where: "group", "Collections" %}
{% for item in collections %}
  <div class="mb-4">
    {{ item.content | markdownify }}
  </div>
{% endfor %}

<!-- Diğer fotoğraf ve kartlar -->
<div class="row">
  {% assign others = site.showcase | where_exp: "item", "item.group != 'Collections'" %}
  {% for item in others %}
    <div class="col-lg-4 col-md-6 col-sm-12 mb-4 d-flex">
      <div class="card h-100 w-100">
        {% if item.image %}
          <img src="{{ item.image }}" class="card-img-top" alt="{{ item.title }}">
        {% endif %}
        <div class="card-body">
          <h5 class="card-title">{{ item.title }}</h5>
          <p class="card-text">{{ item.description }}</p>
          {{ item.content | markdownify }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>