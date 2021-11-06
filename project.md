---
layout: default
title: Catatan
---

# 💻️ Project

This page contains all project that I have been working, the content will be delivered in english.

{% assign postsByYearMonth = site.project | sort: 'date' | reverse | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <!-- <h3>{{ yearMonth.name }}</h3> -->
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}