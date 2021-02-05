---
layout: page
title: About
permalink: /probelm-solving/
---
## Problem Çözümleri
<ul>
  {% for post in site.categories.problem-solving %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>