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


## Method

<div class="method-container">
  <img src="assets/images/pipeline.png" alt="Pipeline Image" class="method-image">

  <p class="method-caption">
  Pipeline of <span class="x-scene_1">𝒳</span><span class="x-scene_2">-</span><span class="x-scene_3">S</span><span class="x-scene_4">c</span><span class="x-scene_5">e</span><span class="x-scene_6">n</span><span class="x-scene_7">e</span> for scalable driving scene generation: <strong>(a) Multi-granular controllability</strong> supports both high-level text prompts and low-level geometric constraints for flexible specification;  <strong>(b) Joint occupancy-image generation</strong> synthesizes aligned 3D voxels and multi-view images via conditional diffusion; <strong>(c) Large-scale extrapolation and reconstruction</strong> enables coherent scene expansion through consistency-aware outpainting.
  </p>
</div>


## Scene Generation Results

### 1. Layout Conditioned Generation

<div class="demo-section">
  <div class="video-row">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/generation_1.webm" type="video/webm">
    </video>
  </div>

  <div class="video-row">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/generation_2.webm" type="video/webm">
    </video>
  </div>
</div>

### 2. Text-to-Scene Generation
<!-- <div class="demo-section">
  <div class="video-row">
    <img src="assets/images/text2scene_1_1.png" alt="Text2Scene 1_1" class="video-medium">
    <video class="video-medium" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_1_2.webm" type="video/webm">
    </video>
  </div>

  <div class="video-row">
    <img src="assets/images/text2scene_2_1.png" alt="Text2Scene 2_1" class="video-medium">
    <video class="video-medium" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_2_2.webm" type="video/webm">
    </video>
  </div>

  <div class="video-row">
    <img src="assets/images/text2scene_3_1.png" alt="Text2Scene 3_1" class="video-medium">
    <video class="video-medium" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_3_2.webm" type="video/webm">
    </video>
  </div>

  <div class="video-row">
    <img src="assets/images/text2scene_4_1.png" alt="Text2Scene 4_1" class="video-medium">
    <video class="video-medium" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_4_2.webm" type="video/webm">
    </video>
  </div>
</div> -->

<div class="button-row">
  <button class="toggle-btn active" onclick="showScene(1)">Scene 1</button>
  <button class="toggle-btn" onclick="showScene(2)">Scene 2</button>
  <button class="toggle-btn" onclick="showScene(3)">Scene 3</button>
  <button class="toggle-btn" onclick="showScene(4)">Scene 4</button>
</div>

<div class="demo-section">
  <div id="scene-1" class="video-row scene active">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_1_1.webm" type="video/webm">
    </video>
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_1_2.webm" type="video/webm">
    </video>
  </div>

  <div id="scene-2" class="video-row scene">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_2_1.webm" type="video/webm">
    </video>
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_2_2.webm" type="video/webm">
    </video>
  </div>

  <div id="scene-3" class="video-row scene">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_3_1.webm" type="video/webm">
    </video>
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_3_2.webm" type="video/webm">
    </video>
  </div>

  <div id="scene-4" class="video-row scene">
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_4_1.webm" type="video/webm">
    </video>
    <video class="video-normal" autoplay loop muted playsinline preload="metadata">
      <source src="assets/images/text2scene_4_2.webm" type="video/webm">
    </video>
  </div>
</div>


{% include_relative bibtex.md %}
