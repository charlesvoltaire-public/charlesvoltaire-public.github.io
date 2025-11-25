---
layout: default
title: Poetry
permalink: /poetry/
---

<nav style="margin:2rem 0 1.5rem; font-size:0.95em; color:#666;">
  <a href="/">Home</a> › {{ page.title }}
</nav>

<h1 style="margin: 0 0 2rem; font-size: 2.2em;">Poetry</h1>

{% assign poems = site.pages | where_exp: "p", "p.categories contains 'poetry'" | sort: 'date' | reverse %}
{% for poem in poems %}
- <a href="{{ poem.url }}">{{ poem.title }}</a>  
  — {{ poem.author }}
{% endfor %}

{% if poems.size == 0 %}
<p><em>No poems yet — the first one is coming soon.</em></p>
{% endif %}
