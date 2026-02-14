<!DOCTYPE html>  
<html lang="es">  
<head>  
  <meta charset="UTF-8" />  
  <title>Para mi morrodita 💘</title>  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  
  <style>  
    body {  
      margin: 0;  
      padding: 0;  
      font-family: system-ui, sans-serif;  
      background: linear-gradient(135deg, #ff7ac6, #ffb3ec, #ffd6f6);  
      min-height: 100vh;  
      overflow: hidden;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      text-align: center;  
      color: #4a0035;  
    }  
  
    /* Corazones flotando */  
    .heart {  
      position: fixed;  
      bottom: -10px;  
      color: #ff2e93;  
      font-size: 20px;  
      animation: floatUp 6s linear infinite;  
      opacity: 0.7;  
    }  
  
    @keyframes floatUp {  
      0% { transform: translateY(0) translateX(0); opacity: 0.7; }  
      100% { transform: translateY(-120vh) translateX(20px); opacity: 0; }  
    }  
  
    .container {  
      max-width: 500px;  
      padding: 20px;  
      z-index: 10;  
    }  
  
    /* Pantalla inicial */  
    .start-btn {  
      font-size: 32px;  
      font-weight: 700;  
      padding: 20px 30px;  
      border-radius: 20px;  
      background: white;  
      color: #ff2e93;  
      border: none;  
      cursor: pointer;  
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);  
      transition: transform .2s;  
    }  
  
    .start-btn:hover {  
      transform: scale(1.05);  
    }  
  
    /* Tarjeta principal */  
    .card {  
      display: none;  
      background: rgba(255,255,255,0.85);  
      padding: 25px;  
      border-radius: 20px;  
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);  
      animation: fadeIn 1s ease;  
    }  
  
    @keyframes fadeIn {  
      from { opacity: 0; transform: scale(0.95); }  
      to { opacity: 1; transform: scale(1); }  
    }  
  
    h1 {  
      font-size: 26px;  
      margin-bottom: 10px;  
      color: #d1006b;  
    }  
  
    p {  
      font-size: 15px;  
      line-height: 1.5;  
      margin-bottom: 15px;  
    }  
  
    .secret-btn {  
      margin-top: 15px;  
      padding: 10px 15px;  
      border-radius: 15px;  
      border: none;  
      background: #ff2e93;  
      color: white;  
      cursor: pointer;  
      font-size: 14px;  
      transition: .2s;  
    }  
  
    .secret-btn:hover {  
      background: #d1006b;  
    }  
  
    .secret {  
      display: none;  
      margin-top: 15px;  
      background: rgba(255,255,255,0.95);  
      padding: 15px;  
      border-radius: 15px;  
      color: #4a0035;  
      animation: fadeIn 1s ease;  
    }  
  </style>  
</head>  
  
<body>  
  
  <!-- Corazones flotando -->  
  <script>  
    function createHeart() {  
      const heart = document.createElement("div");  
      heart.classList.add("heart");  
      heart.innerHTML = "❤️";  
      heart.style.left = Math.random() * 100 + "vw";  
      heart.style.animationDuration = (4 + Math.random() * 4) + "s";  
      document.body.appendChild(heart);  
  
      setTimeout(() => heart.remove(), 7000);  
    }  
    setInterval(createHeart, 500);  
  </script>  
  
  <div class="container">  
  
    <!-- Pantalla inicial -->  
    <button class="start-btn" onclick="showCard()">  
      Para mi morrodita 💘  
    </button>  
  
    <!-- Contenido revelado -->  
    <div id="mainCard" class="card">  
      <h1>Para ti, mi morrodita 💞</h1>  
  
      <p>  
        Hoy no solo quiero celebrar San Valentín…    
        quiero celebrar <b>a nosotros</b>.  
      </p>  
  
      <p>  
        Gracias por estos 3 meses, por estar conmigo a pesar de la distancia,    
        por no soltarme incluso cuando discutimos,    
        y por demostrarme que quieres seguir aquí conmigo.  
      </p>  
  
      <p>  
        A veces chocamos, a veces nos frustramos,    
        pero siempre encontramos el camino de vuelta.    
        Y eso, morrodita, vale más que cualquier pelea.  
      </p>  
  
      <p>  
        Quiero seguir contigo, seguir creciendo,    
        seguir aprendiendo a amarnos mejor.    
        Te quiero más de lo que estas palabras pueden decir.  
      </p>  
  
      <button class="secret-btn" onclick="toggleSecret()">  
        Mensaje secreto 💗  
      </button>  
  
      <!-- Mensaje íntimo -->  
      <div id="secretMessage" class="secret">  
        <p>  
          Morrodita… gracias por confiar en mí de una manera tan profunda.    
          No hablo solo de lo que sentimos, sino también de cómo te has permitido    
          mostrarte conmigo tal cual eres, sin miedo, incluso en lo físico.  
        </p>  
  
        <p>  
          Esa confianza tuya significa muchísimo para mí.    
          Me hace querer cuidarte más, respetarte más    
          y demostrarte que siempre voy a valorar lo que compartimos.  
        </p>  
  
        <p>  
          Lo que me has mostrado, lo guardo con cariño y respeto.    
          Gracias por abrirte conmigo, morrodita.  
        </p>  
      </div>  
    </div>  
  </div>  
  
  <script>  
    function showCard() {  
      document.querySelector(".start-btn").style.display = "none";  
      document.getElementById("mainCard").style.display = "block";  
  
      // Música  
      const audio = document.getElementById("music");  
      if (audio) audio.play();  
    }  
  
    function toggleSecret() {  
      const box = document.getElementById("secretMessage");  
      box.style.display = box.style.display === "none" ? "block" : "none";  
    }  
  </script>  
  
  <!-- MÚSICA: aquí pegas el link del audio -->  
  <audio id="music" src="AQUÍ_VA_TU_AUDIO.mp3" preload="auto"></audio>  
  
</body>  
</html>  
