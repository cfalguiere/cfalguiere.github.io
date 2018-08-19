---
layout: theme
title: Themes
date: '2017-12-27 10:30:00 CET'
tags: ['Theme']
published: true
assetsFolder: /assets/theme
---


<div class="tags-expo">
  <div class="tags-expo-list">
    {% for group in site.data.presentations.groups  %}
      <a href="#{{ group[0] | slugify }}" class="post-tag">{{ group[0].name }} )</a>
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for group in site.data.presentations.groups  %}
    <h2 id="{{ group | slugify }}">{{ group.name }}</h2>
    <ul class="tags-expo-posts">
      {% for item in group.items %}
        {% if item.relative-url != ""  %}
          {% assign url = site.data.presentations + item.relative-url %}
        {% else %}
          {% assign url = item.url %}
        {% endif %}
        <li>
        <a class="post-title" href="{{ url | }}">
        {{ item.name }}</a>
        <small class="post-date">{{ item.year | "" }}</small>
        <small class="post-date">{{ item.lang | "" }}</small>
        </li>

      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>
