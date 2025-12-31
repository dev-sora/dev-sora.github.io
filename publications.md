---
layout: default
title: Publications
---

{% assign pubs = site.publications | sort: "year" | reverse %}

<ul>
  {% for pub in pubs %}
    <li>
      <a href="{{ pub.url }}">{{ pub.title }}</a>
      <br />
      <small>
        {{ pub.authors | join: ", " }} —
        {{ pub.venue }} ({{ pub.year }})
      </small>
    </li>
  {% endfor %}
</ul>
