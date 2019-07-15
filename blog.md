---
layout: layouts/page.html
title: Latest Blog Posts
---

<!-- Pull in content from posts directory -->
{% for post in collections.post %}
  **[{{ post.data.title }}]({{ post.url }})**  
  Published: {{ post.date | date: "%b %d, %Y" }}
  {{ post.templateContent }}
{% endfor %}
