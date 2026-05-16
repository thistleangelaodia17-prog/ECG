# ECG
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Pulsating Heart</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #111;
    }

    .heart {
      position: relative;
      width: 100px;
      height: 90px;
      background: red;
      transform: rotate(-45deg);
      animation: pulse 1s infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 90px;
      background: red;
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

    @keyframes pulse {
      0%   { transform: rotate(-45deg) scale(1); }
      50%  { transform: rotate(-45deg) scale(1.2); }
      100% { transform: rotate(-45deg) scale(1); }
    }
  </style>
</head>
<body>
  <div class="heart"></div>
</body>
</html>
