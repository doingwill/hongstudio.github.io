---
layout: blog
title: 最新动态
permalink: /blog/
---
{% for post in site.posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <time>{{ post.date | date: "%Y-%m-%d" }}</time>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}