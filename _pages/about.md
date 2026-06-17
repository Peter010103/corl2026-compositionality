---
layout: about
title: Home
permalink: /
subtitle: Half-day workshop organized in conjunction with CoRL 2026
nav: false
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
  .home-organizers .org-name { font-weight: 400; font-size: 0.95rem; line-height: 1.3; }
  .home-organizers .org-aff { font-size: 0.78rem; color: var(--global-text-color-light, #666); margin-top: 0.25rem; line-height: 1.4; }
</style>

<section class="workshop-hero" aria-labelledby="workshop-title">
  <div>
    <div class="workshop-kicker">CoRL 2026 half-day workshop</div>
    <h1 id="workshop-title">Compositionality for Robot Intelligence</h1>
    <p>How robots can compose reusable skills, representations, and policies into behavior that generalizes beyond training.</p>
  </div>
</section>

<div class="intro-grid">
  <section class="intro-panel">
    <h3>Announcements</h3>
    <div class="announcements">
      <div class="item">
        <div class="date">TBA</div>
        <div class="body">Call for papers will open soon. Check back for submission instructions.</div>
      </div>
      <div class="item">
        <div class="date">TBA</div>
        <div class="body">Invited speakers and program details to be announced.</div>
      </div>
    </div>
  </section>

  <section class="intro-panel">
    <h3>Aims and Scope</h3>
    <div class="workshop-content-card workshop-aims-card">
      <p>The 1st Workshop on <strong>Compositionality for Robot Intelligence</strong> at <strong>CoRL 2026</strong> examines how robots can compose reusable parts: skills, representations, and policies into behavior that generalizes to genuinely novel situations.</p>

      <p>Current robot-learning systems scale data and model size to recover representations that recombine within the training distribution, but they struggle with <strong>compositional generalization</strong> in the stronger sense of qualitative extrapolation. The open question is less <em>whether</em> deep networks compose and more <strong>what they compose over</strong>.</p>

      <p>The workshop convenes researchers from robot learning, evaluation, and neighbouring disciplines (language, cognitive science, biology) to discuss what designed structure is needed to close this gap, and how to measure when it has been achieved. The half-day program features invited spotlight talks, lightning talks from accepted papers, a poster session, and an <strong>Oxford-style debate</strong> on a central open question.</p>
    </div>

  </section>
</div>

---

### Topics

<div class="topic-grid">
  <div class="workshop-content-card topic-card">
    <div class="topic-label">Thread 1</div>
    <h4>Building compositional generalization</h4>
    <ul>
      <li>Origins of compositional structure in world, task, information processing, or behavior</li>
      <li>Components and interfaces for latents, states, language, skills, policies, and hierarchies</li>
      <li>Modular, hierarchical, and foundation-model-based robot-learning architectures</li>
      <li>Task and motion planning as a compositional substrate</li>
      <li>Sim-to-real transfer as a probe for structural reuse</li>
    </ul>
  </div>

  <div class="workshop-content-card topic-card">
    <div class="topic-label">Thread 2</div>
    <h4>Evaluating compositional generalization</h4>
    <ul>
      <li>Distinguishing genuinely novel situations from interpolation of training data</li>
      <li>Formal measures of compositionality in learned systems</li>
      <li>Benchmarks for testing compositional generalization</li>
      <li>Diagnostics for failure modes of composition</li>
      <li>Perspectives from compositional semantics, cognitive science, and biology</li>
    </ul>
  </div>
</div>

---

### Invited Speakers

<div class="home-speakers">
{% for speaker in site.data.speakers %}
  <div class="home-speaker-card">
    {% if speaker.photo and speaker.photo != "" %}
      <img class="home-speaker-photo" src="{{ speaker.photo | prepend: '/assets/img/speakers/' | relative_url }}" alt="{{ speaker.name }}" />
    {% else %}
      {% assign parts = speaker.name | split: ' ' %}
      <div class="home-speaker-placeholder">{{ parts[0] | slice: 0 }}{{ parts.last | slice: 0 }}</div>
    {% endif %}
    <div class="home-speaker-name">
      {% if speaker.website and speaker.website != "" %}
        <a href="{{ speaker.website }}" target="_blank">{{ speaker.name }}</a>
      {% else %}
        {{ speaker.name }}
      {% endif %}
    </div>
    <div class="home-speaker-aff">{{ speaker.affiliation }}</div>
  </div>
{% endfor %}
</div>

<p class="home-section-link">
  Full speaker bios and talk titles are available on the <a href="{{ '/speakers/' | relative_url }}">Speakers page</a>.
</p>

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

### Code of Conduct

We are committed to a respectful, inclusive, and constructive workshop environment for all participants. You can **confidentially** contact [Eduardo Sebastian](mailto:es2121@cam.ac.uk) for any concerns during the workshop.
