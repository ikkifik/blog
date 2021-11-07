---
layout: default
title: Catatan
---

# 📑️ Catatan

Hey kamu menemukannya!  
Halaman yang isinya tulisan random, gak jelas, suka-suka yang nulis aja.

{% assign postsByYearMonth = site.notes | sort: 'date' | reverse | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h3>{{ yearMonth.name }}</h3>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

