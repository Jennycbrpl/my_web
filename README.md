<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hola, soy Jenny </title>
  <style>
    /* ====== RESET ====== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Poppins", sans-serif;
      color: #fff;
      background: radial-gradient(circle at 20% 20%, #1e1e2f, #0d0d16 80%);
      background-size: 400% 400%;
      animation: galaxyMove 15s ease infinite;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      text-align: center;
    }

    @keyframes galaxyMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* ====== HEADER ====== */
    header {
      margin-top: 3rem;
    }

    .typewriter {
      font-size: 2rem;
      border-right: 3px solid #fff;
      white-space: nowrap;
      overflow: hidden;
      width: 0;
      animation: typing 3s steps(30, end) forwards, blink 0.8s infinite;
    }

    @keyframes typing {
      from { width: 0; }
      to { width: 100%; }
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    /* ====== MAIN ====== */
    main {
      flex-grow: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      flex-wrap: wrap;
      padding: 2rem;
    }

    img {
      max-width: 280px;
      border-radius: 20px;
      box-shadow: 0 0 25px rgba(255,255,255,0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    img:hover {
      transform: scale(1.05);
      box-shadow: 0 0 40px rgba(255,255,255,0.4);
    }

    /* ====== RANDOM PICS SECTION ====== */
    section#random-pics {
      margin: 4rem 0;
      text-align: center;
    }

    section#random-pics h2 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }

    section#random-pics p {
      font-size: 1rem;
      opacity: 0.8;
      margin-bottom: 2rem;
    }

    .gallery {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
    }

    /* ====== FOOTER ====== */
    footer {
      padding: 1rem;
      font-size: 0.9rem;
      opacity: 0.7;
    }
  </style>
</head>
<body>
  <!-- HEADER -->
  <header>
    <div id="typewriter" class="typewriter"></div>
  </header>

  <!-- MAIN -->
  <main>
    <img src="foto2jpg.jpg" alt="Foto 1">
    <img src="fotoJenny.jpg" alt="Foto Jenny">
  </main>

  <!-- RANDOM PICS -->
  <section id="random-pics">
    <h2>📸 Random Pics</h2>
    <p>Colección de fotos random con mini descripciones ✨</p>
    <div class="gallery">
      <img src="random1.jpg" alt="Random 1">
      <img src="random2.jpg" alt="Random 2">
      <img src="random3.jpg" alt="Random 3">
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    Handmade by me © 2025
  </footer>

  <!-- SCRIPT -->
  <script>
    const frases = [
      "🌎 Hola, soy Jenny ",
      "Hello, I'm Jenny ",
      "Привет, я Дженни ",
      "Ciao, sono Jenny ",
      "Hallo, ich bin Jenny ",
      "你好，我是Jenny ",
      "こんにちは、私はジェニーです ",
      "नमस्ते, मैं जेनी हूँ ",
      "🌎 Ñuqaqa Jenny kani "
    ];

    let i = 0;
    const typewriter = document.getElementById("typewriter");

    function escribir(frase) {
      typewriter.textContent = "";
      typewriter.style.width = "0";
      let j = 0;
      const interval = setInterval(() => {
        if (j < frase.length) {
          typewriter.textContent += frase[j];
          j++;
        } else {
          clearInterval(interval);
          setTimeout(() => borrar(), 1500);
        }
      }, 120);
    }

    function borrar() {
      setTimeout(() => {
        typewriter.style.width = "0";
        i = (i + 1) % frases.length;
        escribir(frases[i]);
        document.title = frases[i];
      }, 6000);
    }

    escribir(frases[i]);
  </script>
</body>
</html>
