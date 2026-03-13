<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vicky Khanna — AI & Automation Expert</title>
<link href="https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&family=Cabinet+Grotesk:wght@300;400;500;700;800&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
/* ─── RESET & VARIABLES ─────────────────────────────────────────── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

:root {
  --bg:       #04040a;
  --surface:  #08080f;
  --panel:    #0e0e1a;
  --border:   #16162a;
  --border2:  #1e1e35;
  --accent1:  #00f0c8;   /* teal/mint */
  --accent2:  #ff4d6d;   /* coral red */
  --accent3:  #7b61ff;   /* electric violet */
  --text:     #d8d8ee;
  --muted:    #6060a0;
  --white:    #ffffff;
  --font-display: 'Cabinet Grotesk', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-display);
  line-height: 1.6;
  overflow-x: hidden;
  cursor: none;
}

/* ─── CUSTOM CURSOR ─────────────────────────────────────────────── */
.cursor {
  position: fixed; width: 12px; height: 12px;
  background: var(--accent1); border-radius: 50%;
  pointer-events: none; z-index: 9999;
  transform: translate(-50%, -50%);
  transition: transform 0.1s, width 0.2s, height 0.2s, opacity 0.2s;
  mix-blend-mode: screen;
}
.cursor-ring {
  position: fixed; width: 36px; height: 36px;
  border: 1px solid rgba(0,240,200,0.4); border-radius: 50%;
  pointer-events: none; z-index: 9998;
  transform: translate(-50%, -50%);
  transition: transform 0.15s ease, width 0.3s, height 0.3s, border-color 0.3s;
}

/* ─── BACKGROUND NOISE ──────────────────────────────────────────── */
body::before {
  content: '';
  position: fixed; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events: none; z-index: 0; opacity: 0.6;
}

/* ─── NAV ────────────────────────────────────────────────────────── */
nav {
  position: fixed; top: 0; left: 0; right: 0;
  z-index: 100;
  padding: 20px 60px;
  display: flex; align-items: center; justify-content: space-between;
  background: rgba(4,4,10,0.85);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: var(--font-mono);
  font-size: 13px; font-weight: 500;
  color: var(--accent1);
  letter-spacing: 0.06em;
  text-decoration: none;
}
.nav-logo span { color: var(--muted); }
.nav-links {
  display: flex; gap: 36px; list-style: none;
}
.nav-links a {
  font-size: 12px; font-weight: 500;
  color: var(--muted); text-decoration: none;
  letter-spacing: 0.1em; text-transform: uppercase;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--white); }
.nav-cta {
  font-family: var(--font-mono);
  font-size: 11px; font-weight: 500;
  color: var(--bg);
  background: var(--accent1);
  border: none; border-radius: 6px;
  padding: 9px 20px;
  cursor: none; text-decoration: none;
  letter-spacing: 0.06em;
  transition: opacity 0.2s, transform 0.2s;
}
.nav-cta:hover { opacity: 0.85; transform: translateY(-1px); }

/* ─── HERO ────────────────────────────────────────────────────────── */
#hero {
  position: relative;
  min-height: 100vh;
  display: flex; align-items: center;
  padding: 120px 60px 80px;
  overflow: hidden;
}

/* Hero grid lines */
#hero::before {
  content: '';
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(0,240,200,0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,240,200,0.03) 1px, transparent 1px);
  background-size: 64px 64px;
}

/* Big orbs */
.hero-orb {
  position: absolute; border-radius: 50%;
  filter: blur(120px); pointer-events: none;
}
.hero-orb-1 { width: 600px; height: 600px; background: rgba(0,240,200,0.12); top: -100px; right: -100px; animation: floatOrb 10s ease-in-out infinite; }
.hero-orb-2 { width: 400px; height: 400px; background: rgba(123,97,255,0.15); bottom: -50px; left: 100px; animation: floatOrb 14s ease-in-out infinite reverse; }
.hero-orb-3 { width: 300px; height: 300px; background: rgba(255,77,109,0.08); top: 40%; right: 25%; animation: floatOrb 8s ease-in-out infinite 3s; }

@keyframes floatOrb {
  0%,100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-30px) scale(1.04); }
}

.hero-content { position: relative; z-index: 2; max-width: 720px; }

.hero-badge {
  display: inline-flex; align-items: center; gap: 8px;
  border: 1px solid rgba(0,240,200,0.25);
  background: rgba(0,240,200,0.05);
  border-radius: 100px;
  padding: 6px 16px;
  font-family: var(--font-mono);
  font-size: 11px; color: var(--accent1);
  letter-spacing: 0.1em; text-transform: uppercase;
  margin-bottom: 32px;
  animation: fadeUp 0.8s 0.1s both;
}
.badge-pulse {
  width: 7px; height: 7px; border-radius: 50%;
  background: var(--accent1);
  animation: pulse 2s ease infinite;
}
@keyframes pulse { 0%,100%{opacity:1;transform:scale(1)}50%{opacity:0.3;transform:scale(0.6)} }

.hero-title {
  font-size: clamp(52px, 7vw, 88px);
  font-weight: 800; line-height: 0.95;
  color: var(--white);
  letter-spacing: -0.03em;
  margin-bottom: 12px;
  animation: fadeUp 0.8s 0.2s both;
}
.hero-title .line2 {
  background: linear-gradient(90deg, var(--accent1), var(--accent3));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  background-clip: text;
}
.hero-title .line3 { color: var(--muted); font-weight: 300; }

.hero-sub {
  font-size: 17px; color: var(--muted); font-weight: 400;
  max-width: 520px; line-height: 1.7;
  margin: 24px 0 40px;
  animation: fadeUp 0.8s 0.35s both;
}
.hero-sub strong { color: var(--text); font-weight: 500; }

.hero-actions {
  display: flex; gap: 16px; flex-wrap: wrap;
  animation: fadeUp 0.8s 0.45s both;
}
.btn-primary {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--accent1); color: var(--bg);
  font-family: var(--font-mono); font-size: 12px; font-weight: 600;
  letter-spacing: 0.06em; text-transform: uppercase;
  padding: 14px 28px; border-radius: 8px; text-decoration: none;
  transition: all 0.25s; border: none; cursor: none;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 12px 40px rgba(0,240,200,0.3); }
.btn-secondary {
  display: inline-flex; align-items: center; gap: 10px;
  background: transparent; color: var(--text);
  font-family: var(--font-mono); font-size: 12px; font-weight: 500;
  letter-spacing: 0.06em; text-transform: uppercase;
  padding: 14px 28px; border-radius: 8px; text-decoration: none;
  border: 1px solid var(--border2); transition: all 0.25s; cursor: none;
}
.btn-secondary:hover { border-color: var(--accent1); color: var(--accent1); }

/* Hero stats */
.hero-stats {
  display: flex; gap: 48px; margin-top: 64px;
  animation: fadeUp 0.8s 0.55s both;
}
.stat-item {}
.stat-num {
  font-family: var(--font-mono); font-size: 28px; font-weight: 500;
  color: var(--white); display: block;
}
.stat-num .accent { color: var(--accent1); }
.stat-label {
  font-size: 11px; color: var(--muted);
  letter-spacing: 0.1em; text-transform: uppercase;
  margin-top: 2px; display: block;
}

/* Floating Instagram mockup */
.hero-visual {
  position: absolute; right: 60px; top: 50%;
  transform: translateY(-50%);
  z-index: 2;
  animation: fadeUp 0.9s 0.6s both;
}
.phone-frame {
  width: 240px;
  background: var(--panel);
  border: 1px solid var(--border2);
  border-radius: 28px;
  overflow: hidden;
  box-shadow:
    0 0 0 1px rgba(0,240,200,0.08),
    0 40px 100px rgba(0,0,0,0.8),
    0 0 60px rgba(0,240,200,0.06);
}
.phone-header {
  background: var(--surface);
  padding: 14px 16px 10px;
  display: flex; align-items: center; gap: 10px;
  border-bottom: 1px solid var(--border);
}
.phone-avatar {
  width: 36px; height: 36px; border-radius: 50%;
  background: linear-gradient(135deg, var(--accent1), var(--accent3));
  display: flex; align-items: center; justify-content: center;
  font-size: 13px; font-weight: 800; color: var(--bg);
  flex-shrink: 0;
}
.phone-info { flex: 1; }
.phone-name { font-size: 12px; font-weight: 700; color: var(--white); }
.phone-handle { font-size: 10px; color: var(--muted); font-family: var(--font-mono); }
.phone-follow {
  font-size: 10px; font-weight: 600; color: var(--bg);
  background: var(--accent1); border-radius: 4px; padding: 4px 10px;
  font-family: var(--font-mono);
}
.phone-body { padding: 14px; display: flex; flex-direction: column; gap: 10px; }
.phone-post {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px; padding: 12px;
}
.post-line { height: 7px; background: var(--border2); border-radius: 4px; margin-bottom: 6px; }
.post-line.w60 { width: 60%; }
.post-line.w80 { width: 80%; }
.post-line.w45 { width: 45%; }
.post-tag {
  display: inline-block;
  background: rgba(0,240,200,0.1); border-radius: 4px;
  padding: 3px 8px; font-size: 9px; color: var(--accent1);
  font-family: var(--font-mono); letter-spacing: 0.06em;
  margin-bottom: 6px;
}
.phone-metrics {
  display: flex; gap: 8px; padding: 8px 0 0;
  font-size: 9px; color: var(--muted); font-family: var(--font-mono);
}
.metric span { color: var(--accent1); }

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ─── SECTION BASE ─────────────────────────────────────────────── */
section { position: relative; z-index: 1; }
.section-inner { max-width: 1200px; margin: 0 auto; padding: 0 60px; }
.section-tag {
  display: inline-flex; align-items: center; gap: 8px;
  font-family: var(--font-mono); font-size: 10px;
  color: var(--accent1); letter-spacing: 0.15em; text-transform: uppercase;
  margin-bottom: 16px;
}
.section-tag::before {
  content: ''; width: 24px; height: 1px; background: var(--accent1);
}
.section-title {
  font-size: clamp(32px, 4vw, 48px); font-weight: 800;
  color: var(--white); letter-spacing: -0.02em;
  line-height: 1.1; margin-bottom: 16px;
}
.section-sub { font-size: 16px; color: var(--muted); max-width: 540px; line-height: 1.7; }

/* ─── TOPICS SECTION ────────────────────────────────────────────── */
#topics { padding: 100px 0; }
.topics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 16px; margin-top: 56px;
}
.topic-card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 24px;
  position: relative; overflow: hidden;
  transition: all 0.3s; cursor: default;
}
.topic-card::before {
  content: ''; position: absolute;
  inset: 0; opacity: 0;
  background: linear-gradient(135deg, rgba(0,240,200,0.05), transparent);
  transition: opacity 0.3s;
}
.topic-card:hover { border-color: rgba(0,240,200,0.2); transform: translateY(-4px); box-shadow: 0 20px 60px rgba(0,0,0,0.5); }
.topic-card:hover::before { opacity: 1; }
.topic-icon {
  width: 44px; height: 44px; border-radius: 10px;
  background: rgba(0,240,200,0.08);
  border: 1px solid rgba(0,240,200,0.15);
  display: flex; align-items: center; justify-content: center;
  font-size: 20px; margin-bottom: 16px;
}
.topic-name {
  font-size: 15px; font-weight: 700; color: var(--white);
  margin-bottom: 6px;
}
.topic-desc { font-size: 12px; color: var(--muted); line-height: 1.6; }
.topic-badge {
  position: absolute; top: 16px; right: 16px;
  font-size: 9px; font-family: var(--font-mono);
  color: var(--accent1); background: rgba(0,240,200,0.08);
  border: 1px solid rgba(0,240,200,0.15);
  border-radius: 4px; padding: 3px 8px; letter-spacing: 0.08em;
}

/* ─── CONTENT PILLARS ───────────────────────────────────────────── */
#pillars { padding: 100px 0; background: var(--surface); }
.pillars-grid {
  display: grid; grid-template-columns: repeat(4, 1fr);
  gap: 2px; margin-top: 56px;
  border-radius: 16px; overflow: hidden;
  border: 1px solid var(--border);
}
.pillar {
  background: var(--panel); padding: 36px 28px;
  transition: background 0.3s;
  position: relative;
}
.pillar:hover { background: #111128; }
.pillar-num {
  font-family: var(--font-mono); font-size: 11px;
  color: var(--border2); font-weight: 400;
  margin-bottom: 20px; letter-spacing: 0.1em;
}
.pillar-icon { font-size: 32px; margin-bottom: 16px; display: block; }
.pillar-title {
  font-size: 18px; font-weight: 800; color: var(--white);
  margin-bottom: 10px;
}
.pillar-desc { font-size: 13px; color: var(--muted); line-height: 1.7; }
.pillar-example {
  margin-top: 16px;
  font-size: 11px; font-family: var(--font-mono);
  color: var(--accent1); line-height: 1.6;
  border-left: 2px solid rgba(0,240,200,0.2);
  padding-left: 10px;
}

/* ─── INSTAGRAM STRATEGY ────────────────────────────────────────── */
#strategy { padding: 100px 0; }
.strategy-layout {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 60px; align-items: center; margin-top: 56px;
}
.strategy-steps { display: flex; flex-direction: column; gap: 0; }
.step {
  display: flex; gap: 24px; padding: 28px 0;
  border-bottom: 1px solid var(--border);
  transition: all 0.3s; cursor: default;
}
.step:last-child { border-bottom: none; }
.step:hover .step-num { background: var(--accent1); color: var(--bg); }
.step-num {
  width: 40px; height: 40px; border-radius: 50%; flex-shrink: 0;
  border: 1px solid var(--border2);
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-mono); font-size: 12px; color: var(--muted);
  transition: all 0.3s;
}
.step-content {}
.step-title { font-size: 16px; font-weight: 700; color: var(--white); margin-bottom: 6px; }
.step-desc { font-size: 13px; color: var(--muted); line-height: 1.6; }

/* Growth chart visual */
.growth-visual {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 20px; padding: 32px;
}
.growth-title {
  font-family: var(--font-mono); font-size: 11px;
  color: var(--muted); letter-spacing: 0.1em;
  text-transform: uppercase; margin-bottom: 24px;
}
.chart-bars {
  display: flex; align-items: flex-end;
  gap: 8px; height: 160px;
}
.bar-wrap { flex: 1; display: flex; flex-direction: column; align-items: center; gap: 6px; }
.bar {
  width: 100%; border-radius: 4px 4px 0 0;
  background: linear-gradient(180deg, var(--accent1), rgba(0,240,200,0.3));
  transition: all 0.3s;
  animation: barGrow 1s ease both;
}
@keyframes barGrow {
  from { height: 0 !important; }
}
.bar:hover { background: linear-gradient(180deg, var(--white), var(--accent1)); }
.bar-month { font-size: 9px; color: var(--muted); font-family: var(--font-mono); }
.chart-legend {
  display: flex; gap: 20px; margin-top: 20px;
  padding-top: 20px; border-top: 1px solid var(--border);
}
.legend-item { display: flex; align-items: center; gap: 6px; font-size: 11px; color: var(--muted); }
.legend-dot { width: 8px; height: 8px; border-radius: 50%; }
.legend-dot.green { background: var(--accent1); }
.legend-dot.red { background: var(--accent2); }

/* ─── TOOLS STRIP ───────────────────────────────────────────────── */
#tools { padding: 80px 0; background: var(--surface); }
.tools-row {
  display: flex; flex-wrap: wrap; gap: 12px;
  margin-top: 40px;
}
.tool-chip {
  display: flex; align-items: center; gap: 8px;
  padding: 10px 18px;
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 100px;
  font-size: 12px; color: var(--text);
  font-family: var(--font-mono); font-weight: 400;
  transition: all 0.25s; cursor: default;
}
.tool-chip:hover {
  border-color: rgba(0,240,200,0.3);
  color: var(--accent1);
  background: rgba(0,240,200,0.04);
  transform: translateY(-2px);
}
.tool-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--accent1); flex-shrink: 0; }

/* ─── CTA SECTION ───────────────────────────────────────────────── */
#cta {
  padding: 120px 0;
  text-align: center;
  position: relative; overflow: hidden;
}
#cta::before {
  content: '';
  position: absolute; left: 50%; top: 50%;
  transform: translate(-50%, -50%);
  width: 700px; height: 400px;
  background: radial-gradient(ellipse, rgba(0,240,200,0.08) 0%, transparent 70%);
  pointer-events: none;
}
.cta-eyebrow {
  font-family: var(--font-mono); font-size: 11px;
  color: var(--accent1); letter-spacing: 0.15em;
  text-transform: uppercase; margin-bottom: 24px;
}
.cta-title {
  font-size: clamp(36px, 5vw, 64px); font-weight: 800;
  color: var(--white); letter-spacing: -0.02em;
  line-height: 1.05; margin-bottom: 20px;
}
.cta-title em {
  font-style: normal;
  background: linear-gradient(90deg, var(--accent1), var(--accent3));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  background-clip: text;
}
.cta-sub { font-size: 16px; color: var(--muted); margin-bottom: 48px; }
.cta-buttons { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }

/* ─── FOOTER ────────────────────────────────────────────────────── */
footer {
  padding: 40px 60px;
  border-top: 1px solid var(--border);
  display: flex; align-items: center; justify-content: space-between;
}
.footer-logo {
  font-family: var(--font-mono); font-size: 13px;
  color: var(--accent1); font-weight: 500; letter-spacing: 0.06em;
}
.footer-copy { font-size: 12px; color: var(--muted); font-family: var(--font-mono); }
.footer-ig {
  display: flex; align-items: center; gap: 8px;
  font-family: var(--font-mono); font-size: 12px;
  color: var(--muted); text-decoration: none;
  transition: color 0.2s;
}
.footer-ig:hover { color: var(--accent1); }
.ig-icon {
  width: 28px; height: 28px; border-radius: 7px;
  background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
  display: flex; align-items: center; justify-content: center;
  font-size: 13px;
}

/* ─── SCROLLBAR ─────────────────────────────────────────────────── */
::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-track { background: var(--bg); }
::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 4px; }

/* ─── RESPONSIVE ─────────────────────────────────────────────────── */
@media (max-width: 1024px) {
  nav { padding: 18px 30px; }
  .nav-links { display: none; }
  #hero { padding: 100px 30px 80px; }
  .hero-visual { display: none; }
  .section-inner { padding: 0 30px; }
  .pillars-grid { grid-template-columns: repeat(2,1fr); }
  .strategy-layout { grid-template-columns: 1fr; }
  footer { padding: 30px; flex-direction: column; gap: 16px; text-align: center; }
}
@media (max-width: 640px) {
  .pillars-grid { grid-template-columns: 1fr; }
  .hero-stats { flex-direction: column; gap: 20px; }
}
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- ── NAV ───────────────────────────────────────────────────────── -->
<nav>
  <a href="#" class="nav-logo">VK<span>.ai</span></a>
  <ul class="nav-links">
    <li><a href="#topics">Topics</a></li>
    <li><a href="#pillars">Content</a></li>
    <li><a href="#strategy">Strategy</a></li>
    <li><a href="#tools">Tools</a></li>
  </ul>
  <a href="https://www.instagram.com/vicky_khanna54/" target="_blank" class="nav-cta">Follow on Instagram ↗</a>
</nav>

<!-- ── HERO ──────────────────────────────────────────────────────── -->
<section id="hero">
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>
  <div class="hero-orb hero-orb-3"></div>

  <div class="hero-content">
    <div class="hero-badge">
      <span class="badge-pulse"></span>
      AI & Automation Expert
    </div>
    <h1 class="hero-title">
      <span class="line1">Vicky</span><br>
      <span class="line2">Khanna</span><br>
      <span class="line3">builds AI</span>
    </h1>
    <p class="hero-sub">
      Teaching <strong>No-Code AI Agents, RAG, Automation & LLMs</strong> to professionals who want to build faster, smarter — without writing a single line of code.
    </p>
    <div class="hero-actions">
      <a href="https://www.instagram.com/vicky_khanna54/" target="_blank" class="btn-primary">
        Follow on Instagram ↗
      </a>
      <a href="#topics" class="btn-secondary">
        Explore Topics →
      </a>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <span class="stat-num">2K<span class="accent">+</span></span>
        <span class="stat-label">Followers</span>
      </div>
      <div class="stat-item">
        <span class="stat-num">20<span class="accent">+</span></span>
        <span class="stat-label">AI Topics</span>
      </div>
      <div class="stat-item">
        <span class="stat-num">🔥</span>
        <span class="stat-label">Trending Niche</span>
      </div>
    </div>
  </div>

  <!-- Phone mockup -->
  <div class="hero-visual">
    <div class="phone-frame">
      <div class="phone-header">
        <div class="phone-avatar">VK</div>
        <div class="phone-info">
          <div class="phone-name">Vicky Khanna</div>
          <div class="phone-handle">@vicky_khanna54</div>
        </div>
        <div class="phone-follow">Follow</div>
      </div>
      <div class="phone-body">
        <div class="phone-post">
          <span class="post-tag">AI AGENTS</span>
          <div class="post-line w80"></div>
          <div class="post-line w60"></div>
          <div class="post-line w45"></div>
        </div>
        <div class="phone-post">
          <span class="post-tag">NO-CODE RAG</span>
          <div class="post-line w60"></div>
          <div class="post-line w80"></div>
          <div class="post-line w50" style="width:50%"></div>
        </div>
        <div class="phone-post">
          <span class="post-tag">AUTOMATION</span>
          <div class="post-line w80"></div>
          <div class="post-line w45"></div>
        </div>
        <div class="phone-metrics">
          <div class="metric">❤️ <span>1.2K</span></div>
          <div class="metric">💬 <span>84</span></div>
          <div class="metric">🔖 <span>340</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── TOPICS ─────────────────────────────────────────────────────── -->
<section id="topics">
  <div class="section-inner">
    <div class="section-tag">What I cover</div>
    <h2 class="section-title">AI Topics I Teach</h2>
    <p class="section-sub">Every post, reel and carousel is designed to make cutting-edge AI accessible and actionable for you.</p>

    <div class="topics-grid">
      <div class="topic-card">
        <span class="topic-badge">HOT</span>
        <div class="topic-icon">🤖</div>
        <div class="topic-name">AI Agents</div>
        <div class="topic-desc">Build autonomous AI agents that think, plan and execute tasks — no code needed.</div>
      </div>
      <div class="topic-card">
        <span class="topic-badge">TRENDING</span>
        <div class="topic-icon">🧠</div>
        <div class="topic-name">RAG Systems</div>
        <div class="topic-desc">Retrieval-Augmented Generation for smarter, more accurate AI responses with your own data.</div>
      </div>
      <div class="topic-card">
        <div class="topic-icon">⚙️</div>
        <div class="topic-name">AI Workflow Automation</div>
        <div class="topic-desc">Connect AI tools into powerful automated pipelines that run your business on autopilot.</div>
      </div>
      <div class="topic-card">
        <span class="topic-badge">NEW</span>
        <div class="topic-icon">🏗️</div>
        <div class="topic-name">No-Code SaaS</div>
        <div class="topic-desc">Launch AI-powered SaaS products without writing code using modern no-code platforms.</div>
      </div>
      <div class="topic-card">
        <div class="topic-icon">💬</div>
        <div class="topic-name">Prompt Engineering</div>
        <div class="topic-desc">Master prompts that get precise, reliable outputs from LLMs every single time.</div>
      </div>
      <div class="topic-card">
        <div class="topic-icon">🔬</div>
        <div class="topic-name">Context Engineering</div>
        <div class="topic-desc">The next evolution beyond prompting — design AI context windows for maximum performance.</div>
      </div>
      <div class="topic-card">
        <div class="topic-icon">📊</div>
        <div class="topic-name">AI Data Analysis</div>
        <div class="topic-desc">Turn raw data into powerful insights using AI-powered analysis and visualization tools.</div>
      </div>
      <div class="topic-card">
        <div class="topic-icon">🎨</div>
        <div class="topic-name">Multimodal AI</div>
        <div class="topic-desc">Work with text, image, audio and video AI models together for powerful content creation.</div>
      </div>
      <div class="topic-card">
        <span class="topic-badge">ADVANCED</span>
        <div class="topic-icon">🧬</div>
        <div class="topic-name">LLM Fine-Tuning</div>
        <div class="topic-desc">Customize large language models on your own datasets for specialized AI applications.</div>
      </div>
    </div>
  </div>
</section>

<!-- ── PILLARS ────────────────────────────────────────────────────── -->
<section id="pillars">
  <div class="section-inner">
    <div class="section-tag">Content Strategy</div>
    <h2 class="section-title">4 Content Pillars</h2>
    <p class="section-sub">Every piece of content I create follows one of these four strategic pillars designed to grow, educate and convert.</p>

    <div class="pillars-grid">
      <div class="pillar">
        <div class="pillar-num">01</div>
        <span class="pillar-icon">🛠️</span>
        <div class="pillar-title">Tutorial</div>
        <div class="pillar-desc">Step-by-step breakdowns of AI tools, workflows and builds that viewers can replicate immediately.</div>
        <div class="pillar-example">"Build an AI Agent in 10 mins — No Code Required"</div>
      </div>
      <div class="pillar">
        <div class="pillar-num">02</div>
        <span class="pillar-icon">💡</span>
        <div class="pillar-title">Insight</div>
        <div class="pillar-desc">Deep knowledge drops on AI concepts — explained simply. These establish authority and get saved.</div>
        <div class="pillar-example">"Why RAG beats fine-tuning for 90% of use cases"</div>
      </div>
      <div class="pillar">
        <div class="pillar-num">03</div>
        <span class="pillar-icon">🔥</span>
        <div class="pillar-title">Tool Review</div>
        <div class="pillar-desc">Honest breakdowns of the best AI tools hitting the market. Timely, shareable, high-reach content.</div>
        <div class="pillar-example">"5 AI Automation tools I'd use if starting today"</div>
      </div>
      <div class="pillar">
        <div class="pillar-num">04</div>
        <span class="pillar-icon">🙋</span>
        <div class="pillar-title">Personal Brand</div>
        <div class="pillar-desc">Behind-the-scenes, wins, lessons and journey content that builds connection and trust.</div>
        <div class="pillar-example">"How I built my first AI workflow from scratch"</div>
      </div>
    </div>
  </div>
</section>

<!-- ── STRATEGY ───────────────────────────────────────────────────── -->
<section id="strategy">
  <div class="section-inner">
    <div class="section-tag">Growth Blueprint</div>
    <h2 class="section-title">Instagram Growth Strategy</h2>
    <p class="section-sub">A proven, step-by-step system for growing from 2K to 10K+ in the AI niche.</p>

    <div class="strategy-layout">
      <div class="strategy-steps">
        <div class="step">
          <div class="step-num">01</div>
          <div class="step-content">
            <div class="step-title">Reels-First Always</div>
            <div class="step-desc">Every insight, tip and tutorial gets packaged as a 30–60 second Reel. Hook in the first 3 seconds — Reels carry 3.5× the organic reach of static posts.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">02</div>
          <div class="step-content">
            <div class="step-title">SEO-Optimised Bio & Captions</div>
            <div class="step-desc">Instagram is used like a search engine in 2026. Keywords in your name field, bio and captions push you into discovery feeds.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">03</div>
          <div class="step-content">
            <div class="step-title">Save-Worthy Carousels</div>
            <div class="step-desc">Saves and watch time outrank likes in 2026's algorithm. Carousels like "7 AI tools that replace a full team" rack up saves and repeat views.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">04</div>
          <div class="step-content">
            <div class="step-title">Consistent 4–5×/Week</div>
            <div class="step-desc">Quality over frequency. Post 4–5 times per week across Reels, carousels and stories. Consistent signals beat sporadic bursts.</div>
          </div>
        </div>
        <div class="step">
          <div class="step-num">05</div>
          <div class="step-content">
            <div class="step-title">Community Engagement Daily</div>
            <div class="step-desc">Comment meaningfully on 10 posts daily from accounts in the AI niche. This sends strong community signals to the algorithm.</div>
          </div>
        </div>
      </div>

      <div class="growth-visual">
        <div class="growth-title">// Projected Follower Growth</div>
        <div class="chart-bars">
          <div class="bar-wrap">
            <div class="bar" style="height:30%; animation-delay: 0.1s"></div>
            <span class="bar-month">Now</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:38%; animation-delay: 0.2s"></div>
            <span class="bar-month">M1</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:48%; animation-delay: 0.3s"></div>
            <span class="bar-month">M2</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:58%; animation-delay: 0.4s"></div>
            <span class="bar-month">M3</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:70%; animation-delay: 0.5s"></div>
            <span class="bar-month">M4</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:82%; animation-delay: 0.6s"></div>
            <span class="bar-month">M5</span>
          </div>
          <div class="bar-wrap">
            <div class="bar" style="height:100%; animation-delay: 0.7s"></div>
            <span class="bar-month">M6</span>
          </div>
        </div>
        <div class="chart-legend">
          <div class="legend-item">
            <div class="legend-dot green"></div>
            Follower Growth
          </div>
          <div class="legend-item">
            <div class="legend-dot red"></div>
            Engagement Rate
          </div>
        </div>

        <div style="margin-top:24px; padding-top:24px; border-top: 1px solid var(--border); display: flex; flex-direction: column; gap: 12px;">
          <div style="display:flex; justify-content:space-between; align-items:center;">
            <span style="font-size:12px; color:var(--muted); font-family:var(--font-mono)">Target: 6 months</span>
            <span style="font-size:14px; font-weight:700; color:var(--accent1); font-family:var(--font-mono)">10K+</span>
          </div>
          <div style="display:flex; justify-content:space-between; align-items:center;">
            <span style="font-size:12px; color:var(--muted); font-family:var(--font-mono)">Niche ranking</span>
            <span style="font-size:14px; font-weight:700; color:var(--white); font-family:var(--font-mono)">🔥 Top 5%</span>
          </div>
          <div style="display:flex; justify-content:space-between; align-items:center;">
            <span style="font-size:12px; color:var(--muted); font-family:var(--font-mono)">Monetization</span>
            <span style="font-size:14px; font-weight:700; color:var(--accent1); font-family:var(--font-mono)">Ready @ 5K</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── TOOLS ──────────────────────────────────────────────────────── -->
<section id="tools">
  <div class="section-inner">
    <div class="section-tag">Ecosystem</div>
    <h2 class="section-title">AI Tools I Cover</h2>
    <p class="section-sub">From automation platforms to LLMs — the full AI stack explained in plain language.</p>
    <div class="tools-row">
      <div class="tool-chip"><span class="tool-dot"></span>ChatGPT / GPT-4o</div>
      <div class="tool-chip"><span class="tool-dot"></span>Claude (Anthropic)</div>
      <div class="tool-chip"><span class="tool-dot"></span>n8n</div>
      <div class="tool-chip"><span class="tool-dot"></span>Make.com</div>
      <div class="tool-chip"><span class="tool-dot"></span>Zapier</div>
      <div class="tool-chip"><span class="tool-dot"></span>Dify</div>
      <div class="tool-chip"><span class="tool-dot"></span>LangChain</div>
      <div class="tool-chip"><span class="tool-dot"></span>LlamaIndex</div>
      <div class="tool-chip"><span class="tool-dot"></span>Pinecone</div>
      <div class="tool-chip"><span class="tool-dot"></span>Supabase</div>
      <div class="tool-chip"><span class="tool-dot"></span>Flowise</div>
      <div class="tool-chip"><span class="tool-dot"></span>Bubble</div>
      <div class="tool-chip"><span class="tool-dot"></span>Voiceflow</div>
      <div class="tool-chip"><span class="tool-dot"></span>Perplexity AI</div>
      <div class="tool-chip"><span class="tool-dot"></span>Midjourney</div>
      <div class="tool-chip"><span class="tool-dot"></span>Hugging Face</div>
      <div class="tool-chip"><span class="tool-dot"></span>Gemini</div>
      <div class="tool-chip"><span class="tool-dot"></span>Mistral</div>
      <div class="tool-chip"><span class="tool-dot"></span>Groq</div>
      <div class="tool-chip"><span class="tool-dot"></span>Replit</div>
    </div>
  </div>
</section>

<!-- ── CTA ────────────────────────────────────────────────────────── -->
<section id="cta">
  <div class="section-inner" style="text-align:center; position: relative; z-index: 1;">
    <div class="cta-eyebrow">Ready to learn AI?</div>
    <h2 class="cta-title">
      Join the community.<br>
      <em>Master AI automation.</em>
    </h2>
    <p class="cta-sub">Follow @vicky_khanna54 on Instagram and DM "AI" to get your free starter toolkit.</p>
    <div class="cta-buttons">
      <a href="https://www.instagram.com/vicky_khanna54/" target="_blank" class="btn-primary">
        Follow @vicky_khanna54 ↗
      </a>
      <a href="https://www.instagram.com/vicky_khanna54/" target="_blank" class="btn-secondary">
        DM "AI" for Free Toolkit
      </a>
    </div>
  </div>
</section>

<!-- ── FOOTER ─────────────────────────────────────────────────────── -->
<footer>
  <div class="footer-logo">VK.ai — Vicky Khanna</div>
  <div class="footer-copy">© 2026 · AI & Automation Expert</div>
  <a href="https://www.instagram.com/vicky_khanna54/" target="_blank" class="footer-ig">
    <div class="ig-icon">📸</div>
    @vicky_khanna54
  </a>
</footer>

<script>
  // Custom cursor
  const cursor = document.getElementById('cursor');
  const ring = document.getElementById('cursorRing');
  let mx = 0, my = 0, rx = 0, ry = 0;

  document.addEventListener('mousemove', e => {
    mx = e.clientX; my = e.clientY;
    cursor.style.left = mx + 'px';
    cursor.style.top  = my + 'px';
  });

  function animRing() {
    rx += (mx - rx) * 0.12;
    ry += (my - ry) * 0.12;
    ring.style.left = rx + 'px';
    ring.style.top  = ry + 'px';
    requestAnimationFrame(animRing);
  }
  animRing();

  document.querySelectorAll('a, button, .topic-card, .step, .pillar, .tool-chip').forEach(el => {
    el.addEventListener('mouseenter', () => {
      cursor.style.width = '20px'; cursor.style.height = '20px';
      ring.style.width = '56px'; ring.style.height = '56px';
      ring.style.borderColor = 'rgba(0,240,200,0.7)';
    });
    el.addEventListener('mouseleave', () => {
      cursor.style.width = '12px'; cursor.style.height = '12px';
      ring.style.width = '36px'; ring.style.height = '36px';
      ring.style.borderColor = 'rgba(0,240,200,0.4)';
    });
  });

  // Scroll-triggered bar animation
  const bars = document.querySelectorAll('.bar');
  const heights = ['30%','38%','48%','58%','70%','82%','100%'];
  const barObserver = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        bars.forEach((b, i) => {
          setTimeout(() => {
            b.style.height = heights[i];
          }, i * 80);
        });
      }
    });
  }, { threshold: 0.3 });

  const chart = document.querySelector('.chart-bars');
  if (chart) barObserver.observe(chart);

  // Reset bars height initially for animation
  bars.forEach(b => b.style.height = '4px');
</script>
</body>
</html>
