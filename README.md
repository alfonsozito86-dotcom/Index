<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MyLady</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #fceabb, #f8b500);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      font-family: 'Garamond', serif;
      overflow: hidden;
      position: relative;
    }

    .container {
      position: relative;
      width: 100%;
      height: 100%;
      text-align: center;
    }

    .heart {
      width: 120px;
      height: 108px;
      position: absolute;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-45deg);
      background: crimson;
      cursor: pointer;
      transition: opacity 1.5s ease, transform 1.5s ease;
      z-index: 2;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 120px;
      height: 108px;
      background: crimson;
      border-radius: 50%;
    }

    .heart::before {
      top: -60px;
      left: 0;
    }

    .heart::after {
      left: 60px;
      top: 0;
    }

    .message {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 1.8em;
      color: #3c2f2f;
      opacity: 0;
      transition: opacity 2s ease;
      z-index: 1;
      padding: 20px;
      background: rgba(255, 255, 255, 0.7);
      border-radius: 12px;
      backdrop-filter: blur(6px);
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }

    .show-message {
      opacity: 1;
    }

    .hide-heart {
      opacity: 0;
      transform: scale(0.5);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="heart" onclick="revealMessage()"></div>
    <div class="message" id="romanticMessage">SE RINASCO<br>VENGO A CERCARTI PRIMA</div>
  </div>

  <script>
    function revealMessage() {
      document.querySelector('.heart').classList.add('hide-heart');
      document.getElementById('romanticMessage').classList.add('show-message');
    }
  </script>
</body>
</html>
