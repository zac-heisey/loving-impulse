---
layout: layouts/list.html
title: Home
description: {{ site.description }}
pagination:
  data: collections.post
  size: 5
  alias: posts
  reverse: true
---

<!-- Display 5 most recent blog posts -->
{% assign first = posts | first %}
{% for post in posts %}
  {% include partials/list.html %}
{% endfor %}
