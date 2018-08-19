---
layout: landpage
title: Landpage
date: '2017-12-29 11:30:00 CET'
category: Landpage
published: true
assetsFolder: /assets/
defaultThumbnail: /assets/blog/images/thumbnail-default-150x150.png
---

{% for post in site.posts limit: 1 %}

  <div style="margin-left:5px;margin-bottom:5px;float:left;">
    <a href="{{ post.url | relative_url  }}" ><img style="float:left;" src="{{ post.thumbnail | default: page.defaultThumbnail }}"> </a>
  </div>

  <div style="margin-left:15px;float:left;width:70%">
    {% for tag in post.tags %}
      <a href="/theme/index#{{ tag | slugify }}">
      <span style="background-color:#DD3664;color:white;font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
      </a>
      {% unless forloop.last %}, {% endunless %}
    {% endfor %}
    <br>
    <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    <br>
    <small class="post-date" style="color:grey;">{{ post.date | date_to_string }}</small>
    {% if post.summary != '' %}
      <br><br>
      <p style="color:white;font-style:italic;">
      {{ post.summary }}
      </p>
    {% endif %}
  </div>

  <div style="clear: both;margin-bottom:20px;">
  </div>
{% endfor %}

{% for post in site.posts offset: 1 limit: 4 %}

<div style="width:24%;margin-left:3px;margin-bottom:15px;float:left;">

    <div style="margin-bottom:5px;">
      <a href="{{ post.url | relative_url  }}" ><img style="float:left;" src="{{ post.thumbnail | default: page.defaultThumbnail }}"> </a>
    </div>
    {% for tag in post.tags %}
      <a href="/theme/index#{{ tag | slugify }}">
      <span style="background-color:#DD3664;color:white;font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
      </a>
      {% unless forloop.last %} {% endunless %}
    {% endfor %}
    <br>
    <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    <br>
    <small class="post-date" style="color:grey;">{{ post.date | date_to_string }}</small>
    <br>

</div>

{% endfor %}

<div style="clear: both;">
</div>


<div style="margin-left:5px;margin-bottom:20px;">
<br>
{% for post in site.posts offset: 5 %}
  <div>
    <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    <br>
    {% for tag in post.tags %}
      <a href="/theme/index#{{ tag | slugify }}">
      <span style="background-color:#DD3664;color:white;font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
      </a>
      {% unless forloop.last %}, {% endunless %}
    {% endfor %}
    <small class="post-date" style="color:grey;">{{ post.date | date_to_string }}</small>
  </div>
  <br>
{% endfor %}
<hr>
</div>

<div style="margin-left:5px;margin-bottom:20px;">
  <h3>Articles plus anciens</h3>
  <ul>
    <li>
      <a href="https://cfalguiere.wordpress.com/"> Aller sur Wordpress.com</a>
    </li>
  </ul>
</div>

