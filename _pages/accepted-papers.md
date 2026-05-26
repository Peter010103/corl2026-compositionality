---
layout: page
title: Accepted Papers
permalink: /accepted-papers/
nav_order: 6
---

Accepted papers will be listed here after the review process is complete.

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

<div class="coming-soon-box">
  <p>&#128203; Paper decisions will be announced after the review process. Check back soon!</p>
</div>

{% endif %}

<style>
.coming-soon-box {
  text-align: center;
  padding: 3rem 2rem;
  border: 2px dashed #ccc;
  border-radius: 8px;
  color: #888;
  font-size: 1.1rem;
  margin-top: 2rem;
}
.papers-list { margin-top: 2rem; }
.paper-card {
  padding: 1.2rem 1.4rem;
  border: 1px solid var(--global-divider-color, #e0e0e0);
  border-radius: 8px;
  margin-bottom: 1.2rem;
  background: var(--global-bg-color, #fff);
}
.paper-title { margin: 0 0 0.3rem; font-size: 1rem; }
.paper-authors { margin: 0 0 0.5rem; font-size: 0.85rem; color: var(--global-text-color-light, #555); }
.paper-abstract { font-size: 0.85rem; margin-top: 0.5rem; }
.paper-links { margin-top: 0.6rem; }
.paper-link {
  display: inline-block;
  margin-right: 0.5rem;
  padding: 0.2rem 0.6rem;
  border: 1px solid #7b68ee;
  border-radius: 4px;
  font-size: 0.78rem;
  color: #7b68ee;
  text-decoration: none;
}
.paper-link:hover { background: #7b68ee; color: white; }
details summary { cursor: pointer; font-size: 0.85rem; color: #555; }
</style>
