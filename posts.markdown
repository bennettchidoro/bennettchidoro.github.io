---
layout: default
title: Posts
permalink: /posts/
---

<div class="mw7  mr4 mt5">
  <h1 class="f2 mb4 tl">All Posts</h1>
  <ul class="list pa0">
    {% assign last_year = "" %}
    {% for post in site.posts %}
      {% assign current_year = post.date | date: "%Y" %}

      {% if current_year != last_year %}
        <h3 class="">{{ current_year }}</h3>
        {% assign last_year = current_year %}
      {% endif %}

      <li class="mb4-l mb3">
        <span class="ttu f7 b mr2 tracked grey db-l dn">
          {{ post.date | date: "%B %-d" }}
        </span>
        <a href="{{ post.url }}" class="f4">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
</div>
