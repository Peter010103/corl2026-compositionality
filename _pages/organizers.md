---
layout: page
title: Organizers
permalink: /organizers/
nav: false
nav_order: 4
---

<div class="organizers-grid">

{% for organizer in site.data.organizers %}

<div class="organizer-card">
  <div class="organizer-photo">
    {% if organizer.photo %}
      <img src="{{ organizer.photo | prepend: '/assets/img/organizers/' | relative_url }}" alt="{{ organizer.name }}" />
    {% else %}
      <div class="organizer-placeholder">{{ organizer.name | split: ' ' | map: 'first' | join: '' | truncate: 2, '' }}</div>
    {% endif %}
  </div>
  <div class="organizer-info">
    <h3>
      {% if organizer.website %}
        <a href="{{ organizer.website }}" target="_blank">{{ organizer.name }}</a>
      {% else %}
        {{ organizer.name }}
      {% endif %}
    </h3>
    <p class="organizer-affiliation">{{ organizer.affiliation }}</p>
    {% if organizer.email %}
      <p class="organizer-email"><a href="mailto:{{ organizer.email }}">{{ organizer.email }}</a></p>
    {% endif %}
    {% if organizer.bio %}
      <p class="organizer-bio">{{ organizer.bio }}</p>
    {% endif %}
  </div>
</div>
{% endfor %}

</div>

### Contact

For any questions regarding the workshop, please reach out to [es2121@cam.ac.uk](mailto:es2121@cam.ac.uk).
