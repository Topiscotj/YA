<!Game Night Invitation Update>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Game Night Invitation</title>
  <style>
    body {
      background-color: #f8f4e3;
      font-family: 'Georgia', serif;
      text-align: center;
      padding: 50px;
    }

    .envelope {
      width: 200px;
      height: 150px;
      background: #c0392b;
      margin: 0 auto;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.6s ease;
    }

    .envelope.open {
      transform: rotateX(180deg);
    }

    .scroll {
      display: none;
      background: #fff8dc;
      border: 2px solid #c49b66;
      border-radius: 10px;
      padding: 20px;
      max-width: 400px;
      margin: 20px auto;
      text-align: left;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      transform: scaleY(0);
      transform-origin: top;
      transition: transform 0.6s ease;
    }

    .scroll.unrolled {
      display: block;
      transform: scaleY(1);
    }

    h1 {
      text-align: center;
    }

    p {
      margin: 5px 0;
    }

    strong {
      display: inline-block;
      width: 100px;
    }
  </style>
</head>
<body>
  <div class="envelope" id="envelope"></div>

  <div class="scroll" id="scroll">
    <h1>🎲 YOUNG ADULTS GAME NIGHT!!!</h1>
    <p><strong>DATE:</strong> October 31st</p>
    <p><strong>TIME:</strong> 6:00 PM</p>
    <p><strong>LOCATION:</strong> 1767 NE Regatta Dr</p>
    <p><strong>ATTIRE:</strong> Costume or Pajamas</p>
    <h1>♟️🧩 Bring your friends, your game face, and food to share!</h1>
  </div>

  <script>
    const envelope = document.getElementById('envelope');
    const scroll = document.getElementById('scroll');

    envelope.addEventListener('click', () => {
      envelope.classList.add('open');
      setTimeout(() => {
        scroll.classList.add('unrolled');
      }, 600);
    });
  </script>
</body>
</html>
