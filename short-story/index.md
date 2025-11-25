---
layout: default
title: Short Story
permalink: /short-story/
---

<nav style="margin:2rem 0 1.5rem; font-size:0.95em; color:#666;">
  <a href="/">Home</a> › Short Story
</nav>

<h1 style="margin:0 0 2rem; font-size:2.2em;">Short Story</h1>

{% assign items = site.pages | where_exp: "p", "p.categories contains 'shortstory'" | sort: 'date' | reverse %}
{% for item in items %}
- <a href="{{ item.url }}">{{ item.title }}</a> — {{ item.author }}
{% endfor %}
