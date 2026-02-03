<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Will You Be My Valentine?</title>
  < style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: #ffd6e8;
      font-family: Arial, sans-serif;
    }

    .card {
      background: #fff;
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      width: 320px;
      position: relative;
    }

    .emoji {
      font-size: 60px;
    }

    h2 {
      margin: 20px 0;
    }

    .buttons {
      margin-top: 20px;
      position: relative;
      height: 120px;
    }

    button {
      padding: 12px 25px;
      border: none;
      border-radius: 25px;
      font-size: 16px;
      cursor: pointer;
    }

    #yes {
      background: #ff4d6d;
      color: white;
    }

    #no {
      position: absolute;
      background: #ccc;
    }
  </style>
</head>
<body>

<div class="card">
  <div class="emoji">🐻❤️</div>
  <h2><span id="name">aaani</span>, will you be my Valentine?</h2>

  <div class="buttons">
    <button id="yes" onclick="yesClicked()">Yes</button>
    <button id="no" onmouseover="moveNo()">No</button>
  </div>

  <p id="message"></p>
</div>

<script>
  function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 200;
    const y = Math.random() * 80;
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }

  function yesClicked() {
    document.getElementById("message").innerHTML =
      "💖 Yay! I knew it 😍";
  }
</script>

</body>
</html>
