---
layout: default
title: "Data Science Wiki"
lang: de
permalink: /de/wiki/
---

# Data Science Wiki & Glossar

Hier findest du alle Artikel:

{% for post in site.wiki %}
  {% if post.lang == "de" %}
  * [{{ post.title }}]({{ post.url }})
  {% endif %}
{% endfor %}
