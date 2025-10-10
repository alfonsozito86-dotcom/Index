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
      height
