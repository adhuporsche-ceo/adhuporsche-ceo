<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Adhithya K — Developer Profile</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.44.0/tabler-icons.min.css"/>
<style>
  *{box-sizing:border-box;margin:0;padding:0}
  body{
    font-family:'Google Sans','Segoe UI',sans-serif;
    background:#f8f9fa;
    color:#202124;
    min-height:100vh;
    padding:2rem 1rem;
  }
  a{color:#1a73e8;text-decoration:none}
  a:hover{text-decoration:underline}

  .wrap{max-width:760px;margin:0 auto}

  /* Google bar */
  .g-bar{
    height:5px;
    border-radius:3px;
    background:linear-gradient(90deg,#4285f4 0%,#4285f4 25%,#ea4335 25%,#ea4335 50%,#fbbc04 50%,#fbbc04 75%,#34a853 75%);
    margin-bottom:1.5rem;
  }

  /* Nav */
  .nav{
    display:flex;align-items:center;justify-content:space-between;
    margin-bottom:1.5rem;flex-wrap:wrap;gap:12px;
  }
  .google-logo{display:flex;gap:0;font-size:22px;font-weight:700;letter-spacing:-0.5px}
  .gl{font-style:normal}
  .gl.gb{color:#4285f4}.gl.go{color:#ea4335}.gl.gy{color:#fbbc04}
  .gl.gg{color:#34a853}.gl.glb{color:#4285f4}.gl.ge{color:#ea4335}
  .nav-sub{font-size:13px;color:#5f6368;margin-left:8px;font-weight:400}
  .nav-links{display:flex;gap:16px}
  .nav-links a{font-size:13px;color:#5f6368;display:inline-flex;align-items:center;gap:5px}
  .nav-links a:hover{color:#1a73e8;text-decoration:none}

  /* Hero */
  .hero{
    display:flex;align-items:flex-start;gap:20px;
    padding:24px 28px;
    background:#fff;
    border:1px solid #dadce0;
    border-radius:16px;
    margin-bottom:1rem;
    flex-wrap:wrap;
  }
  .avatar{
    width:88px;height:88px;border-radius:50%;
    background:linear-gradient(135deg,#1a73e8 0%,#34a853 100%);
    display:flex;align-items:center;justify-content:center;
    font-size:30px;font-weight:700;color:#fff;flex-shrink:0;letter-spacing:-1px;
    box-shadow:0 2px 8px rgba(26,115,232,.25);
  }
  .hero-info{flex:1;min-width:200px}
  .hero-info h1{font-size:24px;font-weight:500;color:#202124;margin-bottom:4px}
  .hero-info .role{font-size:14px;color:#5f6368;margin-bottom:4px}
  .hero-info .loc{font-size:13px;color:#80868b;margin-bottom:12px;display:flex;align-items:center;gap:4px}
  .chips{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:14px}
  .chip{
    display:inline-flex;align-items:center;gap:5px;
    padding:5px 12px;border-radius:20px;font-size:12px;font-weight:500;border:1px solid;
    cursor:default;
  }
  .chip.blue{background:#e8f0fe;color:#1a73e8;border-color:#aecbfa}
  .chip.green{background:#e6f4ea;color:#1e8e3e;border-color:#a8d5b5}
  .chip.red{background:#fce8e6;color:#c5221f;border-color:#f5c6c2}
  .chip.yellow{background:#fef9e7;color:#b06000;border-color:#fde99b}
  .chip.gray{background:#f1f3f4;color:#5f6368;border-color:#dadce0}
  .hero-actions{display:flex;gap:8px;flex-wrap:wrap}
  .btn{
    display:inline-flex;align-items:center;gap:6px;
    padding:8px 18px;border-radius:8px;font-size:13px;font-weight:500;
    border:1px solid #dadce0;cursor:pointer;transition:all .15s;
  }
  .btn:hover{background:#f1f3f4}
  .btn.primary{background:#1a73e8;color:#fff;border-color:#1a73e8}
  .btn.primary:hover{background:#1557b0}
  .btn.outlined{background:transparent;color:#1a73e8;border-color:#aecbfa}
  .btn.outlined:hover{background:#e8f0fe}

  /* Stat row */
  .stat-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:1rem}
  .stat-card{
    background:#fff;border:1px solid #dadce0;border-radius:12px;
    padding:16px;text-align:center;
  }
  .stat-val{font-size:28px;font-weight:500;line-height:1}
  .stat-lbl{font-size:12px;color:#5f6368;margin-top:4px}

  /* Section label */
  .section-label{
    font-size:11px;font-weight:600;letter-spacing:.08em;
    text-transform:uppercase;color:#80868b;margin-bottom:.65rem;margin-top:1.25rem;
  }

  /* Grid cards */
  .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:10px;margin-bottom:.5rem}
  .card{background:#fff;border:1px solid #dadce0;border-radius:12px;padding:16px 18px}
  .card-icon{
    width:40px;height:40px;border-radius:10px;
    display:flex;align-items:center;justify-content:center;margin-bottom:12px;
  }
  .card-icon i{font-size:20px}
  .ci-b{background:#e8f0fe} .ci-b i{color:#1a73e8}
  .ci-g{background:#e6f4ea} .ci-g i{color:#1e8e3e}
  .ci-r{background:#fce8e6} .ci-r i{color:#c5221f}
  .ci-y{background:#fef9e7} .ci-y i{color:#b06000}
  .card h3{font-size:13px;font-weight:500;color:#202124;margin-bottom:4px}
  .card p{font-size:12px;color:#5f6368;line-height:1.55}

  /* Skills */
  .skills-panel{background:#fff;border:1px solid #dadce0;border-radius:12px;padding:18px 20px}
  .prog-row{display:flex;align-items:center;gap:12px;margin-bottom:10px}
  .prog-row:last-child{margin-bottom:0}
  .prog-label{font-size:13px;color:#202124;width:100px;flex-shrink:0}
  .prog-track{flex:1;height:7px;background:#f1f3f4;border-radius:4px;overflow:hidden}
  .prog-bar{height:100%;border-radius:4px;width:0;transition:width 1.1s cubic-bezier(.4,0,.2,1)}
  .prog-pct{font-size:12px;color:#80868b;width:34px;text-align:right;flex-shrink:0}

  /* Timeline */
  .timeline{position:relative;padding-left:22px}
  .timeline::before{
    content:'';position:absolute;left:7px;top:6px;bottom:6px;
    width:1.5px;background:#dadce0;
  }
  .tl-item{position:relative;margin-bottom:18px}
  .tl-item:last-child{margin-bottom:0}
  .tl-dot{
    position:absolute;left:-18px;top:5px;
    width:12px;height:12px;border-radius:50%;border:2.5px solid;
  }
  .tl-dot.b{background:#e8f0fe;border-color:#1a73e8}
  .tl-dot.g{background:#e6f4ea;border-color:#34a853}
  .tl-dot.r{background:#fce8e6;border-color:#ea4335}
  .tl-date{font-size:11px;color:#80868b;margin-bottom:3px}
  .tl-role{font-size:14px;font-weight:500;color:#202124}
  .tl-co{font-size:12px;color:#5f6368;margin-top:2px;display:flex;align-items:center;gap:8px;flex-wrap:wrap}
  .pill{
    display:inline-block;padding:2px 8px;border-radius:4px;font-size:11px;font-weight:500;
    background:#f1f3f4;color:#5f6368;border:1px solid #dadce0;
  }

  /* Projects */
  .proj-card{
    background:#fff;border:1px solid #dadce0;border-radius:12px;
    padding:16px 18px;margin-bottom:10px;
    transition:box-shadow .2s;cursor:default;
  }
  .proj-card:hover{box-shadow:0 2px 10px rgba(0,0,0,.08)}
  .proj-header{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;margin-bottom:6px}
  .proj-title{font-size:15px;font-weight:500;color:#202124;display:flex;align-items:center;gap:8px}
  .proj-dot{width:10px;height:10px;border-radius:50%;flex-shrink:0}
  .proj-body{font-size:13px;color:#5f6368;line-height:1.6;margin-bottom:10px}
  .proj-tags{display:flex;flex-wrap:wrap;gap:5px}
  .tag{
    padding:3px 9px;border-radius:5px;font-size:11px;font-weight:500;
    background:#f1f3f4;color:#5f6368;border:1px solid #dadce0;
  }
  .proj-badge{
    display:inline-flex;align-items:center;padding:3px 10px;border-radius:6px;
    font-size:11px;font-weight:600;white-space:nowrap;flex-shrink:0;
  }
  .pb-b{background:#e8f0fe;color:#1a73e8}
  .pb-g{background:#e6f4ea;color:#1e8e3e}
  .pb-r{background:#fce8e6;color:#c5221f}
  .pb-y{background:#fef9e7;color:#b06000}

  /* Badges */
  .badge-grid{display:flex;flex-wrap:wrap;gap:7px}
  .badge{
    display:inline-flex;align-items:center;gap:5px;
    padding:6px 13px;border-radius:7px;font-size:12px;font-weight:500;border:1px solid;
  }
  .badge.filled-b{background:#1a73e8;color:#fff;border-color:#1a73e8}
  .badge.filled-g{background:#34a853;color:#fff;border-color:#34a853}
  .badge.filled-r{background:#ea4335;color:#fff;border-color:#ea4335}
  .badge.filled-y{background:#fbbc04;color:#5f4100;border-color:#fbbc04}
  .badge.out{background:transparent;color:#202124;border-color:#dadce0}
  .badge.out:hover{background:#f1f3f4}

  /* Divider */
  .divider{height:1px;background:#dadce0;margin:1.25rem 0}

  /* Currently learning */
  .learn-panel{
    background:#fff;border:1px solid #dadce0;border-radius:12px;
    overflow:hidden;
  }
  .learn-header{
    background:#f8f9fa;border-bottom:1px solid #dadce0;
    padding:10px 16px;font-size:12px;color:#5f6368;
    display:flex;align-items:center;gap:8px;
  }
  .dot{width:10px;height:10px;border-radius:50%;display:inline-block}
  .learn-body{padding:14px 18px;font-family:'Roboto Mono','Courier New',monospace;font-size:12.5px;line-height:2}
  .kw{color:#1a73e8}
  .str{color:#34a853}
  .cm{color:#80868b}
  .arr{color:#ea4335}

  /* Contact */
  .contact-row{display:flex;gap:10px;flex-wrap:wrap}
  .contact-card{
    background:#fff;border:1px solid #dadce0;border-radius:10px;
    padding:12px 16px;display:flex;align-items:center;gap:10px;
    flex:1;min-width:180px;
  }
  .contact-card i{font-size:20px;color:#1a73e8}
  .contact-card .c-label{font-size:11px;color:#80868b}
  .contact-card .c-val{font-size:13px;color:#202124;font-weight:500}

  /* Footer */
  .footer{
    display:flex;align-items:center;justify-content:space-between;
    padding-top:14px;border-top:1px solid #dadce0;flex-wrap:wrap;gap:8px;
    margin-top:1rem;
  }
  .footer-links{display:flex;gap:16px}
  .footer-links a{font-size:12px;color:#5f6368;display:inline-flex;align-items:center;gap:4px}
  .footer-links a:hover{color:#1a73e8}

  /* Dark mode */
  @media (prefers-color-scheme:dark){
    body{background:#0d1117;color:#e8eaed}
    .nav-sub,.nav-links a,.stat-lbl,.section-label,.prog-label,.prog-pct,
    .tl-date,.tl-co,.proj-body,.c-label,.footer-links a{color:#9aa0a6}
    .hero,.stat-card,.card,.skills-panel,.proj-card,.learn-panel,
    .contact-card{background:#1c1e24;border-color:#3c4043}
    .hero-info h1,.stat-val,.tl-role,.proj-title,.card h3,.c-val,
    .badge.out{color:#e8eaed}
    .g-bar,.chip.gray,.tag,.pill,.badge.out{border-color:#3c4043}
    .chip.gray{background:#2a2c32;color:#9aa0a6}
    .tag,.pill{background:#2a2c32;color:#9aa0a6;border-color:#3c4043}
    .badge.out{background:transparent}
    .badge.out:hover{background:#2a2c32}
    .btn:hover{background:#2a2c32}
    .chip.blue{background:#1a3a6b;color:#8ab4f8;border-color:#1a73e8}
    .chip.green{background:#0e3a1a;color:#81c995;border-color:#34a853}
    .chip.red{background:#4b1a18;color:#f28b82;border-color:#ea4335}
    .chip.yellow{background:#3d2a00;color:#fdd663;border-color:#fbbc04}
    .ci-b{background:#1a3a6b}.ci-g{background:#0e3a1a}
    .ci-r{background:#4b1a18}.ci-y{background:#3d2a00}
    .pb-b{background:#1a3a6b;color:#8ab4f8}
    .pb-g{background:#0e3a1a;color:#81c995}
    .pb-r{background:#4b1a18;color:#f28b82}
    .pb-y{background:#3d2a00;color:#fdd663}
    .prog-track{background:#2a2c32}
    .timeline::before,.divider,.footer{border-color:#3c4043}
    .learn-header{background:#15171d;border-color:#3c4043}
    .avatar{box-shadow:0 2px 12px rgba(26,115,232,.35)}
    .proj-card:hover{box-shadow:0 2px 10px rgba(0,0,0,.4)}
    .card-icon{border:1px solid #3c4043}
  }
</style>
</head>
<body>

<div class="wrap">

  <!-- Google bar -->
  <div class="g-bar"></div>

  <!-- Nav -->
  <nav class="nav">
    <div style="display:flex;align-items:baseline;gap:0">
      <div class="google-logo">
        <span class="gl gb">G</span><span class="gl go">o</span><span class="gl gy">o</span>
        <span class="gl gg">g</span><span class="gl glb">l</span><span class="gl ge">e</span>
      </div>
      <span class="nav-sub">Developer Profile</span>
    </div>
    <div class="nav-links">
      <a href="https://github.com/adhithya-k" target="_blank"><i class="ti ti-brand-github" aria-hidden="true"></i> GitHub</a>
      <a href="https://linkedin.com/in/adhithya-k-390780292" target="_blank"><i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn</a>
      <a href="mailto:adhicse005@email.com"><i class="ti ti-mail" aria-hidden="true"></i> Email</a>
    </div>
  </nav>

  <!-- Hero -->
  <div class="hero">
    <div class="avatar">AK</div>
    <div class="hero-info">
      <h1>Adhithya K</h1>
      <div class="role">Backend Developer &nbsp;·&nbsp; Cloud Enthusiast &nbsp;·&nbsp; AI Integrator</div>
      <div class="loc">
        <i class="ti ti-map-pin" style="font-size:14px" aria-hidden="true"></i>
        Coimbatore, Tamil Nadu &nbsp;·&nbsp; KCT — B.E. CSE (2025–2028)
      </div>
      <div class="chips">
        <span class="chip blue"><i class="ti ti-coffee" style="font-size:12px" aria-hidden="true"></i> Java</span>
        <span class="chip red"><i class="ti ti-bolt" style="font-size:12px" aria-hidden="true"></i> Spring Boot</span>
        <span class="chip yellow"><i class="ti ti-cloud" style="font-size:12px" aria-hidden="true"></i> AWS</span>
        <span class="chip green"><i class="ti ti-brand-python" style="font-size:12px" aria-hidden="true"></i> Python</span>
        <span class="chip gray"><i class="ti ti-database" style="font-size:12px" aria-hidden="true"></i> MySQL</span>
      </div>
      <div class="hero-actions">
        <a class="btn primary" href="mailto:adhicse005@email.com"><i class="ti ti-mail" style="font-size:14px" aria-hidden="true"></i> Hire Me</a>
        <a class="btn outlined" href="https://github.com/adhithya-k" target="_blank"><i class="ti ti-brand-github" style="font-size:14px" aria-hidden="true"></i> GitHub</a>
        <a class="btn" href="https://linkedin.com/in/adhithya-k-390780292" target="_blank"><i class="ti ti-brand-linkedin" style="font-size:14px" aria-hidden="true"></i> LinkedIn</a>
      </div>
    </div>
  </div>

  <!-- Stats -->
  <div class="stat-row">
    <div class="stat-card">
      <div class="stat-val" style="color:#1a73e8">3</div>
      <div class="stat-lbl"><i class="ti ti-briefcase" style="font-size:12px" aria-hidden="true"></i> Internships</div>
    </div>
    <div class="stat-card">
      <div class="stat-val" style="color:#34a853">5+</div>
      <div class="stat-lbl"><i class="ti ti-code" style="font-size:12px" aria-hidden="true"></i> Projects</div>
    </div>
    <div class="stat-card">
      <div class="stat-val" style="color:#ea4335">2</div>
      <div class="stat-lbl"><i class="ti ti-trophy" style="font-size:12px" aria-hidden="true"></i> Awards</div>
    </div>
  </div>

  <!-- Skills -->
  <div class="section-label">Skill proficiency</div>
  <div class="skills-panel">
    <div class="prog-row">
      <span class="prog-label">Java</span>
      <div class="prog-track"><div class="prog-bar" data-w="88" style="background:#1a73e8"></div></div>
      <span class="prog-pct">88%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">MySQL</span>
      <div class="prog-track"><div class="prog-bar" data-w="82" style="background:#34a853"></div></div>
      <span class="prog-pct">82%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">Python</span>
      <div class="prog-track"><div class="prog-bar" data-w="80" style="background:#fbbc04"></div></div>
      <span class="prog-pct">80%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">Spring Boot</span>
      <div class="prog-track"><div class="prog-bar" data-w="75" style="background:#ea4335"></div></div>
      <span class="prog-pct">75%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">Salesforce</span>
      <div class="prog-track"><div class="prog-bar" data-w="72" style="background:#1a73e8"></div></div>
      <span class="prog-pct">72%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">AWS</span>
      <div class="prog-track"><div class="prog-bar" data-w="70" style="background:#34a853"></div></div>
      <span class="prog-pct">70%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">JavaScript</span>
      <div class="prog-track"><div class="prog-bar" data-w="65" style="background:#fbbc04"></div></div>
      <span class="prog-pct">65%</span>
    </div>
    <div class="prog-row">
      <span class="prog-label">Flask</span>
      <div class="prog-track"><div class="prog-bar" data-w="68" style="background:#ea4335"></div></div>
      <span class="prog-pct">68%</span>
    </div>
  </div>

  <!-- Experience -->
  <div class="section-label">Experience</div>
  <div class="timeline">
    <div class="tl-item">
      <div class="tl-dot b"></div>
      <div class="tl-date">Apr 2025 – May 2025</div>
      <div class="tl-role">Java Developer Intern</div>
      <div class="tl-co">CodSoft &nbsp;·&nbsp; Remote <span class="pill">+30% code reliability</span></div>
    </div>
    <div class="tl-item">
      <div class="tl-dot g"></div>
      <div class="tl-date">Jul 2024 – Aug 2024</div>
      <div class="tl-role">Salesforce CRM Intern</div>
      <div class="tl-co">Inno Valley Works <span class="pill">Trailhead Badges earned</span></div>
    </div>
    <div class="tl-item">
      <div class="tl-dot r"></div>
      <div class="tl-date">Jun 2024 – Jul 2024</div>
      <div class="tl-role">Web Development Intern</div>
      <div class="tl-co">Crescent Infotech <span class="pill">Full Stack Certified</span></div>
    </div>
  </div>

  <!-- Projects -->
  <div class="section-label">Featured projects</div>

  <div class="proj-card">
    <div class="proj-header">
      <div class="proj-title">
        <span class="proj-dot" style="background:#1a73e8"></span>
        Smart Health Care Insights
      </div>
      <span class="proj-badge pb-b">ML · NLP</span>
    </div>
    <div class="proj-body">
      ML-powered patient feedback analysis using TF-IDF vectorization and sentiment classification (positive / negative / neutral) in real time. Admin dashboards enable data-driven hospital quality improvement.
    </div>
    <div class="proj-tags">
      <span class="tag">Python</span><span class="tag">Flask</span><span class="tag">NLP</span>
      <span class="tag">Sentiment Analysis</span><span class="tag">TF-IDF</span><span class="tag">ML</span>
    </div>
  </div>

  <div class="proj-card">
    <div class="proj-header">
      <div class="proj-title">
        <span class="proj-dot" style="background:#34a853"></span>
        Travel Planner AI Chatbot
      </div>
      <span class="proj-badge pb-g">AI · REST</span>
    </div>
    <div class="proj-body">
      Conversational AI travel assistant with intent recognition and entity extraction. Consolidates destinations, hotel suggestions, and emergency info in one unified interface via Flask REST backend.
    </div>
    <div class="proj-tags">
      <span class="tag">Python</span><span class="tag">Flask</span><span class="tag">REST APIs</span>
      <span class="tag">AI / NLP</span><span class="tag">JSON</span>
    </div>
  </div>

  <div class="proj-card">
    <div class="proj-header">
      <div class="proj-title">
        <span class="proj-dot" style="background:#ea4335"></span>
        Railway Reservation System
      </div>
      <span class="proj-badge pb-r">Java · DB</span>
    </div>
    <div class="proj-body">
      Full-featured booking platform covering auth, seat lookup, scheduling, and cancellation. Swing GUI frontend with DAO pattern + MVC-inspired architecture and normalized MySQL schema.
    </div>
    <div class="proj-tags">
      <span class="tag">Java</span><span class="tag">MySQL</span><span class="tag">JDBC</span>
      <span class="tag">Swing GUI</span><span class="tag">OOP</span><span class="tag">MVC</span>
    </div>
  </div>

  <div class="proj-card">
    <div class="proj-header">
      <div class="proj-title">
        <span class="proj-dot" style="background:#fbbc04"></span>
        Library Management System
      </div>
      <span class="proj-badge pb-y">Java · RBAC</span>
    </div>
    <div class="proj-body">
      Comprehensive library platform with book cataloguing, member registration, borrowing workflows, overdue fine calculation, and secure role-based access control for admin vs. member portals.
    </div>
    <div class="proj-tags">
      <span class="tag">Java</span><span class="tag">MySQL</span><span class="tag">JDBC</span>
      <span class="tag">OOP</span><span class="tag">Role-Based Auth</span>
    </div>
  </div>

  <!-- Achievements -->
  <div class="section-label">Achievements</div>
  <div class="cards">
    <div class="card">
      <div class="card-icon ci-b"><i class="ti ti-trophy" aria-hidden="true"></i></div>
      <h3>SIH 2023 — Top Team</h3>
      <p>Smart India Hackathon internal selection — national Govt. of India innovation challenge</p>
    </div>
    <div class="card">
      <div class="card-icon ci-y"><i class="ti ti-award" aria-hidden="true"></i></div>
      <h3>Proficiency Award</h3>
      <p>Academic excellence — DRMCET, 2022–23 academic year</p>
    </div>
    <div class="card">
      <div class="card-icon ci-g"><i class="ti ti-certificate" aria-hidden="true"></i></div>
      <h3>4 Certifications</h3>
      <p>Full Stack · Responsive Web · Salesforce Trailhead · Java OOP</p>
    </div>
    <div class="card">
      <div class="card-icon ci-r"><i class="ti ti-code" aria-hidden="true"></i></div>
      <h3>LeetCode + GFG</h3>
      <p>Active DSA practice — Arrays, Trees, Dynamic Programming, Graphs</p>
    </div>
  </div>

  <!-- Tech stack -->
  <div class="section-label">Full tech stack</div>
  <div class="badge-grid">
    <span class="badge filled-b"><i class="ti ti-coffee" style="font-size:13px" aria-hidden="true"></i> Java</span>
    <span class="badge filled-r"><i class="ti ti-bolt" style="font-size:13px" aria-hidden="true"></i> Spring Boot</span>
    <span class="badge filled-g"><i class="ti ti-brand-python" style="font-size:13px" aria-hidden="true"></i> Python</span>
    <span class="badge filled-y"><i class="ti ti-cloud" style="font-size:13px" aria-hidden="true"></i> AWS</span>
    <span class="badge out"><i class="ti ti-database" style="font-size:13px" aria-hidden="true"></i> MySQL</span>
    <span class="badge out"><i class="ti ti-api" style="font-size:13px" aria-hidden="true"></i> REST APIs</span>
    <span class="badge out"><i class="ti ti-brand-javascript" style="font-size:13px" aria-hidden="true"></i> JavaScript</span>
    <span class="badge out"><i class="ti ti-server" style="font-size:13px" aria-hidden="true"></i> Flask</span>
    <span class="badge out"><i class="ti ti-brand-nodejs" style="font-size:13px" aria-hidden="true"></i> Node.js</span>
    <span class="badge out"><i class="ti ti-brand-git" style="font-size:13px" aria-hidden="true"></i> Git</span>
    <span class="badge out">Salesforce CRM</span>
    <span class="badge out">Odoo ERP</span>
    <span class="badge out"><i class="ti ti-brand-html5" style="font-size:13px" aria-hidden="true"></i> HTML5</span>
    <span class="badge out"><i class="ti ti-brand-css3" style="font-size:13px" aria-hidden="true"></i> CSS3</span>
    <span class="badge out">JDBC</span>
    <span class="badge out">JUnit</span>
    <span class="badge out">Swing GUI</span>
    <span class="badge out">CI / CD</span>
  </div>

  <!-- Currently Learning -->
  <div class="section-label" style="margin-top:1.25rem">Currently learning</div>
  <div class="learn-panel">
    <div class="learn-header">
      <span class="dot" style="background:#ea4335"></span>
      <span class="dot" style="background:#fbbc04"></span>
      <span class="dot" style="background:#34a853"></span>
      &nbsp; roadmap_2025.json
    </div>
    <div class="learn-body">
      <span class="kw">const</span> roadmap = {<br>
      &nbsp;&nbsp;<span class="str">"System Design"</span>: <span class="arr">→</span> <span class="cm">Distributed Systems, Load Balancing, CAP Theorem</span>,<br>
      &nbsp;&nbsp;<span class="str">"Containerization"</span>: <span class="arr">→</span> <span class="cm">Docker, Kubernetes, Helm, Service Mesh</span>,<br>
      &nbsp;&nbsp;<span class="str">"Advanced AWS"</span>: <span class="arr">→</span> <span class="cm">RDS, CloudFormation, IAM, VPC, API Gateway</span>,<br>
      &nbsp;&nbsp;<span class="str">"Microservices"</span>: <span class="arr">→</span> <span class="cm">Spring Cloud, Circuit Breaker, Event Sourcing</span>,<br>
      &nbsp;&nbsp;<span class="str">"LLMs & AI"</span>: <span class="arr">→</span> <span class="cm">LangChain, RAG, Transformer Fine-tuning</span><br>
      };
    </div>
  </div>

  <!-- Education -->
  <div class="section-label">Education</div>
  <div class="cards">
    <div class="card" style="border-left:3px solid #1a73e8">
      <div class="card-icon ci-b"><i class="ti ti-school" aria-hidden="true"></i></div>
      <h3>B.E. — Computer Science & Engineering</h3>
      <p>Kumaraguru College of Engineering & Technology (KCT)<br>Coimbatore · 2025 – 2028</p>
    </div>
    <div class="card" style="border-left:3px solid #34a853">
      <div class="card-icon ci-g"><i class="ti ti-book" aria-hidden="true"></i></div>
      <h3>Diploma — Computer Science</h3>
      <p>Sakthi Polytechnic College (SIT)<br>Bhavani Appakudal, TN · 2022 – 2025</p>
    </div>
  </div>

  <!-- Contact -->
  <div class="section-label">Contact</div>
  <div class="contact-row">
    <a class="contact-card" href="mailto:adhicse005@email.com" style="text-decoration:none;color:inherit">
      <i class="ti ti-mail" aria-hidden="true"></i>
      <div><div class="c-label">Email</div><div class="c-val">adhicse005@email.com</div></div>
    </a>
    <a class="contact-card" href="https://linkedin.com/in/adhithya-k-390780292" target="_blank" style="text-decoration:none;color:inherit">
      <i class="ti ti-brand-linkedin" aria-hidden="true"></i>
      <div><div class="c-label">LinkedIn</div><div class="c-val">adhithya-k-390780292</div></div>
    </a>
    <a class="contact-card" href="https://github.com/adhithya-k" target="_blank" style="text-decoration:none;color:inherit">
      <i class="ti ti-brand-github" aria-hidden="true"></i>
      <div><div class="c-label">GitHub</div><div class="c-val">adhithya-k</div></div>
    </a>
  </div>

  <!-- Footer -->
  <div class="footer">
    <div style="display:flex;align-items:baseline;gap:0">
      <div class="google-logo" style="font-size:16px">
        <span class="gl gb">G</span><span class="gl go">o</span><span class="gl gy">o</span>
        <span class="gl gg">g</span><span class="gl glb">l</span><span class="gl ge">e</span>
      </div>
      <span class="nav-sub" style="font-size:12px">Developer Profile &nbsp;·&nbsp; Adhithya K &nbsp;·&nbsp; 2025</span>
    </div>
    <div class="footer-links">
      <a href="https://github.com/adhithya-k" target="_blank"><i class="ti ti-brand-github" style="font-size:13px" aria-hidden="true"></i> GitHub</a>
      <a href="https://linkedin.com/in/adhithya-k-390780292" target="_blank"><i class="ti ti-brand-linkedin" style="font-size:13px" aria-hidden="true"></i> LinkedIn</a>
      <a href="mailto:adhicse005@email.com"><i class="ti ti-mail" style="font-size:13px" aria-hidden="true"></i> Email</a>
    </div>
  </div>

</div>

<script>
  window.addEventListener('load', () => {
    setTimeout(() => {
      document.querySelectorAll('.prog-bar').forEach(bar => {
        bar.style.width = bar.dataset.w + '%'
      })
    }, 300)
  })
</script>

</body>
</html>
