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

  {% if item.relative_url != "" %}
[{{ item.name }}]({{ site.baseurl }}{{ item.relative_url }})   
  {% else %}
[{{ item.name }}]({{ item.url }})   
  {% endif %}
{{ item.lang }}  {{ item.year }}

  {% endfor %}

{% endfor %}
