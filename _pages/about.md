---
layout: about
title: home
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
  .post > article { text-align: center; }
  .post > article h1,
  .post > article h2,
  .post > article h3,
  .post > article h4 { text-align: center; }
  .post > article ul,
  .post > article ol { display: inline-block; text-align: left; }
  .post > article p,
  .post > article > h3 { margin-top: 1.6rem; margin-bottom: 1.2rem; line-height: 1.7; }

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

<div class="hero-figure">Figure placeholder</div>

### Aims and Scope

The 1st Workshop on **Compositionality for Robot Intelligence** (CRI), to be held within the **Conference on Robot Learning (CoRL) 2026**, is the first CoRL workshop devoted to the structures, mechanisms, and evaluations that let robots compose reusable parts into novel, generalizable behavior.

In recent years, we have witnessed the rapid scaling of data and model size in robot learning, producing systems that are arguably compositional in a weak sense: they recover lower-dimensional representations that reproduce the training distribution through structured combination. Yet these systems still struggle with **compositional generalization** in the stronger sense of qualitative extrapolation to genuinely novel situations. The question, therefore, is less about whether deep networks compose and more about **what they compose over**.

This workshop examines compositionality under the premise that closing this gap calls for deliberate, designed structure. We explore _Compositionality for Robot Intelligence_: robot capabilities that arise from structured combinations of reusable parts&mdash;skills, representations, policies&mdash;such that behavior in novel settings emerges from, and can be explained by, the components and their interaction structure.

The aim of the workshop is to provide researchers from robot learning, evaluation, and neighbouring disciplines a place to share experiences, surface open problems, and contribute to the discussion about how to build and measure compositional generalization in robot behavior.

Researchers willing to participate should submit a contribution through the workshop submission page. Accepted papers will be presented as lightning talks and posters.

---

### Topics

The workshop is organized around two main threads:

**Thread 1 &mdash; Building compositional generalization into a system**

- Sources of compositional structure: world, task, information processing, or behavior
- Components and interfaces: latents, states, language, skills, policies
- Hierarchical and modular architectures for robot learning
- Task and motion planning as a compositional substrate
- Foundation-model-based systems and prompted recomposition
- Sim-to-real as a probe for structural reuse

**Thread 2 &mdash; Evaluating compositional generalization**

- Defining novelty beyond interpolation of the training distribution
- Formal measures of compositionality in learned systems
- Benchmark design for compositional generalization
- Empirical methodologies for diagnosing failure modes of composition
- Insights from compositional semantics in language, cognitive science, and biology

---

### Format

The workshop is a **half-day** event featuring invited spotlight talks, lightning talks from accepted paper contributors, a poster session, and an **Oxford-style debate** on a central open question in compositional robot intelligence.

See the [Program](/corl2026-compositionality/program/) page for the full schedule and the [Call for Papers](/corl2026-compositionality/call-for-papers/) page for submission details.

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
