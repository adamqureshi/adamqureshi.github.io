---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Short notes on building a simple investing process, sales, and how markets work (in plain English).

{% for post in site.posts %}
<div class="card">
  <div class="kicker">{{ post.date | date: "%B %e, %Y" }}</div>
  <h2 style="margin-top:0.4rem;"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  {% if post.excerpt %}
  <p class="small">{{ post.excerpt | strip_html | truncate: 180 }}</p>
  {% endif %}
</div>
{% endfor %}
