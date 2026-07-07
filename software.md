---
layout: default
title: Software / Datasets
---

# 🛠️Software / Datasets

<section class="content-section" markdown="1">

{% assign sws = site.soft %}

<ul>
{% for sw in sws %}
  <li>
    <strong>{{ sw.title }}</strong>
    {% if sw.links.code %} — <a href="{{ sw.links.code }}">[Code]</a>{% endif %}
    {% if sw.links.dataset %} — <a href="{{ sw.links.dataset }}">[Dataset]</a>{% endif %}
    {% if sw.links.paper %} — <a href="{{ sw.links.paper }}">[Paper]</a>{% endif %}
  </li>
{% endfor %}
</ul>
</section>
