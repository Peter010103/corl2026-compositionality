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
    {% if speaker.bio %}
      <p class="speaker-bio">{{ speaker.bio }}</p>
    {% endif %}
    {% if speaker.confirmed == false %}
      <span class="status-badge tentative">Tentative</span>
    {% endif %}
  </div>
</div>
{% endfor %}

</div>

<style>
.speakers-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.15rem;
  margin-top: 2.25rem;
}
.speaker-card {
  display: grid;
  grid-template-columns: 112px minmax(0, 1fr);
  align-items: flex-start;
  gap: 1.15rem;
  min-height: 100%;
  padding: 1.45rem;
  border: 0;
  border-radius: 14px;
  background: rgba(255, 255, 255, 0.84);
  box-shadow: 0 14px 36px rgba(104, 54, 20, 0.07);
}
.speaker-photo img {
  width: 112px;
  height: 112px;
  border-radius: 50%;
  object-fit: cover;
}
.speaker-placeholder {
  width: 112px;
  height: 112px;
  border-radius: 50%;
  background: #e8590c;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  font-weight: bold;
}
.speaker-info h3 { margin: 0 0 0.25rem; font-size: 1.2rem; line-height: 1.1; color: #a8430a; }
.speaker-info h3 a { color: #a8430a; }
.speaker-affiliation {
  margin: 0 0 0.65rem;
  font-size: 0.83rem;
  color: var(--global-text-color-light, #666);
  line-height: 1.35;
}
.speaker-talk {
  margin: 0 0 0.85rem;
  font-size: 0.9rem;
  line-height: 1.45;
}
.speaker-bio {
  margin: 0;
  color: var(--global-text-color-light, #555);
  font-size: 0.9rem;
  line-height: 1.62;
}
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
@media (max-width: 900px) {
  .speakers-grid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .speaker-card {
    grid-template-columns: 1fr;
    padding: 1.25rem;
  }
}
</style>
