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

---

## Jekyll Posts
<ul>
  {% for post in site.tags.jekyll %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>

---


## FME Form Posts
<ul>
  {% for post in site.tags.fme-form %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>

---

## FME Flow Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>
