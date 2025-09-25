---
layout: default
title: Retros by Author
---

# Retros by Author

{% assign retros_by_author = site.retros | group_by: 'author' | sort: 'name' %}

{% for author_group in retros_by_author %}
## {{ author_group.name }}

{% assign sorted_retros = author_group.items | sort: 'date' | reverse %}
{% for retro in sorted_retros %}
- [{{ retro.title }}]({{ retro.url }}) - {{ retro.date | date: "%-d/%m/%Y" }}
{% endfor %}

{% endfor %}