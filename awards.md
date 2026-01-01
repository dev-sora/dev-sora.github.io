---
layout: default
title: Awards
---

# 🎉Awards

<section class="content-section" markdown="1">
{% assign awds = site.awds | sort: "year" | reverse %}

{% for awd in awds %}

- **{{ awd.title }},** {{ awd.year }}{% if awd.note %}({{ awd.note }}){% endif %}.
  {% if awd.link %}<a href="{{ awd.link }}">[Link]</a>{% endif %}

{% endfor %}

</section>
