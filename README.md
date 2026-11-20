<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>تطبيقه | PlayStation Cafe Manager</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;800&family=Inter:wght@400;600;800&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #111111; --card: #1b1b1b; --border: #2e2e2e;
    --text: #f2f2f2; --muted: #9a9a9a;
    --accent: #22c55e; --hero: #181818; --orange: #f97316;
  }
  @media (prefers-color-scheme: light) {
    :root { --bg: #fafaf9; --card: #ffffff; --border: #e5e5e3; --text: #1c1c1c; --muted: #6b6b6b; --hero: #ffffff; --accent: #16a34a; }
  }
  * { box-sizing: border-box; }
  body { margin: 0; background: var(--bg); color: var(--text); font-family: "Inter", "Cairo", system-ui, sans-serif; line-height: 1.7; }
  .wrap { max-width: 980px; margin: 0 auto; padding: 0 20px 60px; }

  /* Hero: plain, no gradient */
  .hero { text-align: center; padding: 64px 20px 44px; background: var(--hero); border-bottom: 1px solid var(--border); }
  .hero h1 { font-family: "Cairo", sans-serif; font-size: 3rem; margin: 0; font-weight: 800; }
  .hero h2 { margin: 6px 0 14px; font-weight: 600; font-size: 1.25rem; color: var(--muted); }
  .hero p { max-width: 640px; margin: 0 auto 22px; color: var(--muted); }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; justify-content: center; }
  .badge { background: var(--card); border: 1px solid var(--border); padding: 5px 14px; border-radius: 999px; font-size: .85rem; font-weight: 600; }
  .badge::before { content: ""; display: inline-block; width: 7px; height: 7px; border-radius: 50%; background: var(--accent); margin-right: 8px; }

  h2.sec { font-size: 1.5rem; margin: 48px 0 16px; padding-bottom: 8px; border-bottom: 1px solid var(--border); }
  .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 14px; }
  .card { background: var(--card); border: 1px solid var(--border); border-radius: 14px; padding: 18px; }
  .card .ico { font-size: 1.6rem; }
  .card h3 { margin: 6px 0 4px; font-size: 1.05rem; }
  .card p { margin: 0; color: var(--muted); font-size: .92rem; }
  table { width: 100%; border-collapse: collapse; background: var(--card); border-radius: 12px; overflow: hidden; border: 1px solid var(--border); }
  th, td { padding: 11px 14px; text-align: left; border-bottom: 1px solid var(--border); font-size: .93rem; }
  th { background: rgba(127,127,127,.12); }
  tr:last-child td { border-bottom: none; }
  pre { background: #0a0a0a; color: #eaeaea; padding: 16px; border-radius: 12px; overflow-x: auto; border: 1px solid var(--border); font-size: .9rem; }
  code { font-family: ui-monospace, Consolas, monospace; }
  p code, li code { background: rgba(127,127,127,.2); padding: 2px 6px; border-radius: 6px; }
  .flow { display: flex; flex-wrap: wrap; gap: 10px; align-items: center; }
  .step { background: var(--card); border: 1px solid var(--border); padding: 9px 16px; border-radius: 999px; font-weight: 600; font-size: .9rem; }
  .arrow { color: var(--muted); }
  .rules li { margin-bottom: 8px; }
  .note { background: rgba(249,115,22,.1); border: 1px solid var(--orange); border-radius: 12px; padding: 14px 18px; }
  .shots { display: flex; flex-wrap: wrap; gap: 14px; justify-content: center; }
  .shot { width: 190px; height: 380px; border: 2px dashed var(--border); border-radius: 22px; display: flex; align-items: center; justify-content: center; color: var(--muted); text-align: center; font-size: .85rem; padding: 10px; }
  .shots img { width: 190px; border-radius: 22px; border: 1px solid var(--border); }
  .two { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 14px; }
  footer { text-align: center; color: var(--muted); padding: 30px 0 0; border-top: 1px solid var(--border); margin-top: 50px; }
  a { color: var(--accent); text-decoration: none; }
  a:hover { text-decoration: underline; }
</style>
</head>
<body>

<header class="hero">
  <h1>🎮 تطبيقه</h1>
  <h2>PlayStation Cafe Management App</h2>
  <p>A simple mobile ERP for PlayStation cafes: manage rooms, run sessions, add drinks, checkout, and track daily and monthly income.</p>
  <div class="badges">
    <span class="badge">Flutter</span>
    <span class="badge">Dart</span>
    <span class="badge">Hive (Local DB)</span>
    <span class="badge">Firebase (Subscription)</span>
    <span class="badge">MVP v1.0</span>
  </div>
</header>

<main class="wrap">

  <h2 class="sec">📖 About</h2>
  <p>
    <b>تطبيقه</b> helps small PlayStation cafe owners run their business from one phone.
    The owner creates rooms, starts a session, and adds drinks while customers play.
    At the end, <b>Checkout</b> gives a final invoice (play time + orders = total),
    and the Dashboard updates automatically.
  </p>

  <div class="note" style="margin-top:18px">
    🔒 <b>Private Source Code:</b> The source code of this project is private.
    I built it during a <b>remote internship</b>, so the code belongs to the company and is not public.
    This page is only to show the idea, the features, and what I worked on.
  </div>

  <h2 class="sec">🔄 How It Works</h2>
  <div class="flow">
    <span class="step">Add Room</span><span class="arrow">→</span>
    <span class="step">Start Session</span><span class="arrow">→</span>
    <span class="step">Add Drinks</span><span class="arrow">→</span>
    <span class="step">Checkout</span><span class="arrow">→</span>
    <span class="step">Dashboard &amp; Archive</span>
  </div>

  <h2 class="sec">✨ Features</h2>
  <div class="grid">
    <div class="card"><div class="ico">🚪</div><h3>Rooms Management</h3><p>Add, edit and delete rooms with an hourly price.</p></div>
    <div class="card"><div class="ico">⏱️</div><h3>Live Sessions</h3><p>Live timer and current total on every room card.</p></div>
    <div class="card"><div class="ico">🥤</div><h3>Drinks &amp; Products</h3><p>Add items with quantities to a running session.</p></div>
    <div class="card"><div class="ico">🧾</div><h3>Checkout Invoice</h3><p>Play cost + products = final total, confirmed before closing.</p></div>
    <div class="card"><div class="ico">📊</div><h3>Dashboard</h3><p>Daily and monthly income, sessions, play time, best and weakest rooms.</p></div>
    <div class="card"><div class="ico">🗂️</div><h3>Archive</h3><p>Review any previous day or month.</p></div>
    <div class="card"><div class="ico">💳</div><h3>Subscription</h3><p>Monthly plan checked with Firebase. Expired plan shows a renewal screen.</p></div>
    <div class="card"><div class="ico">📴</div><h3>Offline-first</h3><p>All cafe data is stored locally with Hive.</p></div>
    <div class="card"><div class="ico">🌗</div><h3>Light / Dark Mode</h3><p>Switch the theme from Settings.</p></div>
  </div>

  <h2 class="sec">📱 Screens</h2>
  <table>
    <tr><th>#</th><th>Screen</th><th>Purpose</th></tr>
    <tr><td>1</td><td>Splash</td><td>Checks first launch and subscription status</td></tr>
    <tr><td>2</td><td>Subscription Expired</td><td>Shown when the subscription is not active</td></tr>
    <tr><td>3</td><td>Setup Cafe</td><td>Enter the cafe name (first launch only)</td></tr>
    <tr><td>4</td><td>Home / Rooms</td><td>Room cards, start sessions, quick add drinks</td></tr>
    <tr><td>5</td><td>Room Details</td><td>Full session details + Checkout</td></tr>
    <tr><td>6</td><td>Add Drinks</td><td>Pick products and quantities</td></tr>
    <tr><td>7</td><td>Products</td><td>Manage products and availability</td></tr>
    <tr><td>8</td><td>Dashboard</td><td>Current day and current month reports</td></tr>
    <tr><td>9</td><td>Archive</td><td>Previous days and months</td></tr>
    <tr><td>10</td><td>Settings</td><td>Cafe name, theme, add room</td></tr>
    <tr><td>11</td><td>Room Settings</td><td>Edit or delete a room</td></tr>
  </table>

  <h2 class="sec">🖼️ Screenshots</h2>
  <div class="shots">
    <!-- Replace each placeholder with: <img src="docs/screenshots/home.png" alt="Home" /> -->
    <div class="shot">Home<br />docs/screenshots/home.png</div>
    <div class="shot">Room Details<br />docs/screenshots/details.png</div>
    <div class="shot">Checkout<br />docs/screenshots/checkout.png</div>
    <div class="shot">Dashboard<br />docs/screenshots/dashboard.png</div>
  </div>

  <h2 class="sec">🧮 Calculation Rules</h2>
  <pre><code>Play cost    = minutes × hourly rate ÷ 60
Products     = sum of (price × quantity)
Final total  = Play cost + Products</code></pre>
  <p><b>Example:</b> 85 minutes at 60 EGP/hour = 85 EGP, plus drinks 55 EGP = <b>140 EGP</b>.</p>

  <h2 class="sec">📌 Business Rules</h2>
  <ul class="rules">
    <li>Only <b>one active session</b> per room at a time.</li>
    <li>Room Settings is hidden while the room is occupied.</li>
    <li>Checkout is done from <b>Room Details</b> only.</li>
    <li>Dashboard and Archive count <b>closed sessions only</b>.</li>
    <li>Each session saves the <b>room name and hourly rate</b> at that time.</li>
    <li>Each order saves the <b>product name and price</b> at that time.</li>
  </ul>
  <div class="note">💡 Because of this, old invoices stay correct even if you edit or delete a room or product later.</div>

  <h2 class="sec">🛠️ Tech Stack</h2>
  <table>
    <tr><th>Part</th><th>Technology</th></tr>
    <tr><td>Framework</td><td>Flutter &amp; Dart</td></tr>
    <tr><td>Local database</td><td>Hive</td></tr>
    <tr><td>Subscription</td><td>Firebase</td></tr>
  </table>

  <h2 class="sec">🗄️ Data Models</h2>
  <div class="two">
    <div class="card"><h3>CafeSettings</h3><p>cafe name, theme mode</p></div>
    <div class="card"><h3>Subscription</h3><p>shop id, is active, end date, last checked, status</p></div>
    <div class="card"><h3>Room</h3><p>id, name, hourly rate</p></div>
    <div class="card"><h3>Product</h3><p>id, name, price, is available</p></div>
    <div class="card"><h3>Session</h3><p>room id, room name, hourly rate, start/end time, minutes, play cost, products cost, total, status</p></div>
    <div class="card"><h3>SessionProduct</h3><p>session id, product name, unit price, quantity, total</p></div>
  </div>

  <h2 class="sec">🔮 Future Ideas</h2>
  <div class="grid">
    <div class="card"><h3>☁️ Cloud Sync</h3><p>Multi-device support</p></div>
    <div class="card"><h3>🌐 Web Dashboard</h3><p>Reports from a computer</p></div>
    <div class="card"><h3>🏪 Multi Branch</h3><p>More than one branch</p></div>
    <div class="card"><h3>👥 Users &amp; Roles</h3><p>Owner / Manager / Cashier</p></div>
    <div class="card"><h3>💸 Expenses</h3><p>Net profit calculation</p></div>
    <div class="card"><h3>📦 Inventory</h3><p>Stock and low-stock alerts</p></div>
    <div class="card"><h3>📄 Export</h3><p>PDF / Excel reports</p></div>
    <div class="card"><h3>🖨️ Printed Invoice</h3><p>Bluetooth printer</p></div>
    <div class="card"><h3>🤖 AI Agent</h3><p>Ask questions about your income and rooms</p></div>
  </div>

  <h2 class="sec">👩‍💻 Author</h2>
  <p>
    <b>Toka Ahmed Elsharkawy</b> — Flutter Developer<br />
    <a href="https://github.com/YOUR_USERNAME">GitHub</a> •
    <a href="https://www.linkedin.com/in/YOUR_LINKEDIN">LinkedIn</a>
  </p>

  <footer>Made with ❤️ using Flutter</footer>
</main>

</body>
</html>
