<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Skibidi Toilet Fan Web</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f0f0f0;
      color: #333;
      transition: background-color 0.3s, color 0.3s;
    }
    body.dark-mode {
      background-color: #121212;
      color: #ffffff;
    }
    header {
      background-color: #333;
      color: white;
      padding: 20px;
      text-align: center;
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
  </style>
</head>
<body>
  <header>
    <h1>Welcome to the Skibidi Toilet Fan Web!</h1>
  </header>
  <nav>
    <a href="#about">About</a>
    <a href="#gallery">Gallery</a>
    <a href="#videos">Videos</a>
    <a href="#submit">Submit Fan Art</a>
  </nav>
  <div class="container">
    <section id="about">
      <h2>About Skibidi Toilet</h2>
      <p>
        Skibidi Toilet is a surreal and viral meme that originated from a YouTube series. It features bizarre and humorous scenarios involving anthropomorphic toilets and other strange characters. The meme has taken the internet by storm, with countless remixes, parodies, and fan creations.
      </p>
    </section>
    <section id="gallery">
      <h2>Gallery</h2>
      <div class="gallery">
        <img src="https://via.placeholder.com/300" alt="Skibidi Toilet Image 1">
        <img src="https://via.placeholder.com/300" alt="Skibidi Toilet Image 2">
        <img src="https://via.placeholder.com/300" alt="Skibidi Toilet Image 3">
      </div>
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
  <script>
    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }
  </script>
</body>
</html>
