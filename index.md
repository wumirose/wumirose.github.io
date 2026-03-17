<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Olawumi Roseline Olasunkanmi</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=Source+Sans+3:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400&display=swap" rel="stylesheet">
  <style>
    :root {
      --ink: #1a1a2e;
      --ink-light: #3d3d5c;
      --ink-muted: #6b6b8d;
      --bg: #faf9f7;
      --bg-warm: #f5f0eb;
      --bg-card: #ffffff;
      --accent: #c0785a;
      --accent-light: #d4956e;
      --accent-bg: #fdf5f0;
      --rule: #e2ddd6;
      --rule-light: #ece8e2;
      --shadow-sm: 0 1px 3px rgba(26,26,46,0.04);
      --shadow-md: 0 4px 20px rgba(26,26,46,0.06);
      --shadow-lg: 0 8px 40px rgba(26,26,46,0.08);
      --radius: 12px;
      --serif: 'Instrument Serif', Georgia, serif;
      --sans: 'Source Sans 3', -apple-system, sans-serif;
    }

    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    html { scroll-behavior: smooth; font-size: 16px; }

    body {
      font-family: var(--sans);
      background: var(--bg);
      color: var(--ink);
      line-height: 1.7;
      -webkit-font-smoothing: antialiased;
      overflow-x: hidden;
    }

    ::selection {
      background: var(--accent);
      color: #fff;
    }

    a {
      color: var(--accent);
      text-decoration: none;
      transition: color 0.25s ease;
    }
    a:hover { color: var(--accent-light); }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      background: rgba(250,249,247,0.85);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--rule-light);
      transition: box-shadow 0.3s ease;
    }
    nav.scrolled { box-shadow: var(--shadow-sm); }

    .nav-inner {
      max-width: 1120px;
      margin: 0 auto;
      padding: 0 2rem;
      height: 64px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .nav-name {
      font-family: var(--serif);
      font-size: 1.25rem;
      color: var(--ink);
      letter-spacing: -0.01em;
    }

    .nav-links { display: flex; gap: 2rem; }
    .nav-links a {
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--ink-muted);
      position: relative;
      letter-spacing: 0.02em;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -4px; left: 0;
      width: 0; height: 1.5px;
      background: var(--accent);
      transition: width 0.3s ease;
    }
    .nav-links a:hover { color: var(--ink); }
    .nav-links a:hover::after { width: 100%; }

    .nav-toggle {
      display: none;
      background: none; border: none; cursor: pointer;
      width: 28px; height: 20px;
      position: relative;
    }
    .nav-toggle span {
      display: block; position: absolute; left: 0;
      width: 100%; height: 2px;
      background: var(--ink);
      transition: all 0.3s ease;
    }
    .nav-toggle span:nth-child(1) { top: 0; }
    .nav-toggle span:nth-child(2) { top: 9px; }
    .nav-toggle span:nth-child(3) { top: 18px; }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 2rem 80px;
    }

    .hero-inner {
      max-width: 1120px;
      margin: 0 auto;
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: center;
    }

    .hero-photo-wrap {
      position: relative;
      justify-self: center;
    }

    .hero-photo-wrap::before {
      content: '';
      position: absolute;
      top: -12px; left: -12px;
      right: 12px; bottom: 12px;
      border: 2px solid var(--accent);
      border-radius: var(--radius);
      opacity: 0.4;
      transition: all 0.4s ease;
    }
    .hero-photo-wrap:hover::before {
      top: -8px; left: -8px;
      opacity: 0.7;
    }

    .hero-photo {
      width: 340px;
      height: 420px;
      object-fit: cover;
      object-position: top center;
      border-radius: var(--radius);
      display: block;
      position: relative;
      z-index: 1;
      box-shadow: var(--shadow-lg);
    }

    .hero-text { max-width: 520px; }

    .hero-label {
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }
    .hero-label::before {
      content: '';
      width: 32px; height: 1.5px;
      background: var(--accent);
    }

    .hero-name {
      font-family: var(--serif);
      font-size: clamp(2.5rem, 4vw, 3.5rem);
      line-height: 1.1;
      letter-spacing: -0.02em;
      color: var(--ink);
      margin-bottom: 0.5rem;
    }

    .hero-title {
      font-size: 1.15rem;
      color: var(--ink-muted);
      font-weight: 400;
      margin-bottom: 1.5rem;
      line-height: 1.5;
    }

    .hero-desc {
      font-size: 1.05rem;
      color: var(--ink-light);
      line-height: 1.8;
      margin-bottom: 2rem;
    }

    .hero-links {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }
    .hero-links a {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.55rem 1.15rem;
      border: 1px solid var(--rule);
      border-radius: 100px;
      font-size: 0.85rem;
      font-weight: 500;
      color: var(--ink-light);
      background: var(--bg-card);
      transition: all 0.25s ease;
    }
    .hero-links a:hover {
      border-color: var(--accent);
      color: var(--accent);
      box-shadow: var(--shadow-sm);
      transform: translateY(-1px);
    }
    .hero-links a svg {
      width: 16px; height: 16px;
      flex-shrink: 0;
    }

    /* ── SECTIONS ── */
    section {
      padding: 5rem 2rem;
    }

    .section-inner {
      max-width: 1120px;
      margin: 0 auto;
    }

    .section-label {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.75rem;
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }
    .section-label::before {
      content: '';
      width: 24px; height: 1.5px;
      background: var(--accent);
    }

    .section-title {
      font-family: var(--serif);
      font-size: clamp(2rem, 3vw, 2.5rem);
      letter-spacing: -0.02em;
      margin-bottom: 1rem;
      line-height: 1.2;
    }

    .section-intro {
      font-size: 1.05rem;
      color: var(--ink-muted);
      max-width: 640px;
      line-height: 1.8;
      margin-bottom: 3rem;
    }

    /* ── ABOUT QUICK LINKS ── */
    .quick-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1.25rem;
    }

    .quick-card {
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: var(--radius);
      padding: 1.75rem 1.5rem;
      transition: all 0.3s ease;
      text-decoration: none;
      display: block;
    }
    .quick-card:hover {
      border-color: var(--accent);
      box-shadow: var(--shadow-md);
      transform: translateY(-3px);
    }

    .quick-card-icon {
      width: 40px; height: 40px;
      border-radius: 10px;
      background: var(--accent-bg);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1rem;
      color: var(--accent);
    }
    .quick-card-icon svg { width: 20px; height: 20px; }

    .quick-card h3 {
      font-family: var(--serif);
      font-size: 1.15rem;
      margin-bottom: 0.4rem;
      color: var(--ink);
    }
    .quick-card p {
      font-size: 0.88rem;
      color: var(--ink-muted);
      line-height: 1.6;
    }

    /* ── EDUCATION ── */
    .edu-timeline {
      position: relative;
      padding-left: 2rem;
    }
    .edu-timeline::before {
      content: '';
      position: absolute;
      left: 0; top: 8px; bottom: 8px;
      width: 1.5px;
      background: var(--rule);
    }

    .edu-item {
      position: relative;
      margin-bottom: 2.5rem;
    }
    .edu-item:last-child { margin-bottom: 0; }

    .edu-item::before {
      content: '';
      position: absolute;
      left: -2rem;
      top: 8px;
      width: 10px; height: 10px;
      border-radius: 50%;
      border: 2px solid var(--accent);
      background: var(--bg);
    }

    .edu-school {
      font-family: var(--serif);
      font-size: 1.3rem;
      margin-bottom: 0.3rem;
    }

    .edu-details {
      color: var(--ink-light);
      font-size: 0.95rem;
      line-height: 1.8;
    }
    .edu-details strong {
      color: var(--ink);
      font-weight: 600;
    }

    /* ── TEACHING ── */
    .bg-warm { background: var(--bg-warm); }

    .teach-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
    }

    .teach-courses {
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }

    .course-tag {
      display: inline-flex;
      align-items: center;
      padding: 0.65rem 1.1rem;
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: 8px;
      font-size: 0.9rem;
      color: var(--ink-light);
      transition: all 0.2s ease;
    }
    .course-tag:hover {
      border-color: var(--accent);
      color: var(--ink);
    }
    .course-tag .code {
      font-weight: 600;
      color: var(--accent);
      margin-right: 0.5rem;
      font-size: 0.8rem;
      letter-spacing: 0.03em;
    }

    .teach-philosophy {
      position: relative;
    }

    .philosophy-card {
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: var(--radius);
      padding: 2rem;
      box-shadow: var(--shadow-sm);
    }

    .philosophy-card h3 {
      font-family: var(--serif);
      font-size: 1.2rem;
      margin-bottom: 1.25rem;
    }

    .pillar {
      display: flex;
      gap: 0.75rem;
      margin-bottom: 1rem;
    }
    .pillar:last-child { margin-bottom: 0; }

    .pillar-num {
      width: 28px; height: 28px;
      border-radius: 50%;
      background: var(--accent-bg);
      color: var(--accent);
      font-weight: 700;
      font-size: 0.8rem;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      margin-top: 2px;
    }

    .pillar-text {
      font-size: 0.95rem;
      color: var(--ink-light);
      line-height: 1.6;
    }
    .pillar-text strong {
      color: var(--ink);
      font-weight: 600;
    }

    .teach-stat {
      display: flex;
      align-items: baseline;
      gap: 0.5rem;
      margin-top: 1.75rem;
      padding-top: 1.5rem;
      border-top: 1px solid var(--rule-light);
    }
    .teach-stat .num {
      font-family: var(--serif);
      font-size: 2.5rem;
      color: var(--accent);
      line-height: 1;
    }
    .teach-stat .label {
      font-size: 0.9rem;
      color: var(--ink-muted);
    }

    /* ── RESEARCH ── */
    .research-areas {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin-bottom: 2.5rem;
    }

    .area-pill {
      padding: 0.5rem 1.15rem;
      background: var(--accent-bg);
      color: var(--accent);
      border-radius: 100px;
      font-size: 0.88rem;
      font-weight: 500;
      border: 1px solid transparent;
      transition: all 0.2s ease;
    }
    .area-pill:hover {
      border-color: var(--accent);
    }

    .pub-list { display: flex; flex-direction: column; gap: 1.25rem; }

    .pub-item {
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: var(--radius);
      padding: 1.75rem 2rem;
      display: flex;
      align-items: flex-start;
      gap: 1.25rem;
      transition: all 0.3s ease;
    }
    .pub-item:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-2px);
    }

    .pub-year {
      font-family: var(--serif);
      font-size: 1.5rem;
      color: var(--accent);
      line-height: 1;
      flex-shrink: 0;
      padding-top: 3px;
    }

    .pub-info h3 {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.3rem;
      color: var(--ink);
      line-height: 1.5;
    }
    .pub-info p {
      font-size: 0.88rem;
      color: var(--ink-muted);
      font-style: italic;
    }

    /* ── SKILLS ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1.25rem;
    }

    .skill-group {
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: var(--radius);
      padding: 1.75rem 1.5rem;
    }

    .skill-group h3 {
      font-family: var(--serif);
      font-size: 1.05rem;
      margin-bottom: 1rem;
      color: var(--ink);
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .skill-tag {
      padding: 0.3rem 0.7rem;
      background: var(--bg-warm);
      border-radius: 6px;
      font-size: 0.82rem;
      color: var(--ink-light);
      font-weight: 500;
    }

    /* ── CTA ── */
    .cta-section {
      background: var(--ink);
      color: #fff;
      text-align: center;
      padding: 5rem 2rem;
    }

    .cta-section .section-label { color: var(--accent-light); justify-content: center; }
    .cta-section .section-label::before { background: var(--accent-light); }

    .cta-section .section-title {
      color: #fff;
      margin-bottom: 1rem;
    }

    .cta-desc {
      color: rgba(255,255,255,0.6);
      font-size: 1.05rem;
      max-width: 480px;
      margin: 0 auto 2rem;
      line-height: 1.7;
    }

    .cta-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.85rem 2rem;
      background: var(--accent);
      color: #fff;
      border-radius: 100px;
      font-weight: 600;
      font-size: 0.95rem;
      transition: all 0.25s ease;
      border: none; cursor: pointer;
    }
    .cta-btn:hover {
      background: var(--accent-light);
      color: #fff;
      transform: translateY(-2px);
      box-shadow: 0 6px 24px rgba(192,120,90,0.35);
    }

    /* ── FOOTER ── */
    footer {
      padding: 3rem 2rem;
      border-top: 1px solid var(--rule-light);
      text-align: center;
      font-size: 0.85rem;
      color: var(--ink-muted);
    }

    /* ── ANIMATIONS ── */
    .reveal {
      opacity: 0;
      transform: translateY(28px);
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

    .hero-text > * {
      opacity: 0;
      transform: translateY(20px);
      animation: heroFadeIn 0.7s ease forwards;
    }
    .hero-text > *:nth-child(1) { animation-delay: 0.2s; }
    .hero-text > *:nth-child(2) { animation-delay: 0.35s; }
    .hero-text > *:nth-child(3) { animation-delay: 0.5s; }
    .hero-text > *:nth-child(4) { animation-delay: 0.65s; }
    .hero-text > *:nth-child(5) { animation-delay: 0.8s; }

    .hero-photo-wrap {
      opacity: 0;
      transform: translateX(-30px);
      animation: heroPhotoIn 0.8s ease 0.3s forwards;
    }

    @keyframes heroFadeIn {
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes heroPhotoIn {
      to { opacity: 1; transform: translateX(0); }
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .hero-inner {
        grid-template-columns: 1fr;
        gap: 3rem;
        text-align: center;
      }
      .hero-photo-wrap { justify-self: center; order: -1; }
      .hero-photo { width: 280px; height: 340px; }
      .hero-text { max-width: 100%; }
      .hero-label { justify-content: center; }
      .hero-links { justify-content: center; }

      .quick-grid { grid-template-columns: repeat(2, 1fr); }
      .teach-grid { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: repeat(2, 1fr); }
    }

    @media (max-width: 640px) {
      .nav-links { display: none; }
      .nav-links.open {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 64px; left: 0; right: 0;
        background: rgba(250,249,247,0.98);
        backdrop-filter: blur(20px);
        padding: 1.5rem 2rem;
        gap: 1rem;
        border-bottom: 1px solid var(--rule-light);
      }
      .nav-toggle { display: block; }

      .quick-grid { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: 1fr; }
      .hero-photo { width: 240px; height: 300px; }

      section { padding: 3.5rem 1.25rem; }
    }
  </style>
</head>
<body>

  <!-- ── NAV ── -->
  <nav id="nav">
    <div class="nav-inner">
      <a href="/" class="nav-name">Olawumi Olasunkanmi</a>
      <div class="nav-links" id="navLinks">
        <a href="https://wumirose.github.io/">Home</a>
        <a href="https://wumirose.github.io/research">Research</a>
        <a href="https://wumirose.github.io/teaching">Teaching</a>
        <a href="https://wumirose.github.io/awards">Awards</a>
        <a href="https://wumirose.github.io/associations">Professional</a>
      </div>
      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
        <span></span><span></span><span></span>
      </button>
    </div>
  </nav>

  <!-- ── HERO ── -->
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-photo-wrap">
        <img class="hero-photo" src="https://wumirose.github.io/assets/images/DSC_9441.jpg" alt="Olawumi Roseline Olasunkanmi">
      </div>
      <div class="hero-text">
        <div class="hero-label">Computer Science</div>
        <h1 class="hero-name">Olawumi Roseline<br>Olasunkanmi</h1>
        <p class="hero-title">Doctoral Candidate &middot; University of North Carolina at Chapel Hill<br>Expected Graduation: May 2026</p>
        <p class="hero-desc">Seeking a teaching-focused faculty position beginning Fall 2026. My research centers on explainable biomedical knowledge graph augmentation, and I bring experience teaching 300+ students across Nigerian and American educational systems.</p>
        <div class="hero-links">
          <a href="mailto:roolasunkanmi@unc.edu">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
            Email
          </a>
          <a href="https://drive.google.com/file/d/1qDdwS1B2fHnVW_0KCw4x7jIbL6OpiPLE/view" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7Z"/><path d="M14 2v4a2 2 0 0 0 2 2h4"/></svg>
            CV
          </a>
          <a href="https://scholar.google.com/citations?user=4tvUEjkAAAAJ&hl=en" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="m8 12 3 3 5-6"/></svg>
            Scholar
          </a>
          <a href="https://www.linkedin.com/in/wumirosey/" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-4 0v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
            LinkedIn
          </a>
          <a href="https://www.x.com/wumirosey/" target="_blank">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4l11.733 16h4.267l-11.733 -16h-4.267z"/><path d="M4 20l6.768 -6.768m2.46 -2.46l6.772 -6.772"/></svg>
            X
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- ── QUICK LINKS ── -->
  <section>
    <div class="section-inner">
      <div class="quick-grid">
        <a href="https://wumirose.github.io/teaching" class="quick-card reveal">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>
          </div>
          <h3>Teaching</h3>
          <p>Courses taught, pedagogical approach, student mentorship</p>
        </a>
        <a href="https://wumirose.github.io/research" class="quick-card reveal reveal-delay-1">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9.937 15.5A2 2 0 0 0 8.5 14.063l-6.135-1.582a.5.5 0 0 1 0-.962L8.5 9.936A2 2 0 0 0 9.937 8.5l1.582-6.135a.5.5 0 0 1 .963 0L14.063 8.5A2 2 0 0 0 15.5 9.937l6.135 1.581a.5.5 0 0 1 0 .964L15.5 14.063a2 2 0 0 0-1.437 1.437l-1.582 6.135a.5.5 0 0 1-.963 0z"/></svg>
          </div>
          <h3>Research</h3>
          <p>Current projects, publications, ongoing collaborations</p>
        </a>
        <a href="https://wumirose.github.io/awards" class="quick-card reveal reveal-delay-2">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg>
          </div>
          <h3>Awards</h3>
          <p>Fellowships, travel awards, honors</p>
        </a>
        <a href="https://wumirose.github.io/associations" class="quick-card reveal reveal-delay-3">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
          </div>
          <h3>Professional</h3>
          <p>Memberships, reviewing, leadership roles</p>
        </a>
      </div>
    </div>
  </section>

  <!-- ── EDUCATION ── -->
  <section class="bg-warm">
    <div class="section-inner">
      <div class="section-label reveal">Education</div>
      <h2 class="section-title reveal">Academic Background</h2>
      <div class="edu-timeline" style="margin-top: 2.5rem;">
        <div class="edu-item reveal">
          <div class="edu-school">University of North Carolina at Chapel Hill</div>
          <div class="edu-details">
            <strong>Ph.D. in Computer Science</strong> (Expected May 2026)<br>
            <strong>M.Sc. in Computer Science</strong> (May 2023)<br><br>
            <strong>Dissertation:</strong> Knowledge Graph Augmentation with Data Integration and Explainable Edge Inference<br>
            <strong>Advisors:</strong> <a href="https://datascience.unc.edu/person/stan-ahalt/">Stanley Ahalt</a> &amp; <a href="https://harlinlee.github.io/">Harlin Lee</a>
          </div>
        </div>
        <div class="edu-item reveal reveal-delay-1">
          <div class="edu-school">Ladoke Akintola University of Technology</div>
          <div class="edu-details">
            <strong>B.Tech. in Computer Science</strong>, First Class Honors<br>
            GPA: 4.52 / 5.00 (2018) &middot; Ogbomoso, Nigeria
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── TEACHING ── -->
  <section>
    <div class="section-inner">
      <div class="section-label reveal">Teaching</div>
      <h2 class="section-title reveal">Teaching at a Glance</h2>
      <p class="section-intro reveal">Experience spanning programming, data structures, data science, and machine learning across diverse student populations.</p>

      <div class="teach-grid">
        <div class="teach-courses reveal">
          <div class="course-tag"><span class="code">DATA 110</span> Introduction to Data Science</div>
          <div class="course-tag"><span class="code">COMP 116</span> Introduction to Scientific Programming</div>
          <div class="course-tag"><span class="code">DMP</span> Data Matters Summer Program (Python &amp; Deep Learning)</div>
          <div class="course-tag"><span class="code">CS</span> Programming Fundamentals</div>
          <div class="course-tag"><span class="code">MATH</span> Discrete Mathematics &amp; Linear Algebra</div>
          <div class="course-tag"><span class="code">AI</span> Python and Machine Learning Training Program</div>
        </div>

        <div class="teach-philosophy reveal reveal-delay-1">
          <div class="philosophy-card">
            <h3>Teaching Philosophy</h3>
            <div class="pillar">
              <div class="pillar-num">1</div>
              <div class="pillar-text"><strong>Relevance drives engagement</strong> &mdash; connecting abstract concepts to real problems students care about</div>
            </div>
            <div class="pillar">
              <div class="pillar-num">2</div>
              <div class="pillar-text"><strong>Inclusion requires intentional design</strong> &mdash; creating classrooms where every student belongs</div>
            </div>
            <div class="pillar">
              <div class="pillar-num">3</div>
              <div class="pillar-text"><strong>Productive struggle builds confidence</strong> &mdash; challenging students at the right edge of their ability</div>
            </div>
            <div class="teach-stat">
              <span class="num">300+</span>
              <span class="label">students taught across<br>two countries</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── RESEARCH ── -->
  <section class="bg-warm">
    <div class="section-inner">
      <div class="section-label reveal">Research</div>
      <h2 class="section-title reveal">Research Highlights</h2>
      <p class="section-intro reveal">Building tools for explainable, knowledge-driven biomedical AI.</p>

      <div class="research-areas reveal">
        <span class="area-pill">Biomedical Knowledge Graphs</span>
        <span class="area-pill">Data Mining</span>
        <span class="area-pill">Explainable AI</span>
        <span class="area-pill">ML for Healthcare</span>
        <span class="area-pill">NLP</span>
      </div>

      <div class="pub-list">
        <div class="pub-item reveal">
          <div class="pub-year">2025</div>
          <div class="pub-info">
            <h3>RELATE: Relation Extraction in Biomedical Abstracts with LLMs and Ontology Constraints</h3>
            <p><strong>Olasunkanmi, O.R.</strong>, et al.</p>
          </div>
        </div>
        <div class="pub-item reveal reveal-delay-1">
          <div class="pub-year">2024</div>
          <div class="pub-info">
            <h3>Explainable Enrichment-Driven Graph Reasoner (EDGAR)</h3>
            <p><strong>Olasunkanmi, O.R.</strong>, et al. &mdash; IEEE Big Data Conference</p>
          </div>
        </div>
      </div>

      <p style="margin-top: 2rem;" class="reveal"><a href="https://wumirose.github.io/research" style="font-weight: 600;">View full research &amp; publications &rarr;</a></p>
    </div>
  </section>

  <!-- ── SKILLS ── -->
  <section>
    <div class="section-inner">
      <div class="section-label reveal">Skills</div>
      <h2 class="section-title reveal">Technical Skills</h2>
      <div class="skills-grid" style="margin-top: 2rem;">
        <div class="skill-group reveal">
          <h3>Programming</h3>
          <div class="skill-tags">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">R</span>
            <span class="skill-tag">SQL</span>
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">PHP</span>
          </div>
        </div>
        <div class="skill-group reveal reveal-delay-1">
          <h3>ML / AI</h3>
          <div class="skill-tags">
            <span class="skill-tag">PyTorch</span>
            <span class="skill-tag">TensorFlow</span>
            <span class="skill-tag">scikit-learn</span>
            <span class="skill-tag">Keras</span>
          </div>
        </div>
        <div class="skill-group reveal reveal-delay-2">
          <h3>Data Science</h3>
          <div class="skill-tags">
            <span class="skill-tag">pandas</span>
            <span class="skill-tag">NumPy</span>
            <span class="skill-tag">NetworkX</span>
            <span class="skill-tag">Neo4j</span>
          </div>
        </div>
        <div class="skill-group reveal reveal-delay-3">
          <h3>Web Dev</h3>
          <div class="skill-tags">
            <span class="skill-tag">React</span>
            <span class="skill-tag">HTML/CSS</span>
            <span class="skill-tag">WordPress</span>
            <span class="skill-tag">Joomla</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── CTA ── -->
  <section class="cta-section">
    <div class="section-inner" style="max-width: 640px;">
      <div class="section-label reveal">Get in Touch</div>
      <h2 class="section-title reveal">Let's Connect</h2>
      <p class="cta-desc reveal">Application materials including teaching statement, research statement, and complete CV are available upon request.</p>
      <a href="mailto:roolasunkanmi@unc.edu" class="cta-btn reveal">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
        roolasunkanmi@unc.edu
      </a>
    </div>
  </section>

  <!-- ── FOOTER ── -->
  <footer>
    <p>&copy; 2026 Olawumi Roseline Olasunkanmi. Built with purpose.</p>
  </footer>

  <script>
    // Nav scroll effect
    const nav = document.getElementById('nav');
    window.addEventListener('scroll', () => {
      nav.classList.toggle('scrolled', window.scrollY > 20);
    });

    // Mobile menu
    const toggle = document.getElementById('navToggle');
    const links = document.getElementById('navLinks');
    toggle.addEventListener('click', () => {
      links.classList.toggle('open');
    });

    // Scroll reveal
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>

</body>
</html>
