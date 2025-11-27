---
layout: default
title: Short Story
---
<nav class="breadcrumb">
  <a href="/">Home</a> → Short Story
</nav>

<h1>Short Story</h1>

<ul>
  {% assign stories = site.pages | where:"categories","short-story" | sort:"date" | reverse %}
  {% for story in stories %}
    <li><a href="{{ story.url }}">{{ story.title }}</a></li>
  {% endfor %}
</ul>
