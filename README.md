<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IT Governance – Key Concepts Infographic</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --green-dark: #1A5C34;
    --green-mid:  #2E8B5A;
    --green-light:#4DB87A;
    --green-pale: #D6F0E3;
    --accent:     #F5A623;
    --accent-dark:#C07A00;
    --ink:        #1A1A1A;
    --ink-mid:    #3D3D3A;
    --ink-muted:  #717166;
    --surface:    #FAFAF7;
    --card:       #FFFFFF;
    --border:     #DDD9CE;
    --chip-bg:    #EFF9F3;
    --chip-stroke:#2E8B5A;
  }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--surface);
    color: var(--ink);
    line-height: 1.6;
  }

  /* ─── HERO ─────────────────────────────────────────── */
  .hero {
    background: var(--green-dark);
    color: #fff;
    padding: 56px 48px 48px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 340px; height: 340px;
    border-radius: 50%;
    background: var(--green-mid);
    opacity: .35;
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px; left: 40%;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: var(--green-light);
    opacity: .2;
  }
  .hero-tag {
    display: inline-block;
    background: var(--accent);
    color: var(--accent-dark);
    font-size: 11px;
    font-weight: 600;
    letter-spacing: .12em;
    text-transform: uppercase;
    padding: 4px 12px;
    border-radius: 100px;
    margin-bottom: 20px;
  }
  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(32px, 5vw, 52px);
    line-height: 1.1;
    max-width: 540px;
    position: relative;
    z-index: 1;
  }
  .hero h1 em {
    font-style: italic;
    color: var(--green-light);
  }
  .hero-sub {
    margin-top: 14px;
    font-size: 15px;
    opacity: .75;
    max-width: 480px;
    position: relative;
    z-index: 1;
  }
  .hero-meta {
    margin-top: 28px;
    display: flex;
    gap: 24px;
    font-size: 12px;
    opacity: .6;
    position: relative;
    z-index: 1;
  }

  /* ─── LAYOUT ────────────────────────────────────────── */
  .page { max-width: 960px; margin: 0 auto; padding: 40px 24px 64px; }

  .section-label {
    font-size: 10px;
    font-weight: 600;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--green-mid);
    margin-bottom: 8px;
  }
  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: 22px;
    color: var(--ink);
    margin-bottom: 24px;
  }

  /* ─── IMPLEMENTATION STEPS ──────────────────────────── */
  .steps-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 16px;
    margin-bottom: 56px;
  }
  .step-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 22px 20px;
    position: relative;
    overflow: hidden;
    transition: transform .2s, box-shadow .2s;
  }
  .step-card:hover { transform: translateY(-3px); box-shadow: 0 8px 28px rgba(0,0,0,.08); }
  .step-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: var(--green-mid);
  }
  .step-num {
    font-family: 'DM Serif Display', serif;
    font-size: 36px;
    color: var(--green-pale);
    line-height: 1;
    margin-bottom: 4px;
  }
  .step-card h3 { font-size: 14px; font-weight: 600; color: var(--green-dark); margin-bottom: 8px; }
  .step-card p { font-size: 13px; color: var(--ink-muted); line-height: 1.55; }

  /* ─── CIO ROLE ──────────────────────────────────────── */
  .cio-block {
    background: var(--green-dark);
    color: #fff;
    border-radius: 18px;
    padding: 36px 32px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    margin-bottom: 56px;
  }
  @media(max-width:600px){ .cio-block { grid-template-columns: 1fr; } }
  .cio-header { font-family: 'DM Serif Display', serif; font-size: 20px; margin-bottom: 6px; }
  .cio-def { font-size: 12px; opacity: .65; margin-bottom: 20px; }
  .cio-chips { display: flex; flex-wrap: wrap; gap: 8px; }
  .chip {
    display: inline-block;
    padding: 5px 12px;
    border-radius: 100px;
    font-size: 12px;
    font-weight: 500;
    border: 1px solid rgba(255,255,255,.3);
    background: rgba(255,255,255,.1);
    color: #fff;
  }
  .cio-right { display: flex; flex-direction: column; gap: 14px; }
  .cio-stat {
    background: rgba(255,255,255,.1);
    border-radius: 10px;
    padding: 14px 16px;
  }
  .cio-stat-label { font-size: 11px; opacity: .6; text-transform: uppercase; letter-spacing: .08em; }
  .cio-stat-val { font-size: 15px; font-weight: 500; margin-top: 4px; }

  /* ─── RACI TABLE ────────────────────────────────────── */
  .raci-section { margin-bottom: 56px; }
  .raci-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
  }
  .raci-card {
    border-radius: 12px;
    padding: 20px 16px;
    text-align: center;
  }
  .raci-card:nth-child(1) { background: #1A5C34; color:#fff; }
  .raci-card:nth-child(2) { background: #2E8B5A; color:#fff; }
  .raci-card:nth-child(3) { background: #4DB87A; color:#fff; }
  .raci-card:nth-child(4) { background: var(--green-pale); color: var(--green-dark); }
  .raci-letter {
    font-family: 'DM Serif Display', serif;
    font-size: 42px;
    line-height: 1;
    margin-bottom: 8px;
  }
  .raci-word { font-size: 13px; font-weight: 600; margin-bottom: 6px; }
  .raci-q { font-size: 12px; opacity: .8; }

  /* ─── COMPONENTS HEXAGONS ───────────────────────────── */
  .comp-section { margin-bottom: 56px; }
  .comp-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }
  @media(max-width:560px){ .comp-grid { grid-template-columns: repeat(2,1fr); } }
  .comp-card {
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 16px;
    background: var(--card);
  }
  .comp-icon {
    width: 36px; height: 36px;
    border-radius: 8px;
    background: var(--chip-bg);
    border: 1px solid var(--chip-stroke);
    display: flex; align-items: center; justify-content: center;
    font-size: 16px;
    margin-bottom: 10px;
  }
  .comp-card h4 { font-size: 13px; font-weight: 600; color: var(--green-dark); margin-bottom: 5px; }
  .comp-card p { font-size: 12px; color: var(--ink-muted); line-height: 1.5; }

  /* ─── BPM LIFECYCLE ─────────────────────────────────── */
  .bpm-section { margin-bottom: 56px; }
  .bpm-flow {
    display: flex;
    gap: 0;
    align-items: stretch;
  }
  @media(max-width:620px){ .bpm-flow { flex-direction: column; } }
  .bpm-step {
    flex: 1;
    background: var(--card);
    border: 1px solid var(--border);
    border-right: none;
    padding: 22px 18px;
    position: relative;
  }
  .bpm-step:last-child { border-right: 1px solid var(--border); border-radius: 0 12px 12px 0; }
  .bpm-step:first-child { border-radius: 12px 0 0 12px; }
  .bpm-step::after {
    content: '→';
    position: absolute;
    right: -14px;
    top: 50%;
    transform: translateY(-50%);
    font-size: 20px;
    color: var(--green-mid);
    z-index: 2;
    background: var(--surface);
    width: 26px;
    text-align: center;
  }
  .bpm-step:last-child::after { display: none; }
  .bpm-dot {
    width: 32px; height: 32px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px; font-weight: 600; color: #fff;
    margin-bottom: 10px;
  }
  .bpm-step h4 { font-size: 13px; font-weight: 600; margin-bottom: 6px; }
  .bpm-step p { font-size: 12px; color: var(--ink-muted); line-height: 1.5; }

  /* ─── TOOLS STRIP ───────────────────────────────────── */
  .tools-section { margin-bottom: 56px; }
  .tools-row { display: flex; flex-wrap: wrap; gap: 12px; }
  .tool-pill {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 100px;
    padding: 10px 18px 10px 12px;
  }
  .tool-dot { width: 10px; height: 10px; border-radius: 50%; }
  .tool-pill strong { font-size: 13px; font-weight: 600; }
  .tool-pill span { font-size: 12px; color: var(--ink-muted); }

  /* ─── SGSTI ─────────────────────────────────────────── */
  .sgsti-section { margin-bottom: 56px; }
  .sgsti-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--border);
  }
  .sgsti-table th {
    background: var(--green-dark);
    color: #fff;
    padding: 12px 16px;
    text-align: left;
    font-weight: 500;
  }
  .sgsti-table td { padding: 11px 16px; border-bottom: 1px solid var(--border); }
  .sgsti-table tr:last-child td { border-bottom: none; }
  .sgsti-table tr:nth-child(even) td { background: var(--chip-bg); }
  .badge {
    display: inline-block;
    padding: 2px 10px;
    border-radius: 100px;
    font-size: 11px;
    font-weight: 600;
    background: var(--chip-bg);
    color: var(--green-dark);
    border: 1px solid var(--chip-stroke);
  }

  /* ─── CONCLUSION ────────────────────────────────────── */
  .conclusion {
    background: linear-gradient(135deg, var(--green-dark), #0F3D22);
    color: #fff;
    border-radius: 18px;
    padding: 40px 36px;
    position: relative;
    overflow: hidden;
  }
  .conclusion::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 220px; height: 220px;
    border-radius: 50%;
    background: var(--green-mid);
    opacity: .25;
  }
  .conclusion h2 {
    font-family: 'DM Serif Display', serif;
    font-size: 24px;
    margin-bottom: 14px;
    position: relative;
    z-index: 1;
  }
  .conclusion p {
    font-size: 14px;
    opacity: .8;
    max-width: 640px;
    line-height: 1.65;
    position: relative;
    z-index: 1;
  }
  .iso-badge {
    margin-top: 24px;
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: rgba(255,255,255,.12);
    border-radius: 10px;
    padding: 10px 16px;
    font-size: 13px;
    position: relative;
    z-index: 1;
  }
  .iso-badge strong { font-weight: 600; }

  /* divider */
  .divider { height: 1px; background: var(--border); margin: 48px 0; }
</style>
</head>
<body>

<!-- ═══ HERO ══════════════════════════════════════════════ -->
<div class="hero">
  <div class="hero-tag">Module Summary · IT Governance – Axis 4</div>
  <h1>Implementing <em>Good</em> IT Governance</h1>
  <p class="hero-sub">A visual guide to the key actions, roles, processes and standards that make IT governance work in real organisations.</p>
  <div class="hero-meta">
    <span>Author: Ángel Alberto Varón Quimbayo</span>
    <span>·</span>
    <span>Fundación Universitaria del Área Andina</span>
  </div>
</div>

<!-- ═══ MAIN CONTENT ══════════════════════════════════════ -->
<div class="page">

  <!-- 1. IMPLEMENTATION STEPS -->
  <p class="section-label">Phase 1</p>
  <p class="section-title">Six Key Actions for Implementing IT Governance</p>
  <div class="steps-grid">

    <div class="step-card">
      <div class="step-num">01</div>
      <h3>Identify Needs</h3>
      <p>Understand organisational objectives, align them through IT, map risks and define mechanisms to address them.</p>
    </div>

    <div class="step-card">
      <div class="step-num">02</div>
      <h3>Planning</h3>
      <p>Generate a plan with tasks, activities and tactics. Ensure maintenance strategies are established and followed consistently.</p>
    </div>

    <div class="step-card">
      <div class="step-num">03</div>
      <h3>Evaluate, Direct & Monitor</h3>
      <p>Assess effectiveness once implemented. Review processes, update policies and adopt new technologies as needed.</p>
    </div>

    <div class="step-card">
      <div class="step-num">04</div>
      <h3>Align, Plan & Organise</h3>
      <p>IT governance must align with the business strategy and provide an organisational structure oriented to strategic objectives.</p>
    </div>

    <div class="step-card">
      <div class="step-num">05</div>
      <h3>Build, Acquire & Implement</h3>
      <p>Acquire the necessary resources — personnel, technology and new processes — to execute the strategy successfully.</p>
    </div>

    <div class="step-card">
      <div class="step-num">06</div>
      <h3>Deliver, Service & Support</h3>
      <p>Once deployed, ensure continuous value delivery and provide the support required by the organisation and its users.</p>
    </div>

  </div>

  <div class="divider"></div>

  <!-- 2. CIO ROLE -->
  <p class="section-label">Organisational Structure</p>
  <p class="section-title">The Role of the CIO & IT Leadership</p>
  <div class="cio-block">
    <div>
      <div class="cio-header">Chief Information Officer (CIO)</div>
      <div class="cio-def">The executive responsible for IT management — strategic vision, decision support, and alignment with the business plan.</div>
      <div class="cio-chips">
        <span class="chip">Technology vision</span>
        <span class="chip">IT strategy</span>
        <span class="chip">Project management</span>
        <span class="chip">Negotiation skills</span>
        <span class="chip">Security policies</span>
        <span class="chip">Budget management</span>
        <span class="chip">User support</span>
        <span class="chip">Systems leadership</span>
        <span class="chip">Decision support</span>
      </div>
    </div>
    <div class="cio-right">
      <div class="cio-stat">
        <div class="cio-stat-label">Supporting roles</div>
        <div class="cio-stat-val">IT Advisor (co-pilot) + Secretary</div>
      </div>
      <div class="cio-stat">
        <div class="cio-stat-label">Core teams</div>
        <div class="cio-stat-val">Systems Development · Information Analysis · IT Services (Infrastructure + Operations)</div>
      </div>
      <div class="cio-stat">
        <div class="cio-stat-label">Sizing depends on</div>
        <div class="cio-stat-val">Sector · Organisation size · Information maturity · Technology requirements</div>
      </div>
    </div>
  </div>

  <!-- 3. RACI MATRIX -->
  <div class="raci-section">
    <p class="section-label">Responsibility Assignment</p>
    <p class="section-title">The RACI Matrix</p>
    <div class="raci-grid">
      <div class="raci-card">
        <div class="raci-letter">R</div>
        <div class="raci-word">Responsible</div>
        <div class="raci-q">Who is doing the activity?</div>
      </div>
      <div class="raci-card">
        <div class="raci-letter">A</div>
        <div class="raci-word">Accountable</div>
        <div class="raci-q">Who ensures the task is completed successfully?</div>
      </div>
      <div class="raci-card">
        <div class="raci-letter">C</div>
        <div class="raci-word">Consulted</div>
        <div class="raci-q">Who provides inputs and expertise?</div>
      </div>
      <div class="raci-card">
        <div class="raci-letter">I</div>
        <div class="raci-word">Informed</div>
        <div class="raci-q">Who receives information about progress?</div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- 4. ORGANISATIONAL COMPONENTS -->
  <div class="comp-section">
    <p class="section-label">Organisational Structure</p>
    <p class="section-title">Seven Components of IT Structure</p>
    <div class="comp-grid">

      <div class="comp-card">
        <div class="comp-icon">📡</div>
        <h4>Communication Flow</h4>
        <p>Identifies management practices, their inputs (source &amp; description) and outputs (destination).</p>
      </div>

      <div class="comp-card">
        <div class="comp-icon">👥</div>
        <h4>People, Skills &amp; Competencies</h4>
        <p>Defines who performs each activity, required skills and competencies to fulfil governance objectives.</p>
      </div>

      <div class="comp-card">
        <div class="comp-icon">📋</div>
        <h4>Policies &amp; Procedures</h4>
        <p>Defines governing rules and procedures with clear descriptions, focused on government and management goals.</p>
      </div>

      <div class="comp-card">
        <div class="comp-icon">🌱</div>
        <h4>Culture, Ethics &amp; Behaviour</h4>
        <p>Builds an organisational culture of excellence and synergy across work teams and the entire organisation.</p>
      </div>

      <div class="comp-card">
        <div class="comp-icon">🖥️</div>
        <h4>Services, Infrastructure &amp; Apps</h4>
        <p>Selects monitoring tools to maintain full operability for all IT services and business activities.</p>
      </div>

      <div class="comp-card">
        <div class="comp-icon">⚙️</div>
        <h4>Methodology</h4>
        <p>Establishes strategies and methodologies for managing services and carrying out operational activities.</p>
      </div>

      <div class="comp-card" style="grid-column: span 3;">
        <div class="comp-icon">🔄</div>
        <h4>Continuous Improvement</h4>
        <p>Evaluates performance of every component and innovates each one to better meet the objectives of the business plan.</p>
      </div>

    </div>
  </div>

  <div class="divider"></div>

  <!-- 5. BPM LIFECYCLE -->
  <div class="bpm-section">
    <p class="section-label">IT Process Management</p>
    <p class="section-title">Business Process Management (BPM) Life Cycle</p>
    <div class="bpm-flow">
      <div class="bpm-step">
        <div class="bpm-dot" style="background:#1A5C34">1</div>
        <h4>Analysis &amp; Design</h4>
        <p>Identify the current state of the organisation and design how IT management will integrate with it to fulfil business objectives.</p>
      </div>
      <div class="bpm-step">
        <div class="bpm-dot" style="background:#2E8B5A">2</div>
        <h4>Implementation</h4>
        <p>Develop and deploy the defined strategy, assembling all components, services, resources and IT providers.</p>
      </div>
      <div class="bpm-step">
        <div class="bpm-dot" style="background:#4DB87A">3</div>
        <h4>Evaluation</h4>
        <p>Monitor and track IT management to verify correct operation and compliance with business plan requirements.</p>
      </div>
    </div>
  </div>

  <!-- 6. TOOLS -->
  <div class="tools-section">
    <p class="section-label">Implementation Stages</p>
    <p class="section-title">Key Tools per Stage</p>
    <div class="tools-row">
      <div class="tool-pill">
        <div class="tool-dot" style="background:#1A5C34"></div>
        <strong>BPA</strong>
        <span>Business Process Analysis — simulation &amp; publication of processes</span>
      </div>
      <div class="tool-pill">
        <div class="tool-dot" style="background:#2E8B5A"></div>
        <strong>ABPD</strong>
        <span>Automated Business Process Discovery — discovers processes from electronic logs</span>
      </div>
      <div class="tool-pill">
        <div class="tool-dot" style="background:#4DB87A"></div>
        <strong>BAM</strong>
        <span>Business Activity Monitoring — real-time KPI tracking &amp; decision support</span>
      </div>
      <div class="tool-pill">
        <div class="tool-dot" style="background:#F5A623"></div>
        <strong>BRMS</strong>
        <span>Business Rule Management Systems — codifies policies &amp; business rules dynamically</span>
      </div>
      <div class="tool-pill">
        <div class="tool-dot" style="background:#C07A00"></div>
        <strong>BPMS</strong>
        <span>Business Process Management Suites — models, simulates &amp; automates process execution</span>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- 7. SGSTI / ISO 20000 -->
  <div class="sgsti-section">
    <p class="section-label">IT Service Management</p>
    <p class="section-title">ITSMS Model — ISO/IEC 20000-1</p>
    <table class="sgsti-table">
      <thead>
        <tr>
          <th>Layer / Category</th>
          <th>Key Processes</th>
          <th>Standard</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Management System</strong></td>
          <td>Direction responsibilities · Documentation requirements · Competence &amp; training</td>
          <td><span class="badge">ISO/IEC 20000-1</span></td>
        </tr>
        <tr>
          <td><strong>Planning &amp; Implementation</strong></td>
          <td>Plan → Do → Check → Act (PDCA cycle)</td>
          <td><span class="badge">PDCA</span></td>
        </tr>
        <tr>
          <td><strong>Service Provisioning</strong></td>
          <td>Service reports · Service level management · IT budgeting &amp; accounting</td>
          <td><span class="badge">SLM</span></td>
        </tr>
        <tr>
          <td><strong>Control Processes</strong></td>
          <td>Capacity · Availability &amp; continuity · Information security · Configuration · Change management</td>
          <td><span class="badge">ITSM</span></td>
        </tr>
        <tr>
          <td><strong>Delivery Processes</strong></td>
          <td>Release &amp; deployment management</td>
          <td><span class="badge">Deploy</span></td>
        </tr>
        <tr>
          <td><strong>Resolution Processes</strong></td>
          <td>Incident management · Problem management</td>
          <td><span class="badge">Incident</span></td>
        </tr>
        <tr>
          <td><strong>Relationship Processes</strong></td>
          <td>Business relationship management · Supplier management</td>
          <td><span class="badge">Relations</span></td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- 8. CONCLUSION -->
  <div class="conclusion">
    <h2>Key Takeaway</h2>
    <p>A robust IT governance structure requires leaders with broad technical, technological and management knowledge. All organisational components — people, processes, tools, culture and continuous improvement — must work in harmony so that business processes generate synergy with IT management, fulfilling the organisation's mission, vision and strategic plan.</p>
    <div class="iso-badge">
      <strong>Governing Standard:</strong> ISO/IEC 38500 · ISO/IEC 20000-1 · COBIT 2019
    </div>
  </div>

</div><!-- /page -->
</body>
</html>
