<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ryza Mahasol | Personal Portfolio</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: #35263f;
      background: #ffffff;
    }

    /* NAVIGATION */

    nav {
      min-height: 60px;
      background: white;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 8%;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.08);
    }

    .logo {
      font-size: 17px;
      font-weight: bold;
      color: #542b72;
      letter-spacing: 1px;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 25px;
    }

    nav ul li a {
      text-decoration: none;
      color: #555;
      font-size: 14px;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #7b3fa0;
    }

    /* HOME */

    .hero {
      min-height: 470px;
      background: linear-gradient(
        135deg,
        #80698b,
        #684f75
      );

      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      padding: 40px 20px;
    }

    .hero h1 {
      font-size: clamp(42px, 7vw, 75px);
      letter-spacing: -2px;
    }

    .hero p {
      margin-top: 18px;
      font-size: 18px;
      letter-spacing: 3px;
    }

    .hero-line {
      width: 80px;
      height: 5px;
      background: white;
      margin: 25px auto;
      border-radius: 10px;
    }

    /* PROFILE */

    .profile {
      background: #eee7ff;
      padding: 50px 9%;
      display: flex;
      align-items: center;
      gap: 40px;
    }

    .profile-photo {
      width: 200px;
      height: 200px;
      flex-shrink: 0;
      border-radius: 8px;
      overflow: hidden;
      background: #d9c8ef;
      box-shadow: 0 8px 20px rgba(60,30,80,0.15);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .profile-photo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .photo-placeholder {
      color: #542b72;
      font-size: 18px;
      font-weight: bold;
      text-align: center;
      padding: 15px;
    }

    .profile-text {
      max-width: 750px;
    }

    .profile-text h2 {
      font-size: 32px;
      color: #4e2869;
      margin-bottom: 15px;
    }

    .profile-text p {
      line-height: 1.8;
      font-size: 15px;
      color: #514858;
    }

    /* SECTIONS */

    section {
      padding: 70px 9%;
    }

    .section-title {
      text-align: center;
      color: #542b72;
      font-size: 34px;
      margin-bottom: 40px;
    }

    /* CARDS */

    .cards {
      max-width: 1100px;
      margin: auto;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .card {
      background: white;
      border: 1px solid #e8dfed;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(50,30,70,0.08);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(50,30,70,0.13);
    }

    .card-image {
      height: 150px;
      background: #eee7ff;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 55px;
    }

    .card-content {
      padding: 22px;
    }

    .card-content h3 {
      color: #542b72;
      margin-bottom: 10px;
    }

    .card-content p {
      font-size: 14px;
      line-height: 1.7;
      color: #625b67;
    }

    /* ABOUT */

    .about {
      background: #faf8fc;
    }

    .about-container {
      max-width: 1050px;
      margin: auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .about-box {
      background: white;
      padding: 30px;
      border: 1px solid #eee5f3;
      box-shadow: 0 5px 15px rgba(50,30,70,0.06);
      border-radius: 8px;
    }

    .about-box h3 {
      color: #542b72;
      margin-bottom: 15px;
    }

    .about-box p {
      line-height: 1.8;
      font-size: 14px;
      color: #625b67;
    }

    /* FAMILY */

    .family {
      text-align: center;
    }

    .family p {
      max-width: 750px;
      margin: auto;
      line-height: 1.8;
      color: #625b67;
    }

    /* DREAMS */

    .dreams {
      background: #eee7ff;
      text-align: center;
    }

    .dreams p {
      max-width: 750px;
      margin: auto;
      line-height: 1.9;
      color: #514858;
    }

    .dream-button {
      display: inline-block;
      margin-top: 25px;
      padding: 13px 25px;
      background: #67358a;
      color: white;
      text-decoration: none;
      border-radius: 25px;
      transition: 0.3s;
    }

    .dream-button:hover {
      background: #4e2869;
    }

    /* FOOTER */

    footer {
      background: #4e2869;
      color: white;
      text-align: center;
      padding: 30px;
    }

    footer p {
      margin: 6px;
      font-size: 13px;
    }

    /* MOBILE */

    @media (max-width: 750px) {

      nav {
        padding: 12px 5%;
      }

      nav ul {
        display: none;
      }

      .profile {
        flex-direction: column;
        text-align: center;
      }

      .profile-photo {
        width: 180px;
        height: 180px;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .about-container {
        grid-template-columns: 1fr;
      }

      .hero {
        min-height: 400px;
      }

      .hero h1 {
        font-size: 45px;
      }

      .profile-text h2 {
        font-size: 28px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="logo">RYZA MAHASOL</div>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About Me</a></li>
      <li><a href="#school">School</a></li>
      <li><a href="#family">Family</a></li>
      <li><a href="#dreams">Dreams</a></li>
    </ul>
  </nav>


  <!-- HOME -->

  <section class="hero" id="home">
    <div>
      <h1>My Personal Portfolio</h1>

      <div class="hero-line"></div>

      <p>LEARN • GROW • DREAM</p>
    </div>
  </section>


  <!-- PROFILE -->

  <section class="profile">

    <div class="profile-photo">

      <img
        src="formal.jpg"
        alt="Ryza Mahasol"
        onerror="this.style.display='none'; document.getElementById('photoPlaceholder').style.display='block';"
      >

      <div class="photo-placeholder" id="photoPlaceholder" style="display:none;">
        RYZA<br>MAHASOL
      </div>

    </div>

    <div class="profile-text">

      <h2>RYZA MAHASOL</h2>

      <p>
        I am Ryza Mahasol, a Bachelor of Elementary Education
        student and an aspiring teacher. I am a simple,
        determined, and family-oriented person who believes
        that education, hard work, and kindness can help
        create a better future.
      </p>

      <br>

      <p>
        I enjoy listening to music, reading Wattpad stories,
        and spending time talking with friends. This portfolio
        shares a little about me, my school journey, my family,
        and the dreams I continue to work toward.
      </p>

    </div>

  </section>


  <!-- MAIN CARDS -->

  <section>

    <div class="cards">

      <div class="card">

        <div class="card-image">💜</div>

        <div class="card-content">

          <h3>About Me</h3>

          <p>
            Get to know my personality, interests,
            hobbies, values, and the things that
            make me who I am.
          </p>

        </div>

      </div>


      <div class="card" id="school">

        <div class="card-image">🎓</div>

        <div class="card-content">

          <h3>My School Journey</h3>

          <p>
            My journey as a Bachelor of Elementary
            Education student and my preparation
            to become a future teacher.
          </p>

        </div>

      </div>


      <div class="card" id="family">

        <div class="card-image">🏡</div>

        <div class="card-content">

          <h3>My Family</h3>

          <p>
            My family is one of the most important
            parts of my life and one of my biggest
            inspirations.
          </p>

        </div>

      </div>

    </div>

  </section>


  <!-- ABOUT ME -->

  <section class="about" id="about">

    <h2 class="section-title">About Me ♡</h2>

    <div class="about-container">

      <div class="about-box">

        <h3>🎓 My Education</h3>

        <p>
          I am taking Bachelor of Elementary Education.
          My goal is to become a teacher who can help
          children learn, grow, and believe in themselves.
        </p>

      </div>


      <div class="about-box">

        <h3>🌷 My Interests</h3>

        <p>
          I love listening to music, reading Wattpad,
          talking with friends, and enjoying simple
          moments. I also love cute, simple, aesthetic
          things, especially the color purple.
        </p>

      </div>


      <div class="about-box">

        <h3>✨ My Personality</h3>

        <p>
          I am a kind and determined person. I may be
          shy around people I do not know well, but I
          always try to keep learning and improving myself.
        </p>

      </div>


      <div class="about-box">

        <h3>🌱 My Values</h3>

        <p>
          I value family, education, kindness,
          perseverance, friendship, and personal growth.
        </p>

      </div>

    </div>

  </section>


  <!-- FAMILY -->

  <section class="family" id="family-section">

    <h2 class="section-title">My Family ♡</h2>

    <p>

      My family is a very important part of my life.
      They are one of the reasons why I continue to
      study and work hard.

      <br><br>

      My dream is to become a teacher, build a stable
      future, and someday be able to support my family
      and give back to the people who have always
      supported me.

    </p>

  </section>


  <!-- DREAMS -->

  <section class="dreams" id="dreams">

    <h2 class="section-title">My Dreams ✨</h2>

    <p>

      One of my biggest dreams is to become a good,
      caring, and dedicated elementary teacher.

      <br><br>

      I want to help children discover their abilities,
      enjoy learning, and believe that they can achieve
      their dreams too.

      <br><br>

      I know that the journey may not always be easy,
      but I will continue to learn, grow, and move
      forward.

    </p>

    <a href="#home" class="dream-button">
      Back to Top ↑
    </a>

  </section>


  <!-- FOOTER -->

  <footer>

    <p>
      <strong>RYZA MAHASOL PORTFOLIO</strong>
    </p>

    <p>
      My story • My journey • My dreams 💜
    </p>

    <p>
      © 2026 Ryza Mahasol
    </p>

  </footer>

</body>
</html>
