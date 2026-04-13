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
      --ink: #0f1a2e;
      --ink-light: #2d3f5e;
      --ink-muted: #5a6e8a;
      --bg: #f7f9fc;
      --bg-warm: #edf1f8;
      --bg-card: #ffffff;
      --accent: #3366cc;
      --accent-light: #5588dd;
      --accent-bg: #eef3fb;
      --rule: #d4dce8;
      --rule-light: #e4eaf2;
      --shadow-sm: 0 1px 3px rgba(15,26,46,0.05);
      --shadow-md: 0 4px 20px rgba(15,26,46,0.07);
      --shadow-lg: 0 8px 40px rgba(15,26,46,0.10);
      --radius: 12px;
      --serif: 'Instrument Serif', Georgia, serif;
      --sans: 'Source Sans 3', -apple-system, sans-serif;
    }

    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    html { scroll-behavior: smooth; font-size: 16px; scroll-padding-top: 72px; }

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
      background: rgba(247,249,252,0.85);
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
    
      white-space: nowrap;
    }
    
    @media (max-width: 420px) {
      .hero-name {
        white-space: normal;
        font-size: 2rem;
      }
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

    /* ── SUBSECTION TITLES ── */
    .subsection-title {
      font-family: var(--serif);
      font-size: 1.2rem;
      color: var(--ink);
      margin-top: 2.5rem;
      margin-bottom: 1rem;
      padding-bottom: 0.5rem;
      border-bottom: 1px solid var(--rule-light);
    }

    /* ── RESEARCH EXPERIENCE ── */
    .experience-item {
      margin-bottom: 1.5rem;
    }
    .exp-header {
      font-size: 0.95rem;
      color: var(--ink);
      line-height: 1.6;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: baseline;
      gap: 0.5rem;
    }
    .exp-date {
      font-size: 0.85rem;
      color: var(--ink-muted);
      font-weight: 500;
      white-space: nowrap;
    }
    .exp-body {
      font-size: 0.93rem;
      color: var(--ink-light);
      line-height: 1.7;
      margin-top: 0.4rem;
    }
    .exp-tech {
      font-size: 0.9rem;
      color: var(--ink-muted);
      margin-top: 0.5rem;
    }

    /* ── POSTER LIST ── */
    .poster-list {
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }
    .poster-item {
      font-size: 0.93rem;
      color: var(--ink-light);
      line-height: 1.7;
      padding-left: 1rem;
      border-left: 2px solid var(--rule-light);
      transition: border-color 0.2s ease;
    }
    .poster-item:hover {
      border-left-color: var(--accent);
    }

    /* ── MENTORSHIP ── */
    .mentorship p {
      font-size: 0.95rem;
      color: var(--ink-light);
      line-height: 1.7;
    }

    /* ── AWARDS ── */
    .awards-grid {
      display: flex;
      flex-direction: column;
      gap: 0;
      margin-top: 2rem;
    }
    .award-item {
      display: flex;
      align-items: baseline;
      gap: 1.25rem;
      padding: 1rem 0;
      border-bottom: 1px solid var(--rule-light);
      transition: padding-left 0.3s ease;
    }
    .award-item:first-child { border-top: 1px solid var(--rule-light); }
    .award-item:hover { padding-left: 0.5rem; }

    .award-year {
      font-family: var(--serif);
      font-size: 1.05rem;
      color: var(--accent);
      flex-shrink: 0;
      min-width: 60px;
    }
    .award-info h3 {
      font-size: 0.95rem;
      font-weight: 500;
      color: var(--ink-light);
      line-height: 1.5;
    }

    /* ── PROFESSIONAL SERVICE ── */
    .pro-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2.5rem;
    }

    .membership-list {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
    }
    .membership-tag {
      padding: 0.45rem 1rem;
      background: var(--bg-card);
      border: 1px solid var(--rule-light);
      border-radius: 100px;
      font-size: 0.88rem;
      color: var(--ink-light);
      font-weight: 500;
      transition: all 0.2s ease;
    }
    .membership-tag:hover {
      border-color: var(--accent);
      color: var(--ink);
    }

    .service-list {
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }
    .service-item {
      font-size: 0.93rem;
      color: var(--ink-light);
      line-height: 1.6;
      padding-left: 0.75rem;
      border-left: 2px solid var(--rule-light);
      transition: border-color 0.2s ease;
    }
    .service-item:hover {
      border-left-color: var(--accent);
    }

    .nav-links a.active { color: var(--ink); }
    .nav-links a.active::after { width: 100%; }

    /* ── NEWS ── */
    .news-feed {
      display: flex;
      flex-direction: column;
      gap: 0;
      margin-top: 2rem;
    }

    .news-item {
      display: flex;
      gap: 1.5rem;
      padding: 1.5rem 0;
      border-bottom: 1px solid var(--rule-light);
      transition: all 0.3s ease;
    }
    .news-item:first-child { border-top: 1px solid var(--rule-light); }
    .news-item:hover { padding-left: 0.5rem; }

    .news-date {
      flex-shrink: 0;
      width: 64px;
      text-align: center;
      padding-top: 4px;
    }
    .news-month {
      display: block;
      font-family: var(--serif);
      font-size: 1.15rem;
      color: var(--ink);
      line-height: 1.2;
    }
    .news-year {
      display: block;
      font-size: 0.8rem;
      color: var(--ink-muted);
      letter-spacing: 0.03em;
    }

    .news-content { flex: 1; }

    .news-badge {
      display: inline-block;
      padding: 0.2rem 0.65rem;
      border-radius: 100px;
      font-size: 0.72rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      background: var(--accent-bg);
      color: var(--accent);
      margin-bottom: 0.5rem;
    }
    .news-badge.badge-completed {
      background: #e6f4f1;
      color: #1a7a6d;
    }
    .news-badge.badge-pub {
      background: #e8f0fe;
      color: #2952a3;
    }
    .news-badge.badge-open {
      background: #e6f4f1;
      color: #1a7a6d;
    }
    .news-badge.badge-degree {
      background: #e8eaf6;
      color: #3949ab;
    }

    .news-content h3 {
      font-family: var(--serif);
      font-size: 1.15rem;
      margin-bottom: 0.35rem;
      color: var(--ink);
    }
    .news-content p {
      font-size: 0.93rem;
      color: var(--ink-light);
      line-height: 1.7;
    }
    .news-content em {
      color: var(--ink-muted);
    }

    /* ── CTA ── */
    .cta-section {
      background: linear-gradient(135deg, #0f1a2e 0%, #1a3058 100%);
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
      box-shadow: 0 6px 24px rgba(51,102,204,0.35);
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
      .pro-grid { grid-template-columns: 1fr; }
    }

    @media (max-width: 640px) {
      .nav-links { display: none; }
      .nav-links.open {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 64px; left: 0; right: 0;
        background: rgba(247,249,252,0.98);
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

      .news-item { gap: 1rem; }
      .news-date { width: 52px; }
    }
  </style>
</head>
<body>

  <!-- ── NAV ── -->
  <nav id="nav">
    <div class="nav-inner">
      <a href="#hero" class="nav-name">Olawumi Olasunkanmi</a>
      <div class="nav-links" id="navLinks">
        <a href="#hero" class="active">Home</a>
        <a href="#news">News</a>
        <a href="#research">Research</a>
        <a href="#teaching">Teaching</a>
        <a href="#awards">Awards</a>
        <a href="#professional">Service</a>
        <a href="#contact">Contact</a>
      </div>
      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
        <span></span><span></span><span></span>
      </button>
    </div>
  </nav>

  <!-- ── HERO ── -->
  <section class="hero" id="hero">
    <div class="hero-inner">
      <div class="hero-photo-wrap">
        <img class="hero-photo" src="https://wumirose.github.io/assets/images/DSC_9441.jpg" alt="Olawumi Roseline Olasunkanmi">
      </div>
      <div class="hero-text">
        <div class="hero-label">Computer Science</div>
        <h1 class="hero-name">Olawumi Roseline Olasunkanmi</h1>
        <p class="hero-title"> Ph.D. Candidate, University of North Carolina at Chapel Hill<br> Dissertation Defended: April 2026<br> Degree Conferral: May 2026</p>
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
        <a href="#teaching" class="quick-card reveal">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>
          </div>
          <h3>Teaching</h3>
          <p>Courses taught, pedagogical approach, student mentorship</p>
        </a>
        <a href="#research" class="quick-card reveal reveal-delay-1">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9.937 15.5A2 2 0 0 0 8.5 14.063l-6.135-1.582a.5.5 0 0 1 0-.962L8.5 9.936A2 2 0 0 0 9.937 8.5l1.582-6.135a.5.5 0 0 1 .963 0L14.063 8.5A2 2 0 0 0 15.5 9.937l6.135 1.581a.5.5 0 0 1 0 .964L15.5 14.063a2 2 0 0 0-1.437 1.437l-1.582 6.135a.5.5 0 0 1-.963 0z"/></svg>
          </div>
          <h3>Research</h3>
          <p>Publications, posters, mentorship, collaborations</p>
        </a>
        <a href="#awards" class="quick-card reveal reveal-delay-2">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg>
          </div>
          <h3>Awards</h3>
          <p>Fellowships, travel awards, honors</p>
        </a>
        <a href="#professional" class="quick-card reveal reveal-delay-3">
          <div class="quick-card-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
          </div>
          <h3>Professional Service</h3>
          <p>Memberships, reviewing, leadership roles</p>
        </a>
      </div>
    </div>
  </section>

  <!-- ── NEWS ── -->
  <section id="news">
    <div class="section-inner">
      <div class="section-label reveal">News</div>
      <h2 class="section-title reveal">Latest Updates</h2>
      <div class="news-feed">

        <div class="news-item reveal">
          <div class="news-date">
            <span class="news-month">Apr</span>
            <span class="news-year">2026</span>
          </div>
          <div class="news-content">
            <span class="news-badge badge-completed">Completed</span>
            <h3>Ph.D. Dissertation Defense</h3>
            <p>Successfully defended my dissertation on <em>Knowledge Graph Augmentation with Data Integration and Explainable Edge Inference</em> at UNC Chapel Hill on April 9, 2026.</p>
          </div>
        </div>

        <div class="news-item reveal reveal-delay-1">
          <div class="news-date">
            <span class="news-month">2026</span>
            <span class="news-year">&nbsp;</span>
          </div>
          <div class="news-content">
            <span class="news-badge badge-open">On the Market</span>
            <h3>Faculty Job Search</h3>
            <p>Actively seeking teaching-focused faculty positions (Teaching Professor, Instructor) beginning Fall 2026. Open to universities, liberal arts colleges, and community colleges. <a href="#contact" style="font-weight: 600;">Get in touch &rarr;</a></p>
          </div>
        </div>

        <div class="news-item reveal reveal-delay-2">
          <div class="news-date">
            <span class="news-month">2025</span>
            <span class="news-year">&nbsp;</span>
          </div>
          <div class="news-content">
            <span class="news-badge badge-pub">Publication</span>
            <h3>RELATE Paper</h3>
            <p>Published <em>RELATE: Relation Extraction in Biomedical Abstracts with LLMs and Ontology Constraints</em>, a biomedical NLP pipeline for triple extraction from PubMed abstracts.</p>
          </div>
        </div>

        <div class="news-item reveal reveal-delay-3">
          <div class="news-date">
            <span class="news-month">Dec</span>
            <span class="news-year">2024</span>
          </div>
          <div class="news-content">
            <span class="news-badge badge-pub">Publication</span>
            <h3>EDGAR at IEEE Big Data</h3>
            <p>Presented the Explainable Enrichment-Driven Graph Reasoner (EDGAR) at the IEEE Big Data Conference.</p>
          </div>
        </div>

        <div class="news-item reveal reveal-delay-4">
          <div class="news-date">
            <span class="news-month">2023</span>
            <span class="news-year">&nbsp;</span>
          </div>
          <div class="news-content">
            <span class="news-badge badge-degree">Degree</span>
            <h3>M.Sc. in Computer Science</h3>
            <p>Completed my Master's degree at UNC Chapel Hill while continuing into the Ph.D. program.</p>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ── EDUCATION ── -->
  <section class="bg-warm" id="education">
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
  <section id="teaching">
    <div class="section-inner">
      <div class="section-label reveal">Teaching</div>
      <h2 class="section-title reveal">Teaching at a Glance</h2>
      <p class="section-intro reveal">Experience spanning programming, data structures, data science, and machine learning across diverse student populations.</p>

      <div class="teach-grid">
        <div class="teach-courses reveal">
          <div class="course-tag"><span class="code">TA</span> Introduction to Data Science (DATA 110)</div>
          <div class="course-tag"><span class="code">TA</span> Introduction to Scientific Programming (COMP 116)</div>
          <div class="course-tag"><span class="code">TA</span> Data Matters Summer Program (Python &amp; Deep Learning)</div>
          <div class="course-tag"><span class="code">Substitute Lecturer</span> Programming Fundamentals</div>
          <div class="course-tag"><span class="code">Substitute Lecturer</span> Discrete Mathematics &amp; Linear Algebra</div>
          <div class="course-tag"><span class="code">Instructor</span> Python and Machine Learning Training Program</div>
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
  <section class="bg-warm" id="research">
    <div class="section-inner">
      <div class="section-label reveal">Research</div>
      <h2 class="section-title reveal">Research</h2>
      <p class="section-intro reveal">Building tools for explainable, knowledge-driven biomedical AI.</p>

      <div class="research-areas reveal">
        <span class="area-pill">Biomedical Knowledge Graphs</span>
        <span class="area-pill">Data Mining</span>
        <span class="area-pill">Explainable AI</span>
        <span class="area-pill">ML for Healthcare</span>
        <span class="area-pill">NLP</span>
      </div>

      <!-- Research Experience -->
      <h3 class="subsection-title reveal">Research Assistant</h3>

      <div class="experience-item reveal">
        <div class="exp-header">
           &mdash; Renaissance Computing Institute (RENCI), UNC Chapel Hill
        </div>
      </div>

      <div class="experience-item reveal">
        <div class="exp-header">
         &mdash; Ladoke Akintola University of Technology, Nigeria
        </div>
      </div>

      <!-- Publications -->
      <h3 class="subsection-title reveal">Publications</h3>

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

      <p style="margin-top: 1.5rem;" class="reveal"><a href="https://scholar.google.com/citations?user=4tvUEjkAAAAJ&hl=en" target="_blank" style="font-weight: 600;">See more on Google Scholar &rarr;</a></p>

      <!-- Posters -->
      <h3 class="subsection-title reveal">Poster Presentations</h3>

      <div class="poster-list">
        <div class="poster-item reveal">
          <em>Enhancing KG Augmentation</em> &mdash; Doctoral Forum, SIAM International Conference on Data Mining (SDM25), Virginia
        </div>
        <div class="poster-item reveal">
          <em>Enhancing Knowledge Graph Inference through Enrichment and Grouping</em> &mdash; Data Science Day, School of Data Science and Society, UNC Chapel Hill
        </div>
        <div class="poster-item reveal">
          <em>Information Extraction for Graph Generation &amp; Inference (A Case Study of COVID-19 KG)</em> &mdash; CRA-WP Grad Cohort for Women, San Francisco
        </div>
        <div class="poster-item reveal">
          <em>Deep Neural Network-Based Approach to Skin Cancer Classification</em> &mdash; 2nd Black in AI Workshop, NeurIPS 2018, Montreal
        </div>
      </div>

      <!-- Mentorship -->
      <h3 class="subsection-title reveal">Student Mentorship</h3>

      <div class="mentorship reveal">
        <p>Co-supervised five undergraduate research projects in Data Mining and Machine Learning.</p>
        <p style="margin-top: 0.5rem;"><strong>Undergraduate Project Outcome:</strong> Abdulquadri Adegbiji &mdash; <a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=4tvUEjkAAAAJ&citation_for_view=4tvUEjkAAAAJ:Y0pCki6q_DkC" target="_blank">Classification of Chronic Kidney Diseases</a></p>
      </div>

    </div>
  </section>

  <!-- ── AWARDS ── -->
  <section id="awards">
    <div class="section-inner">
      <div class="section-label reveal">Recognition</div>
      <h2 class="section-title reveal">Awards &amp; Fellowships</h2>

      <div class="awards-grid">
        <div class="award-item reveal">
          <span class="award-year">2024</span>
          <div class="award-info">
            <h3>NSF Travel Award &mdash; MLSystem</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2024</span>
          <div class="award-info">
            <h3>NSF Travel Award &mdash; IEEE BigData</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2024&ndash;25</span>
          <div class="award-info">
            <h3>ACM Travel Award &mdash; PEARC Conference</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2023</span>
          <div class="award-info">
            <h3>WiML Registration Award &mdash; NeurIPS</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2021</span>
          <div class="award-info">
            <h3>Diversity &amp; Inclusion Fellowship &mdash; UNC Graduate School</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2020</span>
          <div class="award-info">
            <h3>Top 30% Selected Participant &mdash; Cornell&ndash;Maryland&ndash;Max Planck Pre-doctoral School (CMMRS)</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2020</span>
          <div class="award-info">
            <h3>Top 16% Selected &mdash; "Solving the Algorithm: Women in Machine Learning" Conference</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2019</span>
          <div class="award-info">
            <h3>Full Sponsorship &mdash; PyCon Africa, Ghana</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2018</span>
          <div class="award-info">
            <h3>Full Travel Support &mdash; Black in AI Workshop, NeurIPS</h3>
          </div>
        </div>
        <div class="award-item reveal">
          <span class="award-year">2018</span>
          <div class="award-info">
            <h3>Nigerian Women TechSters Fellowship &mdash; Web &amp; Mobile Application Development</h3>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── PROFESSIONAL ── -->
  <section class="bg-warm" id="professional">
    <div class="section-inner">
      <div class="section-label reveal">Service</div>
      <h2 class="section-title reveal">Professional Service</h2>

      <div class="pro-grid">
        <div class="pro-column reveal">
          <h3 class="subsection-title">Memberships</h3>
          <div class="membership-list">
            <span class="membership-tag">ACM</span>
            <span class="membership-tag">Women in Machine Learning (WiML)</span>
            <span class="membership-tag">Black in AI (BAI)</span>
            <span class="membership-tag">IEEE</span>
            <span class="membership-tag">IAENG</span>
          </div>
        </div>

        <div class="pro-column reveal reveal-delay-1">
          <h3 class="subsection-title">Session Chair</h3>
          <div class="service-item">
            Practice and Experience in Advanced Research Computing (PEARC), Application &amp; Software Track 6, PEARC25, Columbus, Ohio (2025)
          </div>
        </div>
      </div>

      <div class="pro-grid" style="margin-top: 2rem;">
        <div class="pro-column reveal">
          <h3 class="subsection-title">Peer Reviewer</h3>
          <div class="service-list">
            <div class="service-item">IEEE ICECET, Paris (2025)</div>
            <div class="service-item">Bioinformatics Open Source Conference (<a href="https://www.open-bio.org/events/bosc-2025/" target="_blank">BOSC</a>), Liverpool, UK (2025)</div>
            <div class="service-item">NeurIPS Position Papers, San Diego (2025)</div>
            <div class="service-item">IEEE <a href="https://camsap25.ig.umons.ac.be/tpc.php" target="_blank">CAMSAP25</a>, Dominican Republic (2025)</div>
            <div class="service-item">Technical Program Reviewer <a href="https://dl.acm.org/action/showFmPdf?doi=10.1145%2F3626203" target="_blank">PEARC24</a>, Providence, Rhode Island (2024)</div>
          </div>
        </div>

        <div class="pro-column reveal reveal-delay-1">
          <h3 class="subsection-title">Volunteering &amp; University Service</h3>
          <div class="service-list">
            <div class="service-item">NeurIPS Logistics Team (2023)</div>
            <div class="service-item">WiML Poster Reviewer, NeurIPS (2023, <a href="https://sites.google.com/wimlworkshop.org/wiml-2024/program#h.1dzx6aq157xv" target="_blank">2024</a>, 2025)</div>
            <div class="service-item">WiML Poster Mentor (2020)</div>
            <div class="service-item">Panelist, "How to make the most of PEARC," PEARC25, Columbus, Ohio (2025)</div>
            <div class="service-item">Graduate &amp; Professional Student Government Representative, UNC Student Technology Council (Fall 2023 &ndash; Spring 2025)</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── SKILLS ── -->
  <section id="skills">
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
  <section class="cta-section" id="contact">
    <div class="section-inner" style="max-width: 640px;">
      <div class="section-label reveal">Get in Touch</div>
      <p class="cta-desc reveal">Application materials including teaching statement, research statement, and complete CV are available upon request.</p>
      <a href="mailto:roolasunkanmi@unc.edu" class="cta-btn reveal">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
        roolasunkanmi@unc.edu
      </a>
    </div>
  </section>

  <!-- ── FOOTER ── -->
  <footer>
    <p>&copy; 2026 Olawumi Roseline Olasunkanmi. Dare to dream.</p>
  </footer>

  <script>
    // Nav scroll effect
    const nav = document.getElementById('nav');
    window.addEventListener('scroll', () => {
      nav.classList.toggle('scrolled', window.scrollY > 20);
    });

    // Mobile menu
    const toggle = document.getElementById('navToggle');
    const navLinks = document.getElementById('navLinks');
    toggle.addEventListener('click', () => {
      navLinks.classList.toggle('open');
    });

    // Close mobile menu on link click
    navLinks.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('open');
      });
    });

    // Scroll spy — highlight active nav link
    const sections = document.querySelectorAll('section[id]');
    const navAnchors = document.querySelectorAll('.nav-links a');

    function updateActiveNav() {
      const scrollY = window.scrollY + 120;
      let currentId = '';

      sections.forEach(section => {
        if (scrollY >= section.offsetTop) {
          currentId = section.getAttribute('id');
        }
      });

      // If at the very top, highlight Home
      if (window.scrollY < 200) currentId = 'hero';

      navAnchors.forEach(a => {
        a.classList.toggle('active', a.getAttribute('href') === '#' + currentId);
      });
    }

    window.addEventListener('scroll', updateActiveNav, { passive: true });
    updateActiveNav();

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
