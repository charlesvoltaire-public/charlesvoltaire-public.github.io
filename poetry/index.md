---
title: Poetry
permalink: /poetry/
---

# Poetry

{% assign poetry_posts = site.posts | where_exp: "post", "post.categories contains 'poetry'" | sort: 'date' | reverse %}
{% for post in poetry_posts %}
- [{{ post.title }}]({{ post.url }})  
  <small>— {{ post.date | date:"%b %d, %Y" }} by {{ post.author }}</small>
{% endfor %}

[← Back to all posts](/)
