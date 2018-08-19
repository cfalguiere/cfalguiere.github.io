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
    <svg height="24" width="24">
        <polygon points="0,0 24,0 24,24 0,24" style="fill:#CCCCCC" />
    {% if link.icon != "" %}
      <image xlink:href="{{ link.icon }}" x="4" y="4" height="16px" width="16px"/>
    {% endif %}
    </svg>
    &nbsp;&nbsp;{{ link.title }} </a>
    </div>
  {% endfor %}
</ul>
