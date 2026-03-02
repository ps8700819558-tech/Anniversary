<!DOCTYPE html>
<html>
<head>
  <title>Happy Anniversary ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #fff5e6, #ffe6cc);
      padding-top: 80px;
      overflow: hidden;
    }

    h1 {
      color: #b30000;
      font-size: 30px;
      padding: 0 20px;
    }

    button {
      padding: 14px 24px;
      font-size: 18px;
      margin: 15px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
    }

    #yesBtn {
      background-color: #cc0000;
      color: white;
    }

    #noBtn {
      background-color: #555;
      color: white;
      position: absolute;
    }

    #message {
      font-size: 24px;
      color: #990000;
      margin-top: 25px;
      padding: 0 20px;
    }

    .heart {
      position: fixed;
      top: -10px;
      font-size: 18px;
      animation: fall 2s linear infinite;
      color: red;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh);
      }
    }

    .confetti {
      position: fixed;
      width: 8px;
      height: 8px;
      background: red;
      top: 0;
      animation: confettiFall 3s linear forwards;
    }

    @keyframes confettiFall {
      to {
        transform: translateY(100vh) rotate(720deg);
      }
    }
  </style>
</head>

<body>

<h1>Will you celebrate every anniversary with me forever? 💍❤️</h1>

<button id="yesBtn" onclick="showLove()">Always Yes ❤️</button>
<button id="noBtn" onmouseover="moveButton()">No 😜</button>

<div id="message"></div>

<script>
function showLove() {
  document.getElementById("message").innerHTML =
    "Happy Anniversary My Love ❤️💍<br><br>You are my forever, my home, my happiness 🥹💖<br><br>Forever Yours,<br>Priyanka ❤️";

  startHearts();
  confettiBlast();
}

function moveButton() {
  let btn = document.getElementById("noBtn");

  let maxX = window.innerWidth - 120;
  let maxY = window.innerHeight - 80;

  let x = Math.random() * maxX;
  let y = Math.random() * maxY;

  btn.style.left = x + "px";
  btn.style.top = y + "px";
}

function startHearts() {
  setInterval(function () {
    let heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (Math.random() * 15 + 15) + "px";
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 2000);
  }, 200);
}

function confettiBlast() {
  for (let i = 0; i < 120; i++) {
    let confetti = document.createElement("div");
    confetti.classList.add("confetti");
    confetti.style.left = Math.random() * 100 + "vw";
    confetti.style.background = ["red", "gold", "pink", "orange"][Math.floor(Math.random()*4)];
    document.body.appendChild(confetti);

    setTimeout(() => confetti.remove(), 3000);
  }
}
</script>

</body>
</html>
