---
layout: default
title: Catatan
---

# 💻️ Project

This page contains all project that I have been working, the content will be delivered in english.

{% assign postsByCategories = site.project | sort | group_by_exp: "post", "post.categories"  %}
{% for categories in postsByCategories %}
  <h3 id="{{ categories.name }}">{{ categories.name }}</h3>
  <ul>
    {% for post in categories.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
  <h3 id="project">Personal Project</h3>
  - <i>Coming soon</i>

<br>
<hr>