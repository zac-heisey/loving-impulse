---
layout: layouts/page.html
title: Home
description: Homepage description...
---

<!-- Display 5 most recent blog posts -->
{% for post in collections.post limit:5 reversed %}
  **[{{ post.data.title }}]({{ post.url }})**  
  By {{ post.author }} · Published: {{ post.date | date: "%b %d, %Y" }}
  Tags: {% for tag in post.data.tags %}{{ tag | remove: "post" }} {% endfor %}
  {{ post.templateContent | truncate: 100 }}
{% endfor %}
