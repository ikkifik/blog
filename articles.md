---
layout: default
title: Artikel
---

# 💡️ Artikel

Halaman untuk sharing ilmu. Gunakan <mark>Ctrl+F</mark> untuk mencari judul materi.  
{% assign items_grouped = site.articles | group_by_exp: "post", "post.tags" %}
Daftar topik yang tersedia: {% for tag in items_grouped %} <mark><a href="#{{ tag.name }}">#{{ tag.name }}({{ tag.size }})</a></mark> {% endfor %}
<hr>

<!-- Group by post categories -->
{% assign postsByCategories = site.articles | sort | group_by_exp: "post", "post.categories"  %}
{% for categories in postsByCategories %}
  <h3 id="{{ categories.name }}"><a href="#{{ categories.name }}">#</a> {{ categories.name }}</h3>
  <ul>
    {% for post in categories.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %} 
  </ul>
{% endfor %}

<br>
<hr>