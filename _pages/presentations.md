---
permalink: /presentations/
title: "Presentations"
classes: wide
assets_folder: /assets/images/presentations/
author: cfalguiere
banner: /assets/images/banner-1200-300.png
presentation_baseurl: http://cfalguiere.github.io/Presentations/
---
{% for group in site.data.presentations.groups %}
{{ group.name }}

  {% for item in group.items %}

  {% if item.hasOwnProperty('relative_url') %}
    {% assign url = page.presentation_baseurl | append: item.relative_url  %}
  {% else %}
    {% assign url = item.url %}
  {% endif %}

  <a href="{{ url }}" target="blank">{{ item.name }}</a> <span style="font-size: 0.7em">{{ item.lang }}  {{ item.year }}</span>

  {% endfor %}

{% endfor %}
