---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Bennett Chidoro
---

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
