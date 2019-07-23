---
layout: layouts/list.html
title: Home
description: {{ site.description }}
---

<!-- Display 5 most recent blog posts -->
{% for post in collections.post limit:5 reversed %}
<section class="list-item">
  <img src="{{ post.data.image }}" alt="{{ post.data.title }} featured image" class="thumbnail">
  <div class="list-item-info">
    <h2 class="title"><a href="{{ post.url }}">{{ post.data.title }}</a></h2>
    <p class="byline">By {{ site.author }} · Published: {{ post.date | date: "%b %d, %Y" }} · Tags: {% for tag in post.data.tags %}{% if tag != "post" %}<a href="/tags/{{ tag }}/">{{ tag }}</a> {% endif %}{% endfor %}</p>
    <p class="content">{{ post.templateContent | truncate: 250 }}</p>
  </div>
</section>
{% endfor %}