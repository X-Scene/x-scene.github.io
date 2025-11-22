---
layout: default
---

<div class="title-container">
  <img src="assets/images/logo.png" alt="Logo" class="logo">
  <h1>
    <span class="main-title"><span class="x-scene_1">𝒳</span><span class="x-scene_2">-</span><span class="x-scene_3">S</span><span class="x-scene_4">c</span><span class="x-scene_5">e</span><span class="x-scene_6">n</span><span class="x-scene_7">e</span>: Large-Scale Driving Scene Generation with High Fidelity and Flexible Controllability</span>
  </h1>
</div>

<p class="venue">NeurIPS 2025</p>

{% include_relative authors.md %}
{% include_relative links.md %}


## Abstract

<div class="method-container">
  <img src="assets/images/teaser.png" alt="Pipeline Image" class="method-image">

  <p class="method-caption">
  Overview of <span class="highlight-x-scene_1">𝒳</span><span class="highlight-x-scene_2">-</span><span class="highlight-x-scene_3">S</span><span class="highlight-x-scene_4">c</span><span class="highlight-x-scene_5">e</span><span class="highlight-x-scene_6">n</span><span class="highlight-x-scene_7">e</span>, a unified world generator that supports <span class="highlight">multi-granular controllability</span> through high-level text-to-layout generation and low-level BEV layout conditioning. It performs <span class="highlight">joint occupancy, image, and video generation</span> for 3D scene synthesis and reconstruction with high fidelity.
  </p>
</div>

<div class="abstract">

Diffusion models are advancing autonomous driving by enabling realistic data synthesis, predictive end-to-end planning, and closed-loop simulation, with a primary focus on temporally consistent generation. However, <span class="highlight">large-scale 3D scenes</span> requiring spatial coherence remains underexplored.

In this paper, we present <span class="highlight-x-scene_1">𝒳</span><span class="highlight-x-scene_2">-</span><span class="highlight-x-scene_3">S</span><span class="highlight-x-scene_4">c</span><span class="highlight-x-scene_5">e</span><span class="highlight-x-scene_6">n</span><span class="highlight-x-scene_7">e</span>, a novel framework for large-scale driving scene generation that achieves geometric intricacy, appearance fidelity, and flexible controllability.

Specifically, 𝒳<span class="italic">-Scene</span> supports multi-granular control, including low-level layout conditioning driven by user input or text for detailed scene composition, and high-level semantic guidance informed by user intent and LLM-enriched prompts for efficient customization.

To enhance geometric and visual fidelity, we introduce a unified pipeline that sequentially generates 3D semantic occupancy and corresponding multi-view images and videos, ensuring alignment and temporal consistency across modalities.

We further extend local regions into large-scale scenes via <span class="highlight">consistency-aware scene outpainting,</span> which extrapolates occupancy and images from previously generated areas to maintain spatial and visual coherence.

The resulting scenes are lifted into high-quality 3DGS representations, supporting diverse applications such as simulation and scene exploration.

Extensive experiments demonstrate that 𝒳<span class="italic">-Scene</span> substantially advances controllability and fidelity in large-scale scene generation, empowering data generation and simulation for autonomous driving.

</div>


## Method

<div class="method-container">
  <img src="assets/images/pipeline.png" alt="Pipeline Image" class="method-image">

  <p class="method-caption">
  Pipeline of <span class="x-scene_1">𝒳</span><span class="x-scene_2">-</span><span class="x-scene_3">S</span><span class="x-scene_4">c</span><span class="x-scene_5">e</span><span class="x-scene_6">n</span><span class="x-scene_7">e</span> for driving scene generation: <strong>(a) Multi-granular controllability</strong> supports both high-level text prompts and low-level geometric constraints for flexible specification;  <strong>(b) Joint occupancy-image-video generation</strong> synthesizes aligned 3D voxels and multi-view images and videos via conditional diffusion; <strong>(c) Large-scale extrapolation</strong> enables coherent scene expansion through consistency-aware outpainting.
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
<div class="button-row">
  <button class="toggle-btn active" onclick="showText2Scene(1)">Scene 1</button>
  <button class="toggle-btn" onclick="showText2Scene(2)">Scene 2</button>
  <button class="toggle-btn" onclick="showText2Scene(3)">Scene 3</button>
  <button class="toggle-btn" onclick="showText2Scene(4)">Scene 4</button>
</div>

<div id="text2scene-container" class="demo-section">
  <div id="text2scene-1" class="video-row scene active">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_1_1.webm" type="video/webm">
      </video>
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_1_2.webm" type="video/webm">
      </video>
    </div>
  </div>

  <div id="text2scene-2" class="video-row scene">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_2_1.webm" type="video/webm">
      </video>
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_2_2.webm" type="video/webm">
      </video>
    </div>
  </div>

  <div id="text2scene-3" class="video-row scene">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_3_1.webm" type="video/webm">
      </video>
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_3_2.webm" type="video/webm">
      </video>
    </div>
  </div>

  <div id="text2scene-4" class="video-row scene">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_4_1.webm" type="video/webm">
      </video>
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/text2scene_4_2.webm" type="video/webm">
      </video>
    </div>
  </div>
</div>

### 3. Large-Scale Scene Generation
<div class="button-row">
  <button class="toggle-btn active" onclick="showLargeScaleScene(1)">Scene 1</button>
  <button class="toggle-btn" onclick="showLargeScaleScene(2)">Scene 2</button>
</div>

<div id="largescale-container" class="demo-section">
  <div id="largescale-1" class="video-row scene active">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/largescale_1_1.webm" type="video/webm">
      </video>
    </div>
    <div class="video-row">
      <video class="video-medium" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/largescale_1_2.webm" type="video/webm">
      </video>
      <video class="video-medium" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/largescale_1_3.webm" type="video/webm">
      </video>
    </div>
  </div>

  <div id="largescale-2" class="video-row scene">
    <div class="video-row">
      <video class="video-normal" autoplay loop muted playsinline preload="metadata">
        <source src="assets/images/largescale_2.webm" type="video/webm">
      </video>
    </div>
  </div>
</div>

{% include_relative bibtex.md %}
