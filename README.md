<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Para Bell 💌</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg1: #fff7fb;
      --bg2: #fff0f6;
      --rose: #ff6b9a;
      --dark: #111;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Quicksand', sans-serif;
      background: url('https://i.postimg.cc/MHP27H7M/5414458239900f09e14a221e78f038ae.jpg') no-repeat center center fixed, linear-gradient(135deg, var(--bg1), var(--bg2));
      background-size: cover;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 28px;
      overflow: hidden;
    }
    .stage {
      width: 100%;
      max-width: 980px;
      background: rgba(255, 255, 255, 0.3);
      border-radius: 24px;
      box-shadow: 0 10px 40px rgba(200, 150, 180, 0.15);
      padding: 28px;
      position: relative;
      overflow: hidden;
    }
    .overlay {
      position: absolute;
      inset: 0;
      background: rgba(255, 255, 255, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 5;
      transition: opacity 0.4s ease;
    }
    .panel {
      text-align: center;
    }
    .panel h1 {
      font-family: 'Pacifico', cursive;
      font-size: 44px;
      color: var(--rose);
    }
    .open-btn {
      margin-top: 18px;
      background: linear-gradient(180deg, var(--rose), #ff84a8);
      border: none;
      padding: 12px 20px;
      border-radius: 12px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 6px 18px rgba(255, 120, 160, 0.25);
      transition: transform 0.18s ease;
    }
    .open-btn:active {
      transform: translateY(2px);
    }
    .envelope-wrap {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 18px;
      position: relative;
      height: 280px;
    }
    .envelope {
      width: 320px;
      height: 280px;
      background: transparent;
      border-radius: 12px;
      position: relative;
      border: 2px solid rgba(200, 150, 170, 0.5);
      box-shadow: 0 10px 30px rgba(200, 150, 170, 0.15);
      cursor: pointer;
      user-select: none;
      z-index: 4;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 22px;
      overflow: hidden;
    }
    .seal {
      position: absolute;
      left: 50%;
      top: 46%;
      width: 68px;
      height: 68px;
      border-radius: 50%;
      background: radial-gradient(#ff7aa6, #ff5b86);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-weight: 800;
      box-shadow: 0 8px 20px rgba(255, 100, 150, 0.25);
      transform: translateX(-50%);
      user-select: none;
      z-index: 7;
      transition: opacity 0.5s ease;
    }
    .hide-envelope {
      opacity: 0;
      pointer-events: none;
    }
    .letter {
      position: relative;
      width: 100%;
      height: 100%;
      background: transparent;
      border-radius: 10px;
      padding: 16px;
      overflow-y: auto;
      user-select: text;
      font-size: 18px;
      line-height: 1.6;
      font-weight: 800; /* Letras mais fortes */
      color: #3c2130;
      text-shadow: 1px 1px 3px rgba(255, 255, 255, 0.8); /* Melhor contraste */
      white-space: pre-wrap;
      display: none;
      z-index: 8;
    }
    .letter h2 {
      font-family: 'Pacifico', cursive;
      margin-bottom: 12px;
      color: var(--rose);
      font-size: 28px;
      text-align: center;
      font-weight: 700;
      text-shadow: 1px 1px 3px rgba(255,255,255,0.8);
    }
    .closing {
      display: none;
      position: absolute;
      inset: 0;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.95);
      z-index: 9;
      user-select: none;
      flex-direction: column;
      text-align: center;
      padding: 24px;
    }
    .closing h3 {
      font-family: 'Pacifico', cursive;
      color: var(--rose);
      font-size: 34px;
      margin: 0 0 10px 0;
    }
    /* Floating hearts animation - formato mais fofo */
    .floating-heart {
      position: absolute;
      width: 30px; /* Aumenta o tamanho dos corações */
      height: 30px; /* Aumenta o tamanho dos corações */
      background: pink; /* Cor de fundo mais suave */
      transform: rotate(-45deg);
      border-radius: 50% 50% 0 0;
      animation: heartUp linear forwards;
      user-select: none;
    }
    .floating-heart::before,
    .floating-heart::after {
      content: "";
      position: absolute;
      width: 30px; /* Aumenta o tamanho dos corações */
      height: 30px; /* Aumenta o tamanho dos corações */
      background: pink; /* Cor de fundo mais suave */
      border-radius: 50%;
    }
    .floating-heart::before {
      top: -15px; /* Ajusta a posição do coração */
      left: 0;
    }
    .floating-heart::after {
      top: 0;
      left: 15px; /* Ajusta a posição do coração */
    }
    @keyframes heartUp {
      0% {
        opacity: 0;
        transform: translateY(0) rotate(-45deg) scale(0.9);
      }
      10% {
        opacity: 1;
      }
      100% {
        opacity: 0;
        transform: translateY(-420px) rotate(-45deg) scale(1.15);
      }
    }
  </style>
</head>
<body>
  <div class="stage" role="main" aria-labelledby="title">
    <div class="overlay" id="intro">
      <div class="panel">
        <h1 id="title">Oi, Bell 💖</h1>
        <p style="color:#7a5362; font-size: 20px; font-weight: 600;">Um presente feito com carinho pra aquecer seu dia.</p> <!-- Aumentada a visibilidade -->
        <button class="open-btn" id="openEnvelope">Abrir presente</button>
      </div>
    </div>

    <div class="envelope-wrap">
      <div class="envelope" id="envelope">
        <div class="seal" id="seal">❤️</div>
        <div class="letter" id="letter">
          <h2>Para Bell</h2>
          <div class="typed"></div>
        </div>
      </div>
    </div>

    <div class="closing" id="closing">
      <div>
        <h3>Te amo, Bell ❤️</h3>
        <p>Obrigado por existir — você é minha alegria.</p>
      </div>
    </div>
  </div>

  <script>
    const intro = document.getElementById('intro');
    const envelope = document.getElementById('envelope');
    const seal = document.getElementById('seal');
    const letter = document.getElementById('letter');
    const typed = letter.querySelector('.typed');
    const stage = document.querySelector('.stage');

    const message = `Bell, meu amor... 

Quando penso em vc, meu coração se aquece como o sol de fim de tarde, trazendo calma e alegria q só vc sabe provocar. Vc é o meu abraço q me conforta nos dias frios, meu sorriso quando tudo parece difícil, minha coragem para seguir em frente. É como se o mundo ficasse mais leve só por saber q vc existe.

Obrigado por cada detalhe seu, pelo seu jeitinho único, pelo sorriso q ilumina meus dias, pelo seu coração tão generoso e lindo q eu tenho a sorte de conhecer. Vc é poesia viva, é paz em forma de gente, é o milagre cotidiano q transforma o simples em extraordinário. VC É O AMOR DA MINHA VIDA. 🥹🫶

Eu quero cuidar de vc em cada momento, fazer vc sorrir msm nas tempestades, dividir sonhos, medos, alegrias e planos. Quero ser seu abrigo quando o mundo pesar, ser silêncio quando vc precisar respirar, ser presença quando tudo parecer ausente. Construir um mundo só nosso, onde só exista amor e compreensão, onde cada gesto seja um laço, cada palavra um carinho.

Te amo mais do q palavras conseguem expressar, mais do q o tempo pode medir, mais do q o infinito possa contar. Meu amor por você é como o universo... Belo, imenso e admirável. Esse amor é tudo q pulsa em mim.💗

Te amo hj, amanhã e sempre. 🥹💖
Com todo meu amor  
— Gidelson`;

    function popHearts(count = 12) { // Mantém a quantidade de corações
      for (let i = 0; i < count; i++) {
        const h = document.createElement('div');
        h.className = 'floating-heart';
        const left = 20 + Math.random() * 60;
        h.style.left = left + '%';
        h.style.bottom = '8%';
        const size = 16 + Math.random() * 30;
        h.style.width = h.style.height = size + 'px';
        h.style.animationDuration = (3 + Math.random() * 2) + 's';
        stage.appendChild(h);
        setTimeout(() => h.remove(), 4500);
      }
    }

    let heartInterval;

    function startHearts() {
      heartInterval = setInterval(() => {
        popHearts(3); // Agora gera 3 corações por vez
      }, 400);
    }

    function typeMessage(text, cb) {
      typed.innerHTML = '';
      let i = 0;
      const speed = 30;
      const timer = setInterval(() => {
        typed.innerHTML += text.charAt(i);
        i++;
        if (i >= text.length) {
          clearInterval(timer);
          if (cb) cb();
        }
      }, speed);
    }

    function openCard() {
      intro.style.opacity = 0;
      setTimeout(() => (intro.style.display = 'none'), 400);
      letter.style.display = 'block'; // Mostra a carta
      seal.classList.add('hide-envelope'); // Remove o selo
      typed.innerHTML = '';
      startHearts();
      setTimeout(() => {
        typeMessage(message);
      }, 200);
    }

    document.getElementById('openEnvelope').addEventListener('click', openCard);
    envelope.addEventListener('click', () => {
      if (intro.style.display !== 'none') {
        openCard();
      }
    });
  </script>
</body>
</html>
