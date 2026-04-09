---
permalink: /
title: "Adaptive Condition Optimization for Text-to-Speech via Inference-Time Gradient Guidance"
author_profile: false
show_title: false
redirect_from:
  - /about/
  - /about.html
---

<style>
  .paper-hero {
    margin-top: 0.5rem;
    padding: 2.25rem 2rem;
    border: 1px solid #d8e0eb;
    border-radius: 24px;
    background: linear-gradient(135deg, #f7fbff 0%, #eef5ff 55%, #f9fafc 100%);
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.08);
  }

  .paper-kicker {
    margin: 0 0 0.75rem;
    font-size: 0.9rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #2563eb;
  }

  .paper-title {
    margin: 0;
    font-size: clamp(2rem, 4vw, 3.1rem);
    line-height: 1.12;
    color: #111827;
  }

  .paper-subtitle {
    margin: 1rem 0 0;
    max-width: 46rem;
    font-size: 1.1rem;
    line-height: 1.75;
    color: #374151;
  }

  .paper-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.85rem;
    margin-top: 1.5rem;
  }

  .paper-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-width: 8.5rem;
    padding: 0.9rem 1.2rem;
    border-radius: 999px;
    text-decoration: none !important;
    font-weight: 700;
    transition: transform 0.18s ease, box-shadow 0.18s ease, background 0.18s ease;
  }

  .paper-button:hover {
    transform: translateY(-1px);
  }

  .paper-button.primary {
    color: #ffffff;
    background: #0f172a;
    box-shadow: 0 14px 24px rgba(15, 23, 42, 0.16);
  }

  .paper-button.secondary {
    color: #0f172a;
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid #cbd5e1;
  }

  .paper-grid {
    display: grid;
    grid-template-columns: minmax(0, 1.15fr) minmax(280px, 0.85fr);
    gap: 1.5rem;
    margin-top: 2rem;
    align-items: start;
  }

  .paper-card {
    padding: 1.5rem;
    border: 1px solid #e5e7eb;
    border-radius: 20px;
    background: #ffffff;
    box-shadow: 0 12px 30px rgba(15, 23, 42, 0.05);
  }

  .paper-card h2,
  .paper-card h3 {
    margin-top: 0;
    margin-bottom: 0.9rem;
    color: #111827;
  }

  .paper-card p {
    margin-bottom: 0;
    line-height: 1.8;
    color: #374151;
  }

  .paper-figure {
    margin-top: 2rem;
  }

  .paper-figure img {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 20px;
    border: 1px solid #dbe3ef;
    background: #ffffff;
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.08);
  }

  .paper-caption {
    margin: 0.8rem 0 0;
    font-size: 0.97rem;
    line-height: 1.7;
    color: #4b5563;
  }

  .paper-meta {
    display: grid;
    gap: 1rem;
  }

  .paper-meta-item strong {
    display: block;
    margin-bottom: 0.35rem;
    color: #111827;
  }

  .paper-meta-item a {
    word-break: break-word;
  }

  @media (max-width: 900px) {
    .paper-hero {
      padding: 1.5rem 1.2rem;
    }

    .paper-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<section class="paper-hero">
  <p class="paper-kicker">TTS Paper Demo</p>
  <h1 class="paper-title">Adaptive Condition Optimization for Text-to-Speech via Inference-Time Gradient Guidance</h1>
  <p class="paper-subtitle">
    Aco-TTS is a training-free inference-time guidance framework for zero-shot
    text-to-speech. It dynamically refines the conditioning signal during
    sampling using reward gradients, enabling online correction of the flow
    trajectory for better intelligibility and perceptual quality.
  </p>

  <div class="paper-actions">
    <a class="paper-button primary" href="/files/Aco_TTS.pdf">Read Paper</a>
    <a class="paper-button secondary" href="https://github.com/Demo-TTS/ACO-TTS">View Code</a>
  </div>
</section>

<section class="paper-grid">
  <div class="paper-card">
    <h2>Abstract</h2>
    <p>
      Existing zero-shot text-to-speech systems typically adopt a two-stage
      architecture combining a large language model with flow matching.
      However, flow matching follows an open-loop inference process without
      real-time correction during sampling, leading to speech distortion and
      unstable quality. A key limitation is that the condition is computed once
      before sampling and fixed throughout inference. Yet as the generation
      trajectory evolves, a static condition cannot adapt accordingly. To
      address this, we propose Adaptive Condition Optimization for Text-to-Speech
      (Aco-TTS), a gradient-guided framework for inference-time optimization
      that dynamically refines the condition during sampling using textual
      alignment and perceptual quality as guidance. This enables online
      correction and better constrains the flow trajectory. Aco-TTS is
      training-free and improves generation through gradient-based feedback at
      inference time. Experiments on SeedTTS, LibriSpeech, and AIShell-1
      demonstrate significant reductions in word error rate and improvements in
      audio quality.
    </p>
  </div>

  <aside class="paper-card paper-meta">
    <div class="paper-meta-item">
      <strong>Project</strong>
      <span>Aco-TTS Demo Page</span>
    </div>
    <div class="paper-meta-item">
      <strong>Paper PDF</strong>
      <a href="/files/Aco_TTS.pdf">/files/Aco_TTS.pdf</a>
    </div>
    <div class="paper-meta-item">
      <strong>Code</strong>
      <a href="https://github.com/Demo-TTS/ACO-TTS">https://github.com/Demo-TTS/ACO-TTS</a>
    </div>
    <div class="paper-meta-item">
      <strong>Demo Site</strong>
      <a href="https://demo-tts.github.io/">https://demo-tts.github.io/</a>
    </div>
  </aside>
</section>

<section class="paper-figure">
  <h2>Main Figure</h2>
  <img src="/images/aco-tts/full-architect.png" alt="Aco-TTS architecture overview">
  <p class="paper-caption">
    Overview of the Aco-TTS framework. The figure illustrates how adaptive
    condition optimization injects reward-guided feedback into inference-time
    sampling for text-to-speech generation.
  </p>
</section>
