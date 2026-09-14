<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>A Note for Harjas ✨</title>  
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;500;700&family=Playfair+Display:ital,wght@0,600;1,400&display=swap" rel="stylesheet">  
  <style>  
    :root {  
      --bg: #0f172a;  
      --card-bg: rgba(255, 255, 255, 0.08);  
      --border: rgba(255, 255, 255, 0.15);  
      --accent: #f472b6;  
      --text: #f8fafc;  
      --muted: #94a3b8;  
    }  
  
    * {  
      box-sizing: border-box;  
      margin: 0;  
      padding: 0;  
    }  
  
    body {  
      min-height: 100vh;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      background: radial-gradient(circle at top, #1e1b4b, #0f172a);  
      font-family: 'Outfit', sans-serif;  
      color: var(--text);  
      overflow-x: hidden;  
      padding: 24px;  
    }  
  
    .container {  
      max-width: 480px;  
      width: 100%;  
      background: var(--card-bg);  
      backdrop-filter: blur(16px);  
      -webkit-backdrop-filter: blur(16px);  
      border: 1px solid var(--border);  
      border-radius: 24px;  
      padding: 36px 28px;  
      box-shadow: 0 20px 50px rgba(0,0,0,0.4), 0 0 40px rgba(244, 114, 182, 0.1);  
      text-align: center;  
      position: relative;  
    }  
  
    .tag {  
      display: inline-block;  
      padding: 6px 14px;  
      font-size: 0.8rem;  
      text-transform: uppercase;  
      letter-spacing: 2px;  
      border-radius: 50px;  
      background: rgba(244, 114, 182, 0.15);  
      color: var(--accent);  
      border: 1px solid rgba(244, 114, 182, 0.3);  
      margin-bottom: 20px;  
    }  
  
    h1 {  
      font-family: 'Playfair Display', serif;  
      font-size: 2.2rem;  
      margin-bottom: 16px;  
      font-weight: 600;  
    }  
  
    .letter {  
      font-size: 1.05rem;  
      line-height: 1.7;  
      color: #e2e8f0;  
      margin-bottom: 28px;  
      text-align: left;  
      background: rgba(255, 255, 255, 0.03);  
      padding: 20px;  
      border-radius: 16px;  
      border-left: 3px solid var(--accent);  
    }  
  
    .letter p + p {  
      margin-top: 14px;  
    }  
  
    .signature {  
      font-family: 'Playfair Display', serif;  
      font-style: italic;  
      color: var(--accent);  
      font-size: 1.2rem;  
      text-align: right;  
      display: block;  
      margin-top: 12px;  
    }  
  
    .interactive-zone {  
      margin-top: 24px;  
      padding-top: 20px;  
      border-top: 1px solid rgba(255, 255, 255, 0.1);  
    }  
  
    .question {  
      font-size: 1rem;  
      color: var(--muted);  
      margin-bottom: 14px;  
    }  
  
    .btn-group {  
      display: flex;  
      justify-content: center;  
      gap: 16px;  
      position: relative;  
      min-height: 48px;  
    }  
  
    button {  
      padding: 12px 24px;  
      font-size: 0.95rem;  
      font-weight: 600;  
      border-radius: 12px;  
      cursor: pointer;  
      transition: transform 0.2s ease, box-shadow 0.2s ease;  
      font-family: 'Outfit', sans-serif;  
    }  
  
    .btn-accept {  
      background: linear-gradient(135deg, #f472b6, #ec4899);  
      color: white;  
      border: none;  
      box-shadow: 0 4px 15px rgba(244, 114, 182, 0.35);  
    }  
  
    .btn-accept:hover {  
      transform: scale(1.05);  
      box-shadow: 0 6px 20px rgba(244, 114, 182, 0.5);  
    }  
  
    .btn-dodge {  
      background: transparent;  
      color: var(--muted);  
      border: 1px solid var(--border);  
      position: relative;  
    }  
  
    #response-msg {  
      margin-top: 18px;  
      font-size: 1.1rem;  
      color: #38bdf8;  
      font-weight: 500;  
      opacity: 0;  
      transition: opacity 0.4s ease;  
    }  
  
    /* Subtle floating sparkles */  
    .sparkle {  
      position: absolute;  
      width: 4px;  
      height: 4px;  
      background: white;  
      border-radius: 50%;  
      opacity: 0.3;  
      animation: float 4s infinite ease-in-out;  
    }  
  
    @keyframes float {  
      0%, 100% { transform: translateY(0); }  
      50% { transform: translateY(-15px); }  
    }  
  </style>  
</head>  
<body>  
  
  <div class="container">  
    <span class="tag">Peace Offering</span>  
    <h1>Dear Harjas,</h1>  
  
    <div class="letter">  
      <p>I really hate that things felt off between us today. You’re my best friend, and upsetting you is the last thing I ever want to do.</p>  
      <p>Whatever went wrong, I'm truly sorry. Our friendship means way too much to me to let a bad moment get in the way. I miss laughing with you already.</p>  
      <p>Treats, snacks, and apologies are on me whenever you're ready.</p>  
      <span class="signature">— Your Best Friend</span>  
    </div>  
  
    <div class="interactive-zone">  
      <div class="question">Ready for a truce?</div>  
      <div class="btn-group">  
        <button class="btn-accept" onclick="showLove()">Truce Accepted 🤝</button>  
        <button class="btn-dodge" id="dodgeBtn" onmouseover="dodge()">Still Grumpy 😤</button>  
      </div>  
      <div id="response-msg">Best decision ever! Snacks incoming soon 🎉</div>  
    </div>  
  </div>  
  
  <script>  
    function showLove() {  
      const msg = document.getElementById('response-msg');  
      msg.style.opacity = '1';  
      document.getElementById('dodgeBtn').style.display = 'none';  
    }  
  
    function dodge() {  
      const btn = document.getElementById('dodgeBtn');  
      const randomX = (Math.random() - 0.5) * 160;  
      const randomY = (Math.random() - 0.5) * 100;  
      btn.style.transform = `translate(${randomX}px, ${randomY}px)`;  
    }  
  </script>  
</body>  
</html>  
