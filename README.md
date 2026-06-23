<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Smart Craft Ventures — Premium Formwork Solutions</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Inter:wght@300;400;500&family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --black:   #080808;
  --dark:    #0D0D0D;
  --dark2:   #141414;
  --dark3:   #1A1A1A;
  --gold:    #C9A84C;
  --gold2:   #E2C07A;
  --gold3:   #F0D9A0;
  --goldlt:  rgba(201,168,76,0.12);
  --goldbdr: rgba(201,168,76,0.25);
  --white:   #FFFFFF;
  --offwhite:#F5F2EC;
  --muted:   rgba(255,255,255,0.45);
  --border:  rgba(255,255,255,0.08);
}

html { scroll-behavior: smooth; }

body {
  font-family: 'Inter', sans-serif;
  background: var(--black);
  color: var(--offwhite);
  font-size: 15px;
  line-height: 1.75;
  overflow-x: hidden;
}

/* SCROLLBAR */
::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-track { background: var(--dark); }
::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 2px; }

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 6%;
  height: 72px;
  background: rgba(8,8,8,0.92);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border);
  transition: all 0.3s;
}

nav.scrolled {
  height: 60px;
  border-bottom-color: var(--goldbdr);
}

.nav-logo {
  display: flex; flex-direction: column; line-height: 1;
  text-decoration: none;
}

.nav-logo-main {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px;
  font-weight: 600;
  color: var(--offwhite);
  letter-spacing: 0.05em;
}

.nav-logo-sub {
  font-size: 9px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-top: 2px;
}

.nav-links {
  display: flex; gap: 36px; list-style: none; align-items: center;
}

.nav-links a {
  text-decoration: none;
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--muted);
  transition: color 0.25s;
  position: relative;
}

.nav-links a::after {
  content: '';
  position: absolute; bottom: -4px; left: 0; right: 0;
  height: 1px; background: var(--gold);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.3s;
}

.nav-links a:hover { color: var(--offwhite); }
.nav-links a:hover::after { transform: scaleX(1); }

.nav-cta {
  border: 1px solid var(--gold) !important;
  color: var(--gold) !important;
  padding: 9px 22px;
  border-radius: 2px;
  font-size: 11px !important;
  letter-spacing: 0.15em !important;
  transition: all 0.3s !important;
}

.nav-cta:hover {
  background: var(--gold) !important;
  color: var(--black) !important;
}

.nav-cta::after { display: none !important; }

/* HERO */
#home {
  min-height: 100vh;
  display: flex; align-items: center;
  background: var(--black);
  position: relative; overflow: hidden;
  padding-top: 72px;
}

.hero-bg {
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse 60% 50% at 70% 50%, rgba(201,168,76,0.06) 0%, transparent 70%),
    radial-gradient(ellipse 40% 60% at 20% 80%, rgba(201,168,76,0.04) 0%, transparent 60%);
}

.hero-lines {
  position: absolute; inset: 0; overflow: hidden; opacity: 0.04;
}

.hero-lines line { stroke: var(--gold); }

.hero-inner {
  max-width: 1200px; margin: 0 auto; padding: 100px 6%;
  display: grid; grid-template-columns: 1.1fr 0.9fr;
  gap: 80px; align-items: center; position: relative; z-index: 2;
}

.hero-tag {
  display: inline-flex; align-items: center; gap: 12px;
  font-size: 10px; font-weight: 500;
  letter-spacing: 0.22em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 28px;
}

.hero-tag::before {
  content: ''; display: block;
  width: 32px; height: 1px; background: var(--gold);
}

.hero-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(48px, 6vw, 80px);
  font-weight: 300;
  line-height: 1.05;
  color: var(--offwhite);
  letter-spacing: -0.5px;
  margin-bottom: 24px;
}

.hero-title em {
  font-style: italic;
  color: var(--gold2);
}

.hero-title strong {
  font-weight: 600;
  display: block;
}

.hero-sub {
  font-size: 15px;
  color: var(--muted);
  line-height: 1.8;
  max-width: 440px;
  margin-bottom: 48px;
  font-weight: 300;
}

.hero-btns { display: flex; gap: 16px; flex-wrap: wrap; align-items: center; }

.btn-gold {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--gold);
  color: var(--black);
  font-size: 11px; font-weight: 600;
  letter-spacing: 0.15em; text-transform: uppercase;
  padding: 15px 32px; border-radius: 2px;
  text-decoration: none;
  transition: all 0.3s;
}

.btn-gold:hover { background: var(--gold2); }

.btn-ghost {
  display: inline-flex; align-items: center; gap: 10px;
  border: 1px solid rgba(255,255,255,0.2);
  color: var(--offwhite);
  font-size: 11px; font-weight: 500;
  letter-spacing: 0.15em; text-transform: uppercase;
  padding: 15px 32px; border-radius: 2px;
  text-decoration: none;
  transition: all 0.3s;
}

.btn-ghost:hover { border-color: var(--gold); color: var(--gold); }

/* Hero visual */
.hero-visual { position: relative; }

.hero-card {
  background: var(--dark2);
  border: 1px solid var(--goldbdr);
  border-radius: 4px;
  padding: 40px;
  position: relative; overflow: hidden;
}

.hero-card::before {
  content: '';
  position: absolute; top: 0; left: 0; right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--gold), transparent);
}

.hero-card-label {
  font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 20px;
}

.hero-product-list { list-style: none; display: flex; flex-direction: column; gap: 0; }

.hero-product-item {
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 0;
  border-bottom: 1px solid var(--border);
  font-size: 13px; color: rgba(255,255,255,0.7);
  transition: color 0.2s;
  cursor: default;
}

.hero-product-item:last-child { border-bottom: none; }
.hero-product-item:hover { color: var(--gold2); }

.hero-product-item span:last-child {
  font-size: 10px; letter-spacing: 0.1em;
  color: var(--gold); opacity: 0.7;
}

.hero-ornament {
  position: absolute; bottom: -20px; right: -20px;
  width: 100px; height: 100px;
  border: 1px solid var(--goldbdr);
  border-radius: 50%; opacity: 0.3;
}

.hero-ornament2 {
  position: absolute; bottom: -10px; right: -10px;
  width: 60px; height: 60px;
  border: 1px solid var(--goldbdr);
  border-radius: 50%; opacity: 0.5;
}

/* MARQUEE */
.marquee-strip {
  background: var(--gold);
  padding: 14px 0;
  overflow: hidden;
  white-space: nowrap;
}

.marquee-inner {
  display: inline-flex; gap: 0;
  animation: marquee 20s linear infinite;
}

.marquee-inner span {
  font-size: 11px; font-weight: 600;
  letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--black);
  padding: 0 32px;
}

.marquee-inner span::after {
  content: '◆';
  margin-left: 32px;
  opacity: 0.4;
}

@keyframes marquee {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

/* STATS */
.stats-section {
  background: var(--dark2);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}

.stats-inner {
  max-width: 1200px; margin: 0 auto; padding: 0 6%;
  display: grid; grid-template-columns: repeat(4, 1fr);
}

.stat-item {
  padding: 48px 32px;
  border-right: 1px solid var(--border);
  text-align: center;
  position: relative;
}

.stat-item:last-child { border-right: none; }

.stat-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 52px; font-weight: 300;
  color: var(--offwhite);
  line-height: 1;
  margin-bottom: 8px;
}

.stat-num em { font-style: normal; color: var(--gold); }

.stat-label {
  font-size: 10px; font-weight: 500;
  letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--muted);
}

/* SECTION COMMON */
section { padding: 120px 0; }

.container { max-width: 1200px; margin: 0 auto; padding: 0 6%; }

.sec-tag {
  display: inline-flex; align-items: center; gap: 12px;
  font-size: 10px; font-weight: 500;
  letter-spacing: 0.22em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 20px;
}

.sec-tag::before {
  content: ''; width: 24px; height: 1px; background: var(--gold);
}

.sec-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(36px, 4vw, 54px);
  font-weight: 300;
  color: var(--offwhite);
  letter-spacing: -0.3px;
  line-height: 1.1;
  margin-bottom: 20px;
}

.sec-title em { font-style: italic; color: var(--gold2); }

.sec-sub {
  font-size: 15px; color: var(--muted);
  max-width: 520px; line-height: 1.8;
  font-weight: 300; margin-bottom: 64px;
}

/* PRODUCTS */
#products { background: var(--black); }

.products-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
}

.product-card {
  background: var(--dark);
  padding: 44px 36px;
  position: relative; overflow: hidden;
  transition: background 0.3s;
  cursor: default;
}

.product-card::after {
  content: '';
  position: absolute; bottom: 0; left: 0; right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--gold), transparent);
  transform: scaleX(0); transform-origin: center;
  transition: transform 0.4s;
}

.product-card:hover { background: var(--dark2); }
.product-card:hover::after { transform: scaleX(1); }

.product-number {
  font-family: 'Cormorant Garamond', serif;
  font-size: 64px; font-weight: 300;
  color: rgba(255,255,255,0.04);
  line-height: 1;
  position: absolute; top: 20px; right: 28px;
  transition: color 0.3s;
}

.product-card:hover .product-number { color: rgba(201,168,76,0.08); }

.product-icon-wrap {
  width: 52px; height: 52px;
  border: 1px solid var(--goldbdr);
  border-radius: 2px;
  display: flex; align-items: center; justify-content: center;
  font-size: 22px;
  margin-bottom: 24px;
  transition: border-color 0.3s;
}

.product-card:hover .product-icon-wrap { border-color: var(--gold); }

.product-name {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px; font-weight: 600;
  color: var(--offwhite);
  margin-bottom: 12px; letter-spacing: 0.02em;
}

.product-desc {
  font-size: 13px; color: var(--muted);
  line-height: 1.7; font-weight: 300;
  margin-bottom: 20px;
}

.product-tag {
  font-size: 9px; font-weight: 600;
  letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--gold);
  border: 1px solid var(--goldbdr);
  padding: 4px 12px; border-radius: 1px;
  display: inline-block;
}

/* GALLERY */
#gallery { background: var(--dark2); padding: 120px 0; }

.gallery-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  grid-template-rows: 300px 300px;
  gap: 2px;
}

.gallery-item {
  position: relative; overflow: hidden;
  display: flex; align-items: flex-end;
}

.gallery-item:first-child { grid-row: 1 / 3; }

.gallery-fill {
  position: absolute; inset: 0;
  transition: transform 0.6s ease;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column; gap: 8px;
}

.gallery-item:hover .gallery-fill { transform: scale(1.04); }

.g1 { background: linear-gradient(135deg, #0a1628 0%, #0d1f3c 100%); }
.g2 { background: linear-gradient(135deg, #111111 0%, #1a1a1a 100%); }
.g3 { background: linear-gradient(135deg, #1a1200 0%, #2a1e00 100%); }
.g4 { background: linear-gradient(135deg, #0d1520 0%, #152030 100%); }
.g5 { background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 100%); }

.gallery-ph-icon { font-size: 40px; opacity: 0.25; }
.gallery-ph-text { font-size: 11px; letter-spacing: 0.1em; text-transform: uppercase; opacity: 0.2; color: var(--offwhite); }

.gallery-caption {
  position: relative; z-index: 2;
  padding: 20px 24px;
  background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, transparent 100%);
  width: 100%;
}

.gallery-caption-text {
  font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
  color: rgba(255,255,255,0.6); font-weight: 500;
}

.gallery-caption-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px; font-weight: 400;
  color: var(--offwhite); margin-top: 2px;
}

.gallery-notice {
  text-align: center; margin-top: 32px;
  font-size: 12px; color: rgba(255,255,255,0.25);
  letter-spacing: 0.08em;
}

/* ABOUT */
#about { background: var(--black); }

.about-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 100px; align-items: center;
}

.about-visual-block {
  position: relative;
}

.about-main-card {
  background: var(--dark2);
  border: 1px solid var(--goldbdr);
  padding: 52px 44px;
  border-radius: 2px;
  position: relative;
}

.about-main-card::before {
  content: '';
  position: absolute; top: 0; left: 0; bottom: 0;
  width: 2px;
  background: linear-gradient(to bottom, transparent, var(--gold), transparent);
}

.about-card-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 28px; font-weight: 300;
  color: var(--offwhite);
  margin-bottom: 32px;
  line-height: 1.3;
}

.values-list { list-style: none; display: flex; flex-direction: column; gap: 20px; }

.value-item { display: flex; align-items: flex-start; gap: 16px; }

.value-line {
  width: 1px; height: 40px; flex-shrink: 0;
  background: linear-gradient(to bottom, var(--gold), transparent);
  margin-top: 4px;
}

.value-content strong {
  display: block; font-size: 13px; font-weight: 500;
  color: var(--offwhite); margin-bottom: 3px;
  letter-spacing: 0.03em;
}

.value-content p {
  font-size: 12px; color: var(--muted); font-weight: 300; line-height: 1.6;
}

.about-float-badge {
  position: absolute; bottom: -24px; right: -24px;
  background: var(--gold);
  color: var(--black);
  width: 96px; height: 96px;
  border-radius: 50%;
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  text-align: center;
}

.about-float-badge .num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 28px; font-weight: 600; line-height: 1;
}

.about-float-badge .lbl {
  font-size: 8px; font-weight: 700;
  letter-spacing: 0.1em; text-transform: uppercase;
  margin-top: 2px;
}

.about-text-content p {
  font-size: 15px; color: var(--muted);
  line-height: 1.85; font-weight: 300; margin-bottom: 20px;
}

.why-strip {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 0; border-top: 1px solid var(--border); margin-top: 80px;
  border-left: 1px solid var(--border);
}

.why-item {
  padding: 36px 32px;
  border-right: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  transition: background 0.3s;
}

.why-item:hover { background: var(--dark2); }

.why-item-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 40px; font-weight: 300;
  color: var(--goldbdr); line-height: 1;
  margin-bottom: 12px;
}

.why-item-title {
  font-size: 14px; font-weight: 500;
  color: var(--offwhite); margin-bottom: 8px;
  letter-spacing: 0.02em;
}

.why-item-desc { font-size: 12px; color: var(--muted); font-weight: 300; line-height: 1.65; }

/* CONTACT */
#contact { background: var(--dark2); }

.contact-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 80px; align-items: start;
}

.contact-form { display: flex; flex-direction: column; gap: 16px; }

.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }

.contact-form input,
.contact-form textarea,
.contact-form select {
  width: 100%;
  background: var(--dark);
  border: 1px solid var(--border);
  border-radius: 2px;
  padding: 14px 18px;
  font-size: 13px;
  color: var(--offwhite);
  font-family: 'Inter', sans-serif;
  font-weight: 300;
  transition: border-color 0.25s;
  outline: none;
  -webkit-appearance: none;
}

.contact-form select option { background: var(--dark); }

.contact-form input::placeholder,
.contact-form textarea::placeholder { color: rgba(255,255,255,0.2); }

.contact-form input:focus,
.contact-form textarea:focus,
.contact-form select:focus { border-color: var(--gold); }

.contact-form textarea { resize: vertical; min-height: 130px; }

.contact-form button {
  background: var(--gold);
  color: var(--black);
  font-weight: 600; font-size: 11px;
  letter-spacing: 0.18em; text-transform: uppercase;
  padding: 16px 36px; border: none; border-radius: 2px;
  cursor: pointer; font-family: 'Inter', sans-serif;
  transition: background 0.3s; width: fit-content;
}

.contact-form button:hover { background: var(--gold2); }

.contact-info-side h3 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 32px; font-weight: 300;
  color: var(--offwhite); margin-bottom: 40px;
  line-height: 1.2;
}

.contact-detail {
  display: flex; align-items: flex-start; gap: 18px;
  padding: 20px 0;
  border-bottom: 1px solid var(--border);
}

.contact-detail:last-of-type { border-bottom: none; }

.contact-detail-icon {
  width: 40px; height: 40px;
  border: 1px solid var(--goldbdr);
  display: flex; align-items: center; justify-content: center;
  font-size: 16px; flex-shrink: 0; border-radius: 2px;
}

.contact-detail strong {
  display: block; font-size: 10px; font-weight: 600;
  letter-spacing: 0.15em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 4px;
}

.contact-detail span { font-size: 14px; color: rgba(255,255,255,0.65); font-weight: 300; }

.wa-btn {
  display: inline-flex; align-items: center; gap: 10px;
  background: transparent; border: 1px solid #25D366;
  color: #25D366;
  font-size: 11px; font-weight: 600;
  letter-spacing: 0.15em; text-transform: uppercase;
  padding: 13px 24px; border-radius: 2px;
  text-decoration: none;
  margin-top: 32px;
  transition: all 0.3s;
}

.wa-btn:hover { background: #25D366; color: var(--black); }

#form-msg { font-size: 13px; color: var(--gold); display: none; margin-top: 4px; letter-spacing: 0.05em; }

/* FOOTER */
footer {
  background: var(--black);
  border-top: 1px solid var(--border);
  padding: 40px 6%;
  display: flex; align-items: center; justify-content: space-between;
  flex-wrap: wrap; gap: 16px;
}

.footer-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 20px; font-weight: 600;
  color: var(--offwhite);
}

.footer-logo span { color: var(--gold); }

.footer-text {
  font-size: 11px; color: rgba(255,255,255,0.2);
  letter-spacing: 0.08em;
  text-align: center;
}

.footer-links {
  display: flex; gap: 24px;
}

.footer-links a {
  font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
  color: rgba(255,255,255,0.25); text-decoration: none;
  transition: color 0.2s;
}

.footer-links a:hover { color: var(--gold); }

/* REVEAL ANIMATION */
.reveal {
  opacity: 0; transform: translateY(24px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}

.reveal.visible { opacity: 1; transform: translateY(0); }

/* MOBILE */
@media (max-width: 900px) {
  .hero-inner, .about-grid, .contact-grid { grid-template-columns: 1fr; gap: 48px; }
  .hero-visual { display: none; }
  .products-grid { grid-template-columns: 1fr 1fr; }
  .stats-inner { grid-template-columns: 1fr 1fr; }
  .gallery-grid { grid-template-columns: 1fr 1fr; grid-template-rows: auto; }
  .gallery-item:first-child { grid-row: auto; }
  .why-strip { grid-template-columns: 1fr; }
  .nav-links { display: none; }
  .form-row { grid-template-columns: 1fr; }
  footer { flex-direction: column; text-align: center; }
  .footer-links { justify-content: center; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav id="navbar">
  <a class="nav-logo" href="#home">
    <span class="nav-logo-main">Smart Craft</span>
    <span class="nav-logo-sub">Ventures · New Delhi</span>
  </a>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#products">Products</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact" class="nav-cta">Get Quote</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="home">
  <div class="hero-bg"></div>
  <svg class="hero-lines" viewBox="0 0 1400 900" preserveAspectRatio="xMidYMid slice">
    <line x1="0" y1="150" x2="1400" y2="150" stroke-width="1"/>
    <line x1="0" y1="350" x2="1400" y2="350" stroke-width="1"/>
    <line x1="0" y1="550" x2="1400" y2="550" stroke-width="1"/>
    <line x1="0" y1="750" x2="1400" y2="750" stroke-width="1"/>
    <line x1="200" y1="0" x2="200" y2="900" stroke-width="1"/>
    <line x1="500" y1="0" x2="500" y2="900" stroke-width="1"/>
    <line x1="900" y1="0" x2="900" y2="900" stroke-width="1"/>
    <line x1="1200" y1="0" x2="1200" y2="900" stroke-width="1"/>
  </svg>

  <div class="hero-inner">
    <div class="reveal">
      <div class="hero-tag">Premium Formwork Solutions</div>
      <h1 class="hero-title">
        Crafted for<br>
        <em>Precision.</em><br>
        <strong>Built to Last.</strong>
      </h1>
      <p class="hero-sub">Smart Craft Ventures supplies the complete range of aluminium formwork consumables and structural accessories to construction sites across India.</p>
      <div class="hero-btns">
        <a href="#products" class="btn-gold">Explore Products →</a>
        <a href="#contact" class="btn-ghost">Request a Quote</a>
      </div>
    </div>

    <div class="hero-visual reveal" style="transition-delay:0.2s">
      <div class="hero-card">
        <div class="hero-card-label">Our Product Range</div>
        <ul class="hero-product-list">
          <li class="hero-product-item"><span>Aluminium Formwork Shuttering Oil</span><span>Consumable</span></li>
          <li class="hero-product-item"><span>Industrial Grease</span><span>Consumable</span></li>
          <li class="hero-product-item"><span>Formstop Sealing</span><span>Sealing</span></li>
          <li class="hero-product-item"><span>PVC Pipe & Cone — Tierods</span><span>Structural</span></li>
          <li class="hero-product-item"><span>Toeboards</span><span>Safety</span></li>
          <li class="hero-product-item"><span>MS Plank</span><span>Structural</span></li>
        </ul>
        <div class="hero-ornament"></div>
        <div class="hero-ornament2"></div>
      </div>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-strip">
  <div class="marquee-inner">
    <span>Shuttering Oil</span><span>Formstop</span><span>MS Plank</span>
    <span>PVC Cones</span><span>Toeboards</span><span>Grease</span>
    <span>New Delhi</span><span>Pan-India Supply</span>
    <span>Shuttering Oil</span><span>Formstop</span><span>MS Plank</span>
    <span>PVC Cones</span><span>Toeboards</span><span>Grease</span>
    <span>New Delhi</span><span>Pan-India Supply</span>
  </div>
</div>

<!-- STATS -->
<div class="stats-section">
  <div class="stats-inner">
    <div class="stat-item reveal">
      <div class="stat-num">6<em>+</em></div>
      <div class="stat-label">Product Lines</div>
    </div>
    <div class="stat-item reveal" style="transition-delay:0.1s">
      <div class="stat-num">Pan<em>-</em>India</div>
      <div class="stat-label">Supply Reach</div>
    </div>
    <div class="stat-item reveal" style="transition-delay:0.2s">
      <div class="stat-num">100<em>%</em></div>
      <div class="stat-label">Quality Assured</div>
    </div>
    <div class="stat-item reveal" style="transition-delay:0.3s">
      <div class="stat-num">Fast</div>
      <div class="stat-label">Delivery Turnaround</div>
    </div>
  </div>
</div>

<!-- PRODUCTS -->
<section id="products">
  <div class="container">
    <div class="sec-tag reveal">Our Range</div>
    <h2 class="sec-title reveal">Formwork Products<br>for <em>Every Site</em></h2>
    <p class="sec-sub reveal">Precision-engineered consumables and structural components that keep your shuttering systems running without interruption.</p>

    <div class="products-grid">
      <div class="product-card reveal">
        <div class="product-number">01</div>
        <div class="product-icon-wrap">🛢</div>
        <div class="product-name">Shuttering Oil</div>
        <p class="product-desc">Premium aluminium formwork release oil ensuring smooth panel removal, clean concrete finish and extended panel life.</p>
        <span class="product-tag">Consumable</span>
      </div>
      <div class="product-card reveal" style="transition-delay:0.1s">
        <div class="product-number">02</div>
        <div class="product-icon-wrap">⚙️</div>
        <div class="product-name">Grease</div>
        <p class="product-desc">High-performance industrial grease for formwork pin joints, hardware and mechanical components on site.</p>
        <span class="product-tag">Consumable</span>
      </div>
      <div class="product-card reveal" style="transition-delay:0.2s">
        <div class="product-number">03</div>
        <div class="product-icon-wrap">🔩</div>
        <div class="product-name">Formstop</div>
        <p class="product-desc">Reliable sealing solution to prevent concrete leakage at formwork joints, delivering a smooth pour every time.</p>
        <span class="product-tag">Sealing</span>
      </div>
      <div class="product-card reveal" style="transition-delay:0.1s">
        <div class="product-number">04</div>
        <div class="product-icon-wrap">🔗</div>
        <div class="product-name">PVC Pipe & Cone</div>
        <p class="product-desc">Durable PVC sleeves and cones for tierod systems, ensuring proper concrete cover and clean tie-hole finishing.</p>
        <span class="product-tag">Structural</span>
      </div>
      <div class="product-card reveal" style="transition-delay:0.2s">
        <div class="product-number">05</div>
        <div class="product-icon-wrap">🪵</div>
        <div class="product-name">Toeboards</div>
        <p class="product-desc">Safety-compliant toeboards for formwork platforms and scaffolding edges, meeting all site safety standards.</p>
        <span class="product-tag">Safety</span>
      </div>
      <div class="product-card reveal" style="transition-delay:0.3s">
        <div class="product-number">06</div>
        <div class="product-icon-wrap">🔧</div>
        <div class="product-name">MS Plank</div>
        <p class="product-desc">Heavy-duty mild steel planks for working platforms, walkways and scaffolding decking at construction sites.</p>
        <span class="product-tag">Structural</span>
      </div>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section id="gallery">
  <div class="container">
    <div class="sec-tag reveal">Project Gallery</div>
    <h2 class="sec-title reveal">Products <em>in Action</em></h2>
    <p class="sec-sub reveal">A showcase of Smart Craft Ventures products across real construction sites.</p>

    <div class="gallery-grid reveal">
      <div class="gallery-item">
        <div class="gallery-fill g1">
          <div class="gallery-ph-icon">🏗</div>
          <div class="gallery-ph-text">Add Site Photo</div>
        </div>
        <div class="gallery-caption">
          <div class="gallery-caption-text">Aluminium Formwork</div>
          <div class="gallery-caption-title">High-Rise Site, Delhi</div>
        </div>
      </div>
      <div class="gallery-item">
        <div class="gallery-fill g2">
          <div class="gallery-ph-icon">🛢</div>
          <div class="gallery-ph-text">Add Product Photo</div>
        </div>
        <div class="gallery-caption">
          <div class="gallery-caption-text">Application</div>
          <div class="gallery-caption-title">Shuttering Oil</div>
        </div>
      </div>
      <div class="gallery-item">
        <div class="gallery-fill g3">
          <div class="gallery-ph-icon">🔩</div>
          <div class="gallery-ph-text">Add Site Photo</div>
        </div>
        <div class="gallery-caption">
          <div class="gallery-caption-text">Tierod System</div>
          <div class="gallery-caption-title">PVC Cones & Pipes</div>
        </div>
      </div>
      <div class="gallery-item">
        <div class="gallery-fill g4">
          <div class="gallery-ph-icon">🪵</div>
          <div class="gallery-ph-text">Add Site Photo</div>
        </div>
        <div class="gallery-caption">
          <div class="gallery-caption-text">Platform</div>
          <div class="gallery-caption-title">MS Plank Walkways</div>
        </div>
      </div>
      <div class="gallery-item">
        <div class="gallery-fill g5">
          <div class="gallery-ph-icon">🏢</div>
          <div class="gallery-ph-text">Add Project Photo</div>
        </div>
        <div class="gallery-caption">
          <div class="gallery-caption-text">Delivery</div>
          <div class="gallery-caption-title">Project Fulfilment</div>
        </div>
      </div>
    </div>
    <p class="gallery-notice">Replace placeholders with your own site photographs to complete the gallery</p>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="about-grid">
      <div class="about-visual-block reveal">
        <div class="about-main-card">
          <div class="about-card-title">Why contractors trust<br>Smart Craft Ventures</div>
          <ul class="values-list">
            <li class="value-item">
              <div class="value-line"></div>
              <div class="value-content">
                <strong>Consistent Quality</strong>
                <p>Products tested to match the demands of aluminium and conventional formwork systems.</p>
              </div>
            </li>
            <li class="value-item">
              <div class="value-line"></div>
              <div class="value-content">
                <strong>Competitive Pricing</strong>
                <p>Transparent rate cards with MOQ-based slabs — no hidden charges.</p>
              </div>
            </li>
            <li class="value-item">
              <div class="value-line"></div>
              <div class="value-content">
                <strong>Reliable Supply</strong>
                <p>Timely dispatch so your site never faces a material shortage.</p>
              </div>
            </li>
            <li class="value-item">
              <div class="value-line"></div>
              <div class="value-content">
                <strong>Technical Support</strong>
                <p>Application guidance from a team that understands formwork.</p>
              </div>
            </li>
          </ul>
        </div>
        <div class="about-float-badge">
          <div class="num">6+</div>
          <div class="lbl">Products</div>
        </div>
      </div>

      <div class="about-text-content reveal" style="transition-delay:0.15s">
        <div class="sec-tag">About Us</div>
        <h2 class="sec-title" style="margin-bottom:24px">Specialists in<br><em>Formwork Supply</em></h2>
        <p>Smart Craft Ventures is a dedicated formwork products supplier serving civil construction contractors, EPC firms, and real estate developers across India from New Delhi.</p>
        <p>We supply the complete range of consumables and structural components needed for both aluminium and conventional shuttering systems — from release oils and greases to MS planks, toeboards, and tierod accessories.</p>
        <p>Our focus is simple: give site teams exactly what they need, when they need it, at prices that make sense for every project size.</p>
        <a href="#contact" class="btn-gold" style="margin-top:16px; display:inline-flex">Contact Us →</a>
      </div>
    </div>

    <div class="why-strip reveal" style="transition-delay:0.2s">
      <div class="why-item">
        <div class="why-item-num">01</div>
        <div class="why-item-title">Full Formwork Range</div>
        <p class="why-item-desc">One supplier for all your formwork consumables — reduces procurement complexity on site.</p>
      </div>
      <div class="why-item">
        <div class="why-item-num">02</div>
        <div class="why-item-title">Flexible Order Quantities</div>
        <p class="why-item-desc">From small trial orders to bulk supply — MOQs that match your project scale.</p>
      </div>
      <div class="why-item">
        <div class="why-item-num">03</div>
        <div class="why-item-title">Fast Turnaround</div>
        <p class="why-item-desc">Quick quotation response and reliable dispatch — your schedule is never held up.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="sec-tag reveal">Get in Touch</div>
    <h2 class="sec-title reveal">Request a <em>Quote</em></h2>
    <p class="sec-sub reveal">Share your requirement and we'll send a competitive quotation within 24 hours.</p>

    <div class="contact-grid">
      <form class="contact-form reveal" onsubmit="handleSubmit(event)">
        <div class="form-row">
          <input type="text" placeholder="Your name" required>
          <input type="text" placeholder="Company / Firm name">
        </div>
        <div class="form-row">
          <input type="tel" placeholder="Phone number" required>
          <input type="email" placeholder="Email address">
        </div>
        <select>
          <option value="" disabled selected>Product of interest</option>
          <option>Shuttering Oil</option>
          <option>Grease</option>
          <option>Formstop</option>
          <option>PVC Pipe & Cone (Tierods)</option>
          <option>Toeboards</option>
          <option>MS Plank</option>
          <option>Full Range Inquiry</option>
        </select>
        <textarea placeholder="Describe your requirement — quantity, packing size, project location..."></textarea>
        <button type="submit">Send Inquiry →</button>
        <p id="form-msg">✦ Thank you — we'll respond within 24 hours.</p>
      </form>

      <div class="contact-info-side reveal" style="transition-delay:0.15s">
        <h3>Let's build something<br>great together.</h3>
        <div class="contact-detail">
          <div class="contact-detail-icon">📍</div>
          <div>
            <strong>Location</strong>
            <span>New Delhi, India</span>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">📞</div>
          <div>
            <strong>Phone & WhatsApp</strong>
            <span>+91 97291 39139</span>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">✉️</div>
          <div>
            <strong>Email</strong>
            <span>smartcraftventures@gmail.com</span>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-detail-icon">🕐</div>
          <div>
            <strong>Business Hours</strong>
            <span>Mon – Sat · 9:00 AM – 6:00 PM</span>
          </div>
        </div>
        <a class="wa-btn" href="https://wa.me/919729139139?text=Hi%20Smart%20Craft%20Ventures%2C%20I%20would%20like%20to%20inquire%20about%20your%20formwork%20products." target="_blank">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
          Chat on WhatsApp
        </a>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Smart Craft <span>Ventures</span></div>
  <div class="footer-text">© 2025 Smart Craft Ventures · New Delhi · +91 97291 39139 · smartcraftventures@gmail.com</div>
  <div class="footer-links">
    <a href="#products">Products</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script>
// Nav scroll effect
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
  navbar.classList.toggle('scrolled', window.scrollY > 60);
});

// Scroll reveal
const reveals = document.querySelectorAll('.reveal');
const revObs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) { e.target.classList.add('visible'); }
  });
}, { threshold: 0.1 });
reveals.forEach(r => revObs.observe(r));

// Active nav
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('.nav-links a');
const secObs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      navLinks.forEach(a => a.style.color = '');
      const active = document.querySelector(`.nav-links a[href="#${e.target.id}"]`);
      if (active && !active.classList.contains('nav-cta')) {
        active.style.color = 'var(--gold)';
      }
    }
  });
}, { threshold: 0.4 });
sections.forEach(s => secObs.observe(s));

// Form
function handleSubmit(e) {
  e.preventDefault();
  document.getElementById('form-msg').style.display = 'block';
  e.target.reset();
}
</script>
</body>
</html>
