---
layout: splash
permalink: /
title: "Adaptive Condition Optimization for Text-to-Speech via Inference-Time Gradient Guidance"
author_profile: false
show_title: false
redirect_from:
  - /about/
  - /about.html
---

<style>
  #main {
    max-width: 1500px;
    padding-left: 1.5rem;
    padding-right: 1.5rem;
  }

  .splash .page__content {
    width: 100%;
    padding-top: 0;
  }

  .paper-shell {
    display: grid;
    gap: 2rem;
  }

  .paper-hero {
    display: grid;
    grid-template-columns: minmax(0, 1.02fr) minmax(420px, 0.98fr);
    gap: 1.6rem;
    margin-top: 0.25rem;
    padding: 2rem;
    border: 1px solid #d8e0eb;
    border-radius: 24px;
    background: linear-gradient(135deg, #f7fbff 0%, #eef5ff 55%, #f9fafc 100%);
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.08);
    align-items: center;
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
    grid-template-columns: minmax(0, 1.35fr) minmax(280px, 0.65fr);
    gap: 1.5rem;
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

  .paper-hero-figure {
    margin: 0;
  }

  .paper-hero-figure img,
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

  .paper-hero-note {
    margin-top: 0.8rem;
    font-size: 0.96rem;
    line-height: 1.65;
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

  .paper-figure {
    margin: 0;
    padding: 1.5rem;
    border: 1px solid #e5e7eb;
    border-radius: 20px;
    background: #ffffff;
    box-shadow: 0 12px 30px rgba(15, 23, 42, 0.05);
  }

  @media (max-width: 900px) {
    #main {
      padding-left: 1rem;
      padding-right: 1rem;
    }

    .paper-hero {
      grid-template-columns: 1fr;
      padding: 1.5rem 1.2rem;
    }

    .paper-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="paper-shell">
  <section class="paper-hero">
    <div>
      <p class="paper-kicker">TTS Paper Demo</p>
      <h1 class="paper-title">Adaptive Condition Optimization for Text-to-Speech via Inference-Time Gradient Guidance</h1>
      <p class="paper-subtitle">
        Aco-TTS is a training-free inference-time guidance framework for
        zero-shot text-to-speech. It dynamically refines the conditioning signal
        during sampling using reward gradients, enabling online correction of
        the flow trajectory for better intelligibility and perceptual quality.
      </p>

      <div class="paper-actions">
        <a class="paper-button primary" href="/files/Aco_TTS.pdf">Read Paper</a>
        <a class="paper-button secondary" href="https://github.com/Demo-TTS/ACO-TTS">View Code</a>
      </div>

      <p class="paper-hero-note">
        Training-free guidance at inference time for more robust zero-shot TTS.
      </p>
    </div>

    <figure class="paper-hero-figure">
      <img src="/images/aco-tts/full-architect.png" alt="Aco-TTS architecture overview">
      <p class="paper-caption">
        Main architecture overview of Aco-TTS and its adaptive condition
        optimization process.
      </p>
    </figure>
  </section>

  <section class="paper-grid">
    <div class="paper-card">
      <h2>Abstract</h2>
      <p>
        Existing zero-shot text-to-speech systems typically adopt a two-stage
        architecture combining a large language model with flow matching.
        However, flow matching follows an open-loop inference process without
        real-time correction during sampling, leading to speech distortion and
        unstable quality. A key limitation is that the condition is computed
        once before sampling and fixed throughout inference. Yet as the
        generation trajectory evolves, a static condition cannot adapt
        accordingly. To address this, we propose Adaptive Condition
        Optimization for Text-to-Speech (Aco-TTS), a gradient-guided framework
        for inference-time optimization that dynamically refines the condition
        during sampling using textual alignment and perceptual quality as
        guidance. This enables online correction and better constrains the flow
        trajectory. Aco-TTS is training-free and improves generation through
        gradient-based feedback at inference time. Experiments on SeedTTS,
        LibriSpeech, and AIShell-1 demonstrate significant reductions in word
        error rate and improvements in audio quality.
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
</div>
