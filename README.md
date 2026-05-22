<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#FBFAF7">
<title>YourLocalEye Toscana — Téléchargez l'application</title>
<meta name="description" content="Téléchargez YourLocalEye Toscana — votre guide local de la Toscane, sur App Store et Google Play.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700;900&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500;1,600&display=swap" rel="stylesheet">

<style>
  :root {
    /* Brand palette — matches the itinerary pages */
    --blue:           #003366;
    --blue-deep:      #001a33;
    --blue-mid:       #15406D;
    --blue-soft:      #E8F0F8;
    --yellow:         #FFCC00;
    --yellow-deep:    #E6B800;
    --yellow-glow:    rgba(255, 204, 0, 0.35);
    --cream:          #FBFAF7;
    --cream-deep:     #F0EBE0;
    --paper:          #FFFFFF;
    --ink:            #0A1729;
    --ink-soft:       #6B7A8E;
    --muted:          #6B7A8E;
    --line:           rgba(0, 51, 102, 0.08);
    --line-strong:    rgba(0, 51, 102, 0.18);

    /* Kept for back-compat with existing rules — green stays as an accent */
    --green:          #3FAE3F;
    --green-deep:     #2D8A2D;
    --green-soft:     rgba(63, 174, 63, 0.10);

    --radius:         24px;
    --radius-sm:      14px;
    --shadow-sm:      0 4px 14px -4px rgba(0, 51, 102, 0.10), 0 2px 4px rgba(0, 51, 102, 0.04);
    --shadow-md:      0 8px 24px -8px rgba(0, 51, 102, 0.16), 0 2px 6px rgba(0, 51, 102, 0.05);
    --shadow-lg:      0 22px 54px -16px rgba(0, 51, 102, 0.30);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
  html, body {
    font-family: 'Lato', -apple-system, BlinkMacSystemFont, sans-serif;
    color: var(--ink);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    min-height: 100%;
    background: var(--cream);
    overflow-x: hidden;
  }

  /* ═══════════════════════════════════════════
     PAGE BACKDROP — sun-baked landscape feel
     ═══════════════════════════════════════════ */
  body {
    position: relative;
    min-height: 100vh;
    padding: 40px 22px 60px;
    background:
      radial-gradient(ellipse 80% 50% at 50% 0%, rgba(0, 51, 102, 0.05), transparent 60%),
      radial-gradient(ellipse 70% 50% at 50% 100%, rgba(255, 204, 0, 0.06), transparent 60%),
      var(--cream);
  }

  /* Drifting paper grain — disabled to match itinerary pages' clean look */

  /* Soft yellow glow top-right — brand accent */
  .deco-sun {
    position: absolute;
    top: 36px; right: 32px;
    width: 110px; height: 110px;
    border-radius: 50%;
    background: radial-gradient(circle, var(--yellow) 0%, rgba(255, 204, 0, 0.25) 50%, transparent 75%);
    pointer-events: none;
    z-index: 0;
    opacity: 0.5;
    animation: sunPulse 8s ease-in-out infinite;
  }
  /* Soft navy glow bottom-left */
  .deco-orb-blue {
    position: absolute;
    bottom: 80px; left: -30px;
    width: 160px; height: 160px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(0, 51, 102, 0.14) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
    animation: sunPulse 10s ease-in-out infinite 2s;
  }
  @keyframes sunPulse {
    0%, 100% { opacity: 0.45; transform: scale(1); }
    50%      { opacity: 0.75; transform: scale(1.08); }
  }

  /* ═══════════════════════════════════════════
     CONTAINER
     ═══════════════════════════════════════════ */
  .container {
    position: relative;
    z-index: 2;
    max-width: 480px;
    margin: 0 auto;
  }

  /* ═══════════════════════════════════════════
     INTRO — eyebrow + brand mark
     ═══════════════════════════════════════════ */
  .intro {
    text-align: center;
    margin-bottom: 36px;
    animation: rise 1s cubic-bezier(0.16, 1, 0.3, 1) backwards;
  }
  .intro-eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 16px;
    color: var(--blue-deep);
    letter-spacing: 0.4px;
    margin-bottom: 6px;
  }
  .intro-eyebrow::before, .intro-eyebrow::after {
    content: '';
    width: 22px; height: 1px;
    background: var(--blue);
    opacity: 0.6;
  }

  /* App icon — the user's PNG */
  .app-icon-wrap {
    width: 132px; height: 132px;
    margin: 8px auto 22px;
    border-radius: 32px;
    background: var(--paper);
    box-shadow:
      0 0 0 5px rgba(255, 255, 255, 0.7),
      0 24px 40px -16px rgba(0, 51, 102, 0.30),
      0 50px 80px -30px rgba(0, 51, 102, 0.20);
    overflow: hidden;
    position: relative;
    animation: float 6s ease-in-out infinite;
  }
  @keyframes float {
    0%, 100% { transform: translateY(0) rotate(-1deg); }
    50%      { transform: translateY(-6px) rotate(1deg); }
  }
  .app-icon-wrap img {
    width: 100%; height: 100%;
    object-fit: cover;
    display: block;
  }
  /* Fallback if icon doesn't load */
  .app-icon-fallback {
    position: absolute; inset: 0;
    display: grid; place-items: center;
    background: linear-gradient(135deg, var(--blue) 0%, var(--blue-deep) 100%);
    color: var(--cream);
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-weight: 600;
    font-size: 38px;
    z-index: 1;
  }

  .app-title {
    font-family: 'Lato', sans-serif;
    font-weight: 900;
    font-size: 36px;
    color: var(--ink);
    letter-spacing: -1px;
    line-height: 1;
    margin-bottom: 8px;
  }
  .app-title em {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-weight: 500;
    color: var(--yellow-deep);
    letter-spacing: -0.5px;
  }
  .app-tag {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 18px;
    color: var(--ink-soft);
    max-width: 320px;
    margin: 0 auto;
    line-height: 1.4;
  }

  @keyframes rise {
    from { opacity: 0; transform: translateY(28px); filter: blur(6px); }
    to   { opacity: 1; transform: translateY(0); filter: blur(0); }
  }

  /* ═══════════════════════════════════════════
     STORE BUTTONS
     ═══════════════════════════════════════════ */
  .stores {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 34px;
    animation: rise 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s backwards;
  }
  .store-btn {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 14px 22px 14px 16px;
    background: var(--blue);
    color: #fff;
    text-decoration: none;
    border-radius: 999px;
    box-shadow: 0 12px 24px -8px rgba(0, 51, 102, 0.40);
    transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1), box-shadow 0.25s;
    border: 2px solid var(--blue-deep);
  }
  .store-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 18px 36px -10px rgba(0, 51, 102, 0.50);
  }
  .store-btn:active { transform: translateY(0) scale(0.99); }
  .store-icon {
    width: 38px; height: 38px;
    display: grid; place-items: center;
    flex-shrink: 0;
  }
  .store-icon svg {
    width: 28px; height: 28px;
    fill: #fff;
  }
  .store-text {
    flex: 1;
    line-height: 1;
  }
  .store-label {
    font-family: 'Lato', sans-serif;
    font-size: 10.5px;
    font-weight: 400;
    color: rgba(255, 255, 255, 0.75);
    letter-spacing: 1.2px;
    text-transform: uppercase;
    margin-bottom: 3px;
  }
  .store-name {
    font-family: 'Lato', sans-serif;
    font-size: 19px;
    font-weight: 900;
    letter-spacing: -0.3px;
    color: #fff;
  }
  .store-arrow {
    width: 26px; height: 26px;
    border-radius: 50%;
    background: var(--yellow);
    display: grid; place-items: center;
    flex-shrink: 0;
    color: var(--blue-deep);
    font-size: 13px;
    font-weight: 900;
    transition: transform 0.25s;
  }
  .store-btn:hover .store-arrow { transform: translateX(3px); }

  /* ═══════════════════════════════════════════
     DIVIDER WITH "OR"
     ═══════════════════════════════════════════ */
  .divider {
    display: flex;
    align-items: center;
    gap: 14px;
    margin: 0 0 28px;
    color: var(--ink-soft);
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 14px;
    letter-spacing: 1px;
  }
  .divider::before, .divider::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--blue) 50%, transparent);
    opacity: 0.4;
  }

  /* ═══════════════════════════════════════════
     QR CARD
     ═══════════════════════════════════════════ */
  .qr-card {
    background: var(--paper);
    border-radius: var(--radius);
    padding: 28px 22px 24px;
    box-shadow: var(--shadow-md);
    border: 2px solid var(--cream-deep);
    text-align: center;
    position: relative;
    overflow: hidden;
    animation: rise 1s cubic-bezier(0.16, 1, 0.3, 1) 0.4s backwards;
  }
  .qr-card::before {
    content: '';
    position: absolute;
    top: -40px; left: -40px;
    width: 120px; height: 120px;
    background: radial-gradient(circle, var(--yellow-glow) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
  }
  .qr-card::after {
    content: '';
    position: absolute;
    bottom: -40px; right: -40px;
    width: 120px; height: 120px;
    background: radial-gradient(circle, var(--green-soft) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
  }
  .qr-eyebrow {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 14px;
    color: var(--green-deep);
    letter-spacing: 0.4px;
    margin-bottom: 4px;
    position: relative;
    z-index: 1;
  }
  .qr-title {
    font-family: 'Lato', sans-serif;
    font-weight: 900;
    font-size: 22px;
    color: var(--ink);
    letter-spacing: -0.5px;
    margin-bottom: 4px;
    position: relative;
    z-index: 1;
  }
  .qr-sub {
    font-family: 'Lato', sans-serif;
    font-size: 13px;
    color: var(--ink-soft);
    line-height: 1.5;
    max-width: 280px;
    margin: 0 auto 22px;
    position: relative;
    z-index: 1;
  }
  .qr-tabs {
    display: inline-flex;
    background: var(--cream-deep);
    border-radius: 999px;
    padding: 4px;
    margin-bottom: 22px;
    position: relative;
    z-index: 1;
  }
  .qr-tab {
    padding: 8px 18px;
    border: none;
    background: transparent;
    color: var(--ink-soft);
    font-family: 'Lato', sans-serif;
    font-weight: 900;
    font-size: 11px;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    border-radius: 999px;
    cursor: pointer;
    transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    display: inline-flex;
    align-items: center;
    gap: 6px;
  }
  .qr-tab svg { width: 13px; height: 13px; fill: currentColor; }
  .qr-tab.active {
    background: var(--blue);
    color: #fff;
    box-shadow: 0 6px 14px -4px rgba(0, 51, 102, 0.4);
  }
  .qr-box {
    display: inline-block;
    padding: 18px;
    background: #fff;
    border-radius: 22px;
    box-shadow: 0 0 0 4px var(--cream-deep), 0 16px 30px -10px rgba(0, 51, 102, 0.18);
    position: relative;
    z-index: 1;
  }
  .qr-box svg {
    display: block;
    width: 200px; height: 200px;
  }
  /* Loading state */
  .qr-loading {
    width: 200px; height: 200px;
    display: grid; place-items: center;
    color: var(--ink-soft);
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 14px;
  }
  .qr-foot {
    margin-top: 18px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 13px;
    color: var(--ink-soft);
    line-height: 1.45;
    position: relative;
    z-index: 1;
    max-width: 280px;
    margin-left: auto; margin-right: auto;
  }
  .qr-foot strong {
    font-family: 'Lato', sans-serif;
    font-style: normal;
    font-weight: 900;
    color: var(--blue-deep);
  }

  /* ═══════════════════════════════════════════
     FOOTER — gentle sign-off
     ═══════════════════════════════════════════ */
  .footer {
    text-align: center;
    margin-top: 36px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 14px;
    color: var(--ink-soft);
    animation: rise 1s cubic-bezier(0.16, 1, 0.3, 1) 0.6s backwards;
  }
  .footer .rule {
    display: inline-flex;
    align-items: center;
    gap: 14px;
    color: var(--blue);
    margin-bottom: 6px;
  }
  .footer .rule::before, .footer .rule::after {
    content: '';
    width: 28px; height: 1px;
    background: var(--blue);
    opacity: 0.6;
  }
  .footer-loc {
    font-family: 'Lato', sans-serif;
    font-style: normal;
    font-size: 11px;
    font-weight: 900;
    color: var(--green-deep);
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin-top: 12px;
    display: inline-flex;
    align-items: center;
    gap: 6px;
  }
  .footer-loc::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--blue);
    border-radius: 50%;
  }

  @media (max-width: 380px) {
    .app-title { font-size: 30px; }
    .store-btn { padding: 12px 18px 12px 14px; }
    .store-name { font-size: 17px; }
  }
</style>
</head>
<body>

  <!-- Decorative ambient accents -->
  <div class="deco-sun"></div>
  <div class="deco-orb-blue"></div>

  <div class="container">

    <!-- Intro -->
    <header class="intro">
      <div class="intro-eyebrow">le regard local de la Toscane</div>

      <div class="app-icon-wrap">
        <div class="app-icon-fallback">YLE</div>
        <img
          src="https://yletoscana.bestoftours.app/apiv3/photo/iphone/compilation_images_Icon@original.png?v=1765435493"
          alt="YourLocalEye Toscana app icon"
          onload="this.previousElementSibling.style.display='none'">
      </div>

      <h1 class="app-title">YourLocalEye<br><em>Toscana</em></h1>
      <p class="app-tag">Votre guide local de la Toscane — paysages, villages et adresses confidentielles, dans votre poche.</p>
    </header>

    <!-- Store buttons -->
    <section class="stores">

      <!-- App Store -->
      <a class="store-btn" href="https://apps.apple.com/tr/app/yourlocaleye-toscana/id6758154235" target="_blank" rel="noopener">
        <div class="store-icon">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.81-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/>
          </svg>
        </div>
        <div class="store-text">
          <div class="store-label">Télécharger sur</div>
          <div class="store-name">App Store</div>
        </div>
        <div class="store-arrow">→</div>
      </a>

      <!-- Google Play -->
      <a class="store-btn" href="https://play.google.com/store/apps/details?id=botler.yletoscana" target="_blank" rel="noopener">
        <div class="store-icon">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M3.61 1.81C3.23 2.2 3 2.81 3 3.6V20.4c0 .79.23 1.4.61 1.79l.05.05L13.7 12.1v-.2L3.66 1.76l-.05.05M16.81 8.88l-2.95 1.66L13.86 12l3.95 3.95L14.95 17.8l-1.6.95v-.07L3.65 22.18c.55.04 1.18-.18 1.83-.55l13.8-7.83-2.47-4.92M3.66 1.76L13.7 12.1l3.11-3.22-13.15-7.12z"/>
            <path d="M3.61 1.81C3.23 2.2 3 2.81 3 3.6V20.4c0 .79.23 1.4.61 1.79L13.86 12 3.66 1.76l-.05.05M20.16 10.85l-3.35-1.92-3.11 3.07L16.81 15.12l3.35-1.92c.96-.54.96-1.81 0-2.35z"/>
          </svg>
        </div>
        <div class="store-text">
          <div class="store-label">Disponible sur</div>
          <div class="store-name">Google Play</div>
        </div>
        <div class="store-arrow">→</div>
      </a>

    </section>

    <div class="divider">ou scannez avec votre téléphone</div>

    <!-- QR Card -->
    <section class="qr-card">
      <div class="qr-eyebrow">scannez et téléchargez</div>
      <h2 class="qr-title">QR Code</h2>
      <p class="qr-sub">Pointez l'appareil photo de votre téléphone sur le code pour accéder directement à l'application.</p>

      <div class="qr-tabs">
        <button class="qr-tab active" data-target="ios">
          <svg viewBox="0 0 24 24"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.81-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/></svg>
          iOS
        </button>
        <button class="qr-tab" data-target="android">
          <svg viewBox="0 0 24 24"><path d="M3.61 1.81C3.23 2.2 3 2.81 3 3.6V20.4c0 .79.23 1.4.61 1.79L13.86 12 3.66 1.76l-.05.05M16.81 8.88l-2.95 1.66L13.86 12l3.95 3.95L14.95 17.8l-1.6.95v-.07L3.65 22.18c.55.04 1.18-.18 1.83-.55l13.8-7.83-2.47-4.92"/></svg>
          Android
        </button>
      </div>

      <div class="qr-box">
        <div id="qrTarget">
          <div class="qr-loading">Génération du QR code…</div>
        </div>
      </div>

      <p class="qr-foot">Compatible <strong>iPhone</strong>, <strong>iPad</strong> et appareils <strong>Android</strong>.</p>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="rule">grazie</div>
      <p>Une application pensée pour les voyageurs curieux.</p>
      <div class="footer-loc">Toscana · Italia</div>
    </footer>

  </div>

  <!-- QR code generation — Naver qrcodejs, served from cdnjs -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
  <script>
    (function () {
      'use strict';

      var APP_URLS = {
        ios:     'https://apps.apple.com/tr/app/yourlocaleye-toscana/id6758154235',
        android: 'https://play.google.com/store/apps/details?id=botler.yletoscana'
      };

      function renderQr(target) {
        var url = APP_URLS[target];
        if (!url) return;
        var host = document.getElementById('qrTarget');
        host.innerHTML = ''; // reset before redraw

        if (typeof QRCode === 'undefined') {
          // Library didn't load — graceful fallback: show URL as text
          host.innerHTML = '<div class="qr-loading" style="font-size:11px; text-align:center; padding:0 8px; word-break:break-all;">' + url + '</div>';
          return;
        }
        try {
          new QRCode(host, {
            text: url,
            width: 200,
            height: 200,
            colorDark:  '#001a33',   // matches --blue-deep
            colorLight: '#ffffff',
            correctLevel: QRCode.CorrectLevel.M
          });
        } catch (err) {
          host.innerHTML = '<div class="qr-loading" style="font-size:11px; text-align:center; padding:0 8px; word-break:break-all;">' + url + '</div>';
          console.warn('QR generation failed:', err);
        }
      }

      // Tab switching
      var tabs = document.querySelectorAll('.qr-tab');
      tabs.forEach(function (tab) {
        tab.addEventListener('click', function () {
          tabs.forEach(function (t) { t.classList.remove('active'); });
          tab.classList.add('active');
          renderQr(tab.dataset.target);
        });
      });

      // Initial render — wait for library if needed
      function init() {
        if (typeof QRCode === 'undefined') {
          setTimeout(init, 200);
          return;
        }
        renderQr('ios');
      }
      if (document.readyState === 'loading') {
        document.addEventListener('DOMContentLoaded', init);
      } else {
        init();
      }
    })();
  </script>

</body>
</html>
