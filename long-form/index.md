---
layout: default
title: Long Form
---
<nav class="breadcrumb">
  <a href="/">Home</a> → Long Form
</nav>

<h1>Long Form</h1>

<ul>
  {% assign pieces = site.pages | where:"categories","long-form" | sort:"date" | reverse %}
  {% for piece in pieces %}
    <li><a href="{{ piece.url }}">{{ piece.title }}</a></li>
  {% endfor %}
</ul>
