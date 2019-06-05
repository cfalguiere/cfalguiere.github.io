---
permalink: /presentations/
title: "Presentations"
layout: splash
classes: wide
assets_folder: /assets/posters/
---
<div>
  <span style="font-size:2em;font-family: 'Source Sans Pro, sans-serif;font-weight: bold;">Les présentations</span>

</div>
{% for group in site.data.presentations.groups %}
{{ group.name }}

    {% for item in group.items %}
      {% if item.relative_url != "" %}
        {% assign url = site.data.presentations.url_prefix + item.relative_url %}
      {% else %}
        {% assign url = item.url %}
      {% endif %}
      {{ item.name }}   {{ item.lang | "" }}  {{ item.year | "" }}
    {% endfor %}

{% endfor %}
