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
      <!-- Corrected link to point to the individual blog post -->
      <a href="{{ post.url }}" class="read-more">Read more</a>
    </div>
  {% endfor %}
</div>
