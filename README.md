<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Nazia</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: "Poppins", sans-serif;
      overflow: hidden;
      text-align: center;
      color: #fff;
    }
    h1 {
      font-size: 2.5rem;
      margin-top: 60px;
      text-shadow: 2px 2px 6px rgba(0,0,0,0.3);
      animation: glow 2s infinite alternate;
    }
    h2 {
      font-size: 2rem;
      margin: 15px 0;
      font-family: "Brush Script MT", cursive;
      color: #ffe066;
      text-shadow: 0 0 10px #fffa65;
    }
    p {
      font-size: 1.1rem;
    }
    .balloon {
      position: absolute;
      width: 60px;
      height: 80px;
      border-radius: 50%;
      background: red;
      animation: float 8s infinite;
    }
    @keyframes float {
      0% { transform: translateY(100vh) rotate(0deg); }
      100% { transform: translateY(-120vh) rotate(360deg); }
    }
    @keyframes glow {
      from { text-shadow: 0 0 5px #ff6b6b, 0 0 15px #ff6b6b; }
      to { text-shadow: 0 0 20px #ffe066, 0 0 30px #ffe066; }
    }
    .cake {
      margin: 50px auto;
      width: 180px;
      height: 100px;
      background: #e07a5f;
      border-radius: 0 0 20px 20px;
      position: relative;
    }
    .cake::before {
      content: "";
      position: absolute;
      top: -30px;
      left: 15px;
      width: 150px;
      height: 30px;
      background: #f2cc8f;
      border-radius: 10px 10px 0 0;
    }
    .candle {
      width: 10px;
      height: 40px;
      background: white;
      margin: -50px 10px;
      display: inline-block;
      border-radius: 3px;
      position: relative;
    }
    .flame {
      width: 15px;
      height: 15px;
      background: gold;
      border-radius: 50%;
      position: absolute;
      top: -18px;
      left: -2px;
      box-shadow: 0 0 10px yellow;
      animation: flicker 0.3s infinite alternate;
    }
    @keyframes flicker {
      from { transform: scale(1); opacity: 0.9; }
      to { transform: scale(1.2); opacity: 0.6; }
    }
    .footer {
      margin-top: 40px;
      font-size: 0.9rem;
      color: #fff;
    }
  </style>
</head>
<body>
  <h1>🎉 Happy Birthday 🎉</h1>
  <h2>Nazia</h2>
  <p>Wishing you joy, love, and endless happiness 💖</p>

  <div class="cake">
    <div class="candle"><div class="flame"></div></div>
    <div class="candle"><div class="flame"></div></div>
    <div class="candle"><div class="flame"></div></div>
  </div>

  <div class="footer">With love 💕 — From Your Friend</div>

  <script>
    // Generate floating balloons 🎈
    function createBalloon() {
      const colors = ["#ff6b6b", "#ffd93d", "#6bcb77", "#4d96ff", "#c77dff", "#ff8a5b"];
      const balloon = document.createElement("div");
      balloon.classList.add("balloon");
      balloon.style.left = Math.random() * window.innerWidth + "px";
      balloon.style.background = colors[Math.floor(Math.random() * colors.length)];
      balloon.style.animationDuration = 5 + Math.random() * 5 + "s";
      document.body.appendChild(balloon);

      setTimeout(() => { balloon.remove(); }, 10000);
    }
    setInterval(createBalloon, 700);
  </script>
</body>
</html>
