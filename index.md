# index.html
---
layout: default
title: "The Jordan Lab"
date: 2025-06-26
tags: [github-pages, website, dark-mode]
---

<!-- Main Container -->
<style>
/* --- Jordan Lab dark-mode palette --- */
:root {
  --bg: #181c20;
  --fg: #f6f6f6;
  --muted: #b8bcc2;
  --accent: #39e0a0;
  --card: #22262b;
  --border: #3a4049;
  --pill-bg: #23272f;
  --pill-border: #24292f;
  font-family: Inter, "Segoe UI", Arial, sans-serif;
  line-height: 1.6;
}

/* Global */
body {
  margin: 0;
  background: var(--bg);
  color: var(--fg);
}
a {
  color: var(--accent);
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
hr.divider {
  border: none;
  border-top: 1.5px solid var(--border);
  width: 90%;
  margin: 2.5rem auto;
}

/* Layout helpers */
.container {
  width: 90%;
  max-width: 1100px;
  margin: 0 auto;
}
.grid-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.4rem;
}

/* Hero */
.hero {
  text-align: center;
  padding: 4rem 1rem 2.5rem;
}
.hero h1 {
  font-size: 3.2rem;
  font-weight: 700;
  letter-spacing: -2px;
  margin: 0 0 0.8rem;
}
.hero p {
  font-size: 1.25rem;
  color: var(--muted);
  max-width: 600px;
  margin: 0 auto;
}

/* Pills */
.pills {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7em;
  justify-content: center;
  margin-bottom: 3rem;
}
.pill {
  background: var(--pill-bg);
  border: 1px solid var(--pill-border);
  border-radius: 2em;
  padding: 0.65rem 1.4rem;
  font-size: 1rem;
}

/* Cards */
.card {
  background: var(--card);
  border-radius: 9px;
  padding: 1.2rem 1rem;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.06);
}
.card-title {
  font-weight: 600;
  font-size: 1.05rem;
  margin: 0 0 0.3rem;
}
.card-desc {
  font-size: 0.99rem;
  color: var(--muted);
}

/* Collapsibles */
details summary {
  cursor: pointer;
  font-size: 1.04rem;
  color: var(--accent);
}

/* Footer */
footer {
  border-top: 1px solid #24272e;
  text-align: center;
  font-size: 0.98rem;
  padding: 1.2rem 0;
  margin-top: 3.5rem;
  color: #65696f;
}

/* Responsive tweaks */
@media (max-width: 600px) {
  .hero h1 {
    font-size: 2.4rem;
  }
}
</style>

<div class="hero">
  <h1>The Jordan Group</h1>
  <p>
    Advancing our understanding of metabolic regulation, post-transcriptional
    control, and adipose tissue biology
  </p>
</div>

<div class="pills">
  <a class="pill" href="https://github.com/the-jordan-lab">🏠 Home</a>
  <a class="pill"
     href="https://github.com/orgs/the-jordan-lab/repositories">📊 Repositories</a>
  <a class="pill"
     href="https://github.com/orgs/the-jordan-lab/people">👥 Members</a>
  <a class="pill"
     href="https://github.com/orgs/the-jordan-lab/teams">👨‍👩‍👧‍👦 Teams</a>
</div>

<hr class="divider">

<!-- About -->
<div class="container" style="max-width: 680px; margin-bottom: 2.5rem;">
  <h2>About Our Research</h2>
  <ul>
    <li>Post-transcriptional gene regulation</li>
    <li>Adipose tissue development and maintenance</li>
    <li>Hepatic metabolism and lipid homeostasis</li>
    <li>Chromatin remodeling in metabolic disease</li>
  </ul>
</div>

<!-- Projects -->
<div class="container" style="margin-bottom: 3rem;">
  <h2>Research Projects</h2>
  <div class="grid-cards">
    <div class="card">
      <a class="card-title"
         href="https://github.com/the-jordan-lab/proj001-Ybx1_in_WAT">
        YBX1 in White Adipose Tissue
      </a>
      <div class="card-desc">
        YBX1 function in white adipose tissue development and maintenance
      </div>
    </div>
    <div class="card">
      <a class="card-title"
         href="https://github.com/the-jordan-lab/proj002-Ybx1_in_liver_metab">
        YBX1 in Hepatic Metabolism
      </a>
      <div class="card-desc">
        YBX1 role in hepatic metabolism and lipid homeostasis
      </div>
    </div>
    <!-- Add more cards here -->
  </div>
  <div style="color:#888; font-size:0.97rem; margin-top:0.8rem;">
    Visit <a href="https://github.com/the-jordan-lab?tab=repositories">all
    repositories</a> for more projects.
  </div>
</div>

<!-- Resources -->
<div class="container" style="max-width: 700px; margin-bottom: 2.5rem;">
  <h2>Resources &amp; Documentation</h2>

  <details>
    <summary>Lab Protocols &amp; SOPs</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/protocols">Protocols
        Repository</a> &mdash; SOPs for lab techniques
      </li>
    </ul>
  </details>

  <details>
    <summary>Templates &amp; Forms</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/templates">Templates
        Repository</a> &mdash; Data collection &amp; project planning
      </li>
    </ul>
  </details>

  <details>
    <summary>Training &amp; Guides</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/guides">Guides Repository</a>
        &mdash; Equipment, software, and best practices
      </li>
    </ul>
  </details>

  <details>
    <summary>Data &amp; References</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/library">Library
        Repository</a> &mdash; Literature &amp; references
      </li>
      <li>
        <a href="https://github.com/the-jordan-lab/omics-dbs">Omics Databases</a>
      </li>
      <li>
        <a href="https://github.com/the-jordan-lab/primers">Primer Database</a>
      </li>
    </ul>
  </details>
</div>

<!-- Lab Management -->
<div class="container" style="max-width: 700px; margin-bottom: 2.5rem;">
  <h2>Lab Management</h2>

  <details>
    <summary>New Member Resources</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/onboarding">Onboarding
        Repository</a>
      </li>
    </ul>
  </details>

  <details>
    <summary>Inventory &amp; Tracking</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/registries">Registries
        Repository</a>
      </li>
    </ul>
  </details>

  <details>
    <summary>Safety &amp; Compliance</summary>
    <ul>
      <li>
        <a
          href="https://github.com/the-jordan-lab/environmental_health_and_safety">
          EHS Repository</a>
      </li>
    </ul>
  </details>

  <details>
    <summary>Presentations &amp; Communications</summary>
    <ul>
      <li>
        <a href="https://github.com/the-jordan-lab/presentations">Presentations
        Repository</a>
      </li>
    </ul>
  </details>
</div>

<!-- Example Analyses -->
<div class="container" style="max-width: 700px; margin-bottom: 2.5rem;">
  <h2>Example Analyses</h2>
  <ul>
    <li>
      <a
        href="https://github.com/the-jordan-lab/proj002-Ybx1_in_liver_metab/tree/main/ca018_pparg_and_pparg_regulators_in_huh7_oapav6_glucose_bodipy-orflo">
        ORO Fluorescence Analysis</a> &ndash; Automated Oil Red O quantification
    </li>
    <li>
      <a
        href="https://github.com/the-jordan-lab/templates/tree/main/for-workflow-agent">
        RT-qPCR ΔΔCt Template</a> &ndash; Standardized qPCR analysis
    </li>
    <li>
      <a
        href="https://github.com/the-jordan-lab/proj001-Ybx1_in_WAT/tree/main/jj002-ybx1-conservation-analysis-main">
        YBX1 Conservation Analysis</a> &ndash; Cross-species evolutionary
        analysis
    </li>
  </ul>
</div>

<!-- Footer -->
<footer>
  © 2025 The Jordan Lab &middot; Florida State University<br>
  <span style="font-size: 0.92rem;">
    Internal resource for lab members.
    For external inquiries contact
    <a href="mailto:jmjordan@fsu.edu">jmjordan@fsu.edu</a>.
  </span>
</footer>
