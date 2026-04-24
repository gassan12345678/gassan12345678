<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ghassan Jaha · AI & Automotive Engineer · GitHub README Banner</title>
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0f1722;  /* dark tech background */
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      font-family: 'Segoe UI', 'Roboto', 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'SF Pro Text', sans-serif;
      padding: 2rem;
    }

    /* main card container — exactly as GitHub readme friendly, but visually rich */
    .gh-readme-card {
      max-width: 1060px;
      width: 100%;
      background: #0a0e1a;
      border-radius: 2rem;
      box-shadow: 0 25px 45px -12px rgba(0,0,0,0.6), 0 0 0 1px rgba(66, 153, 225, 0.2);
      overflow: hidden;
      transition: transform 0.2s ease;
    }

    /* header / hero area with ZR1 visual - replaced GTR with 2011 C6 ZR1 */
    .hero-panel {
      background: linear-gradient(135deg, #0f1728 0%, #111b2c 100%);
      padding: 1.8rem 2.2rem 1.2rem 2.2rem;
      border-bottom: 1px solid rgba(56, 189, 248, 0.2);
      position: relative;
    }

    /* ZR1 showcase row — "hero car visual" that blends background colors */
    .zr1-showcase {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 1.5rem;
      margin-bottom: 1.2rem;
    }

    .car-visual {
      flex: 2;
      min-width: 240px;
    }

    .car-title {
      flex: 1;
      text-align: right;
    }

    .zr1-badge {
      font-size: 0.85rem;
      letter-spacing: 1px;
      background: rgba(255,255,245,0.05);
      backdrop-filter: blur(4px);
      padding: 0.3rem 1rem;
      border-radius: 40px;
      display: inline-block;
      color: #a5f0ff;
      border: 1px solid rgba(80, 180, 255, 0.3);
      font-weight: 500;
    }

    .zr1-model {
      font-size: 1.9rem;
      font-weight: 700;
      background: linear-gradient(135deg, #E6E9F0, #9bb6d0);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-top: 0.2rem;
    }

    /* SVG illustration — 2011 C6 ZR1, color matched to background (deep steel blue / charcoal) */
    .zr1-svg {
      max-width: 100%;
      height: auto;
      filter: drop-shadow(0 8px 12px rgba(0,0,0,0.4));
    }

    /* profile row */
    .profile-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin-top: 1rem;
      gap: 1rem;
    }

    .name-title h1 {
      font-size: 1.8rem;
      font-weight: 700;
      background: linear-gradient(120deg, #ffffff, #b9e2ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -0.3px;
    }
    .name-title p {
      color: #8eacd4;
      font-weight: 500;
      margin-top: 4px;
    }

    .contact-links {
      display: flex;
      gap: 1.5rem;
    }
    .contact-links a {
      color: #b9d6f5;
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 500;
      transition: 0.2s;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }
    .contact-links a:hover {
      color: #7bc5ff;
      transform: translateY(-1px);
    }

    /* stats grid */
    .stats-grid {
      display: flex;
      flex-wrap: wrap;
      background: #0c1120;
      padding: 1.2rem 2rem;
      gap: 1rem;
      border-bottom: 1px solid #1e2a3e;
    }
    .stat-card {
      flex: 1;
      background: #10162a;
      border-radius: 1.2rem;
      padding: 0.75rem 1rem;
      text-align: center;
      backdrop-filter: blur(2px);
      border: 1px solid #253449;
    }
    .stat-number {
      font-size: 1.6rem;
      font-weight: 800;
      color: #7fc9ff;
      letter-spacing: 1px;
    }
    .stat-label {
      font-size: 0.7rem;
      text-transform: uppercase;
      font-weight: 500;
      color: #8ba0c2;
    }

    /* language bars */
    .lang-section {
      padding: 1.5rem 2rem 1.2rem 2rem;
      background: #0b1020;
    }
    .section-title {
      color: #c7e2ff;
      font-weight: 600;
      margin-bottom: 1rem;
      font-size: 1rem;
      letter-spacing: 0.3px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .lang-bars {
      display: flex;
      flex-direction: column;
      gap: 0.8rem;
    }
    .lang-item {
      display: flex;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
    }
    .lang-name {
      width: 100px;
      font-weight: 500;
      color: #ccdeff;
    }
    .bar-bg {
      flex: 1;
      height: 8px;
      background: #1f2a3e;
      border-radius: 10px;
      overflow: hidden;
    }
    .bar-fill {
      height: 100%;
      width: 0%;
      background: linear-gradient(90deg, #3b82f6, #7aaef5);
      border-radius: 10px;
    }
    .lang-percent {
      width: 55px;
      color: #bbd4ff;
      font-size: 0.8rem;
      font-weight: 500;
    }
    .second-stats {
      display: flex;
      justify-content: space-between;
      margin-top: 1.2rem;
      background: #0a0f1c;
      border-radius: 1.2rem;
      padding: 0.8rem 1.2rem;
    }

    /* projects & connect */
    .projects-connect {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding: 1.2rem 2rem 1.8rem 2rem;
      gap: 2rem;
      border-top: 1px solid #18212f;
      background: #0c111f;
    }
    .projects {
      flex: 2;
    }
    .connect {
      flex: 1.2;
    }
    .project-item {
      background: #0f1626;
      padding: 0.5rem 1rem;
      border-radius: 1rem;
      margin-top: 0.5rem;
      display: inline-block;
      font-size: 0.85rem;
      color: #bbddff;
    }
    .connect-icons {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
      margin-top: 0.5rem;
    }
    .connect-icons a {
      color: #b6d0f5;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 0.85rem;
    }
    .footer-note {
      font-size: 0.7rem;
      text-align: center;
      padding: 1rem;
      background: #070c18;
      color: #5b759b;
    }
    hr {
      border-color: #1d2a40;
      margin: 0.5rem 0;
    }
    i {
      width: 24px;
    }
    @media (max-width: 700px) {
      .hero-panel { padding: 1.2rem; }
      .zr1-model { font-size: 1.3rem; }
    }
  </style>
</head>
<body>
<div class="gh-readme-card">
  <!-- Hero area with replaced car: 2011 C6 Corvette ZR1, color integrated with background -->
  <div class="hero-panel">
    <div class="zr1-showcase">
      <div class="car-visual">
        <!-- Custom vector styled ZR1 silhouette + details matching deep blue/grey background -->
        <svg class="zr1-svg" viewBox="0 0 520 130" xmlns="http://www.w3.org/2000/svg" style="width:100%; max-width:480px;">
          <defs>
            <linearGradient id="bodyGrad" x1="0%" y1="0%" x2="100%" y2="40%">
              <stop offset="0%" stop-color="#2b3e5a" />
              <stop offset="40%" stop-color="#415f82" />
              <stop offset="100%" stop-color="#1f3148" />
            </linearGradient>
            <linearGradient id="darkAccent" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#171f33" />
              <stop offset="100%" stop-color="#0c1223" />
            </linearGradient>
            <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
              <feGaussianBlur in="SourceAlpha" stdDeviation="2" />
              <feMerge>
                <feMergeNode in="offsetblur" />
                <feMergeNode in="SourceGraphic" />
              </feMerge>
            </filter>
          </defs>
          <!-- Main chassis C6 ZR1 style, low wide stance, color blends with #0f1728 / #111b2c background -->
          <path d="M45,65 L62,52 L88,45 L120,41 L180,38 L240,36 L300,37 L360,39 L420,43 L455,48 L475,55 L485,63 L490,75 L482,82 L460,87 L420,90 L360,92 L300,93 L240,93 L180,92 L130,90 L95,86 L68,80 L48,74 L43,68 Z" fill="url(#bodyGrad)" stroke="#7899c0" stroke-width="1.2" />
          <!-- Front splitter / aero -->
          <path d="M43,68 L35,72 L32,78 L38,80 L48,74 Z" fill="#141e32" stroke="#6582aa" />
          <!-- Rear wing element subtle ZR1 style -->
          <path d="M465,50 L488,53 L495,65 L482,68 L468,64 Z" fill="#1a2942" stroke="#7a9bc9" stroke-width="1" />
          <!-- Side intake / carbon accents -->
          <path d="M185,70 L215,66 L245,64 L245,78 L215,81 L185,80 Z" fill="#0d1427" opacity="0.9" />
          <path d="M310,69 L340,65 L370,64 L370,78 L340,80 L310,81 Z" fill="#0d1427" opacity="0.9" />
          <!-- Wheels (deep dish, ZR1 style cup wheels) -->
          <circle cx="110" cy="81" r="16" fill="#11161f" stroke="#5f789e" stroke-width="1.5" />
          <circle cx="110" cy="81" r="8" fill="#252f44" stroke="#8aa9d4" stroke-width="1" />
          <circle cx="390" cy="82" r="16" fill="#11161f" stroke="#5f789e" stroke-width="1.5" />
          <circle cx="390" cy="82" r="8" fill="#252f44" stroke="#8aa9d4" stroke-width="1" />
          <!-- brake caliper hint -->
          <circle cx="110" cy="81" r="3" fill="#c54132" />
          <circle cx="390" cy="82" r="3" fill="#c54132" />
          <!-- Headlights quad-style -->
          <ellipse cx="54" cy="60" rx="6" ry="4" fill="#e9f2ff" stroke="#a6c5ff" />
          <ellipse cx="70" cy="57" rx="4" ry="3" fill="#cce6ff" />
          <!-- Taillights modern leds -->
          <rect x="460" y="58" width="8" height="6" rx="2" fill="#ff3a4d" opacity="0.95" />
          <rect x="474" y="60" width="6" height="5" rx="1.5" fill="#ff3a4d" opacity="0.9" />
          <!-- ZR1 emblem text on side -->
          <text x="260" y="81" font-size="7" fill="#bddaff" font-weight="bold" font-family="monospace">ZR1</text>
          <!-- supercharger bulge subtle -->
          <path d="M215,45 L225,39 L275,38 L300,40 L290,47 L255,48 Z" fill="#1a2a42" opacity="0.7" />
        </svg>
      </div>
      <div class="car-title">
        <div class="zr1-badge"><i class="fas fa-car"></i> 2011 C6 CORVETTE ZR1</div>
        <div class="zr1-model">LS9 Supercharged • 638 hp</div>
      </div>
    </div>
    <div class="profile-row">
      <div class="name-title">
        <h1>Ghassan Jaha</h1>
        <p><i class="fas fa-microchip"></i> Artificial Intelligence | Automotive Performance Enthusiast</p>
      </div>
      <div class="contact-links">
        <a href="mailto:sanoo268668@gmail.com"><i class="fas fa-envelope"></i> sanoo268668</a>
        <a href="https://www.linkedin.com/in/gassan-jaha-194315308/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="#"><i class="fab fa-github"></i> Ghassan_Jaha</a>
      </div>
    </div>
  </div>

  <!-- stats row: contributions / repos / followers (matching original card) -->
  <div class="stats-grid">
    <div class="stat-card"><div class="stat-number">1,234</div><div class="stat-label">Total Contributions</div></div>
    <div class="stat-card"><div class="stat-number">24</div><div class="stat-label">Public Repositories</div></div>
    <div class="stat-card"><div class="stat-number">187</div><div class="stat-label">Followers</div></div>
    <div class="stat-card"><div class="stat-number">92</div><div class="stat-label">Following</div></div>
  </div>

  <!-- Most used languages + commits per language (updated from original) -->
  <div class="lang-section">
    <div class="section-title"><i class="fas fa-code"></i> Most Used Languages &nbsp;▏&nbsp; <i class="fas fa-chart-line"></i> Commit Activity</div>
    <div class="lang-bars">
      <div class="lang-item"><span class="lang-name">Python</span><div class="bar-bg"><div class="bar-fill" style="width:62.1%"></div></div><span class="lang-percent">62.1%</span><span style="color:#89b9ff; margin-left:auto;"><i class="fas fa-arrow-right"></i> Commits: 8.7%</span></div>
      <div class="lang-item"><span class="lang-name">JavaScript</span><div class="bar-bg"><div class="bar-fill" style="width:13.4%"></div></div><span class="lang-percent">13.4%</span><span style="color:#89b9ff; margin-left:auto;">Commits: 6.2%</span></div>
      <div class="lang-item"><span class="lang-name">SQL</span><div class="bar-bg"><div class="bar-fill" style="width:4.1%"></div></div><span class="lang-percent">4.1%</span><span style="color:#89b9ff; margin-left:auto;">Commits: 5.5%</span></div>
      <div class="lang-item"><span class="lang-name">Other (HTML/CSS, C++)</span><div class="bar-bg"><div class="bar-fill" style="width:5.5%"></div></div><span class="lang-percent">5.5%</span><span style="color:#89b9ff; margin-left:auto;">Commits: 3.9%</span></div>
    </div>
    <div class="second-stats">
      <span><i class="fas fa-database"></i> ML Focus: Predictive maintenance & engine analytics</span>
      <span><i class="fas fa-tachometer-alt"></i> ECU Tuning • Performance simulation</span>
    </div>
  </div>

  <!-- Projects + Connect (updated email/linkedin and fixed image replacement context) -->
  <div class="projects-connect">
    <div class="projects">
      <div class="section-title" style="margin-bottom:0.5rem;"><i class="fas fa-rocket"></i> Projects (Coming Soon)</div>
      <div class="project-item"><i class="fas fa-chart-line"></i> Engine data analysis & predictive maintenance suite</div>
      <div class="project-item" style="margin-top:0.5rem;"><i class="fas fa-car-crash"></i> ZR1 telemetry & AI-driven knock detection</div>
      <div class="project-item"><i class="fas fa-microchip"></i> Real-time vehicle health monitoring with edge ML</div>
      <div class="project-item"><i class="fas fa-brain"></i> LLM for automotive diagnostic assistance</div>
    </div>
    <div class="connect">
      <div class="section-title" style="margin-bottom:0.5rem;"><i class="fas fa-address-card"></i> Connect with me</div>
      <div class="connect-icons">
        <a href="mailto:sanoo268668@gmail.com"><i class="fas fa-envelope"></i> sanoo268668@gmail.com</a>
        <a href="https://www.linkedin.com/in/gassan-jaha-194315308/" target="_blank"><i class="fab fa-linkedin"></i> linkedin.com/in/gassan-jaha</a>
        <a href="#"><i class="fab fa-github"></i> github.com/GhassanJaha (coming)</a>
        <a href="#"><i class="fab fa-discord"></i> Automotive AI community</a>
      </div>
      <hr>
      <div style="font-size:0.7rem; color:#6a84ab; margin-top:12px;"><i class="fas fa-crown"></i> "Code & Combustion — perfect synergy"</div>
    </div>
  </div>

  <!-- small note about engine data + model sample (snippet from original but not displayed as code) -->
  <div class="footer-note">
    <i class="fas fa-laptop-code"></i> Python • sklearn • RandomForestRegressor • Real-time telemetry ·   <span style="color:#8fb6e8;">"2011 C6 ZR1 • Carbon fiber • LS9 • 6-speed manual"</span>
  </div>
</div>
</body>
</html>
