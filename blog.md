---
layout: post
title: Blog
---
  {% for post in site.posts limit:3 %}
  <a href="{{ post.url }}">{{ post.title }}</a>
  <p>{{ post.excerpt }}</p>
  {% endfor %}