---
layout: default
title: Data Science Glossar
permalink: /de/wiki/
---
# Data Science Glossar

Hier findest du Erklärungen zu wichtigen Metriken und Konzepten:

<ul>
  {% assign wiki_de = site.wiki | where: "lang", "de" %}
  {% for item in wiki_de %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
  {% endfor %}
</ul>
