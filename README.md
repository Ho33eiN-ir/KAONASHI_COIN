<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>KAONASHI COIN</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn&display=swap" rel="stylesheet" />
  <style>
    body {
      background-color: #121212;
      color: #fff;
      font-family: 'Vazirmatn', sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    header, footer {
      background-color: #1f1f1f;
      padding: 20px;
    }
    .logo {
      width: 160px;
      border-radius: 10px;
      margin: 20px auto;
    }
    .section {
      padding: 40px 20px;
      border-bottom: 1px solid #333;
    }
    .section h2 {
      color: #f1c40f;
    }
    .roadmap-table {
      width: 90%;
      margin: auto;
      border-collapse: collapse;
    }
    .roadmap-table th, .roadmap-table td {
      border: 1px solid #555;
      padding: 10px;
    }
    input, textarea {
      width: 80%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: none;
    }
    .social-icons img {
      width: 40px;
      margin: 0 10px;
    }
    .price-box {
      background: #1f1f1f;
      display: inline-block;
      padding: 15px 25px;
      margin: 10px;
      border-radius: 10px;
      font-size: 1.1rem;
    }
    .whitepaper-btn {
      display: inline-block;
      background: #1abc9c;
      color: #000;
      padding: 10px 20px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
    }
  </style>
</head>
<body>

<header>
  <img src="https://upload.wikimedia.org/wikipedia/en/4/46/Kaonashi.png" alt="Kaonashi Logo" class="logo" />
  <h1>KAONASHI COIN</h1>
  <p>A mysterious coin. A symbol of anonymity in crypto.</p>
  <a href="whitepaper.html" class="whitepaper-btn">📄 View Whitepaper</a>
</header>

<section class="section">
  <h2>💸 Live Prices</h2>
  <div id="prices">
    <div class="price-box" id="btc">Bitcoin: ...</div>
    <div class="price-box" id="eth">Ethereum: ...</div>
    <div class="price-box" id="kaonashi">Kaonashi: ~1000 KNS (placeholder)</div>
  </div>
</section>

<section class="section">
  <h2>📍 Roadmap</h2>
  <table class="roadmap-table">
    <tr><th>Phase</th><th>Date</th><th>Status</th></tr>
    <tr><td>Website Launch</td><td>Q2 2025</td><td>✅ Done</td></tr>
    <tr><td>Whitepaper Release</td><td>Q3 2025</td><td>🛠 In Progress</td></tr>
    <tr><td>DEX Listing</td><td>Q4 2025</td><td>📅 Planned</td></tr>
  </table>
</section>

<section class="section">
  <h2>👤 About Us</h2>
  <p>
    We are an independent team inspired by the No-Face character. KAONASHI COIN stands for privacy, community, and decentralization. No marketing, no owner. Just pure crypto.
  </p>
</section>

<section class="section">
  <h2>📨 Contact Us</h2>
  <form>
    <input type="text" placeholder="Your Name" /><br />
    <input type="email" placeholder="Your Email" /><br />
    <textarea rows="4" placeholder="Your Message"></textarea><br />
    <input type="submit" value="Send Message" />
  </form>
</section>

<section class="section">
  <h2>🌐 Social Media</h2>
  <div class="social-icons">
    <a href="#"><img src="https://img.icons8.com/ios-filled/50/ffffff/telegram-app.png" alt="Telegram" /></a>
    <a href="#"><img src="https://img.icons8.com/ios-filled/50/ffffff/twitter.png" alt="Twitter" /></a>
  </div>
</section>

<footer>
  <p>© 2025 KAONASHI COIN. All rights reserved.</p>
</footer>

<script>
  async function fetchPrices() {
    try {
      const res = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=bitcoin,ethereum&vs_currencies=usd');
      const data = await res.json();
      document.getElementById('btc').innerText = 'Bitcoin: $' + data.bitcoin.usd;
      document.getElementById('eth').innerText = 'Ethereum: $' + data.ethereum.usd;
    } catch (e) {
      console.error('Error fetching prices');
    }
  }
  fetchPrices();
</script>

</body>
</html>

