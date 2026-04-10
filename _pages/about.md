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
  :root {
    --paper-bg: linear-gradient(135deg, #f7fbff 0%, #eef5ff 55%, #f9fafc 100%);
    --paper-border: #d8e0eb;
    --paper-card-bg: #ffffff;
    --paper-card-border: #e5e7eb;
    --paper-audio-bg: #f8fafc;
    --paper-strong: #111827;
    --paper-text: #374151;
    --paper-muted: #4b5563;
    --paper-kicker-bg: #e8f0ff;
    --paper-kicker-text: #1d4ed8;
    --paper-button-primary-bg: #0f172a;
    --paper-button-primary-text: #ffffff;
    --paper-button-secondary-bg: rgba(255, 255, 255, 0.9);
    --paper-button-secondary-text: #0f172a;
    --paper-button-secondary-border: #cbd5e1;
    --paper-shadow-lg: 0 18px 40px rgba(15, 23, 42, 0.08);
    --paper-shadow-md: 0 12px 30px rgba(15, 23, 42, 0.05);
  }

  html[data-theme="dark"] {
    --paper-bg: linear-gradient(135deg, #111827 0%, #0f172a 55%, #111827 100%);
    --paper-border: #334155;
    --paper-card-bg: #111827;
    --paper-card-border: #334155;
    --paper-audio-bg: #0f172a;
    --paper-strong: #f8fafc;
    --paper-text: #d1d5db;
    --paper-muted: #94a3b8;
    --paper-kicker-bg: rgba(59, 130, 246, 0.16);
    --paper-kicker-text: #93c5fd;
    --paper-button-primary-bg: #eff6ff;
    --paper-button-primary-text: #0f172a;
    --paper-button-secondary-bg: rgba(15, 23, 42, 0.72);
    --paper-button-secondary-text: #e5eefb;
    --paper-button-secondary-border: #475569;
    --paper-shadow-lg: 0 18px 40px rgba(2, 6, 23, 0.32);
    --paper-shadow-md: 0 12px 30px rgba(2, 6, 23, 0.24);
  }

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
    padding: 1.7rem 1.8rem;
    border: 1px solid var(--paper-border);
    border-radius: 24px;
    background: var(--paper-bg);
    box-shadow: var(--paper-shadow-lg);
    align-items: center;
  }

  .paper-kicker {
    margin: 0 0 0.75rem;
    font-size: 0.9rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--paper-kicker-text);
  }

  .paper-title {
    margin: 0;
    font-size: clamp(1.85rem, 3.35vw, 2.95rem);
    line-height: 1.06;
    letter-spacing: -0.03em;
    color: var(--paper-strong);
  }

  .paper-subtitle {
    margin: 0.85rem 0 0;
    max-width: 44rem;
    font-size: 1.02rem;
    line-height: 1.68;
    color: var(--paper-text);
  }

  .paper-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.85rem;
    margin-top: 1.15rem;
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
    color: var(--paper-button-primary-text);
    background: var(--paper-button-primary-bg);
    box-shadow: 0 14px 24px rgba(15, 23, 42, 0.16);
  }

  .paper-button.secondary {
    color: var(--paper-button-secondary-text);
    background: var(--paper-button-secondary-bg);
    border: 1px solid var(--paper-button-secondary-border);
  }

  .paper-grid {
    display: grid;
    grid-template-columns: minmax(0, 1.35fr) minmax(280px, 0.65fr);
    gap: 1.5rem;
    align-items: start;
  }

  .paper-card {
    padding: 1.5rem;
    border: 1px solid var(--paper-card-border);
    border-radius: 20px;
    background: var(--paper-card-bg);
    box-shadow: var(--paper-shadow-md);
  }

  .paper-card h2,
  .paper-card h3 {
    margin-top: 0;
    margin-bottom: 0.9rem;
    color: var(--paper-strong);
  }

  .paper-card p {
    margin-bottom: 0;
    line-height: 1.8;
    color: var(--paper-text);
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
    border: 1px solid var(--paper-border);
    background: var(--paper-card-bg);
    box-shadow: var(--paper-shadow-lg);
  }

  .paper-caption {
    margin: 0.8rem 0 0;
    font-size: 0.97rem;
    line-height: 1.7;
    color: var(--paper-muted);
  }

  .paper-meta {
    display: grid;
    gap: 1rem;
  }

  .paper-meta-item strong {
    display: block;
    margin-bottom: 0.35rem;
    color: var(--paper-strong);
  }

  .paper-meta-item a {
    word-break: break-word;
  }

  .paper-demos {
    display: grid;
    gap: 1.25rem;
  }

  .paper-demo-card {
    padding: 1.5rem;
    border: 1px solid var(--paper-card-border);
    border-radius: 20px;
    background: var(--paper-card-bg);
    box-shadow: var(--paper-shadow-md);
  }

  .paper-demo-card h3 {
    margin: 0 0 0.75rem;
    color: var(--paper-strong);
  }

  .paper-demo-heading {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    margin-bottom: 0.85rem;
    flex-wrap: wrap;
  }

  .paper-demo-kicker {
    display: inline-flex;
    align-items: center;
    padding: 0.28rem 0.7rem;
    border-radius: 999px;
    background: var(--paper-kicker-bg);
    color: var(--paper-kicker-text);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.04em;
    text-transform: uppercase;
  }

  .paper-demo-section-title {
    margin: 0 0 0.25rem;
    color: var(--paper-strong);
  }

  .paper-demo-section-note {
    margin: 0 0 1rem;
    color: var(--paper-muted);
    line-height: 1.7;
  }

  .paper-demo-text {
    display: grid;
    gap: 0.65rem;
    margin-bottom: 1rem;
    color: var(--paper-text);
    line-height: 1.75;
  }

  .paper-demo-text strong {
    color: var(--paper-strong);
  }

  .paper-audio-grid {
    display: grid;
    grid-template-columns: repeat(5, minmax(0, 1fr));
    gap: 0.9rem;
  }

  .paper-audio-item {
    padding: 0.9rem;
    border: 1px solid var(--paper-card-border);
    border-radius: 16px;
    background: var(--paper-audio-bg);
  }

  .paper-audio-item strong {
    display: block;
    margin-bottom: 0.55rem;
    color: var(--paper-strong);
  }

  .paper-audio-item audio {
    width: 100%;
  }

  .paper-figure {
    margin: 0;
    padding: 1.5rem;
    border: 1px solid var(--paper-card-border);
    border-radius: 20px;
    background: var(--paper-card-bg);
    box-shadow: var(--paper-shadow-md);
  }

  @media (max-width: 900px) {
    #main {
      padding-left: 1rem;
      padding-right: 1rem;
    }

    .paper-hero {
      grid-template-columns: 1fr;
      padding: 1.35rem 1.1rem;
    }

    .paper-grid {
      grid-template-columns: 1fr;
    }

    .paper-audio-grid {
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

  <section class="paper-demos">
    <div class="paper-demo-card">
      <h2 class="paper-demo-section-title">Audio Cases</h2>
      <p class="paper-demo-section-note">
        Comparisons use the CosyVoice2 backbone baseline together with the two
        reward-guided variants from the paper: Aco-TTS-ASR and Aco-TTS-MOS.
        The English samples come from SeedTTS test-en, and the Chinese samples
        come from SeedTTS test-zh.
      </p>
    </div>

    <div class="paper-demo-card">
      <div class="paper-demo-heading">
        <span class="paper-demo-kicker">Case 1</span>
        <h3>English Demo</h3>
      </div>
      <div class="paper-demo-text">
        <div><strong>Prompt text:</strong> You've got the Mayor and Pullman backed against a wall.</div>
        <div><strong>Target text:</strong> Her old man was Doc Mitchell.</div>
      </div>
      <div class="paper-audio-grid">
        <div class="paper-audio-item">
          <strong>Prompt</strong>
          <audio controls preload="none" src="/files/audio-demo/prompt-common_voice_en_2331.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Ground Truth</strong>
          <audio controls preload="none" src="/files/audio-demo/gt-common_voice_en_2331-common_voice_en_2330.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>CosyVoice2</strong>
          <audio controls preload="none" src="/files/audio-demo/seed-common_voice_en_2331-common_voice_en_2330.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-ASR</strong>
          <audio controls preload="none" src="/files/audio-demo/asr-common_voice_en_2331-common_voice_en_2330.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-MOS</strong>
          <audio controls preload="none" src="/files/audio-demo/mos-common_voice_en_2331-common_voice_en_2330.wav"></audio>
        </div>
      </div>
    </div>

    <div class="paper-demo-card">
      <div class="paper-demo-heading">
        <span class="paper-demo-kicker">Case 2</span>
        <h3>English Demo</h3>
      </div>
      <div class="paper-demo-text">
        <div><strong>Prompt text:</strong> I shall be neither more nor less meritorious.</div>
        <div><strong>Target text:</strong> Tyler, Lucy, Michelle, we're going to space!</div>
      </div>
      <div class="paper-audio-grid">
        <div class="paper-audio-item">
          <strong>Prompt</strong>
          <audio controls preload="none" src="/files/audio-demo/prompt-common_voice_en_15734837.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Ground Truth</strong>
          <audio controls preload="none" src="/files/audio-demo/gt-common_voice_en_15734837-common_voice_en_15734838.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>CosyVoice2</strong>
          <audio controls preload="none" src="/files/audio-demo/seed-common_voice_en_15734837-common_voice_en_15734838.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-ASR</strong>
          <audio controls preload="none" src="/files/audio-demo/asr-common_voice_en_15734837-common_voice_en_15734838.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-MOS</strong>
          <audio controls preload="none" src="/files/audio-demo/mos-common_voice_en_15734837-common_voice_en_15734838.wav"></audio>
        </div>
      </div>
    </div>

    <div class="paper-demo-card">
      <div class="paper-demo-heading">
        <span class="paper-demo-kicker">Case 3</span>
        <h3>English Demo</h3>
      </div>
      <div class="paper-demo-text">
        <div><strong>Prompt text:</strong> On the second day, the boy climbed to the top of a cliff near the camp.</div>
        <div><strong>Target text:</strong> The area was swirling in dust so intense that it hid the moon from view.</div>
      </div>
      <div class="paper-audio-grid">
        <div class="paper-audio-item">
          <strong>Prompt</strong>
          <audio controls preload="none" src="/files/audio-demo/prompt-common_voice_en_17161.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Ground Truth</strong>
          <audio controls preload="none" src="/files/audio-demo/gt-common_voice_en_17161-common_voice_en_17160.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>CosyVoice2</strong>
          <audio controls preload="none" src="/files/audio-demo/seed-common_voice_en_17161-common_voice_en_17160.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-ASR</strong>
          <audio controls preload="none" src="/files/audio-demo/asr-common_voice_en_17161-common_voice_en_17160.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-MOS</strong>
          <audio controls preload="none" src="/files/audio-demo/mos-common_voice_en_17161-common_voice_en_17160.wav"></audio>
        </div>
      </div>
    </div>

    <div class="paper-demo-card">
      <div class="paper-demo-heading">
        <span class="paper-demo-kicker">Case 4</span>
        <h3>Chinese Demo</h3>
      </div>
      <div class="paper-demo-text">
        <div><strong>Prompt text:</strong> 我挣扎了好久，把闹钟定在了八点。</div>
        <div><strong>Target text:</strong> 自动驾驶将大幅提升出行安全，效率。</div>
      </div>
      <div class="paper-audio-grid">
        <div class="paper-audio-item">
          <strong>Prompt</strong>
          <audio controls preload="none" src="/files/audio-demo/prompt-zh-10002739-00000104.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Ground Truth</strong>
          <audio controls preload="none" src="/files/audio-demo/gt-zh-10002739-00000011.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>CosyVoice2</strong>
          <audio controls preload="none" src="/files/audio-demo/seed-zh-10002739-00000011.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-ASR</strong>
          <audio controls preload="none" src="/files/audio-demo/asr-zh-10002739-00000011.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-MOS</strong>
          <audio controls preload="none" src="/files/audio-demo/mos-zh-10002739-00000011.wav"></audio>
        </div>
      </div>
    </div>

    <div class="paper-demo-card">
      <div class="paper-demo-heading">
        <span class="paper-demo-kicker">Case 5</span>
        <h3>Chinese Demo</h3>
      </div>
      <div class="paper-demo-text">
        <div><strong>Prompt text:</strong> 真正落地成为产品服务进入每个人的生活。</div>
        <div><strong>Target text:</strong> 就在营救进行的同时，楼下却不断地发出欢呼，起哄声。</div>
      </div>
      <div class="paper-audio-grid">
        <div class="paper-audio-item">
          <strong>Prompt</strong>
          <audio controls preload="none" src="/files/audio-demo/prompt-zh-10002481-00000010.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Ground Truth</strong>
          <audio controls preload="none" src="/files/audio-demo/gt-zh-10002481-00000105.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>CosyVoice2</strong>
          <audio controls preload="none" src="/files/audio-demo/seed-zh-10002481-00000105.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-ASR</strong>
          <audio controls preload="none" src="/files/audio-demo/asr-zh-10002481-00000105.wav"></audio>
        </div>
        <div class="paper-audio-item">
          <strong>Aco-TTS-MOS</strong>
          <audio controls preload="none" src="/files/audio-demo/mos-zh-10002481-00000105.wav"></audio>
        </div>
      </div>
    </div>
  </section>
</div>
