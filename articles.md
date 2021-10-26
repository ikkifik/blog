---
layout: default
title: Artikel
---

# 💡️ Artikel

Halaman untuk sharing ilmu. Gunakan <mark>Ctrl+F</mark> untuk mencari topik bahasan.
<!-- Group by post categories -->
{% assign postsByCategories = site.articles | sort: 'date' | reverse | group_by_exp: "post", "post.categories"  %}
{% for categories in postsByCategories %}
  <h3>{{ categories.name }}</h3>
  <ul>
    {% for post in categories.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %} 
  </ul>
{% endfor %}

<!-- Group by post date -->
<!-- {% assign postsByYearMonth = site.articles | sort: 'date' | reverse | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h3>{{ yearMonth.name }}</h3>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %} -->