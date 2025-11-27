---
layout: default
title: Metaphysical News
---
<nav class="breadcrumb">
  <a href="/">Home</a> → Metaphysical News
</nav>

<h1>Metaphysical News</h1>

<ul>
  {% assign news = site.pages | where:"categories","news" | sort:"date" | reverse %}
  {% for item in news %}
    <li><a href="{{ item.url }}">{{ item.title }}</a> — {{ item.date | date:"%B %d, %Y" }}</li>
  {% endfor %}
</ul>
