<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amal</title>
    <style>
      body {
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="5" y="25" font-family="Arial" font-size="5" fill="rgba(255, 255, 255, 0.1)">Amal</text></svg>');
        background-color: #ffe6f2;
        overflow: hidden;
      }

      .flower-container {
        position: relative;
        animation: rotate 10s linear infinite;
      }

      .flower {
        font-size: 500px;
        color: #ff1493;
        animation: float 5s ease-in-out infinite alternate; /* animation de flottement */
      }

      .star {
        position: absolute;
        color: white;
        font-size: 30px;
        animation: sparkle 2s infinite linear alternate;
      }

      .name {
        font-weight: bold;
      }

      @keyframes float {
        0% {
          transform: translateY(0);
        }
        50% {
          transform: translateY(-20px);
        }
        100% {
          transform: translateY(0);
        }
      }

      @keyframes rotate {
        0% {
          transform: rotate(0deg);
        }
        100% {
          transform: rotate(360deg);
        }
      }

      @keyframes sparkle {
        0% {
          opacity: 0.5;
          transform: scale(1);
        }
        50% {
          opacity: 1;
          transform: scale(1.2);
        }
        100% {
          opacity: 0.5;
          transform: scale(1);
        }
      }

      .button-container {
        text-align: center; /* aligner les boutons au centre */
        margin-top: 20px;
      }

      .button {
        margin: 5px;
        padding: 10px 20px;
        font-size: 16px;
        background-color: #ff1493; /* rose */
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s;
      }

      .button:hover {
        background-color: #ff69b4; /* rose plus clair au survol */
      }

      .heart-button {
        font-size: 50px;
        padding: 20px 40px;
        margin-top: 20px;
        background-color: #ff1493; /* rose */
        color: white;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.3s;
      }

      .heart-button:hover {
        background-color: #ff69b4; /* rose plus clair au survol */
        transform: scale(1.1);
      }

      .heart {
        display: none;
        font-size: 100px;
        color: #ff1493; /* rose */
        margin-top: 20px;
      }

      .flower-img {
        display: none;
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <div class="flower-container">
      <div class="flower">&#127802;</div>
      <div class="star" style="top: 40%; left: 30%">&#9733;</div>
      <div class="star" style="top: 50%; left: 60%">&#9733;</div>
      <div class="star" style="top: 70%; left: 40%">&#9733;</div>
      <div class="star" style="top: 20%; left: 80%">&#9733;</div>
      <div class="star" style="top: 80%; left: 20%">&#9733;</div>
    </div>
    <h1><span class="name">Amal</span></h1>
    <div class="button-container">
      <button class="button" onclick="showValentineMessage()">
        Clique pour recevoir ton cadeau
      </button>
    </div>

    <div id="valentine-message" style="display: none">
      <h2>Voulez-vous être ma Valentine très chère dulcinée?</h2>
      <div class="button-container">
        <button class="button" onclick="showHeart()">Oui</button>
        <button class="button" onclick="showHamara()">Non</button>
      </div>
    </div>

    <div class="heart">
      &#10084;
      <img
        src="https://emojicdn.elk.sh/🌹"
        alt="fleur rouge"
        class="flower-img"
      />
      Je t'aime HAYATI!
    </div>

    <script>
      function showValentineMessage() {
        document.getElementById("valentine-message").style.display = "block";
      }

      function showHeart() {
        var heart = document.querySelector(".heart");
        var flowerImg = document.querySelector(".flower-img");
        heart.style.display = "block";
        flowerImg.style.display = "block";
      }

      function showHamara() {
        var hamara = document.createElement("div");
        hamara.innerText = "🐴🐴🐴 Hamara! 🐴🐴🐴";
        hamara.style.position = "absolute";
        hamara.style.top = "0";
        hamara.style.left = "50%";
        hamara.style.transform = "translate(-50%, 0)";
        hamara.style.fontSize = "40px";
        hamara.style.color = "#ff1493"; /* rose */
        document.body.appendChild(hamara);

        setTimeout(function () {
          hamara.style.opacity = "0";
          setTimeout(function () {
            hamara.remove();
          }, 1000);
        }, 2000);
      }
    </script>
  </body>
</html>
