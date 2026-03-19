# kwizeradavid.github.io<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kwizera David — Copywriter & Content Strategist</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0d0d0d;
    --paper: #f5f0e8;
    --cream: #ede8dc;
    --accent: #c8472a;
    --accent2: #1a3a5c;
    --gold: #c9a84c;
    --muted: #7a6e5f;
    --rule: #c8b89a;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NOISE TEXTURE OVERLAY ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.2rem 3rem;
    background: rgba(245, 240, 232, 0.9);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--rule);
  }

  .nav-logo {
    font-family: 'DM Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 80px;
    position: relative;
    overflow: hidden;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 5rem 4rem 5rem 5rem;
    position: relative;
    z-index: 2;
  }

  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .hero-eyebrow::before {
    content: '';
    display: block;
    width: 40px;
    height: 1px;
    background: var(--accent);
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3.5rem, 7vw, 6.5rem);
    font-weight: 900;
    line-height: 0.95;
    letter-spacing: -0.02em;
    margin-bottom: 0.4rem;
  }

  .hero-name .first { color: var(--ink); }
  .hero-name .last {
    color: transparent;
    -webkit-text-stroke: 2px var(--ink);
    display: block;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1rem, 2vw, 1.4rem);
    font-style: italic;
    color: var(--muted);
    margin: 1.8rem 0 2.5rem;
    font-weight: 400;
    line-height: 1.4;
  }

  .hero-summary {
    font-size: 1rem;
    line-height: 1.8;
    color: #3a3228;
    max-width: 480px;
    margin-bottom: 3rem;
    font-weight: 300;
  }

  .hero-cta {
    display: flex;
    gap: 1.2rem;
    align-items: center;
  }

  .btn-primary {
    background: var(--accent);
    color: white;
    padding: 0.9rem 2rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    border: none;
    cursor: pointer;
    transition: all 0.25s;
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
  }

  .btn-primary:hover {
    background: var(--accent2);
    transform: translateY(-2px);
  }

  .btn-secondary {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transition: color 0.2s;
  }

  .btn-secondary:hover { color: var(--ink); }

  .hero-right {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .hero-bg-text {
    position: absolute;
    font-family: 'Playfair Display', serif;
    font-size: 20vw;
    font-weight: 900;
    color: transparent;
    -webkit-text-stroke: 1px var(--rule);
    line-height: 1;
    user-select: none;
    letter-spacing: -0.05em;
    z-index: 0;
    opacity: 0.5;
  }

  .hero-card {
    position: relative;
    z-index: 2;
    background: var(--accent2);
    color: white;
    padding: 3rem 2.5rem;
    width: 340px;
    transform: rotate(2deg);
    box-shadow: 8px 8px 0 var(--accent);
  }

  .hero-card-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    opacity: 0.6;
    margin-bottom: 2rem;
    display: flex;
    align-items: center;
    gap: 0.6rem;
  }

  .hero-card-label::before {
    content: '';
    display: block;
    width: 20px;
    height: 1px;
    background: rgba(255,255,255,0.4);
  }

  .hero-card-stat {
    margin-bottom: 2rem;
  }

  .hero-card-stat .number {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem;
    font-weight: 900;
    line-height: 1;
    color: var(--gold);
  }

  .hero-card-stat .label {
    font-size: 0.85rem;
    opacity: 0.7;
    margin-top: 0.2rem;
    font-weight: 300;
  }

  .hero-divider { width: 100%; height: 1px; background: rgba(255,255,255,0.15); margin: 1.5rem 0; }

  .expertise-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
  }

  .tag {
    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(255,255,255,0.15);
    color: rgba(255,255,255,0.85);
    padding: 0.3rem 0.7rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    transition: all 0.2s;
  }

  .tag:hover {
    background: var(--accent);
    border-color: var(--accent);
  }

  /* ── SECTION COMMON ── */
  section { position: relative; }

  .section-inner {
    max-width: 1200px;
    margin: 0 auto;
    padding: 6rem 3rem;
  }

  .section-header {
    display: flex;
    align-items: baseline;
    gap: 1.5rem;
    margin-bottom: 4rem;
  }

  .section-num {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    color: var(--accent);
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
  }

  .section-rule {
    flex: 1;
    height: 1px;
    background: var(--rule);
    margin-left: 1rem;
  }

  /* ── EXPERIENCE ── */
  #experience { background: var(--paper); }

  .exp-grid {
    display: grid;
    gap: 0;
  }

  .exp-item {
    display: grid;
    grid-template-columns: 220px 1fr;
    gap: 3rem;
    padding: 3rem 0;
    border-top: 1px solid var(--rule);
    position: relative;
    transition: all 0.3s;
  }

  .exp-item:last-child { border-bottom: 1px solid var(--rule); }

  .exp-item::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 0;
    background: var(--cream);
    transition: width 0.4s ease;
    z-index: 0;
  }

  .exp-item:hover::before { width: 100%; }

  .exp-meta { position: relative; z-index: 1; }

  .exp-period {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.12em;
    color: var(--accent);
    margin-bottom: 0.6rem;
    display: block;
  }

  .exp-company {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--accent2);
    line-height: 1.3;
    margin-bottom: 0.3rem;
  }

  .exp-location {
    font-size: 0.8rem;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.08em;
  }

  .exp-content { position: relative; z-index: 1; }

  .exp-role {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    font-weight: 700;
    margin-bottom: 1.2rem;
    color: var(--ink);
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .exp-role-dot {
    width: 8px;
    height: 8px;
    background: var(--accent);
    border-radius: 50%;
    flex-shrink: 0;
  }

  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.7rem;
  }

  .exp-bullets li {
    font-size: 0.95rem;
    line-height: 1.7;
    color: #3a3228;
    padding-left: 1.2rem;
    position: relative;
    font-weight: 300;
  }

  .exp-bullets li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--gold);
    font-family: 'DM Mono', monospace;
  }

  /* ── EXPERTISE ── */
  #expertise { background: var(--ink); }

  #expertise .section-title { color: var(--paper); }
  #expertise .section-num { color: var(--gold); }
  #expertise .section-rule { background: rgba(255,255,255,0.15); }

  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: rgba(255,255,255,0.08);
    margin-top: 3rem;
  }

  .expertise-cell {
    background: var(--ink);
    padding: 2.5rem;
    transition: background 0.3s;
    cursor: default;
  }

  .expertise-cell:hover { background: var(--accent2); }

  .expertise-icon {
    font-size: 1.8rem;
    margin-bottom: 1rem;
    display: block;
  }

  .expertise-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--paper);
    margin-bottom: 0.5rem;
    line-height: 1.3;
  }

  .expertise-desc {
    font-size: 0.85rem;
    color: rgba(245, 240, 232, 0.5);
    line-height: 1.6;
    font-weight: 300;
  }

  /* ── EDUCATION ── */
  #education { background: var(--cream); }

  .edu-card {
    background: var(--paper);
    border: 1px solid var(--rule);
    padding: 3rem;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    align-items: start;
    position: relative;
    overflow: hidden;
  }

  .edu-card::after {
    content: 'ALU';
    position: absolute;
    right: -1rem;
    bottom: -2rem;
    font-family: 'Playfair Display', serif;
    font-size: 8rem;
    font-weight: 900;
    color: var(--cream);
    line-height: 1;
    pointer-events: none;
    letter-spacing: -0.05em;
  }

  .edu-degree {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--ink);
    line-height: 1.2;
    margin-bottom: 0.5rem;
  }

  .edu-school {
    color: var(--accent2);
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1.1rem;
    margin-bottom: 0.3rem;
  }

  .edu-location {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.1em;
  }

  .edu-period {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    color: var(--accent);
    text-align: right;
    white-space: nowrap;
  }

  /* ── LANGUAGES ── */
  .lang-strip {
    background: var(--accent);
    padding: 2rem 3rem;
    display: flex;
    align-items: center;
    gap: 3rem;
    overflow: hidden;
  }

  .lang-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.6);
    white-space: nowrap;
  }

  .lang-items {
    display: flex;
    gap: 2rem;
  }

  .lang-item {
    display: flex;
    align-items: center;
    gap: 0.7rem;
    color: white;
  }

  .lang-dot {
    width: 6px;
    height: 6px;
    background: rgba(255,255,255,0.5);
    border-radius: 50%;
  }

  .lang-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
  }

  .lang-level {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    opacity: 0.6;
    text-transform: uppercase;
  }

  /* ── CONTACT ── */
  #contact { background: var(--paper); }

  .contact-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
  }

  .contact-headline {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.5rem);
    font-weight: 900;
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 1.5rem;
  }

  .contact-headline em {
    font-style: italic;
    color: var(--accent);
  }

  .contact-sub {
    font-size: 1rem;
    color: var(--muted);
    line-height: 1.7;
    font-weight: 300;
    margin-bottom: 2.5rem;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .contact-link {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.2rem 0;
    border-bottom: 1px solid var(--rule);
    text-decoration: none;
    color: var(--ink);
    transition: all 0.2s;
    group: true;
  }

  .contact-link:first-child { border-top: 1px solid var(--rule); }

  .contact-link:hover { padding-left: 0.5rem; color: var(--accent); }

  .contact-link-left {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .contact-link-icon {
    width: 36px;
    height: 36px;
    background: var(--cream);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1rem;
    flex-shrink: 0;
    transition: background 0.2s;
  }

  .contact-link:hover .contact-link-icon { background: var(--accent); }

  .contact-link-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    display: block;
    margin-bottom: 0.1rem;
  }

  .contact-link-value {
    font-size: 0.95rem;
    font-weight: 400;
  }

  .contact-link-arrow {
    font-size: 1.2rem;
    color: var(--muted);
    transition: transform 0.2s;
  }

  .contact-link:hover .contact-link-arrow { transform: translate(4px, -4px); }

  .contact-right {
    position: relative;
  }

  .contact-card {
    background: var(--accent2);
    padding: 3rem;
    color: white;
    position: relative;
  }

  .contact-card::before {
    content: '"';
    position: absolute;
    top: -1rem;
    left: 2.5rem;
    font-family: 'Playfair Display', serif;
    font-size: 6rem;
    color: var(--gold);
    line-height: 1;
  }

  .contact-quote {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    font-style: italic;
    line-height: 1.6;
    margin-bottom: 2rem;
    opacity: 0.9;
    padding-top: 2rem;
  }

  .contact-quote-attr {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    opacity: 0.5;
  }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    color: rgba(245, 240, 232, 0.4);
    padding: 2rem 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  footer span { color: var(--gold); }

  /* ── SCROLL ANIMATIONS ── */
  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  /* ── HERO ENTRANCE ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(40px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to   { opacity: 1; }
  }

  .hero-eyebrow { animation: fadeUp 0.8s ease 0.2s both; }
  .hero-name    { animation: fadeUp 0.8s ease 0.35s both; }
  .hero-title   { animation: fadeUp 0.8s ease 0.5s both; }
  .hero-summary { animation: fadeUp 0.8s ease 0.65s both; }
  .hero-cta     { animation: fadeUp 0.8s ease 0.8s both; }
  .hero-card    { animation: fadeIn 1s ease 1s both; }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .hero { grid-template-columns: 1fr; min-height: auto; }
    .hero-right { display: none; }
    .hero-left { padding: 5rem 2rem 3rem; }
    .exp-item { grid-template-columns: 1fr; gap: 1rem; }
    .expertise-grid { grid-template-columns: 1fr 1fr; }
    .contact-layout { grid-template-columns: 1fr; }
    nav { padding: 1rem 1.5rem; }
    .nav-links { gap: 1.5rem; }
    .section-inner { padding: 4rem 1.5rem; }
  }

  @media (max-width: 600px) {
    .expertise-grid { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    .edu-card { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">KD — Portfolio</div>
  <ul class="nav-links">
    <li><a href="#experience">Work</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">Copywriter &amp; Content Strategist</div>
    <h1 class="hero-name">
      <span class="first">Kwizera</span>
      <span class="last">David</span>
    </h1>
    <p class="hero-title">Crafting copy that connects brands<br>to the people they exist to serve.</p>
    <p class="hero-summary">
      Dedicated copywriter with a passion for storytelling and brand building. 
      Specialising in digital platforms — from social media campaigns and website 
      copy to conference messaging and scripts — with experience spanning fintech, 
      conservation, logistics, and agricultural communications.
    </p>
    <div class="hero-cta">
      <a href="#contact" class="btn-primary">
        Get in Touch →
      </a>
      <a href="#experience" class="btn-secondary">
        View Work ↓
      </a>
    </div>
  </div>

  <div class="hero-right">
    <div class="hero-bg-text">KD</div>
    <div class="hero-card">
      <div class="hero-card-label">At a Glance</div>

      <div class="hero-card-stat">
        <div class="number">3+</div>
        <div class="label">Years of professional experience</div>
      </div>

      <div class="hero-divider"></div>

      <div class="hero-card-stat">
        <div class="number">2K+</div>
        <div class="label">Farmers reached through content</div>
      </div>

      <div class="hero-divider"></div>

      <div class="hero-card-label" style="margin-bottom: 0.8rem;">Areas of Expertise</div>
      <div class="expertise-tags">
        <span class="tag">Campaign Copy</span>
        <span class="tag">Brand Messaging</span>
        <span class="tag">Social Media</span>
        <span class="tag">Email Campaigns</span>
        <span class="tag">Content Strategy</span>
        <span class="tag">Web Copy</span>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-num">01</span>
      <h2 class="section-title">Work Experience</h2>
      <div class="section-rule"></div>
    </div>

    <div class="exp-grid">

      <!-- Job 1 -->
      <div class="exp-item reveal reveal-delay-1">
        <div class="exp-meta">
          <span class="exp-period">Nov 2025 — Present</span>
          <div class="exp-company">Inclusive FinTech Forum 2026</div>
          <div class="exp-location">Kigali, Rwanda</div>
        </div>
        <div class="exp-content">
          <div class="exp-role">
            <div class="exp-role-dot"></div>
            Website Content Manager
          </div>
          <ul class="exp-bullets">
            <li>Wrote all website copy including the homepage and daily event updates published throughout the forum, maintaining a clear and consistent voice for an international audience.</li>
            <li>Developed and executed end-to-end email campaigns that kept attendees, partners, and stakeholders informed and engaged before and during the event.</li>
            <li>Contributed to the pre-event social media rollout, creating platform-specific content that built anticipation, drove attendance, and increased engagement throughout the campaign period.</li>
          </ul>
        </div>
      </div>

      <!-- Job 2 -->
      <div class="exp-item reveal reveal-delay-2">
        <div class="exp-meta">
          <span class="exp-period">Jan 2025 — Sept 2025</span>
          <div class="exp-company">Messenger Logistics &amp; Trade Ltd</div>
          <div class="exp-location">Kigali, Rwanda</div>
        </div>
        <div class="exp-content">
          <div class="exp-role">
            <div class="exp-role-dot"></div>
            Copywriter
          </div>
          <ul class="exp-bullets">
            <li>Developed a social media content strategy and brand messaging framework that positioned Messenger as a credible, professional, and distinctly African logistics brand.</li>
            <li>Created content that balanced professionalism with cultural authenticity, building trust and visibility in a competitive sector.</li>
          </ul>
        </div>
      </div>

      <!-- Job 3 -->
      <div class="exp-item reveal reveal-delay-3">
        <div class="exp-meta">
          <span class="exp-period">Feb 2023 — Aug 2024</span>
          <div class="exp-company">One Acre Fund</div>
          <div class="exp-location">Kigali, Rwanda</div>
        </div>
        <div class="exp-content">
          <div class="exp-role">
            <div class="exp-role-dot"></div>
            Content Writer
          </div>
          <ul class="exp-bullets">
            <li>Developed farmer-facing content for over 2,000 smallholder farmers across Rwanda, translating complex product and service information into clear, accessible language.</li>
            <li>Wrote communications supporting warranty, returns, and contract programs, helping beneficiaries understand their rights and next steps at every touchpoint.</li>
            <li>Contributed to service delivery improvements by ensuring written communications were accurate, empathetic, and aligned with the needs of communities with varying levels of literacy.</li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-num">02</span>
      <h2 class="section-title">Areas of Expertise</h2>
      <div class="section-rule"></div>
    </div>

    <div class="expertise-grid">
      <div class="expertise-cell reveal reveal-delay-1">
        <span class="expertise-icon">✍️</span>
        <div class="expertise-name">Campaign Copy</div>
        <div class="expertise-desc">Persuasive, audience-first writing that drives action across paid and organic campaigns.</div>
      </div>
      <div class="expertise-cell reveal reveal-delay-2">
        <span class="expertise-icon">🎯</span>
        <div class="expertise-name">Brand Messaging</div>
        <div class="expertise-desc">Frameworks that give brands a clear, consistent voice they can own across every channel.</div>
      </div>
      <div class="expertise-cell reveal reveal-delay-3">
        <span class="expertise-icon">📱</span>
        <div class="expertise-name">Social Media Content</div>
        <div class="expertise-desc">Platform-native content that builds community, drives engagement, and grows audiences.</div>
      </div>
      <div class="expertise-cell reveal reveal-delay-1">
        <span class="expertise-icon">🌐</span>
        <div class="expertise-name">Website Copy</div>
        <div class="expertise-desc">Clear, compelling web copy that guides users and converts visitors into believers.</div>
      </div>
      <div class="expertise-cell reveal reveal-delay-2">
        <span class="expertise-icon">📧</span>
        <div class="expertise-name">Email Campaigns</div>
        <div class="expertise-desc">End-to-end campaign copy from subject lines to CTAs that keep subscribers engaged.</div>
      </div>
      <div class="expertise-cell reveal reveal-delay-3">
        <span class="expertise-icon">🌾</span>
        <div class="expertise-name">Agricultural &amp; Impact Comms</div>
        <div class="expertise-desc">Accessible, empathetic communications for development organisations and field-level audiences.</div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-num">03</span>
      <h2 class="section-title">Education</h2>
      <div class="section-rule"></div>
    </div>
    <div class="edu-card reveal">
      <div>
        <div class="edu-degree">BA. Computer Science</div>
        <div class="edu-school">African Leadership University</div>
        <div class="edu-location">Kigali, Rwanda</div>
      </div>
      <div class="edu-period">September 2017<br>— July 2021</div>
    </div>
  </div>
</section>

<!-- LANGUAGES STRIP -->
<div class="lang-strip">
  <div class="lang-label">Languages</div>
  <div class="lang-items">
    <div class="lang-item">
      <div class="lang-dot"></div>
      <div>
        <div class="lang-name">English</div>
        <div class="lang-level">Fluent</div>
      </div>
    </div>
    <div class="lang-item">
      <div class="lang-dot"></div>
      <div>
        <div class="lang-name">Kinyarwanda</div>
        <div class="lang-level">Native</div>
      </div>
    </div>
  </div>
</div>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-num">04</span>
      <h2 class="section-title">Get in Touch</h2>
      <div class="section-rule"></div>
    </div>

    <div class="contact-layout">
      <div class="reveal">
        <h3 class="contact-headline">Let's build something<br><em>worth reading.</em></h3>
        <p class="contact-sub">Whether you need a full brand voice overhaul, a campaign that cuts through the noise, or content that speaks to communities — let's talk.</p>

        <div class="contact-links">
          <a href="/cdn-cgi/l/email-protection#ed869a8497889f8c898c9b8489dfddad8a808c8481c38e8280" class="contact-link">
            <div class="contact-link-left">
              <div class="contact-link-icon">✉</div>
              <div>
                <span class="contact-link-label">Email</span>
                <span class="contact-link-value"><span class="__cf_email__" data-cfemail="a5ced2ccdfc0d7c4c1c4d3ccc19795e5c2c8c4ccc98bc6cac8">[email&#160;protected]</span></span>
              </div>
            </div>
            <span class="contact-link-arrow">↗</span>
          </a>
          <a href="tel:+250786206549" class="contact-link">
            <div class="contact-link-left">
              <div class="contact-link-icon">📞</div>
              <div>
                <span class="contact-link-label">Phone</span>
                <span class="contact-link-value">+250 786 206 549</span>
              </div>
            </div>
            <span class="contact-link-arrow">↗</span>
          </a>
          <a href="#" class="contact-link">
            <div class="contact-link-left">
              <div class="contact-link-icon">in</div>
              <div>
                <span class="contact-link-label">LinkedIn</span>
                <span class="contact-link-value">Kwizera David</span>
              </div>
            </div>
            <span class="contact-link-arrow">↗</span>
          </a>
          <a href="#" class="contact-link">
            <div class="contact-link-left">
              <div class="contact-link-icon">💬</div>
              <div>
                <span class="contact-link-label">Skype</span>
                <span class="contact-link-value">Kwizera david</span>
              </div>
            </div>
            <span class="contact-link-arrow">↗</span>
          </a>
          <div class="contact-link" style="cursor: default;">
            <div class="contact-link-left">
              <div class="contact-link-icon">📍</div>
              <div>
                <span class="contact-link-label">Location</span>
                <span class="contact-link-value">KG 25 Street, Kigali, Rwanda</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="contact-right reveal reveal-delay-2">
        <div class="contact-card">
          <p class="contact-quote">
            "I craft copy that connects brands to the people they exist to serve — with clarity, empathy, and a distinctly African voice."
          </p>
          <div class="contact-quote-attr">— Kwizera David, Copywriter</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div>© 2025 Kwizera David — <span>Kigali, Rwanda</span></div>
  <div>Copywriter &amp; Content Strategist</div>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' });

  reveals.forEach(el => observer.observe(el));

  // Active nav highlight
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');

  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
      if (window.scrollY >= 
