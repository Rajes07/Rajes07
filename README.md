[index.html](https://github.com/user-attachments/files/29368122/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Rajesh Kumar Mohan — Senior Java Backend Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #1c2330;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #8b949e;
    --accent: #58a6ff;
    --accent2: #1f6feb;
    --green: #3fb950;
    --orange: #d29922;
    --purple: #a371f7;
    --teal: #39d353;
    --mono: 'JetBrains Mono', monospace;
    --sans: 'Inter', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--sans);
    background: var(--bg);
    color: var(--text);
    line-height: 1.7;
    font-size: 15px;
    min-height: 100vh;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(13,17,23,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 2rem; height: 56px;
  }
  .nav-logo {
    font-family: var(--mono);
    font-size: 14px;
    color: var(--accent);
    letter-spacing: 0.02em;
  }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 13px;
    font-weight: 500;
    transition: color 0.2s;
    letter-spacing: 0.04em;
    text-transform: uppercase;
  }
  .nav-links a:hover { color: var(--text); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center; justify-content: center;
    padding: 7rem 2rem 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; bottom: 0;
    background:
      radial-gradient(ellipse 60% 50% at 70% 40%, rgba(31,111,235,0.08) 0%, transparent 70%),
      radial-gradient(ellipse 40% 40% at 20% 70%, rgba(88,166,255,0.05) 0%, transparent 60%);
    pointer-events: none;
  }
  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    max-width: 1100px;
    width: 100%;
    align-items: center;
  }
  .hero-tag {
    font-family: var(--mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1rem;
    display: flex; align-items: center; gap: 8px;
  }
  .hero-tag::before {
    content: ''; display: inline-block;
    width: 24px; height: 1px; background: var(--accent);
  }
  h1 {
    font-size: clamp(2.2rem, 5vw, 3.4rem);
    font-weight: 600;
    line-height: 1.15;
    letter-spacing: -0.02em;
    margin-bottom: 1rem;
  }
  .h1-accent { color: var(--accent); }
  .hero-sub {
    font-size: 15px;
    color: var(--muted);
    max-width: 440px;
    margin-bottom: 2rem;
  }
  .hero-badges {
    display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 2rem;
  }
  .badge {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    background: rgba(88,166,255,0.08);
    border: 1px solid rgba(88,166,255,0.2);
    padding: 4px 10px;
    border-radius: 4px;
    letter-spacing: 0.04em;
  }
  .badge.green { color: var(--green); background: rgba(63,185,80,0.08); border-color: rgba(63,185,80,0.2); }
  .badge.purple { color: var(--purple); background: rgba(163,113,247,0.08); border-color: rgba(163,113,247,0.2); }
  .badge.orange { color: var(--orange); background: rgba(210,153,34,0.08); border-color: rgba(210,153,34,0.2); }

  .cta-group { display: flex; gap: 12px; flex-wrap: wrap; }
  .btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 20px;
    border-radius: 6px;
    font-size: 14px; font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer; border: none;
  }
  .btn-primary {
    background: var(--accent2);
    color: #fff;
  }
  .btn-primary:hover { background: var(--accent); }
  .btn-ghost {
    background: transparent;
    color: var(--text);
    border: 1px solid var(--border);
  }
  .btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

  /* ── TERMINAL CARD ── */
  .terminal {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    font-family: var(--mono);
    font-size: 13px;
  }
  .terminal-bar {
    background: var(--bg3);
    padding: 10px 16px;
    display: flex; align-items: center; gap: 8px;
    border-bottom: 1px solid var(--border);
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-r { background: #ff5f57; }
  .dot-y { background: #ffbd2e; }
  .dot-g { background: #28c840; }
  .terminal-title { font-size: 11px; color: var(--muted); margin-left: 8px; }
  .terminal-body { padding: 20px 24px; }
  .t-line { margin: 4px 0; display: flex; gap: 8px; }
  .t-prompt { color: var(--green); user-select: none; }
  .t-cmd { color: var(--text); }
  .t-out { color: var(--muted); margin-left: 16px; }
  .t-key { color: var(--accent); }
  .t-val { color: var(--purple); }
  .t-str { color: var(--orange); }
  .t-comment { color: #484f58; }
  .t-cursor {
    display: inline-block; width: 8px; height: 14px;
    background: var(--accent); vertical-align: middle;
    animation: blink 1.2s step-end infinite;
  }
  @keyframes blink { 50% { opacity: 0; } }

  /* ── SECTIONS ── */
  section { padding: 80px 2rem; max-width: 1100px; margin: 0 auto; }
  .section-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
  }
  h2 {
    font-size: 1.75rem;
    font-weight: 600;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }
  .section-divider {
    width: 40px; height: 2px;
    background: linear-gradient(90deg, var(--accent), transparent);
    margin-bottom: 3rem;
  }

  /* ── STATS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
    margin-bottom: 3rem;
  }
  .stat-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.25rem 1.5rem;
    text-align: center;
  }
  .stat-num {
    font-size: 2rem; font-weight: 600;
    color: var(--accent);
    font-family: var(--mono);
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-label { font-size: 12px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; }

  /* ── ABOUT ── */
  .about-grid { display: grid; grid-template-columns: 3fr 2fr; gap: 3rem; align-items: start; }
  .about-text p { color: var(--muted); margin-bottom: 1rem; }
  .about-text p strong { color: var(--text); }
  .about-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.5rem;
  }
  .about-card-title { font-size: 12px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 1rem; }
  .info-row { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
  .info-icon { width: 32px; height: 32px; border-radius: 6px; background: rgba(88,166,255,0.1); display: flex; align-items: center; justify-content: center; font-size: 15px; flex-shrink: 0; }
  .info-label { font-size: 11px; color: var(--muted); }
  .info-value { font-size: 13px; color: var(--text); font-weight: 500; }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.25rem;
  }
  .skill-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.25rem 1.5rem;
    transition: border-color 0.2s;
  }
  .skill-card:hover { border-color: var(--accent2); }
  .skill-card-header {
    display: flex; align-items: center; gap: 10px;
    margin-bottom: 1rem;
  }
  .skill-icon { font-size: 20px; }
  .skill-cat { font-size: 12px; font-weight: 600; color: var(--text); text-transform: uppercase; letter-spacing: 0.06em; }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .skill-tag {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    background: var(--bg3);
    border: 1px solid var(--border);
    padding: 3px 8px;
    border-radius: 4px;
  }
  .skill-tag.hot { color: var(--accent); border-color: rgba(88,166,255,0.3); background: rgba(88,166,255,0.06); }

  /* ── EXPERIENCE ── */
  .timeline { position: relative; padding-left: 2rem; }
  .timeline::before {
    content: '';
    position: absolute; left: 0; top: 8px; bottom: 0;
    width: 1px; background: var(--border);
  }
  .exp-item { position: relative; margin-bottom: 3rem; }
  .exp-dot {
    position: absolute; left: -2rem; top: 6px;
    width: 10px; height: 10px;
    border-radius: 50%; border: 2px solid var(--accent);
    background: var(--bg);
    transform: translateX(-4.5px);
  }
  .exp-dot.active { background: var(--accent); }
  .exp-header { margin-bottom: 0.5rem; }
  .exp-role { font-size: 1rem; font-weight: 600; color: var(--text); }
  .exp-meta { font-size: 13px; color: var(--muted); margin-bottom: 0.75rem; }
  .exp-meta span { color: var(--accent); }
  .exp-bullets { list-style: none; }
  .exp-bullets li {
    color: var(--muted);
    font-size: 14px;
    margin-bottom: 8px;
    padding-left: 1.25rem;
    position: relative;
  }
  .exp-bullets li::before {
    content: '▸';
    position: absolute; left: 0;
    color: var(--accent);
    font-size: 10px; top: 4px;
  }
  .exp-bullets li strong { color: var(--text); }

  /* ── PROJECTS ── */
  .projects-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.25rem; }
  .project-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.5rem;
    display: flex; flex-direction: column;
    transition: border-color 0.2s, transform 0.2s;
    position: relative; overflow: hidden;
  }
  .project-card:hover { border-color: var(--accent2); transform: translateY(-2px); }
  .project-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--purple));
    opacity: 0; transition: opacity 0.2s;
  }
  .project-card:hover::before { opacity: 1; }
  .project-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 0.75rem; }
  .project-icon { font-size: 22px; }
  .project-lang {
    font-family: var(--mono);
    font-size: 11px; color: var(--orange);
    display: flex; align-items: center; gap: 6px;
  }
  .lang-dot { width: 10px; height: 10px; border-radius: 50%; background: var(--orange); }
  .project-name { font-size: 15px; font-weight: 600; color: var(--accent); margin-bottom: 0.5rem; }
  .project-desc { font-size: 13px; color: var(--muted); flex: 1; margin-bottom: 1rem; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .project-tag {
    font-family: var(--mono);
    font-size: 11px; color: var(--muted);
    background: var(--bg3);
    border: 1px solid var(--border);
    padding: 2px 8px; border-radius: 4px;
  }

  /* ── GITHUB README ── */
  .readme-box {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
  }
  .readme-topbar {
    background: var(--bg3);
    border-bottom: 1px solid var(--border);
    padding: 10px 16px;
    display: flex; align-items: center; gap: 8px;
    font-family: var(--mono);
    font-size: 12px; color: var(--muted);
  }
  .readme-body { padding: 2rem; }
  .readme-body pre {
    font-family: var(--mono);
    font-size: 12.5px;
    line-height: 1.8;
    color: var(--muted);
    white-space: pre-wrap;
    overflow-x: auto;
  }
  .readme-body pre .md-h1 { color: var(--text); font-weight: 600; font-size: 16px; }
  .readme-body pre .md-h2 { color: var(--text); font-weight: 600; }
  .readme-body pre .md-link { color: var(--accent); }
  .readme-body pre .md-bold { color: var(--text); font-weight: 600; }
  .readme-body pre .md-badge { color: var(--green); }
  .copy-btn {
    margin-top: 1rem;
    display: inline-flex; align-items: center; gap: 8px;
    padding: 8px 16px;
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 6px;
    color: var(--muted);
    font-size: 13px; cursor: pointer;
    transition: all 0.2s; font-family: var(--sans);
  }
  .copy-btn:hover { border-color: var(--accent); color: var(--accent); }

  /* ── CONTACT ── */
  .contact-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; }
  .contact-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.5rem;
    text-align: center;
    text-decoration: none;
    transition: all 0.2s;
    display: block;
  }
  .contact-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .contact-icon { font-size: 28px; margin-bottom: 0.75rem; }
  .contact-label { font-size: 12px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 4px; }
  .contact-value { font-size: 13px; color: var(--accent); font-family: var(--mono); }

  /* ── FOOTER ── */
  footer {
    border-top: 1px solid var(--border);
    padding: 2rem;
    text-align: center;
    color: var(--muted);
    font-size: 13px;
    font-family: var(--mono);
  }

  /* ── CONTRIB GRAPH ── */
  .contrib-section { margin-top: 2rem; }
  .contrib-graph {
    display: flex; gap: 3px; flex-wrap: nowrap; overflow: hidden;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.5rem;
  }
  .contrib-col { display: flex; flex-direction: column; gap: 3px; }
  .contrib-cell {
    width: 11px; height: 11px; border-radius: 2px;
  }
  .c0 { background: var(--bg3); }
  .c1 { background: #0e4429; }
  .c2 { background: #006d32; }
  .c3 { background: #26a641; }
  .c4 { background: #39d353; }
  .contrib-label {
    font-family: var(--mono);
    font-size: 11px; color: var(--muted);
    margin-bottom: 0.75rem;
  }

  /* ── SCROLL INDICATOR ── */
  .scroll-hint {
    position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 8px;
    color: var(--muted); font-size: 11px; letter-spacing: 0.1em;
    text-transform: uppercase; animation: fadeUpDown 2s ease-in-out infinite;
  }
  .scroll-arrow { width: 1px; height: 40px; background: linear-gradient(to bottom, var(--accent), transparent); }
  @keyframes fadeUpDown { 0%,100% { opacity:0.4; transform:translateX(-50%) translateY(0); } 50% { opacity:1; transform:translateX(-50%) translateY(6px); } }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .hero-grid { grid-template-columns: 1fr; gap: 2rem; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .about-grid { grid-template-columns: 1fr; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .projects-grid { grid-template-columns: 1fr; }
    .contact-grid { grid-template-columns: 1fr; }
    .nav-links { display: none; }
  }

  /* ── ACTIVE NAV ── */
  .pill-status {
    display: inline-flex; align-items: center; gap: 6px;
    background: rgba(63,185,80,0.1);
    border: 1px solid rgba(63,185,80,0.25);
    border-radius: 20px;
    padding: 3px 10px;
    font-size: 12px; color: var(--green);
    font-family: var(--mono);
  }
  .status-dot {
    width: 7px; height: 7px; border-radius: 50%;
    background: var(--green);
    animation: pulse 2s ease infinite;
  }
  @keyframes pulse { 0%,100% { opacity:1; } 50% { opacity:0.4; } }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">rajesh.kumar.mohan</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#readme">README</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-grid">
    <div>
      <div class="hero-tag">Senior Software Engineer</div>
      <h1>Rajesh<br/><span class="h1-accent">Kumar Mohan</span></h1>
      <p class="hero-sub">Java Backend Engineer with 5 years building production-grade distributed systems in Healthcare/Medicaid (MMIS). Spring Boot · Kafka · Microservices · AWS.</p>
      <div class="hero-badges">
        <span class="badge">Java 8–21</span>
        <span class="badge">Spring Boot</span>
        <span class="badge green">Kafka</span>
        <span class="badge purple">Microservices</span>
        <span class="badge orange">AWS</span>
        <span class="badge">Kubernetes</span>
        <span class="badge green">Docker</span>
      </div>
      <div class="cta-group">
        <a href="mailto:hrajes57@gmail.com" class="btn btn-primary">📬 Hire Me</a>
        <a href="#experience" class="btn btn-ghost">View Experience →</a>
        <a href="https://github.com/Rajes07" class="btn btn-ghost" target="_blank">GitHub ↗</a>
      </div>
    </div>

    <!-- Terminal -->
    <div class="terminal">
      <div class="terminal-bar">
        <div class="dot dot-r"></div>
        <div class="dot dot-y"></div>
        <div class="dot dot-g"></div>
        <div class="terminal-title">~/rajesh — zsh</div>
      </div>
      <div class="terminal-body">
        <div class="t-line"><span class="t-prompt">❯</span><span class="t-cmd">cat profile.json</span></div>
        <div class="t-line"><span class="t-out">{</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"name"</span>: <span class="t-str">"Rajesh Kumar Mohan"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"role"</span>: <span class="t-str">"Senior Software Engineer"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"experience"</span>: <span class="t-val">5</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"domain"</span>: <span class="t-str">"Healthcare / MMIS"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"stack"</span>: [<span class="t-str">"Java"</span>, <span class="t-str">"Spring Boot"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"Kafka"</span>, <span class="t-str">"AWS"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"Kubernetes"</span>, <span class="t-str">"Docker"</span>],</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"open_to"</span>: <span class="t-str">"Senior / Lead Backend Roles"</span>,</span></div>
        <div class="t-line"><span class="t-out">&nbsp;&nbsp;<span class="t-key">"available"</span>: <span class="t-val">true</span></span></div>
        <div class="t-line"><span class="t-out">}</span></div>
        <div class="t-line" style="margin-top:12px"><span class="t-prompt">❯</span>&nbsp;<span class="t-cursor"></span></div>
      </div>
    </div>
  </div>
  <div class="scroll-hint">
    <div class="scroll-arrow"></div>
    scroll
  </div>
</div>

<!-- STATS -->
<section style="padding-top: 2rem; padding-bottom: 2rem;">
  <div class="stats-row">
    <div class="stat-card">
      <div class="stat-num">5+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">40%</div>
      <div class="stat-label">Overhead Reduced</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">99.9%</div>
      <div class="stat-label">Uptime SLA</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">5K+</div>
      <div class="stat-label">Daily Sessions Served</div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">// about me</div>
  <h2>Crafting Reliable Backend Systems</h2>
  <div class="section-divider"></div>
  <div class="about-grid">
    <div class="about-text">
      <p>
        I'm a <strong>Senior Software Engineer at Infinite Computer Solutions</strong>, Chennai, with 5 years
        of hands-on experience building and maintaining mission-critical Java backend systems
        in the <strong>Healthcare / Medicaid (MMIS)</strong> domain.
      </p>
      <p>
        My work spans the full backend lifecycle — from <strong>architecting Spring Boot microservices</strong> and
        building <strong>event-driven Kafka pipelines</strong> to optimizing Oracle SQL queries that run
        at peak enrollment scale. I've led production support for systems serving
        <strong>5,000+ daily sessions with 99.9% uptime</strong>.
      </p>
      <p>
        I'm deeply focused on <strong>JVM internals, concurrency, and distributed system design</strong> —
        and I apply SOLID principles, TDD, and design patterns not as buzzwords but as daily tools.
        I hold an <strong>ICT Cloud Solution Architect certification</strong> and actively explore
        Spring AI integrations with GPT-4 and Anthropic Claude.
      </p>
      <p>
        Currently open to <strong>Senior Java Backend / Lead Engineer roles</strong> where I can drive
        architectural decisions and deliver measurable impact.
      </p>
      <div style="margin-top: 1.5rem;">
        <span class="pill-status"><span class="status-dot"></span>Open to opportunities</span>
      </div>
    </div>
    <div class="about-card">
      <div class="about-card-title">Quick Info</div>
      <div class="info-row">
        <div class="info-icon">🏢</div>
        <div><div class="info-label">Company</div><div class="info-value">Infinite Computer Solutions</div></div>
      </div>
      <div class="info-row">
        <div class="info-icon">📍</div>
        <div><div class="info-label">Location</div><div class="info-value">Chennai, India</div></div>
      </div>
      <div class="info-row">
        <div class="info-icon">🎓</div>
        <div><div class="info-label">Education</div><div class="info-value">BCA — Gurunanak College (9.1 CGPA)</div></div>
      </div>
      <div class="info-row">
        <div class="info-icon">🏥</div>
        <div><div class="info-label">Domain</div><div class="info-value">Healthcare · MMIS · Medicaid</div></div>
      </div>
      <div class="info-row">
        <div class="info-icon">☕</div>
        <div><div class="info-label">Primary Stack</div><div class="info-value">Java · Spring Boot · Kafka</div></div>
      </div>
      <div class="info-row">
        <div class="info-icon">📜</div>
        <div><div class="info-label">Certification</div><div class="info-value">ICT Cloud Solution Architect</div></div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills" style="background: var(--bg2); max-width: 100%; border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);">
  <div style="max-width: 1100px; margin: 0 auto;">
    <div class="section-label">// tech stack</div>
    <h2>Skills &amp; Technologies</h2>
    <div class="section-divider"></div>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">☕</span><span class="skill-cat">Core Java</span></div>
        <div class="skill-tags">
          <span class="skill-tag hot">Java 8–21</span>
          <span class="skill-tag hot">Streams &amp; Lambdas</span>
          <span class="skill-tag">Concurrency</span>
          <span class="skill-tag">JVM Internals</span>
          <span class="skill-tag">Virtual Threads</span>
          <span class="skill-tag">DSA</span>
          <span class="skill-tag">OOD / SOLID</span>
          <span class="skill-tag">Design Patterns</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">🌱</span><span class="skill-cat">Spring Ecosystem</span></div>
        <div class="skill-tags">
          <span class="skill-tag hot">Spring Boot</span>
          <span class="skill-tag hot">Spring MVC</span>
          <span class="skill-tag">Spring Data JPA</span>
          <span class="skill-tag">Spring Security</span>
          <span class="skill-tag">Spring AI</span>
          <span class="skill-tag">Hibernate</span>
          <span class="skill-tag">OAuth2 / JWT</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">🏗️</span><span class="skill-cat">Architecture</span></div>
        <div class="skill-tags">
          <span class="skill-tag hot">Microservices</span>
          <span class="skill-tag hot">Event-Driven (Kafka)</span>
          <span class="skill-tag">RESTful APIs</span>
          <span class="skill-tag">SOAP / Web Services</span>
          <span class="skill-tag">HLD / LLD</span>
          <span class="skill-tag">Distributed Systems</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">☁️</span><span class="skill-cat">Cloud &amp; DevOps</span></div>
        <div class="skill-tags">
          <span class="skill-tag hot">AWS (EC2, S3, CloudWatch)</span>
          <span class="skill-tag hot">Docker</span>
          <span class="skill-tag">Kubernetes</span>
          <span class="skill-tag">Jenkins</span>
          <span class="skill-tag">GitHub Actions</span>
          <span class="skill-tag">CI/CD</span>
          <span class="skill-tag">Maven / Gradle</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">🗄️</span><span class="skill-cat">Databases</span></div>
        <div class="skill-tags">
          <span class="skill-tag hot">Oracle SQL</span>
          <span class="skill-tag">PostgreSQL</span>
          <span class="skill-tag">MySQL</span>
          <span class="skill-tag">MongoDB</span>
          <span class="skill-tag">Redis</span>
          <span class="skill-tag">Query Tuning</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-header"><span class="skill-icon">📊</span><span class="skill-cat">Observability &amp; Testing</span></div>
        <div class="skill-tags">
          <span class="skill-tag">Prometheus</span>
          <span class="skill-tag">Grafana</span>
          <span class="skill-tag">ELK Stack</span>
          <span class="skill-tag">Splunk</span>
          <span class="skill-tag hot">JUnit / Mockito</span>
          <span class="skill-tag">TDD / BDD</span>
          <span class="skill-tag">SonarQube</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">// work history</div>
  <h2>Experience</h2>
  <div class="section-divider"></div>
  <div class="timeline">

    <div class="exp-item">
      <div class="exp-dot active"></div>
      <div class="exp-header">
        <div class="exp-role">Senior Software Engineer</div>
        <div class="exp-meta">Infinite Computer Solutions &nbsp;·&nbsp; <span>Apr 2025 – Present</span> &nbsp;·&nbsp; Chennai</div>
      </div>
      <ul class="exp-bullets">
        <li>Architected end-to-end <strong>OpenText xPression integration</strong> via Spring Boot SOAP handler — automated letter generation, reducing caseworker overhead by <strong>40%</strong>.</li>
        <li>Engineered <strong>DocFinity REST API layer</strong> for metadata search and inline document rendering, supporting <strong>5,000+ daily sessions</strong> with zero production downtime.</li>
        <li>Reduced response latency by <strong>25%</strong> on high-traffic MMIS portal endpoints through query tuning and Spring Boot service refactoring.</li>
        <li>Led <strong>L3 production support &amp; incident response</strong>, consistently resolving P1 tickets within 24-hour SLA windows — maintaining 99.9% availability.</li>
      </ul>
    </div>

    <div class="exp-item">
      <div class="exp-dot"></div>
      <div class="exp-header">
        <div class="exp-role">Software Engineer</div>
        <div class="exp-meta">Infinite Computer Solutions &nbsp;·&nbsp; <span>Apr 2023 – Apr 2025</span> &nbsp;·&nbsp; Chennai</div>
      </div>
      <ul class="exp-bullets">
        <li>Led enterprise-wide <strong>Java 8 migration</strong> for TSU project — refactored <strong>200+ classes</strong> using Streams and Lambdas, reducing technical debt by 30%.</li>
        <li>Orchestrated complex <strong>Medicaid business workflows</strong> using IBM BPEL, integrating <strong>12+ service components</strong> into reliable transaction chains.</li>
        <li>Automated deployment pipelines via <strong>C#/.NET utilities and Shell scripts</strong> — saved engineering team <strong>10+ hours/week</strong>.</li>
        <li>Standardized API docs with <strong>Swagger/OpenAPI</strong>, reducing cross-team integration friction by 20%.</li>
      </ul>
    </div>

    <div class="exp-item">
      <div class="exp-dot"></div>
      <div class="exp-header">
        <div class="exp-role">Associate Software Engineer</div>
        <div class="exp-meta">Infinite Computer Solutions &nbsp;·&nbsp; <span>Oct 2021 – Apr 2023</span> &nbsp;·&nbsp; Bangalore</div>
      </div>
      <ul class="exp-bullets">
        <li>Modernized <strong>legacy J2EE modules</strong> (JSP/JSF/EJB), resolving 50+ critical production defects in the MMIS portal.</li>
        <li>Tuned Oracle SQL for high-volume enrollment — reduced DB CPU utilization by <strong>20%</strong> during peak periods.</li>
        <li>Authored <strong>15+ LLD technical design docs</strong> that became the foundation for the Spring Boot modernization roadmap.</li>
      </ul>
    </div>

    <div class="exp-item">
      <div class="exp-dot"></div>
      <div class="exp-header">
        <div class="exp-role">Graduate Trainee</div>
        <div class="exp-meta">Infinite Computer Solutions &nbsp;·&nbsp; <span>Jul 2021 – Oct 2021</span> &nbsp;·&nbsp; Chennai</div>
      </div>
      <ul class="exp-bullets">
        <li>Intensive full-stack training in <strong>Core Java, Spring Framework, and Oracle DB</strong> — graduated in the <strong>top 5%</strong> of the cohort.</li>
      </ul>
    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" style="background: var(--bg2); max-width: 100%; border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);">
  <div style="max-width: 1100px; margin: 0 auto;">
    <div class="section-label">// featured work</div>
    <h2>Projects &amp; Contributions</h2>
    <div class="section-divider"></div>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-top">
          <span class="project-icon">🏥</span>
          <span class="project-lang"><span class="lang-dot"></span>Java</span>
        </div>
        <div class="project-name">MMIS Medicaid Portal — Spring Boot Modernization</div>
        <div class="project-desc">Led end-to-end refactor of legacy J2EE MMIS portal to Spring Boot microservices. Improved performance, maintainability, and introduced CI/CD pipelines. Handles eligibility, enrollment, and claims workflows for Medicaid members.</div>
        <div class="project-tags">
          <span class="project-tag">Spring Boot</span>
          <span class="project-tag">Oracle SQL</span>
          <span class="project-tag">IBM BPEL</span>
          <span class="project-tag">Microservices</span>
          <span class="project-tag">Maven</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-top">
          <span class="project-icon">📄</span>
          <span class="project-lang"><span class="lang-dot"></span>Java</span>
        </div>
        <div class="project-name">OpenText xPression — Automated Letter Generation</div>
        <div class="project-desc">Architected Spring Boot SOAP integration with OpenText xPression for automated caseworker letter generation. Reduced manual overhead by 40% across Medicaid operations. Zero-downtime deployment with 99.9% SLA.</div>
        <div class="project-tags">
          <span class="project-tag">Spring Boot</span>
          <span class="project-tag">SOAP</span>
          <span class="project-tag">IBM WebSphere</span>
          <span class="project-tag">OpenText</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-top">
          <span class="project-icon">🔍</span>
          <span class="project-lang"><span class="lang-dot" style="background:var(--purple)"></span>Java</span>
        </div>
        <div class="project-name">DocFinity REST API — Document Management Layer</div>
        <div class="project-desc">Built high-performance document metadata search and inline rendering REST API layer using DocFinity integration. Serves 5,000+ daily sessions. Custom Java user-exit utilities resolved complex Medicaid logic gaps, cutting document errors by 15%.</div>
        <div class="project-tags">
          <span class="project-tag">REST API</span>
          <span class="project-tag">Spring Boot</span>
          <span class="project-tag">DocFinity</span>
          <span class="project-tag">Java</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-top">
          <span class="project-icon">🤖</span>
          <span class="project-lang"><span class="lang-dot" style="background:var(--green)"></span>Java</span>
        </div>
        <div class="project-name">Spring AI — GenAI Integration (Learning Project)</div>
        <div class="project-desc">Exploring Spring AI integrations with OpenAI GPT-4/4o and Anthropic Claude for intelligent document classification and query automation in healthcare data workflows. Prompt engineering for structured JSON extraction from clinical text.</div>
        <div class="project-tags">
          <span class="project-tag">Spring AI</span>
          <span class="project-tag">GPT-4</span>
          <span class="project-tag">Anthropic Claude</span>
          <span class="project-tag">Prompt Engineering</span>
        </div>
      </div>

    </div>

    <!-- Contribution Graph -->
    <div class="contrib-section">
      <div class="contrib-label">Simulated activity heatmap — Replace with GitHub Readme Stats widget</div>
      <div class="contrib-graph" id="contribGraph"></div>
    </div>
  </div>
</section>

<!-- GITHUB README -->
<section id="readme">
  <div class="section-label">// github profile</div>
  <h2>Profile README.md</h2>
  <div class="section-divider"></div>
  <p style="color: var(--muted); margin-bottom: 1.5rem; font-size: 14px;">Copy this into your <code style="font-family: var(--mono); font-size: 12px; background: var(--bg2); padding: 2px 6px; border-radius: 4px; border: 1px solid var(--border);">Rajes07/Rajes07</code> repository's README.md to transform your GitHub profile.</p>
  <div class="readme-box">
    <div class="readme-topbar">
      📄 README.md &nbsp;·&nbsp; Rajes07/Rajes07
    </div>
    <div class="readme-body">
      <pre id="readmeContent">
<span class="md-h1"># Hi, I'm Rajesh Kumar Mohan 👋</span>

<span class="md-badge">![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=58A6FF&width=500&lines=Senior+Java+Backend+Engineer;Spring+Boot+%7C+Kafka+%7C+Microservices;Healthcare+%2F+MMIS+Domain+Expert;5%2B+Years+of+Production+Experience)</span>

<span class="md-bold">**Senior Software Engineer** at Infinite Computer Solutions, Chennai</span>
Building reliable, high-performance Java backend systems in the Healthcare/Medicaid domain.

---

<span class="md-h2">## 🚀 About Me</span>

- 🏥 5+ years building **MMIS (Medicaid Management Information System)** platforms
- ⚡ Architected systems serving **5,000+ daily sessions** with **99.9% uptime**
- 🔧 Led Java 8 migration refactoring **200+ classes** — reduced tech debt by 30%
- 📄 Integrated OpenText xPression, reducing caseworker overhead by **40%**
- 🤖 Exploring **Spring AI** with GPT-4 and Anthropic Claude
- 📜 ICT **Cloud Solution Architect** certified

---

<span class="md-h2">## 🛠️ Tech Stack</span>

<span class="md-badge">![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)</span>
<span class="md-badge">![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)</span>
<span class="md-badge">![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white)</span>
<span class="md-badge">![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)</span>
<span class="md-badge">![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)</span>
<span class="md-badge">![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)</span>
<span class="md-badge">![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)</span>
<span class="md-badge">![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)</span>

---

<span class="md-h2">## 📊 GitHub Stats</span>

![Rajesh's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Rajes07&show_icons=true&theme=github_dark&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Rajes07&layout=compact&theme=github_dark&hide_border=true)

---

<span class="md-h2">## 🏆 Highlights</span>

| Metric | Impact |
|--------|--------|
| 🎯 Latency Reduction | 25% on high-traffic MMIS endpoints |
| 📄 Letter Automation | 40% reduction in manual overhead |
| 🔄 Classes Refactored | 200+ during Java 8 migration |
| ⏱️ Time Saved | 10+ hrs/week via automation scripts |
| 🔒 Uptime | 99.9% SLA maintained |

---

<span class="md-h2">## 📫 Connect</span>

<span class="md-link">[![Email](https://img.shields.io/badge/hrajes57@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:hrajes57@gmail.com)</span>
<span class="md-link">[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)</span>
<span class="md-link">[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=black)](https://leetcode.com/YOUR_HANDLE)</span>

---
<span style="color: #484f58">⭐ Open to Senior Java Backend / Lead Engineer roles · Chennai or Remote</span>
      </pre>
      <button class="copy-btn" onclick="copyReadme()">📋 Copy README to clipboard</button>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">// get in touch</div>
  <h2>Contact</h2>
  <div class="section-divider"></div>
  <p style="color: var(--muted); margin-bottom: 2rem;">Open to Senior Java Backend and Lead Engineer roles. Let's build something production-grade.</p>
  <div class="contact-grid">
    <a href="mailto:hrajes57@gmail.com" class="contact-card">
      <div class="contact-icon">📬</div>
      <div class="contact-label">Email</div>
      <div class="contact-value">hrajes57@gmail.com</div>
    </a>
    <a href="https://github.com/Rajes07" target="_blank" class="contact-card">
      <div class="contact-icon">🐙</div>
      <div class="contact-label">GitHub</div>
      <div class="contact-value">github.com/Rajes07</div>
    </a>
    <a href="tel:+917358470999" class="contact-card">
      <div class="contact-icon">📱</div>
      <div class="contact-label">Phone</div>
      <div class="contact-value">+91 7358470999</div>
    </a>
  </div>
</section>

<footer>
  <span style="color: var(--accent)">Rajesh Kumar Mohan</span> &nbsp;·&nbsp; Senior Software Engineer &nbsp;·&nbsp; Chennai, India &nbsp;·&nbsp; Built with ❤️ &amp; Java
</footer>

<script>
// Generate contribution graph
const graph = document.getElementById('contribGraph');
const levels = [0,0,0,1,1,2,2,3,4,3,2,1,2,3,4,4,3,2,1,0,1,2,3,4,3,2,3,4,4,3,2,1,0,0,1,2,3,4,3,2,1,2,3,4,3,2,1,0,1,2,2];
for(let w=0; w<52; w++) {
  const col = document.createElement('div');
  col.className = 'contrib-col';
  for(let d=0; d<7; d++) {
    const cell = document.createElement('div');
    const lvl = levels[Math.floor(Math.random()*levels.length)];
    cell.className = 'contrib-cell c' + lvl;
    col.appendChild(cell);
  }
  graph.appendChild(col);
}

// Copy README
function copyReadme() {
  const el = document.getElementById('readmeContent');
  const text = el.innerText;
  navigator.clipboard.writeText(text).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ Copied!';
    setTimeout(() => btn.innerHTML = '📋 Copy README to clipboard', 2000);
  });
}
</script>
</body>
</html>
