<!GAME NIGHT INVITATION UPDATE!>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Game Night Invite</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(180deg, #ffb347, #ffcc33, #d87c3e);
      font-family: "Comic Sans MS", "Fredoka One", cursive;
      overflow: hidden;
    }

    .envelope {
      position: relative;
      width: 180px;
      height: 120px;
      background: #b85c38;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      transition: transform 0.5s ease;
    }

    .envelope::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 0;
      height: 0;
      border-left: 90px solid transparent;
      border-right: 90px solid transparent;
      border-bottom: 60px solid #e07b39;
      transform-origin: top;
      transition: transform 0.6s ease;
    }

    .envelope.open::before {
      transform: rotateX(180deg);
    }

    .envelope::after {
      content: "CLICK HERE";
      position: absolute;
      top: 35%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: #fff;
      font-weight: bold;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
      transition: opacity 0.5s ease;
    }

    .envelope.open::after {
      opacity: 0;
    }

    .scroll {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%) scaleY(0);
      width: 250px;
      background: #fff8dc;
      border: 4px solid #c89b3c;
      border-radius: 10px;
      text-align: center;
      padding: 20px;
      font-size: 1rem;
      color: #5a3e1b;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      transition: transform 1s ease 0.5s;
      transform-origin: top;
    }

    .scroll.unrolled {
      transform: translateX(-50%) scaleY(1);
    }

    .scroll h1 {
      font-size: 1.2rem;
      color: #b85c38;
      margin-bottom: 10px;
    }

    .scroll p {
      margin: 6px 0;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }

    .envelope:hover {
      animation: float 1.5s infinite;
    }
  </style>
</head>
<body>
  <div class="envelope" id="envelope"></div>
  <div class="scroll" id="scroll">
    <h1>🎲 YOUNG ADULTS GAME NIGHT!!! </h1>
    <p><strong>Date:</strong> October 31st</p>
    <p><strong>Time:</strong> 6:00 PM</p>
    <p><strong>Location:</strong> 1767 NE Regatta Dr</p>
    <p><strong>Attire:</strong> Costume or Pajamas</p>
    <p><strong>Bring Your friends, your game face, and food to share!</p>

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
