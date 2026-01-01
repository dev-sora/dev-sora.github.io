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
My research explores wireless sensing and deep neural signal processing, with the goal of transforming commodity radio signals into scalable, privacy-preserving perception systems. I study how Wi-Fi and mmWave radar measurements—originally designed for communication—can be repurposed to infer human states and environments by integrating classical signal processing with modern deep learning. A central focus of my work is improving the accessibility and usability of wireless sensing data, including learning-based modeling of standardized Wi-Fi beamforming reports and structured perception from mmWave radar signals. By embedding physical signal structure and measurement constraints into learning frameworks, my research aims to bridge communication and sensing, enabling robust perception under incomplete, compressed, and noisy radio observations.
</section>

<section class="content-section" markdown="1">
## Biography
<div class="timeline">
  <ul>
    <li style="--index: 1">
      <h3>2017-2021</h3>
      <p>Bachelor (Engineering), <br> The University of Osaka</p>
    </li>
    <li style="--index: 2">
      <h3>2021-2023</h3>
      <p>Master (Information Science), <br> The University of Osaka</p>
    </li>
    <li style="--index: 3">
      <h3>2023-now</h3>
      <p>Ph.D. Candidate, <br> The University of Osaka</p>
    </li>
    <li style="--index: 4">
      <h3>2023 July - 2024 June</h3>
      <p>Visiting Student / Internship, <br> Mitsubishi Electric Research Laboratories</p>
    </li>
  </ul>
  </div>
</section>

<section class="content-section" markdown="1">
## Recent Publications

{% assign pubs = site.pubs | sort: "year" | reverse %}
{% for pub in pubs limit:3 %}

- **[{{ pub.title }}]({{ pub.url }})**, {{ pub.container }}, {{ pub.year }}.
  {% endfor %}

[View all publications →](/publications.html)

</section>
