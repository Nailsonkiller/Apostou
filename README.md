# Apostou
Postagens 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Galeria da Marca</title>
  <style>
    body {
      margin: 0;
      background: #111;
      font-family: Arial, sans-serif;
      color: #fff;
      text-align: center;
    }

    h1 {
      margin-top: 20px;
    }

    .slider {
      position: relative;
      max-width: 800px;
      margin: 40px auto;
      overflow: hidden;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.5);
    }

    .slides {
      display: flex;
      transition: transform 0.6s ease-in-out;
      width: 100%;
    }

    .slide {
      min-width: 100%;
      box-sizing: border-box;
    }

    .slide img {
      width: 100%;
      height: auto;
      display: block;
    }

    .controls {
      position: absolute;
      top: 50%;
      width: 100%;
      display: flex;
      justify-content: space-between;
      transform: translateY(-50%);
      padding: 0 10px;
    }

    .controls button {
      background: rgba(0,0,0,0.5);
      border: none;
      color: white;
      font-size: 24px;
      padding: 10px;
      cursor: pointer;
      border-radius: 50%;
    }

    .controls button:hover {
      background: rgba(255,255,255,0.2);
    }
  </style>
</head>
<body>

  <h1>Galeria da Marca - Apostou Oficial</h1>

  <div class="slider">
    <div class="slides" id="slides">
      <!-- Slide 1: Jogador -->
      <div class="slide">
        <img src="Captura de tela 2025-08-05 092824.png" alt="Jogador Apostou">
      </div>

      <!-- Slide 2: Raspinha -->
      <div class="slide">
        <img src="Captura de tela 2025-08-05 092848.png" alt="Mascote Raspinha">
      </div>
    </div>

    <!-- Controles -->
    <div class="controls">
      <button onclick="prevSlide()">❮</button>
      <button onclick="nextSlide()">❯</button>
    </div>
  </div>

  <script>
    let index = 0;
    const slides = document.getElementById('slides');
    const totalSlides = slides.children.length;

    function showSlide(i) {
      index = (i + totalSlides) % totalSlides;
      slides.style.transform = `translateX(${-index * 100}%)`;
    }

    function nextSlide() {
      showSlide(index + 1);
    }

    function prevSlide() {
      showSlide(index - 1);
    }

    // Troca automática a cada 5 segundos
    setInterval(nextSlide, 5000);
  </script>

</body>
</html>
