---
title: Blog
layout: default
permalink: /blog/
---

# Blog

Thoughts on data analysis, forecasting, and side projects.

{% if paginator and paginator.posts %}
{% for post in paginator.posts %}
- **[{{ post.title }}]({{ post.url }})** — <span class="muted">{{ post.date | date: "%b %d, %Y" }}</span>  
  {{ post.excerpt | strip_html | truncate: 160 }}
{% endfor %}

<nav>
{% if paginator.previous_page %}[← Newer]({{ paginator.previous_page_path }}){% endif %}
{% if paginator.next_page %} | [Older →]({{ paginator.next_page_path }}){% endif %}
</nav>
{% else %}
_No posts yet. Soon!_
{% endif %}
