<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shaik Mohammed Owais — Software Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:ital,wght@0,300;0,400;1,300&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg:       #0a0a0a;
    --surface:  #111111;
    --border:   #1e1e1e;
    --muted:    #3a3a3a;
    --text:     #e8e4dc;
    --sub:      #888;
    --accent:   #c8f060;
    --accent2:  #60c8f0;
    --ff-head:  'Syne', sans-serif;
    --ff-serif: 'Instrument Serif', serif;
    --ff-mono:  'DM Mono', monospace;
    --ease:     cubic-bezier(.16,1,.3,1);
  }
  html { scroll-behavior: smooth; }
  body { background:var(--bg);color:var(--text);font-family:var(--ff-head);font-size:16px;line-height:1.6;overflow-x:hidden;cursor:none; }

  #cursor { position:fixed;top:0;left:0;z-index:9999;width:10px;height:10px;background:var(--accent);border-radius:50%;pointer-events:none;transition:transform .15s var(--ease);transform:translate(-50%,-50%); }
  #cursor-ring { position:fixed;top:0;left:0;z-index:9998;width:36px;height:36px;border:1.5px solid rgba(200,240,96,.35);border-radius:50%;pointer-events:none;transition:transform .45s var(--ease),width .3s var(--ease),height .3s var(--ease),border-color .3s;transform:translate(-50%,-50%); }
  body.hovering #cursor { transform:translate(-50%,-50%) scale(2.5); }
  body.hovering #cursor-ring { width:56px;height:56px;border-color:rgba(200,240,96,.6); }
  body::before { content:'';position:fixed;inset:0;z-index:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");opacity:.028;pointer-events:none; }

  nav { position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:1.4rem 3rem;background:rgba(10,10,10,.75);backdrop-filter:blur(20px);border-bottom:1px solid var(--border); }
  .nav-logo { font-size:.85rem;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:var(--accent);font-family:var(--ff-mono); }
  .nav-links { display:flex;gap:2.5rem;list-style:none; }
  .nav-links a { font-size:.82rem;font-weight:600;letter-spacing:.12em;text-transform:uppercase;color:var(--sub);text-decoration:none;position:relative;transition:color .25s; }
  .nav-links a::after { content:'';position:absolute;bottom:-4px;left:0;width:0;height:1px;background:var(--accent);transition:width .3s var(--ease); }
  .nav-links a:hover { color:var(--text); }
  .nav-links a:hover::after { width:100%; }
  .nav-cta { font-size:.8rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:var(--bg);background:var(--accent);padding:.55rem 1.3rem;border:none;border-radius:4px;cursor:pointer;font-family:var(--ff-head);transition:transform .2s var(--ease),box-shadow .2s; }
  .nav-cta:hover { transform:translateY(-2px);box-shadow:0 8px 24px rgba(200,240,96,.3); }

  section { position:relative;z-index:1; }

  /* HERO */
  #hero { min-height:100vh;display:grid;grid-template-rows:1fr auto;padding:10rem 3rem 4rem;overflow:hidden; }
  .hero-grid { display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;max-width:1200px;margin:0 auto;width:100%; }
  .hero-badge { display:inline-flex;align-items:center;gap:.5rem;font-family:var(--ff-mono);font-size:.75rem;color:var(--accent);border:1px solid rgba(200,240,96,.25);padding:.35rem .75rem;border-radius:100px;margin-bottom:1.5rem;animation:fadeUp .8s var(--ease) .1s both; }
  .hero-badge::before { content:'';width:6px;height:6px;border-radius:50%;background:var(--accent);animation:pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1}50%{opacity:.3} }
  .hero-name { font-size:clamp(2.8rem,5.5vw,5rem);font-weight:800;line-height:1.05;letter-spacing:-.03em;animation:fadeUp .8s var(--ease) .2s both; }
  .hero-name em { font-family:var(--ff-serif);font-style:italic;font-weight:400;color:var(--accent); }
  .hero-title { font-size:1rem;color:var(--sub);font-family:var(--ff-mono);font-weight:300;margin:1.2rem 0;animation:fadeUp .8s var(--ease) .3s both; }
  .hero-desc { font-size:.97rem;color:#aaa;line-height:1.8;max-width:420px;animation:fadeUp .8s var(--ease) .4s both; }
  .hero-actions { display:flex;gap:1rem;margin-top:2.5rem;flex-wrap:wrap;animation:fadeUp .8s var(--ease) .5s both; }
  .btn-primary { display:inline-flex;align-items:center;gap:.5rem;background:var(--accent);color:var(--bg);font-family:var(--ff-head);font-size:.85rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;padding:.85rem 2rem;border-radius:6px;text-decoration:none;border:none;cursor:pointer;transition:transform .25s var(--ease),box-shadow .25s; }
  .btn-primary:hover { transform:translateY(-3px);box-shadow:0 12px 32px rgba(200,240,96,.35); }
  .btn-ghost { display:inline-flex;align-items:center;gap:.5rem;background:transparent;color:var(--text);font-family:var(--ff-head);font-size:.85rem;font-weight:600;letter-spacing:.08em;text-transform:uppercase;padding:.85rem 2rem;border-radius:6px;text-decoration:none;border:1px solid var(--border);cursor:pointer;transition:border-color .25s,background .25s; }
  .btn-ghost:hover { border-color:var(--muted);background:var(--surface); }

  .hero-visual { position:relative;animation:fadeUp .8s var(--ease) .3s both; }
  .hero-card { background:var(--surface);border:1px solid var(--border);border-radius:16px;padding:2rem;position:relative;overflow:hidden; }
  .hero-card::before { content:'';position:absolute;top:-60px;right:-60px;width:200px;height:200px;background:radial-gradient(circle,rgba(200,240,96,.12) 0%,transparent 70%);pointer-events:none; }
  .code-snippet { font-family:var(--ff-mono);font-size:.78rem;line-height:1.9;color:#666; }
  .code-snippet .kw { color:var(--accent2); }
  .code-snippet .fn { color:var(--accent); }
  .code-snippet .str { color:#c084fc; }
  .code-snippet .cm { color:#555;font-style:italic; }
  .code-snippet .num { color:#fb923c; }
  .stat-row { display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--border);border-radius:10px;overflow:hidden;margin-top:1.5rem; }
  .stat-cell { background:var(--surface);padding:1rem;text-align:center; }
  .stat-cell .val { font-size:1.4rem;font-weight:800;color:var(--accent);display:block; }
  .stat-cell .lbl { font-size:.68rem;color:var(--sub);text-transform:uppercase;letter-spacing:.1em;font-family:var(--ff-mono); }
  .hero-scroll { display:flex;align-items:center;gap:.75rem;font-size:.75rem;font-family:var(--ff-mono);color:var(--sub);padding-top:2rem;animation:fadeIn 1s var(--ease) 1s both; }
  .scroll-line { width:48px;height:1px;background:var(--muted);position:relative;overflow:hidden; }
  .scroll-line::after { content:'';position:absolute;top:0;left:-100%;width:100%;height:100%;background:var(--accent);animation:scrollLine 2s ease-in-out infinite 1.2s; }
  @keyframes scrollLine { 0%{left:-100%}100%{left:100%} }

  /* ABOUT */
  #about { padding:8rem 3rem;max-width:1200px;margin:0 auto; }
  .section-label { font-family:var(--ff-mono);font-size:.72rem;color:var(--accent);text-transform:uppercase;letter-spacing:.2em;display:flex;align-items:center;gap:.6rem;margin-bottom:1rem; }
  .section-label::before { content:'//';opacity:.5; }
  .section-heading { font-size:clamp(2rem,4vw,3.5rem);font-weight:800;letter-spacing:-.03em;line-height:1.1;margin-bottom:3rem; }
  .section-heading span { color:var(--accent); }
  .about-grid { display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start; }
  .about-text p { color:#999;line-height:1.9;margin-bottom:1.2rem;font-size:.97rem; }
  .about-text p strong { color:var(--text); }
  .about-text .highlight-box { border-left:2px solid var(--accent);padding:.8rem 1.2rem;background:rgba(200,240,96,.04);border-radius:0 8px 8px 0;margin:1.5rem 0;font-style:italic;font-family:var(--ff-serif);font-size:1.05rem;color:var(--text); }
  .skills-grid { display:grid;grid-template-columns:1fr 1fr;gap:.6rem; }
  .skill-tag { display:flex;align-items:center;gap:.6rem;background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:.65rem 1rem;font-size:.8rem;font-family:var(--ff-mono);transition:border-color .2s,transform .2s var(--ease); }
  .skill-tag:hover { border-color:var(--accent);transform:translateX(4px); }
  .skill-tag .dot { width:6px;height:6px;border-radius:50%;background:var(--accent);flex-shrink:0; }

  /* PROJECTS */
  #projects { padding:8rem 3rem;background:var(--surface);border-top:1px solid var(--border);border-bottom:1px solid var(--border); }
  .projects-inner { max-width:1200px;margin:0 auto; }
  .projects-list { display:grid;gap:1.5rem;margin-top:1rem; }
  .project-card { background:var(--bg);border:1px solid var(--border);border-radius:14px;padding:2.2rem;display:grid;grid-template-columns:1fr auto;gap:2rem;align-items:start;transition:border-color .25s,transform .3s var(--ease),box-shadow .3s;cursor:pointer;position:relative;overflow:hidden; }
  .project-card::before { content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(200,240,96,.03) 0%,transparent 60%);opacity:0;transition:opacity .3s; }
  .project-card:hover { border-color:rgba(200,240,96,.3);transform:translateY(-4px);box-shadow:0 20px 48px rgba(0,0,0,.4); }
  .project-card:hover::before { opacity:1; }
  .project-num { font-family:var(--ff-mono);font-size:.7rem;color:var(--sub);margin-bottom:.5rem; }
  .project-name { font-size:1.35rem;font-weight:700;margin-bottom:.6rem;transition:color .2s; }
  .project-card:hover .project-name { color:var(--accent); }
  .project-desc { color:#888;font-size:.9rem;line-height:1.7;max-width:560px; }
  .tech-tags { display:flex;flex-wrap:wrap;gap:.4rem;margin-top:1.2rem; }
  .tech-tag { font-family:var(--ff-mono);font-size:.7rem;color:var(--accent2);border:1px solid rgba(96,200,240,.2);border-radius:4px;padding:.2rem .55rem; }
  .project-links { display:flex;flex-direction:column;gap:.6rem;align-items:flex-end; }
  .icon-btn { width:40px;height:40px;border-radius:8px;background:var(--surface);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;text-decoration:none;color:var(--sub);font-size:.72rem;font-family:var(--ff-mono);font-weight:700;transition:background .2s,color .2s,border-color .2s; }
  .icon-btn:hover { background:var(--accent);color:var(--bg);border-color:var(--accent); }
  .featured-badge { display:inline-flex;align-items:center;gap:.4rem;font-family:var(--ff-mono);font-size:.65rem;color:var(--bg);background:var(--accent);padding:.2rem .6rem;border-radius:4px;text-transform:uppercase;letter-spacing:.1em;position:absolute;top:1.2rem;right:1.2rem; }

  /* EXPERIENCE */
  #experience { padding:8rem 3rem;max-width:1200px;margin:0 auto; }
  .timeline { position:relative;padding-left:2rem; }
  .timeline::before { content:'';position:absolute;left:0;top:8px;bottom:0;width:1px;background:linear-gradient(to bottom,var(--accent),transparent); }
  .timeline-item { position:relative;margin-bottom:3rem;padding-left:1.5rem;opacity:0;transform:translateX(-20px);transition:opacity .6s var(--ease),transform .6s var(--ease); }
  .timeline-item.visible { opacity:1;transform:translateX(0); }
  .timeline-item::before { content:'';position:absolute;left:-2rem;top:8px;width:9px;height:9px;border-radius:50%;background:var(--accent);border:2px solid var(--bg);box-shadow:0 0 0 4px rgba(200,240,96,.15); }
  .exp-meta { display:flex;align-items:center;gap:1rem;flex-wrap:wrap;margin-bottom:.5rem; }
  .exp-period { font-family:var(--ff-mono);font-size:.72rem;color:var(--sub); }
  .exp-badge { font-family:var(--ff-mono);font-size:.65rem;border:1px solid var(--border);color:var(--sub);padding:.1rem .5rem;border-radius:4px; }
  .exp-role { font-size:1.2rem;font-weight:700;margin-bottom:.2rem; }
  .exp-company { color:var(--accent);font-size:.9rem;font-weight:600;margin-bottom:.7rem; }
  .exp-desc { color:#888;font-size:.9rem;line-height:1.8;max-width:620px; }
  .exp-desc li { margin-left:1.2rem;margin-bottom:.3rem; }

  /* EDUCATION */
  #education { padding:6rem 3rem;background:var(--surface);border-top:1px solid var(--border); }
  .education-inner { max-width:1200px;margin:0 auto; }
  .edu-card { background:var(--bg);border:1px solid var(--border);border-radius:14px;padding:2rem 2.5rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:1.5rem;transition:border-color .3s,transform .3s var(--ease); }
  .edu-card:hover { border-color:rgba(200,240,96,.3);transform:translateY(-3px); }
  .edu-degree { font-size:1.2rem;font-weight:700;margin-bottom:.3rem; }
  .edu-school { color:var(--accent);font-size:.9rem;font-weight:600;margin-bottom:.3rem; }
  .edu-meta { font-family:var(--ff-mono);font-size:.75rem;color:var(--sub); }
  .edu-gpa { font-family:var(--ff-mono);font-size:2.2rem;font-weight:800;color:var(--accent);text-align:right; }
  .edu-gpa span { display:block;font-size:.7rem;color:var(--sub);text-align:right;margin-top:.2rem;letter-spacing:.1em;text-transform:uppercase; }

  /* CONTACT */
  #contact { padding:8rem 3rem;border-top:1px solid var(--border); }
  .contact-inner { max-width:700px;margin:0 auto;text-align:center; }
  .contact-heading { font-size:clamp(2.5rem,5vw,4.5rem);font-weight:800;letter-spacing:-.04em;line-height:1.05;margin-bottom:1.2rem; }
  .contact-heading em { font-family:var(--ff-serif);font-style:italic;font-weight:400;color:var(--accent); }
  .contact-sub { color:#888;margin-bottom:2.5rem;font-size:.95rem;line-height:1.8; }
  .contact-form { display:grid;gap:1rem;text-align:left;margin-bottom:2rem; }
  .form-row { display:grid;grid-template-columns:1fr 1fr;gap:1rem; }
  .form-group { display:flex;flex-direction:column;gap:.4rem; }
  .form-group label { font-family:var(--ff-mono);font-size:.72rem;text-transform:uppercase;letter-spacing:.1em;color:var(--sub); }
  .form-group input,.form-group textarea,.form-group select { background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:.8rem 1rem;color:var(--text);font-family:var(--ff-head);font-size:.9rem;transition:border-color .2s,box-shadow .2s;outline:none; }
  .form-group input:focus,.form-group textarea:focus,.form-group select:focus { border-color:rgba(200,240,96,.4);box-shadow:0 0 0 3px rgba(200,240,96,.08); }
  .form-group textarea { resize:vertical;min-height:120px; }
  .form-group select option { background:var(--surface); }
  .submit-btn { width:100%;padding:1rem;background:var(--accent);color:var(--bg);border:none;border-radius:8px;cursor:pointer;font-family:var(--ff-head);font-size:.9rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;transition:transform .25s var(--ease),box-shadow .25s; }
  .submit-btn:hover { transform:translateY(-2px);box-shadow:0 12px 32px rgba(200,240,96,.3); }
  .contact-links { display:flex;justify-content:center;gap:1rem;margin-top:2rem;flex-wrap:wrap; }
  .contact-link { display:inline-flex;align-items:center;gap:.5rem;padding:.65rem 1.2rem;border-radius:8px;background:var(--surface);border:1px solid var(--border);color:var(--sub);text-decoration:none;font-family:var(--ff-mono);font-size:.75rem;transition:all .2s var(--ease); }
  .contact-link:hover { background:var(--accent);color:var(--bg);border-color:var(--accent);transform:translateY(-2px); }

  footer { padding:2rem 3rem;border-top:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;font-family:var(--ff-mono);font-size:.75rem;color:var(--sub);position:relative;z-index:1; }

  .marquee-wrap { border-top:1px solid var(--border);border-bottom:1px solid var(--border);overflow:hidden;padding:1rem 0;background:var(--surface);position:relative;z-index:1; }
  .marquee-track { display:flex;gap:0;width:max-content;animation:marquee 20s linear infinite; }
  .marquee-track span { white-space:nowrap;padding:0 2.5rem;font-size:.8rem;font-weight:700;letter-spacing:.15em;text-transform:uppercase;color:var(--sub); }
  .marquee-track span.accent { color:var(--accent); }
  @keyframes marquee { 0%{transform:translateX(0)}100%{transform:translateX(-50%)} }

  @keyframes fadeUp { from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:translateY(0)} }
  @keyframes fadeIn { from{opacity:0}to{opacity:1} }
  .reveal { opacity:0;transform:translateY(30px);transition:opacity .7s var(--ease),transform .7s var(--ease); }
  .reveal.visible { opacity:1;transform:translateY(0); }

  #toast { position:fixed;bottom:2rem;right:2rem;z-index:999;background:var(--accent);color:var(--bg);padding:.8rem 1.4rem;border-radius:8px;font-family:var(--ff-mono);font-size:.8rem;font-weight:700;transform:translateY(80px);opacity:0;transition:all .4s var(--ease); }
  #toast.show { transform:translateY(0);opacity:1; }

  @media(max-width:768px){
    nav { padding:1rem 1.5rem; }
    .nav-links { display:none; }
    #hero { padding:8rem 1.5rem 3rem; }
    .hero-grid { grid-template-columns:1fr;gap:2.5rem; }
    #about,#experience,#education { padding:5rem 1.5rem; }
    #projects,#contact { padding:5rem 1.5rem; }
    .about-grid { grid-template-columns:1fr;gap:3rem; }
    .skills-grid { grid-template-columns:1fr; }
    .form-row { grid-template-columns:1fr; }
    .edu-card { flex-direction:column; }
    .edu-gpa { text-align:left; }
    .edu-gpa span { text-align:left; }
    footer { flex-direction:column;gap:.5rem;text-align:center; }
  }
</style>
</head>
<body>
<div id="cursor"></div>
<div id="cursor-ring"></div>
<div id="toast">✓ Message sent — I'll get back to you soon!</div>

<nav>
  <div class="nav-logo">SMD.dev</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="nav-cta" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Hire Me</button>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid">
    <div>
      <div class="hero-badge">Open to opportunities · 2026 Graduate</div>
      <h1 class="hero-name">Shaik<br>Mohammed<br><em>Owais</em></h1>
      <p class="hero-title">// Full-Stack Developer &amp; Web3 Builder</p>
      <p class="hero-desc">I build full-stack web applications and decentralised systems. From MERN-stack products to Move smart contracts on Aptos — I love turning ideas into working software.</p>
      <div class="hero-actions">
        <a href="#projects" class="btn-primary"><span>↓</span> View My Work</a>
        <a href="https://github.com/SMD111-git" target="_blank" class="btn-ghost">GitHub →</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-card">
        <div class="code-snippet">
          <span class="cm">// full-stack &amp; web3 developer</span><br>
          <span class="kw">const</span> owais = {<br>
          &nbsp;&nbsp;name: <span class="str">'Shaik Mohammed Owais'</span>,<br>
          &nbsp;&nbsp;stack: [<span class="str">'React'</span>, <span class="str">'Node'</span>, <span class="str">'MongoDB'</span>],<br>
          &nbsp;&nbsp;web3: <span class="str">'Aptos (Move) + IPFS'</span>,<br>
          &nbsp;&nbsp;graduating: <span class="num">2026</span>,<br>
          &nbsp;&nbsp;status: <span class="fn">() =&gt;</span> {<br>
          &nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> <span class="str">'actively seeking roles'</span><br>
          &nbsp;&nbsp;}<br>
          }<br><br>
       
        </div>
        <div class="stat-row">
          <div class="stat-cell"><span class="val" id="c1">0</span><span class="lbl">Projects</span></div>
          <div class="stat-cell"><span class="val" id="c2">0</span><span class="lbl">Tech Stack</span></div>
          <div class="stat-cell"><span class="val" id="c3">0</span><span class="lbl">CGPA</span></div>
        </div>
      </div>
    </div>
  </div>
  <div class="hero-scroll"><div class="scroll-line"></div>Scroll to explore</div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <span>React.js</span><span class="accent">✦</span><span>Node.js</span><span class="accent">✦</span><span>Express</span><span class="accent">✦</span><span>MongoDB</span><span class="accent">✦</span><span>MySQL</span><span class="accent">✦</span><span>TypeScript</span><span class="accent">✦</span><span>JavaScript</span><span class="accent">✦</span><span>Java</span><span class="accent">✦</span><span>Python</span><span class="accent">✦</span><span>Aptos Move</span><span class="accent">✦</span><span>IPFS</span><span class="accent">✦</span><span>Git &amp; GitHub</span><span class="accent">✦</span>
    <span>React.js</span><span class="accent">✦</span><span>Node.js</span><span class="accent">✦</span><span>Express</span><span class="accent">✦</span><span>MongoDB</span><span class="accent">✦</span><span>MySQL</span><span class="accent">✦</span><span>TypeScript</span><span class="accent">✦</span><span>JavaScript</span><span class="accent">✦</span><span>Java</span><span class="accent">✦</span><span>Python</span><span class="accent">✦</span><span>Aptos Move</span><span class="accent">✦</span><span>IPFS</span><span class="accent">✦</span><span>Git &amp; GitHub</span><span class="accent">✦</span>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About Me</div>
  <h2 class="section-heading reveal">Who I <span>Am</span></h2>
  <div class="about-grid">
    <div class="about-text reveal">
      <p>Hey — I'm Owais, a <strong>final-year Computer Science student</strong> at MITS University (graduating Apr 2026) with a deep passion for full-stack development and decentralised applications.</p>
      <div class="highlight-box">"I don't just learn technologies — I build things with them, from security tools to Web3 DApps."</div>
      <p>My journey spans <strong>MERN-stack web apps</strong>, real-time backends, open-source collaboration, and most recently <strong>Move smart contracts on Aptos blockchain</strong> with IPFS-based storage.</p>
      <p>I served as <strong>Student Coordinator of the College Coding Club</strong>, organising workshops, coding contests, and hackathon prep sessions — because I believe community makes better engineers.</p>
    </div>
    <div class="reveal">
      <div style="font-family:var(--ff-mono);font-size:.72rem;color:var(--sub);text-transform:uppercase;letter-spacing:.12em;margin-bottom:1rem;">Technical Skills</div>
      <div class="skills-grid">
        <div class="skill-tag"><span class="dot"></span>React.js</div>
        <div class="skill-tag"><span class="dot"></span>Node.js</div>
        <div class="skill-tag"><span class="dot"></span>Express.js</div>
        <div class="skill-tag"><span class="dot"></span>MongoDB</div>
        <div class="skill-tag"><span class="dot"></span>MySQL</div>
        <div class="skill-tag"><span class="dot"></span>JavaScript</div>
        <div class="skill-tag"><span class="dot"></span>TypeScript</div>
        <div class="skill-tag"><span class="dot"></span>Java</div>
        <div class="skill-tag"><span class="dot"></span>Python</div>
        <div class="skill-tag"><span class="dot"></span>Aptos Move</div>
        <div class="skill-tag"><span class="dot"></span>Redux Toolkit</div>
        <div class="skill-tag"><span class="dot"></span>Git &amp; GitHub</div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="projects-inner">
    <div class="section-label">Selected Work</div>
    <h2 class="section-heading reveal">Projects I've <span>Built</span></h2>
    <div class="projects-list">

      <div class="project-card reveal">
        <span class="featured-badge">★ Featured</span>
        <div>
          <div class="project-num">01</div>
          <div class="project-name">Skill Passport DPP (NFT Web3)</div>
          <div class="project-desc">A decentralised skill-verification DApp on Aptos blockchain using Move smart contracts to issue NFT-based credentials. Features wallet authentication, role-based access control, and IPFS-based certificate storage with a React + TypeScript frontend.</div>
          <div class="tech-tags"><span class="tech-tag">React.js</span><span class="tech-tag">TypeScript</span><span class="tech-tag">Aptos Move</span><span class="tech-tag">IPFS</span><span class="tech-tag">Smart Contracts</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

      <div class="project-card reveal">
        <div>
          <div class="project-num">02</div>
          <div class="project-name">Email Spoofing Analyzer</div>
          <div class="project-desc">A MERN-based web application that analyses security data and maps it to MITRE ATT&amp;CK tactics and techniques, helping security teams understand attacker behaviour in a structured, visual format.</div>
          <div class="tech-tags"><span class="tech-tag">React.js</span><span class="tech-tag">Node.js</span><span class="tech-tag">Express.js</span><span class="tech-tag">MongoDB</span><span class="tech-tag">MITRE ATT&CK</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

      <div class="project-card reveal">
        <div>
          <div class="project-num">03</div>
          <div class="project-name">Video Platform Backend</div>
          <div class="project-desc">A production-grade RESTful backend built with Node.js and Express, implementing JWT authentication, bcrypt password hashing, video uploads via Multer, and complete APIs for likes, comments, and subscriptions with MongoDB schemas.</div>
          <div class="tech-tags"><span class="tech-tag">Node.js</span><span class="tech-tag">Express.js</span><span class="tech-tag">MongoDB</span><span class="tech-tag">JWT</span><span class="tech-tag">Multer</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

      <div class="project-card reveal">
        <div>
          <div class="project-num">04</div>
          <div class="project-name">URL Shortener</div>
          <div class="project-desc">A full-stack URL shortener using the MERN stack. Generates, stores, and redirects shortened links with input validation and collision handling. Clean, minimal UI with instant redirect.</div>
          <div class="tech-tags"><span class="tech-tag">React.js</span><span class="tech-tag">Node.js</span><span class="tech-tag">Express.js</span><span class="tech-tag">MongoDB</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

      <div class="project-card reveal">
        <div>
          <div class="project-num">05</div>
          <div class="project-name">Todo App (Redux Toolkit)</div>
          <div class="project-desc">A scalable Todo application using React and Redux Toolkit, featuring centralised state management and full CRUD operations with predictable UI updates. Clean architecture with Redux slices and selectors.</div>
          <div class="tech-tags"><span class="tech-tag">React.js</span><span class="tech-tag">Redux Toolkit</span><span class="tech-tag">JavaScript</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

      <div class="project-card reveal">
        <div>
          <div class="project-num">06</div>
          <div class="project-name">Tic-Tac-Toe (Ticateo)</div>
          <div class="project-desc">A browser-based Tic-Tac-Toe game in React with win/draw detection, turn management, and responsive state handling using React Hooks. Clean, intuitive UI with instant game-state feedback.</div>
          <div class="tech-tags"><span class="tech-tag">React.js</span><span class="tech-tag">JavaScript</span><span class="tech-tag">React Hooks</span></div>
        </div>
        <div class="project-links">
          <a href="https://github.com/SMD111-git" target="_blank" class="icon-btn">GH</a>
          <a href="#" class="icon-btn">↗</a>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">Experience</div>
  <h2 class="section-heading reveal">Where I've <span>Contributed</span></h2>
  <div class="timeline">

    <div class="timeline-item">
      <div class="exp-meta"><span class="exp-period">Feb 2025 — Aug 2025</span><span class="exp-badge">Leadership</span></div>
      <div class="exp-role">Coding Club — Student Coordinator</div>
      <div class="exp-company">MITS University</div>
      <ul class="exp-desc">
        <li>Led and managed the college coding club, driving a culture of active problem-solving.</li>
        <li>Organised workshops, coding contests, and hackathon preparation sessions.</li>
        <li>Helped students build collaborative development skills and competitive programming habits.</li>
      </ul>
    </div>

    <div class="timeline-item">
      <div class="exp-meta"><span class="exp-period">Open Source</span><span class="exp-badge">Contributor</span></div>
      <div class="exp-role">Open-Source Contributor — Web Development</div>
      <div class="exp-company">VSOC (Virtual Summer of Code)</div>
      <ul class="exp-desc">
        <li>Contributed to a travel booking web project, developing React frontend components and Node.js backend APIs.</li>
        <li>Worked with Git-based collaborative workflows and participated in code reviews.</li>
        <li>Improved UI functionality and API integration in a distributed open-source team environment.</li>
      </ul>
    </div>

  </div>
</section>



<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div class="section-label" style="justify-content:center;">Contact</div>
    <h2 class="contact-heading reveal">Let's Build Something <em>Together</em></h2>
    <p class="contact-sub reveal">I'm actively looking for full-time roles and internships. If you have an opportunity, a project, or just want to connect — I reply to every message.</p>
    <form class="contact-form reveal" id="contactForm" onsubmit="handleSubmit(event)">
      <div class="form-row">
        <div class="form-group"><label>Your Name</label><input type="text" placeholder="Jane Smith" required></div>
        <div class="form-group"><label>Email</label><input type="email" placeholder="jane@company.com" required></div>
      </div>
      <div class="form-group">
        <label>Subject</label>
        <select><option>Job Opportunity</option><option>Internship</option><option>Freelance / Project</option><option>Open Source Collab</option><option>Just Saying Hi</option></select>
      </div>
      <div class="form-group"><label>Message</label><textarea placeholder="Tell me about the role or project..."></textarea></div>
      <button type="submit" class="submit-btn">Send Message →</button>
    </form>
    <div class="contact-links reveal">
      <a href="https://github.com/SMD111-git" target="_blank" class="contact-link">⌥ GitHub</a>
      <a href="https://www.linkedin.com/in/smd-owais-7703b7245/" target="_blank" class="contact-link">in LinkedIn</a>
      <a href="mailto:owaissmd33@gmail.com" class="contact-link">✉ Email</a>
      
    </div>
  </div>
</section>

<footer>
  <span>© 2025 Shaik Mohammed Owais · All rights reserved.</span>
  <span>owaissmd33@gmail.com</span>
</footer>

<script>
const cursor=document.getElementById('cursor'),ring=document.getElementById('cursor-ring');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;cursor.style.left=mx+'px';cursor.style.top=my+'px';});
(function a(){rx+=(mx-rx)*.12;ry+=(my-ry)*.12;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(a);})();
document.querySelectorAll('a,button,.project-card,.skill-tag,.icon-btn,.contact-link,.nav-cta,.edu-card').forEach(el=>{
  el.addEventListener('mouseenter',()=>document.body.classList.add('hovering'));
  el.addEventListener('mouseleave',()=>document.body.classList.remove('hovering'));
});

function animateCount(el,target,suffix,duration,decimals){
  let start=null;
  function step(ts){
    if(!start)start=ts;
    const p=Math.min((ts-start)/duration,1);
    const ease=1-Math.pow(1-p,3);
    const val=ease*target;
    el.textContent=(decimals?val.toFixed(2):Math.round(val))+suffix;
    if(p<1)requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
}
let countersRan=false;
const heroObs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting&&!countersRan){
      countersRan=true;
      animateCount(document.getElementById('c1'),6,'+',1600,false);
      animateCount(document.getElementById('c2'),12,'+',1800,false);
      animateCount(document.getElementById('c3'),7.33,'',1800,true);
    }
  });
},{threshold:.3});
heroObs.observe(document.getElementById('hero'));

const obs=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target);}});},{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

const tlObs=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible');});},{threshold:.2});
document.querySelectorAll('.timeline-item').forEach((el,i)=>{el.style.transitionDelay=(i*0.18)+'s';tlObs.observe(el);});

function handleSubmit(e){
  e.preventDefault();
  const toast=document.getElementById('toast');
  toast.classList.add('show');
  setTimeout(()=>toast.classList.remove('show'),4000);
  e.target.reset();
}

window.addEventListener('scroll',()=>{
  let current='';
  document.querySelectorAll('section[id]').forEach(s=>{if(window.scrollY>=s.offsetTop-200)current=s.id;});
  document.querySelectorAll('.nav-links a').forEach(a=>{a.style.color=a.getAttribute('href')==='#'+current?'var(--text)':'';});
});
</script>
</body>
</html>
