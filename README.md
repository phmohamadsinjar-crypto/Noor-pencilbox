[Pencil Box.html](https://github.com/user-attachments/files/33737805/Pencil.Box.html)
<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Pencil Box</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Grandstander:wght@600;800&family=Lexend:wght@400;500;600&display=swap">
<style>
/* Layout: an exercise book on squared paper. One playable notebook beside the headline, a centimetre ruler as the grade picker, and a star chart that remembers each child's best scores. Dark theme is a chalkboard. */
:root {
  --paper: #F5F9FF;
  --grid: #DCE6F5;
  --ink: #1B2559;
  --ink-soft: #4B567F;
  --card: #FFFFFF;
  --edge: #1B2559;

  --math: #2F6FEB;  --math-tint: #DCE8FF;  --on-math: #FFFFFF;
  --read: #E5483B;  --read-tint: #FFDDD7;  --on-read: #FFFFFF;
  --sci: #16A06A;   --sci-tint: #CBF0DF;   --on-sci: #FFFFFF;
  --art: #F0A500;   --art-tint: #FFEDB5;   --on-art: #1B2559;

  --good: #0B6B40;  --good-tint: #CBF0DF;
  --bad: #A61E17;   --bad-tint: #FFDDD7;

  --mark: #FFD65C;
  --ruler: #FFD65C;
  --ruler-ink: #1B2559;
  --focus: #2F6FEB;
  --wood: #EBCB9E;
  --eraser: #F28BA0;
  --silver: #AEB7C9;

  --font-display: "Grandstander", "Comic Sans MS", "Trebuchet MS", system-ui, sans-serif;
  --font-body: "Lexend", "Segoe UI", system-ui, -apple-system, sans-serif;
  --r: 14px;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --paper: #14211D;
    --grid: #213730;
    --ink: #F2F6EE;
    --ink-soft: #B6C6BB;
    --card: #1C2E28;
    --edge: #F2F6EE;

    --math: #78A8FF;  --math-tint: #1F3558;  --on-math: #10201A;
    --read: #FF8F83;  --read-tint: #51292A;  --on-read: #10201A;
    --sci: #62D9A5;   --sci-tint: #1B4637;   --on-sci: #10201A;
    --art: #FFD35E;   --art-tint: #4A3E17;   --on-art: #10201A;

    --good: #62D9A5;  --good-tint: #1B4637;
    --bad: #FF9A90;   --bad-tint: #52292B;

    --mark: #7A6420;
    --ruler: #CDAE45;
    --ruler-ink: #14211D;
    --focus: #FFD35E;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --paper: #14211D;
  --grid: #213730;
  --ink: #F2F6EE;
  --ink-soft: #B6C6BB;
  --card: #1C2E28;
  --edge: #F2F6EE;

  --math: #78A8FF;  --math-tint: #1F3558;  --on-math: #10201A;
  --read: #FF8F83;  --read-tint: #51292A;  --on-read: #10201A;
  --sci: #62D9A5;   --sci-tint: #1B4637;   --on-sci: #10201A;
  --art: #FFD35E;   --art-tint: #4A3E17;   --on-art: #10201A;

  --good: #62D9A5;  --good-tint: #1B4637;
  --bad: #FF9A90;   --bad-tint: #52292B;

  --mark: #7A6420;
  --ruler: #CDAE45;
  --ruler-ink: #14211D;
  --focus: #FFD35E;
  color-scheme: dark;
}

html { font-size: 100%; }
* { box-sizing: border-box; }
body {
  background-color: var(--paper);
  background-image:
    linear-gradient(var(--grid) 1px, transparent 1px),
    linear-gradient(90deg, var(--grid) 1px, transparent 1px);
  background-size: 28px 28px;
  color: var(--ink);
  font-family: var(--font-body);
  font-size: 1.0625rem;
  line-height: 1.6;
  padding-block: 0;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
}
.wrap { max-width: 1120px; margin-inline: auto; }
h1, h2, h3, h4, p { margin: 0; }
h1, h2, h3 { font-family: var(--font-display); font-weight: 800; text-wrap: balance; }
a { color: inherit; }
button { font: inherit; color: inherit; }
:focus-visible { outline: 3px solid var(--focus); outline-offset: 3px; }
svg { display: block; }

.s-math { --s: var(--math); --s-tint: var(--math-tint); --on-s: var(--on-math); }
.s-read { --s: var(--read); --s-tint: var(--read-tint); --on-s: var(--on-read); }
.s-sci  { --s: var(--sci);  --s-tint: var(--sci-tint);  --on-s: var(--on-sci); }
.s-art  { --s: var(--art);  --s-tint: var(--art-tint);  --on-s: var(--on-art); }

/* ---------- Header ---------- */
.top { display: flex; align-items: center; flex-wrap: wrap; gap: 12px 24px; padding-block: 18px; }
.brand { display: flex; align-items: center; gap: 10px; font: 800 1.5rem/1 var(--font-display); text-decoration: none; }
.top nav { display: flex; flex-wrap: wrap; gap: 4px 22px; margin-left: auto; }
.top nav a { text-decoration: none; font-weight: 500; padding: 8px 2px; border-bottom: 2px solid transparent; }
.top nav a:hover { border-bottom-color: var(--edge); }
.pill {
  display: inline-flex; align-items: center; gap: 8px; min-height: 40px; padding: 0 14px;
  border: 2px solid var(--edge); border-radius: 999px; background: var(--card);
  font: 600 .95rem var(--font-body); text-decoration: none;
  font-variant-numeric: tabular-nums;
}
.pill svg { width: 20px; height: 20px; }
@media (max-width: 640px) {
  .top nav { order: 3; flex-basis: 100%; margin-left: 0; }
  .pill { margin-left: auto; }
}

/* ---------- Stars ---------- */
.star { fill: var(--s, var(--art)); stroke: var(--edge); stroke-linejoin: round; stroke-width: 1.6; }
.star.off { fill: transparent; stroke: var(--ink-soft); stroke-width: 1.4; }

/* ---------- Buttons ---------- */
.btn {
  display: inline-flex; align-items: center; justify-content: center; gap: 8px;
  min-height: 48px; padding: 0 22px; border: 2px solid var(--edge); border-radius: 999px;
  background: var(--card); color: var(--ink); font: 600 1rem/1 var(--font-body);
  text-decoration: none; cursor: pointer; transition: transform .12s, box-shadow .12s;
}
.btn:hover { transform: translate(-2px, -2px); box-shadow: 3px 3px 0 var(--edge); }
.btn:active { transform: none; box-shadow: none; }
.btn.primary { background: var(--ink); color: var(--paper); }

/* ---------- Hero ---------- */
.hero {
  display: grid; grid-template-columns: minmax(0, 1.05fr) minmax(0, .95fr);
  gap: clamp(32px, 5vw, 72px); align-items: center;
  padding-block: clamp(48px, 7vw, 88px) clamp(40px, 6vw, 72px);
}
.eyebrow { font: 600 .8rem/1.3 var(--font-body); letter-spacing: .12em; text-transform: uppercase; color: var(--ink-soft); }
.hero h1 { font-size: clamp(2.6rem, 7.2vw, 4.6rem); line-height: 1.02; letter-spacing: -.01em; margin-top: 14px; }
.mark { background: linear-gradient(transparent 58%, var(--mark) 58% 92%, transparent 92%); padding: 0 .08em; -webkit-box-decoration-break: clone; box-decoration-break: clone; }
.lede { font-size: 1.2rem; color: var(--ink-soft); max-width: 46ch; margin-top: 20px; }
.cta { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 28px; }
.fine { margin-top: 18px; font-size: .9rem; color: var(--ink-soft); }
@media (max-width: 900px) { .hero { grid-template-columns: minmax(0, 1fr); } .pencil { display: none; } }

/* ---------- Notebook (the lesson) ---------- */
.nb-wrap { position: relative; }
.pencil { position: absolute; top: -32px; right: 10px; width: 210px; height: auto; transform: rotate(-9deg); z-index: 2; pointer-events: none; }
.notebook {
  position: relative; background: var(--card); border: 2px solid var(--edge); border-radius: var(--r);
  box-shadow: 6px 6px 0 var(--edge); padding: 22px 22px 26px 56px; min-width: 0;
}
.notebook::before {
  content: ""; position: absolute; left: 14px; top: 18px; bottom: 18px; width: 20px;
  background-image: radial-gradient(circle, var(--paper) 0 5px, var(--edge) 5.5px 7px, transparent 7.5px);
  background-size: 20px 34px; background-repeat: repeat-y;
}
@media (max-width: 480px) {
  .notebook { padding: 18px 16px 22px 46px; box-shadow: 4px 4px 0 var(--edge); }
  .notebook::before { left: 10px; }
}
.nb-date { font: 600 .75rem/1.3 var(--font-body); letter-spacing: .12em; text-transform: uppercase; color: var(--ink-soft); }
.chips { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 12px; }
.chip {
  display: inline-flex; align-items: center; gap: 8px; min-height: 44px; padding: 0 14px;
  border: 2px solid var(--edge); border-radius: 999px; background: var(--card); cursor: pointer;
  font: 500 .95rem var(--font-body);
}
.chip i { width: 12px; height: 12px; border-radius: 50%; background: var(--s); border: 2px solid var(--edge); }
.chip[aria-pressed="true"] { background: var(--s-tint); font-weight: 600; }
.chip:hover { background: var(--s-tint); }

.quiz { min-height: 392px; margin-top: 20px; }
.progress { display: flex; align-items: center; justify-content: space-between; gap: 12px; font-size: .9rem; color: var(--ink-soft); }
.dots { display: flex; gap: 6px; }
.dot { width: 12px; height: 12px; border-radius: 50%; border: 2px solid var(--edge); }
.dot.done { background: var(--ink); }
.dot.now { background: var(--s); }
.q { font: 800 clamp(1.5rem, 4vw, 2rem)/1.2 var(--font-display); margin-top: 16px; text-wrap: balance; }
.q:focus { outline: none; }
.opts { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 12px; margin-top: 20px; }
@media (max-width: 520px) { .opts { grid-template-columns: minmax(0, 1fr); } }
.opt {
  position: relative; display: flex; align-items: center; gap: 12px; min-height: 60px; padding: 10px 14px;
  background: var(--card); color: var(--ink); border: 2px solid var(--edge); border-radius: 12px;
  font: 500 1.125rem/1.25 var(--font-body); text-align: left; cursor: pointer;
  transition: transform .12s, box-shadow .12s, background .12s;
}
.opt .key {
  flex: none; display: grid; place-items: center; width: 32px; height: 32px; border-radius: 50%;
  border: 2px solid var(--edge); font: 600 .85rem var(--font-body);
}
.opt .label { flex: 1; min-width: 0; overflow-wrap: anywhere; }
.opt .tag { flex: none; font: 600 .8rem var(--font-body); }
.opt:hover:not(.locked) { transform: translate(-2px, -2px); box-shadow: 3px 3px 0 var(--edge); background: var(--s-tint); }
.opt:active:not(.locked) { transform: none; box-shadow: none; }
.opt.locked { cursor: default; }
.opt.locked:not(.correct):not(.wrong) { opacity: .6; }
.opt.correct { background: var(--good-tint); border-color: var(--good); }
.opt.correct .tag { color: var(--good); }
.opt.wrong { background: var(--bad-tint); border-color: var(--bad); }
.opt.wrong .tag { color: var(--bad); }
.fb { margin-top: 16px; border-radius: 12px; padding: 0; min-height: 0; }
.fb.show { padding: 12px 16px; }
.fb.is-good { background: var(--good-tint); }
.fb.is-bad { background: var(--bad-tint); }
.fb strong { font-family: var(--font-display); font-weight: 800; font-size: 1.15rem; margin-right: 6px; }
.fb.is-good strong { color: var(--good); }
.fb.is-bad strong { color: var(--bad); }
.next-row { display: flex; justify-content: flex-end; margin-top: 16px; min-height: 48px; }

.result { text-align: left; }
.result .stars-big { display: flex; gap: 8px; margin-top: 8px; }
.result .stars-big svg { width: 48px; height: 48px; }
.result .stars-big .star:not(.off) { animation: pop .5s ease-out both; animation-delay: var(--d, 0s); transform-origin: center; transform-box: fill-box; }
@keyframes pop { 0% { transform: scale(.4) rotate(-20deg); } 60% { transform: scale(1.2); } 100% { transform: none; } }
.result h3 { font-size: clamp(1.8rem, 5vw, 2.4rem); line-height: 1.1; margin-top: 16px; }
.result p { margin-top: 10px; color: var(--ink-soft); max-width: 40ch; }
.result .cta { margin-top: 22px; }

/* ---------- Sections ---------- */
.section { padding-block: clamp(48px, 8vw, 96px); }
.section h2 { font-size: clamp(1.9rem, 4.6vw, 2.9rem); line-height: 1.1; }
.section .intro { color: var(--ink-soft); max-width: 56ch; margin-top: 14px; }

/* Subjects */
.subjects { display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 18px; margin-top: 36px; }
@media (max-width: 1000px) { .subjects { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
@media (max-width: 560px) { .subjects { grid-template-columns: minmax(0, 1fr); } }
.subject {
  display: flex; flex-direction: column; gap: 14px; min-width: 0; padding: 22px;
  background: var(--s-tint); border: 2px solid var(--edge); border-radius: var(--r);
  transition: transform .12s, box-shadow .12s;
}
.subject:hover { transform: translate(-3px, -3px); box-shadow: 5px 5px 0 var(--edge); }
.s-icon { display: grid; place-items: center; width: 56px; height: 56px; border-radius: 50%; background: var(--s); color: var(--on-s); border: 2px solid var(--edge); }
.s-icon svg { width: 32px; height: 32px; fill: none; stroke: currentColor; stroke-width: 2.5; stroke-linecap: round; stroke-linejoin: round; }
.subject h3 { font-size: 1.6rem; line-height: 1.1; }
.subject p { font-size: .98rem; }
.topics { list-style: none; margin: 0; padding: 0; display: flex; flex-wrap: wrap; gap: 6px; }
.topics li { font-size: .82rem; line-height: 1.2; padding: 4px 10px; border-radius: 999px; background: var(--card); border: 1.5px solid var(--edge); }
.subject .btn { margin-top: auto; min-height: 44px; font-size: .95rem; }

/* Grades ruler */
.ruler {
  position: relative; display: grid; grid-template-columns: repeat(6, minmax(0, 1fr)); gap: 4px;
  margin-top: 36px; padding: 12px 8px 40px; background: var(--ruler); color: var(--ruler-ink);
  border: 2px solid var(--edge); border-radius: 8px;
}
.ruler::after {
  content: ""; position: absolute; left: 0; right: 0; bottom: 0; height: 24px; pointer-events: none;
  background-image:
    linear-gradient(90deg, var(--ruler-ink) 1px, transparent 1px),
    linear-gradient(90deg, var(--ruler-ink) 1.5px, transparent 1.5px);
  background-size: 8px 10px, 80px 22px;
  background-repeat: repeat-x, repeat-x;
  background-position: left bottom, left bottom;
}
.grade {
  display: flex; flex-direction: column; align-items: center; justify-content: center; min-height: 72px;
  background: transparent; border: 2px solid transparent; border-radius: 10px; cursor: pointer; color: var(--ruler-ink);
  font-family: var(--font-body);
}
.grade:hover { border-color: var(--ruler-ink); }
.grade .gl { font: 600 .68rem/1 var(--font-body); letter-spacing: .1em; text-transform: uppercase; }
.grade .gn { font: 800 2.1rem/1.1 var(--font-display); }
.grade[aria-pressed="true"] { background: var(--ink); color: var(--paper); border-color: var(--ink); }
@media (max-width: 420px) { .grade .gl { font-size: .6rem; letter-spacing: .04em; } }

.gp { margin-top: 24px; background: var(--card); border: 2px solid var(--edge); border-radius: var(--r); padding: clamp(18px, 3vw, 28px); }
.gp-head { display: flex; flex-wrap: wrap; align-items: baseline; gap: 4px 16px; }
.gp-head h3 { font-size: 1.8rem; }
.gp-head p { color: var(--ink-soft); }
.gp-cols { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 22px; margin-top: 18px; }
@media (max-width: 700px) { .gp-cols { grid-template-columns: minmax(0, 1fr); } }
.gp-col { border-top: 4px solid var(--s); padding-top: 12px; min-width: 0; }
.gp-col h4 { font: 600 .8rem/1.3 var(--font-body); letter-spacing: .12em; text-transform: uppercase; color: var(--ink-soft); }
.gp-col ul { list-style: none; margin: 10px 0 0; padding: 0; display: grid; gap: 8px; }
.gp-col li { position: relative; padding-left: 20px; }
.gp-col li::before { content: ""; position: absolute; left: 0; top: .55em; width: 10px; height: 10px; border-radius: 2px; background: var(--s); border: 1.5px solid var(--edge); }
.note { margin-top: 14px; font-size: .88rem; color: var(--ink-soft); }

/* Star chart */
.chart { display: grid; grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr); gap: 20px; margin-top: 36px; align-items: stretch; }
@media (max-width: 760px) { .chart { grid-template-columns: minmax(0, 1fr); } }
.rows { list-style: none; margin: 0; padding: 8px 22px; background: var(--card); border: 2px solid var(--edge); border-radius: var(--r); }
.row { display: grid; grid-template-columns: 92px minmax(0, 1fr) auto; align-items: center; gap: 12px; padding: 14px 0; border-bottom: 1.5px dashed var(--ink-soft); }
.row:last-child { border-bottom: 0; }
.r-name { font: 800 1.15rem/1.1 var(--font-display); }
.r-stars { display: flex; gap: 4px; }
.r-stars svg { width: 26px; height: 26px; }
.r-num { font-variant-numeric: tabular-nums; color: var(--ink-soft); font-size: .92rem; }
@media (max-width: 420px) { .row { grid-template-columns: 74px minmax(0, 1fr) auto; } .r-stars svg { width: 22px; height: 22px; } .rows { padding-inline: 16px; } }
.total { display: flex; flex-direction: column; justify-content: center; gap: 6px; padding: 24px; background: var(--art-tint); border: 2px solid var(--edge); border-radius: var(--r); }
.total .big { font: 800 clamp(4rem, 12vw, 6rem)/1 var(--font-display); font-variant-numeric: tabular-nums; }
.total .of { color: var(--ink-soft); }
.total .btn { margin-top: 14px; align-self: flex-start; min-height: 44px; font-size: .92rem; }

/* Grown-ups */
.trio { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 28px; margin-top: 32px; }
@media (max-width: 760px) { .trio { grid-template-columns: minmax(0, 1fr); gap: 22px; } }
.trio > div { border-top: 2px solid var(--edge); padding-top: 14px; }
.trio h3 { font-size: 1.35rem; line-height: 1.2; }
.trio p { margin-top: 8px; color: var(--ink-soft); }

.foot { padding-block: 32px 56px; border-top: 2px solid var(--edge); color: var(--ink-soft); font-size: .9rem; }
.foot p + p { margin-top: 6px; }
.foot .credit { font-size: 1.05rem; color: var(--ink); }
.foot .credit strong { font-family: var(--font-display); font-weight: 800; }

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { animation: none !important; transition: none !important; }
}
</style>

<svg width="0" height="0" style="position:absolute" aria-hidden="true" focusable="false">
  <symbol id="star" viewBox="0 0 24 24"><path d="M12 2.5l2.9 6.2 6.8.8-5 4.7 1.3 6.7L12 17.5 6 20.9l1.3-6.7-5-4.7 6.8-.8z"/></symbol>
</svg>

<div id="top"></div>
<header class="top wrap">
  <a class="brand" href="#top" aria-label="Pencil Box home">
    <svg width="30" height="30" viewBox="0 0 32 32" aria-hidden="true">
      <path d="M5 27l2.2-7.6L21.6 5a2.6 2.6 0 013.7 0l1.7 1.7a2.6 2.6 0 010 3.7L12.6 24.8z" fill="var(--mark)" stroke="var(--edge)" stroke-width="2" stroke-linejoin="round"/>
      <path d="M5 27l2.2-7.6 5.4 5.4z" fill="var(--wood)" stroke="var(--edge)" stroke-width="2" stroke-linejoin="round"/>
    </svg>
    Pencil Box
  </a>
  <nav aria-label="Main">
    <a href="#lesson">Lesson</a>
    <a href="#subjects">Subjects</a>
    <a href="#grades">Grades</a>
    <a href="#stars">Star chart</a>
  </nav>
  <a class="pill" href="#stars" aria-label="Your stars">
    <svg viewBox="0 0 24 24" aria-hidden="true"><use href="#star" class="star"/></svg>
    <span><span id="starTotal">0</span> / 20</span>
  </a>
</header>

<main>
  <section class="hero wrap">
    <div>
      <p class="eyebrow">Primary school · Grades 1 to 6</p>
      <h1>Five-minute lessons for <span class="mark">curious</span> kids.</h1>
      <p class="lede">Maths, reading, science and art for ages 6 to 12. Pick a subject, answer five questions and collect stars.</p>
      <div class="cta">
        <a class="btn primary" href="#lesson">Try a lesson</a>
        <a class="btn" href="#grades">See the grades</a>
      </div>
      <p class="fine">No sign-up. Your stars stay on this device.</p>
    </div>

    <div class="nb-wrap">
      <svg class="pencil" viewBox="0 0 220 30" aria-hidden="true">
        <g stroke="var(--edge)" stroke-width="2" stroke-linejoin="round">
          <rect x="1" y="3" width="22" height="24" rx="5" fill="var(--eraser)"/>
          <rect x="23" y="3" width="20" height="24" fill="var(--silver)"/>
          <path d="M29 3v24M36 3v24" fill="none"/>
          <rect x="43" y="3" width="130" height="24" fill="var(--art)"/>
          <path d="M173 3L208 15 173 27z" fill="var(--wood)"/>
          <path d="M199 12l9 3-9 3z" fill="var(--ink)"/>
        </g>
      </svg>
      <div class="notebook s-math" id="lesson">
        <p class="nb-date" id="today">Today’s lesson</p>
        <div class="chips" role="group" aria-label="Choose a subject">
          <button type="button" class="chip s-math" data-subj="math" aria-pressed="true"><i></i>Maths</button>
          <button type="button" class="chip s-read" data-subj="read" aria-pressed="false"><i></i>Reading</button>
          <button type="button" class="chip s-sci" data-subj="sci" aria-pressed="false"><i></i>Science</button>
          <button type="button" class="chip s-art" data-subj="art" aria-pressed="false"><i></i>Art</button>
        </div>
        <div class="quiz" id="quiz"></div>
      </div>
    </div>
  </section>

  <section class="section wrap" id="subjects">
    <h2>Choose a subject</h2>
    <p class="intro">Every subject has short lessons that build on each other. Start anywhere.</p>
    <div class="subjects">
      <article class="subject s-math">
        <div class="s-icon"><svg viewBox="0 0 32 32" aria-hidden="true"><path d="M16 7v18M7 16h18"/></svg></div>
        <h3>Maths</h3>
        <p>Count, add, share and measure with real things.</p>
        <ul class="topics"><li>Counting</li><li>Add and subtract</li><li>Times tables</li><li>Shapes</li><li>Measuring</li><li>Fractions</li></ul>
        <button type="button" class="btn" data-go="math">Try maths</button>
      </article>
      <article class="subject s-read">
        <div class="s-icon"><svg viewBox="0 0 32 32" aria-hidden="true"><text x="16" y="23" text-anchor="middle" font-family="Grandstander, sans-serif" font-weight="800" font-size="17" fill="currentColor" stroke="none">Aa</text></svg></div>
        <h3>Reading</h3>
        <p>Sounds, words and sentences, then whole stories.</p>
        <ul class="topics"><li>Letter sounds</li><li>Rhymes</li><li>Sentences</li><li>Word meanings</li><li>Stories</li></ul>
        <button type="button" class="btn" data-go="read">Try reading</button>
      </article>
      <article class="subject s-sci">
        <div class="s-icon"><svg viewBox="0 0 32 32" aria-hidden="true"><path d="M7 25C7 14 13 8 25 7c0 12-6 18-16 18zM7 25l10-10"/></svg></div>
        <h3>Science</h3>
        <p>Ask why, look closely and find out how things work.</p>
        <ul class="topics"><li>Living things</li><li>Plants</li><li>Materials</li><li>Earth and space</li><li>Weather</li></ul>
        <button type="button" class="btn" data-go="sci">Try science</button>
      </article>
      <article class="subject s-art">
        <div class="s-icon"><svg viewBox="0 0 32 32" aria-hidden="true"><circle cx="12" cy="13" r="6"/><circle cx="20" cy="13" r="6"/><circle cx="16" cy="20" r="6"/></svg></div>
        <h3>Art</h3>
        <p>Mix colours, spot shapes and make patterns.</p>
        <ul class="topics"><li>Colour mixing</li><li>Shapes</li><li>Drawing</li><li>Patterns</li></ul>
        <button type="button" class="btn" data-go="art">Try art</button>
      </article>
    </div>
  </section>

  <section class="section wrap" id="grades">
    <h2>Find your grade</h2>
    <p class="intro">Lessons follow six grades, from counting to 100 up to angles and electric circuits. Tap a grade on the ruler.</p>
    <div class="ruler" id="ruler" role="group" aria-label="Choose a grade">
      <button type="button" class="grade" data-g="1" aria-pressed="false"><span class="gl">Grade</span><span class="gn">1</span></button>
      <button type="button" class="grade" data-g="2" aria-pressed="false"><span class="gl">Grade</span><span class="gn">2</span></button>
      <button type="button" class="grade" data-g="3" aria-pressed="true"><span class="gl">Grade</span><span class="gn">3</span></button>
      <button type="button" class="grade" data-g="4" aria-pressed="false"><span class="gl">Grade</span><span class="gn">4</span></button>
      <button type="button" class="grade" data-g="5" aria-pressed="false"><span class="gl">Grade</span><span class="gn">5</span></button>
      <button type="button" class="grade" data-g="6" aria-pressed="false"><span class="gl">Grade</span><span class="gn">6</span></button>
    </div>
    <div class="gp" id="gradePanel" aria-live="polite"></div>
    <p class="note">Sample outline. Swap in your national curriculum before launch.</p>
  </section>

  <section class="section wrap" id="stars">
    <h2>Your star chart</h2>
    <p class="intro">Each lesson can earn up to five stars. The chart keeps your best score for every subject.</p>
    <div class="chart">
      <ul class="rows" id="rows"></ul>
      <div class="total">
        <p class="eyebrow">Stars collected</p>
        <p class="big" id="bigTotal">0</p>
        <p class="of">out of 20</p>
        <button type="button" class="btn" id="clearBtn">Clear my stars</button>
      </div>
    </div>
  </section>

  <section class="section wrap" id="grownups">
    <h2>For teachers and parents</h2>
    <div class="trio">
      <div>
        <h3>Short on purpose</h3>
        <p>A lesson is five questions and takes about five minutes, so children finish what they start.</p>
      </div>
      <div>
        <h3>Easy on the eyes</h3>
        <p>The text face, Lexend, was designed to make reading easier. Buttons are big enough for small fingers.</p>
      </div>
      <div>
        <h3>Nothing to sign up for</h3>
        <p>Stars are saved in the browser on the device. There are no accounts, no ads and no personal details.</p>
      </div>
    </div>
  </section>
</main>

<footer class="foot wrap">
  <p class="credit">Designed by <strong>Noor Mohammed Sinjar</strong></p>
  <p>Pencil Box is a design prototype for primary school learning. Questions and grade outlines are samples.</p>
</footer>

<script>
(function () {
  'use strict';

  var KEY = 'pencilbox.stars.v1';
  var ORDER = ['math', 'read', 'sci', 'art'];

  var DATA = {
    math: { name: 'Maths', qs: [
      { q: '7 + 5 = ?', a: ['11', '12', '13', '14'], c: 1, why: '7 + 3 makes 10, then 2 more makes 12.' },
      { q: '6 × 4 = ?', a: ['20', '24', '28', '26'], c: 1, why: 'Count four sixes: 6, 12, 18, 24.' },
      { q: 'Which number is the biggest?', a: ['408', '480', '84', '804'], c: 3, why: '804 has 8 hundreds. The others have fewer.' },
      { q: 'A ruler shows 15 cm. How many millimetres is that?', a: ['15 mm', '105 mm', '150 mm', '1,500 mm'], c: 2, why: '1 cm is 10 mm, so 15 cm is 150 mm.' },
      { q: 'What is half of 18?', a: ['8', '9', '10', '6'], c: 1, why: 'Share 18 into two equal groups and each group has 9.' }
    ] },
    read: { name: 'Reading', qs: [
      { q: 'Which word rhymes with “cake”?', a: ['lake', 'cook', 'kick', 'cap'], c: 0, why: 'Cake and lake both end with the sound -ake.' },
      { q: 'Which word means the opposite of “huge”?', a: ['tiny', 'giant', 'tall', 'loud'], c: 0, why: 'Huge means very big. Tiny means very small.' },
      { q: 'Which sentence is written correctly?', a: ['the dog ran fast', 'The dog ran fast.', 'the dog ran fast.', 'The dog ran fast'], c: 1, why: 'It starts with a capital letter and ends with a full stop.' },
      { q: 'How many syllables are in “butterfly”?', a: ['1', '2', '3', '4'], c: 2, why: 'Clap it out: but-ter-fly. That is 3 claps.' },
      { q: 'Which of these words is a noun?', a: ['run', 'quickly', 'river', 'blue'], c: 2, why: 'A noun names a thing or a place. A river is a thing.' }
    ] },
    sci: { name: 'Science', qs: [
      { q: 'Which one is a living thing?', a: ['rock', 'tree', 'water', 'chair'], c: 1, why: 'A tree grows, needs water and makes seeds.' },
      { q: 'What do plants need to grow?', a: ['Light, water and air', 'Sand and plastic', 'Darkness only', 'Milk and sugar'], c: 0, why: 'Plants use light, water and air to make their own food.' },
      { q: 'Which planet do we live on?', a: ['Mars', 'Earth', 'Venus', 'Jupiter'], c: 1, why: 'We live on Earth, the third planet from the Sun.' },
      { q: 'When ice melts, what does it turn into?', a: ['steam', 'water', 'rock', 'sand'], c: 1, why: 'Heat turns solid ice into liquid water.' },
      { q: 'How many legs does an insect have?', a: ['4', '6', '8', '10'], c: 1, why: 'All insects have 6 legs. Spiders have 8, so they are not insects.' }
    ] },
    art: { name: 'Art', qs: [
      { q: 'Mix blue and yellow paint. Which colour do you get?', a: ['green', 'orange', 'purple', 'pink'], c: 0, why: 'Blue and yellow make green.' },
      { q: 'Which are the three primary colours?', a: ['Red, yellow, blue', 'Green, orange, purple', 'Black, white, grey', 'Pink, brown, red'], c: 0, why: 'Primary colours can not be mixed from other paints. All other colours come from them.' },
      { q: 'Which of these is a warm colour?', a: ['blue', 'red', 'grey', 'green'], c: 1, why: 'Red feels like fire and sunshine, so it is a warm colour.' },
      { q: 'Which shape has exactly 3 sides?', a: ['circle', 'square', 'triangle', 'oval'], c: 2, why: 'Tri means three. A triangle has 3 sides and 3 corners.' },
      { q: 'Mix red with white. Which colour do you get?', a: ['pink', 'brown', 'grey', 'green'], c: 0, why: 'White makes any colour lighter. Red and white make pink.' }
    ] }
  };

  var GRADES = {
    1: { age: '6 to 7',   math: ['Counting to 100', 'Adding within 20', 'Shapes around us'],        read: ['Letter sounds', 'Reading short words', 'Writing your name'],        sci: ['Our five senses', 'Pets and farm animals', 'Day and night'] },
    2: { age: '7 to 8',   math: ['Tens and ones', 'Adding and subtracting to 100', 'Telling the time'], read: ['Rhymes and blends', 'Simple sentences', 'Short stories'],            sci: ['Plants and seeds', 'Hot and cold', 'Water around us'] },
    3: { age: '8 to 9',   math: ['Times tables 2, 5 and 10', 'Measuring in cm and m', 'Simple fractions'], read: ['Syllables', 'Nouns and verbs', 'Story characters'],               sci: ['Living and non-living', 'Animal homes', 'Materials and their uses'] },
    4: { age: '9 to 10',  math: ['Times tables to 12', 'Perimeter', 'Fractions and decimals'],         read: ['Paragraphs', 'Adjectives', 'Finding the main idea'],                sci: ['Food chains', 'Solids, liquids and gases', 'Sound and light'] },
    5: { age: '10 to 11', math: ['Long multiplication', 'Area', 'Equivalent fractions'],               read: ['Prefixes and suffixes', 'Reading between the lines', 'Writing a report'], sci: ['The solar system', 'The water cycle', 'Forces and motion'] },
    6: { age: '11 to 12', math: ['Ratio and averages', 'Angles', 'Negative numbers'],                  read: ['Persuasive writing', 'Comparing texts', 'Research skills'],         sci: ['The human body', 'Electric circuits', 'Ecosystems'] }
  };

  var best = { math: 0, read: 0, sci: 0, art: 0 };
  try {
    var raw = localStorage.getItem(KEY);
    if (raw) {
      var saved = JSON.parse(raw);
      ORDER.forEach(function (k) {
        var v = Number(saved && saved[k]);
        if (v >= 0 && v <= 5) best[k] = Math.floor(v);
      });
    }
  } catch (e) {}
  function persist() { try { localStorage.setItem(KEY, JSON.stringify(best)); } catch (e) {} }

  var $ = function (id) { return document.getElementById(id); };
  var quiz = $('quiz'), notebook = $('lesson');
  var st = { s: 'math', i: 0, score: 0, answered: false, opts: [], done: false };
  var reduce = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  function shuffle(arr) {
    for (var i = arr.length - 1; i > 0; i--) {
      var j = Math.floor(Math.random() * (i + 1));
      var t = arr[i]; arr[i] = arr[j]; arr[j] = t;
    }
    return arr;
  }
  function buildOpts() {
    var q = DATA[st.s].qs[st.i];
    st.opts = shuffle(q.a.map(function (t, idx) { return { t: t, ok: idx === q.c }; }));
  }
  function starSvg(on, extra) {
    return '<svg viewBox="0 0 24 24" aria-hidden="true"' + (extra || '') + '><use href="#star" class="star' + (on ? '' : ' off') + '"/></svg>';
  }

  function startRun(s) {
    st.s = s; st.i = 0; st.score = 0; st.answered = false; st.done = false;
    buildOpts();
    notebook.className = 'notebook s-' + s;
    Array.prototype.forEach.call(document.querySelectorAll('.chip'), function (c) {
      c.setAttribute('aria-pressed', c.getAttribute('data-subj') === s ? 'true' : 'false');
    });
    render();
  }

  function render() { st.done ? renderResult() : renderQuestion(); }

  function renderQuestion() {
    var q = DATA[st.s].qs[st.i];
    var dots = '';
    for (var d = 0; d < 5; d++) dots += '<span class="dot' + (d < st.i ? ' done' : d === st.i ? ' now' : '') + '"></span>';
    var keys = ['A', 'B', 'C', 'D'];
    var btns = st.opts.map(function (o, idx) {
      return '<button type="button" class="opt" data-i="' + idx + '"><span class="key">' + keys[idx] + '</span><span class="label">' + o.t + '</span><span class="tag"></span></button>';
    }).join('');
    quiz.innerHTML =
      '<div class="progress"><span>Question ' + (st.i + 1) + ' of 5</span><span class="dots" aria-hidden="true">' + dots + '</span></div>' +
      '<p class="q" id="qtext" tabindex="-1">' + q.q + '</p>' +
      '<div class="opts" role="group" aria-labelledby="qtext">' + btns + '</div>' +
      '<div class="fb" id="fb" aria-live="polite"></div>' +
      '<div class="next-row" id="nextRow"></div>';
  }

  function answer(idx) {
    if (st.answered) return;
    st.answered = true;
    var q = DATA[st.s].qs[st.i];
    var ok = st.opts[idx].ok;
    if (ok) st.score++;
    var btns = quiz.querySelectorAll('.opt');
    Array.prototype.forEach.call(btns, function (b, j) {
      b.classList.add('locked');
      var tag = b.querySelector('.tag');
      if (st.opts[j].ok) { b.classList.add('correct'); tag.textContent = 'Correct'; }
      else if (j === idx) { b.classList.add('wrong'); tag.textContent = 'Not quite'; }
    });
    var fb = $('fb');
    fb.className = 'fb show ' + (ok ? 'is-good' : 'is-bad');
    fb.innerHTML = '<strong>' + (ok ? 'Correct!' : 'Not quite.') + '</strong>' + q.why;
    $('nextRow').innerHTML = '<button type="button" class="btn primary" data-act="next">' + (st.i < 4 ? 'Next question' : 'See my stars') + '</button>';
  }

  function next() {
    if (st.i < 4) {
      st.i++; st.answered = false; buildOpts(); renderQuestion();
      var qt = $('qtext'); if (qt) qt.focus({ preventScroll: true });
    } else {
      st.done = true;
      if (st.score > best[st.s]) { best[st.s] = st.score; persist(); }
      updateStars();
      renderResult();
    }
  }

  function renderResult() {
    var sc = st.score;
    var heads = ['Keep going!', 'Keep going!', 'Nice try!', 'Good job!', 'Great work!', 'Perfect score!'];
    var stars = '';
    for (var k = 0; k < 5; k++) stars += starSvg(k < sc, ' style="--d:' + (k * 0.12).toFixed(2) + 's"');
    var nextKey = ORDER[(ORDER.indexOf(st.s) + 1) % ORDER.length];
    quiz.innerHTML =
      '<div class="result"><p class="eyebrow">' + DATA[st.s].name + ' lesson finished</p>' +
      '<div class="stars-big" role="img" aria-label="' + sc + ' of 5 stars">' + stars + '</div>' +
      '<h3>' + heads[sc] + '</h3>' +
      '<p>You got ' + sc + ' of 5 right. Your best in ' + DATA[st.s].name + ' is ' + best[st.s] + ' of 5.</p>' +
      '<div class="cta"><button type="button" class="btn primary" data-act="again">Play again</button>' +
      '<button type="button" class="btn" data-act="other" data-to="' + nextKey + '">Try ' + DATA[nextKey].name + '</button></div></div>';
  }

  function updateStars() {
    var total = 0;
    ORDER.forEach(function (k) { total += best[k]; });
    $('starTotal').textContent = total;
    $('bigTotal').textContent = total;
    $('rows').innerHTML = ORDER.map(function (k) {
      var s = '';
      for (var n = 0; n < 5; n++) s += starSvg(n < best[k]);
      return '<li class="row s-' + k + '"><span class="r-name">' + DATA[k].name + '</span>' +
        '<span class="r-stars" role="img" aria-label="Best score ' + best[k] + ' of 5">' + s + '</span>' +
        '<span class="r-num">' + best[k] + ' / 5</span></li>';
    }).join('');
  }

  function renderGrade(n) {
    var g = GRADES[n];
    function col(k, label) {
      return '<div class="gp-col s-' + k + '"><h4>' + label + '</h4><ul>' + g[k].map(function (t) { return '<li>' + t + '</li>'; }).join('') + '</ul></div>';
    }
    $('gradePanel').innerHTML =
      '<div class="gp-head"><h3>Grade ' + n + '</h3><p>Ages ' + g.age + '</p></div>' +
      '<div class="gp-cols">' + col('math', 'Maths') + col('read', 'Reading') + col('sci', 'Science') + '</div>';
    Array.prototype.forEach.call(document.querySelectorAll('.grade'), function (b) {
      b.setAttribute('aria-pressed', b.getAttribute('data-g') === String(n) ? 'true' : 'false');
    });
  }

  function goLesson(s) {
    startRun(s);
    notebook.scrollIntoView({ behavior: reduce ? 'auto' : 'smooth', block: 'center' });
  }

  quiz.addEventListener('click', function (e) {
    var opt = e.target.closest('.opt');
    if (opt) { answer(Number(opt.getAttribute('data-i'))); return; }
    var b = e.target.closest('[data-act]');
    if (!b) return;
    var act = b.getAttribute('data-act');
    if (act === 'next') next();
    else if (act === 'again') startRun(st.s);
    else if (act === 'other') startRun(b.getAttribute('data-to'));
  });
  Array.prototype.forEach.call(document.querySelectorAll('.chip'), function (c) {
    c.addEventListener('click', function () { startRun(c.getAttribute('data-subj')); });
  });
  Array.prototype.forEach.call(document.querySelectorAll('[data-go]'), function (b) {
    b.addEventListener('click', function () { goLesson(b.getAttribute('data-go')); });
  });
  Array.prototype.forEach.call(document.querySelectorAll('.grade'), function (b) {
    b.addEventListener('click', function () { renderGrade(Number(b.getAttribute('data-g'))); });
  });

  var clearBtn = $('clearBtn'), clearTimer = null;
  clearBtn.addEventListener('click', function () {
    if (!clearTimer) {
      clearBtn.textContent = 'Tap again to clear';
      clearTimer = setTimeout(function () { clearBtn.textContent = 'Clear my stars'; clearTimer = null; }, 3000);
      return;
    }
    clearTimeout(clearTimer); clearTimer = null;
    clearBtn.textContent = 'Clear my stars';
    ORDER.forEach(function (k) { best[k] = 0; });
    persist(); updateStars();
    if (st.done) renderResult();
  });

  try {
    $('today').textContent = 'Today’s lesson · ' + new Date().toLocaleDateString('en-GB', { weekday: 'long', day: 'numeric', month: 'long' });
  } catch (e) {}

  updateStars();
  renderGrade(3);
  startRun('math');
})();
</script>

</body></html>
