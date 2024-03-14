---
layout: default
title: Posts
permalink: /posts/
---

# Latest Posts

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>
