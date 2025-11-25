---
layout: default
title: Authors
permalink: /authors/
---

<nav style="margin:2rem 0 1.5rem; font-size:0.95em; color:#666;">
  <a href="/">Home</a> › <a href="/authors/">Authors</a> › {{ page.title }}
</nav>

<h1 style="margin: 0 0 2rem; font-size: 2.2em;">Authors</h1>

{% assign author_list = site.pages | where: "layout", "author" | sort: "title" %}
{% for author in author_list %}
- <a href="{{ author.url }}">{{ author.title }}</a>
{% endfor %}

{% if author_list.size == 0 %}
<p><em>No author pages yet.</em></p>
{% endif %}
