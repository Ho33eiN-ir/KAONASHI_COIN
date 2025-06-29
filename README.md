# ساخت پوشه برای مرحله FAQ
faq_path = "/mnt/data/kaonashi_faq"
os.makedirs(faq_path, exist_ok=True)

# HTML صفحه FAQ
faq_html = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FAQ - KAONASHI COIN</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn&display=swap" rel="stylesheet">
  <style>
    body {
      background: #121212;
      color: #fff;
      font-family: 'Vazirmatn', sans-serif;
      padding: 40px 20px;
      line-height: 1.8;
      text-align: left;
      max-width: 800px;
      margin: auto;
    }
    h1 {
      text-align: center;
      color: #f1c40f;
    }
    .faq-item {
      margin-bottom: 30px;
    }
    .question {
      font-weight: bold;
      color: #1abc9c;
    }
    .answer {
      margin-top: 8px;
    }
    a.back-link {
      display: block;
      text-align: center;
      margin-top: 40px;
      background: #1abc9c;
      color: #000;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      width: fit-content;
      margin-left: auto;
      margin-right: auto;
    }
  </style>
</head>
<body>

<h1>🤔 Frequently Asked Questions</h1>

<div class="faq-item">
  <div class="question">What is KAONASHI COIN?</div>
  <div class="answer">
    KAONASHI is a decentralized meme-coin inspired by the mysterious “No-Face” from the anime Spirited Away. It's about community, privacy, and no central control.
  </div>
</div>

<div class="faq-item">
  <div class="question">Who created it?</div>
  <div class="answer">
    No central team. It was created anonymously and is maintained by the community. There is no official owner or developer.
  </div>
</div>

<div class="faq-item">
  <div class="question">Is there a presale or token allocation?</div>
  <div class="answer">
    No. 100% of tokens were released publicly. There were no private sales, no VC funds, and no locked wallets.
  </div>
</div>

<div class="faq-item">
  <div class="question">Where can I buy it?</div>
  <div class="answer">
    Initially on decentralized exchanges like PancakeSwap or Uniswap. More listings will follow.
  </div>
</div>

<div class="faq-item">
  <div class="question">What’s the utility of this token?</div>
  <div class="answer">
    It's a community-driven meme-token with a goal to evolve into a DAO where holders vote on proposals and development directions.
  </div>
</div>

<a href="index.html" class="back-link">⬅ Back to Home</a>

</body>
</html>
"""

# ذخیره فایل HTML
faq_file_path = os.path.join(faq_path, "faq.html")
with open(faq_file_path, "w", encoding="utf-8") as f:
    f.write(faq_html)

# ساخت فایل zip
faq_zip = "/mnt/data/kaonashi_faq.zip"
with ZipFile(faq_zip, "w") as zipf:
    zipf.write(faq_file_path, "faq.html")

faq_zip

