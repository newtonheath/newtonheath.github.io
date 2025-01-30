---
layout: page
title: Categories
permalink: /categories/
---

<ul>
{% for category in site.categories %}
  {% capture category_name %}{{ category[0] }}{% endcapture %}
  {% assign category_page = site.pages | where: "category", category_name | first %}
  <li><a href="/category/{{ category_name | downcase }}">{{ category_page.title | default: category_name }}</a> ({{ category[1].size }})</li>
{% endfor %}
</ul>
