# GAME NIGHT INVITATION UPDATE
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Game Night Invitation</title>
  <style>
    body {
      background: linear-gradient(180deg, #fbe8c3, #f6d7a7, #f2b880);
      font-family: 'Georgia', serif;
      text-align: center;
      padding: 50px;
      overflow-x: hidden;
      color: #5a2d0c;
    }

    /* ENVELOPE BASE */
    .envelope {
      position: relative;
      width: 240px;
      height: 160px;
      margin: 0 auto;
      background: linear-gradient(135deg, #c54b30, #b0371d);
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
      background: linear-gradient(135deg, #e8683d, #d94a27);
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
      background: #fdf5e2;
      background-image: radial-gradient(circle at 10% 20%, rgba(255, 233, 190, 0.3) 0%, transparent 60%),
                        radial-gradient(circle at 90% 80%, rgba(255, 219, 158, 0.2) 0%, transparent 60%);
      border: 3px solid #d7a86e;
      border-radius: 12px;
      padding: 30px 20px;
      max-width: 420px;
      margin: 30px auto;
      box-shadow: 0 8px 16px rgba(0,0,0,0.25);
      transform: translateY(200px);
      opacity: 0;
      transition: transform 1s ease, opacity 1s ease;
      background-blend-mode: multiply;
    }

    /* When unrolled */
    .scroll.unrolled {
      transform: translateY(0);
      opacity: 1;
    }

    h1 {
      text-align: center;
      margin-bottom: 20px;
      color: #8b3a11;
      text-shadow: 1px 1px 2px rgba(139, 58, 17, 0.3);
    }

    p {
      margin: 10px 0;
      font-size: 18px;
      text-align: center;
      color: #5a2d0c;
    }

    strong {
      font-weight: bold;
      color: #a14b12;
    }

    /* Fun hover effect */
    .envelope:hover {
      box-shadow: 0 0 20px rgba(217, 72, 39, 0.7);
      transform: scale(1.02);
    }

    /* Animation hint text */
    .hint {
      margin-top: 15px;
      font-style: italic;
      color: #7a471c;
      font-size: 14px;
    }

    /* Decorative accents for fall vibe */
    .scroll::before {
      content: "🍁🍂🎃";
      display: block;
      font-size: 26px;
      text-align: center;
      margin-bottom: 10px;
    }

    .scroll::after {
      content: "🍂🍁";
      display: block;
      font-size: 22px;
      text-align: center;
      margin-top: 10px;
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
