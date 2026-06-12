<!--DOCTYPE html-->
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>JC@webs – WhatsApp Web Solutions</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --green:   #25D366;
      --green-d: #128C47;
      --black:   #0d0d0d;
      --offwhite:#F7F5F0;
      --gray:    #6b7280;
      --card:    #161616;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--offwhite);
      color: var(--black);
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      background: var(--black);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .nav-logo {
      font-family: 'Syne', sans-serif;
      font-size: 1.4rem;
      color: var(--green);
      letter-spacing: -0.5px;
    }
    .nav-links a {
      color: #ccc;
      text-decoration: none;
      margin-left: 28px;
      font-size: 0.9rem;
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--green); }

    /* ── HERO ── */
    .hero {
      background: var(--black);
      color: white;
      text-align: center;
      padding: 100px 24px 80px;
    }
    .hero-tag {
      display: inline-block;
      background: var(--green-d);
      color: white;
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      padding: 6px 16px;
      border-radius: 99px;
      margin-bottom: 24px;
    }
    .hero h1 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(2.2rem, 6vw, 4rem);
      line-height: 1.1;
      max-width: 700px;
      margin: 0 auto 20px;
    }
    .hero h1 span { color: var(--green); }
    .hero p {
      color: #aaa;
      max-width: 480px;
      margin: 0 auto 40px;
      font-size: 1.05rem;
      line-height: 1.7;
    }
    .btn-wa {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: var(--green);
      color: #fff;
      font-weight: 600;
      font-size: 1rem;
      padding: 16px 32px;
      border-radius: 99px;
      text-decoration: none;
      transition: background .2s, transform .15s;
      box-shadow: 0 4px 20px rgba(37,211,102,0.35);
    }
    .btn-wa:hover { background: var(--green-d); transform: translateY(-2px); }

    /* ── STATS STRIP ── */
    .stats {
      display: flex;
      justify-content: center;
      gap: 60px;
      padding: 50px 24px;
      background: white;
      flex-wrap: wrap;
    }
    .stat-item { text-align: center; }
    .stat-item strong {
      display: block;
      font-family: 'Syne', sans-serif;
      font-size: 2.2rem;
      color: var(--green-d);
    }
    .stat-item span { font-size: 0.85rem; color: var(--gray); }

    /* ── SERVICES ── */
    .section { padding: 80px 24px; max-width: 1100px; margin: 0 auto; }
    .section-label {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--green-d);
      margin-bottom: 12px;
    }
    .section h2 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(1.8rem, 4vw, 2.6rem);
      margin-bottom: 48px;
    }
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
    }
    .card {
      background: var(--card);
      color: white;
      border-radius: 16px;
      padding: 32px 28px;
      transition: transform .2s;
    }
    .card:hover { transform: translateY(-4px); }
    .card-icon { font-size: 2rem; margin-bottom: 16px; }
    .card h3 { font-family: 'Syne', sans-serif; font-size: 1.15rem; margin-bottom: 10px; }
    .card p { color: #aaa; font-size: 0.9rem; line-height: 1.7; }

    /* ── HOW IT WORKS ── */
    .how { background: white; }
    .steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 32px;
      counter-reset: steps;
    }
    .step { position: relative; }
    .step-num {
      font-family: 'Syne', sans-serif;
      font-size: 3rem;
      color: #e5e7eb;
      line-height: 1;
      margin-bottom: 12px;
    }
    .step h3 { font-size: 1rem; font-weight: 600; margin-bottom: 8px; }
    .step p { font-size: 0.88rem; color: var(--gray); line-height: 1.7; }

    /* ── WORKS / PORTFOLIO ── */
    .portfolio-card {
      background: var(--card);
      color: white;
      border-radius: 16px;
      padding: 36px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 24px;
    }
    .portfolio-card h3 { font-family: 'Syne', sans-serif; font-size: 1.4rem; margin-bottom: 8px; }
    .portfolio-card p { color: #aaa; font-size: 0.9rem; max-width: 420px; line-height: 1.7; }
    .tag {
      display: inline-block;
      background: rgba(37,211,102,0.15);
      color: var(--green);
      font-size: 0.75rem;
      padding: 4px 12px;
      border-radius: 99px;
      margin-bottom: 12px;
    }

    /* ── CONTACT ── */
    .contact-wrap {
      background: var(--black);
      color: white;
      border-radius: 20px;
      padding: 60px 40px;
      text-align: center;
    }
    .contact-wrap h2 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(1.6rem, 3.5vw, 2.4rem);
      margin-bottom: 12px;
    }
    .contact-wrap p { color: #aaa; margin-bottom: 32px; }
    .contact-btns { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }
    .btn-outline {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid #444;
      color: white;
      padding: 14px 28px;
      border-radius: 99px;
      text-decoration: none;
      font-size: 0.9rem;
      transition: border-color .2s, color .2s;
    }
    .btn-outline:hover { border-color: var(--green); color: var(--green); }

    /* ── FOOTER ── */
    footer {
      background: var(--black);
      color: #666;
      text-align: center;
      padding: 30px 24px;
      font-size: 0.85rem;
      border-top: 1px solid #1f1f1f;
    }
    footer span { color: var(--green); }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">JC@webs</div>
  <div class="nav-links">
    <a href="#services">Services</a>
    <a href="#works">Works</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-tag">🟢 WhatsApp-Powered Websites</div>
  <h1>Get More Customers<br/>Through <span>WhatsApp</span></h1>
  <p>We build simple, fast websites that connect your business directly to your customers via WhatsApp — no apps, no fuss.</p>
  <a href="https://wa.me/255689276948" class="btn-wa">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.119.554 4.107 1.523 5.832L.057 23.486a.5.5 0 0 0 .612.612l5.654-1.466A11.945 11.945 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.9a9.9 9.9 0 0 1-5.031-1.371l-.361-.214-3.741.97.997-3.643-.235-.374A9.862 9.862 0 0 1 2.1 12C2.1 6.532 6.532 2.1 12 2.1c5.469 0 9.9 4.432 9.9 9.9 0 5.469-4.431 9.9-9.9 9.9z"/></svg>
    Chat With Us on WhatsApp
  </a>
</section>

<!-- STATS -->
<div class="stats">
  <div class="stat-item"><strong>Fast</strong><span>Sites live in 3–7 days</span></div>
  <div class="stat-item"><strong>Simple</strong><span>No tech skills needed from you</span></div>
  <div class="stat-item"><strong>Affordable</strong><span>Packages from $50</span></div>
</div>

<!-- SERVICES -->
<div class="section" id="services">
  <p class="section-label">What We Do</p>
  <h2>Services We Offer</h2>
  <div class="cards">
    <div class="card">
      <div class="card-icon">🌐</div>
      <h3>Business Websites</h3>
      <p>Clean, professional websites designed to attract and convert customers for your business.</p>
    </div>
    <div class="card">
      <div class="card-icon">📲</div>
      <h3>WhatsApp Integration</h3>
      <p>Every site we build connects directly to your WhatsApp — customers message you in one tap.</p>
    </div>
    <div class="card">
      <div class="card-icon">🔧</div>
      <h3>Website Maintenance</h3>
      <p>We keep your website updated, running fast, and looking great every month.</p>
    </div>
    <div class="card">
      <div class="card-icon">🎨</div>
      <h3>Landing Pages</h3>
      <p>Single-page sites built to promote a product, service, or event and drive quick action.</p>
    </div>
  </div>
</div>

<!-- HOW IT WORKS -->
<div class="how">
  <div class="section">
    <p class="section-label">The Process</p>
    <h2>How It Works</h2>
    <div class="steps">
      <div class="step">
        <div class="step-num">01</div>
        <h3>You Contact Us</h3>
        <p>Send us a WhatsApp message telling us about your business and what you need.</p>
      </div>
      <div class="step">
        <div class="step-num">02</div>
        <h3>We Design It</h3>
        <p>We create a custom website design based on your brand and goals.</p>
      </div>
      <div class="step">
        <div class="step-num">03</div>
        <h3>You Approve</h3>
        <p>Review the design and request any changes before we go live.</p>
      </div>
      <div class="step">
        <div class="step-num">04</div>
        <h3>Go Live!</h3>
        <p>Your site launches and starts connecting you with customers instantly.</p>
      </div>
    </div>
  </div>
</div>

<!-- WORKS -->
<div class="section" id="works">
  <p class="section-label">Our Work</p>
  <h2>Recent Projects</h2>
  <div class="portfolio-card">
    <div>
      <span class="tag">Cargo & Logistics</span>
      <h3>Africa Cargo Delivery</h3>
      <p>A clean business website for a cargo delivery company operating across Africa. Customers can book and enquire directly via WhatsApp with one tap.</p>
    </div>
    <a href="https://wa.me/255794699408?text=Hello%20I%20need%20cargo%20services" class="btn-wa" style="white-space:nowrap;">
      View on WhatsApp
    </a>
  </div>
</div>

<!-- CONTACT -->
<div class="section" id="contact">
  <div class="contact-wrap">
    <h2>Ready to Get Your Website?</h2>
    <p>Reach out today — we'll build your site and connect it to WhatsApp.</p>
    <div class="contact-btns">
      <a href="https://wa.me/255689276948" class="btn-wa">
        💬 WhatsApp Us
      </a>
      <a href="mailto:chalemajericho25@gmail.com" class="btn-outline">
        📧 Send an Email
      </a>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <p>© 2024 <span>JC@webs</span> – Web Solutions for African Businesses</p>
</footer>

</body>
</html>
