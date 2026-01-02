---
layout: default
title: Home
---

<div class="profile">
  <img
    src="{{ '/assets/images/profile.jpg' | relative_url }}"
    alt="Profile photo"
    class="profile-img"
  />

  <div class="profile-text">
    <h1>Sorachi Kato (加藤 空知)</h1>

    <p>
      Ph.D. Candidate, the University of Osaka, Japan<br />
      Wireless sensing (IEEE 802.11 / mmWave radar), Signal Processing, Deep Learning<br />

        <div class="profile-links">
          {% assign profile_links =
            "GitHub|https://github.com/dev-sora|github.svg,
             LinkedIn|https://www.linkedin.com/in/sorachi-kato-a90138227|linkedin.png,
             ORCID|https://orcid.org/0000-0002-6896-5293|orcid.svg,
             Scholar|https://scholar.google.com/citations?user=C537Uf4AAAAJ|google_scholar.svg,
             Email|mailto:kato.sorachi@ist.osaka-u.ac.jp|mail.svg"
             | split: "," %}

        {% for item in profile_links %}
        {% assign parts = item | split: "|" %}
        <a href="{{ parts[1] }}" target="_blank" rel="noopener">
        <img
                src="{{ '/assets/icons/' | append: parts[2] | relative_url }}"
                alt="{{ parts[0] }}"
                title="{{ parts[0] }}"
              />
        </a>
        {% endfor %}
        </div>
    </p>

  </div>
</div>

<section class="content-section" markdown="1">
## Research Overview

My research primarily focuses on **wireless sensing**, which aims to predict
motions and status of human subjects and environments.
Wireless sensing has attracted significant attention as a promising alternative to conventional sensing modalities such as cameras and wearable sensors, due to its non-intrusive nature, reduced privacy concerns, and wide-area coverage.

I mainly work on two types of approaches: communication-based sensing using wireless signals such as Wi-Fi and BLE, and radar-based sensing methods built on mmWave signal processing.
With the ultimate goal of eliminating unobservable spaces in the physical world, I develop advanced wireless sensing methods, primarily leveraging deep learning techniques.

Beyond wireless sensing, I am also interested in related topics including **multimedia transmission**, **signal compression**, and **3D reconstruction**.

</section>

<section class="content-section" markdown="1">
## Biography
<div id="timeline-container">
  <div class="inner-container">
    <ul class="timeline">
      <li class="timeline-item" data-date="2017-2021">Bachelor Deg. (Engineer), the University of Osaka, Japan</li>
      <li class="timeline-item" data-date="2021-2023">Master Deg. (Information Science), the University of Osaka, Japan</li>
      <li class="timeline-item" data-date="2021.07-2021.08">NTT, Inc., Summer Internship, Japan</li>
      <li class="timeline-item" data-date="2023-now">Ph.D. candidate, the University of Osaka, Japan</li>
      <li class="timeline-item" data-date="2023.07-2024.06">Mitsubishi Electric Research Laboratories, Visiting student / Internship, USA</li>
    </ul>
  </div>
</div>
</section>
<script src="{{ '/assets/js/biography-timeline.js' | relative_url }}"></script>

<section class="content-section" markdown="1">
## Recent Publications

{% assign pubs = site.pubs | sort: "year" | reverse %}
{% for pub in pubs limit:3 %}

- **{{ pub.title }}**, {{ pub.container }}, {{ pub.year }}.
  {% endfor %}

[View all publications →](/publications.html)

</section>
