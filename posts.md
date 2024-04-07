---
layout: default
title: Posts
permalink: /posts/
---

### Latest Posts

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}" class="link--post">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

### Jekyll Posts
<ul>
  {% for post in site.tags.jekyll %}
    <li>
      <a href="{{ post.url }}" class="link--post">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

<!--
### FME Form Posts
<ul>
  {% for post in site.tags.fme-form %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

### FME Flow Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

### Ansible Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

### Home Assistant Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

### Power Automate Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

-->
