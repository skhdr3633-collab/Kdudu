<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aura_iQ | بوابتك لعالم الذكاء الاصطناعي</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;900&family=Montserrat:wght@600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0a0a;
    --bg-elev: #121012;
    --red: #e1122a;
    --red-bright: #ff2f45;
    --red-dark: #5c0a12;
    --red-soft: rgba(225,18,42,0.22);
    --text: #f2efee;
    --text-muted: #a39d9c;
    --border: rgba(255,255,255,0.08);
    --radius-card: 14px;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Tajawal', sans-serif;
    line-height: 1.7;
    overflow-x: hidden;
    position: relative;
  }
  body::before, body::after {
    content: "";
    position: fixed;
    width: 60vw;
    height: 60vw;
    border-radius: 50%;
    filter: blur(120px);
    opacity: 0.16;
    z-index: 0;
    pointer-events: none;
  }
  body::before {
    background: var(--red);
    top: -20vw;
    left: -15vw;
  }
  body::after {
    background: var(--red-dark);
    bottom: -25vw;
    right: -15vw;
  }
  .wrap { position: relative; z-index: 1; }
  section { padding: 100px 24px; max-width: 1100px; margin: 0 auto; }
  a { color: inherit; text-decoration: none; }
  header {
    position: fixed;
    top: 0; right: 0; left: 0;
    z-index: 50;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 32px;
    backdrop-filter: blur(10px);
    background: linear-gradient(to bottom, rgba(10,10,10,0.85), transparent);
  }
  .brand {
    font-family: 'Montserrat', sans-serif;
    font-weight: 800;
    font-size: 1.15rem;
    letter-spacing: 0.5px;
    color: var(--text);
  }
  .brand span { color: var(--red-bright); }
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding-top: 120px;
    position: relative;
  }
  .hero-orb {
    position: absolute;
    width: 420px;
    height: 420px;
    border-radius: 50%;
    background: radial-gradient(circle, var(--red-soft) 0%, transparent 70%);
    filter: blur(10px);
    z-index: -1;
    animation: breathe 6s ease-in-out infinite;
  }
  @keyframes breathe {
    0%,100% { transform: scale(1); opacity: 0.7; }
    50% { transform: scale(1.15); opacity: 1; }
  }
  .hero-mark {
    font-family: 'Montserrat', sans-serif;
    font-weight: 800;
    font-size: clamp(2.4rem, 7vw, 4.5rem);
    letter-spacing: 1px;
    margin-bottom: 22px;
  }
  .hero-mark .dim { color: var(--text); }
  .hero-mark .glow {
    color: var(--red-bright);
    text-shadow: 0 0 30px var(--red-soft), 0 0 60px rgba(225,18,42,0.25);
  }
  .hero p.tagline {
    font-size: clamp(1.05rem, 2.4vw, 1.35rem);
    color: var(--text-muted);
    max-width: 620px;
    margin-bottom: 44px;
    font-weight: 400;
  }
  .cta-row {
    display: flex;
    gap: 18px;
    flex-wrap: wrap;
    justify-content: center;
  }
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 15px 30px;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.98rem;
    transition: transform 0.25s ease, box-shadow 0.25s ease;
  }
  .btn-primary {
    background: var(--red);
    color: #fff;
  }
  .btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 30px rgba(225,18,42,0.35);
  }
  .btn-outline {
    border: 1.5px solid var(--border);
    color: var(--text);
  }
  .btn-outline:hover {
    transform: translateY(-3px);
    border-color: var(--red);
    box-shadow: 0 10px 30px rgba(225,18,42,0.18);
  }
  .btn svg { width: 20px; height: 20px; }
  .section-head { margin-bottom: 52px; text-align: center; }
  .section-head h2 {
    font-size: clamp(1.7rem, 4vw, 2.3rem);
    font-weight: 700;
    margin-bottom: 14px;
  }
  .section-head p {
    color: var(--text-muted);
    max-width: 560px;
    margin: 0 auto;
    font-size: 1.02rem;
  }
  .features {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 26px;
  }
  .feature {
    padding: 32px 26px;
    border: 1px solid var(--border);
    border-radius: var(--radius-card);
    background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
    text-align: center;
  }
  .feature .icon {
    width: 44px; height: 44px;
    margin: 0 auto 18px;
    color: var(--red-bright);
  }
  .feature h3 { font-size: 1.1rem; margin-bottom: 10px; font-weight: 700; }
  .feature p { color: var(--text-muted); font-size: 0.95rem; }
  .shortcuts-section {
    background: var(--bg-elev);
    border: 1px solid var(--border);
    border-radius: var(--radius-card);
    padding: 30px;
  }
  .shortcuts-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 18px;
  }
  .shortcut-card {
    border: 1px solid var(--border);
    border-radius: var(--radius-card);
    overflow: hidden;
    background: var(--bg-elev);
    transition: all 0.3s ease;
  }
  .shortcut-card:hover {
    transform: translateY(-6px);
    border-color: var(--red);
    box-shadow: 0 10px 25px rgba(225,18,42,0.15);
  }
  .shortcut-media {
    width: 100%;
    aspect-ratio: 4/3;
    background: linear-gradient(135deg, #1a1414, #0d0a0a);
    display: flex;
    align-items: center;
    justify-content: center;
    border-bottom: 2px solid var(--red-dark);
  }
  .shortcut-media img {
    width: 100%; height: 100%; object-fit: cover; display: block;
    -webkit-touch-callout: default;
    -webkit-user-select: auto;
    user-select: auto;
    pointer-events: auto;
  }
  .shortcut-media .placeholder-icon {
    width: 34px; height: 34px; color: var(--text-muted); opacity: 0.5;
  }
  .shortcut-card figcaption {
    padding: 14px 16px 4px;
    font-size: 0.95rem;
    font-weight: 500;
    text-align: center;
  }
  .view-btn {
    display: block;
    width: calc(100% - 32px);
    margin: 10px 16px 16px;
    padding: 10px 0;
    background: var(--red);
    color: #fff;
    border: none;
    border-radius: 999px;
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: 0.9rem;
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .view-btn:active {
    transform: scale(0.97);
  }
  .view-btn:hover {
    box-shadow: 0 6px 16px rgba(225,18,42,0.3);
  }
  .empty-shortcuts {
    text-align: center;
    padding: 40px;
    color: var(--text-muted);
  }
  .reveal {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.8s ease, transform 0.8s ease;
  }
  .reveal.in { opacity: 1; transform: translateY(0); }
  footer {
    padding: 60px 24px 40px;
    text-align: center;
    border-top: 1px solid var(--border);
  }
  footer .brand { display: block; margin-bottom: 14px; }
  footer .social-row {
    display: flex;
    justify-content: center;
    gap: 22px;
    margin-bottom: 22px;
  }
  footer .social-row a {
    width: 42px; height: 42px;
    display: flex; align-items: center; justify-content: center;
    border: 1px solid var(--border);
    border-radius: 50%;
    transition: transform 0.3s ease, border-color 0.3s ease;
  }
  footer .social-row a:hover {
    transform: translateY(-4px) scale(1.06);
    border-color: var(--red);
    box-shadow: 0 8px 22px rgba(225,18,42,0.25);
  }
  footer .social-row svg { width: 19px; height: 19px; }
  footer p.copy { color: var(--text-muted); font-size: 0.85rem; }
  @media (max-width: 820px) {
    .features { grid-template-columns: 1fr; }
    section { padding: 80px 20px; }
  }
  @media (max-width: 480px) {
    header { padding: 16px 20px; }
    .cta-row { flex-direction: column; width: 100%; }
    .btn { justify-content: center; }
  }
</style>
</head>
<body>

<header>
  <div class="brand">Aura<span>_iQ</span></div>
</header>

<div class="wrap">
  <section class="hero">
    <div class="hero-orb"></div>
    <div class="hero-mark"><span class="dim">Aura</span><span class="glow">_iQ</span></div>
    <p class="tagline">
      نكتشف أدوات الذكاء الاصطناعي قبل أن تنتشر، ونشرحها بطريقة عملية
      تفيدك في التصميم والكتابة والإنتاجية وأكثر.
    </p>
    <div class="cta-row">
      <a class="btn btn-primary" href="https://www.instagram.com/auraa_i?igsi=YmJzd3FjbGN5NDRt" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
          <rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.2" cy="6.8" r="1.1" fill="currentColor" stroke="none"/>
        </svg>
        تابعنا على انستغرام
      </a>
      <a class="btn btn-outline" href="https://t.me/aurra_iq" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
          <path d="M21 4 3 11.5l6 2M21 4l-3.2 16-6-4.3M21 4 9.8 13.2M9.8 13.2 9 20l2.8-3.5"/>
        </svg>
        برومبتات الصور على التلجرام
      </a>
    </div>
  </section>

  <section class="reveal">
    <div class="section-head">
      <h2>ماذا نقدّم لمتابعينا</h2>
      <p>محتوى مختصر ومباشر، مبني على تجربة فعلية مع الأدوات قبل نشرها.</p>
    </div>
    <div class="features">
      <div class="feature">
        <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
          <path d="M12 3v3M12 18v3M4.2 4.2l2.1 2.1M17.7 17.7l2.1 2.1M3 12h3M18 12h3M4.2 19.8l2.1-2.1M17.7 6.3l2.1-2.1"/><circle cx="12" cy="12" r="4.5"/>
        </svg>
        <h3>أدوات AI مختارة</h3>
        <p>نجرّب الأدوات الجديدة ونعرض لك الأنسب فعلاً لاستخدامك اليومي.</p>
      </div>
      <div class="feature">
        <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
          <rect x="4" y="4" width="16" height="16" rx="3"/><path d="M8 9h8M8 13h5"/>
        </svg>
        <h3>برومبتات جاهزة</h3>
        <p>مكتبة برومبتات لتوليد الصور بجودة عالية، جاهزة للنسخ والتجربة.</p>
      </div>
      <div class="feature">
        <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
          <path d="M4 19V6a2 2 0 0 1 2-2h9l5 5v10a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2Z"/><path d="M9 12h6M9 16h4"/>
        </svg>
        <h3>شروحات عملية</h3>
        <p>خطوات واضحة بدون تعقيد، تناسب المبتدئ والمستخدم المتقدم.</p>
      </div>
    </div>
  </section>

  <section class="reveal">
    <div class="section-head">
      <h2>الاختصارات</h2>
      <p>أهم الأدوات والمصادر التي نرشحها لمتابعينا.</p>
    </div>
    <div id="shortcuts-container" class="shortcuts-section"></div>
  </section>
</div>

<footer>
  <span class="brand">Aura<span style="color:var(--red-bright)">_iQ</span></span>
  <div class="social-row">
    <a href="https://www.instagram.com/auraa_i?igsi=YmJzd3FjbGN5NDRt" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.2" cy="6.8" r="1.1" fill="currentColor" stroke="none"/></svg>
    </a>
    <a href="https://t.me/aurra_iq" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M21 4 3 11.5l6 2M21 4l-3.2 16-6-4.3M21 4 9.8 13.2M9.8 13.2 9 20l2.8-3.5"/></svg>
    </a>
  </div>
  <p class="copy">© 2026 Aura_iQ — جميع الحقوق محفوظة</p>
</footer>

<script>
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        entry.target.classList.add('in');
        io.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });
  revealEls.forEach(el => io.observe(el));

  function viewImage(base64, title) {
    // فتح الصورة بصفحة منفصلة كاملة الحجم ليأخذ المتابع لقطة شاشة لها
    const win = window.open('', '_blank');
    if (win) {
      win.document.write(`
        <!DOCTYPE html>
        <html lang="ar" dir="rtl">
        <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>${title}</title>
          <style>
            body { margin:0; background:#0a0a0a; display:flex; flex-direction:column; align-items:center; justify-content:center; min-height:100vh; font-family: sans-serif; }
            img { max-width:100%; max-height:80vh; border-radius:8px; }
            p { color:#a39d9c; margin-top:16px; font-size:14px; text-align:center; padding:0 20px; }
          </style>
        </head>
        <body>
          <img src="${base64}" alt="${title}">
          <p>📸 خذ لقطة شاشة الآن لحفظ الصورة</p>
        </body>
        </html>
      `);
      win.document.close();
    }
  }

  function displayShortcuts() {
    const shortcuts = JSON.parse(localStorage.getItem('auriq_daily_shortcuts') || '{}');
    const allList = Object.values(shortcuts).flat();
    const container = document.getElementById('shortcuts-container');

    if (allList.length === 0) {
      container.innerHTML = '<div class="empty-shortcuts"><p>سيتم إضافة الاختصارات قريباً... 🚀</p></div>';
      return;
    }

    const html = `<div class="shortcuts-grid">
      ${allList.map(s => `
        <div class="shortcut-card">
          <div class="shortcut-media">
            ${s.imageBase64 ? `<img src="${s.imageBase64}" alt="${s.title}">` : `
            <svg class="placeholder-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
              <rect x="3" y="3" width="18" height="18" rx="3"/><circle cx="8.5" cy="9" r="1.5"/><path d="m21 15-5-5-9 9"/>
            </svg>`}
          </div>
          <figcaption>${s.title}</figcaption>
          ${s.imageBase64 ? `
          <button class="view-btn" onclick="viewImage('${s.imageBase64}', '${(s.title || 'image').replace(/'/g, "\\'")}')">
            🔍 اضغط لعرض الصورة كاملة
          </button>` : ''}
        </div>
      `).join('')}
    </div>`;

    container.innerHTML = html;
  }

  displayShortcuts();
  window.addEventListener('storage', displayShortcuts);
</script>
</body>
</html>
