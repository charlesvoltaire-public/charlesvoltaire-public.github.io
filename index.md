---
title: Voltaire Press
---

# Voltaire Press

Writing, Poetry and the Metaphysical News

## All posts
{% assign all_posts = site.posts | where: "date", "" | concat: site.html_pages | where: "date", "" | sort: 'date' | reverse %}
{% for post in all_posts limit: 10 %}
{% if post.title %}
- [{{ post.title }}]({{ post.url | relative_url }})
  <small>— {{ post.date | date: "%b %d, %Y" }}{% if post.author %} by {{ post.author }}{% endif %}{% if post.categories %} ({{ post.categories | join: ", " }}){% endif %}</small>
{% endif %}
{% endfor %}
{% if all_posts.size == 0 %}
<p><em>No posts yet — the first one is coming soon.</em></p>
{% endif %}

[Poetry →](/poetry/)
