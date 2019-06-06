---
permalink: /presentations/
title: "Presentations"
layout: splash
classes: wide
assets_folder: /assets/posters/
---
<div>
  <span style="font-size:2em;font-family: 'Source Sans Pro', sans-serif;font-weight: bold;">Les présentations</span>

</div>
{% for group in site.data.presentations.groups %}
{{ group.name }}

    {% for item in group.items %}
      {% if item.relative_url != "" %}
        {% assign url = str.concat( site.data.presentations.url_prefix, item.relative_url ) %}
      {% else %}
        {% assign url = item.url %}
      {% endif %}
      <!--
      [{{ item.name }}]({{ url }})   {{ item.lang | "" }}  {{ item.year | "" }}
      -->
      <a href="{{url}}" target="_blank" class=".btn .btn--success .btn--large">{{ item.name }}</a>

    {% endfor %}

{% endfor %}
