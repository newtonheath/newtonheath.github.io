---
layout: page
title: Categories
permalink: /categories/
---

<ul>
{% for category in site.categories %}
  <li><a href="/category/{{ category[0] | downcase }}">{{ category[0] }}</a> ({{ category[1].size }})</li>
{% endfor %}
</ul>
