---
layout: default
title: Posts
permalink: /posts/
---

### Latest Posts

<ul>
  {% for post in site.posts %}
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
      <h4><a href="{{ post.url }}" class="link--post">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

---

<!--
### FME Form Posts
<ul>
  {% for post in site.tags.fme-form %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

---

### FME Flow Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

---

### Ansible Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>

---

### Home Assistant Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

---

### Power Automate Posts
<ul>
  {% for post in site.tags.fme-flow %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }} {{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

-->
