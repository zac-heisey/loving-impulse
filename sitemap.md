---
layout: layouts/base.html
title: Sitemap
---

{% for item in collections.all %}
  ### [{{ item.data.title }}]({{ item.url }})
{% endfor %}
