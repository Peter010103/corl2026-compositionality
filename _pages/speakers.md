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
