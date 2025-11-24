---
title: Charles Voltaire
permalink: /user/
---

# All Writing

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts %}
- [{{ post.title }}]({{ post.url }}) – {{ post.date | date:"%B %d, %Y" }}
{% endfor %}
