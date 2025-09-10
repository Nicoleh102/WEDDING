<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wedding Home Page</title>
  <link rel="stylesheet" href="style.css" />
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: #000;
      color: #fff;
    }

    .showcase {
      position: absolute;
      right: 0;
      width: 100%;
      min-height: 100vh;
      padding: 100px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #111;
      z-index: 2;
      transition: 0.5s;
    }

    .showcase.active {
      right: 300px;
    }

    .showcase header {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      padding: 40px 100px;
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      text-transform: uppercase;
      font-size: 1.5em;
      color: #fff;
      cursor: pointer;
    }

     .logo a {
  color: inherit;
  text-decoration: none;
}

    .toggle {
      position: relative;
      width: 40px;
      height: 40px;
      background: url('white menu.png') no-repeat center center / cover;
      cursor: pointer;
      z-index: 1000;
    }

    .toggle.active {
      background: url('white close.png') no-repeat center center / cover;
    }

    .showcase video {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      opacity: 0.8;
      z-index: 0;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.4);
      mix-blend-mode: overlay;
      z-index: 1;
    }

    .text {
      position: absolute;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      text-align: center;
      z-index: 2;
    }

    .text h2 {
      font-size: 3em;
      font-weight: 600;
      text-transform: uppercase;
    }

    .text h3 {
      font-size: 2em;
      font-weight: 300;
      text-transform: uppercase;
    }

    .text p {
      font-size: 1.1em;
      margin: 20px 0;
      font-weight: 300;
    }

    .text a {
      display: inline-block;
      font-size: 1em;
      background: #fff;
      padding: 10px 30px;
      text-decoration: none;
      color: #111;
      margin-top: 10px;
      text-transform: uppercase;
      letter-spacing: 2px;
      transition: 0.2s;
    }

    .text a:hover {
      letter-spacing: 6px;
    }

    .menu {
      position: fixed;
      top: 0;
      right: -300px;
      width: 300px;
      height: 100vh;
      background: #fff;
      z-index: 999;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: right 0.4s ease;
    }

    .menu.active {
      right: 0;
    }

    .menu ul {
      list-style: none;
      padding: 0;
      text-align: center;
    }

    .menu ul li a {
      display: block;
      padding: 15px;
      font-size: 1.2em;
      color: #111;
      text-decoration: none;
      transition: color 0.3s;
    }

    .menu ul li a:hover {
      color: #999;
    }

    @media (max-width: 768px) {
      .showcase header {
        padding: 20px 30px;
      }

      .text h2 {
        font-size: 2em;
      }

      .text p {
        font-size: 1em;
      }
    }
  </style>
</head>
<body>

  <section class="showcase">
    <header>
      <h2 class="logo"><a href="index.html">Nicole + Jeremy</a></h2>
      <div class="toggle"></div>
    </header>

    <video src="header.mp4" loop autoplay></video>
    <div class="overlay"></div>
    <div class="text">
      <h2>Diving In</h2>
      <h3>May 23, 2026</h3>
      <p>Playa Grande, Costa Rica</p>
      <a href="RSVP.html">RSVP</a>
    </div>
  </section>

  <div class="menu">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="RSVP.html">RSVP</a></li>
      <li><a href="TravelDetails.html">Travel Details</a></li>
      <li><a href="venue.html">Wedding Details</a></li>
      <li><a href="CostaRica.html">Costa Rica</a></li>
    </ul>
  </div>

  <script>
    const menuToggle = document.querySelector('.toggle');
    const showcase = document.querySelector('.showcase');
    const menu = document.querySelector('.menu');
    const menuLinks = document.querySelectorAll('.menu a');

    menuToggle.addEventListener('click', () => {
      menuToggle.classList.toggle('active');
      showcase.classList.toggle('active');
      menu.classList.toggle('active');
    });

    menuLinks.forEach(link => {
      link.addEventListener('click', () => {
        menuToggle.classList.remove('active');
        showcase.classList.remove('active');
        menu.classList.remove('active');
      });
    });
  </script>

</body>
</html>
# WEDDING
