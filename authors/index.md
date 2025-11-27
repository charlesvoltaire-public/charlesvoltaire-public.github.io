---
layout: default
title: Authors
---
<nav class="breadcrumb">
  <a href="/">Home</a> → Authors
</nav>

<h1>Authors</h1>

<ul>
  {% assign authors = site.pages | where:"layout","author" | sort:"title" %}
  {% for author in authors %}
    <li><a href="{{ author.url }}">{{ author.title }}</a></li>
  {% endfor %}
</ul>
