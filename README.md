<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PULSE X — True Wireless Earbuds</title>
<meta name="description" content="PULSE X pairs studio-tuned 11mm drivers with adaptive noise cancellation. 38 hours of playback. $179.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@400;500;600;700&family=Bricolage+Grotesque:opsz,wght@12..96,400..800&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
--bg:#16140F;
--bg-elevated:#211D16;
--bg-elevated-2:#2A2419;
--copper:#C97A3D;
--copper-bright:#F0A868;
--cream:#F2EDE4;
--taupe:#948C7C;
--taupe-dim:#5C5648;
--border:rgba(242,237,228,0.09);
--font-display:'Bricolage Grotesque', sans-serif;
--font-body:'Archivo', sans-serif;
--font-mono:'IBM Plex Mono', monospace;
}

*{ margin:0; padding:0; box-sizing:border-box; }
html{ scroll-behavior:smooth; }

body{
background:var(--bg);
color:var(--cream);
font-family:var(--font-body);
line-height:1.5;
overflow-x:hidden;
position:relative;
}

body::before{
content:'';
position:fixed;
inset:0;
z-index:999;
pointer-events:none;
opacity:0.035;
mix-blend-mode:overlay;
background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}

img,svg{ display:block; max-width:100%; }
a{ color:inherit; text-decoration:none; }
ul{ list-style:none; }
button{ font-family:inherit; border:none; background:none; cursor:pointer; color:inherit; }

.container{ width:min(1160px, 90%); margin:0 auto; }

a:focus-visible, button:focus-visible, .swatch:focus-visible{
outline:2px solid var(--copper-bright);
outline-offset:4px;
}

h1,h2,h3{ font-family:var(--font-display); font-weight:700; letter-spacing:-0.01em; }

.eyebrow{
font-family:var(--font-mono);
font-size:0.75rem;
letter-spacing:0.16em;
text-transform:uppercase;
color:var(--copper-bright);
}

/* ---------- reveal-on-scroll ---------- */
.reveal{ opacity:0; transform:translateY(28px); transition:opacity 0.9s ease, transform 0.9s ease; }
.reveal.in-view{ opacity:1; transform:translateY(0); }
.reveal-delay-1.in-view{ transition-delay:0.1s; }
.reveal-delay-2.in-view{ transition-delay:0.22s; }
.reveal-delay-3.in-view{ transition-delay:0.34s; }

/* ---------- buttons ---------- */
.btn{
display:inline-flex;
align-items:center;
justify-content:center;
padding:0.95rem 1.9rem;
border-radius:100px;
font-weight:600;
font-size:0.95rem;
transition:transform 0.25s ease, background 0.25s ease, border-color 0.25s ease;
white-space:nowrap;
}
.btn-primary{ background:var(--copper); color:#1A1610; }
.btn-primary:hover{ background:var(--copper-bright); transform:translateY(-2px); }
.btn-ghost{ border:1px solid var(--border); color:var(--cream); }
.btn-ghost:hover{ border-color:var(--copper); color:var(--copper-bright); transform:translateY(-2px); }
.btn-small{ padding:0.6rem 1.3rem; font-size:0.85rem; }

/* ---------- nav ---------- */
#mainNav{
position:fixed; top:0; left:0; right:0; z-index:500;
padding:1.4rem 0;
transition:background 0.4s ease, padding 0.4s ease, border-color 0.4s ease;
border-bottom:1px solid transparent;
}
#mainNav.scrolled{
background:rgba(22,20,15,0.82);
backdrop-filter:blur(16px);
-webkit-backdrop-filter:blur(16px);
padding:1rem 0;
border-bottom:1px solid var(--border);
}
.nav-inner{ display:flex; align-items:center; justify-content:space-between; gap:2rem; }
.logo{ font-family:var(--font-display); font-weight:800; font-size:1.2rem; letter-spacing:0.02em; }
.nav-links{ display:flex; gap:2.2rem; font-size:0.92rem; color:var(--taupe); }
.nav-links a:hover{ color:var(--copper-bright); }

@media (max-width:768px){ .nav-links{ display:none; } }

/* ---------- hero ---------- */
.hero{
position:relative;
min-height:100vh;
display:flex;
flex-direction:column;
align-items:center;
justify-content:center;
text-align:center;
padding:8rem 1.5rem 4rem;
overflow:hidden;
}
.hero-glow{
position:absolute;
top:38%; left:50%;
width:60vw; height:60vw; max-width:800px; max-height:800px;
transform:translate(-50%,-50%);
background:radial-gradient(circle, rgba(201,122,61,0.16), transparent 70%);
pointer-events:none;
}
.hero-content{ position:relative; z-index:2; max-width:820px; }
.hero-content .eyebrow{ margin-bottom:1.4rem; }
.hero-title{
font-size:clamp(2.4rem, 6.4vw, 4.6rem);
line-height:1.05;
margin-bottom:1.5rem;
}
.hero-title .accent{ color:var(--copper-bright); }
.hero-sub{
font-size:clamp(1rem, 1.6vw, 1.2rem);
color:var(--taupe);
max-width:560px;
margin:0 auto 2.4rem;
}
.hero-actions{ display:flex; gap:1rem; justify-content:center; flex-wrap:wrap; margin-bottom:5rem; }

.hero-eq{
position:absolute;
bottom:0; left:0; right:0;
height:min(34vh, 280px);
display:flex;
align-items:flex-end;
justify-content:center;
gap:5px;
z-index:1;
-webkit-mask-image:linear-gradient(to top, black 30%, transparent 95%);
mask-image:linear-gradient(to top, black 30%, transparent 95%);
}
.eq-bar{
width:4px;
min-height:6px;
border-radius:3px 3px 0 0;
background:linear-gradient(to top, var(--copper) 0%, var(--copper-bright) 100%);
opacity:0.55;
transform-origin:bottom;
animation:eqPulse ease-in-out infinite;
}
@keyframes eqPulse{
0%,100%{ transform:scaleY(0.15); }
50%{ transform:scaleY(1); }
}

.scroll-cue{
position:relative; z-index:2;
display:flex; flex-direction:column; align-items:center; gap:0.6rem;
font-family:var(--font-mono); font-size:0.7rem; letter-spacing:0.14em; text-transform:uppercase; color:var(--taupe-dim);
}
.scroll-line{ width:1px; height:40px; background:linear-gradient(to bottom, var(--copper), transparent); animation:scrollDrop 2s ease-in-out infinite; }
@keyframes scrollDrop{ 0%{ opacity:0.2; } 50%{ opacity:1; } 100%{ opacity:0.2; } }

/* ---------- stats strip ---------- */
.stats-strip{
background:var(--bg-elevated);
border-top:1px solid var(--border);
border-bottom:1px solid var(--border);
}
.stats-inner{
display:grid;
grid-template-columns:repeat(4,1fr);
text-align:center;
}
.stat{ padding:2.2rem 1rem; border-left:1px solid var(--border); }
.stat:first-child{ border-left:none; }
.stat-value{ font-family:var(--font-mono); font-size:clamp(1.4rem,3vw,2rem); color:var(--copper-bright); }
.stat-label{ font-size:0.78rem; color:var(--taupe); margin-top:0.4rem; }
@media (max-width:640px){
.stats-inner{ grid-template-columns:repeat(2,1fr); }
    .stat:nth-child(3){ border-left:none; }
  }

  /* ---------- signal divider ---------- */
  .signal-divider{ position:relative; height:1px; width:min(90%,1000px); margin:5.5rem auto; background:linear-gradient(90deg, transparent, var(--taupe-dim) 50%, transparent); }
  .signal-dot{ position:absolute; left:50%; top:50%; width:6px; height:6px; background:var(--copper-bright); border-radius:50%; transform:translate(-50%,-50%); box-shadow:0 0 14px var(--copper-bright); animation:signalPulse 2.4s ease-in-out infinite; }
  @keyframes signalPulse{ 0%,100%{ opacity:0.35; transform:translate(-50%,-50%) scale(1); } 50%{ opacity:1; transform:translate(-50%,-50%) scale(2); } }

  /* ---------- feature rows ---------- */
  .features{ padding:2rem 0 1rem; }
  .feature-row{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:4rem;
    align-items:center;
    padding:3.5rem 0;
  }
  .feature-row.reverse .feature-visual{ order:2; }
  .feature-row.reverse .feature-text{ order:1; }
  .feature-tag{ font-family:var(--font-mono); font-size:0.72rem; letter-spacing:0.16em; text-transform:uppercase; color:var(--copper); margin-bottom:1rem; }
  .feature-text h3{ font-size:clamp(1.5rem,3vw,2.1rem); margin-bottom:1.1rem; line-height:1.15; }
  .feature-text p{ color:var(--taupe); font-size:1rem; max-width:440px; }
  .feature-visual{ display:flex; align-items:center; justify-content:center; height:280px; position:relative; }

  @media (max-width:860px){
    .feature-row, .feature-row.reverse{ grid-template-columns:1fr; gap:2rem; }
    .feature-row.reverse .feature-visual, .feature-row.reverse .feature-text{ order:unset; }
    .feature-visual{ height:220px; order:-1; }
  }

  /* rings visual (ANC) */
  .rings{ position:relative; width:200px; height:200px; }
  .ring{ position:absolute; top:50%; left:50%; border:1px solid var(--copper); border-radius:50%; opacity:0; animation:ringExpand 3.2s ease-out infinite; }
  .ring:nth-child(2){ animation-delay:1.05s; }
  .ring:nth-child(3){ animation-delay:2.1s; }
  .ring-core{ position:absolute; top:50%; left:50%; width:14px; height:14px; background:var(--copper-bright); border-radius:50%; transform:translate(-50%,-50%); box-shadow:0 0 20px var(--copper-bright); }
  @keyframes ringExpand{
    0%{ width:14px; height:14px; opacity:0.9; transform:translate(-50%,-50%); }
    100%{ width:200px; height:200px; opacity:0; transform:translate(-50%,-50%); }
  }

  /* waveform visual (Sound) */
  .waveform{ width:100%; max-width:280px; }
  .waveform path{ fill:none; stroke:var(--copper-bright); stroke-width:2; stroke-linecap:round; stroke-dasharray:600; stroke-dashoffset:600; animation:drawWave 3.5s ease-in-out infinite; }
  @keyframes drawWave{ 0%{ stroke-dashoffset:600; } 50%{ stroke-dashoffset:0; } 100%{ stroke-dashoffset:-600; } }

  /* battery visual (Endurance) */
  .battery-shell{ width:190px; height:100px; border:2px solid var(--taupe-dim); border-radius:14px; position:relative; overflow:hidden; padding:5px; }
  .battery-shell::after{ content:''; position:absolute; right:-10px; top:38px; width:7px; height:24px; background:var(--taupe-dim); border-radius:0 3px 3px 0; }
  .battery-fill{ height:100%; width:20%; background:linear-gradient(90deg, var(--copper), var(--copper-bright)); border-radius:8px; animation:batteryCharge 3.6s ease-in-out infinite; }
  @keyframes batteryCharge{ 0%{ width:8%; } 55%{ width:96%; } 100%{ width:96%; } }

  /* earbud silhouette (Fit) with tilt */
  .earbud-wrap{ perspective:900px; }
  .earbud-shape{ width:120px; height:150px; position:relative; transition:transform 0.15s ease-out; transform-style:preserve-3d; }
  .earbud-shape .body{ width:100%; height:78%; background:linear-gradient(150deg, #E9DFC9, #C9B48F); border-radius:48% 48% 45% 45%/58% 58% 42% 42%; box-shadow:0 18px 40px rgba(0,0,0,0.45), inset 0 2px 3px rgba(255,255,255,0.5); position:absolute; top:0; }
  .earbud-shape .stem{ width:22%; height:46%; background:linear-gradient(180deg, #C9B48F, #A88F63); border-radius:0 0 10px 10px; position:absolute; bottom:-30%; left:39%; box-shadow:inset 0 -2px 3px rgba(0,0,0,0.2); }
  .earbud-shape .dot{ position:absolute; top:14%; left:50%; width:8px; height:8px; background:var(--copper); border-radius:50%; transform:translateX(-50%); }

  /* ---------- colors ---------- */
  .colors-section{ padding:6rem 0; text-align:center; }
  .colors-section h2{ font-size:clamp(1.7rem,3.4vw,2.4rem); margin-bottom:0.7rem; }
  .colors-section > .container > p{ color:var(--taupe); margin-bottom:3rem; }
  .swatch-row{ display:flex; justify-content:center; gap:1.6rem; flex-wrap:wrap; margin-bottom:2.4rem; }
  .swatch{ display:flex; flex-direction:column; align-items:center; gap:0.7rem; padding:0.4rem; border-radius:16px; transition:transform 0.25s ease; }
  .swatch:hover{ transform:translateY(-4px); }
  .swatch-color{ width:52px; height:52px; border-radius:50%; border:2px solid rgba(242,237,228,0.15); transition:border-color 0.25s ease, box-shadow 0.25s ease; }
  .swatch[aria-pressed="true"] .swatch-color{ border-color:var(--copper-bright); box-shadow:0 0 0 4px rgba(240,168,104,0.18); }
  .swatch-name{ font-size:0.8rem; color:var(--taupe); }
  .color-preview{ width:130px; height:160px; margin:0 auto; border-radius:48% 48% 45% 45%/58% 58% 42% 42%; background:var(--preview-color, #C9B48F); box-shadow:0 20px 50px rgba(0,0,0,0.5), inset 0 2px 3px rgba(255,255,255,0.35); transition:background 0.4s ease; }

  /* ---------- specs ---------- */
  .specs-section{ padding:6rem 0; }
  .specs-section h2{ font-size:clamp(1.7rem,3.4vw,2.4rem); margin-bottom:3rem; text-align:center; }
  .specs-grid{ display:grid; grid-template-columns:1fr 1fr; gap:0; border-top:1px solid var(--border); max-width:820px; margin:0 auto; }
  .spec-row{ display:flex; justify-content:space-between; padding:1.1rem 1.4rem; border-bottom:1px solid var(--border); font-family:var(--font-mono); font-size:0.88rem; }
  .spec-row:nth-child(odd){ border-right:1px solid var(--border); }
  .spec-label{ color:var(--taupe); }
  .spec-value{ color:var(--cream); }
  @media (max-width:700px){
    .specs-grid{ grid-template-columns:1fr; }
    .spec-row:nth-child(odd){ border-right:none; }
  }

  /* ---------- reviews ---------- */
  .reviews-section{ padding:6rem 0; background:var(--bg-elevated); border-top:1px solid var(--border); border-bottom:1px solid var(--border); }
  .reviews-top{ text-align:center; margin-bottom:3rem; }
  .rating-number{ font-family:var(--font-display); font-size:3.4rem; color:var(--copper-bright); }
  .rating-sub{ color:var(--taupe); font-size:0.9rem; }
  .quotes-grid{ display:grid; grid-template-columns:repeat(2,1fr); gap:1.6rem; max-width:820px; margin:0 auto; }
  .quote-card{ background:var(--bg-elevated-2); border:1px solid var(--border); border-radius:16px; padding:1.6rem; }
  .quote-card p{ font-size:0.98rem; margin-bottom:0.9rem; }
  .quote-name{ font-family:var(--font-mono); font-size:0.78rem; color:var(--taupe); }
  @media (max-width:640px){ .quotes-grid{ grid-template-columns:1fr; } }

  /* ---------- pricing / CTA ---------- */
  .pricing-section{ padding:7rem 0; text-align:center; }
  .pricing-section h2{ font-size:clamp(2rem,4vw,3rem); margin-bottom:1rem; }
  .pricing-section > .container > p{ color:var(--taupe); margin-bottom:2.4rem; }
  .price-tag{ font-family:var(--font-mono); font-size:1.1rem; color:var(--copper-bright); margin-bottom:1.6rem; }
  .price-tag span{ font-size:1.6rem; }
  .fine-print{ margin-top:1.4rem; font-size:0.8rem; color:var(--taupe-dim); }

  /* ---------- footer ---------- */
  footer{ border-top:1px solid var(--border); padding:3.5rem 0 2rem; }
  .footer-inner{ display:flex; justify-content:space-between; flex-wrap:wrap; gap:2.5rem; margin-bottom:2.5rem; }
  .footer-cols{ display:flex; gap:3.5rem; flex-wrap:wrap; }
  .footer-col h4{ font-size:0.78rem; letter-spacing:0.1em; text-transform:uppercase; color:var(--taupe-dim); margin-bottom:0.9rem; font-family:var(--font-mono); font-weight:500; }
  .footer-col a{ display:block; font-size:0.9rem; color:var(--taupe); margin-bottom:0.6rem; }
  .footer-col a:hover{ color:var(--copper-bright); }
  .footer-bottom{ display:flex; justify-content:space-between; flex-wrap:wrap; gap:1rem; padding-top:2rem; border-top:1px solid var(--border); font-size:0.8rem; color:var(--taupe-dim); }

  @media (prefers-reduced-motion: reduce){
    *, *::before, *::after{
      animation-duration:0.01ms !important;
      animation-iteration-count:1 !important;
      transition-duration:0.01ms !important;
      scroll-behavior:auto !important;
    }
  }
</style>
</head>
<body>

<nav id="mainNav">
  <div class="container nav-inner">
    <a href="#" class="logo">PULSE X</a>
    <div class="nav-links">
      <a href="#features">Sound</a>
      <a href="#specs">Specs</a>
      <a href="#colors">Colors</a>
      <a href="#reviews">Reviews</a>
    </div>
    <a href="#pricing" class="btn btn-primary btn-small">Buy — $179</a>
  </div>
</nav>

<section class="hero">
  <div class="hero-glow" aria-hidden="true"></div>
  <div class="hero-content">
    <p class="eyebrow">PULSE X — TRUE WIRELESS</p>
    <h1 class="hero-title">Hear everything.<br>Or <span class="accent">nothing</span> at all.</h1>
    <p class="hero-sub">PULSE X pairs studio-tuned 11mm drivers with adaptive noise cancellation, so you decide exactly how much of the world gets in.</p>
    <div class="hero-actions">
      <a href="#pricing" class="btn btn-primary">Buy PULSE X — $179</a>
      <a href="#features" class="btn btn-ghost">See how it works</a>
    </div>
  </div>
  <div class="hero-eq" id="heroEq" aria-hidden="true"></div>
  <div class="scroll-cue"><span class="scroll-line"></span>Scroll</div>
</section>

<div class="stats-strip">
  <div class="container stats-inner">
    <div class="stat"><div class="stat-value">38 hrs</div><div class="stat-label">Total playback</div></div>
    <div class="stat"><div class="stat-value">-42 dB</div><div class="stat-label">Max noise reduction</div></div>
    <div class="stat"><div class="stat-value">IPX5</div><div class="stat-label">Water resistant</div></div>
    <div class="stat"><div class="stat-value">5.3</div><div class="stat-label">Bluetooth</div></div>
  </div>
</div>

<section class="features" id="features">
  <div class="container">

    <div class="feature-row">
      <div class="feature-visual reveal">
        <div class="rings" aria-hidden="true">
          <div class="ring"></div><div class="ring"></div><div class="ring"></div>
          <div class="ring-core"></div>
        </div>
      </div>
      <div class="feature-text reveal">
        <p class="feature-tag">Silence</p>
        <h3>Turns down the world, not the volume.</h3>
        <p>Three ANC modes track the sound around you in real time — a train platform, an open office, a flight — and cancel it before it reaches your ear. Switch to Transparency and it's gone in an instant, no dial to fumble for.</p>
      </div>
    </div>

    <div class="signal-divider"><span class="signal-dot"></span></div>

    <div class="feature-row reverse">
      <div class="feature-visual reveal">
        <svg class="waveform" viewBox="0 0 280 100" aria-hidden="true">
          <path d="M0,50 Q20,10 40,50 T80,50 T120,50 T160,50 T200,50 T240,50 T280,50" />
        </svg>
      </div>
      <div class="feature-text reveal">
        <p class="feature-tag">Clarity</p>
        <h3>Tuned by ear, not just by spec.</h3>
        <p>An 11mm dynamic driver and Hi-Res certification handle the low end cleanly, without losing detail up top. You hear where an instrument sits in the mix, not just that it's there.</p>
      </div>
    </div>

    <div class="signal-divider"><span class="signal-dot"></span></div>

    <div class="feature-row">
      <div class="feature-visual reveal">
        <div class="battery-shell" aria-hidden="true"><div class="battery-fill"></div></div>
      </div>
      <div class="feature-text reveal">
        <p class="feature-tag">Endurance</p>
        <h3>Doesn't ask you to think about it.</h3>
        <p>Eight hours in the earbuds, thirty more riding in the case — thirty-eight hours before you need a cable. Ten minutes on the charger buys another two hours, so a dead battery is rarely the problem it used to be.</p>
      </div>
    </div>

    <div class="signal-divider"><span class="signal-dot"></span></div>

    <div class="feature-row reverse">
      <div class="feature-visual reveal">
        <div class="earbud-wrap">
          <div class="earbud-shape" id="earbudTilt">
            <div class="body"></div>
            <div class="stem"></div>
            <div class="dot"></div>
          </div>
        </div>
      </div>
      <div class="feature-text reveal">
        <p class="feature-tag">Disappear</p>
        <h3>The best fit is the one you forget.</h3>
        <p>Each earbud weighs 4.5 grams. Four tip sizes ship in the box so you can find the seal that actually holds — through a run, a commute, or a full day at a desk.</p>
      </div>
    </div>

  </div>
</section>

<section class="colors-section reveal" id="colors">
  <div class="container">
    <h2>Choose your finish</h2>
    <p>Four colorways. Same 11mm driver inside every one.</p>
    <div class="color-preview" id="colorPreview"></div>
    <div class="swatch-row" style="margin-top:2.4rem" role="group" aria-label="Color options">
      <button class="swatch" data-color="#C9B48F" data-name="Signature Copper" aria-pressed="true">
        <span class="swatch-color" style="background:#C9B48F"></span>
        <span class="swatch-name">Signature Copper</span>
      </button>
      <button class="swatch" data-color="#211D16" data-name="Midnight Black" aria-pressed="false">
        <span class="swatch-color" style="background:#2B2721"></span>
        <span class="swatch-name">Midnight Black</span>
      </button>
      <button class="swatch" data-color="#EDE6D6" data-name="Warm Ivory" aria-pressed="false">
        <span class="swatch-color" style="background:#EDE6D6"></span>
        <span class="swatch-name">Warm Ivory</span>
      </button>
      <button class="swatch" data-color="#3A4A3C" data-name="Deep Forest" aria-pressed="false">
        <span class="swatch-color" style="background:#3A4A3C"></span>
        <span class="swatch-name">Deep Forest</span>
      </button>
    </div>
  </div>
</section>

<section class="specs-section reveal" id="specs">
  <div class="container">
    <h2>Specifications</h2>
    <div class="specs-grid">
      <div class="spec-row"><span class="spec-label">Driver</span><span class="spec-value">11mm dynamic</span></div>
      <div class="spec-row"><span class="spec-label">Frequency response</span><span class="spec-value">20Hz – 40kHz</span></div>
      <div class="spec-row"><span class="spec-label">ANC depth</span><span class="spec-value">Up to -42dB</span></div>
      <div class="spec-row"><span class="spec-label">Battery, earbuds</span><span class="spec-value">8 hrs (ANC on)</span></div>
      <div class="spec-row"><span class="spec-label">Battery, with case</span><span class="spec-value">38 hrs total</span></div>
      <div class="spec-row"><span class="spec-label">Fast charge</span><span class="spec-value">10 min = 2 hrs</span></div>
      <div class="spec-row"><span class="spec-label">Charging</span><span class="spec-value">USB-C + Qi</span></div>
      <div class="spec-row"><span class="spec-label">Bluetooth</span><span class="spec-value">5.3, multipoint</span></div>
      <div class="spec-row"><span class="spec-label">Water resistance</span><span class="spec-value">IPX5</span></div>
      <div class="spec-row"><span class="spec-label">Weight</span><span class="spec-value">4.5g / earbud</span></div>
      <div class="spec-row"><span class="spec-label">Controls</span><span class="spec-value">Touch + app</span></div>
      <div class="spec-row"><span class="spec-label">Ear tips</span><span class="spec-value">XS / S / M / L</span></div>
    </div>
  </div>
</section>

<section class="reviews-section reveal" id="reviews">
  <div class="container">
    <div class="reviews-top">
      <div class="rating-number">4.8 / 5</div>
      <div class="rating-sub">From 12,400+ orders</div>
    </div>
    <div class="quotes-grid">
      <div class="quote-card">
        <p>"I can't hear my downstairs neighbor's TV anymore. Worth it for that alone."</p>
        <div class="quote-name">— Aanya R., verified buyer</div>
      </div>
      <div class="quote-card">
        <p>"Forgot to charge them for four days straight before the case finally died."</p>
        <div class="quote-name">— Rohan K., verified buyer</div>
      </div>
    </div>
  </div>
</section>

<section class="pricing-section reveal" id="pricing">
  <div class="container">
    <h2>Get PULSE X.</h2>
    <p>Ships free. Thirty days to decide if they're staying.</p>
    <div class="price-tag"><span>$179</span> · one-time</div>
    <a href="#" class="btn btn-primary">Buy Now</a>
    <div class="fine-print">Available in 4 finishes · 2-year warranty</div>
  </div>
</section>

<footer>
  <div class="container">
    <div class="footer-inner">
      <div>
        <div class="logo">PULSE X</div>
      </div>
      <div class="footer-cols">
        <div class="footer-col">
          <h4>Product</h4>
          <a href="#features">Sound</a>
          <a href="#specs">Specs</a>
          <a href="#colors">Colors</a>
        </div>
        <div class="footer-col">
          <h4>Support</h4>
          <a href="#">Contact</a>
          <a href="#">Warranty</a>
          <a href="#">FAQ</a>
        </div>
        <div class="footer-col">
          <h4>Company</h4>
          <a href="#">About</a>
          <a href="#">Press</a>
        </div>
      </div>
    </div>
    <div class="container footer-bottom" style="width:100%; padding-left:0; padding-right:0;">
      <span>© 2026 PULSE X Audio. All rights reserved.</span>
      <span>Designed for how you actually listen.</span>
    </div>
  </div>
</footer>

<script>
  // Build hero equalizer bars
  const eq = document.getElementById('heroEq');
  const barCount = 56;
  for (let i = 0; i < barCount; i++) {
    const bar = document.createElement('div');
    bar.className = 'eq-bar';
    const height = 40 + Math.random() * 220;
    bar.style.height = height + 'px';
    bar.style.animationDuration = (1.1 + Math.random() * 1.4) + 's';
    bar.style.animationDelay = (Math.random() * 2) + 's';
    eq.appendChild(bar);
  }

  // Nav scroll state
  const nav = document.getElementById('mainNav');
  window.addEventListener('scroll', () => {
    nav.classList.toggle('scrolled', window.scrollY > 40);
  }, { passive: true });

  // Scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('in-view');
        io.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });
  revealEls.forEach(el => io.observe(el));

  // Tilt on earbud shape
  const tiltEl = document.getElementById('earbudTilt');
  const tiltWrap = tiltEl.closest('.earbud-wrap');
  tiltWrap.addEventListener('mousemove', (e) => {
    const rect = tiltWrap.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    const rotateX = ((y - rect.height / 2) / rect.height) * -22;
    const rotateY = ((x - rect.width / 2) / rect.width) * 22;
    tiltEl.style.transform = `perspective(900px) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
  });
  tiltWrap.addEventListener('mouseleave', () => {
    tiltEl.style.transform = 'perspective(900px) rotateX(0) rotateY(0)';
  });

  // Color swatches
  const swatches = document.querySelectorAll('.swatch');
  const preview = document.getElementById('colorPreview');
  swatches.forEach(sw => {
    sw.addEventListener('click', () => {
      swatches.forEach(s => s.setAttribute('aria-pressed', 'false'));
      sw.setAttribute('aria-pressed', 'true');
      preview.style.background = sw.dataset.color;
    });
  });
</script>

</body>
</html>

