<!doctype html>
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
