---
layout: theme
title: Présentations
date: '2017-12-27 10:30:00 CET'
tags: ['Theme']
published: true
assetsFolder: /assets/theme
---

<!--
<div class="tags-expo">
  <div class="tags-expo-list">
    {% for group in site.data.presentations.groups  %}
      <a href="#{{ group.name | slugify }}" class="post-tag">{{ group.name }} </a>
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  </div>
  <hr/>
</div>
-->

  <hr/>
  <div class="tags-expo-section">
    {% for group in site.data.presentations.groups  %}
    <h3 id="{{ group.name | slugify }}">{{ group.name }}</h3>
    <ul class="tags-expo-posts">
      {% for item in group.items %}
        {% if item.relative_url != "" %}
          {% assign url = site.data.presentations.url_prefix + item.relative_url %}
        {% else %}
          {% assign url = item.url %}
        {% endif %}
        <a class="post-title" href="{{ url }}">
        <li>
          {{ item.name }}
        </li>
        </a> {{ item.lang | "" }} {{ item.year | "" }}
      {% endfor %}
    </ul>
    <hr/>
    {% endfor %}
  </div>
