---
permalink: /presentations/
title: "Presentations"
classes: wide
assets_folder: /assets/images/presentations/
author: cfalguiere
banner: /assets/images/banner-1200-300.png
---
{% for group in site.data.presentations.groups %}
{{ group.name }}

  {% for item in group.items %}

  has property: {{ item.hasOwnProperty('relative_url') }}
  url: {{ item.url }}
  relative_url: {{ item.relative_url }}

  {% if item.hasOwnProperty('relative_url') %}
    {% capture url %} http://cfalguiere.github.io/Presentations/{{ item.relative_url }}{% endcapture %}
  {% else %}
    {% assign url = item.url %}
  {% endif %}

  <a href="{{ url }}" target="blank">{{ item.name }}</a> <span style="font-size: 0.7em">{{ item.lang }}  {{ item.year }}</span>

  {% endfor %}

{% endfor %}
