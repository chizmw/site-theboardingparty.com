---
layout: page
title: Hosts (Part Time Gamers)
exclude: true
permalink: /groups/part-time-gamers/hosts/
menufontawesome: fas fa-dice
---

## Hosts

It's useful to have an idea of where the hosts are based.

Clearly we can't navigate to the exact address ... there are some scary people on the internet! ;-)

{%  comment %}
{% google_map no_cluster src="_data/hosts-map.yml" %}
{%  endcomment %}

### More Information

Learn more about each host by viewing their details page:

<ul>
{% assign sitepages = site.pages | sort: 'order' %}
{% for sitepage in sitepages %}
{% if sitepage.url != '/people/' %}
 {% if sitepage.url contains '/people/' and sitepage.isperson %}
  <li {% if page.url == sitepage.url %} class="active"{% endif %}>
    <i class="fas fa-user-circle"></i>
    <a href="{{ sitepage.url }}">{{ sitepage.title }}</a>
  </li>
 {% endif %}
{% endif %}
{% endfor %}
</ul>
