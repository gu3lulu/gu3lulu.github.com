---
title: Y = N * ( 1 + p )^x
layout: page
---

<ul class="listing">
{% for post in site.posts %}
  {% capture month %}
      {{post.date | date:"%B %Y"}}
  {% endcapture %}
  {% if last_month != month %}
      {% if last_month %}
      {% endif %}
      <li class="listing-seperator">{{ month }}</li>
      <li class="listing-item">
      <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%b %d" }}</time>
      <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
      </li>
      {% assign last_month = month %}
  {% else %}
      <li class="listing-item">
      <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%b %d" }}</time>
      <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
      </li>
  {% endif %}
{% endfor %}
</ul>

