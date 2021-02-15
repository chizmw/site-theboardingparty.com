---
layout: page
title: Groups
exclude: false
permalink: /groups/
menufontawesome: fad fa-users
---

{% include link-up.md %}

For more information about any of these groups, please follow the relevant link:

<ul>
{% assign sitepages = site.pages | sort: 'order' %}
{% for sitepage in sitepages %}
{% if sitepage.url != '/groups/' %}
 {% if sitepage.url contains '/groups/' and sitepage.isgroup %}
  <li {% if page.url == sitepage.url %} class="active"{% endif %}>
    {%-if page.menufontawesome%}<i class="{{page.menufontawesome}}"></i>{%endif%}
    <a href="{{ sitepage.url }}">{{ sitepage.title }}</a>
  </li>
 {% endif %}
{% endif %}
{% endfor %}
</ul>
