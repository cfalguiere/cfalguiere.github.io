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
      <a href="#{{ group.name | slugify }}" class="post-tag">{{ group.name }} </a>
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  </div>
  <hr/>
</div>
