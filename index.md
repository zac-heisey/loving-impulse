---
layout: layouts/list.html
title: Home
description: {{ site.description }}
---

<!-- Display 5 most recent blog posts -->
{% assign first = collections.post limit:5 reversed | last %}
{% for post in collections.post limit:5 reversed %}
  {% include partials/list.html %}
{% endfor %}
