<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Escola Nossa Senhora da Luz | Portal Oficial</title>
<style>
:root {
  --azul: #0b3d91;
  --azul-escuro: #062a68;
  --azul-claro: #e8f0ff;
  --dourado: #d4af37;
  --amarelo: #f5b301;
  --cinza: #f5f7fa;
  --texto: #1f2937;
  --branco: #ffffff;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Arial, sans-serif;
}
html { scroll-behavior: smooth; }
body {
  background: var(--cinza);
  color: var(--texto);
  line-height: 1.6;
}

/* ============ HEADER ============ */
header {
  background: var(--azul);
  color: white;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 12px rgba(0,0,0,.2);
}
.nav {
  max-width: 1200px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 20px;
  gap: 16px;
  flex-wrap: wrap;
}
.logo {
  display: flex;
  align-items: center;
  gap: 12px;
  font-weight: bold;
  font-size: 1.15rem;
}
.logo .emblema {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  background: radial-gradient(circle at 30% 30%, #fff, var(--dourado));
  display: grid;
  place-items: center;
  color: var(--azul);
  font-weight: 900;
  font-size: 1.2rem;
  box-shadow: 0 0 0 3px var(--dourado), 0 0 20px rgba(212,175,55,.6);
}
nav ul {
  display: flex;
  list-style: none;
  gap: 6px;
  flex-wrap: wrap;
}
nav a {
  color: white;
  text-decoration: none;
  padding: 8px 14px;
  border-radius: 20px;
  font-weight: 600;
  transition: .2s;
  cursor: pointer;
}
nav a:hover, nav a.active {
  background: var(--dourado);
  color: var(--azul);
}

/* ============ HERO ============ */
.hero {
  background: linear-gradient(135deg, var(--azul-escuro), var(--azul));
  color: white;
  padding: 50px 20px 70px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.hero::after {
  content: "";
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 80% 20%, rgba(212,175,55,.15), transparent 60%);
  pointer-events: none;
}
.hero h1 {
  font-size: 2.4rem;
  margin-bottom: 8px;
  letter-spacing: 1px;
  text-shadow: 0 2px 10px rgba(0,0,0,.3);
}
.hero .subtitulo {
  color: var(--dourado);
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  font-size: .9rem;
  margin-bottom: 16px;
}
.hero p {
  max-width: 720px;
  margin: auto;
  opacity: .95;
}

/* ============ IMAGEM (SVG IA) ============ */
.imagem-escola {
  max-width: 900px;
  margin: 30px auto 0;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 20px 50px rgba(0,0,0,.35);
  border: 4px solid var(--dourado);
}
.imagem-escola svg {
  display: block;
  width: 100%;
  height: auto;
}
.legenda-imagem {
  background: var(--azul-escuro);
  color: var(--dourado);
  padding: 10px;
  font-size: .85rem;
  font-style: italic;
  text-align: center;
  letter-spacing: 1px;
}

/* ============ CONTEÚDO ============ */
.container {
  max-width: 1200px;
  margin: auto;
  padding: 50px 20px;
}
.section-title {
  text-align: center;
  margin-bottom: 36px;
}
.section-title h2 {
  color: var(--azul);
  font-size: 2rem;
  position: relative;
  display: inline-block;
  padding-bottom: 10px;
}
.section-title h2::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 70px;
  height: 4px;
  background: var(--dourado);
  border-radius: 2px;
}
.section-title p {
  color: #555;
  margin-top: 8px;
}

/* ============ GRID DE CLASSES ============ */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
  gap: 22px;
}
.card {
  background: white;
  border-radius: 16px;
  padding: 24px 20px;
  box-shadow: 0 4px 16px rgba(0,0,0,.08);
  cursor: pointer;
  transition: transform .25s, box-shadow .25s, border-color .25s;
  border-top: 5px solid var(--azul);
  text-align: center;
  position: relative;
}
.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 14px 30px rgba(11,61,145,.2);
  border-top-color: var(--dourado);
}
.card .badge {
  display: inline-block;
  background: var(--azul-claro);
  color: var(--azul);
  padding: 4px 12px;
  border-radius: 20px;
  font-size: .75rem;
  font-weight: bold;
  margin-bottom: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
}
.card .numero {
  font-size: 2.2rem;
  font-weight: 900;
  color: var(--azul);
  line-height: 1;
}
.card h3 {
  margin: 8px 0 6px;
  color: var(--azul);
  font-size: 1.05rem;
}
.card p {
  color: #555;
  font-size: .9rem;
}
.card .seta {
  color: var(--dourado);
  font-weight: bold;
  margin-top: 8px;
  display: block;
}

/* ============ PÁGINAS ============ */
.pagina { display: none; animation: fade .4s ease; }
.pagina.ativa { display: block; }
@keyframes fade {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ============ PRESENÇA ONLINE ============ */
.presenca-hero {
  background: linear-gradient(135deg, #062a68, #0b3d91);
  color: white;
  padding: 50px 20px;
  text-align: center;
  border-radius: 20px;
  margin-bottom: 40px;
  box-shadow: 0 10px 30px rgba(11,61,145,.25);
}
.presenca-hero h2 {
  font-size: 2rem;
  margin-bottom: 10px;
}
.presenca-hero p {
  max-width: 700px;
  margin: auto;
  opacity: .95;
}
.redes {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  margin-bottom: 40px;
}
.rede {
  background: white;
  border-radius: 14px;
  padding: 22px;
  text-align: center;
  text-decoration: none;
  color: var(--texto);
  box-shadow: 0 4px 14px rgba(0,0,0,.07);
  transition: .25s;
  border-bottom: 4px solid transparent;
}
.rede:hover {
  transform: translateY(-6px);
  border-bottom-color: var(--dourado);
  box-shadow: 0 12px 24px rgba(0,0,0,.12);
}
.rede .icone {
  font-size: 2.4rem;
  display: block;
  margin-bottom: 8px;
}
.rede h4 {
  color: var(--azul);
  margin-bottom: 4px;
}
.rede span {
  font-size: .85rem;
  color: #666;
}

.servicos-online {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}
.servico {
  background: white;
  border-left: 5px solid var(--dourado);
  border-radius: 14px;
  padding: 22px;
  box-shadow: 0 4px 14px rgba(0,0,0,.07);
}
.servico h4 {
  color: var(--azul);
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.servico p {
  color: #555;
  font-size: .92rem;
  margin-bottom: 12px;
}
.servico a {
  display: inline-block;
  background: var(--azul);
  color: white;
  padding: 8px 16px;
  border-radius: 20px;
  text-decoration: none;
  font-size: .85rem;
  font-weight: 600;
  transition: .2s;
}
.servico a:hover {
  background: var(--dourado);
  color: var(--azul);
}

/* ============ MODAL ============ */
.modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(6,42,104,.75);
  z-index: 200;
  align-items: center;
  justify-content: center;
  padding: 20px;
  backdrop-filter: blur(4px);
}
.modal.ativo { display: flex; }
.modal-content {
  background: white;
  max-width: 560px;
  width: 100%;
  border-radius: 20px;
  padding: 32px;
  position: relative;
  max-height: 90vh;
  overflow: auto;
  border-top: 6px solid var(--dourado);
}
.modal-content h2 {
  color: var(--azul);
  margin-bottom: 10px;
}
.modal-content .close {
  position: absolute;
  top: 12px;
  right: 18px;
  font-size: 1.8rem;
  cursor: pointer;
  color: #666;
  background: none;
  border: none;
}
.modal-content ul {
  margin: 10px 0 0 20px;
}
.modal-content .detalhe {
  margin: 8px 0;
}
.modal-content .detalhe strong {
  color: var(--azul);
}

/* ============ FOOTER ============ */
footer {
  background: var(--azul-escuro);
  color: white;
  padding: 40px 20px 20px;
  margin-top: 40px;
}
.footer-grid {
  max-width: 1200px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 30px;
  margin-bottom: 24px;
}
.footer-grid h4 {
  color: var(--dourado);
  margin-bottom: 12px;
}
.footer-grid p, .footer-grid a {
  color: #d0d8e8;
  font-size: .9rem;
  text-decoration: none;
  display: block;
  margin-bottom: 6px;
}
.footer-grid a:hover { color: var(--dourado); }
.copyright {
  text-align: center;
  border-top: 1px solid rgba(255,255,255,.15);
  padding-top: 18px;
  font-size: .85rem;
  color: #aab6cc;
}

@media (max-width: 640px) {
  .hero h1 { font-size: 1.7rem; }
  .nav { justify-content: center; }
  nav ul { justify-content: center; }
}
</style>
</head>
<body>

<header>
  <div class="nav">
    <div class="logo">
      <div class="emblema">NSL</div>
      <div>
        Escola Nossa Senhora da Luz<br>
        <span style="font-size:.75rem; font-weight:400; opacity:.85;">Ensino Primário e Iniciação</span>
      </div>
    </div>
    <nav>
      <ul>
        <li><a class="nav-link active" data-page="inicio">Início</a></li>
        <li><a class="nav-link" data-page="classes">Classes</a></li>
        <li><a class="nav-link" data-page="presenca">Presença Online</a></li>
        <li><a class="nav-link" data-page="contactos">Contactos</a></li>
      </ul>
    </nav>
  </div>
</header>

<!-- ================= PÁGINA INÍCIO ================= -->
<section id="inicio" class="pagina ativa">
  <div class="hero">
    <div class="subtitulo">Bem-vindo ao nosso portal</div>
    <h1>Escola Nossa Senhora da Luz</h1>
    <p>Educar com fé, disciplina e excelência. Um espaço de aprendizagem para a Iniciação até à 6ª Classe, onde cada criança brilha como uma luz.</p>

    <!-- Imagem da escola (SVG estilo IA) -->
    <div class="imagem-escola">
      <svg viewBox="0 0 900 500" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Ilustração da Escola Nossa Senhora da Luz">
        <defs>
          <linearGradient id="ceu" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stop-color="#87CEEB"/>
            <stop offset="60%" stop-color="#c6e5f7"/>
            <stop offset="100%" stop-color="#f7e6c6"/>
          </linearGradient>
          <linearGradient id="parede" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stop-color="#ffffff"/>
            <stop offset="100%" stop-color="#e6e9ee"/>
          </linearGradient>
          <linearGradient id="telhado" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stop-color="#a03030"/>
            <stop offset="100%" stop-color="#6d1a1a"/>
          </linearGradient>
          <radialGradient id="sol" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stop-color="#fff8b0"/>
            <stop offset="60%" stop-color="#ffe066"/>
            <stop offset="100%" stop-color="#ffd633" stop-opacity="0"/>
          </radialGradient>
          <radialGradient id="luz" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stop-color="#fffbe0" stop-opacity=".9"/>
            <stop offset="100%" stop-color="#fffbe0" stop-opacity="0"/>
          </radialGradient>
        </defs>

        <!-- Céu -->
        <rect width="900" height="500" fill="url(#ceu)"/>

        <!-- Sol -->
        <circle cx="770" cy="80" r="55" fill="url(#sol)"/>
        <circle cx="770" cy="80" r="32" fill="#ffe680"/>

        <!-- Nuvens -->
        <g fill="#ffffff" opacity=".9">
          <ellipse cx="140" cy="90" rx="50" ry="20"/>
          <ellipse cx="180" cy="80" rx="40" ry="22"/>
          <ellipse cx="200" cy="95" rx="45" ry="18"/>
          <ellipse cx="620" cy="110" rx="45" ry="18"/>
          <ellipse cx="660" cy="100" rx="38" ry="20"/>
          <ellipse cx="680" cy="115" rx="42" ry="16"/>
        </g>

        <!-- Colinas -->
        <path d="M0 380 Q150 300 300 360 T600 350 T900 380 L900 500 L0 500 Z" fill="#8fc98f"/>
        <path d="M0 420 Q200 370 450 420 T900 410 L900 500 L0 500 Z" fill="#6faf6f"/>

        <!-- Caminho -->
        <path d="M420 500 L480 500 L460 400 L440 400 Z" fill="#c9b89a"/>
        <path d="M430 500 L470 500 L458 410 L442 410 Z" fill="#d8c8a8"/>

        <!-- Corpo principal do edifício -->
        <rect x="180" y="220" width="540" height="200" fill="url(#parede)" stroke="#b9c0cc" stroke-width="2"/>

        <!-- Telhado principal -->
        <polygon points="150,220 450,120 750,220" fill="url(#telhado)" stroke="#4d1010" stroke-width="2"/>
        <!-- Linha decorativa do telhado -->
        <polygon points="150,220 450,120 750,220" fill="none" stroke="#d4af37" stroke-width="3"/>
        <line x1="180" y1="210" x2="720" y2="210" stroke="#8a2020" stroke-width="4"/>

        <!-- Torre central (campanário) -->
        <rect x="410" y="60" width="80" height="160" fill="url(#parede)" stroke="#b9c0cc" stroke-width="2"/>
        <polygon points="395,60 450,10 505,60" fill="url(#telhado)" stroke="#4d1010" stroke-width="2"/>
        <polygon points="395,60 450,10 505,60" fill="none" stroke="#d4af37" stroke-width="2.5"/>
        <!-- Cruz no topo -->
        <rect x="447" y="-8" width="6" height="22" fill="#d4af37"/>
        <rect x="439" y="0" width="22" height="6" fill="#d4af37"/>
        <!-- Janela do campanário -->
        <circle cx="450" cy="120" r="18" fill="#3a5a8c" stroke="#d4af37" stroke-width="3"/>
        <circle cx="450" cy="120" r="8" fill="#ffe680"/>
        <line x1="450" y1="102" x2="450" y2="138" stroke="#d4af37" stroke-width="2"/>
        <line x1="432" y1="120" x2="468" y2="120" stroke="#d4af37" stroke-width="2"/>

        <!-- Estrela/luz de Nossa Senhora -->
        <g transform="translate(450,190)">
          <circle r="18" fill="url(#luz)"/>
          <polygon points="0,-14 4,-4 14,-4 6,3 9,13 0,7 -9,13 -6,3 -14,-4 -4,-4"
                   fill="#fff3b0" stroke="#d4af37" stroke-width="1.5"/>
        </g>

        <!-- Janelas andar de cima -->
        <g>
          <rect x="230" y="250" width="55" height="55" fill="#7fb3e0" stroke="#d4af37" stroke-width="3" rx="4"/>
          <line x1="257" y1="250" x2="257" y2="305" stroke="#d4af37" stroke-width="2"/>
          <line x1="230" y1="277" x2="285" y2="277" stroke="#d4af37" stroke-width="2"/>

          <rect x="320" y="250" width="55" height="55" fill="#7fb3e0" stroke="#d4af37" stroke-width="3" rx="4"/>
          <line x1="347" y1="250" x2="347" y2="305" stroke="#d4af37" stroke-width="2"/>
          <line x1="320" y1="277" x2="375" y2="277" stroke="#d4af37" stroke-width="2"/>

          <rect x="525" y="250" width="55" height="55" fill="#7fb3e0" stroke="#d4af37" stroke-width="3" rx="4"/>
          <line x1="552" y1="250" x2="552" y2="305" stroke="#d4af37" stroke-width="2"/>
          <line x1="525" y1="277" x2="580" y2="277" stroke="#d4af37" stroke-width="2"/>

          <rect x="615" y="250" width="55" height="55" fill="#7fb3e0" stroke="#d4af37" stroke-width="3" rx="4"/>
          <line x1="642" y1="250" x2="642" y2="305" stroke="#d4af37" stroke-width="2"/>
          <line x1="615" y1="277" x2="670" y2="277" stroke="#d4af37" stroke-width="2"/>
        </g>

        <!-- Porta principal -->
        <rect x="415" y="330" width="70" height="90" fill="#5a3a1a" stroke="#d4af37" stroke-width="3" rx="35 35 0 0"/>
        <line x1="450" y1="330" x2="450" y2="420" stroke="#d4af37" stroke-width="2"/>
        <circle cx="438" cy="378" r="3" fill="#d4af37"/>
        <circle cx="462" cy="378" r="3" fill="#d4af37"/>
        <!-- Arco sobre a porta -->
        <path d="M405 330 Q450 285 495 330" fill="none" stroke="#d4af37" stroke-width="4"/>
        <text x="450" y="318" text-anchor="middle" font-size="12" fill="#0b3d91" font-weight="bold">NSL</text>

        <!-- Degraus -->
        <rect x="400" y="420" width="100" height="10" fill="#d8c8a8" stroke="#b9a88a"/>
        <rect x="390" y="430" width="120" height="10" fill="#c9b89a" stroke="#b9a88a"/>

        <!-- Bandeira ao lado -->
        <rect x="760" y="220" width="4" height="200" fill="#8a6a3a"/>
        <path d="M764 230 L830 245 L764 260 Z" fill="#0b3d91"/>
        <circle cx="785" cy="245" r="5" fill="#d4af37"/>

        <!-- Árvores -->
        <g>
          <rect x="90" y="360" width="12" height="60" fill="#6b4a1f"/>
          <circle cx="96" cy="345" r="38" fill="#3f8f3f"/>
          <circle cx="76" cy="355" r="26" fill="#4aa04a"/>
          <circle cx="116" cy="355" r="26" fill="#4aa04a"/>

          <rect x="800" y="370" width="10" height="50" fill="#6b4a1f"/>
          <circle cx="805" cy="355" r="30" fill="#3f8f3f"/>
          <circle cx="788" cy="365" r="20" fill="#4aa04a"/>
          <circle cx="822" cy="365" r="20" fill="#4aa04a"/>
        </g>

        <!-- Alunos (silhuetas) -->
        <g fill="#1f2937" opacity=".85">
          <circle cx="330" cy="470" r="8"/>
          <rect x="324" y="478" width="12" height="22" rx="4"/>
          <circle cx="360" cy="472" r="7"/>
          <rect x="355" y="480" width="10" height="20" rx="4"/>
          <circle cx="560" cy="470" r="8"/>
          <rect x="554" y="478" width="12" height="22" rx="4"/>
          <circle cx="590" cy="472" r="7"/>
          <rect x="585" y="480" width="10" height="20" rx="4"/>
        </g>
      </svg>
      <div class="legenda-imagem">✦ Imagem Criada pela Escola Nossa senhora da Luz✦</div>
    </div>
  </div>

  <div class="container">
    <div class="section-title">
      <h2>Sobre a Nossa Escola</h2>
      <p>Formando gerações com valores cristãos, saber e cidadania desde a infância.</p>
    </div>
    <div class="grid">
      <div class="card" style="cursor:default;">
        <div class="badge">Missão</div>
        <p>Oferecer ensino de qualidade da Iniciação à 6ª classe, promovendo o desenvolvimento integral do aluno.</p>
      </div>
      <div class="card" style="cursor:default;">
        <div class="badge">Visão</div>
        <p>Ser referência em educação primária, reconhecida pelo rigor académico e pela formação humana.</p>
      </div>
      <div class="card" style="cursor:default;">
        <div class="badge">Valores</div>
        <p>Fé, disciplina, respeito, responsabilidade, solidariedade e amor ao próximo.</p>
      </div>
    </div>
  </div>
</section>

<!-- ================= PÁGINA CLASSES ================= -->
<section id="classes" class="pagina">
  <div class="hero" style="padding:40px 20px;">
    <h1 style="font-size:1.8rem;">As Nossas Classes</h1>
    <p>Da Iniciação à 6ª Classe — clique numa turma para ver os detalhes.</p>
    <div style="margin-top:22px;">
      <input type="text" id="pesquisa" placeholder="🔍 Pesquisar classe..."
        style="width:min(480px,90%); padding:14px 20px; border:none; border-radius:30px; font-size:1rem; outline:none; box-shadow:0 6px 20px rgba(0,0,0,.2);">
    </div>
  </div>

  <div class="container">
    <div class="grid" id="gridClasses"></div>
  </div>
</section>

<!-- ================= PÁGINA PRESENÇA ONLINE ================= -->
<section id="presenca" class="pagina">
  <div class="container">
    <div class="presenca-hero">
      <h2>🌐 Presença Online</h2>
      <p>A Escola Nossa Senhora da Luz está cada vez mais perto de ti. Acompanha as nossas novidades, eventos e serviços digitais nas plataformas abaixo.</p>
    </div>

    <div class="section-title">
      <h2>Redes Sociais</h2>
      <p>Siga-nos e fique por dentro de tudo.</p>
    </div>
    <div class="redes">
      <a class="rede" href="#" target="_blank" rel="noopener">
        <span class="icone">📘</span>
        <h4>Facebook</h4>
        <span>/EscolaNossaSenhoraDaLuz</span>
      </a>
      <a class="rede" href="#" target="_blank" rel="noopener">
        <span class="icone">📸</span>
        <h4>Instagram</h4>
        <span>@escola.nsl</span>
      </a>
      <a class="rede" href="#" target="_blank" rel="noopener">
        <span class="icone">▶️</span>
        <h4>YouTube</h4>
        <span>/EscolaNSL</span>
      </a>
      <a class="rede" href="#" target="_blank" rel="noopener">
        <span class="icone">💬</span>
        <h4>WhatsApp</h4>
        <span>+244 921316260</span>
      </a>
      <a class="rede" href="#" target="_blank" rel="noopener">
        <span class="icone">✉️</span>
        <h4>Email</h4>
        <span>geral@nossasenhoradaluz.ao</span
