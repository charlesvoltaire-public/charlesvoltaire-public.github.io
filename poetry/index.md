---
layout: default
title: Poetry
permalink: /poetry/
---

<nav style="margin:2rem 0 1.5rem; font-size:0.95em; color:#666;">
  <a href="/">Home</a> › Poetry
</nav>

<h1 style="margin:0 0 2rem; font-size:2.2em;">Poetry</h1>

{% assign items = site.pages | where_exp: "p", "p.categories contains 'poetry'" | sort: 'date' | reverse %}
{% for item in items %}
- <a href="{{ item.url }}">{{ item.title }}</a> — {{ item.author }}
{% endfor %}
