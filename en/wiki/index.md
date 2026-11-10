
---
layout: default
title: Data Science Glossary
permalink: /en/wiki/
---
# Data Science Glossary

Explore definitions and concepts used in my machine learning projects:

<ul>
  {% assign wiki_en = site.wiki | where: "lang", "en" %}
  {% for item in wiki_en %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
  {% endfor %}
</ul>
