---
layout: default
title: Retired Replicant Blogs
---

# Retired Replicant Blogs

Welcome to the **Retired Replicant Blogs**, where we reflect on technology, life, and the future. Dive into our minimalist and sleek design.

<div class="blog-list">
  {% for post in site.posts %}
    <div class="blog-tile">
      <h2>{{ post.title }}</h2>
      <p class="date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <button class="read-more" onclick="toggleContent('{{ post.url | relative_url }}')">Read more</button>
      <div class="full-content" id="content-{{ post.id }}" style="display: none;">
        <div class="content-body">
          <h3>{{ post.title }}</h3>
          <p class="date">{{ post.date | date: "%B %d, %Y" }}</p>
          <div class="content">{{ post.content }}</div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<script>
  function toggleContent(postUrl) {
    var content = document.getElementById('content-' + postUrl);
    if (content.style.display === 'none') {
      content.style.display = 'block';
    } else {
      content.style.display = 'none';
    }
  }
</script>
