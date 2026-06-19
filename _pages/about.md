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

<section class="workshop-hero ws-reveal" aria-labelledby="workshop-title">
  <div class="ws-hero-copy">
    <div class="workshop-kicker">CoRL 2026 · HALF-DAY WORKSHOP</div>
    <h1 id="workshop-title">Compositionality for Robot Intelligence</h1>
    <p>How robots can compose reusable skills, representations, and policies into behavior that generalizes beyond training.</p>
    <div class="ws-cta-row">
      <a class="ws-btn ws-btn-primary" href="{{ '/call-for-papers/' | relative_url }}">Call for Papers</a>
      <a class="ws-btn ws-btn-ghost" href="{{ '/speakers/' | relative_url }}">Speakers</a>
    </div>
  </div>

  <div class="ws-hero-visual" aria-hidden="true">
    <div class="ws-hero-motif">
    <svg viewBox="0 0 320 320" role="img" xmlns="http://www.w3.org/2000/svg">
      <!-- outer frame: the "whole" -->
      <rect x="8" y="8" width="304" height="304" rx="22" ry="22"
            fill="none" stroke="#e6e9ef" stroke-width="1.5"/>

      <!-- compositional modules tiling the frame -->
      <rect x="28" y="28" width="120" height="84" rx="14" ry="14"
            fill="#e8590c" fill-opacity="0.92"/>
      <rect x="28" y="124" width="56" height="56" rx="12" ry="12"
            fill="none" stroke="rgba(232,89,12,0.24)" stroke-width="1.5"/>
      <rect x="92" y="124" width="56" height="56" rx="12" ry="12"
            fill="rgba(232,89,12,0.08)" stroke="rgba(232,89,12,0.24)" stroke-width="1.5"/>
      <rect x="28" y="192" width="120" height="100" rx="14" ry="14"
            fill="none" stroke="#e6e9ef" stroke-width="1.5"/>

      <rect x="160" y="28" width="132" height="56" rx="12" ry="12"
            fill="none" stroke="#e6e9ef" stroke-width="1.5"/>
      <rect x="160" y="96" width="62" height="84" rx="14" ry="14"
            fill="rgba(232,89,12,0.08)" stroke="rgba(232,89,12,0.24)" stroke-width="1.5"/>
      <rect x="230" y="96" width="62" height="84" rx="14" ry="14"
            fill="none" stroke="rgba(232,89,12,0.24)" stroke-width="1.5"/>
      <rect x="160" y="192" width="62" height="100" rx="14" ry="14"
            fill="none" stroke="#e6e9ef" stroke-width="1.5"/>
      <rect x="230" y="192" width="62" height="44" rx="12" ry="12"
            fill="#e8590c" fill-opacity="0.92"/>
      <rect x="230" y="248" width="62" height="44" rx="12" ry="12"
            fill="none" stroke="#e6e9ef" stroke-width="1.5"/>
    </svg>
    </div>
    <span class="ws-hero-tag">
      <img src="{{ '/assets/img/organizers/corl_2026_logo.png' | relative_url }}" alt="" />
      CoRL 2026
    </span>
  </div>
</section>

<div class="intro-grid ws-reveal">
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

<div class="topic-grid ws-reveal">
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

<div class="home-speakers ws-reveal">
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

<div class="key-dates ws-reveal">
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

<div class="home-organizers ws-reveal">
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

<div class="workshop-content-card ws-coc-card">
  <p markdown="span">We are committed to a respectful, inclusive, and constructive workshop environment for all participants. You can **confidentially** contact [Eduardo Sebastian](mailto:es2121@cam.ac.uk) for any concerns during the workshop.</p>
</div>
