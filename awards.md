---
layout: default
title: Awards
---

## Awards

{% assign awds = site.awards | sort: "year" | reverse %}

{% for awd in awds %}

- **{{ awd.title }},** {{ awd.year }}{% if awd.note %}({{ awd.note }}){% endif %}.
  {% if awd.link %}<a href="{{ awd.link }}">[Link]</a>{% endif %}

{% endfor %}
