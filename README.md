<!GAME NIGHT INVITATION UPDATE>
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
      overflow-x: hidden;
    }

    /* ENVELOPE BASE */
    .envelope {
      position: relative;
      width: 240px;
      height: 160px;
      margin: 0 auto;
      background: #c0392b;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
      perspective: 1000px;
      overflow: hidden;
      transition: transform 0.5s ease;
    }

    /* FLAP */
    .flap {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 80px;
      background: #e74c3c;
      clip-path: polygon(0 0, 50% 100%, 100% 0);
      transform-origin: top;
      transition: transform 0.6s ease;
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
      z-index: 2;
    }

    /* When envelope opens */
    .envelope.open .flap {
      transform: rotateX(180deg);
    }

    /* SCROLL INVITE (initially hidden inside envelope) */
    .scroll {
      position: relative;
      background: #fff8dc;
      border: 2px solid #c49b66;
      border-radius: 10px;
      padding: 25px;
      max-width: 420px;
      margin: 30px auto;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      transform: translateY(200px);
      opacity: 0;
      transition: transform 1s ease, opacity 1s ease;
    }

    /* When unrolled */
    .scroll.unrolled {
      transform: translateY(0);
      opacity: 1;
    }

    h1 {
      text-align: center;
      margin-bottom: 15px;
    }

    p {
      margin: 8px 0;
      font-size: 18px;
      text-align: center;
    }

    strong {
      font-weight: bold;
    }

    /* Fun hover effect */
    .envelope:hover {
      box-shadow: 0 0 15px rgba(192, 57, 43, 0.7);
    }

    /* Animation hint text */
    .hint {
      margin-top: 15px;
      font-style: italic;
      color: #666;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="envelope" id="envelope">
    <div class="flap"></div>
  </div>
  <div class="hint">(Click the envelope to open your invitation!)</div>

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
      }, 800);
    });
  </script>
</body>
</html>
