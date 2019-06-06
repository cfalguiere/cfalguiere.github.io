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

test
{% endfor %}

{% assign group = site.data.presentations.groups['Clojure'] %}
{% for item in group.items %}
  {% if item.relative_url != "" %}
    [{{ item.name }}]({{ site.baseurl }}{{ item.relative_url }})   
    {{ item.lang }}  {{ item.year }}
  {% else %}
    [{{ item.name }}]({{ item.url }})   
    {{ item.lang }}  {{ item.year }}
  {% endif %}
{% endfor %}
