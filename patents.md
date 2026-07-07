---
layout: default
title: Patents
---

# ⚖️Patents

<section class="content-section" markdown="1">

{% assign pats = site.patents | sort: "year" | reverse %}

<ul>
{% for pat in pats %}
  <li>
    <strong>「{{ pat.title }}」</strong>
    ({{ pat.inventors }}),
    {{ pat.number }}, {{ pat.publication }}, {{ pat.year }}.
    {% if pat.link %}<a href="{{ pat.link }}">[Link]</a>{% endif %}
  </li>
{% endfor %}
</ul>
</section>
