<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Young Adults Game Night</title>
  <style>
    body, html {
      margin: 0; padding: 0;
      font-family: 'Comic Sans MS', Papyrus, cursive;
      background: linear-gradient(to bottom, #ffefc0, #ffd59a, #ffe8b0);
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .envelope {
      width: 250px; height: 180px;
      background: linear-gradient(to bottom, #f59e0b, #d97706);
      border: 4px solid #b45309;
      border-radius: 12px;
      display: flex; align-items: center; justify-content: center;
      cursor: pointer;
      box-shadow: 0 6px 15px rgba(0,0,0,0.3);
      position: relative;
      transform-style: preserve-3d;
      transition: transform 1s ease-in-out;
    }
    .envelope.open {
      transform: rotateX(180deg);
    }
    .envelope span {
      color: white;
      font-weight: bold;
      font-size: 18px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.4);
    }
    .scroll {
      background: #fffae5;
      border: 4px solid #b45309;
      border-radius: 12px;
      padding: 20px;
      max-width: 300px;
      text-align: center;
      box-shadow: 0 6px 15px rgba(0,0,0,0.3);
      opacity: 0;
      transform: scaleY(0);
      transform-origin: top;
      transition: opacity 1s ease, transform 1s ease;
      position: absolute;
      top: -50px;
    }
    .scroll.show {
      opacity: 1;
      transform: scaleY(1);
    }
    h1 { font-size: 20px; margin: 5px 0; }
    h2 { font-size: 24px; margin: 10px 0; color: #c2410c; }
    p { margin: 5px 0; font-size: 16px; }
    @media (max-width: 500px) {
      .envelope { width: 200px; height: 140px; }
      .scroll { max-width: 90%; padding: 15px; }
      h1 { font-size: 18px; }
      h2 { font-size: 20px; }
      p { font-size: 14px; }
    }
  </style>
</head>
<body>
  <div class="envelope" id="envelope"><span>CLICK HERE</span></div>
  <div class="scroll" id="scroll">
    <h1>YOUNG ADULTS</h1>
    <h2>GAME NIGHT!!!</h2>
    <p><strong>DATE</strong><br>OCTOBER 31ST</p>
    <p><strong>TIME</strong><br>6PM</p>
    <p><strong>LOCATION</strong><br>1767 NE Regatta Dr</p>
    <p><strong>ATTIRE</strong><br>COSTUME OR PAJAMAS</p>
    <p>BRING YOUR FRIENDS</p>
    <p>YOUR GAME FACE</p>
    <p>AND FOOD TO SHARE</p>
  </div>

  <script>
    const envelope = document.getElementById('envelope');
    const scroll = document.getElementById('scroll');

    envelope.addEventListener('click', () => {
      envelope.classList.add('open');
      setTimeout(() => {
        scroll.classList.add('show');
      }, 1200);
    });
  </script>
</body>
</html>
