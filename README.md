
<header class="hero">
  <h1>🎮 Tatbiqa</h1>
</header>
  <h2 class="sec">📖 About</h2>
  <p>
    <b> Tatbiqa</b> helps small PlayStation cafe owners run their business from one phone.
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
  </div>

  <h2 class="sec">🖼️ Screenshots</h2>
  <div class="shots">
<img width="200"  alt="image" src="https://github.com/user-attachments/assets/4167d76d-94bf-46af-8ab7-13340e239c7b" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/49982d96-368e-42c3-9466-c8ed26698e4d" />

<img width="200"  alt="image" src="https://github.com/user-attachments/assets/0857df7e-bb14-4451-aeff-c5ae44b46b54" />

<img width="200"  alt="image" src="https://github.com/user-attachments/assets/727fb132-1dca-4852-a8d8-63cf2849eac2" />

<img width="200" alt="image" src="https://github.com/user-attachments/assets/86cf226c-4937-4681-a3ce-b81b9dfcc96f" />

<img width="200"  alt="image" src="https://github.com/user-attachments/assets/152ff59d-37a5-4796-9d63-64431d2108fb" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/949b0216-5527-4b27-a560-27dec0a49006" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/f28b88d9-fe5b-49e4-9445-59a94640f1e9" />
<img width="200"  alt="image" src="https://github.com/user-attachments/assets/065334ca-4edb-4010-96a5-42143c7b447b" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/495116db-73ba-421c-a9c6-56a19072ace9" />
<img width="200"  alt="image" src="https://github.com/user-attachments/assets/5d15f42b-36a9-4784-987d-a0220c75ed15" />
<img width="200"  alt="image" src="https://github.com/user-attachments/assets/092ff484-d9a0-4365-a862-fef5ff8b3025" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/ebc2ec86-b6a8-4234-b978-2b5a2d6fe1cb" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/52ba012d-0bd2-4baf-9ea0-eeefe722f81c" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/73b4d278-2a64-4b45-bcdf-d5e6a0a5e854" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/6673dd60-d401-44c0-a7e5-13cc78ba97e2" />
<img width="200" alt="image" src="https://github.com/user-attachments/assets/248fa555-d0d0-4bdc-be8b-a661746d230e" />
<img width="200"  alt="image" src="https://github.com/user-attachments/assets/57ec04f0-dd95-4c6c-928b-3eab8698cacc" />


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



  <h2 class="sec">👩‍💻 Author</h2>
  <p>
    <b>Toka Ahmed Elsharkawy</b> — Flutter Developer<br />

  </p>

  <footer>Made with ❤️ using Flutter</footer>
</main>

</body>
</html>
