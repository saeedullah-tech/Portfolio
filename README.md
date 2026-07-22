<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Saeed Ullah — Data & BI Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EEF0EA;
    --paper-deep:#E4E7DE;
    --line:#C9CFC0;
    --line-soft:#DADFD1;
    --ink:#161F17;
    --ink-soft:#4C5750;
    --ink-faint:#8A937F;
    --card:#F7F8F3;
    --gold:#C8871F;
    --gold-soft:#E9C889;
    --blue:#2C4A72;
    --blue-soft:#7C9CC0;
    --red-stamp:#9B3B2E;
    --serif:"Fraunces","Georgia",serif;
    --sans:"Inter","Segoe UI",system-ui,-apple-system,sans-serif;
    --mono:"JetBrains Mono","SFMono-Regular",Consolas,monospace;
  }

  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:
      repeating-linear-gradient(to bottom, transparent, transparent 35px, rgba(20,26,20,0.035) 35px, rgba(20,26,20,0.035) 36px),
      var(--paper);
    color:var(--ink);
    font-family:var(--sans);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  a{color:inherit; text-decoration:none;}
  ::selection{ background:var(--gold-soft); color:var(--ink); }
  img{max-width:100%; display:block;}

  .wrap{ max-width:1040px; margin:0 auto; padding:0 30px; }

  .reveal{ opacity:0; transform:translateY(14px); transition:opacity .6s ease, transform .6s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  a:focus-visible, button:focus-visible, summary:focus-visible{
    outline:2px solid var(--gold); outline-offset:3px; border-radius:2px;
  }

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:50;
    background:rgba(238,240,234,0.9);
    backdrop-filter: blur(8px);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{ display:flex; align-items:center; justify-content:space-between; height:66px; }
  .brand{ display:flex; align-items:center; gap:10px; font-family:var(--serif); font-weight:600; font-size:18px; }
  .stamp{
    width:32px; height:32px; border-radius:50%; border:1.5px solid var(--ink);
    display:flex; align-items:center; justify-content:center;
    font-family:var(--mono); font-size:11px; font-weight:700; letter-spacing:.02em;
    transform:rotate(-6deg);
  }
  .navlinks{ display:flex; align-items:center; gap:26px; font-family:var(--mono); font-size:12.5px; color:var(--ink-soft); }
  .navlinks a{ transition:color .2s; border-bottom:1px solid transparent; padding-bottom:2px; }
  .navlinks a:hover{ color:var(--ink); border-color:var(--gold); }
  .navlinks .cta{
    background:var(--ink); color:var(--paper); padding:8px 15px; border-radius:3px;
    letter-spacing:.03em;
  }
  .navlinks .cta:hover{ background:var(--blue); }
  @media (max-width:720px){ .navlinks a:not(.cta){ display:none; } }

  /* ---------- HERO ---------- */
  header.hero{ padding:76px 0 0; }
  .eyebrow{
    font-family:var(--mono); font-size:12px; letter-spacing:.1em; text-transform:uppercase;
    color:var(--gold); margin-bottom:20px; display:flex; align-items:center; gap:8px;
  }
  .eyebrow .cellref{
    border:1px solid var(--line); background:var(--card); padding:2px 7px; border-radius:2px; color:var(--ink-soft);
  }
  h1{
    font-family:var(--serif); font-weight:600; font-size:clamp(38px,6vw,66px);
    letter-spacing:-0.01em; line-height:1.04; color:var(--ink);
  }
  h1 em{ font-style:italic; font-weight:500; color:var(--blue); }

  .role-line{ margin-top:22px; font-size:17px; color:var(--ink-soft); max-width:600px; }
  .role-line strong{ color:var(--ink); font-weight:600; }

  /* formula bar */
  .fx-bar{
    margin-top:36px; display:flex; align-items:center; gap:0;
    border:1px solid var(--line); background:var(--card); border-radius:5px; overflow:hidden;
    max-width:600px;
  }
  .fx-label{
    font-family:var(--mono); font-size:12.5px; color:var(--ink-faint); background:var(--paper-deep);
    padding:11px 14px; border-right:1px solid var(--line); font-weight:600;
  }
  .fx-text{
    font-family:var(--mono); font-size:13.5px; color:var(--blue); padding:11px 14px; flex:1;
    white-space:nowrap; overflow:hidden;
  }
  .fx-text .cursor{ display:inline-block; width:7px; height:14px; background:var(--gold); margin-left:2px; vertical-align:-2px; animation:blink 1s step-end infinite; }
  @keyframes blink{ 50%{ opacity:0; } }

  .hero-tags{ margin-top:28px; display:flex; flex-wrap:wrap; gap:8px; }
  .htag{
    font-family:var(--mono); font-size:12px; color:var(--ink-soft);
    border:1px solid var(--line); padding:5px 11px; border-radius:20px; background:var(--card);
  }

  /* ledger metric row */
  .ledger-row{ margin-top:52px; border:1px solid var(--line); border-radius:6px; overflow:hidden; }
  .ledger-head{
    display:grid; grid-template-columns:56px repeat(4,1fr); background:var(--paper-deep);
    font-family:var(--mono); font-size:11px; color:var(--ink-faint); letter-spacing:.06em;
  }
  .ledger-head div{ padding:8px 14px; border-right:1px solid var(--line); }
  .ledger-head div:last-child{ border-right:none; }
  .ledger-body{ display:grid; grid-template-columns:56px repeat(4,1fr); background:var(--card); }
  .ledger-body .rownum{
    display:flex; align-items:center; justify-content:center; font-family:var(--mono);
    font-size:12px; color:var(--ink-faint); border-right:1px solid var(--line);
  }
  .lcell{ padding:20px 14px; border-right:1px solid var(--line); }
  .lcell:last-child{ border-right:none; }
  .lcell .num{ font-family:var(--mono); font-size:24px; font-weight:700; color:var(--ink); }
  .lcell .lab{ font-size:12px; color:var(--ink-soft); margin-top:5px; }
  @media (max-width:720px){
    .ledger-head{ display:none; }
    .ledger-body{ grid-template-columns:1fr; }
    .ledger-body .rownum{ display:none; }
    .lcell{ border-right:none; border-bottom:1px solid var(--line); }
    .lcell:last-child{ border-bottom:none; }
  }

  /* ---------- SECTION SCAFFOLD ---------- */
  section{ padding:80px 0; border-bottom:1px solid var(--line); }
  .section-head{ display:flex; align-items:baseline; justify-content:space-between; margin-bottom:40px; gap:16px; }
  .section-head h2{ font-family:var(--serif); font-size:30px; font-weight:600; letter-spacing:-0.01em; }
  .section-tag{ font-family:var(--mono); font-size:11.5px; color:var(--ink-faint); letter-spacing:.06em; text-transform:uppercase; }

  /* ---------- ABOUT ---------- */
  .about-grid{ display:grid; grid-template-columns:1.25fr 1fr; gap:52px; }
  .about-grid p{ color:var(--ink-soft); font-size:15.5px; margin-bottom:15px; }
  .about-grid p strong{ color:var(--ink); font-weight:600; }
  .keyfacts{ border:1px solid var(--line); border-radius:6px; overflow:hidden; background:var(--card); }
  .kf-row{ display:grid; grid-template-columns:52px 1fr; border-bottom:1px solid var(--line-soft); }
  .kf-row:last-child{ border-bottom:none; }
  .kf-cell{
    font-family:var(--mono); font-size:11.5px; color:var(--ink-faint); background:var(--paper-deep);
    display:flex; align-items:center; justify-content:center; border-right:1px solid var(--line-soft);
  }
  .kf-val{ padding:13px 16px; font-size:13.5px; color:var(--ink-soft); }
  .kf-val strong{ color:var(--ink); font-weight:600; }
  @media (max-width:820px){ .about-grid{ grid-template-columns:1fr; } }

  /* ---------- SKILLS ---------- */
  .skills-grid{ display:grid; grid-template-columns:1fr 1fr 1fr; gap:36px; margin-top:60px; }
  .skill-col-head{
    font-family:var(--mono); font-size:11.5px; letter-spacing:.08em; text-transform:uppercase;
    color:var(--gold); margin-bottom:16px; padding-bottom:10px; border-bottom:1px solid var(--line);
  }
  .tag-cloud{ display:flex; flex-wrap:wrap; gap:8px; }
  .tag{
    font-size:12.5px; color:var(--ink-soft); background:var(--card);
    border:1px solid var(--line); padding:6px 12px; border-radius:3px; transition:.2s;
  }
  .tag:hover{ border-color:var(--gold); color:var(--ink); }
  @media (max-width:920px){ .skills-grid{ grid-template-columns:1fr 1fr; } }
  @media (max-width:620px){ .skills-grid{ grid-template-columns:1fr; } }

  /* ---------- PROJECTS ---------- */
  .ptable{ border:1px solid var(--line); border-radius:6px; overflow:hidden; }
  details.project{ border-bottom:1px solid var(--line); background:var(--card); }
  details.project:last-of-type{ border-bottom:none; }
  details.project[open]{ background:#FBFBF8; }
  summary.project-sum{
    list-style:none; cursor:pointer; padding:20px 22px; display:flex; align-items:center;
    justify-content:space-between; gap:16px; flex-wrap:wrap;
  }
  summary.project-sum::-webkit-details-marker{ display:none; }
  .psum-left{ display:flex; align-items:baseline; gap:14px; flex-wrap:wrap; }
  .project h3{ font-family:var(--serif); font-size:19px; font-weight:600; color:var(--ink); }
  .project h3 a{ border-bottom:1px solid transparent; }
  .project h3 a:hover{ border-color:var(--gold); }
  .tools{
    font-family:var(--mono); font-size:11px; color:var(--blue);
    background:rgba(44,74,114,0.07); border:1px solid var(--blue-soft);
    padding:3px 9px; border-radius:20px; white-space:nowrap;
  }
  .chevron{ font-family:var(--mono); font-size:13px; color:var(--ink-faint); transition:transform .25s; }
  details[open] .chevron{ transform:rotate(90deg); }
  .project-body{ padding:0 22px 22px; }
  .project ul{ list-style:none; display:flex; flex-direction:column; gap:9px; margin-top:6px; }
  .project li{ color:var(--ink-soft); font-size:14.5px; padding-left:18px; position:relative; }
  .project li::before{ content:"—"; position:absolute; left:0; color:var(--gold); }

  .more-projects{ margin-top:24px; }
  .more-projects .cap{ font-family:var(--mono); font-size:11.5px; color:var(--ink-faint); margin-bottom:12px; }
  .chip-row{ display:flex; flex-wrap:wrap; gap:10px; }
  .chip{
    font-family:var(--mono); font-size:12.5px; color:var(--ink-soft); border:1px solid var(--line);
    background:var(--card); padding:8px 13px; border-radius:4px; display:flex; align-items:center; gap:6px;
  }
  .chip:hover{ border-color:var(--gold); color:var(--ink); }
  .chip::after{ content:"↗"; color:var(--ink-faint); }

  /* ---------- EXPERIENCE ---------- */
  .xp-row{ display:grid; grid-template-columns:150px 1fr; gap:24px; padding:26px 0; border-bottom:1px solid var(--line-soft); }
  .xp-row:last-child{ border-bottom:none; }
  .xp-date{ font-family:var(--mono); font-size:12px; color:var(--ink-faint); padding-top:3px; }
  .xp-body h4{ font-family:var(--serif); font-size:18px; color:var(--ink); font-weight:600; }
  .xp-body .org{ font-size:13.5px; color:var(--blue); margin-top:3px; margin-bottom:12px; font-weight:500; }
  .xp-body ul{ list-style:none; display:flex; flex-direction:column; gap:8px; }
  .xp-body li{ color:var(--ink-soft); font-size:14.5px; padding-left:16px; position:relative; }
  .xp-body li::before{ content:"—"; position:absolute; left:0; color:var(--ink-faint); }
  @media (max-width:680px){ .xp-row{ grid-template-columns:1fr; gap:6px; } }

  /* ---------- CERTS ---------- */
  .cert-grid{ display:grid; grid-template-columns:repeat(2,1fr); gap:12px; }
  .cert{
    border:1px solid var(--line); border-radius:5px; padding:14px 16px; background:var(--card);
    font-size:13.5px; color:var(--ink-soft); display:flex; align-items:center; gap:11px;
  }
  .cert .badge{
    width:20px; height:20px; border-radius:50%; border:1.4px solid var(--gold); color:var(--gold);
    font-family:var(--mono); font-size:11px; font-weight:700; display:flex; align-items:center; justify-content:center; flex-shrink:0;
  }
  @media (max-width:680px){ .cert-grid{ grid-template-columns:1fr; } }

  /* ---------- FOOTER ---------- */
  footer{ padding:76px 0 50px; }
  .footer-inner{ text-align:center; }
  footer h2{ font-family:var(--serif); font-size:34px; font-weight:600; margin-bottom:14px; }
  footer p{ color:var(--ink-soft); max-width:480px; margin:0 auto 32px; font-size:15px; }
  .contact-row{ display:flex; justify-content:center; gap:12px; flex-wrap:wrap; }
  .contact-btn{
    font-family:var(--mono); font-size:13px; padding:11px 20px; border-radius:4px;
    border:1px solid var(--line); color:var(--ink-soft); transition:.2s; background:var(--card);
  }
  .contact-btn.primary{ background:var(--ink); color:var(--paper); border-color:var(--ink); font-weight:600; }
  .contact-btn:hover{ border-color:var(--gold); color:var(--ink); }
  .contact-btn.primary:hover{ background:var(--blue); border-color:var(--blue); }
  .balance-line{
    margin-top:44px; padding-top:20px; border-top:1px dashed var(--line);
    font-family:var(--mono); font-size:11.5px; color:var(--ink-faint);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:8px;
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    .reveal{ opacity:1; transform:none; transition:none; }
    .cursor{ animation:none; }
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="brand"><span class="stamp">SU</span> Saeed Ullah</div>
    <div class="navlinks">
      <a href="#about">About</a>
      <a href="#skills">Skills &amp; Tools</a>
      <a href="#projects">Projects</a>
      <a href="#experience">Experience</a>
      <a href="#certifications">Certs</a>
      <a class="cta" href="#contact">Contact</a>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <div class="eyebrow"><span class="cellref">A1</span> Riyadh, Saudi Arabia · Open to Data &amp; BI roles</div>
    <h1>Saeed Ullah<br>turns raw tables into <em>decisions.</em></h1>
    <p class="role-line">
      Computer Science graduate working across <strong>SQL, Power BI, Python, and Excel</strong> — building
      dashboards, cleaning messy datasets, and writing reports that hold up under scrutiny.
    </p>

    <div class="fx-bar">
      <div class="fx-label">fx</div>
      <div class="fx-text" id="fxText"></div>
    </div>

    <div class="hero-tags">
      <span class="htag">Data Analyst</span>
      <span class="htag">Reporting Analyst</span>
      <span class="htag">BI Analyst</span>
      <span class="htag">Power BI Developer</span>
      <span class="htag">Operations Analyst</span>
    </div>

    <div class="ledger-row reveal">
      <div class="ledger-head">
        <div>Row</div><div>A</div><div>B</div><div>C</div><div>D</div>
      </div>
      <div class="ledger-body">
        <div class="rownum">1</div>
        <div class="lcell"><div class="num">25</div><div class="lab">end-to-end analytics &amp; BI projects</div></div>
        <div class="lcell"><div class="num">9</div><div class="lab">data &amp; BI certifications</div></div>
        <div class="lcell"><div class="num">3</div><div class="lab">tools in daily use: SQL, Power BI, Excel</div></div>
      </div>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-head reveal">
      <h2>About</h2>
      <span class="section-tag">Cell A1:D6</span>
    </div>
    <div class="about-grid">
      <div class="reveal">
        <p>I'm Saeed Ullah, a <strong>Data Analyst</strong> with a Bachelor's degree in Computer Science who enjoys
        transforming raw data into actionable business insights. I have hands-on experience with
        <strong>SQL, Python, Power BI, Excel, Tableau, PostgreSQL, and R</strong>, specializing in data cleaning,
        exploratory data analysis, interactive dashboard development, reporting, and business intelligence.</p>
        <p>This portfolio showcases projects built using real-world datasets across <strong>sales, HR, finance, and
        business operations</strong>. Each project demonstrates my ability to clean and analyze data, write
        efficient SQL queries, automate workflows with Python, and develop dashboards that support
        data-driven decision-making.</p>
        <p>I'm committed to continuous learning and actively seeking opportunities to help organizations solve
        business challenges through <strong>data analytics, reporting, and visualization</strong>.</p>
      </div>
      <div class="keyfacts reveal">
        <div class="kf-row"><div class="kf-cell">A2</div><div class="kf-val"><strong>Query</strong> — SQL: joins, aggregations, subqueries, extraction</div></div>
        <div class="kf-row"><div class="kf-cell">A3</div><div class="kf-val"><strong>Model</strong> — PostgreSQL, MySQL, data modeling</div></div>
        <div class="kf-row"><div class="kf-cell">A4</div><div class="kf-val"><strong>Visualize</strong> — Power BI, Tableau, Excel dashboards</div></div>
        <div class="kf-row"><div class="kf-cell">A5</div><div class="kf-val"><strong>Clean</strong> — Power Query, data validation, ETL</div></div>
        <div class="kf-row"><div class="kf-cell">A6</div><div class="kf-val"><strong>Speak</strong> — English (fluent), Arabic (intermediate), Urdu (native)</div></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-head reveal">
      <h2>Skills &amp; Tools</h2>
      <span class="section-tag">Cell B1:C9</span>
    </div>
    <div class="skills-grid">
      <div class="reveal">
        <div class="skill-col-head">Languages &amp; Platforms</div>
        <div class="tag-cloud">
          <span class="tag">SQL (PostgreSQL)</span>
          <span class="tag">PostgreSQL &amp; pgAdmin 4</span>
          <span class="tag">Python (Pandas, NumPy, Matplotlib, Seaborn)</span>
          <span class="tag">Microsoft Power BI</span>
          <span class="tag">Microsoft Excel (Power Query, Pivot Tables, Advanced Formulas)</span>
          <span class="tag">Tableau</span>
          <span class="tag">R Programming</span>
        </div>
      </div>
      <div class="reveal">
        <div class="skill-col-head">Tools</div>
        <div class="tag-cloud">
          <span class="tag">Power BI</span>
          <span class="tag">Tabluea</span>
          <span class="tag">R Studio</span>
          <span class="tag">Jupyter Notebook</span>
          <span class="tag">Visual Studio Code</span>
          <span class="tag">Microsoft Office Suite</span>
          <span class="tag">pgAdmin 4</span>
          <span class="tag">Power Query</span>
          <span class="tag">GitHub</span>
        </div>
      </div>
      <div class="reveal">
        <div class="skill-col-head">Analytical Skills</div>
        <div class="tag-cloud">
          <span class="tag">Data Cleaning &amp; Data Transformation</span>
          <span class="tag">Exploratory Data Analysis (EDA)</span>
          <span class="tag">Statistical Analysis</span>
          <span class="tag">ETL Concepts</span>
          <span class="tag">Data Modeling</span>
          <span class="tag">Database Management</span>
          <span class="tag">Dashboard Development</span>
          <span class="tag">Data Visualization</span>
          <span class="tag">KPI Development &amp; Performance Reporting</span>
          <span class="tag">Business Intelligence &amp; Reporting</span>
          <span class="tag">Trend &amp; Variance Analysis</span>
        </div>
      </div>
      <div class="reveal" style="grid-column:1 / -1;">
        <div class="skill-col-head">Professional Skills</div>
        <div class="tag-cloud">
          <span class="tag">Problem Solving</span>
          <span class="tag">Analytical Thinking</span>
          <span class="tag">Attention to Detail</span>
          <span class="tag">Communication Skills</span>
          <span class="tag">Documentation</span>
          <span class="tag">Team Collaboration</span>
          <span class="tag">Time Management</span>
          <span class="tag">Continuous Learning</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head reveal">
      <h2>Projects</h2>
      <span class="section-tag">Cell C1:C14 — click a row to expand</span>
    </div>

    <div class="ptable reveal">
     <details class="project" open>
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/REAL-ESTATE-dashboard" target="_blank">European Real Estate Market & Pricing Analytics Dashboard</a></h3>
            <span class="tools">Power BI · DAX · Data Modeling · Bing Maps</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Built an interactive Power BI dashboard analyzing 5,000+ property listings across 10 major European cities to surface pricing, growth, and compliance risk patterns hidden in traditional reports.</li>
            <li>Designed DAX measures — Price Growth %, Price per m², Days on Market, Market Speed Classification, and Premium Amenities Score — to quantify property performance and market velocity.</li>
            <li>Built a pricing risk model classifying listings as Overpriced, Below District Average, or Normal, giving stakeholders visibility into risk exposure by property domain and listing owner.</li>
            <li>Integrated geographic map visuals to track price growth by city and country, supporting location-driven investment and pricing decisions.</li>
            <li>Delivered a multi-page executive dashboard linking data quality and compliance to pricing outcomes, supporting reduced holding costs and improved listing accuracy.</li>
          </ul>
        </div>
      </details>
      <details class="project" open>
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/netflixSQL-project" target="_blank">Netflix Content Analysis — SQL</a></h3>
            <span class="tools">PostgreSQL · SQL</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Analyzed Netflix's full movies and TV shows catalog using SQL to answer 14 business questions on content distribution, ratings, and regional trends.</li>
            <li>Wrote advanced queries using window functions, array unnesting, and date parsing to break down content by country, genre, director, and cast.</li>
            <li>Built a content categorization model flagging titles by keyword sentiment (e.g., violence-related themes) to support content moderation insights.</li>
            <li>Identified the top 5 countries by content volume and ranked release years in India by average content output, surfacing regional programming trends.</li>
            <li>Documented all queries and findings in a structured GitHub repository for reproducibility and reference.</li>
          </ul>
        </div>
      </details>
          <details class="project" open>
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/excel-pivot-dashboard-project" target="_blank">Excel Sales Performance Dashboard</a></h3>
            <span class="tools">Excel · Pivot Tables · Pivot Charts · Slicers</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Built an interactive Excel dashboard using Pivot Tables and Pivot Charts to track sales performance, order status, and customer demographics across regions.</li>
            <li>Designed monthly sales trend visuals to surface seasonality and identify high and low performing periods.</li>
            <li>Broke down order status (Delivered, Cancelled, Returned, Refunded) to highlight fulfillment issues affecting revenue.</li>
            <li>Segmented customer data by gender, age group, and state to identify top-performing markets and sales channels.</li>
            <li>Added interactive slicers for Month, Status, and Channel, enabling stakeholders to filter insights without technical support.</li>
          </ul>
        </div>
      </details>

      <details class="project">
        <summary class="project-sum">
          <div class="psum-left">
            <h3>Payroll Automation Workbook</h3>
            <span class="tools">Excel · Power Query</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Built a formula-driven workbook to automate bi-weekly payroll calculations, replacing manual line-by-line computation.</li>
            <li>Added validation rules on input sheets to catch data-entry errors — missing hours, rate mismatches — before final calculation.</li>
            <li>Reduced average payroll-cycle processing time through reusable formulas and a standardized template.</li>
          </ul>
        </div>
      </details>

      <details class="project">
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/Saudi-Job-Market-Analysis-Bayt.com-Dataset" target="_blank">Saudi Job Market Analysis</a></h3>
            <span class="tools">SQL · Power BI</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Structured job-posting data across roles, sectors, and locations in the Saudi market into a relational format for analysis.</li>
            <li>Used SQL to surface trends in in-demand skills, role frequency, and sector concentration.</li>
            <li>Visualized which technical skills appeared most often across analytics and BI postings.</li>
          </ul>
        </div>
      </details>

      <details class="project">
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/Sales_Analysis" target="_blank">Python Diwali Sales Analysis</a></h3>
            <span class="tools">Python · Pandas · NumPy · Seaborn</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Cleaned and analyzed 11,000+ festive-season retail transactions, resolving missing values and data type issues to produce a reliable 11,239-record dataset.</li>
            <li>Built demographic and regional segmentation with Pandas groupby aggregations, uncovering a 70/30 revenue split by gender and identifying top-performing states, occupations, and product categories.</li>
            <li>Visualized purchasing patterns with Seaborn to define a clear target customer profile.</li>
          </ul>
        </div>
      </details>
      <details class="project" open>
        <summary class="project-sum">
          <div class="psum-left">
            <h3><a href="https://github.com/saeedullah-tech/Mobile-Sales-Dashboard" target="_blank">Mobile Sales Performance Dashboard</a></h3>
            <span class="tools">Power BI · DAX · Data Modeling</span>
          </div>
          <span class="chevron">▸</span>
        </summary>
        <div class="project-body">
          <ul>
            <li>Built an interactive Power BI dashboard analyzing 4,000+ transactions to track mobile sales performance across cities, brands, and time periods.</li>
            <li>Designed DAX measures for MTD sales, average price, and quantity aggregations, consolidating KPIs into a single real-time reporting view.</li>
            <li>Built a geographic map visual identifying top-performing cities (Delhi, Mumbai, Bangalore), directing regional sales and marketing focus.</li>
            <li>Analyzed brand and product-level performance across Apple, Samsung, OnePlus, and Vivo to surface best-selling models and revenue drivers.</li>
            <li>Incorporated customer rating and payment method analysis, linking product satisfaction data to purchasing behavior for retention.</li></ul>
            </div>
            </details>
    </div>

    <div class="more-projects reveal">
      <div class="cap">More on GitHub — Cell C15:C22</div>
      <div class="chip-row">
        <a class="chip" href="https://github.com/saeedullah-tech/powerbi-car-sales-dashboard" target="_blank">Power BI Car Sales Dashboard</a>
        <a class="chip" href="https://github.com/saeedullah-tech/Credit-Card-Fraud-Risk-Analysis" target="_blank">Credit Card Fraud Risk Analysis</a>
        <a class="chip" href="https://github.com/saeedullah-tech/excel-pivot-dashboard-project" target="_blank">Excel Pivot Dashboard</a>
        <a class="chip" href="https://github.com/saeedullah-tech/Pizza-Sales-Analysis" target="_blank">Pizza Sales Analysis</a>
        <a class="chip" href="https://github.com/saeedullah-tech/Library-Management-System-" target="_blank">Library Management System</a>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <div class="section-head reveal">
      <h2>Experience</h2>
      <span class="section-tag">Cell D1:D2</span>
    </div>

    <div class="reveal">
      <div class="xp-row">
        <div class="xp-date">Mar 2026 — Present</div>
        <div class="xp-body">
          <h4>Data &amp; Operations Associate</h4>
          <div class="org">Travel &amp; Visa Services Agency, Riyadh</div>
          <ul>
            <li>Maintain operational trackers across visa applications, client bookings, and case status with high daily transaction volume.</li>
            <li>Consolidate data from multiple intake sources into recurring management reports.</li>
            <li>Standardized reporting templates in Excel, cutting time spent assembling weekly updates.</li>
          </ul>
        </div>
      </div>

      <div class="xp-row">
        <div class="xp-date">Mar 2024 — Sep 2025</div>
        <div class="xp-body">
          <h4>Document Controller</h4>
          <div class="org">[Company Name], Pakistan</div>
          <ul>
            <li>Maintained and organized project documentation, records, and correspondence in line with company and client standards.</li>
            <li>Tracked document submission, review, and approval cycles across multiple departments and stakeholders.</li>
            <li>Implemented a structured filing and version-control system, improving document retrieval and reducing duplication errors.</li>
            <li>Maintained accurate logs and registers to support audit readiness and reporting requirements.</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="certifications">
  <div class="wrap">
    <div class="section-head reveal">
      <h2>Certifications</h2>
      <span class="section-tag">Cell E1:E8</span>
    </div>
    <div class="cert-grid reveal">
      <div class="cert"><span class="badge">✓</span> Microsoft Power BI</div>
      <div class="cert"><span class="badge">✓</span> Advanced Microsoft Excel</div>
      <div class="cert"><span class="badge">✓</span> SQL &amp; MySQL for Data Analysis</div>
      <div class="cert"><span class="badge">✓</span> Data Analytics with Python</div>
      <div class="cert"><span class="badge">✓</span> Data Analytics &amp; Business Intelligence Training</div>
      <div class="cert"><span class="badge">✓</span> Introduction to Finance &amp; Accounting</div>
      <div class="cert"><span class="badge">✓</span> Front-End Web Development</div>
      <div class="cert"><span class="badge">✓</span> Soft Skills Training</div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap footer-inner reveal">
    <h2>Let's talk data.</h2>
    <p>Open to Data Analyst, Reporting Analyst, BI Analyst, Operations Analyst, and entry-level Business
    Analyst roles across Saudi Arabia. Based in Riyadh with a transferable Iqama.</p>
    <div class="contact-row">
      <a class="contact-btn primary" href="mailto:Saeedtech990@gmail.com">Saeedtech990@gmail.com</a>
      <a class="contact-btn" href="https://www.linkedin.com/in/saeed-ullah-83806a3a8" target="_blank" rel="noopener">LinkedIn</a>
      <a class="contact-btn" href="https://github.com/saeedullah-tech" target="_blank" rel="noopener">GitHub</a>
    </div>
    <div class="balance-line">
      <span>© 2026 Saeed Ullah — Riyadh, Saudi Arabia</span>
      <span>Status: Open to opportunities</span>
    </div>
  </div>
</footer>

<script>
  // formula bar cycling
  const formulas = [
    { fx: '=JOIN(SQL, "Power BI", Python, Excel)', out: '→ Data Analyst' },
    { fx: '=CLEAN(raw_data) → dashboard', out: '→ Reporting Analyst' },
    { fx: '=VLOOKUP("root cause", data!A:Z)', out: '→ BI Analyst' },
    { fx: '=SUM(49000, 25, 9) & " wins"', out: '→ Operations Analyst' }
  ];
  const el = document.getElementById('fxText');
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  function typeLoop(){
    if(reduceMotion){ el.textContent = formulas[0].fx + '  ' + formulas[0].out; return; }
    let i = 0;
    const step = () => {
      const item = formulas[i % formulas.length];
      const full = item.fx;
      let pos = 0;
      el.innerHTML = '';
      const typer = setInterval(() => {
        pos++;
        el.innerHTML = full.slice(0, pos) + '<span class="cursor"></span>';
        if(pos >= full.length){
          clearInterval(typer);
          setTimeout(() => {
            el.innerHTML = full + '  <span style="color:var(--gold)">' + item.out + '</span><span class="cursor"></span>';
            setTimeout(() => { i++; step(); }, 1800);
          }, 250);
        }
      }, 28);
    };
    step();
  }
  typeLoop();

  // scroll reveal
  const items = document.querySelectorAll('.reveal');
  if('IntersectionObserver' in window && !reduceMotion){
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => { if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
    }, { threshold: 0.12 });
    items.forEach(it => io.observe(it));
  } else {
    items.forEach(it => it.classList.add('in'));
  }
</script>

</body>
</html>
