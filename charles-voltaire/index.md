---
title: Charles Voltaire
permalink: /charles-voltaire/
---

<nav style="margin:2rem 0 1.5rem; font-size:0.95em; color:#666;">
  <a href="/">Home</a> › {{ page.title }}
</nav>

# All Writing

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url }}) – {{ post.date | date:"%B %d, %Y" }}
{% endfor %}
