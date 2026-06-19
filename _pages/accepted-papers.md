---
layout: page
title: Accepted Papers
permalink: /accepted-papers/
nav: true
nav_order: 6
---

{% if site.data.accepted_papers %}

<div class="papers-list">

{% for paper in site.data.accepted_papers %}

<div class="paper-card">
  <h3 class="paper-title">{{ paper.title }}</h3>
  <p class="paper-authors">{{ paper.authors }}</p>
  {% if paper.abstract %}
    <details>
      <summary>Abstract</summary>
      <p class="paper-abstract">{{ paper.abstract }}</p>
    </details>
  {% endif %}
  <div class="paper-links">
    {% if paper.pdf %}<a href="{{ paper.pdf }}" target="_blank" class="paper-link">PDF</a>{% endif %}
    {% if paper.arxiv %}<a href="{{ paper.arxiv }}" target="_blank" class="paper-link">arXiv</a>{% endif %}
    {% if paper.poster %}<a href="{{ paper.poster }}" target="_blank" class="paper-link">Poster</a>{% endif %}
  </div>
</div>
{% endfor %}

</div>

{% else %}

<div class="ws-empty-state">
  <div class="ws-empty-icon" aria-hidden="true">
    <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" width="56" height="56">
      <rect x="14" y="10" width="36" height="48" rx="6" fill="none" stroke="#e6e9ef" stroke-width="2"/>
      <rect x="22" y="22" width="20" height="3" rx="1.5" fill="rgba(232,89,12,0.08)"/>
      <rect x="22" y="30" width="20" height="3" rx="1.5" fill="rgba(232,89,12,0.08)"/>
      <rect x="22" y="38" width="14" height="3" rx="1.5" fill="rgba(232,89,12,0.08)"/>
    </svg>
  </div>
  <h3>Accepted papers coming soon</h3>
  <p>Paper decisions will be announced after the review process. Check back soon, or visit the <a href="{{ '/call-for-papers/' | relative_url }}">Call for Papers</a> page for submission details.</p>
</div>

{% endif %}
