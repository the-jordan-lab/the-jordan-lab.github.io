---
layout: default
title: "The Jordan Lab"
date: 2025-06-26
tags: [github-pages, website, dark-mode]
---

<style>
:root{
  --bg:#181c20;--fg:#f6f6f6;--muted:#b8bcc2;--accent:#39e0a0;
  --card:#22262b;--border:#3a4049;--pill-bg:#23272f;--pill-border:#24292f;
  font-family:Inter,"Segoe UI",Arial,sans-serif;line-height:1.6;
}
body{margin:0;background:var(--bg);color:var(--fg);}
a{color:var(--accent);text-decoration:none;}a:hover{text-decoration:underline;}
hr.divider{border:none;border-top:1.5px solid var(--border);margin:2.5rem auto;width:90%;}
.hero{padding:4rem 1rem 2.5rem;padding-top:calc(4rem+52px);text-align:center;}
.hero h1{font-size:3.2rem;font-weight:700;letter-spacing:-2px;margin:0 0 .8rem;}
.hero p{font-size:1.25rem;color:var(--muted);max-width:600px;margin:0 auto;}
.pills{display:flex;flex-wrap:wrap;gap:.7em;justify-content:center;margin-bottom:3rem;}
.pill{background:var(--pill-bg);border:1px solid var(--pill-border);
      border-radius:2em;padding:.65rem 1.4rem;font-size:1rem;}
.container{width:90%;max-width:1100px;margin:0 auto;}
.grid-cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:1.4rem;}
.card{background:var(--card);border-radius:9px;padding:1.2rem 1rem;
      box-shadow:0 1px 4px rgba(0,0,0,.06);}
.card-title{font-weight:600;font-size:1.05rem;margin:0 0 .3rem;}
.card-desc{font-size:.99rem;color:var(--muted);}
details summary{cursor:pointer;font-size:1.04rem;color:var(--accent);}
footer{border-top:1px solid #24272e;text-align:center;font-size:.98rem;padding:1.2rem 0;
       margin-top:3.5rem;color:#65696f;}
@media(max-width:600px){.hero h1{font-size:2.4rem;}}
</style>

<div class="hero">
  <h1>The Jordan Group</h1>
  <p>Advancing our understanding of metabolic regulation, post-transcriptional
     control, and adipose tissue biology</p>
</div>

<div class="pills">
  <a class="pill" href="https://github.com/the-jordan-lab">🏠 Home</a>
  <a class="pill" href="https://github.com/orgs/the-jordan-lab/repositories">📊 Repositories</a>
  <a class="pill" href="https://github.com/orgs/the-jordan-lab/people">👥 Members</a>
  <a class="pill" href="https://github.com/orgs/the-jordan-lab/teams">👨‍👩‍👧‍👦 Teams</a>
</div>

<hr class="divider">

<!-- About -->
<div class="container" style="max-width:680px;margin-bottom:2.5rem;">
  <h2>About Our Research</h2>
  <ul>
    <li>Post-transcriptional gene regulation</li>
    <li>Adipose tissue development and maintenance</li>
    <li>Hepatic metabolism and lipid homeostasis</li>
    <li>Chromatin remodeling in metabolic disease</li>
  </ul>
</div>

<!-- Projects fetched dynamically -->
<div class="container" style="margin-bottom:3rem;">
  <h2>Research Projects</h2>
  <div id="projects" class="grid-cards">
    <p style="color:var(--muted);">Loading repositories…</p>
  </div>
</div>

<!-- Resources / Lab Management / Example Analyses blocks unchanged -->
<!-- … you can paste the earlier static sections here … -->

<footer>
  © 2025 The Jordan Lab · Florida State University<br>
  <span style="font-size:.92rem;">Internal resource for lab members. For external
    inquiries contact <a href="mailto:jmjordan@fsu.edu">jmjordan@fsu.edu</a>.</span>
</footer>

<script>
(async()=>{
  const org = 'the-jordan-lab';
  const url = `https://api.github.com/orgs/${org}/repos?per_page=100&type=public`;
  /* If you need private repos too, create a classic PAT with repo scope and
     add: headers:{Authorization:`token YOUR_TOKEN`} */
  try{
    const res = await fetch(url); const repos = await res.json();
    repos.sort((a,b)=>a.name.localeCompare(b.name));
    const wrap = document.getElementById('projects'); wrap.innerHTML='';
    repos.forEach(r=>{
      const card=document.createElement('div'); card.className='card';
      card.innerHTML=`
        <a class="card-title" href="${r.html_url}">${r.name.replace(/-/g,' ')}</a>
        <div class="card-desc">${r.description||'&nbsp;'}</div>`;
      wrap.appendChild(card);
    });
    if(!repos.length) wrap.innerHTML='<p style="color:var(--muted);">No public repos found.</p>';
  }catch(e){
    document.getElementById('projects').innerHTML =
      '<p style="color:#e06666;">Error loading repos.</p>';
    console.error(e);
  }
})();
</script>

