---
layout: about
title: Home
permalink: /
subtitle: Half-day workshop organized in conjunction with CoRL 2026
nav: true
nav_order: 1


announcements:
  enabled: false
latest_posts:
  enabled: false
social: false
selected_papers: false
---

<style>
  .post-header { text-align: center; }
  .post-header .post-title { text-align: center; }
  .post-header .desc { text-align: center; font-size: 1.1rem; margin-top: 0.5rem; }

  /* Body content: left-aligned prose, with section headings centered. */
  .post > article { text-align: left; }
  .post > article > h3 {
    text-align: center;
    margin-top: 2.2rem;
    margin-bottom: 1.2rem;
    font-size: 1.35rem;
  }
  .post > article p { line-height: 1.7; margin: 0.9rem 0; }

  .hero-figure {
    width: 100%;
    aspect-ratio: 16 / 6;
    border: 1px dashed var(--global-divider-color, #d0d0d0);
    border-radius: 8px;
    background: var(--global-code-bg-color, #f6f6f6);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--global-text-color-light, #888);
    font-size: 0.95rem;
    margin: 1rem 0 2rem;
  }

  .announcements {
    margin: 1rem 0 2rem;
    border-left: 3px solid var(--global-divider-color, #e0e0e0);
    padding-left: 1rem;
  }
  .announcements .item { display: flex; gap: 0.8rem; padding: 0.5rem 0; }
  .announcements .item .date {
    flex: 0 0 7rem;
    font-size: 0.85rem;
    color: var(--global-text-color-light, #666);
    font-variant-numeric: tabular-nums;
  }
  .announcements .item .body { font-size: 0.95rem; line-height: 1.5; }

  .key-dates {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0 2rem;
    text-align: center;
  }
  .key-dates .date-card {
    padding: 1rem;
    border: 1px solid var(--global-divider-color, #e0e0e0);
    border-radius: 8px;
  }
  .key-dates .date-label { font-size: 0.85rem; color: var(--global-text-color-light, #666); text-transform: uppercase; letter-spacing: 0.05em; }
  .key-dates .date-value { font-weight: 600; margin-top: 0.4rem; font-size: 1rem; }

  .home-organizers {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 1.25rem;
    margin: 1.5rem 0 2rem;
    text-align: center;
  }
  .home-organizers .org-card { display: flex; flex-direction: column; align-items: center; }
  .home-organizers .org-photo,
  .home-organizers .org-placeholder {
    width: 90px; height: 90px; border-radius: 50%; object-fit: cover; margin-bottom: 0.6rem;
  }
  .home-organizers .org-placeholder {
    background: #5b7fa6; color: #fff; display: flex; align-items: center; justify-content: center;
    font-weight: 600; font-size: 1.1rem;
  }
  .home-organizers .org-name { font-weight: 600; font-size: 0.95rem; line-height: 1.3; }
  .home-organizers .org-aff { font-size: 0.78rem; color: var(--global-text-color-light, #666); margin-top: 0.25rem; line-height: 1.4; }
</style>

### Announcements

<div class="announcements">
  <div class="item">
    <div class="date">TBA</div>
    <div class="body">Call for papers will open soon &mdash; check back for submission instructions.</div>
  </div>
  <div class="item">
    <div class="date">TBA</div>
    <div class="body">Invited speakers and program details to be announced.</div>
  </div>
</div>

---

### Aims and Scope

The 1st Workshop on **Compositionality for Robot Intelligence** at **CoRL 2026** examines how robots can compose reusable parts &mdash; skills, representations, policies &mdash; into behavior that generalizes to genuinely novel situations.

Current robot-learning systems scale data and model size to recover representations that recombine within the training distribution, but they struggle with **compositional generalization** in the stronger sense of qualitative extrapolation. The open question is less *whether* deep networks compose and more **what they compose over**.

The workshop convenes researchers from robot learning, evaluation, and neighbouring disciplines (language, cognitive science, biology) to discuss what designed structure is needed to close this gap, and how to measure when it has been achieved. The half-day program features invited spotlight talks, lightning talks from accepted papers, a poster session, and an **Oxford-style debate** on a central open question.

---

### Topics

The workshop is organized around two threads:

**Thread 1 &mdash; Building compositional generalization**

- Where compositional structure comes from: world, task, information processing, or behavior
- Components and interfaces: latents, states, language, skills, policies, hierarchies
- Modular, hierarchical, and foundation-model-based architectures
- Task and motion planning as a compositional substrate
- Sim-to-real as a probe for structural reuse

**Thread 2 &mdash; Evaluating compositional generalization**

- What makes a situation novel rather than an interpolation of training data
- Formal measures of compositionality in learned systems
- Benchmark design for compositional generalization
- Diagnostics for failure modes of composition
- Insights from compositional semantics, cognitive science, and biology

---

### Key Dates

<div class="key-dates">
  <div class="date-card">
    <div class="date-label">Submission deadline</div>
    <div class="date-value">TBA</div>
  </div>
  <div class="date-card">
    <div class="date-label">Author notification</div>
    <div class="date-value">TBA</div>
  </div>
  <div class="date-card">
    <div class="date-label">Camera-ready</div>
    <div class="date-value">TBA</div>
  </div>
  <div class="date-card">
    <div class="date-label">Workshop date</div>
    <div class="date-value">TBA</div>
  </div>
</div>

---

### Organizers

<div class="home-organizers">
{% for organizer in site.data.organizers %}
  <div class="org-card">
    {% if organizer.photo and organizer.photo != "" %}
      <img class="org-photo" src="{{ organizer.photo | prepend: '/assets/img/organizers/' | relative_url }}" alt="{{ organizer.name }}" />
    {% else %}
      {% assign parts = organizer.name | split: ' ' %}
      <div class="org-placeholder">{{ parts[0] | slice: 0 }}{{ parts.last | slice: 0 }}</div>
    {% endif %}
    <div class="org-name">
      {% if organizer.website and organizer.website != "" %}
        <a href="{{ organizer.website }}" target="_blank">{{ organizer.name }}</a>
      {% else %}
        {{ organizer.name }}
      {% endif %}
    </div>
    <div class="org-aff">{{ organizer.affiliation }}</div>
  </div>
{% endfor %}
</div>

See the [Organizers](/corl2026-compositionality/organizers/) page for full bios and contact information.
