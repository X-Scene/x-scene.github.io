---
layout: default
---

<div class="title-container">
  <img src="assets/images/logo.png" alt="Logo" class="logo">
  <h1>
    <span class="main-title"><span class="x-scene_1">𝒳</span><span class="x-scene_2">-</span><span class="x-scene_3">S</span><span class="x-scene_4">c</span><span class="x-scene_5">e</span><span class="x-scene_6">n</span><span class="x-scene_7">e</span>: Large-Scale Driving Scene Generation with High Fidelity and Flexible Controllability</span>
  </h1>
</div>


{% include_relative authors.md %}
{% include_relative links.md %}


## Abstract

<div class="abstract">
Diffusion models are advancing autonomous driving by enabling realistic data synthesis, predictive end-to-end planning, and closed-loop simulation, with a primary focus on temporally consistent generation. However, the generation of <span class="highlight">large-scale 3D scenes</span> that require spatial coherence remains underexplored.

In this paper, we propose <span class="highlight-x-scene_1">𝒳</span><span class="highlight-x-scene_2">-</span><span class="highlight-x-scene_3">S</span><span class="highlight-x-scene_4">c</span><span class="highlight-x-scene_5">e</span><span class="highlight-x-scene_6">n</span><span class="highlight-x-scene_7">e</span>, a novel framework for large-scale driving scene generation that achieves both geometric intricacy and appearance fidelity, while offering flexible controllability.

Specifically, 𝒳<span class="italic">-Scene</span> supports <span class="highlight">multi-granular control</span>, including low-level conditions such as user-provided or text-driven layout for detailed scene composition and high-level semantic guidance such as user-intent and LLM-enriched text prompts for efficient customization.

To enhance geometrical and visual fidelity, we introduce a unified pipeline that sequentially generates 3D semantic occupancy and the corresponding multiview images, while ensuring alignment between modalities. 

Additionally, we extend the generated local region into a large-scale scene through <span class="highlight">consistency-aware scene outpainting,</span> which extrapolates new occupancy and images conditioned on the previously generated area, enhancing spatial continuity and preserving visual coherence.

The resulting scenes are lifted into high-quality 3DGS representations, supporting diverse applications such as scene exploration.

Comprehensive experiments demonstrate that 𝒳<span class="italic">-Scene</span> significantly advances controllability and fidelity for <span class="highlight">large-scale driving scene generation</span>, empowering data generation and simulation for autonomous driving.
</div>


{% include_relative bibtex.md %}
