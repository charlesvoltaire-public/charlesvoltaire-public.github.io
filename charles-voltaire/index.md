---
layout: default
title: Charles Voltaire
permalink: /charles-voltaire/
---
<nav class="breadcrumb">
  <a href="/">Home</a> → <a href="/authors/">Authors</a> → Charles Voltaire
</nav>
<h1>All Writing</h1>
<ul>
  {% assign posts = site.pages | where:"author","Charles Voltaire" | sort:"date" | reverse %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {% if post.date %} — {{ post.date | date:"%B %d, %Y" }}{% endif %}
      {% if post.categories %} ({{ post.categories | join:", " }}){% endif %}
    </li>
  {% endfor %}
</ul>
