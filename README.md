# Dhanus
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>My GitHub Site</title>
  <meta name="description" content="Personal portfolio hosted on GitHub Pages" />
  <!-- Favicon -->
  <link rel="icon" href="data:;base64,iVBORw0KGgo=" />
  
  <style>
    /* ---------- COLOR THEME - customize these variables ---------- */
    :root{
      --bg: #0f1724;            /* page background */
      --card: #0b1020;          /* card / panel */
      --muted: #9aa6bf;         /* muted text */
      --accent: #7c5cff;        /* primary accent */
      --accent-2: #00d4ff;      /* secondary accent */
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.02);
      --radius: 12px;
      --max-w: 1100px;
      --mono: 'SFMono-Regular', ui-monospace, 'Roboto Mono', Menlo, monospace;
    }

    /* ---------- Basic reset ---------- */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: radial-gradient(1000px 400px at 10% 10%, rgba(124,92,255,0.12), transparent),
                  linear-gradient(180deg, var(--bg), #071026 120%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:40px 20px;
      display:flex;
      justify-content:center;
      align-items:flex-start;
      gap:24px;
      min-height:100vh;
    }

    main{width:100%;max-width:var(--max-w)}

    .topbar{
      display:flex;align-items:center;justify-content:space-between;margin-bottom:28px;
      gap:12px
    }

    .brand{
      display:flex;align-items:center;gap:12px;font-weight:700;letter-spacing:0.3px
    }

    .logo{
      width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent),var(--accent-2));
      display:flex;align-items:center;justify-content:center;font-weight:700;color:#041022;box-shadow:0 6px 18px rgba(92,66,255,0.12);
      font-family:var(--mono);font-size:14px
    }

    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600}
    nav a.cta{background:linear-gradient(90deg,var(--accent),var(--accent-2));padding:8px 12px;border-radius:10px;color:#041022}

    /* ---------- GRID ---------- */
    .grid{display:grid;grid-template-columns:1fr 380px;gap:22px}
    @media (max-width:980px){.grid{grid-template-columns:1fr}}

    /* ---------- Left column (content) ---------- */
    .panel{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:22px;border-radius:var(--radius);backdrop-filter: blur(6px);box-shadow:0 6px 26px rgba(2,6,23,0.6)}

    .hero{display:flex;gap:18px;align-items:center}
    .avatar{width:96px;height:96px;border-radius:14px;background:linear-gradient(180deg,var(--glass),transparent);display:flex;align-items:center;justify-content:center;font-weight:700;color:var(--muted);font-size:30px}

    h1{margin:0 0 6px 0;font-size:28px}
    p.lead{margin:0;color:var(--muted)}

    .badges{display:flex;gap:8px;margin-top:12px}
    .badge{padding:6px 10px;border-radius:999px;background:var(--glass);color:var(--muted);font-weight:600;font-size:13px}

    /* ---------- Projects ---------- */
    .projects{margin-top:18px;display:grid;gap:14px}
    .proj{padding:14px;border-radius:12px;background:linear-gradient(180deg,var(--card), rgba(255,255,255,0.02));border:1px solid rgba(255,255,255,0.02);}
    .proj h3{margin:0 0 6px 0}
    .tags{display:flex;gap:8px;margin-top:8px}
    .tag{font-size:12px;padding:6px 8px;border-radius:8px;background:var(--glass-2);color:var(--muted)}

    /* ---------- Right column (sidebar) ---------- */
    .side{position:sticky;top:28px}
    .contact{display:flex;flex-direction:column;gap:10px}
    .pill{display:flex;justify-content:space-between;align-items:center;padding:12px;border-radius:10px;background:linear-gradient(90deg,rgba(255,255,255,0.02),transparent);border:1px solid rgba(255,255,255,0.02)}
    .socials{display:flex;gap:10px}
    .socials a{padding:8px;border-radius:10px;background:var(--glass);text-decoration:none;color:var(--muted);font-weight:700}

    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}

    /* ---------- Buttons & inputs ---------- */
    .btn{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:10px;border:0;cursor:pointer;font-weight:700}
    .btn-primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#041022}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.04);color:var(--muted)}

    /* small helpers */
    .muted{color:var(--muted)}
    .stack{display:flex;flex-direction:column;gap:10px}

    /* code block look */
    pre{background:#041022;padding:12px;border-radius:10px;font-family:var(--mono);font-size:13px;color:#bfe9ff;overflow:auto}

  </style>
</head>
<body>
  <main>
    <div class="topbar">
      <div class="brand">
        <div class="logo">DH</div>
        <div>
          <div style="font-size:14px">L Dhanus Raghav</div>
          <div style="font-size:12px;color:var(--muted)">Production Engineering • NIT Calicut</div>
        </div>
      </div>
      <nav>
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a class="cta" href="#contact">Contact</a>
      </nav>
    </div>

    <div class="grid">
      <!-- left: main content -->
      <section>
        <div class="panel hero">
          <div class="avatar">LR</div>
          <div>
            <h1>Hi — I'm Dhanus. I build mechanical systems & drones.</h1>
            <p class="lead">Student, team lead, and maker. I design drones, EV systems, and mechanical modules — I like rapid prototypes you can test in a day.</p>
            <div class="badges">
              <div class="badge">Aerothon 2025 Captain</div>
              <div class="badge">EV Challenge — Bosch & IPG</div>
            </div>
          </div>
        </div>

        <div id="projects" class="projects">
          <div class="proj">
            <h3>Autonomous Quadcopter — Disaster Response</h3>
            <div class="muted">A complete BOM, control algorithms, and FPV mapping.</div>
            <div class="tags"><span class="tag">Raspberry Pi</span><span class="tag">Pixhawk</span><span class="tag">SLAM</span></div>
          </div>

          <div class="proj">
            <h3>Adjustable Motorcycle Footrest</h3>
            <div class="muted">Ergonomic design and strength calculations — parametric in SolidWorks.</div>
            <div class="tags"><span class="tag">CAD</span><span class="tag">FEM</span></div>
          </div>

          <div class="proj">
            <h3>Automated Waste Sorting Prototype</h3>
            <div class="muted">Miniature conveyor system with sensor-based classification for JASC 2025.</div>
            <div class="tags"><span class="tag">Embedded</span><span class="tag">Mechatronics</span></div>
          </div>
        </div>

        <div id="about" class="panel" style="margin-top:18px">
          <h2>About</h2>
          <p class="muted">I'm a B.Tech student at NIT Calicut focused on production engineering, vehicle systems, and autonomous platforms. I enjoy end-to-end product development — from BOM and CAD to embedded testing.</p>
          <div style="margin-top:12px" class="stack">
            <div class="pill"><div>Skills</div><div class="muted">CAD • MATLAB • Embedded • SLAM • Prototyping</div></div>
            <div class="pill"><div>Current</div><div class="muted">Team captain — Aerothon 2025</div></div>
          </div>
        </div>

        <footer>
          Built with ❤️ · Hosted on GitHub Pages · Customize colors in <code>:root</code>
        </footer>
      </section>

      <!-- right: sidebar -->
      <aside class="side">
        <div class="panel contact">
          <h3>Contact</h3>
          <div class="muted">Want to collaborate or view the source? Reach out or check my GitHub.</div>
          <div class="stack" style="margin-top:8px">
            <a href="#" class="btn btn-primary">View GitHub</a>
            <a href="#" class="btn btn-ghost">Download Resume</a>
          </div>

          <div style="margin-top:12px" class="pill">
            <div>Location</div>
            <div class="muted">Calicut, India</div>
          </div>

          <div style="margin-top:12px">
            <div style="font-size:13px;color:var(--muted);margin-bottom:6px">Social</div>
            <div class="socials">
              <a href="#">GH</a>
              <a href="#">LI</a>
              <a href="#">IG</a>
            </div>
          </div>
        </div>

        <div class="panel" style="margin-top:14px">
          <h4>Theme</h4>
          <div class="muted">Change the colors at the top of the file (the <code>:root</code> CSS variables).</div>
          <pre>--accent: #7c5cff;
--accent-2: #00d4ff;
--bg: #0f1724;</pre>
        </div>
      </aside>
    </div>
  </main>
</body>
</html>

Its Me

![my pic](https://media.licdn.com/dms/image/v2/D5603AQEdhI-8bq9WMw/profile-displayphoto-crop_800_800/B56ZfP4QjNG0AM-/0/1751539322417?e=1759968000&v=beta&t=mRYZKsqfBtCnCbn5PqKFMLc7AEmnVKfVYN8SWs7LdDg)
