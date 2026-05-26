---
layout: about
title: home
permalink: /
nav_order: 1

profile:
  align: right
  image: corl_logo.png
  image_circular: false

announcements:
  enabled: false
latest_posts:
  enabled: false
social: false
selected_papers: false
---

## 1st Workshop on Compositionality for Robot Intelligence

**CoRL 2026 &mdash; Half-day Workshop**

---

Compositionality is the capacity of intelligent systems to produce novel, generalizable behavior by recombining known parts. Although it is widely held to be a desirable property for robots, the underlying mechanisms of compositionality remain poorly understood.

The dominant trend in robot learning has been to pursue generalization by scaling data and model size, arguably resulting in models that are compositional: they recover lower-dimensional representations that reproduce the training distribution through structured combination. However, these models struggle with **compositional generalization** in the stronger sense of qualitative extrapolation to genuinely novel situations.

Therefore, the question is less about whether deep networks compose and more about **what they compose over**. This workshop examines compositionality under the premise that closing this gap calls for deliberate, designed structure, and convenes researchers to ask what such structure is.

Specifically, we explore *Compositionality for Robot Intelligence*: robot capabilities that arise from structured combinations of reusable parts&mdash;skills, representations, policies&mdash;such that behavior in novel settings emerges from, and can be explained by, the components and their interaction structure.

---

### Overarching Questions

The overarching question we want to open for discussion is: **how do we build and evaluate compositional generalization in robot behavior?** We propose to organize the conversation around two threads:

**Thread 1: How do we build compositional generalization into a system?**
- Where does compositional structure come from? The world, the task, the information processing, or the observed behavior?
- Given an answer to the above: what are the right components, interfaces, and interaction structure? Latents? States? Language? Are hierarchies needed to achieve composition?

**Thread 2: How do we evaluate compositional generalization?**
- What makes a situation truly novel rather than just an interpolation of the training data?
- Given a notion of novelty, what is a valid measure of compositionality?

---

### Target Audience

The workshop is aimed at researchers spanning three overlapping communities:

1. **Robot-learning researchers** building systems designed to recombine skills, representations, or policies in new settings — including work on policy learning, hierarchical and modular architectures, task and motion planning, and foundation-model-based systems.
2. **Benchmark and evaluation researchers** focused on defining compositional generalization in practice: benchmark design, sim-to-real as a generalization probe, and formal approaches to characterising structure and novelty.
3. **Researchers from neighbouring disciplines** whose primary object of study is compositional structure itself — compositional semantics in language, structured and hierarchical representations in cognitive science and neuroscience, and modular reuse in biological systems.

---

### Format

The workshop is a **half-day** event featuring invited spotlight talks, lightning talks from accepted paper contributors, a poster session, and an **Oxford-style debate** on a central open question in compositional robot intelligence.

See the [Program](/corl2026-compositionality/program/) page for the full schedule.
