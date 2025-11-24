---
title: Voltaire Press
---

# Voltaire Press

Writing, Poetry and the Metaphysical News

## All posts
{% assign sorted = site.posts | sort: 'date' | reverse %}
{% for post in sorted %}
- [{{ post.title }}]({{ post.url }})  
  <small>— {{ post.date | date:"%b %d, %Y" }}{% if post.author %} by {{ post.author }}{% endif %}</small>
{% endfor %}
