---
layout: page
title: People
exclude: false
permalink: /people/
menufontawesome: fad fa-users
---

{% include link-up.md %}

Some people in the groups have publicly available board gaming related information.

For more information about any of these people, please follow the relevant link:

<ul>
{% assign sitepages = site.pages | sort: 'order' %}
{% for sitepage in sitepages %}
{% if sitepage.url != '/people/' %}
 {% if sitepage.url contains '/people/' and sitepage.isperson %}
  <li {% if page.url == sitepage.url %} class="active"{% endif %}>
    {%-if page.menufontawesome%}<i class="{{page.menufontawesome}}"></i>{%endif%}
    <a href="{{ sitepage.url }}">{{ sitepage.title }}</a>
  </li>
 {% endif %}
{% endif %}
{% endfor %}
</ul>
