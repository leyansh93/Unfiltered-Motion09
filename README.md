<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="referrer" content="strict-origin-when-cross-origin">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Unfiltered Motion — premium motion design for SaaS launches, app reels, and bold brands. App launch videos, short-form content, and VSLs that convert.">
<title>Unfiltered Motion — Premium Motion Design Studio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=DM+Mono:wght@300;400;500&family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
/* ============================================
   RESET & BASE
   ============================================ */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  /* Colors */
  --black: #050508;
  --off-black: #0a0a10;
  --dark: #0d0d18;
  --blue: #2563FF;
  --blue-light: #3b75ff;
  --blue-dim: rgba(37,99,255,0.12);
  --blue-glow: rgba(37,99,255,0.35);
  --white: #f0f0f5;
  --grey: #888899;
  --grey-dim: rgba(136,136,153,0.15);
  --border: rgba(255,255,255,0.07);
  --border-soft: rgba(255,255,255,0.045);

  /* Type */
  --font-display: 'Syne', sans-serif;
  --font-body: 'DM Mono', monospace;
  --font-serif: 'Cormorant Garamond', serif;

  /* Layout grid — single source of truth for horizontal rhythm */
  --container: 1280px;
  --gutter: 60px;
  --gutter-tablet: 40px;
  --gutter-mobile: 24px;

  /* Vertical rhythm */
  --section-pad: 140px;
  --section-pad-tablet: 100px;
  --section-pad-mobile: 72px;

  /* Motion */
  --ease: cubic-bezier(0.16, 1, 0.3, 1);
  --t-fast: 0.2s;
  --t-med: 0.4s;
  --t-slow: 0.7s;
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 90px;
}

body {
  background: var(--black);
  color: var(--white);
  font-family: var(--font-body);
  font-size: 15px;
  line-height: 1.6;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
}

::selection { background: var(--blue-dim); color: var(--white); }

img { max-width: 100%; display: block; }

a { color: inherit; }

/* Visible focus state for accessibility — never removed */
a:focus-visible,
button:focus-visible,
input:focus-visible,
select:focus-visible,
textarea:focus-visible,
[tabindex]:focus-visible {
  outline: 2px solid var(--blue);
  outline-offset: 3px;
  border-radius: 4px;
}

/* Skip link for keyboard / screen-reader users */
.skip-link {
  position: absolute; left: -9999px; top: auto;
  background: var(--blue); color: var(--white);
  padding: 12px 20px; border-radius: 8px;
  font-family: var(--font-body); font-size: 12px;
  letter-spacing: 0.08em; text-transform: uppercase;
  z-index: 1000;
}
.skip-link:focus {
  left: 16px; top: 16px;
}

/* ============================================
   LAYOUT GRID
   ============================================ */
.container {
  max-width: var(--container);
  margin: 0 auto;
  padding-left: var(--gutter);
  padding-right: var(--gutter);
}

section { padding: var(--section-pad) 0; }

@media (max-width: 1024px) {
  :root { --gutter: var(--gutter-tablet); --section-pad: var(--section-pad-tablet); }
}
@media (max-width: 640px) {
  :root { --gutter: var(--gutter-mobile); --section-pad: var(--section-pad-mobile); }
}

/* ============================================
   GRID BACKGROUND
   ============================================ */
.grid-bg {
  position: fixed; inset: 0; pointer-events: none; z-index: 0; opacity: 0.025;
  background-image:
    linear-gradient(rgba(37,99,255,1) 1px, transparent 1px),
    linear-gradient(90deg, rgba(37,99,255,1) 1px, transparent 1px);
  background-size: 80px 80px;
}

/* ============================================
   NAV
   ============================================ */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  background: linear-gradient(to bottom, rgba(5,5,8,0.9), transparent);
  border-bottom: 1px solid transparent;
  transition: background var(--t-med) var(--ease), border-color var(--t-med) var(--ease), backdrop-filter var(--t-med) var(--ease);
}
nav .container {
  display: flex; align-items: center; justify-content: space-between;
  padding-top: 22px; padding-bottom: 22px;
}
nav.scrolled {
  background: rgba(5,5,8,0.85);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border);
}

.nav-logo {
  display: flex; align-items: center; gap: 12px;
  text-decoration: none;
  flex-shrink: 0;
}
.nav-logo-mark {
  width: 38px; height: 38px;
  border-radius: 9px;
  overflow: hidden;
  display: flex; align-items: center; justify-content: center;
  background: #03040a;
  box-shadow: 0 0 0 1px var(--border), 0 0 24px rgba(37,99,255,0.18);
  flex-shrink: 0;
}
.nav-logo-mark img {
  width: 100%; height: 100%; object-fit: cover;
}
.nav-logo-text {
  font-family: var(--font-display);
  font-size: 14px; font-weight: 700;
  letter-spacing: 0.06em; text-transform: uppercase;
  color: var(--white);
  white-space: nowrap;
}

.nav-links { display: flex; align-items: center; gap: 36px; }
.nav-links a:not(.btn-nav) {
  font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase;
  color: var(--grey); text-decoration: none;
  transition: color var(--t-fast) var(--ease);
  position: relative;
  padding-bottom: 4px;
}
.nav-links a:not(.btn-nav)::after {
  content: ''; position: absolute; bottom: -1px; left: 0;
  width: 0; height: 1px; background: var(--blue);
  transition: width var(--t-med) var(--ease);
}
.nav-links a:not(.btn-nav):hover { color: var(--white); }
.nav-links a:not(.btn-nav):hover::after,
.nav-links a:not(.btn-nav).active::after { width: 100%; }
.nav-links a.active { color: var(--white); }

.btn-nav {
  padding: 10px 24px;
  border: 1px solid var(--blue);
  color: var(--blue);
  border-radius: 100px;
  text-decoration: none;
  font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase;
  transition: background var(--t-fast) var(--ease), color var(--t-fast) var(--ease), box-shadow var(--t-fast) var(--ease);
  white-space: nowrap;
}
.btn-nav:hover {
  background: var(--blue);
  color: var(--white);
  box-shadow: 0 0 24px var(--blue-glow);
}

/* Mobile nav toggle */
.nav-toggle {
  display: none;
  width: 40px; height: 40px;
  align-items: center; justify-content: center;
  background: transparent; border: 1px solid var(--border);
  border-radius: 8px; cursor: pointer;
  flex-shrink: 0;
}
.nav-toggle span,
.nav-toggle span::before,
.nav-toggle span::after {
  content: ''; display: block;
  width: 16px; height: 1px; background: var(--white);
  position: relative; transition: transform var(--t-fast) var(--ease), opacity var(--t-fast) var(--ease);
}
.nav-toggle span::before { position: absolute; top: -5px; }
.nav-toggle span::after { position: absolute; top: 5px; }
.nav-toggle[aria-expanded="true"] span { background: transparent; }
.nav-toggle[aria-expanded="true"] span::before { transform: translateY(5px) rotate(45deg); }
.nav-toggle[aria-expanded="true"] span::after { transform: translateY(-5px) rotate(-45deg); }

@media (max-width: 860px) {
  .nav-toggle { display: flex; }
  .nav-links {
    position: fixed; top: 0; right: 0;
    width: min(320px, 80vw); height: 100vh;
    background: rgba(8,8,14,0.98);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    flex-direction: column; align-items: flex-start;
    justify-content: center; gap: 28px;
    padding: 0 var(--gutter-mobile);
    border-left: 1px solid var(--border);
    transform: translateX(100%);
    transition: transform var(--t-med) var(--ease);
  }
  .nav-links.open { transform: translateX(0); }
  .nav-links a:not(.btn-nav) { font-size: 13px; }
  .btn-nav { width: 100%; text-align: center; padding: 14px 24px; }
}

/* ============================================
   BUTTONS (shared)
   ============================================ */
.btn-primary, .btn-ghost, .btn-submit {
  display: inline-flex; align-items: center; justify-content: center; gap: 10px;
  font-family: var(--font-body); font-size: 11px; font-weight: 500;
  letter-spacing: 0.12em; text-transform: uppercase;
  text-decoration: none; border: none; cursor: pointer;
  border-radius: 100px; white-space: nowrap;
}
.btn-primary {
  padding: 16px 34px;
  background: var(--blue); color: var(--white);
  transition: box-shadow var(--t-fast) var(--ease), transform var(--t-fast) var(--ease), background var(--t-fast) var(--ease);
}
.btn-primary:hover { box-shadow: 0 0 36px var(--blue-glow); transform: translateY(-2px); }
.btn-primary:active { transform: translateY(0); }

.btn-ghost {
  padding: 16px 34px;
  background: transparent; color: var(--grey);
  border: 1px solid var(--border);
  transition: border-color var(--t-fast) var(--ease), color var(--t-fast) var(--ease), background var(--t-fast) var(--ease);
}
.btn-ghost:hover { border-color: var(--blue); color: var(--white); background: var(--blue-dim); }

.btn-block { width: 100%; }

/* ============================================
   HERO
   ============================================ */
.hero {
  min-height: 100vh;
  display: flex; align-items: center;
  padding-top: 140px; padding-bottom: 80px;
  position: relative; overflow: hidden;
}
.hero .container {
  display: grid; grid-template-columns: 1.05fr 1fr; gap: 64px;
  align-items: center;
  width: 100%;
}
.hero-bg { position: absolute; inset: 0; pointer-events: none; z-index: 0; }
.hero-arc {
  position: absolute;
  border: 1px solid var(--border-soft);
  border-radius: 50%; pointer-events: none;
}
.hero-arc-1 { width: 900px; height: 900px; top: -240px; left: -180px; }
.hero-arc-2 { width: 600px; height: 600px; top: -90px; left: -60px; }
.hero-arc-3 { width: 1240px; height: 1240px; top: -440px; left: -380px; }
.hero-glow {
  position: absolute;
  width: 560px; height: 560px;
  background: radial-gradient(circle, rgba(37,99,255,0.14) 0%, transparent 70%);
  top: 6%; left: 28%;
  pointer-events: none;
}

.hero-left { position: relative; z-index: 1; }
.hero-tag {
  display: inline-flex; align-items: center; gap: 10px;
  font-size: 10px; letter-spacing: 0.24em; text-transform: uppercase;
  color: var(--blue); margin-bottom: 28px;
  opacity: 0; animation: fadeUp 0.8s 0.1s var(--ease) forwards;
}
.hero-tag::before { content: ''; display: block; width: 24px; height: 1px; background: var(--blue); }

.hero-title {
  font-family: var(--font-serif);
  font-size: clamp(44px, 6vw, 84px);
  font-weight: 400; line-height: 1.08;
  letter-spacing: -0.01em;
  color: var(--white);
  opacity: 0; animation: fadeUp 0.8s 0.22s var(--ease) forwards;
}
.hero-title em {
  font-style: italic;
  color: transparent;
  -webkit-text-stroke: 1px rgba(240,240,245,0.55);
}
.hero-sub {
  margin-top: 24px;
  font-size: 13px; line-height: 1.85;
  color: var(--grey); max-width: 420px;
  letter-spacing: 0.01em;
  opacity: 0; animation: fadeUp 0.8s 0.34s var(--ease) forwards;
}
.hero-ctas {
  display: flex; flex-wrap: wrap; gap: 16px; align-items: center;
  margin-top: 44px;
  opacity: 0; animation: fadeUp 0.8s 0.46s var(--ease) forwards;
}

/* HERO RIGHT — showreel */
.hero-right {
  position: relative; z-index: 1;
  display: flex; flex-direction: column; align-items: stretch; gap: 16px;
}
.showreel-label {
  font-size: 10px; letter-spacing: 0.24em; text-transform: uppercase; color: var(--grey);
  opacity: 0; animation: fadeUp 0.8s 0.34s var(--ease) forwards;
}

/* Responsive 16:9 video container, ready for Vimeo / YouTube embeds */
.video-frame {
  position: relative;
  width: 100%;
  aspect-ratio: 16 / 9;
  background: var(--dark);
  border: 1px solid var(--border);
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 40px 80px rgba(0,0,0,0.55), 0 0 0 1px var(--border-soft);
  opacity: 0; animation: fadeUp 0.8s 0.46s var(--ease) forwards;
}
.video-frame iframe,
.video-frame video {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  border: 0; display: block;
}
.video-frame .video-poster {
  position: absolute; inset: 0;
  width: 100%; height: 100%; object-fit: cover;
  cursor: pointer;
}
.video-frame .video-placeholder {
  position: absolute; inset: 0;
  display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 16px;
  background: linear-gradient(135deg, #0d1225 0%, #0a0a15 100%);
  cursor: pointer; border: none; width: 100%; padding: 0;
  color: var(--grey);
  font-family: var(--font-body);
}
.video-frame .video-placeholder:hover .play-btn { transform: scale(1.08); box-shadow: 0 0 56px var(--blue-glow); }
.video-frame .video-placeholder p {
  font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase;
}

.play-btn {
  width: 64px; height: 64px;
  background: var(--blue); border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 0 36px var(--blue-glow);
  transition: transform var(--t-fast) var(--ease), box-shadow var(--t-fast) var(--ease);
  flex-shrink: 0;
}
.play-btn svg { fill: white; margin-left: 3px; }

/* Scroll hint */
.scroll-hint {
  position: absolute; bottom: 36px; left: 50%;
  transform: translateX(-50%);
  display: flex; flex-direction: column; align-items: center; gap: 10px;
  font-size: 9px; letter-spacing: 0.24em; color: var(--grey);
  animation: fadeUp 1s 1s var(--ease) both;
  text-transform: uppercase;
  z-index: 1;
}
.scroll-line {
  width: 1px; height: 36px;
  background: linear-gradient(to bottom, var(--blue), transparent);
  animation: scrollPulse 2.4s ease-in-out infinite;
}
@keyframes scrollPulse {
  0%, 100% { opacity: 0.25; transform: scaleY(0.5); transform-origin: top; }
  50% { opacity: 1; transform: scaleY(1); }
}

@media (max-width: 900px) {
  .hero { padding-top: 120px; }
  .hero .container { grid-template-columns: 1fr; gap: 56px; }
  .hero-right { order: -1; }
  .scroll-hint { display: none; }
}

/* ============================================
   TRUSTED BY (marquee)
   ============================================ */
.trusted {
  padding: 36px 0;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  overflow: hidden;
  position: relative;
}
.trusted::before, .trusted::after {
  content: ''; position: absolute; top: 0; bottom: 0; width: 80px; z-index: 1;
  pointer-events: none;
}
.trusted::before { left: 0; background: linear-gradient(to right, var(--black), transparent); }
.trusted::after { right: 0; background: linear-gradient(to left, var(--black), transparent); }
.trusted-track {
  display: flex; gap: 56px; align-items: center;
  animation: marquee 32s linear infinite;
  width: max-content;
}
.trusted:hover .trusted-track { animation-play-state: paused; }
.trusted-label {
  font-size: 10px; letter-spacing: 0.24em; color: var(--grey);
  text-transform: uppercase; white-space: nowrap; flex-shrink: 0;
}
.trusted-item {
  font-family: var(--font-display);
  font-size: 12px; letter-spacing: 0.16em; text-transform: uppercase;
  color: rgba(136,136,153,0.55); white-space: nowrap; flex-shrink: 0;
  transition: color var(--t-fast) var(--ease);
}
.trusted-item:hover { color: var(--white); }
@keyframes marquee {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

/* ============================================
   SECTION HEADERS (shared)
   ============================================ */
.section-tag {
  font-size: 10px; letter-spacing: 0.28em; text-transform: uppercase;
  color: var(--blue); margin-bottom: 18px;
  display: flex; align-items: center; gap: 10px;
}
.section-tag::before { content: ''; display: block; width: 20px; height: 1px; background: var(--blue); }
.section-title {
  font-family: var(--font-serif);
  font-size: clamp(34px, 4vw, 60px);
  font-weight: 400; line-height: 1.15; color: var(--white);
}
.section-title em { font-style: italic; color: transparent; -webkit-text-stroke: 1px rgba(240,240,245,0.4); }

/* ============================================
   WORKS
   ============================================ */
#works { background: var(--black); }
.works-header {
  display: flex; justify-content: space-between; align-items: flex-end; gap: 32px;
  margin-bottom: 56px; flex-wrap: wrap;
}
.works-grid {
  display: grid; grid-template-columns: repeat(2, 1fr); gap: 24px;
}
.work-item {
  position: relative; border-radius: 14px; overflow: hidden;
  background: var(--dark); border: 1px solid var(--border);
  transition: transform var(--t-med) var(--ease), box-shadow var(--t-med) var(--ease), border-color var(--t-med) var(--ease);
}
.work-item:hover {
  transform: translateY(-6px);
  box-shadow: 0 24px 60px rgba(0,0,0,0.5);
  border-color: var(--border);
}
.work-item:first-child { grid-column: 1 / -1; }

.work-video-wrap {
  aspect-ratio: 16 / 9; background: var(--off-black);
  position: relative; overflow: hidden;
}
.work-video-wrap iframe, .work-video-wrap video {
  position: absolute; inset: 0; width: 100%; height: 100%; border: none;
}
.work-video-wrap .video-poster {
  position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover;
  transition: transform var(--t-slow) var(--ease);
}
.work-item:hover .video-poster { transform: scale(1.04); }
.work-video-wrap .video-overlay {
  position: absolute; inset: 0;
  display: flex; align-items: center; justify-content: center;
  background: rgba(5,5,8,0.32);
  transition: background var(--t-fast) var(--ease);
}
.work-item:hover .video-overlay { background: rgba(5,5,8,0.12); }
.work-video-wrap .video-placeholder {
  position: absolute; inset: 0;
  display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 12px;
  background: linear-gradient(135deg, #0d1225 0%, #0a0a15 100%);
}
.work-video-wrap .video-placeholder p {
  font-size: 10px; letter-spacing: 0.14em; color: var(--grey); text-transform: uppercase;
}

.work-info {
  padding: 22px 26px;
  display: flex; justify-content: space-between; align-items: center; gap: 16px;
}
.work-title {
  font-family: var(--font-display);
  font-size: 15px; font-weight: 600;
}
.work-tag {
  font-size: 9px; letter-spacing: 0.16em; text-transform: uppercase;
  color: var(--grey); padding: 6px 14px; flex-shrink: 0;
  border: 1px solid var(--border); border-radius: 100px;
}

@media (max-width: 760px) {
  .works-grid { grid-template-columns: 1fr; }
  .work-item:first-child { grid-column: auto; }
}

/* ============================================
   SERVICES
   ============================================ */
#services {
  background: var(--off-black);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}
.services-grid {
  display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px;
  margin-top: 64px;
  background: var(--border);
  border-radius: 14px;
  overflow: hidden;
}
.service-card {
  padding: 44px 38px;
  background: var(--dark);
  position: relative; overflow: hidden;
  transition: background var(--t-med) var(--ease);
}
.service-card::before {
  content: ''; position: absolute;
  bottom: 0; left: 0; right: 0; height: 2px;
  background: var(--blue);
  transform: scaleX(0); transform-origin: left;
  transition: transform var(--t-med) var(--ease);
}
.service-card:hover { background: rgba(37,99,255,0.06); }
.service-card:hover::before { transform: scaleX(1); }
.service-num {
  font-size: 10px; letter-spacing: 0.24em; color: var(--blue);
  margin-bottom: 28px; display: block;
}
.service-icon {
  width: 28px; height: 28px; margin-bottom: 22px;
  color: var(--blue);
}
.service-icon svg { width: 100%; height: 100%; }
.service-name {
  font-family: var(--font-display);
  font-size: 18px; font-weight: 600; color: var(--white);
  margin-bottom: 14px;
}
.service-desc {
  font-size: 12px; line-height: 1.85; color: var(--grey);
}

@media (max-width: 900px) {
  .services-grid { grid-template-columns: 1fr; }
}

/* ============================================
   PROCESS
   ============================================ */
#process { background: var(--black); }
.process-intro {
  text-align: center; max-width: 620px; margin: 0 auto;
}
.process-intro .section-tag { justify-content: center; }
.process-grid {
  display: grid; grid-template-columns: repeat(4, 1fr); gap: 32px;
  margin-top: 72px; position: relative;
}
.process-grid::before {
  content: ''; position: absolute;
  top: 23px; left: calc(12.5% + 24px); right: calc(12.5% + 24px); height: 1px;
  background: linear-gradient(to right, transparent, var(--border), var(--blue), var(--border), transparent);
  z-index: 0;
}
.process-step {
  text-align: center; position: relative; z-index: 1;
}
.step-num {
  width: 48px; height: 48px;
  background: var(--black); border: 1px solid var(--blue);
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-body); font-size: 12px;
  color: var(--blue); margin: 0 auto 28px;
  box-shadow: 0 0 20px var(--blue-dim);
}
.step-title {
  font-family: var(--font-display);
  font-size: 15px; font-weight: 600; color: var(--white);
  margin-bottom: 10px;
}
.step-desc {
  font-size: 12px; line-height: 1.75; color: var(--grey);
}

@media (max-width: 760px) {
  .process-grid { grid-template-columns: 1fr; gap: 48px; }
  .process-grid::before { display: none; }
}

/* ============================================
   FAQ
   ============================================ */
#faq {
  background: var(--off-black);
  border-top: 1px solid var(--border);
}
.faq-grid {
  display: grid; grid-template-columns: 1fr 1.3fr; gap: 72px;
  margin-top: 64px; align-items: start;
}
.faq-intro-text {
  margin-top: 24px; font-size: 13px; line-height: 1.85; color: var(--grey);
}
.faq-list { display: flex; flex-direction: column; }
.faq-item { border-bottom: 1px solid var(--border); }
.faq-q {
  display: flex; justify-content: space-between; align-items: center; gap: 16px;
  width: 100%; text-align: left;
  padding: 24px 0; cursor: pointer;
  font-size: 13px; color: var(--white);
  letter-spacing: 0.02em;
  background: none; border: none; font-family: var(--font-body);
  transition: color var(--t-fast) var(--ease);
}
.faq-q:hover { color: var(--blue); }
.faq-plus {
  font-size: 18px; color: var(--blue); flex-shrink: 0;
  width: 20px; height: 20px;
  display: flex; align-items: center; justify-content: center;
  transition: transform var(--t-med) var(--ease);
  font-family: var(--font-body);
}
.faq-item[data-open="true"] .faq-plus { transform: rotate(45deg); }
.faq-a {
  max-height: 0; overflow: hidden;
  transition: max-height var(--t-med) var(--ease), padding var(--t-fast) var(--ease);
  font-size: 12px; line-height: 1.85; color: var(--grey);
}
.faq-a > div { padding-bottom: 22px; }
.faq-item[data-open="true"] .faq-a { max-height: 240px; }

@media (max-width: 900px) {
  .faq-grid { grid-template-columns: 1fr; gap: 40px; }
}

/* ============================================
   CONTACT
   ============================================ */
#contact { background: var(--black); }
.contact-wrap {
  display: grid; grid-template-columns: 1fr 1.1fr; gap: 80px;
  align-items: start; margin-top: 64px;
}
.contact-left { position: relative; }
.contact-arc {
  position: absolute; pointer-events: none;
  border: 1px solid var(--border-soft);
  border-radius: 50%;
}
.contact-arc-1 { width: 420px; height: 420px; top: -120px; left: -120px; }
.contact-arc-2 { width: 290px; height: 290px; top: -50px; left: -50px; }

.contact-email {
  margin-top: 36px;
  font-family: var(--font-body);
  font-size: 13px; color: var(--grey);
}
.contact-email-label {
  font-size: 10px; letter-spacing: 0.18em; text-transform: uppercase; color: var(--grey);
  margin-bottom: 10px; display: block;
}
.contact-email a {
  color: var(--blue); text-decoration: none;
  transition: color var(--t-fast) var(--ease);
  word-break: break-all;
}
.contact-email a:hover { color: var(--white); }

.contact-meta {
  margin-top: 28px;
  font-size: 11px; letter-spacing: 0.06em; color: var(--grey);
  display: flex; flex-direction: column; gap: 8px;
}
.contact-meta strong { color: var(--white); font-weight: 500; }

.socials { display: flex; gap: 12px; margin-top: 28px; }
.social-icon {
  width: 38px; height: 38px;
  border: 1px solid var(--border); border-radius: 9px;
  display: flex; align-items: center; justify-content: center;
  color: var(--grey); transition: border-color var(--t-fast) var(--ease), color var(--t-fast) var(--ease);
  text-decoration: none;
}
.social-icon:hover { border-color: var(--blue); color: var(--blue); }

/* Form */
.contact-form-wrap { position: relative; }
.contact-form { display: flex; flex-direction: column; gap: 20px; }
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
.field-group { display: flex; flex-direction: column; gap: 8px; position: relative; }
label {
  font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: var(--grey);
}
label .req { color: var(--blue); margin-left: 2px; }
input, select, textarea {
  background: var(--dark); border: 1px solid var(--border);
  border-radius: 8px; padding: 14px 16px;
  font-family: var(--font-body); font-size: 13px;
  color: var(--white); outline: none; width: 100%;
  transition: border-color var(--t-fast) var(--ease), box-shadow var(--t-fast) var(--ease);
  appearance: none; -webkit-appearance: none;
}
input:focus, select:focus, textarea:focus {
  border-color: var(--blue);
  box-shadow: 0 0 0 3px var(--blue-dim);
}
input[aria-invalid="true"], textarea[aria-invalid="true"] {
  border-color: #ff5c5c;
  box-shadow: 0 0 0 3px rgba(255,92,92,0.12);
}
select {
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6' viewBox='0 0 10 6' fill='none'%3E%3Cpath d='M1 1L5 5L9 1' stroke='%23888899' stroke-width='1.4' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: right 16px center;
  padding-right: 38px;
}
select option { background: var(--dark); }
textarea { resize: vertical; min-height: 130px; font-family: var(--font-body); }
::placeholder { color: rgba(136,136,153,0.4); }

.field-error {
  font-size: 10px; letter-spacing: 0.04em; color: #ff8080;
  min-height: 14px; display: none;
}
.field-error.visible { display: block; }

.btn-submit {
  padding: 17px;
  background: var(--white); color: var(--black);
  border-radius: 8px; font-weight: 500;
  transition: background var(--t-fast) var(--ease), box-shadow var(--t-fast) var(--ease), transform var(--t-fast) var(--ease);
}
.btn-submit:hover { background: var(--blue); color: white; box-shadow: 0 0 30px var(--blue-glow); transform: translateY(-2px); }
.btn-submit:disabled { opacity: 0.6; cursor: not-allowed; transform: none; }

.form-note {
  font-size: 10px; letter-spacing: 0.04em; color: var(--grey);
  text-align: center;
}

/* Success state */
.contact-success {
  display: none;
  flex-direction: column; align-items: flex-start; gap: 18px;
  padding: 48px 40px;
  background: var(--dark);
  border: 1px solid var(--border);
  border-radius: 14px;
  text-align: left;
  animation: fadeUp 0.6s var(--ease) both;
}
.contact-success.visible { display: flex; }
.contact-success .success-icon {
  width: 52px; height: 52px; border-radius: 50%;
  background: var(--blue-dim); border: 1px solid var(--blue);
  display: flex; align-items: center; justify-content: center;
  color: var(--blue);
}
.contact-success h3 {
  font-family: var(--font-display); font-size: 20px; font-weight: 600; color: var(--white);
}
.contact-success p {
  font-size: 12px; line-height: 1.8; color: var(--grey); max-width: 380px;
}
.contact-success .btn-primary { margin-top: 6px; }

@media (max-width: 900px) {
  .contact-wrap { grid-template-columns: 1fr; gap: 56px; }
  .form-row { grid-template-columns: 1fr; }
}

/* ============================================
   FOOTER
   ============================================ */
footer {
  border-top: 1px solid var(--border);
  padding: 56px 0 40px;
}
.footer-top {
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 28px;
  padding-bottom: 40px;
}
.footer-brand { display: flex; align-items: center; gap: 14px; }
.footer-brand .nav-logo-mark { width: 34px; height: 34px; }
.footer-tagline {
  font-family: var(--font-serif); font-style: italic;
  font-size: 20px; color: var(--white);
}
.footer-nav { display: flex; gap: 32px; flex-wrap: wrap; }
.footer-nav a {
  font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--grey); text-decoration: none; transition: color var(--t-fast) var(--ease);
}
.footer-nav a:hover { color: var(--white); }
.footer-bottom {
  padding-top: 28px; border-top: 1px solid var(--border-soft);
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 16px;
}
.footer-copy {
  font-size: 10px; color: rgba(136,136,153,0.5);
  letter-spacing: 0.05em;
}
.footer-credit {
  font-size: 10px; color: rgba(136,136,153,0.5);
  letter-spacing: 0.05em;
}

@media (max-width: 640px) {
  .footer-top, .footer-bottom { flex-direction: column; align-items: flex-start; text-align: left; }
}

/* ============================================
   REVEAL ON SCROLL — subtle, premium
   ============================================ */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.reveal {
  opacity: 0; transform: translateY(24px);
  transition: opacity 0.8s var(--ease), transform 0.8s var(--ease);
}
.reveal.visible { opacity: 1; transform: translateY(0); }
.reveal-delay-1 { transition-delay: 0.08s; }
.reveal-delay-2 { transition-delay: 0.16s; }
.reveal-delay-3 { transition-delay: 0.24s; }
.reveal-delay-4 { transition-delay: 0.32s; }

/* Utility */
.visually-hidden {
  position: absolute; width: 1px; height: 1px;
  overflow: hidden; clip: rect(0,0,0,0); white-space: nowrap;
}
</style>
</head>
<body>

<a href="#main" class="skip-link">Skip to content</a>

<div class="grid-bg" aria-hidden="true"></div>

<!-- ============================================
     NAV
     ============================================ -->
<nav id="nav">
  <div class="container">
    <a href="#home" class="nav-logo" aria-label="Unfiltered Motion — home">
      <span class="nav-logo-mark">
        <!-- LOGO: replace src with a high-resolution SVG or PNG (transparent background recommended) for retina display -->
        <img src="data:image/jpeg;base64,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" alt="Unfiltered Motion logo" width="38" height="38" loading="eager">
      </span>
      <span class="nav-logo-text">Unfiltered Motion</span>
    </a>

    <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation menu" aria-expanded="false" aria-controls="navLinks">
      <span></span>
    </button>

    <div class="nav-links" id="navLinks">
      <a href="#works">Works</a>
      <a href="#services">Services</a>
      <a href="#process">Process</a>
      <a href="#faq">FAQ</a>
      <a href="client.html" class="btn-nav">Client Portal</a>
    </div>
  </div>
</nav>

<main id="main">
  <!-- ============================================
       HERO
       ============================================ -->
  <section class="hero" id="home">
    <div class="hero-bg" aria-hidden="true">
      <div class="hero-arc hero-arc-1"></div>
      <div class="hero-arc hero-arc-2"></div>
      <div class="hero-arc hero-arc-3"></div>
      <div class="hero-glow"></div>
    </div>
    <div class="container">
      <div class="hero-left">
        <div class="hero-tag">Motion Design Studio</div>
        <h1 class="hero-title">
          Premium launch videos<br>
          for <em>startups</em> &amp;<br>bold brands
        </h1>
        <p class="hero-sub">Your product, explained in seconds. We turn complex ideas into clear, cinematic motion that helps people understand — and act.</p>
        <div class="hero-ctas">
          <a href="#contact" class="btn-primary">Start a project</a>
        </div>
      </div>

      <div class="hero-right">
        <span class="showreel-label">Showreel</span>
        <!-- VIDEO: replace with your Vimeo or YouTube embed.
             Vimeo example: <iframe src="https://player.vimeo.com/video/YOUR_ID" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
             YouTube example: <iframe src="https://www.youtube.com/embed/YOUR_ID" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
        <div class="video-frame" id="heroShowreel">
          <button class="video-placeholder" type="button" data-video-embed="https://www.youtube-nocookie.com/embed/wv4isuuv9dM" aria-label="Play showreel" style="position:absolute;inset:0;padding:0;border:none;background:transparent;display:block;cursor:pointer;">
            <img class="video-poster" src="https://img.youtube.com/vi/wv4isuuv9dM/maxresdefault.jpg" alt="" loading="lazy" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;" onerror="this.src='https://img.youtube.com/vi/wv4isuuv9dM/hqdefault.jpg'">
            <div class="video-overlay" style="position:absolute;inset:0;display:flex;align-items:center;justify-content:center;flex-direction:column;gap:14px;background:rgba(5,5,8,0.35);">
              <div class="play-btn" aria-hidden="true">
                <svg width="18" height="20" viewBox="0 0 18 20" fill="white"><path d="M1 1l16 9-16 9V1z"/></svg>
              </div>
              <p style="font-family:var(--font-body);font-size:10px;letter-spacing:0.18em;text-transform:uppercase;color:var(--grey);">Play showreel</p>
            </div>
          </button>
        </div>
      </div>
    </div>

    <div class="scroll-hint" aria-hidden="true">
      <div class="scroll-line"></div>
      Scroll
    </div>
  </section>

  <!-- ============================================
       TRUSTED BY
       ============================================ -->
  <div class="trusted">
    <div class="trusted-track" id="trustedTrack" aria-hidden="true">
      <span class="trusted-label">Trusted by</span>
      <span class="trusted-item">SaaS Startups</span>
      <span class="trusted-item">App Founders</span>
      <span class="trusted-item">Bold Brands</span>
      <span class="trusted-item">Tech Companies</span>
      <span class="trusted-item">Product Teams</span>
      <span class="trusted-item">Growth Agencies</span>
      <!-- duplicate set for seamless marquee loop -->
      <span class="trusted-label">Trusted by</span>
      <span class="trusted-item">SaaS Startups</span>
      <span class="trusted-item">App Founders</span>
      <span class="trusted-item">Bold Brands</span>
      <span class="trusted-item">Tech Companies</span>
      <span class="trusted-item">Product Teams</span>
      <span class="trusted-item">Growth Agencies</span>
    </div>
  </div>

  <!-- ============================================
       WORKS
       ============================================ -->
  <section id="works">
    <div class="container">
      <div class="works-header reveal">
        <div>
          <div class="section-tag">Portfolio</div>
          <h2 class="section-title">Selected <em>works</em></h2>
        </div>
      </div>
      <div class="works-grid" id="worksGrid">
        <!-- Work items injected via JS — see PROJECTS config near end of file -->
      </div>
    </div>
  </section>

  <!-- ============================================
       SERVICES
       ============================================ -->
  <section id="services">
    <div class="container">
      <div class="reveal">
        <div class="section-tag">What we do</div>
        <h2 class="section-title">Services built for<br><em>high-growth</em> brands</h2>
      </div>
      <div class="services-grid">
        <div class="service-card reveal reveal-delay-1">
          <span class="service-num">01</span>
          <span class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><polygon points="5 3 19 12 5 21 5 3"/></svg>
          </span>
          <div class="service-name">SaaS promo videos</div>
          <p class="service-desc">Motion-driven product videos that turn visitors into users. Built for app launches, Product Hunt drops, and landing pages.</p>
        </div>
        <div class="service-card reveal reveal-delay-2">
          <span class="service-num">02</span>
          <span class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><rect x="7" y="2" width="10" height="20" rx="2"/><line x1="12" y1="18" x2="12" y2="18.01"/></svg>
          </span>
          <div class="service-name">Short-form reels</div>
          <p class="service-desc">Vertical content engineered for Instagram, TikTok, and LinkedIn. High-retention edits with motion design built in.</p>
        </div>
        <div class="service-card reveal reveal-delay-3">
          <span class="service-num">03</span>
          <span class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
          </span>
          <div class="service-name">VSLs &amp; sales videos</div>
          <p class="service-desc">Video sales letters designed to move people through your funnel. Cinematic style, built with conversion in mind.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================
       PROCESS
       ============================================ -->
  <section id="process">
    <div class="container">
      <div class="process-intro reveal">
        <div class="section-tag">How it works</div>
        <h2 class="section-title">From <em>brief</em> to<br>final delivery</h2>
      </div>
      <div class="process-grid">
        <div class="process-step reveal reveal-delay-1">
          <div class="step-num" aria-hidden="true">01</div>
          <div class="step-title">Discovery</div>
          <p class="step-desc">Fill out the project form. We align on your brand, goals, style references, and timeline in a short call.</p>
        </div>
        <div class="process-step reveal reveal-delay-2">
          <div class="step-num" aria-hidden="true">02</div>
          <div class="step-title">Concept &amp; script</div>
          <p class="step-desc">We develop a visual concept and script. You approve the direction before we touch a single frame.</p>
        </div>
        <div class="process-step reveal reveal-delay-3">
          <div class="step-num" aria-hidden="true">03</div>
          <div class="step-title">Production</div>
          <p class="step-desc">Motion design, editing, colour, and sound — built frame by frame in After Effects.</p>
        </div>
        <div class="process-step reveal reveal-delay-4">
          <div class="step-num" aria-hidden="true">04</div>
          <div class="step-title">Delivery</div>
          <p class="step-desc">Revisions and final exports in every format you need, delivered on time, every time.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================
       FAQ
       ============================================ -->
  <section id="faq">
    <div class="container">
      <div class="faq-grid">
        <div class="reveal">
          <div class="section-tag">FAQ</div>
          <h2 class="section-title">Frequently<br><em>asked</em></h2>
          <p class="faq-intro-text">Still have questions? Reach out through the client portal or send an email — happy to help.</p>
        </div>
        <div class="faq-list reveal reveal-delay-1">
          <div class="faq-item" data-open="false">
            <button class="faq-q" aria-expanded="false">
              What does a motion video typically cost?
              <span class="faq-plus" aria-hidden="true">+</span>
            </button>
            <div class="faq-a"><div>Pricing starts at $800 for short-form reels and $1,500+ for full SaaS promo videos. Final cost depends on length, complexity, and style. Fill out the project form for a custom quote.</div></div>
          </div>
          <div class="faq-item" data-open="false">
            <button class="faq-q" aria-expanded="false">
              How long does a project take?
              <span class="faq-plus" aria-hidden="true">+</span>
            </button>
            <div class="faq-a"><div>Standard turnaround is 3–7 days depending on scope. Rush delivery is available for an additional fee. Your timeline is confirmed after the discovery call.</div></div>
          </div>
          <div class="faq-item" data-open="false">
            <button class="faq-q" aria-expanded="false">
              How many revisions are included?
              <span class="faq-plus" aria-hidden="true">+</span>
            </button>
            <div class="faq-a"><div>Every project includes two rounds of revisions. Additional rounds can be added if needed. A thorough brief process means we usually nail the direction on the first draft.</div></div>
          </div>
          <div class="faq-item" data-open="false">
            <button class="faq-q" aria-expanded="false">
              How does payment work?
              <span class="faq-plus" aria-hidden="true">+</span>
            </button>
            <div class="faq-a"><div>50% upfront to secure your slot, 50% on delivery. Payments accepted via Stripe, Wise, or PayPal.</div></div>
          </div>
          <div class="faq-item" data-open="false">
            <button class="faq-q" aria-expanded="false">
              What do you need from me to get started?
              <span class="faq-plus" aria-hidden="true">+</span>
            </button>
            <div class="faq-a"><div>Your brand kit (logo, colours, fonts), product access or screen recordings, and any style references. Fill out the client portal and we'll guide you through the rest.</div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================
       CONTACT
       ============================================ -->
  <section id="contact">
    <div class="container">
      <div class="contact-wrap">
        <div class="contact-left reveal">
          <div class="contact-arc contact-arc-1" aria-hidden="true"></div>
          <div class="contact-arc contact-arc-2" aria-hidden="true"></div>
          <div class="section-tag">Contact</div>
          <h2 class="section-title">Let's <em>work</em><br>together</h2>
          <a href="https://calendly.com/leyanshedits-business93/30min" target="_blank" rel="noopener" class="btn-primary" style="margin-top:32px;">Book a call</a>

          <div class="contact-email">
            <span class="contact-email-label">Email</span>
            <a href="mailto:hello@unfilteredmotion.co">hello@unfilteredmotion.co</a>
          </div>

          <div class="contact-meta">
            <span><strong>Response time:</strong> within 24 hours</span>
            <span><strong>Starting price:</strong> $200</span>
          </div>

          <div class="socials">
            <a href="#" class="social-icon" aria-label="Instagram">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor" stroke="none"/></svg>
            </a>
            <a href="#" class="social-icon" aria-label="X (Twitter)">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.744l7.737-8.835L1.254 2.25H8.08l4.253 5.622 5.911-5.622zm-1.161 17.52h1.833L7.084 4.126H5.117L17.083 19.77z"/></svg>
            </a>
          </div>
        </div>

        <div class="contact-form-wrap reveal reveal-delay-2">
          <form class="contact-form" id="contactForm" novalidate>
            <div class="form-row">
              <div class="field-group">
                <label for="cf-name">Name<span class="req">*</span></label>
                <input type="text" id="cf-name" name="name" placeholder="Your name" autocomplete="name" required aria-required="true" aria-describedby="err-name">
                <span class="field-error" id="err-name" role="alert">Please enter your name.</span>
              </div>
              <div class="field-group">
                <label for="cf-email">Email<span class="req">*</span></label>
                <input type="email" id="cf-email" name="email" placeholder="your@email.com" autocomplete="email" required aria-required="true" aria-describedby="err-email">
                <span class="field-error" id="err-email" role="alert">Please enter a valid email address.</span>
              </div>
            </div>

            <div class="field-group">
              <label for="cf-budget">Budget</label>
              <select id="cf-budget" name="budget">
                <option value="$200 – $500">$200 – $500</option>
                <option value="$500 – $1K">$500 – $1K</option>
                <option value="$1K – $2K">$1K – $2K</option>
                <option value="$2K – $5K">$2K – $5K</option>
                <option value="$5K+">$5K+</option>
              </select>
            </div>

            <div class="field-group">
              <label for="cf-message">Project details<span class="req">*</span></label>
              <textarea id="cf-message" name="message" placeholder="Tell me about your project, timeline, and goals..." required aria-required="true" aria-describedby="err-message"></textarea>
              <span class="field-error" id="err-message" role="alert">Please tell us a bit about your project.</span>
            </div>

            <button type="submit" class="btn-submit btn-block">Send message</button>
            <p class="form-note">We typically reply within 24 hours.</p>
          </form>

          <div class="contact-success" id="contactSuccess" role="status" aria-live="polite">
            <div class="success-icon" aria-hidden="true">
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"/></svg>
            </div>
            <h3>Message sent</h3>
            <p>Thanks for reaching out — we'll get back to you within 24 hours. Want to skip the wait? Book a discovery call and we can talk through your project live.</p>
            <!-- CALENDLY: replace href with your scheduling link -->
            <a href="https://calendly.com/leyanshedits-business93/30min" target="_blank" rel="noopener" class="btn-primary">Book a discovery call</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<!-- ============================================
     FOOTER
     ============================================ -->
<footer>
  <div class="container">
    <div class="footer-top">
      <div class="footer-brand">
        <span class="nav-logo-mark">
          <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/4gHYSUNDX1BST0ZJTEUAAQEAAAHIAAAAAAQwAABtbnRyUkdCIFhZWiAH4AABAAEAAAAAAABhY3NwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAA9tYAAQAAAADTLQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAlkZXNjAAAA8AAAACRyWFlaAAABFAAAABRnWFlaAAABKAAAABRiWFlaAAABPAAAABR3dHB0AAABUAAAABRyVFJDAAABZAAAAChnVFJDAAABZAAAAChiVFJDAAABZAAAAChjcHJ0AAABjAAAADxtbHVjAAAAAAAAAAEAAAAMZW5VUwAAAAgAAAAcAHMAUgBHAEJYWVogAAAAAAAAb6IAADj1AAADkFhZWiAAAAAAAABimQAAt4UAABjaWFlaIAAAAAAAACSgAAAPhAAAts9YWVogAAAAAAAA9tYAAQAAAADTLXBhcmEAAAAAAAQAAAACZmYAAPKnAAANWQAAE9AAAApbAAAAAAAAAABtbHVjAAAAAAAAAAEAAAAMZW5VUwAAACAAAAAcAEcAbwBvAGcAbABlACAASQBuAGMALgAgADIAMAAxADb/2wBDAAUDBAQEAwUEBAQFBQUGBwwIBwcHBw8LCwkMEQ8SEhEPERETFhwXExQaFRERGCEYGh0dHx8fExciJCIeJBweHx7/2wBDAQUFBQcGBw4ICA4eFBEUHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh7/wAARCAQ4BDgDASIAAhEBAxEB/8QAHAABAQEAAgMBAAAAAAAAAAAAAAECAwQFBgcI/8QAWxABAAIBAgMEBQcGBwsJBgcBAAECEQMEBSExBhJBUQdhcYGREyIyobHB8AgUQlLR4SM0YnJ0gpIVJDNDRJOio7TC8RYlJ1Nzg7KzwzU2N0VjpBcmVFVkZYSU/8QAGwEBAQEBAQEBAQAAAAAAAAAAAAECAwQFBgf/xAA6EQEBAAIBAgMECAYBAwQDAAAAAQIRAwQhBRIxMkFRcSIzYYGRscHRBhM0cqHwIxQkUkJi0uE1ovH/2gAMAwEAAhEDEQA/APxkA0AAAAAAAAAAAAAAAAACaABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAaAAAAAAAAAAAAAAAAAAAAABNAAgAAAAAAAAALoBcLFWpjaMjljStNe9FZx54Ymq3jsTbIuEYsUAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAGgAAAAAAAAAAAAAAAAAAAAAAAAAAAQADQC4WIamOxMLFct0pMy7entqzfuRb53TnHi9HHwXJm5adaulblOJ5uzGjSIrFu9FsZmXappXjV5Z7nq5xiGqzS+rN76ccufLk9uHBMXO5Otr6M0mK6cxPdjw65deZ8L1iftdjWrFrTNbxMz58nHM6lYxeMx64ymU7kcM6dLfRtj1SxfRtXrHLz8HY/g7edZ+MLFLxzpPej+TP3OV4pk1t0pqmHcnuz9OnPzjkxOjFvoWifVPKXHLp/gvmdUc19K1ZxNZj2uOauGXHZ6tbZFwjGlAE0ACAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0AAAAAAAAAAAAAAAAAAAAAAAAAAALEGhFiGqxMziHLo6ebRmOXWXbDiuSWuOlJtMR4y7OhtrWvERzj1c3Lt6aeZmYmMRnzc2jpRFbWraPKOeHu4+CRzuTOhH8Jm1KzEc+jm0a6fzr86zEe3m1WNSmlm0TMTOIzGY/HRrNI0oiaYmefKfx63qmOnO006WrS16WiZnlGJ5s6l5ppYvWJm0+MYnH4+xyXrXFaVvzx0nzlxbq2pWe7Hzq15ecLe0HUv8naes1n180iupH0Ld6PVP3E2rP0qY9kndrP0b/Hk89bTNZ+nSPbHJYpWfo35+U8mpnUiPnR3o855/Wn8HPWJr7OZoWflIj59e9Hr5/Wz3dO3nSfXzhyUraP8HeJ9k4JnE41NPn6uUrpGYpqRHzcXr5Rzj4OO1NO3Ws1n1OaK1nnS+J8p5NW+UiM6lIvHnP7YLjKbdO22mfoTF/Z1+DhtpzHg8h3NO3SZpPr5wtqamM2rGpWPHr9fg5ZcGNamTxc1TDyFtHSt50n184cOptbxGYjvR5xzebPprPRqZuoOWaTHgxNXC8djW2RcIxpQBNAAgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAANaAAAAAAAAAAAAAAAAAAAAAAAAAFjqBEOTTp3pwmnEZzMZiHY0u53bTMTHhyeri45e9ZtXR0eczE1nEebsaUalKWm0TMYxGYcdIpGnMxbGZ8Yc0ReunWKzznnyl7sMZPRytapNY0udI5z4Thvu07lYi0xM8+cJa1omtLVicR4w3E6dtXE1nEeU+EO0Zb7l4mtaWiZiPCWpmZ1sXrE1jzjHKGKd2bWv38Y5848WqfKV05ms573KIiWohFqTa2paLVmOfLzdPUjNs0vGfbh2Ne8104rekZnnPLDp2nTmf0q/W551qQtOpHO9e9HnMfen8HPWJr7OZWJic01Iz7cLM3iM2pEx64+9yaK1mJzTUjPtw1M2j6enEx5zDMfJz1i1fZzbpEx9DUj44aiJjTn9av1t1jUiMUtF48uv1Sk96IzfTiY88Y+wiNOf1q+3movzc4vp4n1cmqRic6epifXylY7+MVvW8R4dfqknuxOL6c1n1cvtXSLbMf4TSiY84jBWtM5peaz6/2rSMf4PVx6p5NzExzvpRMfrRy+zk1pGbRfGdSkXj9aP2wxFKTOaWmk+v9sOWsVic01JpPr/bDWLYzalbx5x+2PvNG3BfSnGdTTi8frR+2PvcFtrp2+hbE+Vv2u9WK5zS9qT6/2w1NJmM3063j9av7vvS8cqzLTw+rtdSnOa8vPwcNqTHg858nXn8nqTWZ6xLj1dvExnU0v61eX7nnz6WX0ambwk1TDyeps4n/AAd4n1Tyl1dXb3pOLVmPbDy59NlG5nHVHJNJhmYcLhY1tkXCMaUATQAGgATQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAANgAAAmgAAAAAAAAAAAAAAAAAAAAWEahZBun0Zn3NxypHrlmPoxDVvCPU9uE1GG5nEVj1OTvTOpFemOTijnq+cR9kLSfpW9TtKzp2dLXvF5tFpjHPk3p6+KWm0Vnw6OpE4pPrlqZ5Vr73SZ1NO58rp/JxE1mJtOeU/j1t27kzWlb49seLpd6J1PVX7mflJxa8zz6fFr+YnldnX1bzae7fNekRn7nXteYn5+nHww61rznqV1bV6TMe958ueWtTF2InTn9aPrapy501MT8JdeNafHE+2Go1KeNceyVnJiadqPlPGsXjxnGfrgiaT1rNZ9UuvW9PC0xPrhzV1L+F62iPOf2ukylTTkriJzTV7vt5Nx8p40rePVz+xxd7lHf0sR5xyInTnpNq/W3tHJHyc9YtWfVzclO9jFNWJjyn9/JiLWnpqVv7f3tdIzfSmI845NRlvHLN9Ll5xy/cte7E5pqWpPr/czSaxOa6lqz6/3OWO9MdKan2/tagRF560rqezr9RHczym1J+KYrE4tW9J+LkibTHLUrb1W/e0ixF7eFNX7f2rEVieXf07Qd2MZtpzWPOs8m6zyxXUiY8IvDUgndtbwpq+zr+1IisT821tOfW5JpyzbSxHnWeSxzjEakWjyvC6RxW08xm2nFo86MfJRMYreMfq3jl+x2e5Ec5pan8qvOPx71xNvGmp/O5SeTZt43W2lJ+lpzTPjXnEupqbG36GL+zr8Hm5pFZx8/TmfCecSxfRi3WkW9dP2OWXBK1Mq9dvo2rPOJcc1mHsN9GL8s1v6rxifj+91tfZU8rac+uMw8ufSfBucjwswmHf1tlqViZiO9HnHN1raVo8Hkz6fKOkylcA3NZSYcLhYu2RcIzpQAABAANAAaABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAbAAAAAAAA0ACAAAAAAAAAAAAAAA0kNVjNohvCbqVyYzMRDVeepny5s1+lM+9Y5Vmfc9uLC1+jafcvSkeuU6UiPPm3j58V8IbhSYzatVifnzfy5x9yRPO1vxzOlPbLSEcqTPnycetOKxX3uS0fOivhHX73X1Ld60y5cmWosZCWXhtbaGQ2rWZai0sZMtTOxNOWuras5i0x7JcldxbxmJ9sOuOuPPlE8ruV16TjNPhLk09akc63tWXj8rFpdcepvvZuLy1dWZ5d/Tv7f3uSLRjM6UxHnWeTw8Xlumtas5i0w7Y9TPezcHmKXrjFdWY9UxybiZn9HTv7JxLxVd3qeMxb2xly03df0qR7pw7Y82NZuNeTrMUt/jNOfx7HJSc+Onf28p+Lx+lu6R0venq6uemvW2PnaVv8AR/Y7Y5ys6dyIiMWmt6euObUT3v0qX/nRifj+9waepjnWL19dZzDlrq1t+nS386uJdJYjlrHd+djU0/XHOGojvf8AV3/0ZYp1zWtonzpbOG4tEzztWf59cT9TcRZr3Yx8+mfC0ZiWZ089Kxb10nE/By0zH0YvHn3J70ExW3/V29vzZ/Yuk24ZjM4m0W9V4xPxSdPux0tWPjWXYmsxHPvRHh3o70fFK155rHPzpb7pPKu3UnRiZzFYmfOk8/g4NTbVv1itvb82XkrUrM4nuzPrjuyl9Pl87OP5cZj4sXjlNvB6+wjPzZms+VodLW2mpTrWcefg9m+S5conHq+dHwcc6ETnux1/Un7pcM+mxybmdj1W2nMeDE1l7Hq7Kl8/NiZ9XKfh+x09fh0xM92eflPKXkz6O+5ucjw8wmHc1trek4tWYn2OC2nMeDyZcGUdJk4RuapMONwsXbIuEZ0oAAAAAgAGgAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABcI2AAAAAAAAAAAAAAAAAAAAAAAALDen1yy3T6My68U7pWq/Rmfcs/RiPPmk8qw3EfwmPJ65GFx8/HhHUjpaxXpMnhEebcRZ+jEefNf0/VUj6cz4VTpT2qMWnFZnz5OCerl1p8PJxPJzZd9NRJRZR5mwAAABcmDAKJhQAF2GVzKDUyqaai0tRqTHi4xucliadimves8rOxp7/Wjrbve3n9rx+Vy649RlEuMeX0+IR+lSvtjk7WnxDTnETe8RHhOLQ9fizUXl6MerrF449lputK0Z72nM++s/sdmut3vG0x7rvU66to8XLTc3jpLvj1cZvG9qpqUzGJrE/ybTWfrb5TGZ5x52ry+MPWtPiOtGIm8zHlPN2dLicxOZrXPnHL7HfHqcazcK89WcxiJzHlE5+qWoiInwifbNZ/Y8Tp8T07fSmfXM4s7OlvtKYxF4iPLMxn7YdseTG+9nVd2aR1mI9sxj64Tud7rHe9vzvrjm49PXrM5rMZny8Ph+xyxqUmesTjzxn7pbmqyzOnFoxHP/S/fDFtGJjEfCOf1TzdjMTjvfX+/9rWImOfTwz0+v9q+WU28ffbRMd3Hujn9Uunr8OpaZxXE/wAn9kvOTSMerw8vr5fWk6UTHPp4eX18vrYy4ZVmVj1bW4beM9353qjr8HS1Nves84l7nfbxMc45eGf3/tdfW2dbRi1c+38ZebPo5fRucj062nMeDE1ezbjhVZme7ExPx/e8dr8O1K5mK5jzh4uTo7HSckeJmEw7ept7V6w4bacx4PJlwWOkycI3NUmHG4WLtkXCM6UAAAAAQADQAIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAANJhRsTCNICC4QAAAAAAAAAAAAAAAAAABYRoByR9GHHHVyxGbRD08UZrUR8+I8lr0mUr+lZf0Y9b0xmr4RDUfTmfCvRP0pn9U/Q9stIdKeuZLcrY8Kws/T9VY/H1uPUnFPamV1Bw3nMoDwZ3ddIJhRzVMGFAAAAAAF0ABoADQAKAAAAmjJkF3UXvLFpZGpnRyReW661o8XAZbnLYmncpubx4y7GlxHWrGO/OPLLxmV73rdsepyiXCPO6PFr1nnj3cvsdvR4tTlmMT5w9Yi0tRqTHi74dZlGLxx7jpcR0LT9KIn1/j73a09zpW5xeJn28/2vR661o8XNTd6lf0penDrfixeN7xW1ZnlPP62orWeUPTtHiWrTlF5j3u7o8Z1IiImYmPKXpx6vCs3jr2SdKsx4Y+r8e5x320W8Of49/wBjxuhxus/SrGfVPR3tHim2viJmY88+LtOTjy97OrHDr8O07xOax7fx+943c8H69z4S9j0tzt9TExqVz7ejmjTpaOWDLgwzJlY9E3HDtXT61l09Tb2r1h9Evs63zyzl0dzwjTvnFcPJyeH79G5yvQ7acwzNZe1brgd4zNYy8VuOG6unMxNZj3PBydFlj7nWckrxEwmHc1NtavWsuG2nMeDyZcFjpMnDhHJNZSYcbhYu2BcGGdKgCAAgAGgAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAaAbAABFATCNAJBhQGRoBkaAZGgGTDQCYMKAmDCgJgwoAAsFrzly16zLj0+uW45VevinZitR9H2y30t7GY+lEeUL+jM+bvGT9H2y30t/NhI+lEeUH6PtloSfo+uZcOtPPHlyc1pxMz+rHJ1rTzcebLU0sQB4q3ABNKAKAAAAmwANgAbAAADQAGkAF0ABoADQAGgAAMgouTPrQN0bi0rF5cZluZ2GnNXVmPFy03F48XVyZbnNYnleR097qV/Sl29vxXVpPK8x7JeEiZWLS749VlGbhHte24/rVxm+fbzeT2/aClv8Jp1n2Th6HGpPm5K61o8Xrw8Qynvc7xR9G0eJ7DVj52azPqy5/kdhuYxXV0p9Uzj7XzjT3epX9J29HiepX9KXrw6/G+1GLxX3Pcd12epqV71K4jzjnDw287P6tMzFMx6nBtOO62lMTXVtWfOJw8vte0+rMRGrNNSP5dYn6+rfm6fl9ezOs49Y3HC9Skz82XS1dpevWsvoVeKcK3cY3G1isz46dvun9rOpwvhW7jO33dKzP6OrHd+vo5Z9Bhn7F21OWz1fOLaUx4OOaS963vZjWrXvVpFqz0tWcx8Xhd1wXWpn5lo9zxcvh+ePudMeWV67NUmHk9bYalf0XVvt7R1h4s+myjpM46uEc1tOY8GZrLheKxvbjGphMOdxqoLhEABNAAgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0A2AAAAAAAAAAAAAAAAAAAAAAADUSt06S3EZ7sM1+jDcfSn1Q9uE7MVY/SlqI5xHvlIjlEeax+lPuh1iL4TPjJPKf5sEdY9UZSekR5yo49ScViPPm4W9WczLDx8t3WoAODQAGwAAA0gAugAAAAAUADQAGgANAAaAA0ABoADQAGgANAAAAgGQAyuUF2NRMrFpYGpnYacsak+bkrrWjxdfJluctiad7T3d69LS7ehxPUp+lLw8TKxaXfDqcozcI9q2XH9fRnNNW1Z9U4eW0O0WnrRjc6WnqeuI7s/V+x6DGpMeLkprWjpL2cfiGc97neKPoM34Xu4zFopafC8fe6254Po2rmtYmP1qzmHp+lvdSv6Uu/teMa2lOa6lo9kvROr48/ajHks9Hd3PBqxmY+x47X4Ves8oy8voccreMa1a29ccpdmu52mvHzbxEz4TyLxcPJ6Hmyj1PV2OrXPzJda+haPB7lq7elvCJdPW2tZ8M+3m8+fRz3Nzkeq205jwZmsvYNXZUnPzYdTV2MR0zDx59JY6TkeJmEw72ptLRzcNtvePDPs5vPl0+UamcdYcs6cx4MzVxvHY1tgXBhi4qgCaABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABoB1ABNAAgAKABoADQAGgANAAaAA0ACgAAR1Fr1awm6y5K9Yajp7ZSOst18I973YxlfGfVCxHKI98pHT2yvnPuh0iHWJnxmWbzjM+XKGp5e6HFqzyiPezndQjit1QkeDK7rYAzoAAAAAFAA0AC6AAAAABdABg0AuDBoQwoaEwuANBgA0ABoADQAGgANAYA0GEwomhMCiaEFwYNCBgQDIAuTKBujUSsWlgy1M7DTmrqzHi5tPc3r0mXUyZdceaxLjHl9vxPV0+UXnHk72lxWl4xqR74etxaWovMPTh1eUYvHHtVdfS1fo2hm9Yl65TXtHi7Ojv9SvW2fa9GPVY5erFwseTvpR5c3X1NGJzyTT31LcrcnLGpS/OJiW945eid46l9H4OG+hHln3fseQtiXFesTzn8fj2uWWErUrx1tGPxLjto49Xth5C9fP6/wB7jtTHq+pwy4ZWpk6E6c+WWZrMeDuWp6vq/YxNfL6pcMuCNTJ1MJh2bUj1e+MMzT1fByvDWvM4ByTSPP4szVyvHV2yLMTCYZuNUAZAAAAAAAAAAAAAAAAAAAAAAAAAAAAGgHUAAAAAAAAAAAAAAAAAAABNgADWn1Zbp0duOd0rcdPbLfnPuZr1j1RlqI6R5vZjGGo5e6CPD4nX3ydc48ZxDSJPTn485cF5zMy5dSeU/CHBZw5svc1igDyVoAAANAAoAAALoADQAYUBcBo2mFwC6TYAaNgBoAF0ABoBQ0IKGhADQAGgATQAGjYAml2AGgATQAJoMJhRNCCpgABNAAihkAXJlBfNTTcWlumtas8pmHCZbx5bEsd7T3do683PTc1t44l4vKxZ3x6m+9m4R5XvxPSeqTjweOpq2r0ly13Hm7TmxrPldiY8fx9TFoz6/rSNWtvFZnM+bW5UYmPL6pZmPPH2OSefr+tmfV9X7GLFccx7cfFmY9jkmOfh9iTH4lzuLW3FMY84Zx7Jcsx5fUzPtj3udxXbjmvqSauSY9XwSfb8XO4RduPBhvHqTDncF2wNY9hhm4qyKjOgAQAAAAAAAAAAAAAAAAAAAAaAdQAAAAAAAAAE2ABsADYAAAIAAALIEOSvT2uOOrmr4PRxRK1Hi14z6owlfD4rHhnx5y9UjK9PdBPL3Qe3xnMpaeX1y0jj1Z548nDPVu0sPFyXddIAOQAAALoADQAYUBcBoMGAU2ALpAUwaEGsC6EMKGhMGFF0GADQAGgANAAaAA0BgDQmDChoTBhRNDI0YNDIuDCaEATQAJpdgBoAE0BgE0IKmEABNAAi7AE0oAgGRMrs01Fm66kx4uLJlucliadiNWJ6t9+J9bq5WJl1nP8AFnyuznP4yns+pwxefHm1F4nr9bpOSVNNzj1fYk/jJnl+JM/iC9xmY9XwT3/Fpn3/ABZsVJj1J72vqT4SxYrMx6k97SSxYIYPce9ixUFRnSoKiaABNAAgAAAAAAAAAAAAAA0A6oABsAAAEAAAAAAAAADQALoAAAFgtXNHj8HHSOcOWsdHr4p2Zqx4/Brz+CV8PiseHxeiMnnHuY1J5e1ueUeyHDqTz9jPJdRY47Iso8NbAE0AAAYXCiLgF0AAAphdIi4UUTCgugANAAugANAGFwqIKobTBhQEwYUNCYMKGhMGFDQmDChoZwNCaGRTBoQXCYFAEBMKGhMI0JoZFwiaABNGwBNKAJoEwozoQWYRAATSgAokwoyMizCAAAuTKBsaiWot5uMamdiac3ez+8z6/i4srFm5yppyev7En3SzFlznylrzSmj4wAgiNJLNggDNioKnuZUQEAAABkAAAAAAAAAAAAaAdWQAAAAAAA0AC6AA0AAAAAAAAAENSDko5IYpHJyR9728c7M1f+DX2Z+pI/evq9ztGWbTyz73BZyas8va4p6vPzZe5rGMz1CR5mgFwCLgFABQFMGjYYUVABdAAugAXQAYXQGFwppNpgUNAAujQAaADBpQMGF0gLgwaNoLgNG0FMJo2guDAbQMGE0AYDSiYUNCYRoTQyLgwmhAEEwKJoZFwiaABNGwBNKAM6EFSYTQAJoAEXYAipKNJMIIAaABAAAXKANRZYlgamVNN5MsLlfMml9wZgXYHsBmqnuRfeJRAEAAABNAAaABAAAAAABoB1ZAAAFAAAAAAAAAAAAABQAUFhGobxncclOjkhmsfsbjz9724zsxVhJWPJm88nS9oji1JzLjWyPDnd10iSuAY0AAAC6BYgiFU2ALpABdAAugAXQGFwqptFA0AGF0AuBdG0MKGjaYXAGkAF0AGDQC4MGhBcGDRtBcGDRtBcGE0IGA0ACaDCYUTQmBQXaBgTSoYUTQyKYTQgCCYRoTQyKiaABnS7AE0EwikwzoQBAARQBNKkwjSTCCAAAIAAAAAAACbFyZQXYvtgQXYqKiAAACggqAAJQAQAAAAaAdmQAAAAAAAAAAAABQAUAAAAI6t06sw3R2453K5KtwzVuHtxjnSeji1Zctujr3nM5Y5bqLGZ6oDx1sANAAoLEEKukAFABQAXQAsQqEQKGgDC4a0IuANGwBUBcGF0INBo2mDCi6TaYUMLoAwuDQguDBoQXBg0ILgwaEFwYTQgYDQJhRNCYRoTRtkXBhNLtAE0GEUTS7QXCJoRMNCaVkWYRASYUTQyNTCM6EATQAM6UmEUlBAGQARQBFSYRpJhBAAAEAAAAABAAQAAADYALsFRVgHiCiAIADIAAAA0A7MgAAAAAAAACgAugAAAAAAAhRYcmnDEOWnR6OKd0rdW4ZrDT2RzY1JxDry5dWcy4p6vLy5breMQBxaAAFiCIVSgC6QAUAGtAEKqCi4NImFBrQAAC4VdCYUF0bBcC6RFwC6QwC4XRtBcLg0MqoaEwYXBg0bTBhcGDRtMGFwGjaYMKGjaYRoTQyYawmDSphGsImhBcJhNAmFE0MjSTCaXaAM2CTAoi7RFE0qTCNJMM6RAEVJRpJhLBAGbAAZsUmEVJhAAZABFAEVJRpJQQAABAAAAAAQAEAAAAABYCoKAAACUAEAAGgHZkAAAAAXQAKAAAAAAAC6ABQWEUgsdXNSHFSObno9fDGcmqwXnELHRx6s8not1GI4rTzYWUeHK7dIAMqLAqmwBpABdAAugIIaVAiCIVdIALoBYhVEwoYa0BhRdIYAVNguFiDQhhrAukTC4UXQmBQ0AYMLoAwuDSbQXBg0bQXBg0bRGsJhNG0wYXBg0rOBpE0ILhMJpdpgUTRtkwuDBpWRUwzoEmFE0MizCM6USYUZ0IEwI0kwjSJYiAMqkwjSTCWCAMgAipIqMgAyACKAJVSYRpJhBAAAEAAAAABAAQAAAXxa0IAAAAAyAAAANAOzIAugAUAAAAAAAAAF0ACgBEAsANSDdIc9YcWnDnrD28U7MVfB19Wcy59ScVda08zluppMWZ6oDyOkAWFRYAUAFABdARCxCtJsIghVkQBYhRFwougCIVdBgBrTILhV0JhYhYhV0iKGF0AuBdCYXAuDSbQawYXSJgw1gwaGcGGjHqNG2cK1gwujbKYbwYTRtjBhrHqMGjbODDWEwDJhpMJpWcDWETRtkw1hE0rIphNDOBRnSso1hE0qBMCWDI0kwzYqEwDNggswiNIjSM2IgDKpMI0kwlggDNgEgyqBIgAMgAigCVUlGklBAAAEAAAAABAANC+R5qNjK+J4olABAASgAgAA0A7xkAUAAAAAAAAAFABQBYgCIAUFjqi16t4zuVzaccnNXo49OHJ0h78JqOVcWtPg4JcmpOZccvNy5brc9EAcVVUhWgAUAGgWIIhVQBYVAFiFCIUF0BEEQrWk2AsQ1pBcCxC6RIhVFAwuBdBgXCxC6RMLEKLpDAuDC6TaLhcLg0M4XDWDC6RnC4awYNG2cGGseox6jRtnBhrHqMeo0bZwmG8GDRtjCYbwYTQxhMN4TCaXbOEawYTS7YwjeEwgzhGsIml2yjUwM6VlJhqYRNLtkmGkTSsizCM6EmEaSYZsESYUZsVAkSxpEaRmxEAZVJRpJSiAMgiks1UAZoAIACLABFZkaZQAEoAAAAAALHVFggoDaJIqeKKIeAyACUAEAAGgHoZAAAAAAAF0ACgAACxAEQAoAAN0jmw5NOObtxzulc+nC6s4qtI5OPXnnjye2/Rxc/WuG3VhZR4su7oLCNQgAKACgsJDTUSgEKiwAsFhQaAgVZEAWGtIRCixCoRCixDWhMKLELpNixBEKukBViF0m0wsQuFiF0iYWIWIXDWhnC4awuDSbZwYbwYXRtnBhvBj1Gk2xhcNYMGjbOEw3gwaNsYMN4TBo2xgw3hMJpWMGGsEwmhiYTDeEmE0rEwkw3MJhNDGEluYZmGdNbZmEmGphJhNDKTDSSzY0yKiaESYaRlWRZRlUlGmWbFElRlUASxUlGklhEASqyLKM0AGasSRZRKADNABKACNCSoyMiygACAAAAA1HRlprGJQPA8W0AGaqeOEWUZqgDAAAAA0A9DIAAAAAoAKAAALEARACgAAAsFjq5dKHFDsaMPTwzuzk5elcutqTmZc+tOKY83Wnq6819zOLMoDytrCkCwAFAFhpBQVBUhVgLBCtACwsiEAsNSIQosNIQosQoQKrUiJENRBEC6QWIWIWIXSJENRBENRDWkSIWIWIWIXSbSIWIaiFiF0m2cLhrCtaTbOFw1iTumkTBhruvKcN7PcZ4jj8z4buNSs/pTXu1+M4hvHDLK6k2lyk9XiR79wz0ZcU18W3282+1rPhWJvaPsj63tHDPRxwDbYtuZ195fx79+7X4Q9vH4Zz5+7XzcMuq48fft8b09O+peKadLXtPSKxmXb1+EcU0NCNfW4bu9PSnpa2jaI+x+guH8M4fw+kU2Wy0NCI/UpEO1ymMTETE+Evbj4L2+ll3+Tz3ru/aPzNhMQ/Q3EuzXAuJZnd8M217T+nWvdt8Y5vWOJei3hWtm2x3u42tvCL41K/dP1uHJ4PzY+zZXTHrcL69nyDupiXvHE/Rn2h2ubbWdtva+EUv3bfC3L63rHEODcV4fMxveH7nQiPG2nPd+PR8/l6Xl4vbxsenDlwy9K8bhMOTCTV59Om3HMJhuYTCaXbGEmG5hJhnSuOYSYckwzMJYrEwkw3MMzDNisTCNzDMwisyjSSzYrIqM2KiS1LLNVElZGbFZFlGbFJRUllYAM0rMioyCSolVkVGaCSpLKoAyACAAyoAijMtEoMgAAIAALDSQsdHTGJTyTwanxRqogDNVJRZRiqAMAAAADQD0MgAADQAAAAAsQBEAKAAACwAFg1V2tGOTr0jm7VPm0mfKHt4Z73PJxbi2bY8nBLd55uOXLky3Woiwiw5KoDQAQosKDTICwoAsNCgLEpCkDUgNJCtIQ0kLCoQo01IgsQRCw0gosQukIhqIIhYhZE2RDUQRDUQ1pnaRDUQsQ5trttxub9zbaGrrW8tOk2n6mpjv0S1wxCxD2Th3Yrj+7xM7Wu3rP6WtaI+qMy9j4d6ONOMW3/ELW866NcfXP7Hs4+h5+T0x/Fwy5+PH1r51FXb2PDd9vbRXZ7PX15n9SkzHxfYOG9k+A7HE02GnqXj9LV+fP1vOaVKadYrSla1jpERiHv4vB8r7eX4PPn1s/wDTHybh3o/47uZidxXR2lfHv3zb4Rl7Pw70b8N0oi2+3evubeMV+ZX9v1vdmo6PocXhfBh6zfzebPq+TL3vG8M7P8F4fidrw3QpeP05r3rfGeby8YiMREQ446tw+hhw44TWM082WdvrWolrLEdWnSYs7aWCFhfKbahqEiGohfKm1gtWt4mLVi0eUwsQ1g8pt4PifZPs9xLM7nheh35/TpXuW+MPV+J+irhmtm3D99r7aZ6VvEXrH2T9b6LEc1w83J0PBy+1jHXHqOTH0r4hxT0ZdpNrmdtXb72vh8nqd20+62Pteq8S4PxTh1pje8P3O3x4305iPj0fpqIW+nS9e7elbRPhMZfP5fA+HL2LZ/l6MevzntTb8qykw/R3FOxnZriWbbjhWhW89b6cdy31PVOK+iPh+rM24bxLX28+FdWsXj7pfN5fBOox746r1Ydfx317PjUwkw964t6MO02z71tvpaO9pHT5K+Jx7Jw9U4lwfinDZmN9w/c7fHjqacxE+/o+Zy9LzcXt42PXhzYZ+zXjphJhuYSYeax1ccwkw3MMzDKsTCNyzKVWUaRixplJalGaMo1KSiozLSSzYqAMVUCRK0JKjCMgJVSUaSWaIAzRJFlGaoAzQAQAEWACVUlGklBAAAWCQWGkjovm7YzsyJPiqTC2CAMVUlCeo5VQBkAAAAaAehkAaAAAAACIBYgBQAAAUAFBY6osNYwrl0ozaHPrz3dOI8+bj29c2NzbN5x0jk9uP0cHP1rhszKyk9XlyrYpAgANQFIVYlAGkIUFgNJCqBAsNRBYRqGkFhGmkFIWGtJSFgWGkVRYhYhENO7wfhXEOL7r824dtdTcauMzFY6R5y9u4b6N9/q4tvd5paMeNaRNpj7Hp4el5eb2MduPJzYYe1Xo0Q3pad9S8U06WvaekVjMy+t8N7A8C22J1qa26tH/AFl8R8Iw9i2XD9jsq9zabTR0K+VKRD6PF4Py5e3dPLn1uM9Jt8f4d2R4/vcTTh+ppUn9LW+Z9U8/qeycP9G+rOJ3/EK1866NM/XP7H0aehEPo8XhPDj7Xd5c+tzvp2eucO7F8A2eJnaTuLx+lrW731dHsG30NDQpFNDRppUjpFKxEOSIaiOT6HH0+HH7M08+XJll61mGoIhqIdpgxasLWCGo6tzFnY3DOG4hqRNkdW4hIjm1ELImysN4SIaw1pNmGoIhawujbUNR7CIarCyJtYa8EiGscjSbIhYhYhYg0bIhYj1LELEGl2RCxHNYgiOZYbIhNTT09SO7qUraPKYy3giEsNvXOL9iOzHE4m2vwnRpqT+npR3J+p6fxb0PbPUzbhnFNbRnwrrVi8fGMPqeOSxHteTl6Dp+X28J+X5O2HU8uHpk/PvF/Rd2p2XetobfS3tI550b88eycPUeI8M4jw68032x3O2mJx/C6c1+3q/WOPaxr6Gjr0nT1tKmrSYxMWrExMPl83gHDl3wys/y9eHiWc9qbfkSWZfpji/YDsrxLvW1uE6WlqW/T0P4Oc+fLq9N4z6GttbNuFcU1dKfCmvWLR8Yw+XzeBdTh7Osv9+17MPEOLL17PjEpL2Xtx2L452P19vTjGhFNPdVtbQ1K57upEYzjMRPjD1qXxuTjy48rjlNWPdjlMpvH0RJWRysbZZalJZqsyKjNVJRplmrBFSWVgAzSpKKjJABmqyLKM0EVJZqwAZABAAZoADQSDIyLKALBCrBqPD4rjoQr0SMs/eLPVPIsE8cIssy5ZKgDkoAyAAAANAPSyAKAAAEQBEKCgAAAAA0AADVWW69XTCd0rs7f5tLX8ocF55ue/zNCsfrc3Ws9PJdSRiIkLPQh5mwBQBYUUBqMiwitACx1UWAGohCkDUFhSBqMrCwLCwGkhYajKw1CQrSUhuEiFhqRK8pwDda221Lzoat9K/KYtS01mMeuHunDPSD2h2mKbvU2/FNLxrvtLv3n/vIxqf6T0ThsxGpPnP7Jd276nS8uWOE1Xi5sJll3j6twrt72Y3kRXiWx4hwvUnrfb2ruNKP6s920R77PZ+GafDuL4jgXG+HcStPTSpq/J6/+b1O7afdl8AicLFph9Lj67Oery5dPjfR9+3uy3Wz1Z0t3t9bQ1P1dSk1n4S6/d9r5bwPt52s4PpV0Npxvc220f5PuMa+j/Y1Imvwh7dwz0p7DXiNPj/ZnR73juOGas6Nvb8nbvU+Hde3j67C+scMunyno9liObUQ4+H8a7H8WnHDu0ejttWemhxLTnb29kX50n4w8ruOEb7Q0Y176E20J5xq6cxfTn2WrmHrw5ePP0rjcbPV46IXDc0mJ6Jjm7SMEQtYWIWsc1Qw3EJhuIVEiObeEiObcQ1IlIjm1hYhqK+prSJENVhqKt0ouk2kQ3ENRVuKqjjiG8cliGsAzELELELhBMLELhYBIWI5tRCxHNKqYMc24rM9Hb4dwvf8Q1O5strrbi3j3KTOPbPgxlnjjN26WTfo6WOSxHLxeb3vCNlweme0PHeH8LtHP5Dv/La8/wDd0zLwW/7bdkeG1mvC+FbviurHTV3upGlp59VKc5j1TMOWPN/M+qxuXy9Pxup/lryWevZz6Ghq6+rGlo6epqXnpWtZmfhDu7vhleHUjU4zvtnwqkxmI3WrFb2j1UjNp90PQ+MekftJvNO2jtt5The3npo8O0428R/Wr8+ffaXp2vudTV1LXvabXvObWmecz5zL0Y9NzZe1Zj8u9/TX4U7PpvEO1/ZfYRNdnpb3i+rH6Vv730vrzefhV67xH0g8b1e9Xh/5twnT6R+Z6Xd1Mf8AaTm/wtD0y1plM5dJ03Fj6zfz/b0/w1NvW/SruNbdX2evr6l9XVvN5vqalpta08uszzl6JL3L0j3zbZU8otP2PT5fgfG7vrc/u/KPv9F9TGEalmXyK9cSUaSWFZSVlEqokrIxVZAZqoEjNaElUlmogDNUZaSWaISDIgDKgCAAyACKAJVEwogFeci06t4TdStwL4JL06ZSUWUZok9fYzKyy4Z1qADmoAgAIAANAPUyAAAQBEKCgAAAAAoAKACwWOrk04zMQ44djbx87Plzd+KbrNXcz8/ux4Rh156t6k5tMsLy5bqQ8QHNoAWA0kKsSgDSLACwFhGmigLDUQWEWGoirCK0iqkNQsSqsJDUNoqwkNQsZqtRCQ1ENRmuxw+P75r7J+yXes6Oynu7mnlOYn4S713s4b9F5+T1ZhM8yEd5XNZWGZIbmSN56vJ8C4/xnger8rwfim72NvH5DVmsT7Y6T73ilh0xzsSzb6Jw30q8VzFeOcL4dxaPHVin5trf2tPFZ99Zex7Dtx2Q4h3YvrbvhOrP6O60/ldP+3Tn8aw+MxKxL1cfV8mHpXHLgwr9CbXR/O9D842Gtob7Qjrq7bVrq1j293p78M92azzfA9rudxtdxXcbXX1dvrV+jqaV5pePZMc4e0cM9IPaTa92u53GjxLTj9HeaXen+3Wa3+Npe/j8Ql9qPPl0191fVG4en8O9I3A9zMV4hw/ecPtPKb6Vo19P24+baI/tS9q4XvuGcViP7lcU2e8tP+Lpqd3U/wA3bFvqezj6niz9K4ZcWePrHYr1ckQW0tTTt3b0tW3lMYlY5PRHJutXJFebFZctZajNaisNVhImPNYlpG1hmJaiURTBlQTCrFczy6vI7XgnEdfRnXnRjQ28fS19e0aWnX22tiGMuTHCbyulkt9HjYarHrc254j2Q4ZH9/cdtv8AVjro8M0u/H+ctinwy8XvPSVt9n83s/2e2O2mOm43kzudX2xE4rWfdLMy5M/q8Lfn2n+e/wCErXl1617HwngPFOJTH5nstbUr437vdpH9aeTs7ra9m+D5/u72m2ddWv0ttsoncavsmY5Vn2vlfHe2naLjPerxHi+71tOeul3+7p/2K4r9TwFtxeZ6y3Oj5s/bz19mP739mpcZ6R9Y4h6QuzvD4mvAezVdzqR03HFNSdTP/dUmK/W9V456Re1XFKTpanF9bb6HSNDaY0NOI8sUxmPbl6ZbUmfFmbcnfDoun47vy7vxve/59PuPNlXPrbm97TNp6zmXBa8yzlHquSSEzOJY5t4O6xtWMLEN91Yq5ZVqPSPSJn882seHyc/a9Vl7b6Rsfne2jxitv916lL+d+Md+tz+78o+/0n1OLMwy3LMvl16mUWRmtMyy3LMs1UlFSWaqSjTLFURUllYAM0rIT1GVAGaMiyjNEkVGaoAyACAAlABGgBNA3SOTDkp0duKd2a0iyT4/B6NMssz9rU+LMueSsyys9EeTK92wBAAAAZAAGgHqZAAIUFAAAAABYACgAACtQq1c9Pm6cz5uGvVy3nFIh6ePtNsVxWRZRyyvdQBFAWFBQaZCBY6KADQsdVSFaSiwitQGkhWkpHVpIWOrSKsI01GVhqEjqsNJVhpIahYzViGoSGobiObbRHfzPhMY/tQ7tnR0Yzq0j+VH2u9bq9PF6OHJ6sQiwjtK5ix1RYXYqwy1DUqEAT1blRVhFhuVlcrOJiGWnSZI89wfth2k4XFdPbcX3F9GvTR15jWpjyiL5x7sPbOF+lCs2ivGODVnz1dlqTTH9S+c/wBqr5rHVZenj588PZrllx45esfduF9quy/E8RteMaWhqT00t5HyFvZmfmT7rS85bS1aVraaT3LRmto5xMeqfF+bo6S8hwfjPFuEX73DOJbraeddLUmKz7a9J98PdxdflPam3nz6We6vv+Z8mqWy+W8N9J3F9Lu14jsdlv6eNoidHUn31+b/AKL3nsj2u7Ncdtq01dbdcL1dPTnUtXX0vlKYjGe7anOevjWHuw6rDPs82XBlj3ecicuSlbWmK1iZmZ6R4vH7/tf2T2MzXZbff8X1I/SvMbbRn6pvPwr7Xgd/6QeO6lZpw6dtwjSnljZaXdvMevUtM3+Ew74/zM/Zx/Ht/wDf+GPJ8XvtuGa+hoRuOIX0OHaE9NTeasaMT7O9zn3RLxu77Sdj+HRP99b3i+rH6O10/ktLPlN78/fFZfLN1u9xute243Ovq6+tb6WpqXm1p9szzcXenPVudNb7eX4dv/v8lkk9Hv299JXEKxNOCcN4fwmvhqV0/l9f+3qZj4Vh6nxbjXE+LavyvEd/ut3eOk62rN8ezPT3PGZ59Vy7cfDx8d3jO/x9/wCPqttrfylp8ZJtPmwrttFyZ5kQuEtEG4q1FGbRx4WKueulM9IeS4FwHi3G9z+bcH4Zu9/q9Jrt9Kb93+dMRivtnEMZ8mOE82V1GsZcrqR4iKkVexdr+ynGeye822045tqbbcbnbxuK6Uatb2rWbWri01mYzms9Jl4PuufHzYcuPnwu5ffFyxuN1fVxd1cN4MFpHz/0iz/zzp18tGJ/Hwery9p9I2J47T/sKx9cvV5fzzxTv1fJ836DpfqsWElqUl82vTGEVJZqxGZbZlmqySDKxElUlirEJBlUAZq1JRZ6IyQAZqkstIyIkqSzViAM0AEoAMgAigApHVzVjlhxUjMueOmfe9XFOzFT1+9Gpjw9zM/e61IzLFm5+1xz1efkvZqJKLPVHlrQAAAAAgAGhoB6WRYRSAAoAAAAANAAAAsBYRqGojdOq6k88JVLTzl6L2xZZAcWgAgLCNNRKANRBUjqqgA1BY6KCxCOqkDcFhUhWmVhYFjoqVYWEhqOjcRYahIaWJVhYSGobjNahuGYbhqM1vRnu6lZ9cO7fq6dI6+qJn6nc1OrvxuObEIqS6sI9g9HfCtjxztjsuFcSjV/NtxGrFvkr922a6V7RicT41jwl6+9o9E9u76R+Cz569q/2tO9fvcue2ceVnwawn0o9u496HtzS1tTgPF9HcV6xobys6d/ZF65rafbFIeh8d7M9oOBRNuLcI3W104nHys172l/nK5pPxfpnxcmla1JzW0xmMTier5fH1/Lh693ovDjX5MjniSer636fODcL2fD+F8S2PDtrtNxq7jV09e+hpxT5T5tZrmIxEzGLc8Z5vkb6/T885cPNHm5MPLdNEO1wnhnEOLbv804XstfebiKW1PktGvevNY64rHOfZGZcO40Nfbbi+23Ohq6Gvpzi+lq0ml6+2s8497vM5vW+7HlutuNplXaZM2LHVWY6q6Y1mtQsdWYaq7Y1lyQ8/2OnG73X9Gt9sPAQ892Q/jW5/o9vth9LofrsXn5vYry8TOSZliOrdLYnOH6CPFVM808ViFRfFYjksQ3WvqRWIhuKtxpz5Ozs9nuN1uabXa7fV3G41PoaOjSb6l/ZWMzPuhLlJ3pJvtHUirUVdncbXW2uvqbfcaOpo62leaamnqUmtqWicTExPOJiYnlKVpzTzSzcTTGnp5mIiMzPSH1zsn6Bu1vEpjU4xfa8D0J6xq2jW1vdSk9343ifU9K9G3DP7q9v+z/AA/u9+NXiOja0YzmtLRe+fV3a2ftqYxaX5P+I/GufocseLg1LZu31+Wvd8X1Og6TDmlyzfMOzXoR7E8IiurvdDccZ146zvL/AMHn1adcRMeq3efRNntdrstpXa7LbaO20KRimlo6cUpX2RHKHZv0ljwfguo6zn6m75s7l832sOPDjmsZp+afyrYz264Z6uFU/wDO1nx2YfZPyq//AH64dH/9Vp/+drPjto5v6d4F/wDj+L5fq/O9b9fl/vuYwmGpgiH0688fN+3897tBb1acR9cvXZew9u5i3Hr4/VxP9qz1+X898R79VyfOv0HT/VY/JiWWpZeCu8ZlJasyzWoiSoxVYnqiyjNVJFlGasZFlGKqSLPREqjLTM9WSADFUSVJZoyAlIgSMqAMgAgAM0AFkG9KObniHHow5cZ9r3cc+izWZ6M2/c3LFv3rkkcdp6sNX8mZePlvduMgOFaAAAAAAAAaAehkhSBYAAAAACwAFAAABQahI6tQ6YRGo5My1PRiXTOpABzUAUWFSOiqgA0hHVUhWgAjqo0A1EWOgQNRGo6LCLDURVSOqtRK0sI1HVqIsdWo6pCw1Ga1DUMx0ahuM1uG6sQ3DcZrcZxMR4xMO7qfSdOnKYmejuanV1wcs3HDLTLowPYPRtfuekHs/PnxHRr8bxH3vX5eZ7C6kaXbbgOpPSvE9tP+tq583fjy+TWHtR+m/FqrMROMN1fnXufPPygtObdjdhrfqcSpX+1pas/7r4dL716fKzPo80Zj9Hi2hM/5nXj73wWX2/D7/wAX3vJz+0949BWp3PSdw3T/AOt0tzT4bfUt/uvv/EuHcO4toRt+K7Da7/SjlWu40ov3f5szzr7Yw/PHoXvGn6UOCWnxncV/tbfVr979I1jm8XiHbm39jtw+w+fcd9D/AGX33e1OGa+84Tqz0rWfl9L+zee9/pvlXpA7FcR7G7ja03m62u70d38p8jqaHej6HdzFotEYn59ekzHrfpl8o/KVp/zZ2f1PGNbc1+NdKfub6LquX+bMLdys8vHj5bdPisL4pHVfF+ixrw1qOi1SFh3xYrkq892P/jm5/o1vth4KHneyP8c3P9Gt9sPp9F9bi8/N7FeUhqGY6tRh+gjxNQ3WGauWsLRzbTb6u416aGhpamtq3nFNPTrNrWnyiI5zPqh9G7Kehntxxvu6mpwyOE7ef8bxG06Vv83idTPtrHta/Jrnu+lnhvr0deP9TafufraJ6PyHj/j3P0PN/I4ZO83u/f8As+n0XRYc2HnzfHuy35P/AGb2Xc1ePcR3fFtWI56Wn/e+jn+rM3n+1HsfU+z/AADgnANr+bcE4Ts+H6Ux86NvoxSbeu0xztPrnLyENVfh+q8Q6rq7/wA2dv5fh6PscfDx8fsTT8iflB8KjhnpZ4v3azXT3kae804x4XpEWn36lNSXoVa833T8rbhfd4twLjda/wCG0NTaatsdO5aL0j/WanwfDqxzf03wTn/ndBxZfZr8O36Pz3WYeTnyj6X+TVw+N76VdprTWMbHa6+6iZ88Rpf+t9T9WT9KX5//ACSdjNuIdoeJ3rONPR2+hpT4T3ralr/+DT+L9AeMvw38Uc38zxDLH/xkn6/q+z4fj5eCfaxfpLHg5NTpLH6L889r80flTWie3+zr+rwvS/8AN1nyG3V9X/Khvn0k6Vc/R4Zof+ZrPlFn9Y8Fmug4vk/NdZ9fkxISQ+jXnfMO2czPaPd1n9G2I+373hJeb7Z/+829/nR/4YeFl/POt79Tyf3X836Dg+rx+UYlmerUsy8ddklhtmerNaZkWUYrTNmW5YZoIqT1ZrSSjTLFURUnqzVgk9VSWSIAzVAGaIiyjNISiozVAEoAM0AEAjqLVrGdx2NKPmuSYTTjFYamMfjyfRxmo52sWjw9zit9rls4dSernndRY47TmWZ6Kkvn5XddIgDKgCAAAAAADQD0MrHQI6CgAAAoAKAAACwAFKsNJVp1wZpM8mVlDK9yADKgEdVGgGmQBoIUgUFjqiw0KA1EVUWOrUSqsI00hHVqOrMNR1aiVY6tQzDUNRGoahmOjUNRlpqGWoajLdW6sQ3VuMVyVr3vm+fJ2s5pWfOsT9TraU929beUxLsV/wADp/zI+x1wc82WZahltgl3uz2rGj2g4brT0095o3+F6z9zotaV509WmpHWtomPczn3xq4+sfrbWr3Na9PK0wVcm/8A47rxHT5S32sVfm3vem+m+kX9G26nH+D3Whqf6Xd/33578X6O9MGnF/RlxmZ/QjQtH/8A0aUfe/OL7Ph1/wCO/N5ef1j2f0V37npH7Pz+tvaU/tfN+9+nKxzfljsBedPt72cvE4xxbafD5ej9U1jm83iM/wCSfJ04PZWIfL/yk9PPZjg+t+pvr1/taef919SiHzb8o+uew3D7/q8W04+Ohr/sefpLrmx+bfJ7NfA46qleq+L9Xi+bWo6NVZjo1V3wZrkq892R/je5/o1vth4Crz3ZH+N7j+j2+2H1Oh+txebm9ivKQ1DMdWoffjxN1c1HDVzUVH0r8nGcelzg8eddx/s+pL9cx4PyJ+Tnn/8AGDgcecbn/ZdZ+vI8H82/i7+ux/tn519/wz6n7/2ajq1CQ1D8tX0ny/8AKb4b+fejC+7iM24fvdHcZ9VpnSn3fwufc/LUdX7b7e8LnjfYjjfCa877rY6unp/z+7Pd/wBLD8Sac9+K2xiLREx739B/hLn83S58f/jfz/8A5XxPFMNZzL4v0/8Aks7D829He53s1jvb3iOpeLY5zWtaaeP7Vb/F9X/Sl6j6F9jPDvRX2d281ms32ddxMTOeerM6s/8Aje1a+rpaGlqa2tqU09LTrN73vOK1rEZmZmekQ/F+J8v87rOXP45X8+z63Bj5OLGfYup0lj9Fbzmsyz+i8Lq/Lf5Tk/8ASlaPLhu3/wDHqvl0y+n/AJTk/wDSlec//LtvH+lqftfLpf1nwf8AoeL5R+a6v6/ItKRKWlInm91cHy/tVbv9oN5afG/3Q8TLynaX/wBt7ifOaz8aw8ZL+e9Vd8+d+2/m/QcXsT5MSxLcsz0eWurLNmkszWmZRUYrUSWZ6tSzLNESVJYqozLST1ZrSJKk9GaIkqksVUASqAM0SUaZZBJUlmqgDNABAAZBvTjMxDDn0IzePU78WO6ldmkRj1JaHJEcse7P49jFvt+99DXZzcV58fe6+pPPDn1J8fe61uryc91G8USVSXhrogCAAgAAAAAA0A9DKx0COgoAAALAAUAAAFAFjqsRYaZhp1xSsz1AZqgBAWEWGkUBYgA1BYCBQWEWGoVSOoR1aiKsdUWOrSVWmYaaiENQzDUNRKsNQzDUNRGo6NVZhqrUYahqGY6tQ3EbhyQ44clW4xW6u1OIpWI8Ih1auxWf4KmfL73TFzzSGZWGW2BLzilp8oWUmMxMefJL6LPV+ub3+UtOp+vPe+PNqjqcM1I1uEcP145xq7PR1P7WnWfvdqj83XveA9KdJ1PRnx+sc5/N9O3w19O33PzS/T/b+ve7A8frjP8AzfrW/s1m33Py/PV9bw2/Ryebn9Y8h2c1p2/aPhWvH+K3ujf4alZfrm8Y1bR5WmH450tX5DUprx/i57/w5v2Rr/xnV/n2+1y8Sn0sa1welSHz/wDKCpFvR1Ez+hxHRtH9jVj/AHn0CHpHp20vlPRjxC//AFWvt7/62tf954+nuuXH5x1z9mvzhVfFI6rnm/V4Pm1qOi1Z8GqvRixXJWebz3ZGf773H9Ht9sPAVee7I/xvcf0e33Pp9Df+XF5+b2K8rE82oYhqsv0MeFyVctHDVy06rUfSfydP/jBwL1xuf9l1n69h+QfydP8A4w8C/wD9P+yaz9fw/m38Xf12P9s/PJ9/wz6n7/2ajwahI8FpMTnExOOU48H5Z9JYfibttwfU4d264xwHSrat6cQ1NHQrjnFb3zpRH9W1H7afnv0idnY1fynOA0rSJ0uJX2u9vMxjNtHvd6P7O2r/AGn6P+Gur/6fl5N+nlt/Dv8Alt4eu4v5mOPzn+X3zh+209lsdvstGIjT2+lXSpEdIisREfVD1T0y8S/uX6N+M7iLd22pp020ev5bUrpfZefc9yfHvypuIfm/ZTg3Dqz8/ecWpa0THKdPTpeZ+F505fI8P4v5/V8eF77vf869XLl5MLX13Vj6XtY/Rcmt1t7XH4PE6Pyt+U1aJ9KWrGY+bsdCJ/0p+98vmX0j8pG/e9LHEI5fM0NvX/V1n73zWZf1nwnt0PF/bPyfmuq+uy+ZaWYnmzaWe9ze2uEfL+N3+U4nr2/lY+EY+50ZdrinLiO5jy1rfbLq2fzznu+TL51+h4/ZjEsy1LMvPXRlJVJ6s1qMpPVUnqxViT0ZlqeiT0Zqsk9AZqokqksVpAGRElUllUAZqgDNBFSerIgDKoAgAMgAmha9Xa2leeXWq7+0r8zP4/HV7Onx3Wcq5O7yx7vu/a47+r3Oe0YjHj+P3uvq+p7MnOOvrT5OvLk1p5y43zefLddYAPNW2RZRAAAAQAAAAaAehlYCBQAAAWAAoAAAKCwjUNRBZ6IOiADKgBAWOiLDUSqAsQAagsBA1AWEWGoVSBYWILHVFjq3EqtMtKhDUMw1HVqJVhqGYahpK1HRqrMdGqtRhqOrUMw1DcRuHJDjhuG4xXJV2InNImPOftl16uakY0a+2ftl0xYz9CGZWGZajmLHVCOq0fqbspbv9keAzPX+5Ozz/mKPKUeC7B6k6vYjgWpP/wC36Ff7NIr/ALrztH5vKd697p9qaRqdkeN0mMxPDN1H+pu/Kvi/WPF9OdfgXEtCOursdfTj+tpWj735NrzrE+b6Xhvpl9zhz+5NeM6N486zH1P2X3o1J+Ujn3/nfHm/Gto71cecYfr3gepOtwThurPOdTZaF59+nWfvPEp7N+Zwe93nqPpprN/RVx2IjnFdtPw3Wi9tetelevf9GnH6Y/yatv7OrS33Pn8V1yY37Y730fl6vVfFKr4v1uD5lajpK1SOi1ejFiuSHnuyM/33uP6Nb7ngIee7I/xvc/0a/wBz6XRfW4vPzexXlIlusuOGqy/Qx4XLVy06uGsuWnVR9I/J0/8AjBwKf6T/ALLrP2BXq/Hn5PNu76XeBT/K3Ef/AG2s/YdfB/OP4u/rcf7Z+dfe8M+p+9uPB6n2N4vG47d9uODXtHf2O/2mrSOXLT1djoY/06anxe2Q+M9luKfmf5VXa/h1rTFOIbXQriZ+lfT2m2vX/RnVfD6Pg/nYc3xmO/wyx/Tb28mfluP23X+K+0vWOM9nI33pD7PdpMREcL2u807dPnW1fkq0z7IjV+L2aGZ6vHx8mXHd4/Cz8ZqulkvquX52/Kr3/wAr2w7NcMrP8X0b614z1+V1K1ry9XyM/F+h5l+UvTvvP7o+nC+j3sxtdTZ7OIx4fNvPt56tn3P4b4/P1vm/8Zb+n6vL12WuLXxsfq7W629ri8G9WfpOPPJ8B635F/KLtn0wcajyrto/+20p+987mX0H8oqf+l/jfs23+zaL51aX9b8M/ouH+3H8o/NdT9dl81tLEz82Z9TNpY1LY07z5Vl6q4x804laL8Q3N46W1rTHxl1bObdctxqR/Ln7XDL+d8l3lX6HH0jEsy1LLlW2UnqqT1YrUZSVSWasSeiSspLFVkBmqiT0UlitMgJRJ6pKz1SWBAGa0AM0ElUlmiAJVSeosoyADNACOqwclI5w8ntq404z+PxzeP0a5tEPL0rivq/H730emx7bcs64tSJ6eP4/e6mvbETMfjydzV5cvx+Orx+5t4OnLdRMXWvPNCeo+Tnd12gA51oZaSUEAAASgAAADQD0MkdVRVgAAALAAUACAApRpFbiADQAIACwFRpYlAGogAsCFSFagLCLDUFWEWFiCoNxK00ysKix1ajqzHVWolajq1DLUdW0rUNVZhqFjLTUMtVbjNbq3Vx1bq3Ga5Kuak50/ZMw4auakY0v60/ZDeLnn6JDMqy25iwgo/S/ow1PlvRzwHU//j3r/Z1tSv8AuvZqQ9N9DevXW9GnCKVnM6E7jSt7Z3Gpf7Lw9xo/O8s1nfm989HPpU+UtGljPf8Am4888n4/0sxpUz17sP2HsP43of8AaV+1+QdzSdPc6mnMYml5rMeycPd4b65OPP6Rnxh+sOw+pOt2L4BrT1vwvaz/AKmj8nS/U/oy1flvR32f1PLY0p/Ymaf7rp4lPo41ng972N4T0h6fyvYDtDTy4buL/wBnTm33POPFdtKzfsR2jrEZmeD72I9v5vqPl4XWUr0PyZTwaZ6ThfF+vwfMrXgsJHRavRixXJDz3ZD+Obn+jX+54GHneyE/37uf6Nf7n0ui+txcOb2K8nE82qy446txL9BHhrkrLlrLgrLlpKo+ifk+3x6XuAf9prR/9vqv2RV+L/QJfu+l7s969fUj/Uaj9n1fzr+L5/3mH9s/OvveGfVX5uSOsPzL2r4n/cf8rDV3827unHE9lp3nP6Ops9DStPui8z7n6Z8n5D/KIm2n6YuO207TTUmdvato8J/NdGIn6nm/hnjnL1PJx30yws/Gx067Ly4Y5fCx+voYmebo9m+JU4x2f4bxfT+hvtppbmvhiL0i33u7M8353LG42y+57oT5Pxlxre/3Y9MWvu+9MxuO0ERWc5+bG4itfd3Yh+weM76nDeD73iWpaK02m31Ne0z0iKVm0/Y/EnYibanbLs/F+dr8U2kW9s61Mv1n8L8f0efk+E1+d/R87r73wx+1+5tSeUuLPJbzmMsTPJ+SfRfkD8oTU73pc45PlbQj4bfSh89tZ7x6eb970tdofVr6cf6jTehWs/rfh010fFP/AG4/lH5nqO/Ll81tZxatv4HUn+RP2F7OLWt/Aav8yfsem1zj57vpzvNaf/qW+11pcmtbval7eczLjl/Osu9foYzLLVmZYrTKSqMVplJ6qk9WasSUlZSWKrIEs1pCQlmqyAzRJ6pKyks1UAZqgDNBJVJZpEAZqk9EVGaACUFqjdWsJ3HZ2NJtq1w8tjFfU6XC6Zvl5HUiYj1vr8GOsHDK93S3HKJ/H48XjNa2bTLv7y0RE4/H4+94y8vL1OWuzeEZAfNrrABmqAIMiygAAACAADQDuyLCLCwAFABYACgAsABSqrLUNRABQAAAWA0zDSxKANRABYEKkdVaKLCLDUFICFiKA3ErULHRI6LDURVRVStLDMdGo6NRK1HVqGYajq1Ga2tWYWOrcZrkhuHHDcNRmuSrmpOdOf533Q4Ic2n9CXTFzy9EhJ6qzMujmLDKwo+0fk8cSrqcK4rwa1o7+jr13enE9ZresUv7ommn/afVqPzJ6OePx2c7X7PiOraY2tpnR3WP+qvytPunFvbWH6brynGYnymJzE+uJ8XxOt4/JyW/F6+LLeLm0pmLRMTjE5fmj0q8Jvwbt9xXbzTu6WvrTutCfCdPVmbRj1RMzX21l+lqPXfSH2N2XbHhVNK+rG13+3zO13MxmK560vEc5pPL1xPOPGJx0nNOHk3fSryY+bHT8yS/TvohnPoz4DM8v4HV/wDP1Xxqnoo7bW4pXZTw/b1pNue6ndac6MV/W5W73rx3e96n6C4Dw3Q4NwXZcJ21pto7PQro1tMYm2I52n1zOZ971dfzYZ4yY3bHDjZvbyEOrxukavAuJ6M9NTY6+nP9bTtH3uzDi4jMV4Zvb26U22pafZFJmXzHd+PaznE+asaXKlYnrhp+xwfMrcdFr4Mx0aq74udctXnuyH8c3P8ARb/c8BV57sf/ABzc/wBFv9z6nRfW4vPzexXkI6rEsRPNqJfejxuSsuWsuGsuSs81Ze+egiYj0u9nP6Tf/wAnUftOvR+J/QbbHpe7Nevd2j/Vaj9r1l/O/wCL/wCrw/t/WvveF/VX5t+T8i/lJR3fS9xSf1tLb2/1NI+5+uM84fkj8prl6XN/69voT/q4cP4Uv/fX+2/nG/Efqfvfdfyc+J/3R9EvCq2nOrs51drePLu6lu5H+bnTfQLTzfB/yQeK97hnaDglrf4HcaW9rH/aUnTt8PkafH1vutp5vmeM8P8AJ67lx+3f49/1ejps/PxY37Hp/pt307D0Udo9eLTXv7OdvmI/661dL/1H5N7DW/8Az12d9fGNn/tGm/RP5U+//NfRjTbZn+/eJaOhMRPhFb6vP1Z0o+MPzh2Etnt32b5//Odj/tOm/Ufw5x+Xw7kz+Nv5Pn9dlvnwny/N+57z81x55M7zX0dtttXcbjW09HR0q97U1NS8VrSvnMzyiPXL49289P3Zng0X2vZzTnj28jMfKVmabWs/z8Zv/UiYn9aH43puj5+qy8vDjbf9976mfJhxzeV0+J+nG8z6Wu0uZ/yuv1aWnD0W1nkO1HHd52i4/vuN7+NKN1vdWdXUjSrNaROIiIiJmZxiI8ZeItf1v6x0vHeLgwwy9ZJPwj83y5TLkyynvrd7MzaO5fPk47WcW41O7ttW3lXLXJdY2syd3oUsz1WWX87r9BGbJPRZZlitpKLLM9GaqIs9EZqxmepIksVUJ6BLNaQkJYqsgSlESVZnqzVgAzVAGaCSqT1ZpEAZqiKk9WaACBDkpHNiHNoxm0O3FjupXmOFaeNKbOxuOUN7HT7u2ryxPm4d7aIrPl+P3vsyeXB5/WvE76+bYdK3Vza9u9eZnxcE9XyOoy3XfGdgB462ACgDIMtJIIAAAgAA0A7xkIBRQFABYACgAQAGkosIsLBUjqSR1UUBQAWA0yqxKoDUQAWAqLDRRYRY6rBSOoNRFAaiVYWOqQrSNLHRCGhqGoYhqGoy1DUMx1ahqM1uFZhpqJW4aqxVqGozXJVzaWe7b3fe4Ic2jPzLe773XD1c8/QhmWmHVyJWOqELpGp6vu3oR7W14twevZ/e6v8AzhsNPGhNp562hHT+tSOWP1e75Wl8Iy5+H7zdcP3ujvdlr32+50LxfS1aTi1LR4uHUcE5sNe9048/JX65paXLS0+b0j0b9u9j2s29Nrrzp7XjVK/wm3jlXWxHO+l5+c16xz6xze6Vno+DnhlhdZer2S7m47Fbetqs83DWXJSWFcsPCekLe14f2A7Qbq1u7nh+to1nOMW1a/JV/wBK9Xmol8q/KM7QU2/B9n2a0NSPl91eNzuYifo6Vc9yJ/nW5/8Adx5u3Bx3k5Jizll5Zt8OjqvizVrxfrMY+bWo6LVIWrvixXLDz3Y/+O7n+i6n3PAQ8/2N/j26/omp9z6XR/Wxw5vZrueKxLOecrEvvR4nLWW6y4ay1E82h7z6D7f9LvZn+m/+nd+2Yl+IvQfP/S72Y5/5b/6d37aiz+d/xf8A1WH9v619zwv6q/NyZ5vyT+U9bHpb3nP/ACTb/wDgfrPvPyN+VDfHpd3cT/8Ao9v/AOGXD+Ff66/23846eI/U/e7P5L3FfzH0pae0teIpxHZa23iPO8d3Vr9WnaPe/VmpeKxNrTEREZmZ6RHm/BfZXju47O9peHcd2la319juK61aWtMRfHWszHhMTMT6peW7d+kntb2zm+lxjic12Vp5bHbR8nt/VmsTm/tvNpjww+14x4Dy9d1k5MLJjqbv2/L5PJ0vW4cPF5b6vpP5UXbPgPHbcI4RwTie34jO11NbV3V9vbv6dLYpWkRePm2nE6mcTOPHGXxjhXEtbhfFtlxPbxS2tstzpbnTi8TNZtp3reImImOWaxnm8fbU9bFr8n3ei6HDpOnnT495+7xc3Ply8nn9HsfbXtv2n7Ybn5XtBxfX3VK272nt4+Zoac/ydOPm59c5n1y9btZx2uxaz08fFhxY+TjmpPg55ZZZ3eV3XJNuUuObMzbkzlpGrWcO8nOx3H8yW5lxbu2Nlrz4dyXDmuuO37HTD2o9JlJWWZfz2vvxmeqSqSw1GZSVZlmqSys9UlhqIkqk9WaqJPVUZqiT0VJYqoSJKUGZaZZqwAZqgDNBFZZqwAZoJPVUlKAEINQ7Wzp3tSIdaryvBtLv7inLxezpsN5MZ3Uebinc0ojyj4vE8Uvisxnr+P2PNbn5tJetcT1O9qzHlyfS6i+XFxwm66F55sNWZfC5LuvTABxAAaAEoEggyLKAAIAANAOzIA0LAkKoAAANAAQAFSioNCkdUWAUBoAFgLHRFhYlUBqIALAWEIagoCxI0A0VQjoNRKsdVZaaRYWOqQrQqwiwsRqGoYhqGoy3DUMQ1EtRlqOrbDUS2lbh2NH6E+brQ7O1jMW9jpx+rln7JhlyTViYejThtmSFmFiF0bSepCzCxHJrSbNK99PUpqad7aepS0Wras4msxPKYmOkvqXY30wb/ZxTadptvfiWjHKN3pTEbiv86JxXU9vzZ85l8tHLl6fDlmso3jyXH0fqLgvbjsjxbTrba8f2Wnef8VutSNvePVi+In3TLzVuK8J06fKanF+G0p171t3pxX4zOH5EwRHPLw3wqb7ZO06n7H6N7YelTs1wTbXpwvcaXG+ITH8HTQtnQrPnfUjlMeqkzM9M16vgHGuJ77jPFNxxTiWvOvu9zfv6l5jGZ6RERHKIiIiIiOUREQ6UQ14Pd03R4cHp6uPJy3Na9V8Ujqvi92Mcq1HRqrMdGqu2MYrkh7B2Mj+/d1/Q9T7nr8PYOxn8d3f9D1PufR6P6yOHN7NdmesmUmecs5fcjyOSJarPNxxKxPNUe7+hCf8Ape7Mf07/ANO79tROcPwR2I49/wAme13De0H5r+dzsdb5WNH5Tud/5sxjvYnHXyl7D289LXbLtf8AKaG64h/c/h1uX5lsc6enMeV7Z71/XFp7vlWH5Pxzwbn8R6vC4amMne3533PqdH1WHBxWZeu36S7f+mTsb2StqbX87ni/EqTNZ2mxtF+5byvf6NPXHO3qfln0kdr9z227WbjtButpo7O2rSmnTR0rTaKUrGIzaes+c4j2PVsxERERERHKI8ibPoeGeCdP4ffPju5fG/s4dR1mfNNekck2Y7zE2Ymz7FeRyWtyZmzMzyZylVqZZmeaSYQMo1FfU3XTmfBNG3HEOHiUTHDNzP8A9OXfpoTPSHFxrRnS4Ju9S0cvk5j4xh5+pmuHK/ZW+O/TnzfP2ZWUl/Pa/QxGZWWZZrUJZWUliqjMqjKjKyjNWEosozVEnqrLNUSeqozQZVGasAGaoAzQnoysozVgAzQJCUoiwjUEg3pxzexdnNHN5t5Rl4DQrm0PcOA6Pc2d7zHXEPrdDhu7cOW9nHxO/c07T5Q9U3Nu9eXn+PauI7vm9c1JzJ1uffRxRx26oT1HxsvV3AGKAAsABQBkSUaZkAAAAGgHVkAUFRYWAAoANAAAApQBpBUAaAaABYBHUFg0AsZAGoADUFCBUWOipCtKsCR1VYg1HRlYajKqiw1BqBIVqJWlhmFhqM1uGoYhqGkrcNRLES01EbdvYatKXmLxM1t1x4OnEtVnDeOVxu4xlNzTzNdnOtE220xqx5V6x7urqamlaszE1mHFoa1q2iYmYmOkw81s+MZjucQ2ulvtOeU9/MXj2Xjn8cx6nsw5cMva7PLlhlj6d3h7VmPBO69m0+G8F4l/7P4j+aa09NvvuUT6o1axiffFfa6PF+A8S4Xasb3Z6ujW/PTvPOl4862jNbe6Zd/5fbcc/N7q8PMGOTmtpzE9Ge5y6J5V248GObfd9R3ZXym2cEQ13SIXRtlrwMNYakTaQ14kRzJbkTax0aqkdFq64xmuSHsHYz+Pbv8AoWr9zwEQ8/2N/ju8/oWr9z6PST/kjhy+zXNPWUmSessy+zHlaiViebBkG880m3JmZTJsWZ5pMsjKmUWIaispRiVxLlrpzPg5tPb2t4Gk26sUmfByU0ZnweX2fCtbWmIpp2mfY+gdnfRXxfcbGOJ8UnQ4Pw2IzO639/kqTH8mJ+db3RLPJyYcU3ndJLb2j5lo7O9ulZew8C7IcW4pW2pttnedHTjOprWxXTpH8q04iPi9p4p2j9HPZCLafB9jftNxGnL853kfJ7as+ddKJzb+tPufNO23pC7QdpLdzfb6abav+D22jEaejSPKKV5Q+dz+KYcc+jPx/b99X7HXj6fPkeb4tr9mez/epuN7PFN1Xro7OcUifKdSY+yJfPe0/aPdcVrbQimlttrE5jR0o6+2Z5y8Zut1Ns83Q1LzacvznW+Kc3P9Hep8H1On6TDj7+tYllZZl8ivfElCUlmqiSsozViShJLNVJQJZrSSAxSJKLKM1SUJGaJPRFlEqwAZUAZok9UBmqAM0CQnogkNVSG6Rzbwm6V29jTvasQ9222n8jwynnMTZ6rwXS7+tV7Zxu35ttPk+k1rFffh97pMfLhcnl5Lu6eocZ1e/r25+LxV55u1vL97UmXTs+T1We8nfCdkAeCtgCUAEUAFAEoJKkoMgAAA0A6RkAagEAooCgAsABQAUAFiACjUdBIVQAWAA1BY6KkKqADSAChCorSUhplqFUVFhpBUGolaEhViNKzCw1BWmVhqMtQ1DENQ1EbhqGIWFjLcNRLELEtJXJWcOal3BDVZalZsdzT1Zh5/gHafi3CazpbXdZ295/hNvq1jU0b/AM6loms++HrFbOWl3bDkuN7OWWEvq+gaG67Fccr3eI7PccA3c/4/Yx8toTPnbRvMTH9W8RHhVjiXo+4tXaX3/B77fj3D6x3rbjh151JpH8vTmI1Ke2a49cvSKajyvB+M8Q4Xuabnh+819trUnNb6V5raPZMPZh1MvtPPlxWejqam1vWedZ6uK2lMT0fSNl254TxqPke23AtHiV5/y/bTG33ceub1jF/69be13o9H3B+0NJ1uxHaXa77VnnHDuITXa7r2VmZ+S1Pdas/yXrx8mU3L/v8Avx0422dq+TzRO49n7Q9l+McD3ttnxXhu72O4r/i9fSmk484z1j1xyeF1Nvas84lu8N9Vmbo93mvd5OxbSmPBmaSz5F8zhiCY5uXupMLMU2xEcmohYhqsOuOKWtVh57sfGN3vP6Fq/c8HWHn+x8f33vP6Fq/c+h0s+nHDlv0aW6yzLVussy+q8wniuJWInKKzJhuKy1XTkNuKI9rkrSZ83PTQtMxyl3ttsNTUtERWZ9xpm5PHaejM+Eu1obO15jFZl7l2T7Ccb4/uq6HDeHa+5v4xSnKPbPSPbL6btuwXY7sbpxuO3XH9H84pHenh2wmNXV9lrfRrP4y83P1fDw3y5XeXwne/hPz9DGZZTc9Pj7nx3gvZrfcR16aG12urral5xWlKTaZ9kQ+ncM9EenwnbV4j224vtOAbXHejS1J+U3F4/k6cc/j08nU7T+nDa8H2+pw7sBwfa8F0ZjE7isd/cX9t5+74vivaXtdxfjW4vuOIb/W173+lN7zMz7Znq+Zz+Ict/wDZPuuX/wAZ/wDs74cG/t/xP3v+H2rjXpP7FdkdKdr2G4Bp6+6ry/ujxCK6upnzrX6NfbzfHe2nb7tD2m3Vtfi3FNxuZmZxFrzMR6ojwj1Q9Q3G7mZ5y6WtrzPi+Ny9Xq24+vx9b+N/L0+x7+Ppvi7W43cznm8dra02zzY1NTLgtOXzc+S5PbjhIt7ZYklJcLXWRJZlZZlloZWUlmqkpKss1RJVllYJKozVASWasQElmgAyJKE9RGgBgElUlKIAzVAGaACCuTSjMuOHZ2tO9eIejhx3Wcq9m7Jbb5Td6WYzXOZ9kc5c/azcZvNc+uXf7J6EaW21txPLuaeIn1zy+zL1rtDr/Ka95z1l93P/AI+Cfa8s75vCa05tLhlvUnm456vz3NluvXAB5lAAAEAAWAAoAyMyAAADQDoyAKAChCorUAAABoAFgACADQsKirAAWAAoNMrDSVQFQAaBYQUVYQaiRogFWqEDUZWFZahpBUWFGoEhWkrSwzCtRK1DUMQ1EqjcSsMRLUS1Ky3EtRLjhqJaSxuJbrZxRLUSsrOnPWzlrf1urEt1s3KzY7tNXDt7XeaujqRfS1LUtHjEvF1u5K3dMOS43cYywlfVezHpa4/sNlThfF6bXj3Co5Ts+I6Ua1Ij+TnnWfXWYeyae09FHbSsTsd7uex3E7/4ncxbc7K1vKLx8+nv70Q+F01Zh2dDcWrMTFpiXs4uqsv7f7q/fHmz4Pg+ndsPRR2n4DtZ4hOzpv8AhkxmnEOH3jcba0effr9H+tFXoWvsb6c86y9h7E+kXtP2V3Ua3COLbjQjPzqRbNbx5TWeUx7Yl9I2Xbb0ddtI+T7Y9m44Xv8AU5TxLhGNKZt+tfSn5lvXMc3vw55l6zfy9fwv6Xf2PPljcf8Af9/33vhdtCYno47ac5feOL+hfV4htL8Q7DcZ2Pafa1jvTp6E/J7qkfytG05+GfY+XcW7Pb/h+6vtt7tNfba+nOL6erpzS9Z8piecPRxzDk35LvX4z5z1n3s3Oz1er9zktaPKamytXrVx/m0x4Os4rDzx060ef7H6czud7MR02OrP2PG10J8nsfYvb51uITjpw/W+57Onw1lK48mXZ4ya85Sau5OjPenk1G2mfB9HyuHmdKunly00pl5HQ2N7zGIeY4fwHcbi3dppWtMzEcoSxm5yPXdLbWtPT6nkdlwnV1rRFaTM+x9h7J+hviu428cQ41bR4Lw+Iiba+9n5Pl6qzz+yPW8zxDtL6LPR/pRXhuz/AOUPEqdNfdR3dGJ84p4++Pe+byeJ8Utx4p57Ph6T530n47+x0nHle+Xafb+k9XovYv0U9o+0Hd1ttw+9NrEZtuNXGnpRHn3p5T7sy9x1OGejDsFo/Kcb4j/yi4jT/Jtpbu6FZ8ranW3u+D5v6QPTd2m7R1vt53c6G1ziuhpR3NOI8u7HX35fKOI8W3G51LX1ta17TPjL5vP1nJn9ZnqfDH9cvX8JPm78fB8J99/b99vtXbL078Y19rqcL7PaWhwXh2O7XR2dI04x67Rzl8c4tx3eb7WtqbjXvebevk8LrbmZzzdTU15nxfLz6uYy48c1Ps/X4/e92HTd95d67mvupnxdPV15nxcGpqOG93hz5bXqx45G9TU9bhvfLM2mWZlwtdZCZZkmUli1olmZWWZZrUJZlWWaohKMrCUCWVSUCUqpIDFUZWUZURZRmgCSggDLQAzQZWUZoAJVAGaABBqkc3keGaff1YdDTjm8/wBn9Dv61eT6HSYbyjlyXs9snGz7NR4W1rfVEftmXoXE9Tva08/F7x2x1I0NLS2kTy0dOKz7fH63z/dWzeZfQ8Qy8v0fg5cM33de082Fsj89nd16gByAAABKAAoAKAICYUQZGgABtkAagALAWEFFAUAFgAKAClAFiDUMrCwUBoAFAgFGhIVqMgCwAGoLAiqiwqQrUUhUWFQWEGolaEhWkWGoYWFGlhIFStLDMK0y3ErEsNQqNxKxLESsS1KjcS1EsRKwqabiWolxxLUS1KmnJFmq2cWViV2mnYi7kpd1Ys1WzUrOndpqzHi7OluJr0l4yt3JW/rdMeSxi4be18B7S8T4VutPcbLea2jqUnNbUvMTE+qYfYeB+m+nFdtpcN7e8F2XaHaVjuxqa9O7uKR/J1Y5w/PFNWY8XPTcTE9Xrx6nevP31+M+V9Z91efLgnu7P05fsL6PO2WnGv2K7TafD91fnHDuK2ivPypqRyn2TmXpfa70YdpuzV5/upwnX0dPOI1or3tO3svGa/W+U8P4ruNteL6Otekx5S+qdg/Tf2p7PUptZ3s7vY47tttuI+U05jxjuz092H0eHrM57OW/sy/+U/WX5vJnwWe78P2/a/c9YvwfUpbE0x7nsnYLg976nFZ7kzjhutP2Pp/Cu03op7cRWOJbKezXEb/43aRnQtPrpPT3fF7z2Q9F+npxutzwvinD+JbPcbe2lTW0dT9bzjw+t6+Txbh4cN8kuN+30+6zcv47eecHJndY9/8Afh6vzXThGpa+Ip4vYOA9ieKcU3FNDZbLV19W36OnSbTjz5eD7ruOyfYLsfpzue1PF9LW1q8/zTb25z7fH7HpPa70/bThe21eGdjeG7fhehEY79KxOpb1zPSJ+M+tvLxrPmn/AGvHuf8All2x/e/dGf8ApvLdcl+6d7+0+95DhHoj4fwTa13/AG14zteFaWMxoRaLa1/VER92XX4z6VexXYyttDsbwXRncRExG93UfKak+uI8PxyfAO1XbzjHGtzqa+73ure+pzta15mZ9sy9O3O+ve2ZtMvm8/L5+/UZ3P7PTH8PW/ffueri4b/6J5f838fd90fRe3XpT7RdpN3bV3nENa/XGbdPZHSPc+fb3iGprWm19S1pnxmXjNXczM9XW1NaZ8Xj5estnlnaT3e56uPppj397t6u4mfF1dTWmfFwW1HFa7w5ctr1Y4act9T1uG12JszMuVydJFtZmZEmWLWtEyzMkpMs2qSkySyjUhKEpMsqSkkozVgzKzKM1RCUSrBJWUZqgJLBEASqkgMgkqzPVmrABmqASlElAZoAJVAGaCx1RqvVrGbpXNoVzaIe8ditrE7mmpePm0+fb2Rzen7DT72rD6FwLTja8H1NaeU3+bHsjnP3Pu+H8ffby817PAdrtzOputSZnM5eo6s5mXmePa3f1rTnxeEvPN5Ou5PNlXTimoxKE9R8i+rsAMgAgAFABAAGgBKACAAAA3EAFQAUAGhYEVYACgAoALAAWIKgo0JCqADUABYENMrCpVAaQAUFhBoVYQhYkaIBVUIGog0ysNRlQFGolWIaiVFWEGksaWGYVWWolqJYiViVG4lYliJWJXaORcsRKxLW0biVywZXaacmViXHErldppyZaiziXK7TTmrdyRqOrFl7y7TTu01ZiOrm0txMTHN46LtV1JanJYzcNvP7Xf305ia3mJh7b2f7f8f4Pp2rseJ6+jFoxaK36x5PnFdXDlruJiOr1cfWZ49pXDPpscvWPcOK9qOIb+977jdal7W65t1eB3G9taZzaZeLnXnzcd9b1nJ1mefrTDp8cfSO5q7iZ8XXvrT5utbVyxN5eXLktd5hpzX1OfVxWuxNmZlztbkamzMygztrQJMszKbVZlESZZVZlmZJlJlFkJQSZZtUmUERRJEZUSVllkASUrQAxRJQEqhIks0AEoiLKM1YAM1RJWWWQAQgAzVAEoN0jmzDm0a5tDtxY7qV5fgej39WvLxe78WtG14ZXQjl3KYn2z1+uXgeyG1i24re0fNp86fc73ajX/gpjM5l+i4J/L4bXjyu8npfEtTvas83j7dXZ3Vs3mXVl8Hqct16sJ2QB4WwBKACAAAAgACwARQBAAAAaSgCoANAAsBYQUUBQAWAAsABUoA0LCstQsABQAUCAaGhIVWQBqAAsCFRYVKsKy0qiwhDSVQFRYVlYlqVFIBRqJViGolRViUFTTREpEq1KzppYlhcqN5WJYyuVTTeVyxkiV2jeVYyuV2NZXLOTJs03kyxlTaaayuWBTTfe9a96fNxhs033/Wk2ZTKbNNZlMpkybXSplMplNjUyzlMmU2KmUymU2ulykplEa0syiTKM2gTKTIi6BEllSSSWUAEmWapMgM1RJJlEIAMqShIyAJKCSAy0ASyJKAgAMrABAABa9Xd2NO9qQ6lI5vM8F0J1NasRHOZe3psN1zzuo9x4BpRt+HzeYxN/seE7T6+Z7uc+L2PUxo7aunHLuxiHpfaDV72vZ9vqb5OLyvNh3y28HrTmZcUt6k83HL81zXdeyADzqAJQAQAAAEoAAADQAmgANAAQAGoyAKACgAoQqK1AAUAFABQAWILCCjQDQAKACwIaZWFSqA0gAoANCrDKqjQkSqxSJVCJVKoCyosSrKxLW0UBRYlphYlRoSJVTS5VlcrtnS5XLKrtNNZMsrlRrK5YXINZXLGVyu001kyzkybNN5Ms5MmzTWTLOTJs0uTLOTPrNmmsplMplDTWUymUNquTKZRBcplMmU2oZRMptVSZBlRJJlEAmUmUQASZSqsygM1RJJRkgAlUJEZoAJQSRGasAGaok9VZSgAzQARQBAVFr1XGbpXLo1zaHtvZXb/AMJGpMcqxl6zsqd7UiHvXBdH5HZxOMTbm+10PH328/LXNxC+KTHR6NxbUm+tafOXtnFtXu6Vp9U/j4vS95bOpLp12fbTPFHUt1Znq1LL8/ne71QAcwAKADIAAAFABAAFgAKAACQqAAqUAVABYADUAgFFCBQAWAAoAKUAaRYVlqFgAKACgA0LCstKgAsQAagEAoqxLMSqo0JEqqkSqESqKAqLEqyrW0UBQhYlBRvIzlYlRVymQTS5VkXZpoTJldppcrlnKm00uRA2LlWRdjQyJsUyiZNmmsplMmU2ulGQ2LlAym1DKCGgQyiiZEygqTKCABMptUmQGVEmSZRkAEUBJlAkBkASUCUBloAQSUVGQASgAlUAQG6RzZcujXNodeLHdSvK8E0J1NesY6y9z5U0oiOURH1PBdmtDGdSY6RyeZ17YrP4/HJ+h6bHy4beTO7rxHHdWY0rRnnP4+56lrzm0vP8e1OXdnr+I+6XrupOZfO63Pu7cU7MT0RZR8fJ2AGQAAAZAAAAABAAFgAKAAy0ysMigKACxkAaABQAUIVFhYACgA0ACwAFQWEFGhIVQAagAKCxKCjQkKrIA0ACgRIKKsSzEqqNCRKrtSJVBTSgLtBcoLtNNCGWtooAGViUFGsrlhcmxoZyuVFEyuQ0BkyJoyuUA0AZDQGUyGlEyJtdLlMoZBRMoguTKBsBMoguUBNgCM7UmQE2okyTKIugBkASZQJkBAAZoMysolWADNUSVSUogCAAyQASqAAsdXc2VO9qQ6tIeZ4HofKa9eWYe3psN1zzuo9m4XpfJbWsdJnmu6vHd59Px+9y1xFPV+Pu+x097aZrMZ5zy+775fdv0cdPL73rnGtTOpjPg8Rfq73E9Tv61p85dCer4PV5byerCdmZCeo+fXQAQAAAEABAAAAKACAALsADbIDKtCQqgAqUAVABYACgA0KJCqACwAFABSgDSDTKwCgNAAoALAWEFRoSFaQAUAFAgFFEWJVGhlYldrtViUFFEyptABdimUF2mmhlcrtFDIuwAAMgouTKALkygC5MoILkygBkA2AJlBREBcoCbABNqEymRNqAkygrIIoAyAIgSAgAJQRWZZUARQBBJRUZABKACKAICotVxm6Vy6Nc2h7TwDRiunN58eX4/Hg9e2On3tSOT3DZUjS0a1x0jn+Pj8X2ei4/e8/JXY1JxHP3/j4vGcQ1MUmZn159eM/bLvas8sZ9Wfq/a8PxbU/grT5xz985+57eXLUc8Z3ev7q2by6zl1pzaXFL89z3devFAHlqgCAAAAlABAAAAAAQAAAAZAYjRDTKwooCwAFQAVABoAFgLCCigKADQALAAVABRYVlpYACgAoAKCwgsRoSFaQAUAF2AChlUFNNZVkEaEyq7UyuUFNKJlcm00ALsAF2i5MoGzS5XLIbNNDIu000MhsaMshsXJlBNmlyIG10AGzQBlNgZTIm1MgJs0CZRFWZQE2ACAkyCAAgAIAJMoEoDLQAgJKspQAQAEABKoAgN0hmHNo1zaHbix3UteX4Fod7Wi2OnP8AY9krMVry6R0/HweM4Lo9zRiZ5d7x/Hv+DyUzjn08fv8A2PvcGPlxeTK7ri157tZ9Ufu+3LwXGbxjET4z8I5Q8xuLYj2fdGZeu8Vv86K56RH7fvc+oy1i1hO7xt55sStuqS+ByXdeqIA5UAEAAAAABkAAAAAEAAAAGQGGgBRoSFAAaABYyAKACgAosCLCwAGgAUAFABYgsIKNCQqgAsABQAaBYlBRoSJVWQBQAUAFAyBsUQyqaayrIG2hMmV2qmQUXIgGlEMiaUTK5NgGTK7AMmTYBkymwEyZNiiALlMgGgBF0CZQFygJsAEQEyIujICAAmwAQASUCUBFAGaoCSgSgIACUAEUAQAAaq7vD9KdTVrWI5zLp0jm85wPQzbv+XKPbL39Lx7rnndR5zbUiunFY6Yx7v8AhE/FyXnz8cZ9/OfuSuMeUT9Wf3Q49W2YnHWY+uf3Ps+keZ1d1aZrPnMfXM5+x67xG8W1rTHTLzu7vEZmJ6TMx7o5PXNzOby8HV5dnbjjgnqzPVUl8XK93cAYoAIAAAAACAAgAAAAAAAJoZAYaACA0ysKKAsABUoAqACwAFAgGhRIVQAWAAoAKACxBYlBRoSFUAFABQAaAiQBVZWJVNKAu0AFABdgAoGQNi5EFTSrlnK5BcqyBtoZXK7XaiZMmxRMqbAA2AJk2KJkybFEygNJlBDa5QE2mwMpkFMoBoyAm1AEABAATYAkoCAigCKAIEsrKMgAAAyABVAEBY6o1VrGbpXLoVzaHtHC9LuaNY6TPj7f3Z+LwPDNH5TWrHr6vZ9CuKRiMTPT1Z6fU+z0mGpt5+SuWZ5cus9I9vKI+Dh1LRnMTyzMx7I6OS1v0o6c7R7OkOvrZxNY9VPvn63syrnHj+I27ulaPKsR8ebwGrOZl5fimpE0mY/StM49Tw1+r5XV5O/HGUWeiPl11AGQAQAAAAAEoAIAAAAAAAAMgObQAAAosKzDQADQACACoANAAsBYQUUBQAUAFABSgDSDUMqCgNAAoAAAKACi5EFTTQmVVABQAAAXYAAAKBkDYZXKAaUQVNKIBpRMmUNKJkyGlEA0ogGlymQF0ZAQADYAIACbABAATYAkyBMoCNACAAgJJMolABAAQAEUAQAAHJSMyxHVz7evevDvw47rNrzPBdHlNp5Z+bn7fqeZifm5xjlM49vKI+DqbHS7mlWkcpxEe+ev1cnbiY5W8Ppe6OUPucePlx082V3UvjOPDOPdHV1Ne84iZ64m7n1J7tZ9Vfrn9zqbqZiLxHXlT8fBc6R4jiduda+Vft5/e8bbq7vEbROvbE8s4j2OlPV8bqst5PRhOyShI8NbAAAGQAAAAAAAZAAAAAAAAGQHNoAAAAWEFGggUAFSgCxABQAUAFCFRYWAAoANAAsABUAFFVlQUBoADYAKAC7ABQAXYuVZBNNCZVUADYAKAAAC7AA2ABsADYAGwANgAbAA2ACAAAAmwAQADYAmUFTKCbXQAigAACAkyTKIACAAlABFgAUAEAAg1V5LhWlFtaJmOUc5ePpGZec4TpYpGf0p5+yOcvodLhuuWd7PK6UTFMz1xn32/c3fxrE8pmKZ9UdfuZpbGLePO8/d+PWzae7H82v1z/x+p9ZwZvbMxMxym02mPVH4l09a0xFJnrzv+Pg7OtOIt/JrFY9s9fvdDe27tdT1Vivv8fvcs72ajw24nN5cDk1ZzMuN8Tnu69OKT1AeZQAABkAAAAAAAEoAIAAAAAAMgOTQAoAAAEFhWVhRQFgAKlAFQAWAAoANCwIqgAoAKACgAqACiqyoKA0AAACgAoAAAKAC7FyZQE00MrkNKJlVQANgAbAA2AC7AA2ACbAA2ABsAAAEAQybFEyiLpcmUA0AJtQBAATYAAJMkyiAAgAAAMgAKAIAACx1RqrWM3SubbV714h7Ftqd2vcjrypHt8fx63iOGU/hO/P6MZ/Y8zpfNr/Nr9c/j6n2Omx1HnzrnzFuWeVrYifKI/H1Ge9jPKLWzPsj8SzM92J/k17vvnr96Xt3e9/Jr3ffPX73q2w47z3u73p+nfM/j4vGcQ1J+SmZn6d8z7v+LyGtbEz/ACKfb/xeI4jblSvlXn73Dmy1i1jO7x955srbqk9HxOS93piAOQAAAJQAQAAAAAAAEABAAAABkBxaAGgAAAAAUaEhQAGgAGQBQAaABYBAKKECgAsABQAUAFQBVEagFABQAAAUAAAF2AAACgAAAbDK5QXYuTKBtNKrIGmhkDTQzkyGmhnJk2aaGQ2aaRBNmlyZQDS5QBQBNgAbABAAAAQAAEmSZRNgAgAAAMgAKAJQAAAAclIzLEdXY21JvqRWOsziHfhx3WbXlOH6cRp1iY+lPen2R+Jd/T5xXvfpTN7euPxl1tGPmz3f0pilfZH4hzzblaY6TMVr7Pxh9nCajz3u5InPc73PMza3s/GWJnvRWJnne2Z/HxS9sd+Y8Iikfj3SxacWn+RTHx/fLVo49xfNL28b2/H2w8VxG2de0ZzETiPdyeSvOJ046xEd6Y/Hqh4bcTm8vJ1GX0XTCd3DPVJCXx8nZAGQAAASgAgAAAAAAAAAGgAQAEGQHFoAWAAoAAAALCCjQkKoAKlAFiACgAoALAWEFFAUAFgAKACgAqKrKw0KAoALoADQAAAAAAAAALsADYAKAAAAAAAAAAAAACbAA2ACAAAAAAmwAABJlBUQQAAAAAEABFAAAEAAAAg1V39hXGb+UYj2y6WnGZeV2lIrWkTHL6Vvx+Or6HTYe9zzrt0+b/Ur9c/j6m6z3Zr/ACI70+3w+5x0zMViZ53nMz6vxlZtmtrfr2x+PqfQji1GMadZ6TPen2fiGNS0zpzaet7fj7YW04tqTH6Md2Ps/az0vpxj6Md6Y+v7EtHBurYnVnP0a92PseI1ZzMvIbm2NCZn9K32f8Xjby8PVZOuEZSVSer5ldQBAAAAAAZAAAAAAAAAAAAAAGQHnaAAAFABQAAAWCwrKwCgLAAVKAKgAsABQAUIVCFgoCgAoAKACgAu0VWRZRoTJlqUUBqUFwixLU1UQVeS+U2yNd1JiYS4U2gDOlAEAAAAAAAAAAAAAAAAAAAAAA2ACAAAAAJlE2LMoCAAAAAAgAIoAAAgAAAALHVGqtYzdK59rTv6kR4eMvJ6eZpMxHO84iPV+MOntK92lreM8o/H46u9X5tv+zr9f/GX1uHHWLhlXJmIm9o6RHdj8fFqJxesfqV70+3r+xxRjFKec5km+a3v42nH3/sd9stTn5OtY62t/wAPvZ1LRnVtHSIxX8ewzjUjn9Cv19ftcGpbGh1+lb7P+LNpHX3tsUpWPLM/j4Ohbq7W+n+FmP1eXw5OrPV83qcu7tjERZR4a2AAAAAAAIACAAAAAAAAAAAADIDztAAACwAFAAAAABRoSFAAUAFQAVABYACgA0LEiLBAAUAFABQAUABABdguUFGsjK5XYq5ZyrUyGolYlgdJyJpyYiTuZ6SxEysWluZY31TRNJjwTDkrqNROnPWMexfJjfSm64MDn+Trb6Non28mbaVo6xKXip5nENTVJhzuFXaBgZ0oAAAgAAAJsADYAAAAAAAACZE2GRBAAAAAAQAEAAUAAASgAAAAAA5KRmWIdja1ibxnpHOXfhx3WbXc0I7s1jwpHen2/jEOauZpER1vP4+9xUz3Jmedry5c4vaY6UjEfZ+99TH0ca3Nud7x0iO7X7PsTx06T06z+PYxzmtKR1tOfugm2bal46RGI+z7GtotrzNdS89bTj7/ALnHeY7+nWekREz9q2zNKUjrPP7vucerb5+raOkROPs+9m1Y6OtbNpmXC3qTzYfJ5ruu8J6Iso89UAAAAAAAQAEAAAAAAAAAAAAGQHnaAAAAAFABQAAAICwgo0JCgANAARkAUAGgAAAaFgRVAAABoAAAFAATQAuwAUAAXK5ZDY0IZXYpkGpkNRaW6atq9JmHEOmPJYmnZjVifpVifcY0recOssWl1nNv1TyuedKJ6Wj3szpW8ma6kt11G/oZJ3cc0mPBmay7MXiTFZ8ILxS+ht1sI7M6dZ6MzpeTneGr5nAOSdOWZpMeDneOxdsi4lMMXGqAJoAEAAAEmEDKAgAAAAAAAJsAEAAXQAAAUAEAAAAAAg1V29CuNPPjace78YdbTjMu9p8r+rTj6/8Ai9/T4+9zyc1eV/Vpx9f/ABOmnEeNpz+PrYicaXrtLecavq04+z972Oa5/hbTHSkYj7GZnGlEfrTn8fWmcaX86fs/4tf42lesUjn9sgkzjXnw7kfXEftdbUnGjPrn8fc5c/wepbzxH3/c4NxONOke2fx8HPkuo1HVt1ZWeqPlZ3u7QlFlHKgAAAAAAAAAAAmgAQAAAAAAAAZAedoAAAAAAAaAAAAABQhplYBQFgAKlAFiACgAoALAAUUSFUAAAGgAAAXYABoAVABQAAAAVAFyrIuxoZXJsUTKtTIWLTDcXcY3jyWJpzRduLOssWmHbHmTyuzk5OGLtRZ0mcqabmsSzNIXvLlrtUcc6aTpuXIzePGrtwTSfJMS7GISasXhi7dfA55pEszSHO8NNuIbmiTSWLx1dsphrEoxcaqI0M6GRcGEEAAAQAEIACgAACAAAAAAAsI1WGsZulc+2jE979Xm7FeWnHnaXFpxjTiPG05c9cfKZ8KR9n730+OajlW45avq04+z97OcaUz42nH4+pmJxpTPjacfj6mpiJvSnhEc/tddstYidSlJ6REZ+1mLTPyl56z9/wCJItmb39U/WzacaMR5zn8fWbDU5aVY8ZmZdbdz/CY6YiIdi+J1aVmeUYifvdPWtNrzM+PN5+bLWLWLjlAfNydUnqEjAAAAAAAAAAAAAAAAJoAEAAAAGQHnaAAAAAAAFgAKAAAAACjQkKAAoAKgAqACgAoAKBAKKJCqAAADQAAALsAAABABQAUAAAAAAAAUygDWRkXY0JkysyG4tLUXcY6Y8liac0WWJcGWos648qac0SZccWay6zOJpvr6xnJlraNfjyTBE/iDx/EAmMpNYa9v1ns+qU1BiaeqftZmnrcvL1fYfH7WbxyrtwzSUxLmxHqJj2/axeKLtwYMObuxPlKTSPKWLwm3Dgw5JpHmk0nw5ud4qu3GNzEpj1MXCqyLgwz5RBcIml2AJoAEAAAAByaVZtaIhiHPoRiJt5PRw47rNrn08d+bR0rHL7ljlp+u0sdNOI/WnP4+tycp1YrPSsc/ve+OdWYib1pPSI5/eRbM3vPX9v4lK2nF7z16fH8Sk8tKI/WnP4+tdizONKI/WnP4+tbRnUpTPKIiEtGdSlM8oiISLTN739Uz8f8AiDM2mb3v6pn48vvdO/V2bTjStPjM4dW3V5OovZvFAHhrZKKIIAgAAAAAAAAAAAAAAAAAJoAEGQHnaAAAAAAAAAFABQAAAAWEFGgAAGgAEAFQAWAAoAKCxKCihEigAAA0AAAAACgAGgAQAXYAKAAAAAAAAAACoAuVyyLsaWJmGFysysG4s1FsuLKumPKmnLnz+tcuKJmFi3udZySppyxP4gzHqYifeufxLpMk03n2+893wZ+MGff7F2NZ9fxg93wlM+v4nu+C7RffE+09eJ90pnPjn2r7pgDr4/GDu/yfhJ18Yn2k+uJgE98+9MZ8IlrPr+Jj+T8E0rE1jxiYSaR4S5Ix4TMHOfKUuEptxfJz4c2ZrMdYc0xHjExJjyt8WLxRduDHqTDsYn9WJ9jMxHjEw53hNuHA5e5WfH4p8nOOWJ97F4au3EOSaTHWGcepzvHYu2RcLhJjTZWHYrHKtY6zzcelXNohz062v5dHs4cNRm1qMfKZ8K/clZxS1vGeRHLTmfOcFo5Vr49fj+Iehkty06x582pjOrWs9I5T95ynW84r9kM1n6Vs88faC1mZte8+Uz8f+LPTSmfOcfj6jppT/Kn8fampy06Rn1/j4JRjWnGnWPbP4+Drz1c24n52PKIhwvFz3u3igDyNCTKyhQAQAAAAAAAAAAAAAAAAAAAAZAeVoAAAAAAAAAWAAoAAAAAECFQUaAWAAoADIAoAKACgAoLEoKKESKAAACgAoAAAKAAAAgAAAoAGwAXYAAAAAAAJsADYAGxcmUF2NLFp9rC5amdg5ItHsXLiysT5Os5U05Yn1/FfjDj73msW8pdZnKmm/hJ08ZhnPnC59bUyRrn5RPsMx4TMJy8Ywc/OJa2NdfKU5euE5eMTC8/OJ9psXn5xJOPGJhnl4xMLE+VvdIi+y3uk5+NYn1wkz5198HzfCcKHzfXC8+kWifUfOn+V9acvLHsBZz1mse1MVnzj61jzrbH1L87xiJgGYj9WxMW/ViY9i5rPhj2GI8LfFNDOKz1r8JWKVmeU49sNx3/531tafdmYzT4SswlNuTR289ybRNZzyjm3bQtTTiJrMd7m5opSe7SJmJ8pjxctaz8rml4mK+vHKHomEY26d9Ke/WnlyZiM6k3xiI5+zyd2JvEWveufXMdcs/M+SmZpjM45SXCG3SrXFLW9zMxjSiP1p/H3u5fT0/k6xEzEzz5wzq6Gb1pS1ZxER1x9rNwXbqanKK19WU1IzrRXymKuxfRt8tmaz3Yny8Idb9K0z5S55TTUcOtbvXmfOcuJq/Vl83lu66QAcVAAMIoaEFwiAAAAAAAAAAAAAAAAAADIDytAAAAAAAAAAACgAoAAAAAKLCsrAKAsABUAFiAAADQAAAKCxKCihEigAAAoAKAAAC7AAAAAATQAAAAAAAAAAAAAAAAAGgAXQAppcmUFlTTUTMdJai3nDjXLc5LDTlifKVz5xhw5ai0x4us5YmnJnyleXjGHHFo8eTUTPhOXSZbRqM+EnLxhMx48iJ8py1Kix6rE58awmY8Ywseqy7NHzfOYWO94T3vrSZ84OXhOPabFzHjGDl4W+J87HnHxTNZ6xj2KjWb4zPOPPqZrPWMeyWYj9W33NZt+lGfaC1iJnlb48na21dTvZmO9WOc+MOrXuzPOJj2O5pV7unmt4zbl1w64RK5qWie9e1OfnE+MrWKfJzMWmJtOOcfj1M2tetKxaM5584L2pM1p3cTEY5T4uzDeL106xS3OefKTVtaJrS1YnEeMMTFLauIvyjlzjwSt9WL2vEziOc4nMGxq1tO2tiazEZxynwYi1Las37+JjM848XFGvERabVrM4x0w62prVxPdiYzy5y55ckjUxcs3nT71ovHTliXV1Na1sxM5z1YtaZYmXi5effaOkxJQHiyu2wBkAAAAAAMJhQ0ILhMIAAAAAAAAAAAAAAMgPK0AAAAAAAAAAAAANAAAAAAAQCjQkKAAoAKlAFiAAAC7ABQAUFiUFFEiVUAAAF2ACgAAAAAuwAAAAAAADQAJoADQALoADQAAAAAAAAAbAA2ABs0uVyyNTJNNxafa1ExPqcS5dJy33mnLmcecHL2OOJai3nzdZySppuM+E5Mx4wzExPSWszHXm3MkXHlJMz4xn2pmJ9SxmOk59jUofNnzhaxaJ+bOfYmYnrHwIiJnlPxWVHLpzmcWrE/U7WKWvFIma45c3BoTevzpjMRz5826Xpi1piY8OTvj6M1z1m86uazmseU+EM11Z71r3rEzHPy5uLMRpzNbROeXk476166fdnnmfGPBbnpNOaL6fdtbM18I8XBbV7lbd22ZnycGpq5jEREexxTLz588no3MXLqatrRibTLimUyjx58tybkVAcbVAGQAAAAAAAAAAAAwmFAQVMJoAAAAAAAAAAZAeVoAAAAAAAAAAAAAWAAoAAAAALAahlYBQAAGgAEAFQAAAaAAABQAUUQNigKAAAC7ABQAAAAAAAXYAAAAAAAAAAAAAGwATYAAAAAAAAAAAAAGxcrFpjpLI3M7E05ItHjHwajE9JcRl1nL8U05u9PjGfasd2fHDii0x4tRaJ6xh1xzlTTsxNqafzZ685wl9WO7FZrHnOOTr2vz5M2tMzmZby5pPRPK5L6nKIjpDjm0yzlHmz5bWpFygONrQAzsAEAAAAAAAAAAAAAAAAAABMKAgqYTQAAAAAAyA8rQAAAAAAAAAAAAAAA0AAAAAAACiwrLQACwAFAAZAFABQAUAAAGgAAhUWCAAoAAAAANAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAuUF2aXKAbNACAAgAIAAAAAAAAAAAAAAAAAAAAAAAACYUBBUwmgABkB5WgAAAAAAAAAAAAAABYACgAAAAAQFgFFAAAaAASgCxAAABYACgAsABQABQFAAAAABYACgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAgAIAAAAAAAAAAAAAAAAAAAAAAAAAAP/2Q==" alt="" width="34" height="34" loading="lazy">
        </span>
        <span class="footer-tagline">Let's work.</span>
      </div>
      <nav class="footer-nav" aria-label="Footer navigation">
        <a href="#home">Home</a>
        <a href="#works">Works</a>
        <a href="#faq">FAQ</a>
        <a href="client.html">Client Portal</a>
      </nav>
    </div>
    <div class="footer-bottom">
      <span class="footer-copy">© 2026 Unfiltered Motion. All rights reserved.</span>
      <span class="footer-credit">Designed &amp; built by Unfiltered Motion</span>
    </div>
  </div>
</footer>

<script>
(() => {
  'use strict';

  /* === NAV: scroll state + mobile toggle + active link === */
  const nav = document.getElementById('nav');
  const navToggle = document.getElementById('navToggle');
  const navLinks = document.getElementById('navLinks');

  const onScroll = () => nav.classList.toggle('scrolled', window.scrollY > 40);
  onScroll();
  window.addEventListener('scroll', onScroll, { passive: true });

  navToggle.addEventListener('click', () => {
    const isOpen = navLinks.classList.toggle('open');
    navToggle.setAttribute('aria-expanded', String(isOpen));
  });
  navLinks.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', () => {
      navLinks.classList.remove('open');
      navToggle.setAttribute('aria-expanded', 'false');
    });
  });

  // Active link highlighting based on scroll position
  const sections = ['home', 'works', 'services', 'process', 'faq'];
  const navAnchors = Array.from(navLinks.querySelectorAll('a[href^="#"]'));
  const sectionEls = sections.map(id => document.getElementById(id)).filter(Boolean);
  const sectionObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const id = entry.target.id;
        navAnchors.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + id));
      }
    });
  }, { rootMargin: '-45% 0px -50% 0px' });
  sectionEls.forEach(el => sectionObserver.observe(el));

  /* === REVEAL ON SCROLL === */
  const revealObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));

  /* === FAQ ACCORDION (single-open, accessible) === */
  document.querySelectorAll('.faq-item').forEach(item => {
    const btn = item.querySelector('.faq-q');
    btn.addEventListener('click', () => {
      const willOpen = item.dataset.open !== 'true';
      document.querySelectorAll('.faq-item').forEach(i => {
        i.dataset.open = 'false';
        i.querySelector('.faq-q').setAttribute('aria-expanded', 'false');
      });
      if (willOpen) {
        item.dataset.open = 'true';
        btn.setAttribute('aria-expanded', 'true');
      }
    });
  });

  /* === VIDEO EMBEDS ===
     Click-to-load pattern: replaces the placeholder button with an
     iframe pointed at the data-video-embed URL (Vimeo or YouTube). */
  function loadVideo(container) {
    const trigger = container.querySelector('[data-video-embed]');
    if (!trigger) return;
    const url = trigger.getAttribute('data-video-embed');
    if (!url) {
      // No URL configured yet — keep placeholder visible.
      return;
    }
    const iframe = document.createElement('iframe');
    // Use nocookie domain + referrerpolicy to fix YouTube Error 153
    const nocookieUrl = url.replace('youtube.com/embed/', 'youtube-nocookie.com/embed/');
    iframe.src = nocookieUrl + (nocookieUrl.includes('?') ? '&' : '?') + 'autoplay=1&rel=0';
    iframe.title = 'Project video';
    iframe.allow = 'autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; gyroscope';
    iframe.setAttribute('referrerpolicy', 'strict-origin-when-cross-origin');
    iframe.allowFullscreen = true;
    iframe.loading = 'lazy';
    container.innerHTML = '';
    container.appendChild(iframe);
  }
  document.querySelectorAll('[data-video-embed]').forEach(trigger => {
    trigger.addEventListener('click', () => loadVideo(trigger.closest('.video-frame')));
  });

  /* === WORKS GRID ===
     Edit this array to configure each project card.
     embedUrl: a Vimeo (https://player.vimeo.com/video/ID) or
     YouTube (https://www.youtube.com/embed/ID) embed URL.
     poster: a thumbnail image shown before the video loads. */
  const PROJECTS = [
    {
      title: 'SectionCut — Architecture Thought Leadership',
      tag: 'YouTube Channel',
      embedUrl: 'https://www.youtube-nocookie.com/embed/wv4isuuv9dM',
      poster: 'https://img.youtube.com/vi/wv4isuuv9dM/maxresdefault.jpg'
    },
    {
      title: 'SaaS Promo — App Launch Reel',
      tag: 'Motion Design',
      embedUrl: 'https://www.youtube-nocookie.com/embed/LtXH4UutzBw',
      poster: 'https://img.youtube.com/vi/LtXH4UutzBw/maxresdefault.jpg'
    },
    {
      title: 'Short-Form Vertical Edit',
      tag: 'Social Content',
      embedUrl: 'https://www.youtube-nocookie.com/embed/aJBWjsXy2xw',
      poster: 'https://img.youtube.com/vi/aJBWjsXy2xw/maxresdefault.jpg'
    }
  ];

  const grid = document.getElementById('worksGrid');
  PROJECTS.forEach((p, i) => {
    const card = document.createElement('div');
    card.className = 'work-item reveal' + (i > 0 ? ' reveal-delay-' + i : '');

    const wrap = document.createElement('div');
    wrap.className = 'work-video-wrap';

    if (p.embedUrl) {
      // Click-to-play: show thumbnail, click loads iframe inline
      const btn = document.createElement('button');
      btn.className = 'video-placeholder';
      btn.type = 'button';
      btn.setAttribute('data-video-embed', p.embedUrl);
      btn.setAttribute('aria-label', 'Play: ' + p.title);
      btn.style.cssText = 'position:absolute;inset:0;padding:0;border:none;background:transparent;display:block;cursor:pointer;';

      if (p.poster) {
        const img = document.createElement('img');
        img.className = 'video-poster';
        img.src = p.poster;
        img.alt = '';
        img.loading = 'lazy';
        img.onerror = () => { img.src = p.poster.replace('maxresdefault', 'hqdefault'); };
        btn.appendChild(img);
      }

      const overlay = document.createElement('div');
      overlay.className = 'video-overlay';
      const playWrap = document.createElement('div');
      playWrap.className = 'play-btn';
      playWrap.setAttribute('aria-hidden', 'true');
      playWrap.innerHTML = '<svg width="18" height="20" viewBox="0 0 18 20" fill="white"><path d="M1 1l16 9-16 9V1z"/></svg>';
      overlay.appendChild(playWrap);
      btn.appendChild(overlay);
      btn.addEventListener('click', () => loadVideo(wrap));
      wrap.appendChild(btn);
    } else {
      const placeholder = document.createElement('div');
      placeholder.className = 'video-placeholder';
      const playWrap = document.createElement('div');
      playWrap.className = 'play-btn';
      playWrap.setAttribute('aria-hidden', 'true');
      playWrap.innerHTML = '<svg width="18" height="20" viewBox="0 0 18 20" fill="white"><path d="M1 1l16 9-16 9V1z"/></svg>';
      const label = document.createElement('p');
      label.textContent = 'Add embed URL in script';
      placeholder.appendChild(playWrap);
      placeholder.appendChild(label);
      wrap.appendChild(placeholder);
    }

    const info = document.createElement('div');
    info.className = 'work-info';
    info.innerHTML = `<span class="work-title">${p.title}</span><span class="work-tag">${p.tag}</span>`;

    card.appendChild(wrap);
    card.appendChild(info);
    grid.appendChild(card);
    revealObserver.observe(card);
  });

  /* === CONTACT FORM: validation + success state with Calendly CTA === */
  const form = document.getElementById('contactForm');
  const successPanel = document.getElementById('contactSuccess');

  const FIELDS = {
    'cf-name':    { errId: 'err-name',    validate: v => v.trim().length > 0 },
    'cf-email':   { errId: 'err-email',   validate: v => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v.trim()) },
    'cf-message': { errId: 'err-message', validate: v => v.trim().length >= 10 }
  };

  function validateField(id) {
    const el = document.getElementById(id);
    const cfg = FIELDS[id];
    const errEl = document.getElementById(cfg.errId);
    const valid = cfg.validate(el.value);
    el.setAttribute('aria-invalid', String(!valid));
    errEl.classList.toggle('visible', !valid);
    return valid;
  }

  Object.keys(FIELDS).forEach(id => {
    const el = document.getElementById(id);
    el.addEventListener('blur', () => validateField(id));
    el.addEventListener('input', () => {
      if (el.getAttribute('aria-invalid') === 'true') validateField(id);
    });
  });

  form.addEventListener('submit', (e) => {
    e.preventDefault();
    let allValid = true;
    Object.keys(FIELDS).forEach(id => {
      if (!validateField(id)) allValid = false;
    });
    if (!allValid) {
      const firstInvalid = form.querySelector('[aria-invalid="true"]');
      if (firstInvalid) firstInvalid.focus();
      return;
    }

    const submitBtn = form.querySelector('.btn-submit');
    submitBtn.disabled = true;
    submitBtn.textContent = 'Sending…';

    // Simulated submission delay — replace with a real endpoint (e.g. Formspree, Web3Forms, or a serverless function).
    setTimeout(() => {
      form.style.display = 'none';
      successPanel.classList.add('visible');
      successPanel.focus?.();
    }, 600);
  });

})();
</script>
</body>
</html>
