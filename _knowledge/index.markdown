---
layout: page
title: "Все статьи базы знаний"
permalink: /knowledge/статьи/
---

# 📚 Все статьи базы знаний

{% for article in site.knowledge %}
{% if article.path contains 'статьи' and article.name != 'index.md' %}
## [{{ article.title }}]({{ article.url }})
*{{ article.date | date: "%d.%m.%Y" }}* | 
Категории: {{ article.categories | join: ", " }}

{% endif %}
{% endfor %}
