---
layout: page
title: 15_Cloud
---
{% for post in site.posts %}
  {% if post.category == 'cloud' %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
  {% endif %}
{% endfor %}
