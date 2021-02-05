---
layout: page
title: Problem Solving
permalink: /problem-solving/
---
<ul>
  {% for post in site.categories.problem-solving %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>