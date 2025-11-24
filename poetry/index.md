---
layout: default
title: Poetry
permalink: /poetry/
---

← <a href="/">Home</a>

# Poetry

{% assign poems = site.pages | where_exp: "p", "p.categories contains 'poetry'" | sort: 'date' | reverse %}
{% for poem in poems %}
- <a href="{{ poem.url }}">{{ poem.title }}</a>  
  — {{ poem.author }}
{% endfor %}

{% if poems.size == 0 %}
<p><em>No poems yet — the first one is coming soon.</em></p>
{% endif %}
