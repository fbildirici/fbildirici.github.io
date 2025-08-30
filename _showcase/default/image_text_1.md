---
show: true
width: 12
date: 2020-01-12 00:01:00 +0800
---


<div style="width:90%; max-width:600px; max-height:400px; margin:auto;">
  <img data-src="{{ '/assets/images/covers/cover1.jpg' | relative_url }}" 
       class="lazy rounded-xl" 
       style="width:100%; height:auto; max-height:400px; object-fit:cover;"
       src="{{ '/assets/images/empty_300x200.png' | relative_url }}">

  <div class="card-img-overlay" style="overflow:auto; background:rgba(255,255,255,0.85); padding:1rem; max-height:400px;">
    <h5 class="card-title">Image Lazyload</h5>
    <p class="card-text">
      It is highly recommended to use lazyload for images to improve page loading speed, especially for pages with many images.
      Example code snippet:
    </p>
    <p class="card-text">
      {% raw %}
      <code>&lt;img data-src=&quot;[Image URL]&quot; class=&quot;lazy w-100 rounded-xl&quot; src=&quot;{{ '/assets/images/empty_300x200.png' | relative_url }}&quot;&gt;</code>
      {% endraw %}
    </p>
  </div>
</div>
