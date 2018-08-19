---
layout: theme
title: Themes
date: '2017-12-27 10:30:00 CET'
tags: ['Theme']
published: true
assetsFolder: /assets/theme
---

<!--
<p>
  <ul class="tags">
    {% for tag in site.tags | sort %}
      {% assign t = tag | first %}
      {% assign posts = tag | last %}
      {% assign tagName = t | downcase | replace:" ","-"  %}
      {% assign tagCount = posts | size  %}
      <li>{{ tagName }} : {{ tagCount }} posts</li>
    {% endfor %}
</ul>
</p>
-->

<div class="tags-expo">
  <div class="tags-expo-list">
    {% for tag in site.tags %}
      {% assign postsCount = tag | last | size %}
      <a href="#{{ tag[0] | slugify }}" class="post-tag">{{ tag[0] }} ({{postsCount}})</a>
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for tag in site.tags %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag | first }}</h2>
    <ul class="tags-expo-posts">
      {% for post in tag[1] %}
        <a class="post-title" href="{{ site.baseurl }}{{ post.url }}">
      <li>
        {{ post.title }}
      <small class="post-date">{{ post.date | date_to_string }}</small>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>
