---
layout: page
title: Speakers
permalink: /speakers/
nav: true
nav_order: 2
---

<div class="speakers-grid">

{% assign speakers = site.data.speakers %}
{% for speaker in speakers %}

<div class="speaker-card">
  <div class="speaker-photo">
    {% if speaker.photo %}
      <img src="{{ speaker.photo | prepend: '/assets/img/speakers/' | relative_url }}" alt="{{ speaker.name }}" />
    {% else %}
      <div class="speaker-placeholder">{{ speaker.name | split: ' ' | map: 'first' | join: '' | truncate: 2, '' }}</div>
    {% endif %}
  </div>
  <div class="speaker-info">
    <h3>
      {% if speaker.website %}
        <a href="{{ speaker.website }}" target="_blank">{{ speaker.name }}</a>
      {% else %}
        {{ speaker.name }}
      {% endif %}
    </h3>
    <p class="speaker-affiliation">{{ speaker.affiliation }}</p>
    {% if speaker.talk_title %}
      <p class="speaker-talk"><em>{{ speaker.talk_title }}</em></p>
    {% endif %}
    {% if speaker.topics %}
      <p class="speaker-topics">
        {% for topic in speaker.topics %}
          <span class="topic-tag">{{ topic }}</span>
        {% endfor %}
      </p>
    {% endif %}
    {% if speaker.confirmed == false %}
      <span class="status-badge tentative">Tentative</span>
    {% else %}
      <span class="status-badge confirmed">Confirmed</span>
    {% endif %}
  </div>
</div>
{% endfor %}

</div>

<style>
.speakers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}
.speaker-card {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1.2rem;
  border: 1px solid var(--global-divider-color, #e0e0e0);
  border-radius: 8px;
  background: var(--global-bg-color, #fff);
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}
.speaker-photo img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
}
.speaker-placeholder {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: #7b68ee;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  font-weight: bold;
}
.speaker-info h3 { margin: 0 0 0.2rem; font-size: 1rem; }
.speaker-affiliation { margin: 0 0 0.3rem; font-size: 0.85rem; color: var(--global-text-color-light, #666); }
.speaker-talk { margin: 0 0 0.4rem; font-size: 0.85rem; }
.topic-tag {
  display: inline-block;
  background: #f0f0f0;
  border-radius: 4px;
  padding: 0.1rem 0.4rem;
  font-size: 0.75rem;
  margin: 0.1rem 0.1rem 0.1rem 0;
}
.status-badge {
  display: inline-block;
  padding: 0.15rem 0.5rem;
  border-radius: 4px;
  font-size: 0.72rem;
  font-weight: 600;
  text-transform: uppercase;
}
.status-badge.confirmed { background: #e6f4ea; color: #2d7a2d; }
.status-badge.tentative { background: #fff8e1; color: #8a6400; }
</style>
