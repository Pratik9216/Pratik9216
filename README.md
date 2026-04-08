<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Pratik Nichit</title>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=Geist+Mono:wght@300;400;500&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --bg:#fafaf8;
  --white:#ffffff;
  --ink:#18181b;
  --ink2:#52525b;
  --ink3:#a1a1aa;
  --border:#e4e4e7;
  --border2:#d4d4d8;
  --surface:#f4f4f5;
  --surface2:#ececed;
  --a1:#2563eb;    /* blue - accent primary */
  --a1bg:#eff6ff;
  --a1br:#bfdbfe;
  --a2:#059669;    /* emerald */
  --a2bg:#ecfdf5;
  --a2br:#a7f3d0;
  --a3:#d97706;    /* amber */
  --a3bg:#fffbeb;
  --a3br:#fde68a;
  --a4:#7c3aed;    /* violet */
  --a4bg:#f5f3ff;
  --a4br:#ddd6fe;
  --a5:#db2777;    /* pink */
  --a5bg:#fdf2f8;
  --a5br:#fbcfe8;
}
html,body{height:100%}
body{background:var(--bg);color:var(--ink);font-family:'Outfit',sans-serif;font-size:14px;line-height:1.6;overflow-x:hidden}

/* ──────────── LAYOUT ──────────── */
.shell{display:grid;grid-template-columns:260px 1fr;min-height:100vh}

/* ──────────── SIDEBAR ──────────── */
.sidebar{
  background:var(--ink);
  color:#e4e4e7;
  padding:32px 20px;
  display:flex;flex-direction:column;
  position:sticky;top:0;height:100vh;overflow-y:auto;
}

.p-top{padding-bottom:24px;border-bottom:1px solid #3f3f46;margin-bottom:24px}
.avi{
  width:52px;height:52px;border-radius:12px;
  background:linear-gradient(135deg,var(--a1),var(--a4));
  display:flex;align-items:center;justify-content:center;
  font-family:'Geist Mono',monospace;font-size:16px;font-weight:500;color:#fff;
  margin-bottom:12px;letter-spacing:-.02em;
}
.p-name{font-size:17px;font-weight:700;color:#fafafa;letter-spacing:-.02em;line-height:1.2}
.p-role{font-size:12px;color:#a1a1aa;margin-top:3px;font-weight:400}
.p-handle{font-family:'Geist Mono',monospace;font-size:11px;color:var(--a1);margin-top:6px;background:rgba(37,99,235,.15);padding:2px 8px;border-radius:4px;display:inline-block}

.nav-label{font-family:'Geist Mono',monospace;font-size:10px;color:#71717a;letter-spacing:.1em;text-transform:uppercase;padding:0 8px;margin-bottom:4px}
.nav-group{margin-bottom:16px}
.ni{
  display:flex;align-items:center;gap:10px;
  padding:9px 10px;border-radius:8px;
  cursor:pointer;font-size:13px;font-weight:500;color:#a1a1aa;
  transition:all .13s;border:1px solid transparent;
}
.ni:hover{background:#27272a;color:#e4e4e7}
.ni.on{background:#1d4ed8;color:#fff;border-color:#2563eb}
.ni-ic{width:16px;text-align:center;font-size:13px;flex-shrink:0}

.s-meta{margin-top:auto;padding-top:20px;border-top:1px solid #3f3f46}
.s-meta-row{display:flex;align-items:center;gap:7px;font-size:11px;color:#71717a;margin-bottom:5px;font-family:'Geist Mono',monospace}
.green-dot{width:6px;height:6px;border-radius:50%;background:#22c55e;flex-shrink:0;box-shadow:0 0 5px #22c55e}

/* ──────────── MAIN ──────────── */
.main{padding:40px 44px;overflow-y:auto;background:var(--bg)}
.sec{display:none;animation:fadein .22s ease}
.sec.on{display:block}
@keyframes fadein{from{opacity:0;transform:translateY(5px)}to{opacity:1;transform:none}}

/* page header */
.ph{margin-bottom:32px;display:flex;align-items:flex-end;justify-content:space-between;border-bottom:1px solid var(--border);padding-bottom:20px}
.ph-left h1{font-family:'Instrument Serif',serif;font-size:32px;font-weight:400;letter-spacing:-.02em;color:var(--ink);line-height:1}
.ph-left h1 em{font-style:italic;color:var(--a1)}
.ph-left p{font-size:13px;color:var(--ink3);margin-top:5px}
.ph-right{font-family:'Geist Mono',monospace;font-size:11px;color:var(--ink3)}

/* card system */
.card{background:var(--white);border:1px solid var(--border);border-radius:14px;padding:22px}
.card-title{font-family:'Geist Mono',monospace;font-size:10px;font-weight:500;color:var(--ink3);text-transform:uppercase;letter-spacing:.09em;margin-bottom:16px}

/* ──────────── OVERVIEW ──────────── */
.ov-hero{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:14px}
.hero-card{background:var(--white);border:1px solid var(--border);border-radius:14px;padding:24px}

/* stat strip */
.stat-strip{display:grid;grid-template-columns:repeat(3,1fr);gap:0;background:var(--white);border:1px solid var(--border);border-radius:14px;overflow:hidden;margin-bottom:14px}
.stat-cell{padding:20px 22px;border-right:1px solid var(--border)}
.stat-cell:last-child{border:none}
.stat-n{font-family:'Instrument Serif',serif;font-size:34px;color:var(--ink);line-height:1;font-style:italic}
.stat-l{font-size:12px;color:var(--ink3);margin-top:4px;font-weight:500}

/* about bullets */
.about-list{display:flex;flex-direction:column;gap:10px}
.al{display:flex;align-items:flex-start;gap:10px;font-size:13px;color:var(--ink2);line-height:1.6}
.al-mark{width:20px;height:20px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:11px;flex-shrink:0;margin-top:1px}
.al-mark.blue{background:var(--a1bg);color:var(--a1)}
.al-mark.grn{background:var(--a2bg);color:var(--a2)}
.al-mark.vio{background:var(--a4bg);color:var(--a4)}
.al-mark.amb{background:var(--a3bg);color:var(--a3)}
.al-mark.pnk{background:var(--a5bg);color:var(--a5)}

/* lang grid */
.lang-strip{display:grid;grid-template-columns:repeat(6,1fr);gap:8px}
.lc{border:1px solid var(--border);border-radius:10px;padding:12px 10px;text-align:center}
.lc-swatch{width:24px;height:24px;border-radius:6px;margin:0 auto 6px}
.lc-name{font-size:11px;font-weight:600;color:var(--ink)}
.lc-bar{height:2px;border-radius:1px;margin-top:6px}

/* ──────────── PROJECTS ──────────── */
.proj-list{display:flex;flex-direction:column;gap:12px}
.prow{
  background:var(--white);border:1px solid var(--border);border-radius:14px;
  padding:20px 22px;display:grid;grid-template-columns:40px 1fr auto;gap:16px;align-items:start;
  transition:border-color .15s,box-shadow .15s;cursor:default;
}
.prow:hover{border-color:var(--a1br);box-shadow:0 1px 12px rgba(37,99,235,.06)}
.prow-num{font-family:'Instrument Serif',serif;font-style:italic;font-size:28px;color:var(--border2);line-height:1;padding-top:2px;text-align:center}
.prow-name{font-size:15px;font-weight:700;color:var(--ink);letter-spacing:-.01em;margin-bottom:5px}
.prow-desc{font-size:12px;color:var(--ink2);line-height:1.65;margin-bottom:10px}
.tags{display:flex;flex-wrap:wrap;gap:5px}
.tag{padding:3px 9px;border-radius:20px;font-family:'Geist Mono',monospace;font-size:10px;font-weight:400;border:1px solid}
.ta{background:var(--a1bg);color:var(--a1);border-color:var(--a1br)}
.tg{background:var(--a2bg);color:var(--a2);border-color:var(--a2br)}
.tv{background:var(--a4bg);color:var(--a4);border-color:var(--a4br)}
.tb{background:var(--a3bg);color:var(--a3);border-color:var(--a3br)}
.tp{background:var(--a5bg);color:var(--a5);border-color:var(--a5br)}
.tn{background:var(--surface);color:var(--ink2);border-color:var(--border)}
.prow-link{white-space:nowrap;font-size:12px;font-weight:600;color:var(--a1);text-decoration:none;font-family:'Geist Mono',monospace;border:1px solid var(--a1br);background:var(--a1bg);padding:6px 12px;border-radius:8px;transition:background .13s}
.prow-link:hover{background:var(--a1);color:#fff}

/* ──────────── SKILLS ──────────── */
.sk-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.sk-section-head{font-family:'Geist Mono',monospace;font-size:10px;font-weight:500;color:var(--ink3);text-transform:uppercase;letter-spacing:.09em;margin-bottom:12px}
.pill-cloud{display:flex;flex-wrap:wrap;gap:6px}
.pill{padding:5px 12px;border-radius:20px;font-size:11px;font-family:'Geist Mono',monospace;border:1px solid;cursor:default;transition:transform .13s,box-shadow .13s}
.pill:hover{transform:translateY(-1px);box-shadow:0 2px 8px rgba(0,0,0,.06)}
.pa{background:var(--a1bg);color:var(--a1);border-color:var(--a1br)}
.pg{background:var(--a2bg);color:var(--a2);border-color:var(--a2br)}
.pv{background:var(--a4bg);color:var(--a4);border-color:var(--a4br)}
.pb{background:var(--a3bg);color:var(--a3);border-color:var(--a3br)}
.pp{background:var(--a5bg);color:var(--a5);border-color:var(--a5br)}
.pn{background:var(--surface);color:var(--ink2);border-color:var(--border2)}

/* ──────────── EXPERIENCE ──────────── */
.exp-list{display:flex;flex-direction:column;gap:0}
.exp-item{display:grid;grid-template-columns:120px 1fr;gap:24px;padding-bottom:32px;position:relative}
.exp-item:not(:last-child)::after{content:'';position:absolute;left:120px;top:0;bottom:0;width:1px;background:var(--border);transform:translateX(-50%)}
.exp-date{font-family:'Geist Mono',monospace;font-size:11px;color:var(--ink3);line-height:1.5;padding-top:3px;text-align:right;padding-right:24px}
.exp-type{display:inline-block;margin-top:6px;font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.05em;padding:2px 7px;border-radius:4px}
.exp-type.work{background:var(--a1bg);color:var(--a1);border:1px solid var(--a1br)}
.exp-type.edu{background:var(--a2bg);color:var(--a2);border:1px solid var(--a2br)}
.exp-right{padding-left:24px;border-left:1px solid var(--border)}
.exp-co{font-size:16px;font-weight:700;color:var(--ink);letter-spacing:-.01em}
.exp-role{font-size:13px;color:var(--a1);font-weight:500;margin-top:1px}
.exp-role.edu{color:var(--a2)}
.exp-loc{font-size:12px;color:var(--ink3);margin-top:2px;margin-bottom:12px;font-family:'Geist Mono',monospace}
.exp-pts{display:flex;flex-direction:column;gap:5px}
.exp-pt{font-size:12px;color:var(--ink2);padding-left:14px;position:relative;line-height:1.65}
.exp-pt::before{content:'→';position:absolute;left:0;color:var(--ink3);font-size:11px;top:.5px}

/* ──────────── ABOUT ──────────── */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.info-list{display:flex;flex-direction:column}
.ir{display:grid;grid-template-columns:100px 1fr;padding:9px 0;border-bottom:1px solid var(--border);align-items:start}
.ir:last-child{border:none}
.ir-l{font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;color:var(--ink3);font-family:'Geist Mono',monospace;padding-top:1px}
.ir-v{font-size:13px;color:var(--ink2)}
.ir-v a{color:var(--a1);text-decoration:none}
.ir-v a:hover{text-decoration:underline}

.cert-stack{display:flex;flex-direction:column;gap:8px}
.cert{display:flex;align-items:center;gap:12px;padding:12px 14px;border:1px solid var(--border);border-radius:10px;background:var(--white)}
.cert-ic{font-size:18px}
.cert-name{font-size:13px;font-weight:600;color:var(--ink)}
.cert-sub{font-size:11px;color:var(--ink3);margin-top:1px}

.seek-pills{display:flex;flex-wrap:wrap;gap:7px;margin-top:2px}

/* ──────────── README ──────────── */
.rm-wrap{background:var(--ink);border-radius:14px;overflow:hidden}
.rm-topbar{background:#27272a;padding:12px 18px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid #3f3f46}
.rm-dots{display:flex;gap:6px}
.rm-dot{width:10px;height:10px;border-radius:50%}
.rm-label{font-family:'Geist Mono',monospace;font-size:11px;color:#71717a}
.rm-copy{background:rgba(37,99,235,.2);border:1px solid rgba(37,99,235,.4);color:#93c5fd;padding:5px 13px;border-radius:6px;font-size:11px;font-family:'Geist Mono',monospace;cursor:pointer;transition:all .13s}
.rm-copy:hover{background:var(--a1);color:#fff;border-color:var(--a1)}
.rm-code{padding:22px;font-family:'Geist Mono',monospace;font-size:11.5px;line-height:1.85;white-space:pre;overflow-x:auto;max-height:560px;overflow-y:auto;color:#d4d4d8}
.rh{color:#a78bfa}.rc{color:#52525b}.rl{color:#6ee7b7}.rb{color:#93c5fd}

/* ──────────── CONNECT ──────────── */
.cc-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:14px}
.cc{background:var(--white);border:1px solid var(--border);border-radius:14px;padding:22px;text-align:center;cursor:pointer;transition:border-color .15s,box-shadow .15s}
.cc:hover{border-color:var(--a1br);box-shadow:0 2px 14px rgba(37,99,235,.07)}
.cc-icon{font-size:24px;margin-bottom:8px}
.cc-name{font-size:14px;font-weight:700;color:var(--ink);margin-bottom:3px}
.cc-val{font-family:'Geist Mono',monospace;font-size:11px;color:var(--a1)}

.avail-strip{background:var(--white);border:1px solid var(--border);border-radius:14px;overflow:hidden;display:grid;grid-template-columns:repeat(3,1fr)}
.av{padding:20px;text-align:center;border-right:1px solid var(--border)}
.av:last-child{border:none}
.av-v{font-family:'Instrument Serif',serif;font-style:italic;font-size:22px;color:var(--ink)}
.av-l{font-size:11px;color:var(--ink3);margin-top:3px;font-family:'Geist Mono',monospace}

/* scrollbar */
::-webkit-scrollbar{width:3px;height:3px}
::-webkit-scrollbar-track{background:transparent}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:2px}
</style>
</head>
<body>
<div class="shell">

<!-- ── SIDEBAR ── -->
<aside class="sidebar">
  <div class="p-top">
    <div class="avi">PN</div>
    <div class="p-name">Pratik Nichit</div>
    <div class="p-role">Full-Stack · AI / ML · Data Engineering</div>
    <div class="p-handle">@Pratik9216</div>
  </div>

  <div class="nav-group">
    <div class="nav-label">Menu</div>
    <div class="ni on"  onclick="go('overview',this)"><span class="ni-ic">⊞</span>Overview</div>
    <div class="ni"     onclick="go('projects',this)"><span class="ni-ic">◈</span>Projects</div>
    <div class="ni"     onclick="go('skills',this)"><span class="ni-ic">◎</span>Skills</div>
    <div class="ni"     onclick="go('experience',this)"><span class="ni-ic">◷</span>Experience</div>
    <div class="ni"     onclick="go('about',this)"><span class="ni-ic">◉</span>About</div>
    <div class="ni"     onclick="go('readme',this)"><span class="ni-ic">⌘</span>README.md</div>
    <div class="ni"     onclick="go('connect',this)"><span class="ni-ic">◌</span>Connect</div>
  </div>

  <div class="s-meta">
    <div class="s-meta-row"><span class="green-dot"></span>Open to work · Summer 2026</div>
    <div class="s-meta-row">📍 Charlotte, NC</div>
    <div class="s-meta-row">🎓 MS IT · GPA 4.0</div>
  </div>
</aside>

<!-- ── MAIN ── -->
<main class="main">

  <!-- OVERVIEW -->
  <section class="sec on" id="sec-overview">
    <div class="ph">
      <div class="ph-left"><h1>Hi, I'm <em>Pratik.</em></h1><p>Software engineer building at the intersection of code and intelligence</p></div>
      <div class="ph-right">UNC Charlotte · 2025–2026</div>
    </div>

    <div class="stat-strip">
      <div class="stat-cell"><div class="stat-n">4.0</div><div class="stat-l">GPA / 4.0</div></div>
      <div class="stat-cell"><div class="stat-n">2 yrs</div><div class="stat-l">Industry experience</div></div>
      <div class="stat-cell"><div class="stat-n">2</div><div class="stat-l">Hackathons</div></div>
    </div>

    <div class="ov-hero">
      <div class="hero-card">
        <div class="card-title">About me</div>
        <div class="about-list">
          <div class="al"><div class="al-mark blue">🎓</div><span><strong>MS in Information Technology</strong> @ UNC Charlotte — GPA 4.0 / 4.0</span></div>
          <div class="al"><div class="al-mark grn">💼</div><span>Former SWE @ <strong>MindBendersTech</strong> · Java · Spring Boot · Microservices</span></div>
          <div class="al"><div class="al-mark vio">🤖</div><span>Building with <strong>LLMs, RAG pipelines, MCP &amp; AI Agents</strong> — in production, not just notebooks</span></div>
          <div class="al"><div class="al-mark amb">🌱</div><span>Exploring <strong>Agent-to-Agent (A2A)</strong> workflows and Agentic RAG patterns</span></div>
          <div class="al"><div class="al-mark pnk">🎯</div><span>Seeking <strong>Backend · Data Engineer · AI/ML</strong> roles — Summer 2026</span></div>
        </div>
      </div>

      <div class="hero-card">
        <div class="card-title">Languages</div>
        <div class="lang-strip">
          <div class="lc"><div class="lc-swatch" style="background:#3776ab"></div><div class="lc-name">Python</div><div class="lc-bar" style="background:#3776ab"></div></div>
          <div class="lc"><div class="lc-swatch" style="background:#3178c6"></div><div class="lc-name">TS</div><div class="lc-bar" style="background:#3178c6"></div></div>
          <div class="lc"><div class="lc-swatch" style="background:#b07219"></div><div class="lc-name">Java</div><div class="lc-bar" style="background:#b07219"></div></div>
          <div class="lc"><div class="lc-swatch" style="background:#f1e05a"></div><div class="lc-name">JS</div><div class="lc-bar" style="background:#f1e05a"></div></div>
          <div class="lc"><div class="lc-swatch" style="background:#da5b0b"></div><div class="lc-name">Jupyter</div><div class="lc-bar" style="background:#da5b0b"></div></div>
          <div class="lc"><div class="lc-swatch" style="background:#cccccc"></div><div class="lc-name">Other</div><div class="lc-bar" style="background:#ccc"></div></div>
        </div>
      </div>
    </div>

    <!-- quick stack chips -->
    <div class="card">
      <div class="card-title">Core stack</div>
      <div class="pill-cloud">
        <span class="pill pa">Java</span><span class="pill pa">Spring Boot</span><span class="pill pa">Python</span><span class="pill pa">TypeScript</span>
        <span class="pill pg">Next.js</span><span class="pill pg">React</span><span class="pill pg">Angular</span><span class="pill pg">Node.js</span>
        <span class="pill pv">LangChain</span><span class="pill pv">RAG</span><span class="pill pv">LLMs</span><span class="pill pv">MCP</span>
        <span class="pill pb">Apache Spark</span><span class="pill pb">Databricks</span><span class="pill pb">AWS</span><span class="pill pb">Azure</span>
        <span class="pill pn">PostgreSQL</span><span class="pill pn">MongoDB</span><span class="pill pn">MySQL</span><span class="pill pn">Docker</span>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section class="sec" id="sec-projects">
    <div class="ph">
      <div class="ph-left"><h1>My <em>work.</em></h1><p>5 public repositories · full-stack · AI/ML · data engineering</p></div>
    </div>

    <div class="proj-list">
      <div class="prow">
        <div class="prow-num">01</div>
        <div>
          <div class="prow-name">SSDI Invoicing RAG</div>
          <div class="prow-desc">Full-stack invoice extraction & RAG system. Next.js frontend, Node.js backend, Python RAG layer with vector DB for contextual invoice querying and dynamic dashboards.</div>
          <div class="tags"><span class="tag ta">Next.js</span><span class="tag ta">RAG</span><span class="tag tg">Node.js</span><span class="tag tn">TypeScript</span><span class="tag tn">Python</span><span class="tag tn">MongoDB</span></div>
        </div>
        <a class="prow-link" href="https://github.com/Pratik9216/SSDI_Invoicing_RAG" target="_blank">↗ repo</a>
      </div>

      <div class="prow">
        <div class="prow-num">02</div>
        <div>
          <div class="prow-name">Customer360 — Cloud Analytics</div>
          <div class="prow-desc">E-commerce analytics pipeline built for Cloud Computing coursework. Covers data ingestion, EDA, Spark SQL queries with window functions, structured streaming, and MLlib clustering.</div>
          <div class="tags"><span class="tag tb">PySpark</span><span class="tag tb">Spark SQL</span><span class="tag tg">MLlib</span><span class="tag tn">Python</span><span class="tag tn">Parquet</span></div>
        </div>
        <a class="prow-link" href="https://github.com/Pratik9216/Cloud_Comp_Project_Group_6" target="_blank">↗ repo</a>
      </div>

      <div class="prow">
        <div class="prow-num">03</div>
        <div>
          <div class="prow-name">Sentiment Analysis App</div>
          <div class="prow-desc">Interactive NLP app with a live Streamlit UI for real-time sentiment scoring. Deployed on Replit. Jupyter notebooks for model experimentation alongside the production app.</div>
          <div class="tags"><span class="tag ta">Python</span><span class="tag ta">Streamlit</span><span class="tag tg">NLP</span><span class="tag tn">Jupyter</span><span class="tag tn">Replit</span></div>
        </div>
        <a class="prow-link" href="https://github.com/Pratik9216/Sentiment-Analysis" target="_blank">↗ repo</a>
      </div>

      <div class="prow">
        <div class="prow-num">04</div>
        <div>
          <div class="prow-name">Match-day Alerts</div>
          <div class="prow-desc">Real-time ML predictor for cricket big moments (wickets & boundaries) from ball-by-ball ODI data. Handles highly imbalanced datasets. Angular live UI with pre-trained models.</div>
          <div class="tags"><span class="tag tb">Scikit-learn</span><span class="tag tg">Angular</span><span class="tag ta">Python</span><span class="tag tn">Google Colab</span><span class="tag tn">Jupyter</span></div>
        </div>
        <a class="prow-link" href="https://github.com/Pratik9216/matchday-alerts" target="_blank">↗ repo</a>
      </div>

      <div class="prow">
        <div class="prow-num">05</div>
        <div>
          <div class="prow-name">ML Capstone — House Price Prediction</div>
          <div class="prow-desc">Intro to ML capstone benchmarking classical algorithms (Ridge, Random Forest, Gradient Boosting) against two research-paper approaches — spatial feature engineering with XGBoost and two-stage clustering with Explainable Boosting Machine (EBM). Full EDA and preprocessing on Kaggle Ames Housing dataset.</div>
          <div class="tags"><span class="tag tb">Scikit-learn</span><span class="tag tb">XGBoost</span><span class="tag tb">EBM</span><span class="tag tg">Pandas</span><span class="tag tg">NumPy</span><span class="tag tn">Matplotlib</span><span class="tag tn">Python</span><span class="tag tn">Jupyter</span></div>
        </div>
        <a class="prow-link" href="https://github.com/Pratik9216/IntroMLCapstone" target="_blank">↗ repo</a>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section class="sec" id="sec-skills">
    <div class="ph"><div class="ph-left"><h1>My <em>toolkit.</em></h1><p>Technologies I work with across backend, frontend, AI, and data</p></div></div>
    <div class="sk-grid">
      <div>
        <div class="card" style="margin-bottom:14px">
          <div class="sk-section-head">Languages & Frameworks</div>
          <div class="pill-cloud">
            <span class="pill pa">Java</span><span class="pill pa">Python</span><span class="pill pa">TypeScript</span><span class="pill pa">JavaScript</span>
            <span class="pill pg">Spring Boot</span><span class="pill pg">Next.js</span><span class="pill pg">React</span><span class="pill pg">Angular</span><span class="pill pg">Node.js</span><span class="pill pg">Express</span>
          </div>
        </div>
        <div class="card" style="margin-bottom:14px">
          <div class="sk-section-head">AI / ML Engineering</div>
          <div class="pill-cloud">
            <span class="pill pv">LangChain</span><span class="pill pv">RAG Pipelines</span><span class="pill pv">LLMs</span><span class="pill pv">MCP Protocol</span><span class="pill pv">A2A Agents</span><span class="pill pv">Vector DBs</span>
            <span class="pill pb">Scikit-learn</span><span class="pill pb">PyTorch</span><span class="pill pb">Pandas</span><span class="pill pb">NumPy</span><span class="pill pb">Streamlit</span><span class="pill pb">Jupyter</span>
          </div>
        </div>
        <div class="card">
          <div class="sk-section-head">Databases</div>
          <div class="pill-cloud">
            <span class="pill pg">PostgreSQL</span><span class="pill pg">MongoDB</span><span class="pill pg">MySQL</span><span class="pill pg">Oracle</span>
          </div>
        </div>
      </div>
      <div>
        <div class="card" style="margin-bottom:14px">
          <div class="sk-section-head">Cloud & Data Platforms</div>
          <div class="pill-cloud">
            <span class="pill pb">Apache Spark</span><span class="pill pb">Spark SQL</span><span class="pill pb">Apache Kafka</span><span class="pill pb">Apache Airflow</span>
            <span class="pill pa">Databricks</span><span class="pill pa">Snowflake</span><span class="pill pa">AWS</span><span class="pill pa">Azure</span><span class="pill pa">Docker</span><span class="pill pa">Google Colab</span>
          </div>
        </div>
        <div class="card" style="margin-bottom:14px">
          <div class="sk-section-head">DevOps & Testing</div>
          <div class="pill-cloud">
            <span class="pill pg">Git</span><span class="pill pg">GitHub Actions</span><span class="pill pg">Jenkins</span><span class="pill pg">Maven</span><span class="pill pg">Jest</span><span class="pill pg">Postman</span><span class="pill pg">Swagger</span><span class="pill pg">Jira</span>
          </div>
        </div>
        <div class="card">
          <div class="sk-section-head">Methodologies</div>
          <div class="pill-cloud">
            <span class="pill pn">Microservices</span><span class="pill pn">RESTful APIs</span><span class="pill pn">Agile / Scrum</span><span class="pill pn">CI/CD</span><span class="pill pn">OOP</span><span class="pill pn">ETL Pipelines</span><span class="pill pn">Kanban</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section class="sec" id="sec-experience">
    <div class="ph"><div class="ph-left"><h1>My <em>journey.</em></h1><p>Work history and education</p></div></div>
    <div class="card">
      <div class="exp-list">
        <div class="exp-item">
          <div class="exp-date">Jan 2025<br>– Dec 2026<div class="exp-type edu">Education</div></div>
          <div class="exp-right">
            <div class="exp-co">University of North Carolina, Charlotte</div>
            <div class="exp-role edu">MS in Information Technology — GPA 4.0 / 4.0</div>
            <div class="exp-loc">Charlotte, NC</div>
            <div class="exp-pts">
              <div class="exp-pt">Coursework: Cloud Computing for Data Analysis, Intro to ML, Distributed Systems, Database Systems</div>
              <div class="exp-pt">Built 5 public projects across full-stack, big data, and applied AI domains</div>
              <div class="exp-pt">Participated in VTHacks and NASA International Space Apps Challenge</div>
            </div>
          </div>
        </div>
        <div class="exp-item">
          <div class="exp-date">Mar 2023<br>– Dec 2024<div class="exp-type work">Work</div></div>
          <div class="exp-right">
            <div class="exp-co">MindBendersTech</div>
            <div class="exp-role">Software Engineer</div>
            <div class="exp-loc">Navi Mumbai, India</div>
            <div class="exp-pts">
              <div class="exp-pt">Designed and maintained event-driven microservices using Java, Spring Boot, Spring Data JPA & Hibernate — improved fault tolerance across distributed enterprise environments</div>
              <div class="exp-pt">Automated CI/CD pipelines with Git, Jenkins & Maven — reduced deployment time and manual intervention</div>
              <div class="exp-pt">Built coupon system UI in React.js with Jest test coverage; delivered across 6+ Agile sprint cycles</div>
              <div class="exp-pt">Owned backend module delivery from design through production in cross-functional Agile teams</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="sec" id="sec-about">
    <div class="ph"><div class="ph-left"><h1>About <em>me.</em></h1><p>Personal info, certifications & what I'm looking for</p></div></div>
    <div class="about-grid">
      <div class="card">
        <div class="card-title">Info</div>
        <div class="info-list">
          <div class="ir"><span class="ir-l">Name</span><span class="ir-v">Pratik Nichit</span></div>
          <div class="ir"><span class="ir-l">Location</span><span class="ir-v">Charlotte, NC, USA</span></div>
          <div class="ir"><span class="ir-l">Email</span><span class="ir-v"><a href="mailto:Pratik.nichit66@gmail.com">Pratik.nichit66@gmail.com</a></span></div>
          <div class="ir"><span class="ir-l">Phone</span><span class="ir-v">+1 704 208 8060</span></div>
          <div class="ir"><span class="ir-l">GitHub</span><span class="ir-v"><a href="https://github.com/Pratik9216" target="_blank">github.com/Pratik9216</a></span></div>
          <div class="ir"><span class="ir-l">LinkedIn</span><span class="ir-v"><a href="https://linkedin.com/in/Pratik-Nichit" target="_blank">in/Pratik-Nichit</a></span></div>
          <div class="ir"><span class="ir-l">Status</span><span class="ir-v" style="color:#16a34a;font-weight:600">● Open to work</span></div>
        </div>
      </div>
      <div>
        <div class="card" style="margin-bottom:14px">
          <div class="card-title">Certifications</div>
          <div class="cert-stack">
            <div class="cert"><div class="cert-ic">🥇</div><div><div class="cert-name">IBM Data Science Professional</div><div class="cert-sub">IBM · Coursera</div></div></div>
            <div class="cert"><div class="cert-ic">🚀</div><div><div class="cert-name">VTHacks</div><div class="cert-sub">Hackathon participant</div></div></div>
            <div class="cert"><div class="cert-ic">🌍</div><div><div class="cert-name">NASA Space Apps Challenge</div><div class="cert-sub">International hackathon</div></div></div>
          </div>
        </div>
        <div class="card">
          <div class="card-title">Seeking</div>
          <div class="seek-pills">
            <span class="pill pa">Backend SWE Intern</span>
            <span class="pill pg">Data Engineer Intern</span>
            <span class="pill pv">AI / ML Engineer</span>
            <span class="pill pb">Platform Engineer</span>
          </div>
          <p style="font-size:12px;color:var(--ink3);margin-top:12px;line-height:1.7">Available Summer 2026. Interested in roles combining backend systems, data pipelines, or applied LLM work.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- README -->
  <section class="sec" id="sec-readme">
    <div class="ph"><div class="ph-left"><h1>README<em>.md</em></h1><p>Paste into your Pratik9216/Pratik9216 repo</p></div></div>
    <div class="rm-wrap">
      <div class="rm-topbar">
        <div style="display:flex;align-items:center;gap:12px">
          <div class="rm-dots"><div class="rm-dot" style="background:#ef4444"></div><div class="rm-dot" style="background:#f59e0b"></div><div class="rm-dot" style="background:#22c55e"></div></div>
          <span class="rm-label">README.md — Pratik9216/Pratik9216</span>
        </div>
        <button class="rm-copy" onclick="copyRm()">⎘ Copy</button>
      </div>
      <div class="rm-code" id="rmContent"><span class="rc">&lt;!-- Pratik Nichit · GitHub Profile README --&gt;</span>

<span class="rh">&lt;div align="center"&gt;</span>

<span class="rb">![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&duration=3000&pause=800&color=2563EB&center=true&width=680&lines=Hi%2C+I'm+Pratik+Nichit+%F0%9F%91%8B;Full-Stack+%7C+AI+%2F+ML+Engineering+%7C+Data+Pipelines;Building+at+the+edge+of+code+%2B+intelligence;MS+IT+%40+UNC+Charlotte+%E2%80%94+GPA+4.0+%2F+4.0)</span>

<span class="rb">[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/Pratik-Nichit)</span>
<span class="rb">[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Pratik.nichit66@gmail.com)</span>
<span class="rb">[![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pratik9216)</span>

<span class="rh">&lt;/div&gt;</span>

---

<span class="rh">## 🧠 About Me</span>

&gt; *"I build things that think."*

- 🎓 **MS in Information Technology** @ UNC Charlotte — GPA **4.0 / 4.0**
- 💼 Former **Software Engineer** @ MindBendersTech · Java · Spring Boot · Microservices
- 🤖 Hands-on with **LLMs, RAG pipelines, MCP, AI Agents** — shipped, not just studied
- 🌱 Exploring **Agent-to-Agent (A2A)** workflows and Agentic RAG
- 🎯 Seeking: **Backend SWE · Data Engineer · AI/ML Engineer** — Summer 2026
- 🏅 IBM Data Science Certified · VTHacks · NASA Space Apps Challenge

---

<span class="rh">## 🛠️ Tech Stack</span>

<span class="rl">**🚀 Backend & Systems**</span>
<span class="rb">![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)</span>
<span class="rb">![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)</span>
<span class="rb">![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)</span>
<span class="rb">![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)</span>
<span class="rb">![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)</span>

<span class="rl">**🎨 Frontend**</span>
<span class="rb">![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)</span>
<span class="rb">![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)</span>
<span class="rb">![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)</span>

<span class="rl">**🤖 AI / ML (Applied)**</span>
<span class="rb">![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)</span>
<span class="rb">![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)</span>
<span class="rb">![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)</span>
<span class="rb">![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)</span>
<span class="rb">![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)</span>
<span class="rb">![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)</span>

<span class="rl">**📊 Data Platforms & Cloud**</span>
<span class="rb">![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)</span>
<span class="rb">![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)</span>
<span class="rb">![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)</span>
<span class="rb">![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)</span>
<span class="rb">![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)</span>
<span class="rb">![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)</span>
<span class="rb">![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)</span>

<span class="rl">**🗄️ Databases**</span>
<span class="rb">![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)</span>
<span class="rb">![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)</span>
<span class="rb">![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)</span>
<span class="rb">![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)</span>

---

<span class="rh">## 🚀 Featured Projects</span>

| Project | What it does | Stack |
|---------|-------------|-------|
| 🧾 **[SSDI Invoicing RAG](https://github.com/Pratik9216/SSDI_Invoicing_RAG)** | Invoice extraction + RAG system · Next.js frontend · Node.js backend | Next.js · Node.js · Python · RAG |
| 📊 **[Customer360 — Cloud Analytics](https://github.com/Pratik9216/Cloud_Comp_Project_Group_6)** | E-commerce analytics pipeline: ingestion → EDA → Spark SQL → Streaming → MLlib | PySpark · Spark SQL · MLlib |
| 🤖 **[Sentiment Analysis App](https://github.com/Pratik9216/Sentiment-Analysis)** | Live NLP app with Streamlit UI deployed on Replit | Python · Streamlit · NLP |
| 🏏 **[Match-day Alerts](https://github.com/Pratik9216/matchday-alerts)** | Real-time ML for cricket big moments · Angular live UI | Scikit-learn · Angular · Colab |
| 🏠 **[ML Capstone](https://github.com/Pratik9216/IntroMLCapstone)** | House price prediction benchmarking 5 ML models incl. XGBoost + spatial features | Scikit-learn · XGBoost · EBM |

---

<span class="rh">## 📊 GitHub Stats</span>

&lt;p align="center"&gt;
  &lt;img src="https://github-readme-stats.vercel.app/api?username=Pratik9216&show_icons=true&theme=tokyonight&hide_border=true" height="165"/&gt;
  &lt;img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pratik9216&layout=compact&theme=tokyonight&hide_border=true" height="165"/&gt;
&lt;/p&gt;
&lt;p align="center"&gt;
  &lt;img src="https://streak-stats.demolab.com?user=Pratik9216&theme=tokyonight&hide_border=true"/&gt;
&lt;/p&gt;

---

<span class="rh">## 💼 Experience</span>

**Software Engineer · MindBendersTech** · *Mar 2023 – Dec 2024 · Navi Mumbai*
- Event-driven microservices with Java, Spring Boot, JPA & Hibernate
- CI/CD automation with Git, Jenkins & Maven
- React.js UI with Jest coverage · 6+ Agile sprint cycles

---

<span class="rh">## 🏅 Certifications</span>

- 🥇 IBM Data Science Professional Certificate
- 🚀 VTHacks participant
- 🌍 NASA International Space Apps Challenge

---

&lt;p align="center"&gt;
  &lt;img src="https://komarev.com/ghpvc/?username=Pratik9216&label=Profile+views&color=2563EB&style=flat"/&gt;
&lt;/p&gt;</div>
    </div>
  </section>

  <!-- CONNECT -->
  <section class="sec" id="sec-connect">
    <div class="ph"><div class="ph-left"><h1>Let's <em>connect.</em></h1><p>Open for Summer 2026 internship & full-time roles</p></div></div>
    <div class="cc-grid">
      <div class="cc" onclick="window.open('https://linkedin.com/in/Pratik-Nichit','_blank')">
        <div class="cc-icon">💼</div>
        <div class="cc-name">LinkedIn</div>
        <div class="cc-val">in/Pratik-Nichit</div>
      </div>
      <div class="cc" onclick="window.open('mailto:Pratik.nichit66@gmail.com')">
        <div class="cc-icon">📧</div>
        <div class="cc-name">Email</div>
        <div class="cc-val">Pratik.nichit66@gmail.com</div>
      </div>
      <div class="cc" onclick="window.open('https://github.com/Pratik9216','_blank')">
        <div class="cc-icon">⚡</div>
        <div class="cc-name">GitHub</div>
        <div class="cc-val">@Pratik9216</div>
      </div>
    </div>
    <div class="avail-strip">
      <div class="av"><div class="av-v">Summer 2026</div><div class="av-l">target start</div></div>
      <div class="av"><div class="av-v">Intern / FTE</div><div class="av-l">both welcome</div></div>
      <div class="av"><div class="av-v">Remote / Onsite</div><div class="av-l">US preferred</div></div>
    </div>
  </section>

</main>
</div>

<script>
function go(id, el) {
  document.querySelectorAll('.sec').forEach(s => s.classList.remove('on'));
  document.querySelectorAll('.ni').forEach(n => n.classList.remove('on'));
  document.getElementById('sec-' + id).classList.add('on');
  if (el) el.classList.add('on');
}
function copyRm() {
  const raw = document.getElementById('rmContent').innerText;
  navigator.clipboard.writeText(raw).then(() => {
    const b = document.querySelector('.rm-copy');
    b.textContent = '✓ Copied!';
    setTimeout(() => b.textContent = '⎘ Copy', 2500);
  });
}
</script>
</body>
</html>
