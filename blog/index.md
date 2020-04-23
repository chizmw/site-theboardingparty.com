---
layout: posts
title: Blog
permalink: /blog/
menufontawesome: fad fa-paragraph
---

<ul>
  {% for author in site.authors %}
    <li><a href="{{ author.url }}">{{ author.title }}</a></li>
  {% endfor %}
</ul>
