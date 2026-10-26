<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Sufiyan Majid | Mechanical & Product Engineering</title>
<style>
:root {
  color-scheme: light dark;
  --site-primary: #132c45;
  --site-secondary: #dce8f0;
  --site-background: #f4f7f9;
  --site-on-primary: #ffffff;
  --site-on-secondary: #18334b;
  --site-on-background: #152a3c;
  --site-font-body: Inter, "Segoe UI", Arial, sans-serif;
  --site-font-heading: "Arial Narrow", "Segoe UI", Arial, sans-serif;
  --site-heading-scale: 1;
  --site-spacing-scale: 1;
  --site-radius-scale: 1;
  --site-decoration-opacity: 1;
  --surface: light-dark(#ffffff, #17222d);
  --surface-soft: light-dark(#edf2f6, #1d2c39);
  --ink: light-dark(#152a3c, #edf4f8);
  --muted: light-dark(#5a6d7e, #a8b9c7);
  --line: light-dark(#d4dee6, #344656);
  --accent: light-dark(#087e9c, #65c6de);
  --good: light-dark(#1a755d, #75d0ae);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: var(--site-font-body); background: var(--site-background); color: var(--site-on-background); line-height: 1.55; }
#site-root { min-height: 100vh; width: 100%; border-radius: 0; background-color: var(--site-background); color: var(--site-on-background); }
a { color: inherit; }
button, input { font: inherit; }
.wrap { width: min(1160px, calc(100% - 40px)); margin: 0 auto; }
.topbar { background: var(--site-primary); color: var(--site-on-primary); border-bottom: 3px solid var(--accent); }
.nav { min-height: 74px; display: flex; align-items: center; justify-content: space-between; gap: 22px; }
.brand { display: flex; gap: 12px; align-items: center; text-decoration: none; font-weight: 800; letter-spacing: .02em; }
.brand-mark { display: grid; place-items: center; width: 38px; height: 38px; border: 1px solid #7da6bf; font-size: 12px; letter-spacing: .08em; }
.navlinks { display: flex; flex-wrap: wrap; gap: 22px; font-size: 13px; color: #d4e1eb; }
.navlinks a { text-decoration: none; }
.navlinks a:hover { color: #fff; text-decoration: underline; text-underline-offset: 5px; }
.hero { position: relative; overflow: hidden; background: var(--site-primary); color: #fff; padding: calc(72px * var(--site-spacing-scale)) 0 calc(64px * var(--site-spacing-scale)); }
.hero-grid { display: grid; grid-template-columns: 1.15fr .85fr; gap: 42px; align-items: center; }
.kicker { text-transform: uppercase; letter-spacing: .17em; font-size: 11px; font-weight: 800; color: #91d9e9; }
h1,h2,h3 { font-family: var(--site-font-heading); line-height: 1.12; margin: 0; }
h1 { font-size: calc(clamp(38px, 5vw, 66px) * var(--site-heading-scale)); letter-spacing: -.035em; margin: 18px 0; max-width: 720px; }
.hero p { max-width: 650px; color: #d5e1e9; font-size: 16px; }
.hero-actions { display: flex; gap: 12px; flex-wrap: wrap; margin-top: 28px; }
.btn { display: inline-flex; align-items: center; justify-content: center; gap: 9px; padding: 12px 17px; text-decoration: none; font-weight: 750; font-size: 13px; border: 1px solid transparent; border-radius: calc(4px * var(--site-radius-scale)); cursor: pointer; }
.btn-primary { background: #8ed9e8; color: #102b41; }
.btn-outline { border-color: #6f91a8; color: #fff; background: transparent; }
.btn:hover { transform: translateY(-1px); }
.blueprint { border: 1px solid #426078; padding: 14px; background: #10263a; position: relative; }
.blueprint svg { display: block; width: 100%; height: auto; }
.blueprint-label { display: flex; justify-content: space-between; gap: 10px; padding-top: 12px; color: #a8c3d4; font-size: 10px; letter-spacing: .12em; text-transform: uppercase; }
.hero-decor { position: absolute; inset: 0 0 0 auto; width: 35%; opacity: calc(.16 * var(--site-decoration-opacity)); pointer-events: none; background-image: linear-gradient(30deg, transparent 49.5%, #9bbbd0 50%, transparent 50.5%), linear-gradient(150deg, transparent 49.5%, #9bbbd0 50%, transparent 50.5%); background-size: 46px 46px; mask-image: linear-gradient(to left, black, transparent); }
.metrics { background: var(--surface); border-bottom: 1px solid var(--line); }
.metrics-grid { display: grid; grid-template-columns: repeat(4,1fr); }
.metric { padding: 24px 18px; border-right: 1px solid var(--line); }
.metric:first-child { padding-left: 0; }
.metric:last-child { border-right: 0; }
.metric strong { display: block; font-family: var(--site-font-heading); font-size: 27px; letter-spacing: -.03em; color: var(--accent); }
.metric span { display: block; color: var(--muted); font-size: 12px; margin-top: 3px; }
section { padding: calc(72px * var(--site-spacing-scale)) 0; }
.section-head { display: flex; justify-content: space-between; align-items: end; gap: 24px; margin-bottom: 30px; }
.section-head h2 { font-size: calc(34px * var(--site-heading-scale)); letter-spacing: -.025em; }
.section-head p { color: var(--muted); max-width: 480px; margin: 0; font-size: 14px; }
.section-number { color: var(--accent); font-size: 11px; font-weight: 800; letter-spacing: .16em; display: block; margin-bottom: 10px; }
.project-grid { display: grid; grid-template-columns: repeat(2,minmax(0,1fr)); gap: 18px; }
.project { background: var(--surface); border: 1px solid var(--line); min-width: 0; display: flex; flex-direction: column; }
.project-visual { background: var(--surface-soft); border-bottom: 1px solid var(--line); padding: 16px; min-height: 210px; display: grid; place-items: center; }
.project-visual svg { width: 100%; max-width: 450px; max-height: 205px; }
.project-body { padding: 24px; display: flex; flex-direction: column; flex: 1; }
.project-meta { display: flex; justify-content: space-between; gap: 10px; flex-wrap: wrap; color: var(--accent); font-size: 10px; font-weight: 800; letter-spacing: .1em; text-transform: uppercase; }
.project h3 { font-size: 24px; margin: 12px 0; }
.project p { margin: 0 0 17px; color: var(--muted); font-size: 14px; }
.tags { display: flex; gap: 7px; flex-wrap: wrap; margin: auto 0 18px; }
.tag { padding: 5px 8px; background: var(--surface-soft); border: 1px solid var(--line); font-size: 10px; color: var(--ink); }
.details-toggle { align-self: flex-start; background: none; border: 0; padding: 8px 0; color: var(--accent); font-weight: 800; font-size: 12px; cursor: pointer; }
.project-details { border-top: 1px solid var(--line); padding-top: 15px; margin-top: 5px; font-size: 13px; color: var(--muted); }
.project-details[hidden] { display: none; }
.project-details strong { color: var(--ink); }
.note { font-size: 11px; color: var(--muted); border-left: 3px solid var(--accent); padding: 10px 13px; background: var(--surface-soft); margin-top: 20px; }
.capabilities { background: var(--surface-soft); border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); }
.cap-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1px; background: var(--line); border: 1px solid var(--line); }
.cap { background: var(--surface); padding: 24px; }
.cap-index { color: var(--accent); font-size: 11px; font-weight: 800; letter-spacing: .12em; }
.cap h3 { margin: 12px 0 9px; font-size: 20px; }
.cap p { margin: 0; font-size: 13px; color: var(--muted); }
.tool-list { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 24px; }
.tool { border: 1px solid var(--line); background: var(--surface); padding: 10px 13px; font-size: 12px; font-weight: 700; }
.timeline { border-top: 1px solid var(--line); }
.role { display: grid; grid-template-columns: 190px 1fr; gap: 28px; padding: 25px 0; border-bottom: 1px solid var(--line); }
.role-date { font-size: 12px; color: var(--muted); }
.role h3 { font-size: 20px; margin-bottom: 5px; }
.role-org { font-size: 13px; color: var(--accent); font-weight: 750; }
.role p { margin: 10px 0 0; color: var(--muted); font-size: 13px; max-width: 780px; }
.contact { background: var(--site-primary); color: #fff; padding: 58px 0; }
.contact-inner { display: flex; align-items: center; justify-content: space-between; gap: 28px; }
.contact h2 { font-size: calc(34px * var(--site-heading-scale)); }
.contact p { color: #c6d8e4; max-width: 600px; font-size: 14px; }
.contact-links { display: flex; gap: 10px; flex-wrap: wrap; }
.contact-links a { color: #fff; border: 1px solid #58748b; text-decoration: none; padding: 11px 14px; font-size: 12px; }
footer { background: var(--site-primary); color: #a9c0d0; border-top: 1px solid #36536b; padding: 18px 0; font-size: 10px; letter-spacing: .06em; }
.footer-inner { display: flex; justify-content: space-between; gap: 16px; flex-wrap: wrap; }
@media (max-width: 780px) {
  .wrap { width: min(100% - 28px, 620px); }
  .nav { align-items: flex-start; padding: 17px 0; flex-direction: column; }
  .navlinks { gap: 14px; }
  .hero { padding: 48px 0; }
  .hero-grid { grid-template-columns: 1fr; gap: 30px; }
  .blueprint { max-width: 520px; }
  .metrics-grid { grid-template-columns: repeat(2,1fr); }
  .metric { border-bottom: 1px solid var(--line); padding: 18px 12px; }
  .metric:first-child { padding-left: 12px; }
  .metric:nth-child(2) { border-right: 0; }
  .metric:nth-child(3), .metric:nth-child(4) { border-bottom: 0; }
  section { padding: 48px 0; }
  .section-head { display: block; }
  .section-head p { margin-top: 14px; }
  .project-grid, .cap-grid { grid-template-columns: 1fr; }
  .role { grid-template-columns: 1fr; gap: 8px; }
  .contact-inner { align-items: flex-start; flex-direction: column; }
}
@media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } .btn:hover { transform: none; } }
</style>
</head>
<body>
<div id="site-root">
<header class="topbar">
  <div class="wrap nav">
    <a class="brand" href="#home" aria-label="Sufiyan Majid home"><span class="brand-mark">SM / ME</span><span>SUFIYAN MAJID <span style="font-weight:400;color:#a9c3d4">· ENGINEERING PORTFOLIO</span></span></a>
    <nav class="navlinks" aria-label="Main navigation"><a href="#projects">Projects</a><a href="#capabilities">Capabilities</a><a href="#experience">Experience</a><a href="#contact">Contact</a></nav>
  </div>
</header>
<main>
<section class="hero" id="home">
  <div class="hero-decor" aria-hidden="true"></div>
  <div class="wrap hero-grid">
    <div>
      <div class="kicker">Mechanical · Product Development · Reliability</div>
      <h1>Engineering better products through design, analysis &amp; evidence.</h1>
      <p>Mechanical engineer with 8+ years of experience across refrigeration and semiconductor equipment domains. Focused on product development, value engineering, design validation, and resolving field issues with measurable business impact.</p>
      <div class="hero-actions"><a class="btn btn-primary" href="#projects">Explore selected projects <span aria-hidden="true">↘</span></a><a class="btn btn-outline" href="#contact">Contact</a></div>
    </div>
    <div class="blueprint" aria-label="Illustrative technical drawing of a bolted flange assembly">
      <svg viewBox="0 0 520 340" role="img" aria-labelledby="drawing-title drawing-desc">
        <title id="drawing-title">Illustrative mechanical assembly drawing</title><desc id="drawing-desc">A generic flange and bolted-joint sketch with centerlines and dimensions, not a production drawing.</desc>
        <defs><pattern id="grid" width="20" height="20" patternUnits="userSpaceOnUse"><path d="M20 0H0V20" fill="none" stroke="#27445b" stroke-width=".7"/></pattern></defs>
        <rect width="520" height="340" fill="url(#grid)"/>
        <g stroke="#8bd5e6" stroke-width="1.5" fill="none">
          <circle cx="260" cy="160" r="104"/><circle cx="260" cy="160" r="78"/><circle cx="260" cy="160" r="35" stroke-dasharray="4 4"/>
          <circle cx="260" cy="82" r="10"/><circle cx="338" cy="160" r="10"/><circle cx="260" cy="238" r="10"/><circle cx="182" cy="160" r="10"/>
          <path d="M150 160H370M260 50V270" stroke-dasharray="9 5" opacity=".75"/>
          <path d="M156 65L190 95M364 65L330 95M156 255L190 225M364 255L330 225" opacity=".5"/>
          <path d="M156 44H364M156 39V49M364 39V49M260 44V66"/>
          <path d="M390 82V238M385 82H395M385 238H395M365 82H390M365 238H390"/>
          <path d="M390 160H430L450 140"/>
        </g>
        <g fill="#c4e9f1" font-family="monospace" font-size="10"><text x="230" y="34">PCD / REF.</text><text x="399" y="157">SECTION</text><text x="399" y="170">REFERENCE</text><text x="24" y="312">ILLUSTRATIVE CONCEPT ONLY</text><text x="24" y="326" fill="#789fb5">NOT FOR MANUFACTURE</text><text x="267" y="292">CENTERLINE</text></g>
        <g stroke="#8bd5e6" stroke-width="1" fill="none"><path d="M260 245L290 284H260" stroke-dasharray="3 3"/></g>
      </svg>
      <div class="blueprint-label"><span>Technical mindset</span><span>Concept sketch / NTS</span></div>
    </div>
  </div>
</section>
<div class="metrics"><div class="wrap metrics-grid">
  <div class="metric"><strong>$42k</strong><span>Annual warranty cost eliminated*</span></div>
  <div class="metric"><strong>$100k</strong><span>VAVE design savings*</span></div>
  <div class="metric"><strong>8+ years</strong><span>Hands-on engineering experience</span></div>
  <div class="metric"><strong>3 engineers</strong><span>Junior team led at HCL</span></div>
</div></div>
<section id="projects">
  <div class="wrap">
    <div class="section-head"><div><span class="section-number">01 / SELECTED WORK</span><h2>Engineering case studies</h2></div><p>Selected work across reliability, value engineering, product support, and equipment integration. Details are anonymized and intentionally limited to information available in my resume.</p></div>
    <div class="project-grid">
      <article class="project">
        <div class="project-visual">
          <svg viewBox="0 0 440 205" role="img" aria-label="Generic bolted joint technical concept illustration">
            <g fill="none" stroke="#4c7995" stroke-width="1.5"><path d="M35 72H405V104H35Z" fill="#c6d6e1"/><path d="M35 108H405V140H35Z" fill="#a7bdcd"/><path d="M80 72V140M360 72V140" stroke-dasharray="5 4"/><path d="M130 38V166M310 38V166" stroke-dasharray="4 5"/><path d="M118 46H142V117H118ZM298 46H322V117H298Z" fill="#6e91a8"/><path d="M111 46H149L142 36H118Z" fill="#dce7ed"/><path d="M291 46H329L322 36H298Z" fill="#dce7ed"/><path d="M130 25V36M310 25V36M122 25H318M122 21V29M318 21V29"/><path d="M355 72L385 45H410M355 140L385 166H410" stroke-dasharray="3 3"/></g>
            <g fill="#2b5c79" font-size="9" font-family="monospace"><text x="180" y="18">CLAMPED JOINT</text><text x="340" y="39">LOAD PATH</text><text x="20" y="188">CONCEPTUAL SECTION · NOT TO SCALE</text></g>
          </svg>
        </div>
        <div class="project-body"><div class="project-meta"><span>Case 01 / Reliability</span><span>VDI 2230</span></div><h3>Bolted-joint field-failure resolution</h3><p>Evaluated and validated a bolted-joint design to address a critical customer issue and eliminate reported annual warranty costs.</p><div class="tags"><span class="tag">Joint analysis</span><span class="tag">Failure resolution</span><span class="tag">Validation</span><span class="tag">VDI 2230</span></div><button class="details-toggle" aria-expanded="false">View case summary +</button><div class="project-details" hidden><p><strong>Problem:</strong> A field failure identified as a major customer pain point.</p><p><strong>Approach recorded in resume:</strong> Bolted-joint design evaluation and validation in accordance with VDI 2230.</p><p><strong>Reported result:</strong> $42k annual warranty cost eliminated.</p><p><strong>To develop further:</strong> Add approved, non-confidential details on failure mode, preload assumptions, calculation method, validation criteria, and evidence.</p></div></div>
      </article>
      <article class="project">
        <div class="project-visual">
          <svg viewBox="0 0 440 205" role="img" aria-label="Illustration of functional integration and part-count simplification">
            <g stroke="#4c7995" stroke-width="1.5" fill="none"><rect x="25" y="50" width="75" height="65" fill="#d7e4ec"/><rect x="112" y="50" width="75" height="65" fill="#c4d7e4"/><rect x="25" y="123" width="75" height="42" fill="#c4d7e4"/><rect x="112" y="123" width="75" height="42" fill="#d7e4ec"/><path d="M205 105H244M236 97L244 105L236 113" stroke-width="2"/><path d="M260 58H402V150H260Z" fill="#c5d8e5"/><path d="M284 58V150M308 58V150M332 58V150M356 58V150M380 58V150" stroke-dasharray="3 3"/><path d="M260 88H402M260 119H402" stroke-dasharray="3 3"/></g>
            <g fill="#2b5c79" font-size="10" font-family="monospace"><text x="37" y="39">MULTIPLE FUNCTIONS</text><text x="278" y="39">INTEGRATED PART</text><text x="28" y="185">BEFORE</text><text x="260" y="185">AFTER / CONCEPT</text></g>
          </svg>
        </div>
        <div class="project-body"><div class="project-meta"><span>Case 02 / VAVE</span><span>DFM</span></div><h3>Functional integration &amp; design optimization</h3><p>Simplified a multi-function solution into a single component to reduce manufacturing complexity, cycle time, and inventory requirements.</p><div class="tags"><span class="tag">VAVE</span><span class="tag">DFM / DFMA</span><span class="tag">Cost engineering</span><span class="tag">Part consolidation</span></div><button class="details-toggle" aria-expanded="false">View case summary +</button><div class="project-details" hidden><p><strong>Design direction:</strong> Integrate multiple functions into one component.</p><p><strong>Business impact:</strong> $100k savings reported in resume, alongside lower manufacturing complexity, cycle time, and inventory requirements.</p><p><strong>To develop further:</strong> Add approved before/after CAD views, cost breakdown, decision matrix, and implementation status.</p></div></div>
      </article>
      <article class="project">
        <div class="project-visual">
          <svg viewBox="0 0 440 205" role="img" aria-label="Generic gasket seal and housing interface illustration">
            <g fill="none" stroke="#4c7995" stroke-width="1.5"><path d="M68 55H372V79H68Z" fill="#c4d7e4"/><path d="M85 85H355V105H85Z" fill="#e2ebf1"/><path d="M68 111H372V143H68Z" fill="#b1c7d6"/><rect x="100" y="150" width="240" height="18" fill="#d8e4eb"/><path d="M105 83H335" stroke="#087e9c" stroke-width="3"/><path d="M120 85V105M160 85V105M200 85V105M240 85V105M280 85V105M320 85V105" stroke-dasharray="2 3"/><path d="M340 94H382L398 77"/><path d="M98 151L65 171H30" stroke-dasharray="4 3"/></g>
            <g fill="#2b5c79" font-size="10" font-family="monospace"><text x="28" y="32">SEALING INTERFACE</text><text x="302" y="68">GASKET</text><text x="28" y="187">SCHEMATIC · ANONYMIZED</text></g>
          </svg>
        </div>
        <div class="project-body"><div class="project-meta"><span>Case 03 / Quality</span><span>RCA · 8D</span></div><h3>Gasket field-failure corrective action</h3><p>Delivered a root-cause corrective action for a gasket fall-off field issue from investigation through implementation in four months.</p><div class="tags"><span class="tag">Root-cause analysis</span><span class="tag">8D</span><span class="tag">Corrective action</span><span class="tag">Field quality</span></div><button class="details-toggle" aria-expanded="false">View case summary +</button><div class="project-details" hidden><p><strong>Problem:</strong> Gasket fall-off in field use.</p><p><strong>Contribution:</strong> Root-cause corrective action and implementation within a four-month turnaround.</p><p><strong>To develop further:</strong> Add the verified failure mechanism, corrective-action options, validation evidence, and recurrence-monitoring approach if disclosure is approved.</p></div></div>
      </article>
      <article class="project">
        <div class="project-visual">
          <svg viewBox="0 0 440 205" role="img" aria-label="Generic semiconductor vacuum equipment integration sketch">
            <g stroke="#4c7995" stroke-width="1.5" fill="none"><rect x="45" y="40" width="130" height="120" fill="#d5e2ea"/><rect x="61" y="55" width="98" height="40" fill="#eef3f6"/><circle cx="110" cy="126" r="23" fill="#c2d5e2"/><circle cx="110" cy="126" r="10"/><path d="M175 74H228V98H257M175 125H213V147H257"/><rect x="257" y="52" width="135" height="108" fill="#c4d7e4"/><path d="M275 70H374V91H275ZM275 102H374V123H275Z" fill="#e9f0f4"/><path d="M300 160V178M350 160V178M284 178H366"/><path d="M45 172H392" stroke-dasharray="4 4"/></g>
            <g fill="#2b5c79" font-size="10" font-family="monospace"><text x="42" y="25">VACUUM SYSTEM</text><text x="257" y="42">INTEGRATION</text><text x="25" y="194">GENERIC EQUIPMENT SCHEMATIC</text></g>
          </svg>
        </div>
        <div class="project-body"><div class="project-meta"><span>Case 04 / Integration</span><span>Semiconductor</span></div><h3>Vacuum-pump integration projects</h3><p>Delivered three vacuum-pump integration projects at HCL that reduced tool impurity levels and cut the frequency of tool regeneration.</p><div class="tags"><span class="tag">Mechanical integration</span><span class="tag">CAD / drawings</span><span class="tag">PDM / SAP</span><span class="tag">Team leadership</span></div><button class="details-toggle" aria-expanded="false">View case summary +</button><div class="project-details" hidden><p><strong>Scope:</strong> Three vacuum-pump integration projects for semiconductor equipment.</p><p><strong>Reported outcome:</strong> Lower tool impurity levels and reduced regeneration frequency.</p><p><strong>Leadership:</strong> Resume also records leading three junior engineers and coordinating with Safety, Reliability, Marketing, and Purchasing stakeholders.</p><p><strong>To develop further:</strong> Add approved interface drawings, integration constraints, test results, and quantified improvement if available.</p></div></div>
      </article>
    </div>
    <div class="note">Confidentiality note: the diagrams on this page are original generic illustrations created for this portfolio, not company CAD, actual part geometry, or production drawings. All project summaries are based on resume-level facts; no unverified technical details have been added.</div>
  </div>
</section>
<section class="capabilities" id="capabilities">
  <div class="wrap">
    <div class="section-head"><div><span class="section-number">02 / ENGINEERING TOOLKIT</span><h2>Capabilities &amp; methods</h2></div><p>Engineering methods and software listed in my resume, organized around the work they support.</p></div>
    <div class="cap-grid">
      <div class="cap"><span class="cap-index">CAPABILITY 01</span><h3>Product development</h3><p>Requirements definition, concept selection, design reviews, risk assessment, product changes, and manufacturing release.</p></div>
      <div class="cap"><span class="cap-index">CAPABILITY 02</span><h3>Design engineering</h3><p>GD&amp;T, tolerance stack-up, material selection, DFMA, bolted-joint analysis, and detailed drawing release.</p></div>
      <div class="cap"><span class="cap-index">CAPABILITY 03</span><h3>Verification &amp; quality</h3><p>DFMEA, DVP&amp;R, testing and validation, PPAP, FRACAS, RCA, 8D, 5-Why, A3, and Six Sigma methods.</p></div>
      <div class="cap"><span class="cap-index">CAPABILITY 04</span><h3>Value engineering</h3><p>Business cases, costing, VAVE, design simplification, productivity initiatives, and cost / quality trade-offs.</p></div>
      <div class="cap"><span class="cap-index">CAPABILITY 05</span><h3>Cross-functional delivery</h3><p>Project planning, stakeholder management, supplier collaboration, technical presentations, and gate-review approvals.</p></div>
      <div class="cap"><span class="cap-index">CAPABILITY 06</span><h3>Equipment integration</h3><p>Mechanical systems and component integration, prototypes, test interpretation, engineering changes, and PDM/ERP release.</p></div>
    </div>
    <div class="tool-list" aria-label="Software and engineering tools"><span class="tool">CATIA V5</span><span class="tool">Creo 8</span><span class="tool">ANSYS</span><span class="tool">Windchill</span><span class="tool">Teamcenter</span><span class="tool">Oracle Agile e6.0</span><span class="tool">SAP</span><span class="tool">Microsoft Project</span><span class="tool">VDI 2230</span><span class="tool">ASME Y14.5 GD&amp;T</span></div>
  </div>
</section>
<section id="experience">
  <div class="wrap">
    <div class="section-head"><div><span class="section-number">03 / CAREER</span><h2>Experience snapshot</h2></div><p>Professional experience spanning product engineering, mechanical leadership, and design / production fundamentals.</p></div>
    <div class="timeline">
      <div class="role"><div class="role-date">APR 2023 — PRESENT</div><div><h3>Product Engineer</h3><div class="role-org">Trane Technologies · Thermo King product platforms</div><p>Own product development activities across trailer and truck climate-solutions platforms, including design changes, VAVE and quality/reliability projects, field issue resolution, DFMEA/DVP&amp;R, business cases, and design / gate reviews.</p></div></div>
      <div class="role"><div class="role-date">AUG 2019 — APR 2023</div><div><h3>Mechanical Lead Engineer</h3><div class="role-org">HCL Technologies</div><p>Managed engineering changes across mechanical, harnessing, and facilities work; led three junior engineers; delivered three vacuum-pump integration projects; prepared detailed drawings, BOMs, and engineering release documentation.</p></div></div>
      <div class="role"><div class="role-date">AUG 2018 — JUL 2019</div><div><h3>Graduate Engineering Trainee — Design &amp; Production</h3><div class="role-org">Caliper Engineering &amp; Lab Pvt. Ltd.</div><p>Designed, assembled, and leak-tested ball valves; developed parametric 3D models and family tables; supported production, quality, and inventory processes.</p></div></div>
    </div>
    <div class="note">Education: B.E. in Mechanical Engineering, Visvesvaraya Technological University. Additional learning listed in resume includes NVH professional training at IISc Bengaluru and refrigeration-focused courses.</div>
  </div>
</section>
<section class="contact" id="contact">
  <div class="wrap contact-inner">
    <div><span class="section-number">04 / CONNECT</span><h2>Let's solve meaningful engineering problems.</h2><p>Open to senior product engineering and mechanical engineering opportunities in Bengaluru, especially roles involving product development, design engineering, VAVE, reliability, and equipment integration.</p></div>
    <div class="contact-links"><a href="mailto:sufiyanmajid555@gmail.com">Email me ↗</a><a href="https://www.linkedin.com/" target="_blank" rel="noreferrer">LinkedIn profile ↗</a></div>
  </div>
</section>
</main>
<footer><div class="wrap footer-inner"><span>SUFIYAN MAJID / MECHANICAL &amp; PRODUCT ENGINEERING</span><span>Illustrative visuals · Anonymized project summaries · © 2026</span></div></footer>
</div>
<script>
document.querySelectorAll('.details-toggle').forEach(function(button) {
  button.addEventListener('click', function() {
    var details = button.nextElementSibling;
    var willOpen = details.hidden;
    details.hidden = !willOpen;
    button.setAttribute('aria-expanded', String(willOpen));
    button.textContent = willOpen ? 'Hide case summary −' : 'View case summary +';
  });
});
</script>
</body>
</html>
