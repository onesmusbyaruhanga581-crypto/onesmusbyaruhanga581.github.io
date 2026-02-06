<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Valentine’s Day ❤️</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Roboto&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      text-align: center;
      overflow-x: hidden;
    }
    h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 70px;
      color: #d60000;
      margin-top: 50px;
      animation: glow 2s infinite alternate;
    }
    p {
      font-size: 24px;
      color: #333;
      margin: 20px;
    }
    @keyframes glow {
      from { text-shadow: 0 0 10px #ff4d4d; }
      to { text-shadow: 0 0 30px #ff1a75; }
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s infinite;
    }
    .heart::before, .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }
    .heart::before { top: -10px; left: 0; }
    .heart::after { left: 10px; top: 0; }
    @keyframes float {
      0% { transform: translateY(0) rotate(45deg); opacity: 1; }
      100% { transform: translateY(-800px) rotate(45deg); opacity: 0; }
    }
    button {
      background: #d60000;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 20px;
      border-radius: 30px;
      cursor: pointer;
      margin-top: 30px;
      transition: background 0.3s;
    }
    button:hover {
      background: #ff1a75;
    }
    #surprise {
      display: none;
      font-size: 28px;
      color: #d60000;
      margin-top: 20px;
      animation: fadeIn 2s forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    /* Slideshow styles */
    .slideshow-container {
      max-width: 600px;
      position: relative;
      margin: 40px auto;
    }
    .slides {
      display: none;
    }
    img {
      width: 100%;
      border-radius: 20px;
    }
    .prev, .next {
      cursor: pointer;
      position: absolute;
      top: 50%;
      width: auto;
      padding: 16px;
      margin-top: -22px;
      color: white;
      font-weight: bold;
      font-size: 20px;
      transition: 0.6s ease;
      border-radius: 0 3px 3px 0;
      user-select: none;
    }
    .next {
      right: 0;
      border-radius: 3px 0 0 3px;
    }
    .prev:hover, .next:hover {
      background-color: rgba(0,0,0,0.8);
    }
  </style>
</head>
<body>
  <h1>Happy Valentine’s Day, HELLEN BABE ❤️</h1>
  <p>You make my world brighter every single day.</p>
  <button onclick="showSurprise()">Click for a Surprise</button>
  <div id="surprise">Forever yours, Onesmus 💕</div>

  <!-- Slideshow -->
  <div class="slideshow-container">
    <div class="slides">
      <img src="![Image](https://github.com/user-attachments/assets/35300ebb-7d06-444a-befd-6c18ccc4790c)" alt="Us together">
    </div>
    <div class="slides">
      <img src="photo2.jpg" alt="Smiling moment">
    </div>
    <div class="slides">
      <img src="photo3.jpg" alt="Special memory">
    </div>
    <a class="prev" onclick="plusSlides(-1)">❮</a>
    <a class="next" onclick="plusSlides(1)">❯</a>
  </div>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>

  <script>
    // Floating hearts
    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * window.innerWidth + 'px';
      heart.style.top = window.innerHeight + 'px';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 500);

    // Surprise message
    function showSurprise() {
      document.getElementById('surprise').style.display = 'block';
    }

    // Slideshow logic
    let slideIndex = 1;
    showSlides(slideIndex);

    function plusSlides(n) {
      showSlides(slideIndex += n);
    }

    function showSlides(n) {
      let i;
      let slides = document.getElementsByClassName("slides");
      if (n > slides.length) {slideIndex = 1}
      if (n < 1) {slideIndex = slides.length}
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slides[slideIndex-1].style.display = "block";
    }
  </script>
</body>
</html>
