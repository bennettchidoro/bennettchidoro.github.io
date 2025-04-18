---
layout: default
title: Books
permalink: /books/
---

<article class="f4 lh-copy pr6-l pl6-l">
  <div class="pa4 tl">
    <h1 class="f2 mb3">Books I've Read</h1>

    <blockquote class="ml0 pl3 bl bw2 b--primary mb4">
      “I have often reflected upon the new vistas that reading opened to me. I knew right there, in prison, that reading had changed forever the course of my life. As I see it today, the ability to read awoke inside me some long dormant craving to be mentally alive.”
      <br>
      <cite class="f6 db mt2 ttu tracked gray">— Malcolm X</cite>
    </blockquote>

    <ul class="list pl0">
      {% for book in site.data.books %}
        <li class="mb4">
          <span class="b">{{ book.title }}</span>
          {% if book.author %} by {{ book.author }}{% endif %}
          {% if book.year %} <span class="gray">({{ book.year }})</span>{% endif %}
        </li>
      {% endfor %}
    </ul>
  </div>
</article>
