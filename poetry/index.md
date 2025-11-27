---
layout: default
title: Poetry
---
<nav class="breadcrumb">
  <a href="/">Home</a> → Poetry
</nav>

<h1>Poetry</h1>

<ul>
  {% assign poems = site.pages | where:"categories","poetry" | sort:"date" | reverse %}
  {% for poem in poems %}
    <li><a href="{{ poem.url }}">{{ poem.title }}</a></li>
  {% endfor %}
</ul>
