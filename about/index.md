---
layout: about
title: About
date: '2018-06-17 10:30:00 CET'
tags:
published: true
assetsFolder: /assets/about
---

Site personnel de Claude Falguière

Autres sites

{% assign links = site.data.links | where:'group', "perso" %}

<ul class="articles-list">
  {% for link in links %}
    <div data-scroll-reveal="enter ease 0">
    <a href="{{ link.url }}">
    <svg height="32" width="32">
        <polygon points="0,0 150,0 150,50 0,50" style="fill:#333333" />
    </svg>
    {% if link.icon != "" %}
      <image xlink:href="{{ link.icon }}" x="0" y="0" height="32px" width="32px"/>
    {% endif %}
    &nbsp;&nbsp;{{ link.title }} </a>
    </div>
  {% endfor %}
</ul>
