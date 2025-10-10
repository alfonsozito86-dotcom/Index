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
      background: radial-gradient(circle at center, #ffdee9, #b5fffc);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      font-family: 'Georgia', serif;
      overflow: hidden;
      position: relative;
    }

    .container {
      position: relative;
      width: 200px;
      height: 200px;
    }

    .heart {
      width: 100px;
      height: 90px;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-45deg);
      background: crimson;
      transition: opacity 1.5s ease;
      cursor: pointer;
      z-index: 2;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 90px;
      background: crimson;
      border-radius: 50%;
    }

    .heart::before {
      top: -50px;
      left: 0;
    }

    .heart::after {
      left: 50px;
      top: 0;
    }

    .message {
      position: absolute;

    function showMessage() {
      document.getElementById("romanticMessage").classList.add("show");
    }
  </script>
</body>
</html>
