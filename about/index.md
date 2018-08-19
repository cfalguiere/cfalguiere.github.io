---
layout: about
title: About
date: '2018-06-17 10:30:00 CET'
tags:
published: true
assetsFolder: /assets/about
---

Site personnel de Claude Falguière

{% assign links = site.links | where:'group', "perso" %}

<ul class="articles-list">
  {% for link in links %}
    <div data-scroll-reveal="enter ease 0">
    <a href="{{ link.url }}">
    {% if link.icon != "" %} <img src="{{ link.icon }}" />  {% endif %}
    {{ link.title }} </a>
    </div>
  {% endfor %}
</ul>
