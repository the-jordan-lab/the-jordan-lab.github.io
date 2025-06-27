---
layout: default
title: "The Jordan Lab"
date: 2025-06-26
tags: [github-pages, website, dark-mode]
---

<!-- Global layout: flex column -->
<style>
:root {
  --bg:#181c20; --fg:#f6f6f6; --muted:#b8bcc2; --accent:#39e0a0;
  --card:#22262b; --border:#3a4049; --pill-bg:#23272f; --pill-border:#24292f;
  font-family: Inter,"Segoe UI",Arial,sans-serif; line-height:1.6;
}
body{
  margin:0; background:var(--bg); color:var(--fg);
  display:flex; flex-direction:column; min-height:100vh;
}
main{flex:1 0 auto;}          /* pushes footer down */
a{color:var(--accent);text-decoration:none;}
a:hover{text-decoration:underline;}
hr.divider{border:none;border-top:1.5px solid var(--border);
           margin:2.5rem auto;width:90%;}
/* hero offset for theme navbar */
.hero{padding:4rem 1rem 2.5rem; padding-top:calc(4rem+52px);text-align:center;}
.hero h1{font-size:3.2rem;font-weight:700;letter-spacing:-2px;margin:0 0 .8rem;}
.hero p{font-size:1.25rem;color:var(--muted);max-width:600px;margin:0 auto;}
/* pills */
.pills{display:flex;flex-wrap:wrap;gap:.7em;justify-content:center;margin-bottom:3rem;}
.pill{background:var(--pill-bg);border:1px solid var(--pill-border);
      border-radius:2em;padding:.65rem 1.4rem;font-size:1rem;}
/* cards grid */
.grid-cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:1.4rem;}
.card{background:var(--card);border-radius:9px;padding:1.2rem 1rem;
      box-shadow:0 1px 4px rgba(0,0,0,.06);}
.card-title{font-weight:600;font-size:1.05rem;margin:0 0 .3rem;}
.card-desc{font-size:.99rem;color:var(--muted);}
details summary{cursor:pointer;font-size:1.04rem;color:var(--accent);}
footer{flex-shrink:0;border-top:1px solid #24272e;text-align:center;
       font-size:.98rem;padding:1.2rem 0;margin-top:3.5rem;color:#65696f;}
@media(max-width:600px){.hero h1{font-size:2.4rem;}}
</style>

<main>
  <div class="hero">
    <h1>The Jordan Group</h1>
    <p>Advancing our understanding of metabolic regulation,
       post-transcriptional control, and adipose tissue biology</p>
  </div>

  <div class="pills">
    <a class="pill" href="https://github.com/the-jordan-lab">🏠 Home</a>
    <a class="pill" href="https://github.com/orgs/the-jordan-lab/repositories">
      📊 Repositories</a>
    <a class="pill" href="https://github.com/orgs/the-jordan-lab/people">
      👥 Members</a>
    <a class="pill" href="https://github.com/orgs/the-jordan-lab/teams">
      👨‍👩‍👧‍👦 Teams</a>
  </div>

  <hr class="divider">

  <div style="max-width:680px;margin:0 auto 2.5rem;">
    <h2>About Our Research</h2>
    <ul>
      <li>Post-transcriptional gene regulation</li>
      <li>Adipose tissue development and maintenance</li>
      <li>Hepatic metabolism and lipid homeostasis</li>
      <li>Chromatin remodeling in metabolic disease</li>
    </ul>
  </div>

  <div style="max-width:1100px;margin:0 auto 3rem;">
    <h2>Research Projects</h2>
    <div class="grid-cards">
      <div class="card">
        <a class="card-title"
           href="https://github.com/the-jordan-lab/proj001-Ybx1_in_WAT">
          YBX1 in White Adipose Tissue</a>
        <div class="card-desc">YBX1 function in white adipose tissue
          development and maintenance</div>
      </div>
      <div class="card">
        <a class="card-title"
           href="https://github.com/the-jordan-lab/proj002-Ybx1_in_liver_metab">
          YBX1 in Hepatic Metabolism</a>
        <div class="card-desc">YBX1 role in hepatic metabolism and lipid
          homeostasis</div>
      </div>
      <!-- add more cards as needed -->
    </div>
    <div style="color:#888;font-size:.97rem;margin-top:.8rem;">
      Visit <a href="https://github.com/the-jordan-lab?tab=repositories">
      all repositories</a> for more projects.
    </div>
  </div>

  <!-- (Resources, Lab Management, Example Analyses blocks unchanged) -->
</main>

<footer>
  © 2025 The Jordan Lab · Florida State University<br>
  <span style="font-size:.92rem;">Internal resource for lab members. For
    external inquiries contact
    <a href="mailto:jmjordan@fsu.edu">jmjordan@fsu.edu</a>.</span>
</footer>
