<!index.html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>روابطي</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,600&family=Tajawal:wght@400;500;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #0b0b0c;
    --bg-soft: #121213;
    --ink: #ede9e2;
    --muted: #8a867c;
    --line: #232320;
    --gold: #c9a227;
    --gold-soft: rgba(201,162,39,0.14);
  }
  *{ box-sizing: border-box; }
  html,body{
    margin:0; padding:0;
    background: var(--bg);
    color: var(--ink);
    font-family: 'Tajawal','Inter', sans-serif;
    min-height:100vh;
  }
  body{
    display:flex;
    align-items:center;
    justify-content:center;
    padding: 32px 16px 64px;
    position:relative;
    overflow-x:hidden;
  }

  /* ambient glow */
  body::before{
    content:"";
    position:fixed;
    top:-20%; right:-10%;
    width:60vw; height:60vw;
    background: radial-gradient(circle, rgba(201,162,39,0.10), transparent 65%);
    pointer-events:none;
    z-index:0;
  }

  .card{
    position:relative;
    z-index:1;
    width:100%;
    max-width: 420px;
    text-align:center;
  }

  .avatar-wrap{
    position:relative;
    width:104px; height:104px;
    margin: 0 auto 22px;
  }
  .avatar-ring{
    position:absolute; inset:0;
    border-radius:50%;
    border: 1px solid var(--gold);
    opacity:0.55;
    animation: spin 14s linear infinite;
  }
  .avatar-ring::before{
    content:"";
    position:absolute;
    top:-2px; left:50%;
    width:5px; height:5px;
    margin-right:-2.5px;
    background: var(--gold);
    border-radius:50%;
    box-shadow: 0 0 8px 2px var(--gold);
  }
  @keyframes spin{ to{ transform: rotate(360deg); } }

  .avatar{
    position:absolute;
    inset:8px;
    border-radius:50%;
    background: var(--bg-soft);
    border:1px solid var(--line);
    display:flex;
    align-items:center;
    justify-content:center;
    font-family:'Fraunces', serif;
    font-size:30px;
    color: var(--gold);
    overflow:hidden;
  }
  /* لو حبيت تحط صورة بدل الحرف، استبدل محتوى .avatar بـ: <img src="صورتك.jpg"> */

  h1{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size: clamp(26px, 6vw, 32px);
    margin: 0 0 6px;
    letter-spacing: 0.2px;
  }
  .tagline{
    color: var(--muted);
    font-size: 14.5px;
    margin: 0 0 30px;
    line-height:1.7;
  }

  .links{
    display:flex;
    flex-direction:column;
    gap:12px;
  }

  .link-item{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:14px;
    padding: 16px 20px;
    background: var(--bg-soft);
    border:1px solid var(--line);
    border-radius:10px;
    text-decoration:none;
    color: var(--ink);
    transition: border-color .25s ease, transform .2s ease, background .25s ease;
  }
  .link-item:hover{
    border-color: var(--gold);
    background: var(--gold-soft);
    transform: translateY(-2px);
  }
  .link-item:focus-visible{
    outline: 2px solid var(--gold);
    outline-offset: 2px;
  }

  .link-label{
    display:flex;
    align-items:center;
    gap:12px;
    font-size:15.5px;
    font-weight:500;
  }
  .dot{
    width:6px; height:6px;
    border-radius:50%;
    background: var(--muted);
    transition: background .25s ease;
  }
  .link-item:hover .dot{ background: var(--gold); }

  .arrow{
    color: var(--muted);
    font-size:15px;
    transition: transform .25s ease, color .25s ease;
  }
  .link-item:hover .arrow{
    transform: translateX(-4px);
    color: var(--gold);
  }

  footer{
    margin-top:36px;
    color: var(--muted);
    font-size:12.5px;
    letter-spacing:0.3px;
  }

  @media (prefers-reduced-motion: reduce){
    .avatar-ring{ animation:none; }
    .link-item, .arrow, .dot{ transition:none; }
  }
</style>
</head>
<body>

  <div class="card">
    <div class="avatar-wrap">
      <div class="avatar-ring"></div>
      <div class="avatar">N</div>
      <!-- غيّر الحرف "أ" لأول حرف من اسمك، أو ضع صورة داخل .avatar -->
    </div>

    <h1>Nzar Ali</h1>
    <p class="tagline">وصف بسيط عنك أو عن المحتوى اللي بتقدمه</p>

    <div class="links">

      <a class="link-item" href="https://www.instagram.com/nzarali295?igsh=MXNnNXBvZDd2Zmk0aA==" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> إنستقرام</span>
        <span class="arrow">←</span>
      </a>

      <a class="link-item" href="https://x.com/NzarAli411161" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> تويتر / X</span>
        <span class="arrow">←</span>
      </a>

      <a class="link-item" href="https://t.me/nzar295" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> تلجرام</span>
        <span class="arrow">←</span>
      </a>

      <a class="link-item" href="#" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> تيك توك</span>
        <span class="arrow">←</span>
      </a>

      <a class="link-item" href="https://youtube.com/@nzarali295?si=dnAW01K4wVcEvSTK" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> يوتيوب</span>
        <span class="arrow">←</span>
      </a>

      <a class="link-item" href="https://wa.me/qr/CV6327QOP5TGB1" target="_blank" rel="noopener">
        <span class="link-label"><span class="dot"></span> واتساب</span>
        <span class="arrow">←</span>
      </a>

      <!--
        عشان تضيف منصة جديدة، انسخ الكتلة اللي فوق دي كاملة (من <a class="link-item"... لحد </a>)
        وغيّر اسم المنصة والرابط (href="#") برابط حسابك الحقيقي.
      -->

    </div>

    <footer>© 2026</footer>
  </div>

</body>
</html>
