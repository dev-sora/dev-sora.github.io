---
layout: default
title: Publications
---

{% assign pubs = site.publications | sort: "year" | reverse %}

## Journal

{% for pub in pubs %}
  {% if pub.type == "journal" %}
- {{ pub.authors | join: ", " }}  
  **"{{ pub.title }}"**  
  {{ pub.container }}, {{ pub.year }}{% if pub.note %} ({{ pub.note }}){% endif %}.  
  {% if pub.url %}[{{ pub.url }}]{% endif %}
  {% endif %}
{% endfor %}

---

## Conference

{% for pub in pubs %}
  {% if pub.type == "conference" %}
- {{ pub.authors | join: ", " }}  
  **"{{ pub.title }}"**  
  {{ pub.container }}, {{ pub.year }}.
  {% endif %}
{% endfor %}

---

## Domestic Conference / Workshop

{% for pub in pubs %}
  {% if pub.type == "domestic" %}
- {{ pub.authors | join: ", " }}  
  **"{{ pub.title }}"**  
  {{ pub.container }}, {{ pub.year }}.
  {% endif %}
{% endfor %}

---

## Article

{% for pub in pubs %}
  {% if pub.type == "article" %}
- {{ pub.authors | join: ", " }}  
  **"{{ pub.title }}"**  
  {{ pub.container }}, {{ pub.year }}.
  {% endif %}
{% endfor %}
