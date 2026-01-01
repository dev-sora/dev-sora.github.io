---
layout: default
title: Publications
---

{% assign my_names = "Sorachi Kato|加藤 空知" | split: "|" %}
{% assign journal_pubs = site.pubs | where: "type", "journal" | sort: "sortkey" | reverse %}
{% assign conf_pubs = site.pubs | where: "type", "conference" | sort: "sortkey" | reverse %}
{% assign domes_pubs = site.pubs | where: "type", "domestic" | sort: "sortkey" | reverse %}
{% assign article_pubs = site.pubs | where: "type", "article" | sort: "sortkey" | reverse %}

# Publications

<section class="content-section" markdown="1">
## 📕Journal

<ul>
{% for pub in journal_pubs %}
  <li>
    {% for author in pub.authors %}
      {% if my_names contains author %}
        <strong><u>{{ author }}</u></strong>
      {% else %}
        {{ author }}
      {% endif %}
      {% unless forloop.last %}, {% endunless %}
    {% endfor %},<br>
    <strong>"{{ pub.title }}"</strong>,<br>
    <i>{{ pub.container }}</i>,
    {% if pub.vol %} Vol. {{ pub.vol }}, {% endif %}
    {% if pub.number %} No. {{ pub.number }}, {% endif %}
    {% if pub.pages %} pp. {{ pub.pages }}, {% endif %}
    {{ pub.year }}{% if pub.note %} ({{ pub.note }}){% endif %}.
    {% if pub.paper %}<a href="{{ pub.paper }}">[Paper]</a>{% endif %}{% if pub.code %}<a href="{{ pub.code }}">[Code]</a>{% endif %}{% if pub.data %}<a href="{{ pub.data }}">[Dataset]</a>{% endif %}
  </li>
{% endfor %}
</ul>
</section>

<section class="content-section" markdown="1">
## 📑Conference

<ul>
{% for pub in conf_pubs %}
  <li>
    {% for author in pub.authors %}
      {% if my_names contains author %}
        <strong><u>{{ author }}</u></strong>
      {% else %}
        {{ author }}
      {% endif %}
      {% unless forloop.last %}, {% endunless %}
    {% endfor %},<br>
    <strong>"{{ pub.title }}"</strong>,<br>
    in <i>{{ pub.container }}</i>,
    {% if pub.vol %} Vol. {{ pub.vol }}, {% endif %}
    {% if pub.number %} No. {{ pub.number }}, {% endif %}
    {% if pub.pages %} pp. {{ pub.pages }}, {% endif %}
    {{ pub.year }}{% if pub.note %} ({{ pub.note }}){% endif %}.
    {% if pub.paper %}<a href="{{ pub.paper }}">[Paper]</a>{% endif %}{% if pub.code %}<a href="{{ pub.code }}">[Code]</a>{% endif %}{% if pub.data %}<a href="{{ pub.data }}">[Dataset]</a>{% endif %}
  </li>
{% endfor %}
</ul>
</section>

<section class="content-section" markdown="1">
## 🇯🇵Domestic Conference

All papers below are presented in Japanese.

<details>
  <summary>Show Papers</summary>

  <ul>
  {% for pub in domes_pubs %}
    <li>
      {% for author in pub.authors %}
        {% if my_names contains author %}
          <strong><u>{{ author }}</u></strong>
        {% else %}
          {{ author }}
        {% endif %}
        {% unless forloop.last %}, {% endunless %}
      {% endfor %},<br>

      <strong>"{{ pub.title }}"</strong>,<br>
      <i>{{ pub.container }}</i>,
        {% if pub.vol %} Vol. {{ pub.vol }}, {% endif %}
        {% if pub.number %} No. {{ pub.number }}, {% endif %}
        {% if pub.pages %} pp. {{ pub.pages }}, {% endif %}
          {{ pub.year }}{% if pub.note %} ({{ pub.note }}){% endif %}.
      {% if pub.paper %}<a href="{{ pub.paper }}">[Paper]</a>{% endif %}
      {% if pub.code %}<a href="{{ pub.code }}">[Code]</a>{% endif %}
      {% if pub.data %}<a href="{{ pub.data }}">[Dataset]</a>{% endif %}
    </li>

{% endfor %}

  </ul>

</details>
</section>

<section class="content-section" markdown="1">
## ✍️Article

<ul>
{% for pub in article_pubs %}
  <li>
    {% for author in pub.authors %}
      {% if my_names contains author %}
        <strong><u>{{ author }}</u></strong>
      {% else %}
        {{ author }}
      {% endif %}
      {% unless forloop.last %}, {% endunless %}
    {% endfor %},<br>
    <strong>"{{ pub.title }}"</strong>,<br>
    <i>{{ pub.container }}</i>,
    {{ pub.year }}{% if pub.note %} ({{ pub.note }}){% endif %}.
    {% if pub.paper %}<a href="{{ pub.paper }}">[Paper]</a>{% endif %}{% if pub.code %}<a href="{{ pub.code }}">[Code]</a>{% endif %}{% if pub.data %}<a href="{{ pub.data }}">[Dataset]</a>{% endif %}
  </li>
{% endfor %}
</ul>
</section>
