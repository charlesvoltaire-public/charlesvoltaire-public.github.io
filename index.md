---
title: Home
---

<center>
  "Those who can make you believe absurdities can make you commit atrocities" <br>
  - Voltaire
</center>


## All posts

{% assign all_content = site.pages | where_exp: "p", "p.categories != nil" | sort: 'date' | reverse %}
{% for page in all_content %}
{% if page.title and page.date %}
- [{{ page.title }}]({{ page.url | relative_url }})
  <small>— {{ page.date | date:"%b %d, %Y" }}{% if page.author %} by {{ page.author }}{% endif %}{% if page.categories %} ({{ page.categories | join: ", " }}){% endif %}</small>
{% endif %}
{% endfor %}

{% if all_content.size == 0 %}
<em>No posts yet — the first one is coming soon.</em>
{% endif %}

