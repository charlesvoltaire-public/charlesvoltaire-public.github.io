---
title: Voltaire Press
---

# Voltaire Press

Writing, Poetry and the Metaphysical News

## Latest
{% for post in site.posts limit:6 %}
- [{{ post.title }}]({{ post.url }}) – {{ post.date | date:"%b %d, %Y" }}
{% endfor %}

[All writing →](/user/)
