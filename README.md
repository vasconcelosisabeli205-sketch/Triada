<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My GitHub Project</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    :root {
      --bg: #0d1117;
      --bg-soft: #161b22;
      --border: #30363d;
      --text: #e6edf3;
      --accent: #58a6ff;
      --radius: 12px;
      --shadow: 0 0 20px rgba(0,0,0,0.3)

    body {
      margin: 0;
      padding: 0;
      background: var(--bg);
      color: var(--text);
      font-family: "Inter", system-ui, sans-serif;
      line-height: 1.55;
      animation: fadeIn 0.6s ease;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    header {
      text-align: center;
      padding: 48px 20px 34px;
      background: var(--bg-soft);
      border-bottom: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    header h1 {
      margin: 0;
      font-size: 38px;
      letter-spacing: -0.5px;
    }

    header p {
      margin-top: 10px;
      font-size: 16px;
      opacity: 0.85;
    }

    main {
      max-width: 900px;
      margin: 0 auto;
      padding: 32px 20px 60px;
    }

    section {
      background: var(--bg-soft);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 24px 26px;
      margin-bottom: 26px;
      transition: transform 0.2s ease, border-color 0.3s ease;
    }

    section:hover {
      transform: translateY(-2px);
      border-color: var(--accent);
    }

    h2 {
      margin-top: 0;
      font-size: 22px;
      padding-bottom: 10px;
      border-bottom: 1px solid var(--border);

    ul {
      padding-left: 20px;
    }

    code {
      background: #0d1117;
      padding: 3px 6px;
      border-radius: 6px;
      font-size: 0.95em;
      border: 1px solid var(--border);
    }

    pre {
      background: #0d1117;
      padding: 16px;
      border-radius: var(--radius);
      border: 1px solid var(--border);
      font-size: 0.95em;
      overflow-x: auto;
    }

    .badge {
      display: inline-block;
      padding: 4px 12px;
      font-size: 11px;
      text-transform: uppercase;
      border-radius: 999px;
      background: rgba(255,255,255,0.05);
      border: 1px solid var(--border);
      margin-right: 8px;
      margin-bottom: 8px;
    }

    a {
      color: var(--accent);
      text-decoration: none;
      transition: 0.2s ease;
    }

    a:hover {
      text-decoration: underline;
      color: #79b8ff;
    }

    footer {
      text-align: center;
      opacity: 0.6;
      font-size: 13px;
      padding: 20px 0 40px;
    }
  </style>
</head>
<body>

<header>
  <h1>my-new-github-project</h1>
  <p>A modern, clean starter page for your GitHub repository 🚀</p>
</header>

<main>

  <section>
    <span class="badge">version 1.0.0</span>
    <span class="badge">status: active</span>
    <span class="badge">license: MIT</span>
  </section>

  <section>
    <h2>About</h2>
    <p>
      This project serves as a clean, modern template for GitHub repositories.
      You can customize it, extend it, or use it as a base for documentation,
      landing pages, or portfolio projects.
    </p>
  </section>

  <section>
    <h2>Features</h2>
    <ul>
      <li>⚡ Modern UI with dark mode and animations</li>
      <li>📄 Easy to customize structure</li>
      <li>✨ Optimized for GitHub Pages</li>
      <li>💻 Clean code and typography</li>
    </ul>
  </section>

  <section>
    <h2>Installation</h2>
    <p>Clone the repository:</p>
    <pre><code>git clone https://github.com/USERNAME/my-new-github-project.git
cd my-new-github-project</code></pre>
  </section>

  <section>
    <h2>Links</h2>
    <p>
      Repository: <a href="https://github.com/USERNAME/my-new-github-project" target="_blank">GitHub Link</a>
    </p>
    <p>
      GitHub Pages: <code>https://USERNAME.github.io/my-new-github-project/</code>
    </p>
  </section>

</main>

<footer>
  Created with ❤️ — customize in <code>index.html</code>.
</footer>

</body>
</html>
