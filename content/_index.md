---
title: SPEXVA NOTE
comments: false
layout: hextra-home
---

<style>
  .sv-home {
    position: relative;
    padding: 2.5rem 0 1rem;
    overflow: hidden;
  }
  .sv-home::before,
  .sv-home::after {
    content: "";
    position: absolute;
    border-radius: 50%;
    pointer-events: none;
    z-index: 0;
  }
  .sv-home::before {
    width: 480px;
    height: 480px;
    top: -140px;
    left: -160px;
    background: radial-gradient(circle, rgba(30, 27, 75, 0.10), transparent 65%);
  }
  .sv-home::after {
    width: 420px;
    height: 420px;
    top: 60px;
    right: -140px;
    background: radial-gradient(circle, rgba(232, 168, 124, 0.16), transparent 65%);
  }
  html.dark .sv-home::before {
    background: radial-gradient(circle, rgba(99, 102, 241, 0.16), transparent 65%);
  }
  html.dark .sv-home::after {
    background: radial-gradient(circle, rgba(232, 168, 124, 0.10), transparent 65%);
  }

  .sv-hero {
    position: relative;
    z-index: 1;
    text-align: center;
    padding: 1.5rem 0 2rem;
  }
  .sv-hero-badge {
    display: inline-block;
    padding: 0.3rem 1rem;
    border: 1px solid rgba(30, 27, 75, 0.25);
    border-radius: 9999px;
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 0.14em;
    color: #1e1b4b;
    background: rgba(30, 27, 75, 0.05);
  }
  html.dark .sv-hero-badge {
    border-color: rgba(165, 180, 252, 0.3);
    color: #c7d2fe;
    background: rgba(99, 102, 241, 0.08);
  }
  .sv-hero-title {
    margin: 1.2rem auto 0;
    font-size: clamp(2.2rem, 6vw, 3.6rem);
    font-weight: 800;
    letter-spacing: 0.02em;
    line-height: 1.15;
    background: linear-gradient(100deg, #1e1b4b 10%, #4338ca 55%, #e8a87c 100%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  html.dark .sv-hero-title {
    background: linear-gradient(100deg, #e0e7ff 10%, #a5b4fc 55%, #f0c9a3 100%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  .sv-hero-sub {
    margin: 1rem auto 0;
    max-width: 34rem;
    color: #6b7280;
    font-size: 1.05rem;
    line-height: 1.8;
  }
  html.dark .sv-hero-sub { color: #9ca3af; }
  .sv-hero-actions {
    margin-top: 1.8rem;
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap;
  }
  .sv-btn {
    display: inline-block;
    padding: 0.65rem 1.7rem;
    border-radius: 0.75rem;
    font-weight: 600;
    font-size: 0.95rem;
    transition: transform 0.2s ease, box-shadow 0.2s ease, background 0.2s ease;
  }
  .sv-btn:hover { transform: translateY(-2px); }
  .sv-btn-primary {
    background: #1e1b4b;
    color: #fff;
    box-shadow: 0 4px 14px rgba(30, 27, 75, 0.25);
  }
  .sv-btn-primary:hover { box-shadow: 0 8px 20px rgba(30, 27, 75, 0.35); }
  html.dark .sv-btn-primary { background: #4f46e5; }
  .sv-btn-ghost {
    border: 1px solid #d1d5db;
    color: #374151;
    background: transparent;
  }
  .sv-btn-ghost:hover { border-color: #9ca3af; }
  html.dark .sv-btn-ghost {
    border-color: #4b5563;
    color: #d1d5db;
  }
  html.dark .sv-btn-ghost:hover { border-color: #6b7280; }

  .sv-section-head {
    position: relative;
    z-index: 1;
    display: flex;
    align-items: center;
    gap: 0.7rem;
    margin: 2.5rem 0 1.2rem;
  }
  .sv-section-head::before {
    content: "";
    width: 5px;
    height: 1.4em;
    border-radius: 3px;
    background: linear-gradient(180deg, #1e1b4b, #e8a87c);
  }
  .sv-section-head h2 {
    margin: 0;
    font-size: 1.35rem;
    font-weight: 700;
  }

  /* 手機適配 */
  @media (max-width: 640px) {
    .sv-home { padding: 1.2rem 0 0.5rem; }
    .sv-hero { padding: 1rem 0 1.5rem; }
    .sv-hero-title { font-size: clamp(1.9rem, 9vw, 2.6rem); }
    .sv-hero-sub { font-size: 0.95rem; line-height: 1.7; }
    .sv-btn { padding: 0.6rem 1.3rem; font-size: 0.9rem; }
    .sv-section-head { margin-top: 1.8rem; }
    .sv-section-head h2 { font-size: 1.2rem; }
  }
</style>

<div class="sv-home">
  <div class="sv-hero">
    <span class="sv-hero-badge">SPEXVA NOTES</span>
    <h1 class="sv-hero-title">筆記・技術・遊戲</h1>
    <p class="sv-hero-sub">
      學習筆記、Homelab 紀錄與程式筆記 — 中文、數學、M2、物理、ICT、English 與更多，全部整理在這裡。
    </p>
    <div class="sv-hero-actions">
      <a class="sv-btn sv-btn-primary" href="/docs/">探索筆記</a>
      <a class="sv-btn sv-btn-ghost" href="/game/">遊戲專區</a>
    </div>
  </div>

  <div class="sv-section-head">
    <h2>最新筆記</h2>
  </div>

  {{< latest-docs limit="6" >}}
</div>
