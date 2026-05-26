---
layout: page
title: Organizers
permalink: /organizers/
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

---

### Contact

For any questions regarding the workshop, please reach out to the organizers at the email addresses listed above or contact us via the [CoRL 2026 workshop page](https://www.corl.org/program/workshops).

<style>
.organizers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}
.organizer-card {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1.2rem;
  border: 1px solid var(--global-divider-color, #e0e0e0);
  border-radius: 8px;
  background: var(--global-bg-color, #fff);
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}
.organizer-photo img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
}
.organizer-placeholder {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: #5b7fa6;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  font-weight: bold;
  flex-shrink: 0;
}
.organizer-info h3 { margin: 0 0 0.2rem; font-size: 1rem; }
.organizer-affiliation { margin: 0 0 0.2rem; font-size: 0.85rem; color: var(--global-text-color-light, #666); }
.organizer-email { margin: 0 0 0.4rem; font-size: 0.8rem; }
.organizer-bio { margin: 0.4rem 0 0; font-size: 0.82rem; line-height: 1.5; }
</style>
