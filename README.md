<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Para Daniela 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to top right, #ffc3a0, #ffafbd);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding-top: 100px;
      color: #fff;
      z-index: 2;
      position: relative;
    }

    h1 {
      font-size: 3em;
      margin-bottom: 20px;
    }

    .card {
      position: relative;
      width: 300px;
      height: 400px;
      background: url('https://images.emojiterra.com/openmoji/v15.1/1024px/1f48c.png') no-repeat center center;
      background-size: cover;
      margin: 0 auto;
      cursor: pointer;
      transition: transform 0.5s;
      border-radius: 10px;
    }

    .card.open {
      transform: rotateY(180deg);
    }

    .message {
      display: none;
      font-size: 1.2em;
      padding: 20px;
      background-color: white;
      color: #333;
      position: absolute;
      top: 10%; 
      left: 50%;
      transform: translateX(-50%);
      width: 80%;
      max-width: 600px;
      text-align: left;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
      z-index: 10;
      max-height: 70vh;
      overflow-y: auto;
      line-height: 1.6;
    }

    .music-btn {
      margin-top: 20px;
      background-color: #fff;
      color: #e91e63;
      border: none;
      padding: 12px 24px;
      font-size: 1em;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }

    .music-btn:hover {
      background-color: #ffe6e6;
    }

    .footer {
      position: absolute;
      bottom: 20px;
      width: 100%;
      text-align: center;
      font-size: 0.9em;
      color: #fff;
    }

    .heart {
      position: absolute;
      font-size: 40px;
      color: #ff4d88;
      animation: floatHeart 5s infinite;
    }

    @keyframes floatHeart {
      0% {
        transform: translateY(0);
        opacity: 1;
      }
      100% {
        transform: translateY(-300px);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <audio id="audio" loop>
    <source src="c:\\Users\\carlo\\OneDrive\\Escritorio\\S.A.C\\Programación\\Camilo - Corazón de Hojalata (Letra Lyrics).m4a" type="audio/mpeg">
    Tu navegador no soporta audio.
  </audio>

  <div class="container">
    <h1>Para Mi Daniela 💖</h1>
    <p>Haz clic en la carta para leerla.</p>

    <div class="card" onclick="openMessage()"></div>

    <div id="message" class="message">
      <p>
        Desde que te conocí, no puedo dejar de pensar en lo increíble que eres.  <br>
        Eres esa chispa que ilumina cualquier día gris,  <br>
        y siempre sabes cómo sacar una sonrisa en los momentos más inesperados.  <br><br>

        En este pequeño detalle que he creado con todo mi cariño,  <br>
        quiero que sepas que cada palabra, cada letra, lleva un pedazo de mi corazón.  <br><br>

        No importa cuántas veces me cueste encontrar las palabras adecuadas,  <br>
        siempre voy a querer que sepas lo especial que eres para mí.  <br>
        Gracias por ser tú, por hacer el mundo un lugar más bonito con tu presencia.  <br><br>

        Eres mi inspiración,  <br>
        mi basquetbolista favorita,  <br>
        esa chica a la que quiero dedicar mis canastas (aunque falle algunas... jijiji).  <br><br>

        Y aunque esto sea solo una página web, está hecha con todo mi cariño.  <br>
        Quiero que sepas que tienes alguien aquí que te quiere,  <br>
        que amaría estar a tu lado,  <br>
        y que estaría dispuesto a esperar.  <br><br>

        Porque quiero que seas esa persona que me acompañe el resto de mi vida,  <br>
        con quien jugaría mi deporte favorito,  <br>
        con quien vería nuestras series favoritas,  <br>
        con quien cocinaría, a quien cuidaría el resto de mi vida.  <br><br>

        Y lo más importante...  <br>
        con quien iría a la iglesia a alabar a nuestro Dios. 💌  
      </p>
    </div>

    <button id="music-btn" class="music-btn" onclick="toggleMusic()">Reproducir Música</button>
  </div>

  <div class="footer">
    Hecho con 💻 y 💘 por alguien que piensa en ti.
  </div>

  <script>
    function openMessage() {
      document.getElementById('message').style.display = 'block';
      document.querySelector('.card').classList.add('open');
    }

    function toggleMusic() {
      const audio = document.getElementById('audio');
      const button = document.getElementById('music-btn');

      if (audio.paused) {
        audio.play();
        button.textContent = 'Pausar Música';
      } else {
        audio.pause();
        button.textContent = 'Reproducir Música';
      }
    }

    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.textContent = '❤️';
      document.body.appendChild(heart);

      const x = Math.random() * window.innerWidth;
      const duration = Math.random() * 2 + 3;
      heart.style.left = `${x}px`;

      setTimeout(() => {
        heart.remove();
      }, duration * 1000);
    }

    setInterval(createHeart, 500);
  </script>
</body>
</html>

