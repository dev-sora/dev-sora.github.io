---
layout: default
title: Home
---

## Sorachi Kato
Ph.D. Candidate in Graduate School of Information Science and Technology, the University of Osaka, Japan.

---

## Research Overview

---

## Research Interests

---

## Selected Publications

{% assign pubs = site.publications | sort: "year" | reverse %}
{% for pub in pubs limit:3 %}
- **[{{ pub.title }}]({{ pub.url }})**, {{ pub.container }}, {{ pub.year }}.
{% endfor %}

[View all publications →](/publications/)


