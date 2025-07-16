<!-- index.html or index.md (with HTML passthrough) -->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>The Jordan Lab · GitHub Repos</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    :root {
      --bg: #181c20;
      --fg: #f6f6f6;
      --muted: #b8bcc2;
      --accent: #39e0a0;
      --card: #22262b;
      --border: #3a4049;
      --shadow: 0 2px 8px rgba(0,0,0,0.10);
      --link: #39e0a0;
      --link-hover: #2bbd85;
    }
    @media (prefers-color-scheme: light) {
      :root {
        --bg: #f6f6f6;
        --fg: #181c20;
        --muted: #444;
        --accent: #1e8e5f;
        --card: #fff;
        --border: #e0e0e0;
        --shadow: 0 2px 8px rgba(0,0,0,0.04);
        --link: #1e8e5f;
        --link-hover: #39e0a0;
      }
    }
    body {
      background: var(--bg);
      color: var(--fg);
      font-family: Inter, "Segoe UI", Arial, sans-serif;
      margin: 0;
      min-height: 100vh;
      line-height: 1.6;
    }
    header {
      text-align: center;
      padding: 2.5rem 1rem 1.5rem;
    }
    header h1 {
      font-size: 2.5rem;
      margin: 0 0 0.5rem;
      font-weight: 700;
      letter-spacing: -1px;
    }
    header p {
      color: var(--muted);
      font-size: 1.15rem;
      margin: 0;
    }
    main {
      width: 95%;
      max-width: 1100px;
      margin: 0 auto 2.5rem;
    }
    .repo-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
      margin-top: 2rem;
    }
    .repo-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      box-shadow: var(--shadow);
      padding: 1.2rem 1rem 1rem;
      display: flex;
      flex-direction: column;
      transition: transform 0.12s;
    }
    .repo-card:hover {
      transform: translateY(-3px) scale(1.02);
      border-color: var(--accent);
    }
    .repo-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
      color: var(--link);
      text-decoration: none;
      word-break: break-all;
    }
    .repo-title:hover {
      color: var(--link-hover);
      text-decoration: underline;
    }
    .repo-desc {
      color: var(--muted);
      font-size: 0.98rem;
      margin-bottom: 0.2rem;
      min-height: 2.2em;
    }
    footer {
      text-align: center;
      color: var(--muted);
      font-size: 0.98rem;
      padding: 1.5rem 0 0.5rem;
      border-top: 1px solid var(--border);
      margin-top: 2.5rem;
    }
    @media (max-width: 600px) {
      header h1 { font-size: 1.6rem; }
      .repo-grid { gap: 1rem; }
    }
  </style>
</head>
<body>
  <header>
    <h1>The Jordan Lab</h1>
    <p>Advancing our understanding of metabolic regulation, post-transcriptional control, and adipose tissue biology</p>
  </header>
  <main>
    <section>
      <h2 style="font-size:1.3rem;font-weight:500;margin-bottom:0.5rem;">Public Repositories</h2>
      <div id="repo-list" class="repo-grid" aria-live="polite">
        <div style="color:var(--muted);font-size:1.1rem;">Loading repositories…</div>
      </div>
    </section>
  </main>
  <footer>
    &copy; 2025 The Jordan Lab · Florida State University &mdash; <a href="mailto:jmjordan@fsu.edu" style="color:var(--link);">Contact</a>
  </footer>
  <script>
    (async () => {
      const org = 'the-jordan-lab';
      const exclude = ['the-jordan-lab.github.io']; // Exclude the website repo
      const api = `https://api.github.com/orgs/${org}/repos?per_page=100&type=public`;
      const container = document.getElementById('repo-list');
      try {
        const res = await fetch(api);
        if (!res.ok) throw new Error('GitHub API error');
        let repos = await res.json();
        repos = repos.filter(r => !exclude.includes(r.name));
        repos.sort((a, b) => a.name.localeCompare(b.name));
        if (repos.length === 0) {
          container.innerHTML = '<div style="color:var(--muted);font-size:1.1rem;">No repositories found.</div>';
          return;
        }
        container.innerHTML = '';
        for (const repo of repos) {
          const card = document.createElement('div');
          card.className = 'repo-card';
          card.innerHTML = `
            <a class="repo-title" href="${repo.html_url}" target="_blank" rel="noopener">${repo.name.replace(/-/g, ' ')}</a>
            <div class="repo-desc">${repo.description ? repo.description : '<span style="color:var(--border);">No description</span>'}</div>
          `;
          container.appendChild(card);
        }
      } catch (e) {
        container.innerHTML = '<div style="color:#e57373;">Error loading repositories.</div>';
      }
    })();
  </script>
</body>
</html>

