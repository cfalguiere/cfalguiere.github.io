---
layout: landpage
title: Landpage
date: '2017-12-29 11:30:00 CET'
category: Landpage
published: true
assetsFolder: /assets/
defaultThumbnail: /assets/blog/images/thumbnail-default-150x150.png
---

{% for post in site.posts %}
  <div style="margin-left:5px;float:left;">
    <a href="{{ post.url | relative_url  }}" ><img style="float:left;" src="{{ post.thumbnail | default: page.defaultThumbnail }}"> </a>
  </div>

  <div style="margin-left:15px;float:left;">
    {% for tag in post.tags %}
      <span style="background-color:#333333;font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
    {% endfor %}
    <br>
    <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    <br>
    <small class="post-date" style="color:grey;">{{ post.date | date_to_string }}</small>
    <small class="post-date" style="color:grey;">
      {% for tag in post.tags %}
        <span style="font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
      {% endfor %}

    </small>
  </div>

  <div style="clear: both;">
  </div>
  <hr>

{% endfor %}


<!--
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
-->
