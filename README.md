<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>💘 For Rakhi 💘</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Comic Sans MS', 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 30px 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 15px 30px rgba(0,0,0,0.2);
      animation: popIn 1s ease;
      z-index: 2;
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 20px;
    }

    button {
      padding: 12px 25px;
      margin: 10px;
      font-size: 18px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      position: relative;
    }

    .yes {
      background: #ff4d6d;
      color: white;
    }

    .yes:hover {
      transform: scale(1.1);
    }

    .no {
      background: #ccc;
    }

    .message {
      font-size: 24px;
      color: #ff4d6d;
      display: none;
      animation: fadeIn 1s ease forwards;
      text-align: center;
    }

    @keyframes popIn {
      from { transform: scale(0.5); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .heart {
      position: absolute;
      font-size: 20px;
      animation: floatUp 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh) scale(0.5); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translateY(-10vh) scale(1.2); opacity: 0; }
    }
  </style>
</head>

<body>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/02/23/audio_4c9b1e6d7d.mp3?filename=romantic-piano-112191.mp3" type="audio/mpeg">
  </audio>

  <div class="card" id="card">
    <h1>💖 Rakhi, will you be my Valentine? 💖</h1>
    <button class="yes" onclick="sayYes()">Yes 💘</button>
    <button class="no" id="noBtn">No 🙈</button>
  </div>

  <div class="message" id="message">
    Yayyyy Rakhi!!! 🥰💕  
    You just made my heart so happy 💖💖
  </div>

  <script>
    function sayYes() {
      document.getElementById('card').style.display = 'none';
      document.getElementById('message').style.display = 'block';
    }

    const noBtn = document.getElementById('noBtn');
    noBtn.addEventListener('mouseover', () => {
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '💖';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = (Math.random() * 20 + 15) + 'px';
      heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }

    setInterval(createHeart, 300);
  </script>

</body>
</html>
