<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Raajiv | Data Analyst & Data Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=DM+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg: #0d1117;
  --bg2: #161b22;
  --bg3: #21262d;
  --border: #30363d;
  --text: #e6edf3;
  --muted: #8b949e;
  --accent: #58a6ff;
  --green: #3fb950;
  --purple: #bc8cff;
  --orange: #f78166;
  --yellow: #e3b341;
  --mono: 'JetBrains Mono', monospace;
  --sans: 'DM Sans', sans-serif;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { background: var(--bg); color: var(--text); font-family: var(--sans); line-height: 1.6; }
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: var(--bg); }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }

nav {
  position: sticky; top: 0; z-index: 100;
  background: rgba(13,17,23,0.94); backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 48px; height: 60px;
}
.nav-brand { font-family: var(--mono); font-size: 15px; color: var(--accent); }
.nav-links { display: flex; gap: 4px; }
.nav-links a {
  padding: 6px 14px; border-radius: 6px; font-size: 14px; font-weight: 500;
  color: var(--muted); text-decoration: none; transition: all 0.15s;
}
.nav-links a:hover { color: var(--text); background: var(--bg3); }

.page { max-width: 900px; margin: 0 auto; padding: 52px 24px 80px; }

/* PROFILE */
.profile-card {
  display: flex; gap: 32px; align-items: flex-start;
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 12px; padding: 36px; margin-bottom: 24px;
  position: relative; overflow: hidden;
}
.profile-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
  background: linear-gradient(90deg, var(--accent) 0%, var(--purple) 50%, var(--green) 100%);
}
.avatar {
  width: 88px; height: 88px; border-radius: 50%; flex-shrink: 0;
  background: linear-gradient(135deg, var(--accent), var(--purple));
  display: flex; align-items: center; justify-content: center;
  font-size: 32px; font-weight: 700; color: #fff;
  border: 3px solid var(--border);
}
.profile-info { flex: 1; }
.profile-name { font-size: 26px; font-weight: 700; margin-bottom: 3px; }
.profile-handle { font-family: var(--mono); font-size: 13px; color: var(--muted); margin-bottom: 12px; }
.badge-work {
  display: inline-flex; align-items: center; gap: 6px;
  background: rgba(63,185,80,0.1); border: 1px solid rgba(63,185,80,0.28);
  color: var(--green); font-size: 13px; font-weight: 500;
  padding: 4px 12px; border-radius: 20px; margin-bottom: 12px;
}
.dot-live { width: 7px; height: 7px; background: var(--green); border-radius: 50%; animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.4} }
.profile-bio { font-size: 15px; color: var(--muted); line-height: 1.7; margin-bottom: 16px; max-width: 540px; }
.profile-meta { display: flex; flex-wrap: wrap; gap: 14px; font-size: 13px; color: var(--muted); margin-bottom: 18px; }
.profile-meta span { display: flex; align-items: center; gap: 5px; }
.profile-meta a { color: var(--accent); text-decoration: none; }
.profile-meta a:hover { text-decoration: underline; }
.badges { display: flex; gap: 8px; flex-wrap: wrap; }
.badge-btn {
  display: inline-flex; align-items: center; gap: 7px;
  padding: 7px 14px; border-radius: 6px; font-size: 13px; font-weight: 600;
  text-decoration: none; border: 1px solid var(--border);
  color: var(--text); background: var(--bg3); transition: all 0.15s;
}
.badge-btn:hover { border-color: var(--accent); color: var(--accent); }
.badge-btn img { width: 15px; height: 15px; object-fit: contain; }

/* SECTION */
.section { margin-bottom: 32px; }
.sec-head {
  display: flex; align-items: center; gap: 10px;
  font-size: 16px; font-weight: 600;
  margin-bottom: 16px; padding-bottom: 10px;
  border-bottom: 1px solid var(--border);
}

/* SKILLS */
.skills-block { margin-bottom: 22px; }
.skills-label { font-family: var(--mono); font-size: 12px; color: var(--muted); letter-spacing: 0.07em; text-transform: uppercase; margin-bottom: 12px; }
.skill-icons { display: flex; flex-wrap: wrap; gap: 10px; }
.sic {
  display: flex; flex-direction: column; align-items: center; gap: 7px;
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 10px; padding: 14px 16px; min-width: 80px;
  transition: border-color 0.15s, transform 0.15s;
}
.sic:hover { border-color: var(--accent); transform: translateY(-3px); }
.sic img { width: 38px; height: 38px; object-fit: contain; }
.sic .sic-svg { width: 38px; height: 38px; }
.sic span { font-size: 11px; font-weight: 600; color: var(--muted); text-align: center; font-family: var(--mono); }

/* EXPERIENCE */
.exp-card {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 10px; padding: 24px 26px;
  display: flex; gap: 18px;
}
.exp-logo {
  width: 44px; height: 44px; border-radius: 8px; flex-shrink: 0;
  background: linear-gradient(135deg, #7B5EA7, #4A90D9);
  display: flex; align-items: center; justify-content: center;
  font-size: 20px; font-weight: 800; color: white;
}
.exp-role { font-size: 15px; font-weight: 700; margin-bottom: 2px; }
.exp-company { font-size: 14px; color: var(--accent); font-weight: 600; margin-bottom: 4px; }
.exp-period { font-size: 12px; color: var(--muted); font-family: var(--mono); margin-bottom: 10px; }
.exp-desc { font-size: 14px; color: var(--muted); line-height: 1.65; }

/* CERTS */
.certs-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
.cert-card {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 10px; padding: 18px 20px;
  text-decoration: none; color: inherit;
  display: flex; align-items: flex-start; gap: 14px;
  transition: border-color 0.15s, transform 0.15s;
}
.cert-card:hover { border-color: var(--accent); transform: translateY(-2px); }
.cert-icon { font-size: 26px; flex-shrink: 0; line-height: 1; margin-top: 2px; }
.cert-name { font-size: 14px; font-weight: 600; line-height: 1.4; color: var(--text); margin-bottom: 4px; }
.cert-issuer { font-size: 12px; color: var(--muted); margin-bottom: 8px; }
.cert-view { display: inline-flex; align-items: center; gap: 4px; font-size: 12px; font-family: var(--mono); color: var(--accent); font-weight: 600; }
.cert-arrow { transition: transform 0.15s; display: inline-block; }
.cert-card:hover .cert-arrow { transform: translateX(3px); }

/* PROJECT */
.proj-card {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 10px; padding: 24px 26px;
}
.proj-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 12px; margin-bottom: 10px; }
.proj-title { font-size: 16px; font-weight: 700; color: var(--accent); }
.proj-links { display: flex; gap: 8px; flex-shrink: 0; }
.proj-link {
  display: inline-flex; align-items: center; gap: 5px;
  padding: 5px 12px; border-radius: 6px; font-size: 12px; font-weight: 600;
  text-decoration: none; border: 1px solid var(--border);
  color: var(--text); background: var(--bg3); transition: all 0.15s;
}
.proj-link:hover { border-color: var(--accent); color: var(--accent); }
.proj-desc { font-size: 14px; color: var(--muted); line-height: 1.65; margin-bottom: 12px; }
.proj-tags { display: flex; flex-wrap: wrap; gap: 7px; margin-bottom: 14px; }
.proj-tag { font-size: 12px; font-family: var(--mono); padding: 3px 10px; border-radius: 5px; background: var(--bg3); border: 1px solid var(--border); color: var(--muted); }
.proj-pts { list-style: none; display: flex; flex-direction: column; gap: 6px; }
.proj-pts li { font-size: 13px; color: var(--muted); display: flex; gap: 8px; }
.proj-pts li::before { content: '▸'; color: var(--accent); flex-shrink: 0; }

/* LOOKING FOR */
.look-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
.look-item {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 8px; padding: 14px 16px;
  display: flex; gap: 10px; align-items: flex-start;
  font-size: 14px; color: var(--muted);
}
.look-item .em { font-size: 16px; flex-shrink: 0; margin-top: 2px; }

footer {
  border-top: 1px solid var(--border);
  text-align: center; padding: 28px 24px;
  font-size: 13px; color: var(--muted);
}
footer a { color: var(--accent); text-decoration: none; }
footer a:hover { text-decoration: underline; }

@media(max-width: 680px) {
  .profile-card { flex-direction: column; gap: 18px; padding: 24px 18px; }
  nav { padding: 0 18px; }
  .nav-links { display: none; }
  .certs-grid, .look-grid { grid-template-columns: 1fr; }
  .proj-top { flex-direction: column; }
  .page { padding: 28px 14px 60px; }
}
</style>
</head>
<body>

<nav>
  <div class="nav-brand">raajiv / portfolio</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#experience">Experience</a>
    <a href="#certs">Certs</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<div class="page">

  <!-- PROFILE -->
  <div class="profile-card" id="about">
    <div class="avatar">RG</div>
    <div class="profile-info">
      <div class="profile-name">Raajiv</div>
      <div class="profile-handle">@Raajiv-Analyst</div>
      <div class="badge-work"><span class="dot-live"></span> Currently @ Wipro — Associate Data Analyst</div>
      <p class="profile-bio">
        Data Analyst &amp; aspiring Data Engineer passionate about turning raw data into
        meaningful insights. I build dashboards, write clean SQL, and engineer pipelines
        that support smart business decisions. Continuous learner — always levelling up.
      </p>
      <div class="profile-meta">
        <span>🏢 Wipro Limited</span>
        <span>📍 India</span>
        <span>📧 <a href="mailto:rg28@gmail.com">rg28@gmail.com</a></span>
        <span>🔗 <a href="https://www.linkedin.com/in/raajiv28/" target="_blank">linkedin.com/in/raajiv28</a></span>
      </div>
      <div class="badges">
        <a class="badge-btn" href="https://www.linkedin.com/in/raajiv28/" target="_blank">
          <img src="https://img.icons8.com/color/48/linkedin.png" alt="li"/> LinkedIn
        </a>
        <a class="badge-btn" href="mailto:rg28@gmail.com">
          <img src="https://img.icons8.com/color/48/gmail-new.png" alt="gm"/> rg28@gmail.com
        </a>
        <a class="badge-btn" href="https://github.com/Raajiv-Analyst" target="_blank">
          <img src="https://img.icons8.com/ios-glyphs/48/8b949e/github.png" alt="gh"/> GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section" id="skills">
    <div class="sec-head">🛠️ Technical Skills</div>

    <div class="skills-block">
      <div class="skills-label">// Analytics & Visualisation</div>
      <div class="skill-icons">

        <div class="sic">
          <img src="https://img.icons8.com/color/96/microsoft-excel-2019--v1.png" alt="Excel"/>
          <span>Excel</span>
        </div>

        <div class="sic">
          <img src="https://img.icons8.com/color/96/mysql-logo.png" alt="SQL"/>
          <span>SQL</span>
        </div>

        <div class="sic">
          <img src="https://img.icons8.com/color/96/python--v1.png" alt="Python"/>
          <span>Python</span>
        </div>

        <div class="sic">
          <img src="https://img.icons8.com/color/96/power-bi.png" alt="Power BI"/>
          <span>Power BI</span>
        </div>

        <div class="sic">
          <img src="https://img.icons8.com/color/96/tableau-software.png" alt="Tableau"/>
          <span>Tableau</span>
        </div>

      </div>
    </div>

    <div class="skills-block">
      <div class="skills-label">// Engineering & Cloud</div>
      <div class="skill-icons">

        <div class="sic">
          <img src="https://img.icons8.com/color/96/linux--v1.png" alt="Linux"/>
          <span>Linux</span>
        </div>

        <!-- Hadoop -->
        <div class="sic">
          <svg class="sic-svg" viewBox="0 0 38 38" xmlns="http://www.w3.org/2000/svg">
            <rect width="38" height="38" rx="8" fill="#FFC107"/>
            <text x="19" y="15" text-anchor="middle" font-size="7.5" font-weight="700" fill="#fff" font-family="sans-serif">HADOOP</text>
            <!-- elephant simplified -->
            <ellipse cx="19" cy="26" rx="9" ry="7" fill="rgba(255,255,255,0.25)"/>
            <circle cx="14" cy="23" r="4" fill="rgba(255,255,255,0.35)"/>
            <circle cx="24" cy="23" r="4" fill="rgba(255,255,255,0.35)"/>
            <circle cx="19" cy="20" r="5" fill="rgba(255,255,255,0.5)"/>
          </svg>
          <span>Hadoop</span>
        </div>

        <!-- Spark -->
        <div class="sic">
          <svg class="sic-svg" viewBox="0 0 38 38" xmlns="http://www.w3.org/2000/svg">
            <rect width="38" height="38" rx="8" fill="#E25A1C"/>
            <text x="19" y="24" text-anchor="middle" font-size="8" font-weight="700" fill="#fff" font-family="sans-serif">SPARK</text>
            <polygon points="19,4 23,14 33,14 25,20 28,30 19,24 10,30 13,20 5,14 15,14" fill="rgba(255,255,255,0.25)"/>
          </svg>
          <span>Spark</span>
        </div>

        <!-- Airflow -->
        <div class="sic">
          <svg class="sic-svg" viewBox="0 0 38 38" xmlns="http://www.w3.org/2000/svg">
            <rect width="38" height="38" rx="8" fill="#017CEE"/>
            <text x="19" y="15" text-anchor="middle" font-size="6.5" font-weight="700" fill="#fff" font-family="sans-serif">AIRFLOW</text>
            <circle cx="19" cy="26" r="7" fill="none" stroke="rgba(255,255,255,0.5)" stroke-width="2"/>
            <path d="M19 20 L19 26 L24 26" stroke="#fff" stroke-width="2" fill="none" stroke-linecap="round"/>
          </svg>
          <span>Airflow</span>
        </div>

        <!-- AWS -->
        <div class="sic">
          <img src="https://img.icons8.com/color/96/amazon-web-services.png" alt="AWS"/>
          <span>AWS</span>
        </div>

      </div>
    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section" id="experience">
    <div class="sec-head">💼 Work Experience</div>
    <div class="exp-card">
      <div class="exp-logo">W</div>
      <div>
        <div class="exp-role">Associate Data Analyst</div>
        <div class="exp-company">Wipro Limited</div>
        <div class="exp-period">2024 – Present &nbsp;·&nbsp; Full-time</div>
        <div class="exp-desc">
          Contributing to enterprise data solutions at Wipro — extracting, transforming, and
          analysing large datasets to surface insights for clients. Building Power BI dashboards,
          writing optimised SQL queries, and working with cross-functional teams to ensure
          data accuracy and business impact.
        </div>
      </div>
    </div>
  </div>

  <!-- CERTIFICATES -->
  <div class="section" id="certs">
    <div class="sec-head">📜 Certificates &nbsp;<span style="font-size:13px;color:var(--muted);font-weight:400;">— click any card to view</span></div>
    <div class="certs-grid">

      <a class="cert-card" href="https://www.linkedin.com/learning/certificates/a3b8d8eec21ac36352f7699c7314aa249155341d157986874da211ffdc5730f6?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3BvvJOMHs5TvWkVQ6x6tYN0w%3D%3D" target="_blank">
        <div class="cert-icon">📋</div>
        <div>
          <div class="cert-name">Business Analysis Foundations</div>
          <div class="cert-issuer">LinkedIn Learning · Verified</div>
          <div class="cert-view">View Certificate <span class="cert-arrow">→</span></div>
        </div>
      </a>

      <a class="cert-card" href="https://www.linkedin.com/learning/certificates/5831d0d23d8316c2ef7e88804ba55b1e69380216b157ff4d60a856e10549788e?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3BvvJOMHs5TvWkVQ6x6tYN0w%3D%3D" target="_blank">
        <div class="cert-icon">📊</div>
        <div>
          <div class="cert-name">Intro to Career Skills in Data Analytics</div>
          <div class="cert-issuer">LinkedIn Learning · Verified</div>
          <div class="cert-view">View Certificate <span class="cert-arrow">→</span></div>
        </div>
      </a>

      <a class="cert-card" href="https://www.linkedin.com/learning/certificates/5dec5d838efd57efdb0ef08d90de32c642078e055482deced76b5a5ca16bed7e?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3BnjVggO7aQxaRzP6ZxSH1Ww%3D%3D" target="_blank">
        <div class="cert-icon">🗂️</div>
        <div>
          <div class="cert-name">Project Management Foundations</div>
          <div class="cert-issuer">LinkedIn Learning · Verified</div>
          <div class="cert-view">View Certificate <span class="cert-arrow">→</span></div>
        </div>
      </a>

      <a class="cert-card" href="https://www.linkedin.com/learning/certificates/61a7fb3ad797758e389f7856e8ce7602a999b114603be3949155a4ba7c43d0f9" target="_blank">
        <div class="cert-icon">🏆</div>
        <div>
          <div class="cert-name">Project Management Foundations II</div>
          <div class="cert-issuer">LinkedIn Learning · Verified</div>
          <div class="cert-view">View Certificate <span class="cert-arrow">→</span></div>
        </div>
      </a>

    </div>
  </div>

  <!-- PROJECT -->
  <div class="section" id="projects">
    <div class="sec-head">📁 Featured Project</div>
    <div class="proj-card">
      <div class="proj-top">
        <div class="proj-title">📈 Meta-Analysis Dashboard</div>
        <div class="proj-links">
          <a class="proj-link" href="https://github.com/Raajiv-Analyst/Meta-Analysis" target="_blank">⎋ GitHub</a>
          <a class="proj-link" href="https://app.powerbi.com/view?r=eyJrIjoiMDAzMGE5MjEtNjNjNC00ZWIxLThmMGMtMzcxODY1ODE1MDkwIiwidCI6ImY2Zjk3NDE3LTEwNjItNDYyZC05NzU3LTZjOTU4MzZmNDk3MSJ9" target="_blank">🔗 Live Demo</a>
        </div>
      </div>
      <p class="proj-desc">Comprehensive data analysis project focused on Meta's business metrics and performance indicators, with interactive dashboards for data-driven insights.</p>
      <div class="proj-tags">
        <span class="proj-tag">Python</span>
        <span class="proj-tag">Power BI</span>
        <span class="proj-tag">SQL</span>
        <span class="proj-tag">Excel</span>
      </div>
      <ul class="proj-pts">
        <li>Analysed and visualised Meta's business performance data across key KPIs</li>
        <li>Created interactive dashboards enabling self-serve insight exploration</li>
        <li>Built end-to-end data cleaning and transformation pipeline</li>
        <li>Generated actionable recommendations based on findings</li>
      </ul>
    </div>
  </div>

  <!-- LOOKING FOR -->
  <div class="section">
    <div class="sec-head">🎯 What I'm Looking For</div>
    <div class="look-grid">
      <div class="look-item"><span class="em">📊</span> Apply analytical skills to solve real-world business problems</div>
      <div class="look-item"><span class="em">🤝</span> Collaborate with cross-functional data teams</div>
      <div class="look-item"><span class="em">⚡</span> Contribute to data-driven decisions at scale</div>
      <div class="look-item"><span class="em">🌱</span> Grow in a dynamic environment with modern data tools</div>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="section" id="contact">
    <div class="sec-head">📫 Let's Connect</div>
    <div class="badges">
      <a class="badge-btn" href="https://www.linkedin.com/in/raajiv28/" target="_blank">
        <img src="https://img.icons8.com/color/48/linkedin.png" alt="li"/> LinkedIn
      </a>
      <a class="badge-btn" href="mailto:rg28@gmail.com">
        <img src="https://img.icons8.com/color/48/gmail-new.png" alt="gm"/> rg28@gmail.com
      </a>
      <a class="badge-btn" href="https://github.com/Raajiv-Analyst" target="_blank">
        <img src="https://img.icons8.com/ios-glyphs/48/8b949e/github.png" alt="gh"/> Raajiv-Analyst
      </a>
    </div>
  </div>

</div>

<footer>
  <p>Raajiv · Associate Data Analyst @ <strong style="color:var(--text)">Wipro</strong> · <a href="https://www.linkedin.com/in/raajiv28/" target="_blank">linkedin.com/in/raajiv28</a></p>
</footer>

</body>
</html>
