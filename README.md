<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ultimate Skibidi Toilet Fan Web</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css">
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f0f0f0;
      color: #333;
      transition: background-color 0.3s, color 0.3s;
      cursor: url('custom-cursor.png'), auto;
    }
    body.dark-mode {
      background-color: #121212;
      color: #ffffff;
    }
    header {
      background: url('skibidi-header.jpg') center/cover no-repeat;
      color: white;
      padding: 150px 20px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    header::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
    }
    header h1 {
      position: relative;
      z-index: 1;
      font-size: 3rem;
      animation: fadeIn 2s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    nav {
      background-color: #444;
      padding: 10px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #ffcc00;
    }
    .container {
      max-width: 1200px;
      margin: 20px auto;
      padding: 20px;
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      transition: background-color 0.3s;
    }
    body.dark-mode .container {
      background-color: #1e1e1e;
      color: #ffffff;
    }
    h1, h2 {
      color: #333;
    }
    body.dark-mode h1, body.dark-mode h2 {
      color: #ffffff;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 10px;
    }
    .gallery img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
      transition: transform 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }
    .video-container {
      display: flex;
      justify-content: center;
      margin: 20px 0;
    }
    .video-container iframe {
      max-width: 100%;
      border-radius: 8px;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-width: 400px;
      margin: 20px auto;
    }
    form input, form textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    form button {
      padding: 10px;
      background-color: #333;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    form button:hover {
      background-color: #555;
    }
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 20px;
    }
    .social-links a {
      color: white;
      margin: 0 10px;
      font-size: 1.5rem;
      transition: color 0.3s;
    }
    .social-links a:hover {
      color: #ffcc00;
    }
    .dark-mode-toggle {
      position: fixed;
      bottom: 20px;
      right: 20px;
      padding: 10px;
      background-color: #333;
      color: white;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .dark-mode-toggle:hover {
      background-color: #555;
    }
    .countdown {
      text-align: center;
      margin: 20px 0;
      font-size: 1.5rem;
    }
    .chatbot {
      position: fixed;
      bottom: 20px;
      left: 20px;
      background-color: #333;
      color: white;
      padding: 10px;
      border-radius: 8px;
      cursor: pointer;
    }
    .meme-coin-announcement {
      background-color: #ffcc00;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      margin: 20px 0;
    }
    .meme-coin-announcement a {
      color: #333;
      font-weight: bold;
      text-decoration: none;
    }
    .meme-coin-announcement a:hover {
      text-decoration: underline;
    }
    .crypto-tracker {
      background-color: #f8f9fa;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      margin: 20px 0;
    }
    .crypto-tracker h3 {
      margin-bottom: 10px;
    }
    .crypto-tracker p {
      margin: 5px 0;
    }
    .newsletter {
      background-color: #e9ecef;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      margin: 20px 0;
    }
    .newsletter h3 {
      margin-bottom: 10px;
    }
    .chatbot-popup {
      display: none;
      position: fixed;
      bottom: 80px;
      left: 20px;
      width: 300px;
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      z-index: 1000;
    }
    .chatbot-popup.active {
      display: block;
    }
    .chatbot-popup input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      margin-bottom: 10px;
    }
    .chatbot-popup button {
      width: 100%;
      padding: 10px;
      background-color: #333;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .chatbot-popup button:hover {
      background-color: #555;
    }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to the Ultimate Skibidi Toilet Fan Web!</h1>
  </header>
  <nav>
    <a href="#about">About</a>
    <a href="#gallery">Gallery</a>
    <a href="#videos">Videos</a>
    <a href="#submit">Submit Fan Art</a>
    <a href="#meme-coin">Meme Coin</a>
  </nav>
  <div class="container">
    <section id="about">
      <h2>About Skibidi Toilet</h2>
      <p>
        Skibidi Toilet is a surreal and viral meme that originated from a YouTube series. It features bizarre and humorous scenarios involving anthropomorphic toilets and other strange characters. The meme has taken the internet by storm, with countless remixes, parodies, and fan creations.
      </p>
    </section>
    <section id="meme-coin">
      <h2>Official Skibidi Toilet Meme Coin</h2>
      <div class="meme-coin-announcement">
        <p>
          🚨 **BREAKING NEWS** 🚨<br>
          The official Skibidi Toilet Meme Coin has been announced! Check out the announcement on Twitter:
          <a href="https://twitter.com/HqSkibid9586" target="_blank">@HqSkibid9586</a>.
        </p>
        <p>
          🚀 Don't miss out on the next big meme coin! Follow the official account for updates.
        </p>
      </div>
    </section>
    <section id="crypto-tracker">
      <h2>Skibidi Toilet Meme Coin Tracker</h2>
      <div class="crypto-tracker">
        <h3>Live Price</h3>
        <p>Price: <span id="crypto-price">$0.00</span></p>
        <p>Market Cap: <span id="crypto-market-cap">$0.00</span></p>
        <p>24h Change: <span id="crypto-change">0.00%</span></p>
      </div>
    </section>
    <section id="newsletter">
      <h2>Subscribe to Our Newsletter</h2>
      <div class="newsletter">
        <h3>Get the latest updates about Skibidi Toilet and the Meme Coin!</h3>
        <form id="newsletter-form">
          <input type="email" placeholder="Your Email" required>
          <button type="submit">Subscribe</button>
        </form>
      </div>
    </section>
    <section id="gallery">
      <h2>Gallery</h2>
      <div class="gallery">
        <a href="https://i.imgur.com/xyz1234.jpg" data-lightbox="gallery" data-title="Skibidi Toilet Image 1">
          <img src="https://i.imgur.com/xyz1234.jpg" alt="Skibidi Toilet Image 1">
        </a>
        <a href="https://i.imgur.com/abc5678.jpg" data-lightbox="gallery" data-title="Skibidi Toilet Image 2">
          <img src="https://i.imgur.com/abc5678.jpg" alt="Skibidi Toilet Image 2">
        </a>
        <a href="https://i.imgur.com/def9101.jpg" data-lightbox="gallery" data-title="Skibidi Toilet Image 3">
          <img src="https://i.imgur.com/def9101.jpg" alt="Skibidi Toilet Image 3">
        </a>
      </div>
      <button id="load-more" style="display: block; margin: 20px auto;">Load More</button>
    </section>
    <section id="videos">
      <h2>Videos</h2>
      <div class="video-container">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </section>
    <section id="submit">
      <h2>Submit Fan Art</h2>
      <form>
        <input type="text" placeholder="Your Name" required>
        <input type="email" placeholder="Your Email" required>
        <textarea placeholder="Describe your fan art..." rows="4" required></textarea>
        <button type="submit">Submit</button>
      </form>
    </section>
    <section id="countdown">
      <h2>Countdown to Next Skibidi Toilet Event</h2>
      <div class="countdown" id="countdown-timer"></div>
    </section>
  </div>
  <footer>
    <div class="social-links">
      <a href="#" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
      <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
    </div>
    <p>&copy; 2024 Skibidi Toilet Fan Web. All rights reserved.</p>
  </footer>
  <button class="dark-mode-toggle" onclick="toggleDarkMode()">🌙</button>
  <div class="chatbot" onclick="toggleChatbot()">💬 Chat with Skibidi Bot</div>
  <div class="chatbot-popup" id="chatbot-popup">
    <h3>Skibidi Bot</h3>
    <p>Ask me anything about Skibidi Toilet!</p>
    <input type="text" id="chatbot-input" placeholder="Type your question...">
    <button onclick="chatbotResponse()">Send</button>
  </div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/js/lightbox.min.js"></script>
  <script>
    // Smooth Scroll
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
      });
    });

    // Dark Mode with localStorage
    const darkModeToggle = document.querySelector('.dark-mode-toggle');
    const body = document.body;

    if (localStorage.getItem('dark-mode') === 'enabled') {
      body.classList.add('dark-mode');
    }

    function toggleDarkMode() {
      body.classList.toggle('dark-mode');
      if (body.classList.contains('dark-mode')) {
        localStorage.setItem('dark-mode', 'enabled');
      } else {
        localStorage.setItem('dark-mode', 'disabled');
      }
    }

    // Countdown Timer for Skibidi Toilet Event
    const countdownTimer = document.getElementById('countdown-timer');
    const eventDate = new Date('2025-02-16T00:00:00').getTime();

    function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = eventDate - now;

      const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
      const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

      countdownTimer.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

      if (timeLeft < 0) {
        clearInterval(interval);
        countdownTimer.innerHTML = 'Event has started!';
      }
    }

    const interval = setInterval(updateCountdown, 1000);

    // Chatbot
    function toggleChatbot() {
      const chatbotPopup = document.getElementById('chatbot-popup');
      chatbotPopup.classList.toggle('active');
    }

    function chatbotResponse() {
      const input = document.getElementById('chatbot-input').value.toLowerCase();
      let response = "I'm sorry, I don't understand. Can you ask something about Skibidi Toilet?";
      if (input.includes("what is skibidi toilet")) {
        response = "Skibidi Toilet is a viral meme featuring anthropomorphic toilets and strange characters!";
      } else if (input.includes("meme coin")) {
        response = "The Skibidi Toilet Meme Coin is the official cryptocurrency of the Skibidi Toilet universe!";
      }
      alert(response);
    }

    // Load More Gallery Images
    document.getElementById('load-more').addEventListener('click', () => {
      const gallery = document.querySelector('.gallery');
      const newImages = [
        { src: 'https://i.imgur.com/ghi1234.jpg', alt: 'Skibidi Toilet Image 4' },
        { src: 'https://i.imgur.com/jkl5678.jpg', alt: 'Skibidi Toilet Image 5' },
        { src: 'https://i.imgur.com/mno9101.jpg', alt: 'Skibidi Toilet Image 6' },
      ];
      newImages.forEach(image => {
        const newImage = document.createElement('a');
        newImage.href = image.src;
        newImage.setAttribute('data-lightbox', 'gallery');
        newImage.setAttribute('data-title', image.alt)
