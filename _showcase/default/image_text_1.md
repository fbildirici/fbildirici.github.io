---
show: true
width: 12
date: 2024-08-30 00:01:00 +0800
group: Collections
title: Favorite Resources & Tips
description: My favorite sources and practical tips for web and AI projects.
---

<div>
  <img data-src="{{ '/assets/images/covers/cover1.jpg' | relative_url }}" class="lazy w-100 rounded-xl" src="{{ '/assets/images/empty_300x200.png' | relative_url }}">

  <div class="card-img-overlay" style="overflow: auto; background: rgba(255,255,255,0.85); padding: 1rem;">
    <h5 class="card-title">My Favorite Collections</h5>
    <p class="card-text">
      Here you'll find a curated selection of resources, videos, and practical tips I use for web and AI projects.
    </p>
    <ul>
      <li><a href="https://distill.pub/" target="_blank">Distill.pub</a> — Interactive machine learning articles</li>
      <li><a href="https://paperswithcode.com/" target="_blank">Papers with Code</a> — ML papers & code</li>
      <li><a href="https://www.youtube.com/watch?v=NJ0bFj4sTzI" target="_blank">MIT Deep Learning Lectures</a></li>
    </ul>
    <hr>
    <h6 class="card-title">Tip: Image Lazyload</h6>
    <p class="card-text">
      Use lazyload for images to improve page loading speed, especially for pages with many images.
      Example code snippet:
    </p>
    <p class="card-text">
      {% raw %}
      <code>&lt;img data-src=&quot;[Image URL]&quot; class=&quot;lazy w-100 rounded-xl&quot; src=&quot;{{ '/assets/images/empty_300x200.png' | relative_url }}&quot;&gt;</code>
      {% endraw %}
    </p>
  </div>
</div>