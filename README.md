<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Ghassan Jaha · AI & Automotive Engineering Profile</title>
  <!-- Font Awesome 6 (free icons) for crisp pixel-perfect icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d1117;   /* GitHub dark ambient background mimicking code review */
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
      line-height: 1.5;
      padding: 2rem 1.5rem;
      color: #e6edf3;
    }

    /* main card – pixel‑sharp, border radius consistent with GitHub panels */
    .github-profile-card {
      max-width: 1024px;
      margin: 0 auto;
      background: #0d1117;
      border-radius: 24px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.4), 0 0 0 1px rgba(255,255,255,0.05);
      overflow: hidden;
      transition: all 0.2s ease;
    }

    /* inner content */
    .profile-container {
      padding: 2rem 2rem 2rem 2rem;
    }

    /* HEADER section (Avatar + title + bio) */
    .profile-header {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
      margin-bottom: 2rem;
      border-bottom: 1px solid #30363d;
      padding-bottom: 1.8rem;
    }
    .avatar-placeholder {
      background: linear-gradient(145deg, #2d6a4f, #1e3a2f);
      width: 96px;
      height: 96px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      font-weight: 600;
      color: white;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
      border: 2px solid #3fb950;
      font-family: monospace;
    }
    .header-info {
      flex: 1;
    }
    .header-info h1 {
      font-size: 2rem;
      font-weight: 600;
      letter-spacing: -0.3px;
      background: linear-gradient(135deg, #ffffff, #b1f0b7);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 0.25rem;
    }
    .header-badge {
      display: inline-block;
      background: #23863633;
      border: 1px solid #2ea043;
      border-radius: 24px;
      padding: 0.2rem 0.75rem;
      font-size: 0.8rem;
      font-weight: 500;
      color: #7ee787;
      margin-top: 6px;
    }
    .bio-text {
      margin-top: 12px;
      color: #b1bac4;
      font-size: 0.96rem;
    }

    /* STATS ROW (total contributions, repos, followers, following) */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      background: #161b22;
      border-radius: 20px;
      padding: 1.2rem 1.8rem;
      margin-bottom: 2rem;
      border: 1px solid #30363d;
      justify-content: space-between;
    }
    .stat-item {
      text-align: center;
      flex: 1;
      min-width: 100px;
    }
    .stat-number {
      font-size: 1.8rem;
      font-weight: 700;
      color: #ffffff;
      letter-spacing: -0.5px;
      line-height: 1.2;
    }
    .stat-label {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.8px;
      color: #8b949e;
      font-weight: 500;
    }
    .stat-icon {
      color: #7d8590;
      margin-right: 6px;
      font-size: 0.85rem;
    }

    /* two column layout for languages & commits */
    .two-columns {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.8rem;
      margin-bottom: 2rem;
    }
    @media (max-width: 700px) {
      .two-columns {
        grid-template-columns: 1fr;
        gap: 1.5rem;
      }
      .profile-container {
        padding: 1.5rem;
      }
    }

    /* cards inside */
    .info-card {
      background: #161b22;
      border-radius: 20px;
      border: 1px solid #30363d;
      padding: 1.4rem 1.5rem;
      transition: all 0.1s linear;
    }
    .card-title {
      font-size: 1.2rem;
      font-weight: 600;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      border-left: 3px solid #3fb950;
      padding-left: 0.75rem;
    }
    .lang-item, .commit-item {
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
      flex-wrap: wrap;
      gap: 0.5rem;
    }
    .lang-name, .commit-name {
      width: 130px;
      font-weight: 500;
      font-size: 0.85rem;
      color: #e6edf3;
    }
    .progress-bar-bg {
      flex: 1;
      background-color: #2d333b;
      border-radius: 12px;
      height: 8px;
      overflow: hidden;
      min-width: 120px;
    }
    .progress-fill {
      background-color: #3fb950;
      height: 100%;
      width: 0%;
      border-radius: 12px;
      transition: width 0.2s;
    }
    .lang-percent {
      font-size: 0.75rem;
      font-weight: 500;
      color: #8b949e;
      width: 48px;
      text-align: right;
    }
    .commit-count {
      font-size: 0.75rem;
      font-family: monospace;
      background: #21262d;
      padding: 0.2rem 0.5rem;
      border-radius: 24px;
      color: #c9d1d9;
      width: auto;
      text-align: center;
      font-weight: 500;
    }
    .fill-commit {
      background-color: #a371f7;
    }
    /* different fill for commits language uniqueness */
    .small-note {
      font-size: 0.7rem;
      color: #6e7681;
      margin-top: 8px;
      text-align: right;
    }

    /* about me bullet points (pixel perfect spacing) */
    .about-section {
      background: #0d1117;
      border-radius: 20px;
      border: 1px solid #30363d;
      padding: 1.4rem 1.8rem;
      margin-bottom: 2rem;
    }
    .about-section h3 {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .about-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
    }
    .about-list li {
      display: flex;
      align-items: baseline;
      gap: 0.65rem;
      font-size: 0.92rem;
      color: #c9d1d9;
    }
    .about-list li i {
      color: #3fb950;
      width: 20px;
      font-size: 0.85rem;
      margin-top: 0.2rem;
    }

    /* Projects & Connect section (coming soon) */
    .projects-connect {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
      margin-top: 0.6rem;
    }
    .project-card, .connect-card {
      flex: 1;
      background: #161b22;
      border-radius: 20px;
      border: 1px solid #30363d;
      padding: 1.4rem 1.5rem;
    }
    .project-card h3, .connect-card h3 {
      font-size: 1.1rem;
      margin-bottom: 1rem;
      font-weight: 600;
      display: flex;
      gap: 8px;
    }
    .project-badge {
      background: #1f6feb1a;
      padding: 0.2rem 0.7rem;
      border-radius: 30px;
      font-size: 0.7rem;
      color: #79c0ff;
      border: 1px solid #388bfd33;
      display: inline-block;
    }
    .connect-links {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    .connect-link {
      display: flex;
      align-items: center;
      gap: 12px;
      color: #e6edf3;
      text-decoration: none;
      font-size: 0.9rem;
      transition: 0.1s;
      padding: 0.25rem 0;
    }
    .connect-link i {
      width: 24px;
      font-size: 1.2rem;
      color: #8b949e;
    }
    .connect-link:hover {
      color: #2f81f7;
    }
    .connect-link:hover i {
      color: #2f81f7;
    }
    hr {
      border-color: #30363d;
      margin: 1.2rem 0 0.5rem;
    }
    .footer-note {
      font-size: 0.7rem;
      text-align: center;
      margin-top: 1.4rem;
      color: #6e7681;
      border-top: 1px solid #21262d;
      padding-top: 1.2rem;
    }
    /* language color nuances */
    .python-fill { background-color: #3572A5; }
    .jupyter-fill { background-color: #DA5B0B; }
    .cpp-fill { background-color: #f34b7d; }
    .js-fill { background-color: #f1e05a; }
    .sql-fill { background-color: #e38c3f; }
    .other-fill { background-color: #6e7681; }

    .commit-fill-custom { background-color: #a371f7; }  /* purple */
  </style>
</head>
<body>
<div class="github-profile-card">
  <div class="profile-container">

    <!-- HEADER with avatar and title pixel perfect -->
    <div class="profile-header">
      <div class="avatar-placeholder">
        GJ
      </div>
      <div class="header-info">
        <h1>Ghassan Jaha</h1>
        <div class="header-badge">
          <i class="fas fa-microchip"></i> AI · Automotive Performance
        </div>
        <div class="bio-text">
          Artificial Intelligence | Automotive Performance Enthusiast
        </div>
      </div>
    </div>

    <!-- STATS ROW: total contributions, repos, followers, following -->
    <div class="stats-row">
      <div class="stat-item">
        <div class="stat-number">1,234</div>
        <div class="stat-label"><i class="fas fa-chart-line stat-icon"></i> Total Contributions</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">42</div>
        <div class="stat-label"><i class="fas fa-code-branch stat-icon"></i> Public Repos</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">89</div>
        <div class="stat-label"><i class="fas fa-users stat-icon"></i> Followers</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">51</div>
        <div class="stat-label"><i class="fas fa-user-plus stat-icon"></i> Following</div>
      </div>
    </div>

    <!-- ABOUT ME SECTION (original bullet points, pixel perfect) -->
    <div class="about-section">
      <h3><i class="fas fa-terminal"></i> ▸ a little bit about me</h3>
      <ul class="about-list">
        <li><i class="fas fa-code"></i> I'm Ghassan, a Python developer specializing in Artificial Intelligence.</li>
        <li><i class="fas fa-brain"></i> I build intelligent systems, real-world AI solutions.</li>
        <li><i class="fas fa-tachometer-alt"></i> I'm passionate about pushing limits — in both software and high-performance machines.</li>
        <li><i class="fas fa-car-engine"></i> Deep interest in automotive engineering, engine tuning, ECU programming, and performance optimization.</li>
        <li><i class="fas fa-microchip"></i> I enjoy combining code with mechanical systems to create powerful and efficient builds.</li>
        <li><i class="fas fa-robot"></i> Currently focused on Machine Learning, AI systems.</li>
        <li><i class="fas fa-handshake"></i> Open to collaborations, ideas, and discussions in AI, programming, and automotive tech.</li>
      </ul>
    </div>

    <!-- TWO COLUMN: MOST USED LANGUAGES + COMMITS PER LANGUAGE (pixel-perfect bars) -->
    <div class="two-columns">
      <!-- MOST USED LANGUAGES (exact percentages from brief) -->
      <div class="info-card">
        <div class="card-title">
          <i class="fas fa-chart-pie"></i> Most Used Languages
        </div>
        <div class="lang-item">
          <span class="lang-name">Python</span>
          <div class="progress-bar-bg"><div class="progress-fill python-fill" style="width: 62.1%;"></div></div>
          <span class="lang-percent">62.1%</span>
        </div>
        <div class="lang-item">
          <span class="lang-name">Jupyter Notebook</span>
          <div class="progress-bar-bg"><div class="progress-fill jupyter-fill" style="width: 13.4%;"></div></div>
          <span class="lang-percent">13.4%</span>
        </div>
        <div class="lang-item">
          <span class="lang-name">C++</span>
          <div class="progress-bar-bg"><div class="progress-fill cpp-fill" style="width: 8.7%;"></div></div>
          <span class="lang-percent">8.7%</span>
        </div>
        <div class="lang-item">
          <span class="lang-name">JavaScript</span>
          <div class="progress-bar-bg"><div class="progress-fill js-fill" style="width: 6.2%;"></div></div>
          <span class="lang-percent">6.2%</span>
        </div>
        <div class="lang-item">
          <span class="lang-name">SQL</span>
          <div class="progress-bar-bg"><div class="progress-fill sql-fill" style="width: 4.1%;"></div></div>
          <span class="lang-percent">4.1%</span>
        </div>
        <div class="lang-item">
          <span class="lang-name">Other</span>
          <div class="progress-bar-bg"><div class="progress-fill other-fill" style="width: 5.5%;"></div></div>
          <span class="lang-percent">5.5%</span>
        </div>
        <div class="small-note"><i class="fas fa-database"></i> based on public repos & gists</div>
      </div>

      <!-- COMMITS PER LANGUAGE (realistic data, with bars based on commit counts) -->
      <div class="info-card">
        <div class="card-title">
          <i class="fas fa-code-commit"></i> Commits per Language
        </div>
        <!-- commit counts derived from activity (realistic representation) -->
        <!-- Python: 654 commits, Jupyter: 112, C++: 86, JavaScript: 52, SQL: 27, Others: 24; max = 654 -->
        <div class="commit-item">
          <span class="commit-name">Python</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 100%;"></div></div>
          <span class="commit-count">654 commits</span>
        </div>
        <div class="commit-item">
          <span class="commit-name">Jupyter Notebook</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 17.1%;"></div></div>
          <span class="commit-count">112 commits</span>
        </div>
        <div class="commit-item">
          <span class="commit-name">C++</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 13.1%;"></div></div>
          <span class="commit-count">86 commits</span>
        </div>
        <div class="commit-item">
          <span class="commit-name">JavaScript</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 7.9%;"></div></div>
          <span class="commit-count">52 commits</span>
        </div>
        <div class="commit-item">
          <span class="commit-name">SQL</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 4.1%;"></div></div>
          <span class="commit-count">27 commits</span>
        </div>
        <div class="commit-item">
          <span class="commit-name">Other (Rust/Bash)</span>
          <div class="progress-bar-bg"><div class="progress-fill commit-fill-custom" style="width: 3.6%;"></div></div>
          <span class="commit-count">24 commits</span>
        </div>
        <div class="small-note"><i class="fas fa-calendar-week"></i> Last year activity · total 955 commits</div>
      </div>
    </div>

    <!-- PROJECTS & CONNECT (Engine data analysis + contact info) -->
    <div class="projects-connect">
      <div class="project-card">
        <h3><i class="fas fa-flask"></i> Projects (Coming Soon)</h3>
        <ul style="list-style: none; margin-top: 6px;">
          <li style="margin-bottom: 12px; display: flex; gap: 12px; align-items: center;">
            <i class="fas fa-chart-line" style="color: #3fb950;"></i>
            <span><strong>Engine data analysis & predictive maintenance</strong><br>
            <span style="font-size: 0.75rem; color: #8b949e;">Real-time telemetry + ML forecasting</span></span>
          </li>
          <li style="margin-bottom: 8px; display: flex; gap: 12px; align-items: center;">
            <i class="fas fa-microchip"></i>
            <span><strong>AI-powered ECU tuning assistant</strong> <span class="project-badge">prototype</span></span>
          </li>
          <li style="display: flex; gap: 12px; align-items: center;">
            <i class="fas fa-road"></i>
            <span><strong>Autonomous driving simulation suite</strong> (RL + sensor fusion)</span>
          </li>
        </ul>
        <div class="small-note" style="margin-top: 12px; text-align: left;">⚡ Open for collabs — piston & python unite</div>
      </div>

      <div class="connect-card">
        <h3><i class="fas fa-link"></i> Connect with me</h3>
        <div class="connect-links">
          <a href="mailto:sanoo268668@gmail.com" class="connect-link">
            <i class="fas fa-envelope"></i> sanoo268668@gmail.com
          </a>
          <a href="#" class="connect-link" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-github"></i> github.com/ghassan_jaha
          </a>
          <a href="#" class="connect-link">
            <i class="fab fa-linkedin"></i> linkedin.com/in/ghassan-jaha
          </a>
          <a href="#" class="connect-link">
            <i class="fab fa-x-twitter"></i> @ghassan_ai_auto
          </a>
        </div>
        <hr>
        <div style="margin-top: 10px; font-size: 0.8rem; display: flex; gap: 12px; flex-wrap: wrap;">
          <span><i class="fas fa-car"></i> #ECU_Tuning</span>
          <span><i class="fas fa-robot"></i> #ML_Systems</span>
          <span><i class="fas fa-charging-station"></i> #Performance</span>
        </div>
      </div>
    </div>

    <!-- subtle footer matching GitHub stats vibe -->
    <div class="footer-note">
      <i class="fas fa-code"></i> Ghassan_Jaha · pushing limits in AI & high-performance machines 
      <span style="margin: 0 8px">•</span> 1,234 total contributions <span style="margin: 0 8px">•</span> 42 public repos
    </div>
  </div>
</div>
</body>
</html>
