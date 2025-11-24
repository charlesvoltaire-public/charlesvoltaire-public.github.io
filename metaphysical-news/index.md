---
layout: default
title: Metaphysical News
permalink: /news/
---

<nav style="margin: 2rem 0 1.5rem; font-size: 0.95em; color: #666;">
  <a href="/">Voltaire Press</a> › Metaphysical News
</nav>

<h1 style="margin: 0 0 2rem; font-size: 2.2em;">Metaphysical News</h1>

{% assign news_posts = site.pages | where: "layout", "news" | sort: 'date' | reverse %}
{% for post in news_posts %}
- <a href="{{ post.url }}">{{ post.title }}</a>  
  <small style="color:#666;">— {{ post.date | date:"%b %d, %Y" }} by {{ post.author }}</small>
{% endfor %}

{% if news_posts.size == 0 %}
<p><em>No news yet — the first dispatch is coming soon.</em></p>
{% endif %}
