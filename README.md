<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para Você ♡</title>
<link rel="icon" type="image/png" href="/favicon.png">
<link rel="apple-touch-icon" href="/favicon.png">

<!-- ═══════ PERFORMANCE: Preconnect + DNS Prefetch ═══════ -->
<link rel="preconnect" href="https://www.gstatic.com">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="preconnect" href="https://res.cloudinary.com">
<link rel="dns-prefetch" href="https://api.cloudinary.com">
<link rel="dns-prefetch" href="https://firebase.googleapis.com">

<!-- ═══════ FONTS: Preload críticas ═══════ -->
<link rel="preload" as="font" href="https://fonts.gstatic.com/s/playfairdisplay/v30/0fl-8WDjicf-0-0-75eV9UlC5-wjYGAGIFZeJcLW.woff2" crossorigin>
<link rel="preload" as="font" href="https://fonts.gstatic.com/s/dancingscript/v17/If2cXTr6YS-zF4S-G5UHW63e6N6nqUbL.woff2" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;1,400&family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Dancing+Script:wght@400;600;700&family=Crimson+Text:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">

<script>
/* ─── CONFIGURAÇÕES ──────────────────────────────────────── */
const FIREBASE_CONFIG = {
  apiKey:            "AIzaSyDPVgHi6MDNbkQBi4ksnCr8SnHLlvoySkA",
  authDomain:        "para-vc-meu-amor.firebaseapp.com",
  projectId:         "para-vc-meu-amor", 
  storageBucket:     "para-vc-meu-amor.firebasestorage.app",
  messagingSenderId: "419572804720",
  appId:             "1:419572804720:web:92c7ccc1d3fd96564d58b5",
  measurementId:     "G-8KRHQBJW53"
};
const UNLOCK_DATE = new Date("2026-06-12T00:00:00-03:00");
const CLOUDINARY_CLOUD = "nosso-lugar";       
const CLOUDINARY_PRESET = "memories_upload"; 

function throttle(fn, delay = 300) {
  let lastCall = 0;
  return function(...args) {
    const now = Date.now(); 
    if (now - lastCall >= delay) {
      fn(...args);
      lastCall = now;
    }
  };
}
/* ─────────────────────────────────────────────────────────── */
</script>

<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
:root {
  --bg: #07071a; --card: #0f0f2a; --acc: #d4a843; --txt: #e8e0d0;
  --mt: #6868a0; --br: #1e1e40; --fn: 'Playfair Display', serif;
  --script: 'Dancing Script', cursive;
}
html { scroll-behavior: smooth; }
body {
  background: 
    /* Via Láctea - Centro brilhante */
    radial-gradient(ellipse 800px 400px at 50% 30%, rgba(138, 95, 180, 0.25) 0%, rgba(138, 95, 180, 0.08) 25%, transparent 70%),
    
    /* Nuvem de poeira roxa à esquerda */
    radial-gradient(ellipse 600px 500px at 20% 40%, rgba(180, 82, 220, 0.2) 0%, rgba(180, 82, 220, 0.05) 30%, transparent 60%),
    
    /* Nuvem azul à direita */
    radial-gradient(ellipse 700px 450px at 75% 50%, rgba(100, 150, 220, 0.18) 0%, rgba(100, 150, 220, 0.04) 35%, transparent 65%),
    
    /* Nebulosa vermelha inferior */
    radial-gradient(ellipse 500px 300px at 60% 75%, rgba(200, 100, 150, 0.15) 0%, rgba(200, 100, 150, 0.03) 40%, transparent 70%),
    
    /* Nebulosa azul superior esquerda */
    radial-gradient(ellipse 400px 350px at 15% 20%, rgba(80, 120, 200, 0.12) 0%, rgba(80, 120, 200, 0.02) 45%, transparent 75%),
    
    /* Gradiente de fundo linear - céu profundo */
    linear-gradient(180deg, 
      rgba(7, 7, 26, 1) 0%,
      rgba(12, 8, 40, 0.95) 20%,
      rgba(15, 10, 45, 0.9) 40%,
      rgba(18, 12, 50, 0.92) 60%,
      rgba(10, 5, 35, 0.95) 100%
    ),
    
    /* Cor base da galáxia */
    #05050f;
    
  background-attachment: fixed;
  background-size: 100% 100%, 100% 100%, 100% 100%, 100% 100%, 100% 100%, 100% 100%, 100% 100%;
  color: var(--txt);
  font-family: var(--fn);
  min-height: 100vh;
  overflow-x: hidden;
}

#particles { position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden; }
.pt { position: absolute; bottom: -20px; animation: floatUp linear infinite; will-change: transform; transform: translateZ(0); }

@keyframes floatUp {
  0%   { transform: translateY(0) rotate(-10deg) scale(.5); opacity: 0; }
  8%   { opacity: .7; }
  92%  { opacity: .3; }
  100% { transform: translateY(-105vh) rotate(10deg) scale(1); opacity: 0; }
}

@keyframes fadeIn  { from { opacity:0; transform:translateY(14px); } to { opacity:1; transform:translateY(0); } }
@keyframes shimmer { 0%,100%{opacity:.35} 50%{opacity:1} }
@keyframes pulse   { 0%,100%{transform:scale(1)} 50%{transform:scale(1.08)} }
@keyframes spin    { to { transform: rotate(360deg); } }
@keyframes glow    { 0%,100%{box-shadow:0 0 20px #d4a84340} 50%{box-shadow:0 0 50px #d4a84390,0 0 90px #d4a84330} }
@keyframes envelopeOpen { 0%{transform:rotateX(0deg)} 100%{transform:rotateX(-160deg)} }
@keyframes letterRise   { 0%{transform:translateY(0);opacity:0} 100%{transform:translateY(-55%);opacity:1} }
@keyframes wrongShake   { 0%,100%{transform:translateX(0)} 20%{transform:translateX(-8px)} 40%{transform:translateX(8px)} 60%{transform:translateX(-5px)} 80%{transform:translateX(5px)} }
@keyframes unlockBurst  { 0%{transform:scale(1);opacity:1} 100%{transform:scale(30);opacity:0} }

.screen {
  position: fixed; 
  inset: 0; 
  z-index: 100; 
  display: flex;
  align-items: center; 
  justify-content: center;
  background: rgba(5, 3, 15, 0.9); /* Escurece o fundo para destacar a carta no meio */
  transition: opacity .8s, visibility .8s; 
}
.screen.hidden { opacity:0; visibility:hidden; pointer-events:none; }

#screen-countdown {
background: transparent;
  flex-direction: column; text-align: center; padding: 2rem;
}
.countdown-title { font-size: clamp(1.6rem,4vw,2.8rem); color: var(--acc); font-weight:400; }
.countdown-ornament { font-family: var(--script); color: var(--acc); font-size: 1.1rem;
  letter-spacing:.2em; margin-bottom:2.5rem; animation:shimmer 3s infinite; }

.stars { position: fixed; inset: 0; pointer-events: none; z-index: 0; }
.star  { 
  position: absolute; 
  background: white; 
  border-radius: 50%; 
  animation: shimmer linear infinite;
  box-shadow: 0 0 4px 1px rgba(255, 255, 255, 0.4);
}

#screen-envelope {
  background: transparent;
  flex-direction: column; text-align: center; padding: 2rem;
}
.envelope-hint { color:var(--mt); font-size:.75rem; font-style:italic;
  margin-bottom:2.5rem; animation:shimmer 2.5s infinite; }
.envelope-wrapper { perspective:800px; margin:0 auto; width:min(340px,85vw);
  cursor:pointer; position:relative; }
.envelope { width:100%; position:relative; transform-style:preserve-3d; user-select:none; }
.env-body { width:100%; padding-bottom:63%; background:linear-gradient(145deg,#1a0d2e,#0e0720);
  border-radius:4px 4px 10px 10px; position:relative; overflow:hidden;
  border:1px solid #3a1858; box-shadow:0 20px 60px rgba(0,0,0,.6),0 0 0 1px #ffffff08 inset; }
.env-body::before { content:''; position:absolute; inset:0;
  background:linear-gradient(135deg,transparent 49.5%,#ffffff05 50%,transparent 50.5%),
             linear-gradient(225deg,transparent 49.5%,#ffffff05 50%,transparent 50.5%); }
.env-left-flap,.env-right-flap { position:absolute; bottom:0; }
.env-left-flap  { border-right:170px solid transparent; border-bottom:106px solid #13092a; left:0; filter:brightness(.8); }
.env-right-flap { border-left:170px solid transparent;  border-bottom:106px solid #180c35; right:0; filter:brightness(.9); }
.env-top-flap { position:absolute; top:0; left:0; right:0; height:0;
  border-left:170px solid transparent; border-right:170px solid transparent;
  border-top:106px solid #1e1040; transform-origin:top center; z-index:5; }
.envelope-wrapper.opening .env-top-flap { animation:envelopeOpen .7s ease forwards; }
.seal { 
  position: absolute; 
  top: 50%; 
  left: 50%; 
  width: 60px; 
  height: 60px; 
  border-radius: 50%;
  background: radial-gradient(circle at 35% 35%,#c0392b,#7b0000);
  display: flex; 
  align-items: center; 
  justify-content: center; 
  font-size: 1.6rem;
  z-index: 10; 
  cursor: pointer;
  box-shadow: 0 4px 20px rgba(192,57,43,.5), 0 0 0 3px #8b0000, 0 0 0 5px #c0392b40;
  animation: glow 2.5s ease-in-out infinite; 
  transition: transform .2s, opacity .2s; 
  will-change: transform; 
  
  /* 🌟 CORREÇÃO DO ALINHAMENTO CENTRAL: */
  transform: translate(-50%, -50%) !important; 
}

.seal:hover { 
  /* 🌟 GARANTE O CENTRO ATÉ NO EFEITO PASSAR O MOUSE: */
  transform: translate(-50%, -50%) scale(1.08) !important; 
}

.envelope-wrapper.opening .seal { 
  /* 🌟 FAZ SUMIR SUAVEMENTE SEM QUEBRAR O LAYOUT: */
  opacity: 0;
  pointer-events: none;
}

.letter-container { position:absolute; top:50%; left:8%; right:8%;
  transform:translateY(-50%); z-index:3; pointer-events:none; }
.envelope-wrapper.rising .letter-container {
  animation:letterRise .8s cubic-bezier(.2,0,.3,1) .5s forwards; pointer-events:all; }
.letter-paper { background:linear-gradient(160deg,#fdf8ee,#f5ecdb); border-radius:3px;
  padding:1.8rem 1.6rem 2rem; box-shadow:0 -10px 40px rgba(0,0,0,.4);
  position:relative; overflow:hidden; }
.letter-paper::before { content:''; position:absolute; inset:0;
  background:repeating-linear-gradient(transparent,transparent 27px,#d4a84320 28px); pointer-events:none; }
.letter-greeting { font-family:var(--script); color:#3a1a0a; font-size:1.4rem; margin-bottom:.6rem; }
.letter-body     { font-family:'Crimson Text',serif; color:#2a1505; font-size:.92rem;
  line-height:1.85; font-style:italic; margin-bottom:1.2rem; }
.letter-question { font-family:var(--script); color:#7b2e00; font-size:1.1rem;
  margin-bottom:1rem; font-weight:600; }
.letter-input { width:100%; border:none; border-bottom:2px solid #c8a46090;
  background:transparent; font-family:var(--script); font-size:1rem;
  color:#2a1505; padding:.4rem .2rem; outline:none; transition:border-color .3s; }
.letter-input:focus { border-color:#c0392b; }
.letter-input.wrong { animation:wrongShake .4s ease; border-color:#c0392b; }
.letter-submit { margin-top:1.2rem; width:100%;
  background:linear-gradient(135deg,#7b2e00,#b04020); color:#fdf8ee;
  border:none; padding:.65rem; border-radius:4px; font-family:var(--script);
  font-size:1rem; font-weight:600; letter-spacing:.05em;
  transition:opacity .2s,transform .2s; box-shadow:0 4px 15px rgba(120,40,0,.4); }
.letter-submit:hover { opacity:.9; transform:translateY(-1px); }
.letter-err  { color:#9b2e2e; font-size:.72rem; margin-top:.4rem;
  font-family:'Crimson Text',serif; font-style:italic; min-height:1rem; }
.letter-sign { font-family:var(--script); color:#3a1a0a; font-size:1rem;
  margin-top:1rem; text-align:right; }

.unlock-burst { position:fixed; inset:0; background:var(--acc);
  z-index:500; pointer-events:none; opacity:0; }
.unlock-burst.go { animation:unlockBurst .5s ease forwards; }

#screen-site { position:relative; z-index:1; background:var(--bg);
  flex-direction:column; align-items:stretch; justify-content:flex-start; min-height:100vh; }
header { text-align:center; padding:3rem 1rem 1.8rem; position:relative; z-index:1; }
.deco { letter-spacing:.3em; font-size:.68rem; animation:shimmer 3s infinite; }
h1.main-title { font-size:clamp(2.2rem,6vw,4rem); font-weight:400; letter-spacing:.04em;
  cursor:default; transition:color .5s; will-change: color; }
nav#adminNav { border-top:1px solid var(--br); border-bottom:1px solid var(--br);
  padding:.5rem; display:none; gap:.5rem; justify-content:center; flex-wrap:wrap;
  position:sticky; top:0; z-index:10; backdrop-filter:blur(12px);
  background:var(--card-op,#0f0f2aee); }
.btn-nav { background:transparent; border:1px solid var(--br); color:var(--mt);
  padding:.28rem .95rem; border-radius:6px; font-size:.78rem; transition:all .2s; }
.btn-nav.active,.btn-nav:hover { background:var(--acc); color:var(--bg); border-color:var(--acc); }
.btn-nav.active { font-weight:700; }
main#main { width:100%; padding:0; position:relative; z-index:1; }

/* ── POLAROID BOARD ── */
.board { position:relative; width:100%; overflow-x:hidden; overflow-y:visible; }
@keyframes polaroidIn {
  from { opacity:0; transform:var(--base-transform) scale(.7); }
  to   { opacity:1; transform:var(--base-transform) scale(1); }
}
.polaroid {
  position:absolute;
  width: 250px;
  height: auto;
  background:#fdf8ee;
  padding:10px 10px 40px;
  box-shadow: 3px 3px 12px rgba(0,0,0,.45), 0 0 0 1px rgba(0,0,0,.08);
  cursor:pointer;
  transform: var(--base-transform);
  animation: polaroidIn .6s cubic-bezier(.2,0,.3,1) var(--delay) both;
  transition: transform .25s cubic-bezier(.2,0,.3,1), box-shadow .25s, z-index 0s;
  z-index: 2;
  will-change: transform;
  transform-origin: center;
}
.polaroid:hover {
  transform: var(--hover-transform) scale(1.08) !important;
  box-shadow: 8px 8px 30px rgba(0,0,0,.6), 0 0 0 1px rgba(0,0,0,.1);
  z-index: 50 !important;
}
.polaroid-photo { width:100%; aspect-ratio:1/1; object-fit:cover; display:block;
  background:#ddd; border-radius: 2px; }
.polaroid-photo.loading { background: linear-gradient(90deg, #e0e0e0 25%, #f0f0f0 50%, #e0e0e0 75%); background-size: 200% 100%; animation: loading 1.5s infinite; }
@keyframes loading { 0% { background-position: 200% 0; } 100% { background-position: -200% 0; } }
.polaroid-photo-empty { width:100%; aspect-ratio:1/1; background:#e8e0d0;
  display:flex; align-items:center; justify-content:center;
  font-size:2rem; color:#c8b89080; }
.polaroid-caption {
  position:absolute; bottom:0; left:0; right:0; height:40px;
  display:flex; flex-direction:column; align-items:center; justify-content:center;
  padding:0 6px;
}
.polaroid-title {
  font-family:'Dancing Script',fantasy; font-size:1.1rem;
  color:#2a1505; text-align:center; white-space:nowrap;
  overflow:hidden; text-overflow:ellipsis; max-width:100%;
  line-height:1.2;
}
.polaroid-date {
  font-family:'Crimson Text',serif; font-size:.8rem;
  color:#7a5a3a; opacity:.7; margin-top:1px;
}
.polaroid-del {
  position:absolute; top:4px; right:4px;
  background:rgba(180,30,30,.75); color:#fff;
  border:none; border-radius:50%; width:18px; height:18px;
  font-size:.6rem; line-height:18px; text-align:center;
  padding:0; opacity:0; transition:opacity .2s;
}
.polaroid-edit {
  position:absolute; top:4px; left:4px;
  background:rgba(40,40,120,.75); color:#fff;
  border:none; border-radius:50%; width:18px; height:18px;
  font-size:.62rem; line-height:18px; text-align:center;
  padding:0; opacity:0; transition:opacity .2s;
}
.polaroid:hover .polaroid-del,
.polaroid:hover .polaroid-edit { opacity:1; }

/* ── MODAL DE EDIÇÃO ── */
.edit-modal { background:var(--card); border:1px solid var(--br); border-radius:16px;
  max-width:500px; width:100%; max-height:90vh; overflow-y:auto;
  padding:1.8rem; animation:fadeIn .2s ease; position:relative; }
.edit-modal h3 { font-family:var(--fn); color:var(--acc); font-weight:400;
  font-size:1.4rem; margin:0 0 1.4rem; text-align:center; }
.edit-saving { display:inline-block; width:14px; height:14px;
  border:2px solid var(--bg); border-top-color:transparent;
  border-radius:50%; animation:spin .7s linear infinite; vertical-align:middle; }
.empty { text-align:center; padding:5rem 1rem; animation:fadeIn .5s ease; }
.section { max-width:560px; margin:0 auto; animation:fadeIn .35s ease; }
.form-label { display:block; font-size:.68rem; letter-spacing:.12em; text-transform:uppercase;
  margin-bottom:.35rem; color:var(--mt); }
.form-input { background:var(--bg); border:1px solid var(--br); color:var(--txt);
  padding:.62rem .95rem; border-radius:8px; width:100%; font-size:.9rem;
  outline:none; transition:border-color .2s; }
.form-input:focus { border-color:var(--acc); }
.form-group { margin-bottom:1.2rem; }
.save-btn { background:var(--acc); color:var(--bg); border:none; padding:.82rem;
  border-radius:9px; font-size:.97rem; width:100%; font-weight:700;
  letter-spacing:.05em; transition:background .4s; }
.theme-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(175px,1fr)); gap:1rem; }
.theme-card { border-radius:14px; padding:1.4rem 1rem; text-align:center;
  transition:all .25s; border:2px solid transparent; }
.modal-overlay { position:fixed; inset:0; background:rgba(0,0,0,.9);
  display:flex; align-items:center; justify-content:center; z-index:200; padding:1rem; }
footer { text-align:center; padding:2rem 1rem 2.5rem; position:relative; z-index:1; }
.toast { position:fixed; bottom:2rem; left:50%; transform:translateX(-50%);
  background:var(--acc); color:var(--bg); padding:.7rem 1.8rem;
  border-radius:8px; font-size:.88rem; font-weight:700; z-index:300; animation:fadeIn .3s ease; }

/* ═══════ RESPONSIVE ═══════ */
@media (max-width: 768px) {
  .polaroid { width: 200px !important; }
  header { padding: 2rem 1rem 1rem; }
  h1.main-title { font-size: clamp(1.6rem, 5vw, 2.8rem); }
  .theme-grid { grid-template-columns: repeat(auto-fill, minmax(120px, 1fr)); }
}

@media (max-width: 480px) {
  .polaroid { width: 160px !important; }
  .polaroid-title { font-size: 0.9rem; }
  nav#adminNav { flex-direction: column; gap: .3rem; }
  .btn-nav { width: 100%; }
}
</style>
</head>
<body>

<div id="particles"></div>
<div class="stars" id="stars"></div>

<!-- TELA 1: ABERTURA -->
<div class="screen" id="screen-countdown">
  <div style="position:relative;z-index:1;width:100%;max-width:640px;padding:2rem;text-align:center">
    <div style="font-size:5rem;margin-bottom:2.5rem;animation:pulse 2.5s infinite">💕</div>
    <h2 class="countdown-title" style="font-size:4rem;margin-bottom:1.5rem">Para Você</h2>
    <p style="color:var(--mt);font-style:italic;font-size:1.05rem;margin-bottom:3.5rem;line-height:2">
      Um jardim preparado<br>
      <span style="color:var(--acc);font-family:var(--script);font-size:1.2rem">com todo o meu amor</span>
    </p>
    <button onclick="goToEnvelope()" style="
      background:linear-gradient(135deg,var(--acc),#b8860b);color:var(--bg);
      border:none;padding:1rem 2.5rem;border-radius:12px;font-size:1.4rem;
      font-weight:700;letter-spacing:0.12em;cursor:pointer;transition:all 0.3s ease;
      font-family:var(--script);box-shadow:0 10px 30px rgba(212,168,67,0.4);text-transform:uppercase;"
      onmouseover="this.style.transform='scale(1.05)'"
      onmouseout="this.style.transform='scale(1)'">
      ✧ Abrir ✧
    </button>
    <div style="margin-top:3.5rem;font-size:1.3rem;animation:shimmer 2s infinite;color:var(--acc);opacity:0.7">♡ &nbsp;♡ &nbsp;♡</div>
  </div>
</div>

<!-- TELA 2: ENVELOPE -->
<div class="screen hidden" id="screen-envelope">
  <div style="position:relative;z-index:1;width:100%;max-width:420px;padding:2rem;text-align:center">
    <p class="countdown-ornament" style="margin-bottom:1rem">✦ &nbsp; chegou o momento &nbsp; ✦</p>
    <p class="envelope-hint">Você recebeu uma carta especial. Clique no selo para abrir ✉</p>
    <div class="envelope-wrapper" id="envWrapper">
      <div class="envelope">
        <div class="env-body">
          <div class="env-left-flap"></div>
          <div class="env-right-flap"></div>
        </div>
        <div class="env-top-flap" id="envFlap"></div>
        <div class="letter-container" id="letterContainer" style="display:none">
          <div class="letter-paper">
            <p class="letter-greeting">Meu amor,</p>
            <p class="letter-body">
              Este lugar foi criado especialmente para você — um jardim
              guardado de memórias nossas, poemas e palavras que nunca
              caberiam apenas na minha mente.<br><br>
              Para entrar, preciso ter certeza que é você. ♡
            </p>
            <p class="letter-question">Qual foi o dia que oficializamos nosso namoro?</p>
            <input class="letter-input" id="secretInput" type="text" placeholder="escreva aqui...">
            <p class="letter-err" id="secretErr"></p>
            <button class="letter-submit" id="secretBtn">Abrir o jardim ♡</button>
            <p class="letter-sign">Com todo o meu amor</p>
          </div>
        </div>
        <div class="seal" id="envSeal">♥</div>
      </div>
    </div>
  </div>
</div>

<!-- TELA 3: SITE -->
<div class="screen hidden" id="screen-site">
  <div style="width:100%;min-height:100vh;display:flex;flex-direction:column">
    <header>
      <div class="deco" id="deco1" style="color:var(--mt)">❤ ─────────── ❤ ─────────── ❤</div>
      <h1 class="main-title" id="mainTitle" style="color:var(--acc)">Para Maylle 🌻</h1>
      <p style="font-style:italic;font-size:.85rem;margin-top:.5rem;color:var(--mt)">Nosso jardim de memórias e palavras</p>
      <div class="deco" style="margin-top:1rem;color:var(--mt)">❤ ─────────── ❤ ─────────── ❤</div>
    </header>
    <nav id="adminNav">
      <button class="btn-nav active" onclick="setView('gallery')">Galeria</button>
      <button class="btn-nav" onclick="setView('admin')">+ Nova Memória</button>
      <button class="btn-nav" onclick="setView('themes')">Temas</button>
      <button style="background:none;border:none;color:var(--mt);font-size:.72rem;padding-left:.8rem;cursor:pointer" onclick="logout()">sair</button>
    </nav>
    <main id="main" style="flex:1"></main>
    <footer>
      <div style="font-size:1.2rem;margin-bottom:.35rem;animation:pulse 2.5s infinite;color:var(--acc)">♡</div>
      <p id="footTxt" style="font-size:.7rem;font-style:italic;color:var(--mt)">feito com amor, para você</p>
      <p id="footHint" style="font-size:.58rem;margin-top:1.2rem;opacity:.35;color:var(--mt)">Maylle vc é maravilhosa</p>
    </footer>
  </div>
</div>

<div class="unlock-burst" id="unlockBurst"></div>

<!-- ═══════ Firebase (Carregado sob demanda - LAZY LOAD) ═══════ -->
<script id="firebaseLoader">
let firebaseInitialized = false;
let db = null, auth = null;

function loadFirebaseSDK() {
  return new Promise((resolve, reject) => {
    if(window.firebase) { resolve(); return; }
    const scripts = [
      'https://www.gstatic.com/firebasejs/10.12.0/firebase-app-compat.js',
      'https://www.gstatic.com/firebasejs/10.12.0/firebase-firestore-compat.js',
      'https://www.gstatic.com/firebasejs/10.12.0/firebase-auth-compat.js'
    ];
    let loaded = 0;
    scripts.forEach((src) => {
      const s = document.createElement('script');
      s.src = src;
      s.async = false;
      s.onload = () => { if (++loaded === scripts.length) resolve(); };
      s.onerror = () => reject(new Error('Falha ao carregar Firebase SDK: ' + src));
      document.head.appendChild(s);
    });
  });
}
</script>

<script>
/* ══════ THEMES ══════ */
const THEMES = {
  "Noite Estrelada":    {bg:"#07071a",card:"#0f0f2a",acc:"#c084fc",txt:"#e8e0f0",mt:"#8b7aaa",br:"#2a1a4a",fn:"'Playfair Display',serif",em:"✨"},
  "Jardim de Rosas":    {bg:"#190810",card:"#26101c",acc:"#e896b8",txt:"#f8e8f0",mt:"#a06080",br:"#3a1828",fn:"'Cormorant Garamond',serif",em:"🌹"},
  "Crepúsculo":         {bg:"#0c0718",card:"#180e28",acc:"#bb86f5",txt:"#f0e8f8",mt:"#7850a8",br:"#28155a",fn:"'Playfair Display',serif",em:"🌙"},
  "Floresta Encantada": {bg:"#050f08",card:"#0b1e10",acc:"#6dbe78",txt:"#dff0e0",mt:"#4a7858",br:"#162a1a",fn:"'Cormorant Garamond',serif",em:"🌿"},
  "Oceano":             {bg:"#040d14",card:"#0a1a26",acc:"#4fc3e0",txt:"#e0f4f8",mt:"#3a7090",br:"#0e2a3a",fn:"'Playfair Display',serif",em:"🌊"},
  "Deserto Dourado":    {bg:"#130c04",card:"#221508",acc:"#f0a830",txt:"#f5ead0",mt:"#9a7040",br:"#3a2008",fn:"'Crimson Text',serif",em:"🌅"},
};

/* ══════ STATE ══════ */
let tn="Noite Estrelada", mems=[], view="gallery", isAdmin=false;
let clicks=0, form={title:"",date:"",poem:"",photo:null,photoFile:null}, saving=false;

/* ══════ STARS ══════ */
function buildStars(){
  const s=document.getElementById("stars"); s.innerHTML="";
  
  // Aumentar número de estrelas para efeito Via Láctea
  const starCount = 250;
  
  for(let i=0;i<starCount;i++){
    const st=document.createElement("div"); 
    st.className="star";
    
    const sz = 0.3 + (Math.random() * 2.5); // Maior variação de tamanho
    const opacity = 0.15 + (Math.random() * 0.85); // Mais variação de brilho
    const duration = 3 + (Math.random() * 6);
    const delay = Math.random() * 5;
    
    // Cores realistas de estrelas (branco, azul, amarelado, avermelhado)
    const colors = ['#ffffff', '#e8e0d0', '#b3d9ff', '#ffd9b3', '#ffe0d0'];
    const color = colors[Math.floor(Math.random() * colors.length)];
    
    st.style.cssText=`
      width:${sz}px;
      height:${sz}px;
      top:${Math.random()*100}%;
      left:${Math.random()*100}%;
      opacity:${opacity};
      animation-duration:${duration}s;
      animation-delay:${delay}s;
      background: ${color};
      box-shadow: 0 0 ${sz * 1.5}px 0.5px ${color}80;
    `;
    
    s.appendChild(st);
  }
}
buildStars();

/* ══════ PARTICLES ══════ */
function buildParticles(acc){
  const p=document.getElementById("particles"); p.innerHTML="";
  for(let i=0;i<18;i++){
    const h=document.createElement("div"); h.className="pt"; h.textContent="♡";
    h.style.left=`${4+(i*5.8)%92}%`;
    h.style.fontSize=`${9+(i*3)%14}px`;
    h.style.opacity=`${0.06+(i%5)*0.04}`;
    h.style.color=acc;
    h.style.animationDuration=`${10+(i*1.9)%10}s`;
    h.style.animationDelay=`${(i*1.3)%9}s`;
    p.appendChild(h);
  }
}

/* ══════ SCREEN CONTROL ══════ */
function showScreen(id){
  ["screen-countdown","screen-envelope","screen-site"].forEach(s=>{
    document.getElementById(s).classList.toggle("hidden", s!==id);
  });
}

/* ══════ ENVELOPE ══════ */
function goToEnvelope(){
  showScreen("screen-envelope");
  buildParticles("#d4a843");
  setupEnvelope();
}

function setupEnvelope(){
  let opened = false;

  function openEnvelope(e){
    if(e) e.stopPropagation();
    if(opened) return;
    opened = true;

    const w = document.getElementById("envWrapper");
    w.classList.add("opening");

    setTimeout(()=>{
      const lc = document.getElementById("letterContainer");
      lc.style.display = "block";
      w.classList.add("rising");
    }, 600);
  }
  
  const seal = document.getElementById("envSeal");
  const newSeal = seal.cloneNode(true);
  seal.parentNode.replaceChild(newSeal, seal);

  document.getElementById("envSeal").addEventListener("click", openEnvelope);
  document.getElementById("secretBtn").addEventListener("click", checkAnswer);
  document.getElementById("secretInput").addEventListener("keydown", e=>{
    if(e.key==="Enter") checkAnswer();
  });
}
 
function normalizeAnswer(s){
  return s.toLowerCase()
    .normalize("NFD").replace(/[\u0300-\u036f]/g,"")
    .replace(/[^a-z0-9\s]/g,"").trim();
}

function checkAnswer(){
  const input = document.getElementById("secretInput");
  const err   = document.getElementById("secretErr");
  const val   = normalizeAnswer(input.value);
  const has28  = val.includes("28");
  const hasSep = val.includes("setembro") || val.includes("09");
  const has25  = val.includes("2025") || !val.match(/\d{4}/);

  if(has28 && hasSep && has25){
    unlockSite();
  } else {
    input.classList.add("wrong");
    err.textContent = "Hmm... tente novamente, meu amor 💔";
    setTimeout(()=> input.classList.remove("wrong"), 500);
  }
}

 
function unlockSite(){
  localStorage.setItem("lv_unlocked","1");
  const burst = document.getElementById("unlockBurst");
  burst.classList.add("go");
  setTimeout(()=>{
    showSite();
    burst.style.display = "none";
  },);
}

/* ══════ SITE PRINCIPAL ══════ */
async function showSite(){
  showScreen("screen-site");
  applyTheme();
  render();
  initFirebaseOnDemand();

  const title = document.getElementById("mainTitle");
  title.addEventListener("click", ()=>{
    clicks++;
    if(clicks >= 5){ clicks=0; showAdminLogin(); }
  });
}

/* ══════ BOOT ══════ */
(function boot(){
  if(localStorage.getItem("lv_unlocked")==="1"){
    showSite();
  } else {
    showScreen("screen-countdown");
    buildParticles("#d4a843");
  }
})();


/* ══════ THEME ══════ */
function th(){ return THEMES[tn]; }
function applyTheme(){
  const t = th();
  const r = document.documentElement.style;
  r.setProperty("--bg",   t.bg);
  r.setProperty("--card", t.card);
  r.setProperty("--acc",  t.acc);
  r.setProperty("--txt",  t.txt);
  r.setProperty("--mt",   t.mt);
  r.setProperty("--br",   t.br);
  r.setProperty("--card-op", t.card + "ee");

  document.getElementById("screen-site").style.background = "transparent";
  document.getElementById("mainTitle").style.color = t.acc;
  document.getElementById("mainTitle").style.textShadow = `0 0 60px ${t.acc}50`;
  document.getElementById("footTxt").style.color = t.mt;
  document.getElementById("footHint").style.color = t.mt;
  document.getElementById("deco1").style.color = t.mt;
  buildParticles(t.acc);
}

/* ══════ FIREBASE (LAZY INIT) ══════ */
async function initFirebaseOnDemand(){
  if(firebaseInitialized) return;
  firebaseInitialized = true;

  try {
    await loadFirebaseSDK();
    
  try {
  firebase.initializeApp(FIREBASE_CONFIG);
} catch(e) {
  console.error('Firebase init failed:', e);
  showToast("Erro ao conectar ao banco de dados");
}

    try { auth = firebase.auth(); } catch(e){ console.warn("Auth erro:",e); }
    try { db = firebase.firestore(); } catch(e){ console.warn("Firestore erro:",e); }

    if(!auth || !db){ showToast("Firebase não disponível."); return; }

    db.collection("config").doc("theme").get()
      .then(d=>{ if(d.exists){ tn=d.data().name||tn; applyTheme(); } })
      .catch(()=>{});

    const renderThrottled = throttle(() => render(), 500);
    db.collection("memories").orderBy("ts","desc")
      .onSnapshot(snap=>{
        mems = snap.docs.map(d=>({id:d.id,...d.data()}));
        renderThrottled();
        initLazyLoad();
      }, console.error);

    // ✅ COMO DEVE FICAR (Seguro):
auth.onAuthStateChanged(user => {
  if (user) {
    // A validação real de quem pode escrever acontecerá no servidor pelas regras do Firestore
    isAdmin = (user.email === 'macksuelr.santos@gmail.com');
    
    if (isAdmin) {
      document.getElementById("adminNav").style.display = "flex";
      document.getElementById("footHint").style.display = "none";
      render();
    } else {
      // Se for o e-mail dela ou de outra pessoa, apenas limpa o ambiente
      document.getElementById("adminNav").style.display = "none";
    }
  }
});
  } catch(e){
    console.error("Firebase erro:", e);
    showToast("Erro ao carregar dados.");
  }
}

/* ══════ LAZY LOAD IMAGES ══════ */
function initLazyLoad(){
  if(!('IntersectionObserver' in window)) return;
  
  const imageObserver = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
      if(!entry.isIntersecting) return;
      
      const img = entry.target;
      if(img.dataset.src){
        img.src = img.dataset.src;
        img.removeAttribute('data-src');
        img.classList.remove('loading');
        img.classList.add('loaded');
      }
      observer.unobserve(img);
    });
  }, { rootMargin: '50px' });
  
  document.querySelectorAll('img[data-src]').forEach(img => {
    imageObserver.observe(img);
  });
}

/* ══════ VIEWS ══════ */
function setView(v){
  view=v;
  document.querySelectorAll("#adminNav .btn-nav").forEach((b,i)=>{
    b.classList.toggle("active",["gallery","admin","themes"][i]===v);
  });
  render();
}

function logout(){
  isAdmin=false; view="gallery";
  document.getElementById("adminNav").style.display="none";
  document.getElementById("footHint").style.display="";
  if(auth) auth.signOut();
  render();
}

/* ══════ RENDER (OTIMIZADO) ══════ */
function render(){
  const t=th(), main=document.getElementById("main");
  main.innerHTML="";

  /* ── GALERIA POLAROID ── */
  if(view==="gallery"){
    if(mems.length===0){
      main.style.padding="1.5rem 1.2rem 2.5rem";
      main.innerHTML=`<div class="empty">
        <div style="font-size:2.5rem;margin-bottom:1rem;animation:shimmer 2s infinite;color:${t.acc}">${t.em}</div>
        <p style="font-style:italic;font-size:1rem;color:${t.mt}">Este jardim aguarda suas memórias...</p>
        ${isAdmin
          ? `<button onclick="setView('admin')" style="margin-top:1.2rem;background:${t.acc}20;border:1px solid ${t.acc}50;color:${t.acc};padding:.5rem 1.5rem;border-radius:8px;font-size:.85rem">+ Adicionar primeira memória</button>`
          : `<p style="font-size:.68rem;margin-top:1rem;color:${t.mt};opacity:.5">Meu raio de luminosidade, te amor meu amo</p>`}
      </div>`;
    } else {
      main.style.padding = "0";
      const cols = Math.min(3, Math.max(2, Math.floor(window.innerWidth / 320)));
      const CARD_W = 250, CARD_H = 240;
      const PAD_X = 80, PAD_Y = 50;
      const cellW = (window.innerWidth - PAD_X*2) / cols;
      const rows  = Math.ceil(mems.length / cols);
      const boardH = rows * (CARD_H + 80) + PAD_Y * 2 + 60;

      const board = document.createElement("div");
      board.className = "board";
      board.style.height = boardH + "px";

      function seed(id, idx){ return (id.charCodeAt(0)*31 + id.charCodeAt(Math.min(1,id.length-1))*17 + idx*7) % 1000 / 1000; }

      mems.forEach((m, i)=>{
        const col = i % cols;
        const row = Math.floor(i / cols);

        const jitterX = (seed(m.id,1) - .5) * cellW * .4;
        const jitterY = (seed(m.id,2) - .5) * 50;
        const rot     = (seed(m.id,3) - .5) * 16;
        const rotHov  = rot * .3;

        const rawX = PAD_X + col * cellW + cellW/2 - CARD_W/2 + jitterX;
        const baseX = Math.max(10, Math.min(window.innerWidth - CARD_W - 10, rawX));
        const baseY = PAD_Y + row * (CARD_H + 80) + jitterY;

        const baseTr  = `rotate(${rot}deg)`;
        const hoverTr = `rotate(${rotHov}deg)`;

        const card = document.createElement("div");
        card.className = "polaroid";
        card.style.setProperty("--base-transform",  baseTr);
        card.style.setProperty("--hover-transform", hoverTr);
        card.style.setProperty("--delay", `${i * 80}ms`);
        card.style.left = baseX + "px";
        card.style.top  = baseY + "px";
        card.style.zIndex = 2 + (i % 5);

        /* LAZY LOAD: Usar data-src em vez de src */
        if(m.photoURL){
          const img = document.createElement("img");
          img.className = "polaroid-photo loading";
          const thumbUrl = m.photoURL
            .replace('/upload/', '/upload/q_auto,f_auto,w_300,h_300,c_fill,g_auto/')
            .split('?')[0];
          img.dataset.src = thumbUrl;
          img.dataset.fullSrc = m.photoURL;
          img.alt = m.title || "Memória";
          img.loading = "lazy";
          card.appendChild(img);
        } else {
          const ph = document.createElement("div");
          ph.className = "polaroid-photo-empty";
          ph.textContent = t.em;
          card.appendChild(ph);
        }

        const cap = document.createElement("div");
        cap.className = "polaroid-caption";
        cap.innerHTML = `<span class="polaroid-title">${esc(m.title||"Memória")}</span>`+
          (m.date ? `<span class="polaroid-date">${esc(m.date)}</span>` : "");
        card.appendChild(cap);

        if(isAdmin){
          const del = document.createElement("button");
          del.className = "polaroid-del";
          del.textContent = "×";
          del.title = "Remover";
          del.addEventListener("click", async e=>{
            e.stopPropagation();
            if(!confirm("Remover esta memória?")) return;
            if(db) await db.collection("memories").doc(m.id).delete().catch(console.error);
            showToast("Removida");
          });
          card.appendChild(del);

          const edt = document.createElement("button");
          edt.className = "polaroid-edit";
          edt.textContent = "✎";
          edt.title = "Editar";
          edt.addEventListener("click", e=>{
            e.stopPropagation();
            openEditModal(m);
          });
          card.appendChild(edt);
        }

        card.addEventListener("click", ()=> openLightbox(m));
        board.appendChild(card);
      });

      main.appendChild(board);
      setTimeout(() => initLazyLoad(), 100);
    }
  }

  /* ── ADMIN: NOVA MEMÓRIA ── */
  if(view==="admin" && isAdmin){
    main.style.padding = "1.5rem 1.2rem 2.5rem";
    main.style.maxWidth = "1060px";
    main.style.margin = "0 auto";
    main.innerHTML=`<div class="section">
      <h2 style="font-family:${t.fn};color:${t.acc};font-weight:400;font-size:1.8rem;text-align:center;margin:0 0 1.8rem">Nova Memória</h2>
      <div class="form-group"><label class="form-label">Título</label><input class="form-input" id="f_title" placeholder="ex: Nosso primeiro encontro" value="${esc(form.title)}"></div>
      <div class="form-group"><label class="form-label">Data</label><input class="form-input" id="f_date" placeholder="ex: 14 de Fevereiro, 2025" value="${esc(form.date)}"></div>
      <div class="form-group">
        <label class="form-label">Foto</label>
        <input type="file" id="f_file" accept="image/*" style="display:none">
        <button id="f_photo_btn" style="background:${form.photo?"var(--acc)20":"transparent"};border:1px dashed ${form.photo?"var(--acc)":"var(--br)"};color:${form.photo?"var(--acc)":"var(--mt)"};padding:1.3rem;width:100%;border-radius:10px;font-size:.83rem">
          ${form.photo?"✓ Foto selecionada — clique para trocar":"Clique para adicionar uma foto"}
        </button>
        ${form.photo?`<img src="${form.photo}" style="width:100%;max-height:190px;object-fit:cover;border-radius:10px;margin-top:.5rem">`:""}
      </div>
      <div class="form-group"><label class="form-label">Poema / Mensagem</label><textarea class="form-input" id="f_poem" rows="8" style="resize:vertical;line-height:1.9" placeholder="Escreva aqui seu poema,&#10;mensagem ou declaração de amor...">${esc(form.poem)}</textarea></div>
      <button class="save-btn" id="saveBtn">${saving?`<span class="edit-saving"></span> Salvando...`:"Salvar Memória ♡"}</button>
    </div>`;

    document.getElementById("f_title").addEventListener("input", e=> form.title = e.target.value);
    document.getElementById("f_date").addEventListener("input",  e=> form.date  = e.target.value);
    document.getElementById("f_poem").addEventListener("input",  e=> form.poem  = e.target.value);
    document.getElementById("f_photo_btn").addEventListener("click", ()=> document.getElementById("f_file").click());

    document.getElementById("f_file").addEventListener("change", e=>{
      const f = e.target.files[0];
      if(!f) return;
      form.photoFile = f;
      form.photo = URL.createObjectURL(f);
      render();
    });

    document.getElementById("saveBtn").addEventListener("click", saveMemory);
  }

  /* ── TEMAS ── */
  if(view==="themes" && isAdmin){
    main.style.padding = "1.5rem 1.2rem 2.5rem";
    main.style.maxWidth = "1060px";
    main.style.margin = "0 auto";
    const wrap=document.createElement("div"); wrap.className="section"; wrap.style.maxWidth="700px";
    wrap.innerHTML=`<h2 style="font-family:${t.fn};color:${t.acc};font-weight:400;font-size:1.8rem;text-align:center;margin:0 0 1.8rem">Temas</h2>`;
    const grid=document.createElement("div"); grid.className="theme-grid";
    Object.entries(THEMES).forEach(([name,thm])=>{
      const btn=document.createElement("button"); btn.className="theme-card";
      btn.style.cssText=`background:${thm.card};border-color:${tn===name?thm.acc:thm.br};font-family:${thm.fn};border-width:2px`;
      btn.innerHTML=`<div style="font-size:1.8rem;margin-bottom:.4rem">${thm.em}</div>
        <div style="color:${thm.acc};font-size:.85rem;margin-bottom:.3rem">${name}</div>
        <div style="display:flex;gap:3px;justify-content:center;margin-top:.5rem">
          ${[thm.bg,thm.card,thm.acc,thm.txt].map(c=>`<div style="width:13px;height:13px;border-radius:50%;background:${c};border:1px solid ${thm.br}"></div>`).join("")}
        </div>
        ${tn===name?`<div style="color:${thm.acc};font-size:.62rem;margin-top:.35rem;letter-spacing:.08em">✓ ATIVO</div>`:""}`;
      btn.addEventListener("click", async()=>{
        tn=name; applyTheme(); render();
        if(db) await db.collection("config").doc("theme").set({name}).catch(console.error);
        showToast("Tema salvo ✓");
      });
      grid.appendChild(btn);
    });
    wrap.appendChild(grid);
    main.appendChild(wrap);
  }
}

/* ══════ SAVE MEMORY ══════ */
async function saveMemory(){
  if(!form.poem.trim() && !form.photoFile){
    showToast("Adicione uma foto ou mensagem ♡");
    return;
  }
  if(!db){
    showToast("Firebase não configurado.");
    return;
  }

  saving = true;
  render();

  try {
    let photoURL = null;

    if(form.photoFile){
      const formData = new FormData();
      formData.append("file", form.photoFile);
      formData.append("upload_preset", CLOUDINARY_PRESET);

      const response = await fetch(
        `https://api.cloudinary.com/v1_1/${CLOUDINARY_CLOUD}/image/upload`,
        { method: "POST", body: formData }
      );
      const data = await response.json();
      
      // OTIMIZADO: Transformações Cloudinary
      photoURL = (data.secure_url || '')
        .replace('/upload/', '/upload/q_auto,f_auto,w_1200,h_1200,c_fill,g_auto/')
        + '?version=' + Date.now();
    }

    await db.collection("memories").add({
      title:    form.title || "Memória",
      date:     form.date,
      poem:     form.poem,
      photoURL: photoURL,
      ts:       firebase.firestore.FieldValue.serverTimestamp()
    });

    form = { title:"", date:"", poem:"", photo:null, photoFile:null };
    showToast("Memória salva ♡");
    setTimeout(()=> setView("gallery"), 800);

  } catch(e){
    console.error(e);
    showToast("Erro ao salvar: " + e.message);
  }

  saving = false;
  render();
}

/* ══════ EDIT MODAL ══════ */
function openEditModal(m){
  const t = th();
  const ov = document.createElement("div"); ov.className="modal-overlay";
  ov.addEventListener("click", ()=> ov.remove());

  const modal = document.createElement("div"); modal.className="edit-modal";
  modal.addEventListener("click", e=> e.stopPropagation());

  modal.innerHTML=`
    <h3>Editar Memória</h3>
    <div class="form-group">
      <label class="form-label">Título</label>
      <input class="form-input" id="em_title" value="${esc(m.title||"")}">
    </div>
    <div class="form-group">
      <label class="form-label">Data</label>
      <input class="form-input" id="em_date" value="${esc(m.date||"")}">
    </div>
    <div class="form-group">
      <label class="form-label">Poema / Mensagem</label>
      <textarea class="form-input" id="em_poem" rows="8" style="resize:vertical;line-height:1.9">${esc(m.poem||"")}</textarea>
    </div>
    <div style="display:flex;gap:.8rem;margin-top:.5rem">
      <button id="em_cancel" style="flex:1;background:transparent;border:1px solid var(--br);color:var(--mt);padding:.7rem;border-radius:9px;font-size:.9rem">Cancelar</button>
      <button id="em_save" style="flex:2;background:var(--acc);color:var(--bg);border:none;padding:.7rem;border-radius:9px;font-size:.95rem;font-weight:700">Salvar alterações ♡</button>
    </div>
  `;

  ov.appendChild(modal);
  document.body.appendChild(ov);

  document.getElementById("em_cancel").addEventListener("click", ()=> ov.remove());

  document.getElementById("em_save").addEventListener("click", async ()=>{
    const title = document.getElementById("em_title").value.trim();
    const date  = document.getElementById("em_date").value.trim();
    const poem  = document.getElementById("em_poem").value.trim();

    const btn = document.getElementById("em_save");
    btn.innerHTML = `<span class="edit-saving"></span> Salvando...`;
    btn.disabled = true;

    try {
      await db.collection("memories").doc(m.id).update({ title, date, poem });
      showToast("Memória atualizada ♡");
      ov.remove();
    } catch(e){
      console.error(e);
      showToast("Erro ao salvar: " + e.message);
      btn.innerHTML = "Salvar alterações ♡";
      btn.disabled = false;
    }
  });
}

/* ══════ LIGHTBOX ══════ */
function openLightbox(m){
  const t=th();
  const ov=document.createElement("div"); ov.className="modal-overlay";
  ov.addEventListener("click",()=>ov.remove());
  const box=document.createElement("div");
  box.style.cssText=`background:${t.card};border:1px solid ${t.br};border-radius:16px;max-width:640px;width:100%;max-height:90vh;overflow:auto;animation:fadeIn .2s ease`;
  box.addEventListener("click",e=>e.stopPropagation());
  if(m.photoURL){
    const img=document.createElement("img");
    img.style.cssText="width:100%;max-height:380px;object-fit:cover;border-radius:16px 16px 0 0;display:block";
    img.src=m.photoURL;
    img.alt=m.title||"Memória";
    box.appendChild(img);
  }
  const bd=document.createElement("div"); bd.style.cssText="padding:1.6rem 1.8rem";
  bd.innerHTML=`<h2 style="font-family:${t.fn};color:${t.acc};font-weight:400;margin:0 0 .25rem;font-size:1.8rem">${esc(m.title||"Memória")}</h2>`+
    (m.date?`<p style="color:${t.mt};font-size:.7rem;margin:0 0 1.2rem;letter-spacing:.06em">${esc(m.date)}</p>`:"")+
    (m.poem?`<p style="color:${t.txt};font-family:${t.fn};font-style:italic;line-height:2.1;font-size:1.1rem;white-space:pre-wrap;margin:0">${esc(m.poem)}</p>`:"");
  box.appendChild(bd); ov.appendChild(box); document.body.appendChild(ov);
}

/* ══════ ADMIN LOGIN ══════ */
async function showAdminLogin(){
  if(!auth){
    await initFirebaseOnDemand();
    if(!auth){ showToast("Firebase Auth não inicializado."); return; }
  }
  try {
    const provider = new firebase.auth.GoogleAuthProvider();
    const result   = await auth.signInWithPopup(provider);
    const email    = result.user.email;
    const allowed  = ["macksuelr.santos@gmail.com","mayllesilva70@gmail.com"];
    if(!allowed.includes(email)){
      await auth.signOut();
      showToast("Você não tem acesso.");
      return;
    }
    isAdmin = true;
    document.getElementById("adminNav").style.display = "flex";
    document.getElementById("footHint").style.display = "none";
    setView("admin");
    showToast("Login realizado ♡");
  } catch(e){
    console.error(e);
    showToast("Erro ao fazer login.");
  }
}

/* ══════ UTILS ══════ */
function esc(s){ return(s||"").replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;").replace(/"/g,"&quot;"); }
function showToast(msg){
  const d=document.createElement("div"); d.className="toast"; d.textContent=msg;
  document.body.appendChild(d); setTimeout(()=>d.remove(),2500);
}

/* ═══════ PERFORMANCE MONITORING ═══════ */
if(typeof navigator !== 'undefined' && 'performance' in window){
  window.addEventListener('load', () => {
    const perf = window.performance.timing;
    const pageLoadTime = perf.loadEventEnd - perf.navigationStart;
    console.log('⏱️ Page Load Time:', pageLoadTime + 'ms');
  });
}

/* ═══════ SERVICE WORKER REGISTRATION ═══════ */
if('serviceWorker' in navigator) {
  window.addEventListener('load', () => {
    navigator.serviceWorker.register('/sw.js')
      .then(reg => console.log('✅ Service Worker registrado'))
      .catch(err => console.log('Service Worker error:', err));
  });
}
</script>
</body>
</html>
