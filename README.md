<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>PixelWeb · new style</title>
  <!-- Google Fonts: Playfair Display + Inter for fresh typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* reset & base -- no horizontal scroll guaranteed */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      max-width: 100%;
      overflow-x: hidden;
      width: 100%;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: #faf8f5;  /* warm off-white */
      color: #1e1b1b;
      line-height: 1.5;
    }

    .container {
      width: 100%;
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* fresh color palette */
    :root {
      --primary: #b8623c;      /* terracotta */
      --primary-dark: #9e4f2f;
      --accent: #2b5f5f;        /* deep teal */
      --soft-bg: #fff9f2;
      --gray-light: #eae3db;
      --gray: #6b5f57;
      --dark: #2a2623;
    }

    /* typography */
    h1, h2, h3, .logo {
      font-family: 'Playfair Display', serif;
      font-weight: 800;
      letter-spacing: -0.02em;
    }

    /* ----- HEADER (new style) ----- */
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 28px 0;
      flex-wrap: wrap;
      gap: 20px;
      border-bottom: 2px solid var(--gray-light);
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 2rem;
    }

    .logo i {
      font-size: 2.2rem;
      color: var(--primary);
      background: none;
      -webkit-text-fill-color: var(--primary); /* override gradient */
    }

    .logo .pixel {
      background: none;
      color: var(--accent);
      -webkit-text-fill-color: var(--accent);
      font-style: italic;
    }

    .nav-links {
      display: flex;
      gap: 36px;
      font-weight: 500;
      color: var(--dark);
    }

    .nav-links a {
      text-decoration: none;
      color: var(--dark);
      font-size: 1.05rem;
      transition: color 0.2s;
      border-bottom: 2px solid transparent;
      padding-bottom: 4px;
    }

    .nav-links a:hover {
      color: var(--primary);
      border-bottom-color: var(--primary);
    }

    .btn {
      display: inline-block;
      background: var(--primary);
      color: white;
      font-weight: 600;
      padding: 12px 32px;
      border-radius: 0px;  /* sharp edges for modern look */
      text-decoration: none;
      transition: all 0.25s;
      border: 2px solid var(--primary);
      font-size: 1rem;
      letter-spacing: 0.3px;
      box-shadow: 6px 6px 0 var(--accent);
    }

    .btn:hover {
      background: var(--primary-dark);
      border-color: var(--primary-dark);
      transform: translate(-2px, -2px);
      box-shadow: 10px 10px 0 var(--accent);
    }

    .btn-outline {
      background: transparent;
      color: var(--primary);
      border: 2px solid var(--primary);
      box-shadow: 4px 4px 0 var(--accent);
    }

    .btn-outline:hover {
      background: var(--primary);
      color: white;
    }

    /* ----- HERO section (new asymmetric style) ----- */
    .hero {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 40px;
      padding: 60px 0 40px;
      flex-wrap: wrap;
    }

    .hero-content {
      flex: 1 1 350px;
    }

    .hero-content h1 {
      font-size: clamp(2.4rem, 8vw, 3.8rem);
      line-height: 1.1;
      margin-bottom: 20px;
      color: var(--dark);
    }

    .hero-content h1 span {
      color: var(--primary);
      text-decoration: underline wavy var(--accent) 3px;
      display: inline-block;
    }

    .hero-content p {
      font-size: 1.2rem;
      color: var(--gray);
      max-width: 520px;
      margin-bottom: 30px;
      border-left: 4px solid var(--accent);
      padding-left: 20px;
    }

    .hero-buttons {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .hero-image {
      flex: 1 1 300px;
      min-height: 280px;
      background: var(--accent);
      border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; /* organic blob */
      box-shadow: 20px 20px 0 var(--primary);
      background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 600"><rect width="800" height="600" fill="%232b5f5f"/><circle cx="500" cy="200" r="80" fill="%23b8623c" opacity="0.8"/><path d="M200,250 L400,140 L600,250 L600,450 L400,540 L200,450 Z" fill="%23eae3db" opacity="0.2"/><rect x="260" y="280" width="280" height="160" rx="8" fill="none" stroke="%23faf8f5" stroke-width="10" /><text x="320" y="420" font-family="Inter" font-weight="700" fill="%23faf8f5" font-size="48">PW</text></svg>');
      background-size: cover;
      background-position: center;
    }

    /* ----- TRUST BAR (minimal) ----- */
    .trust-bar {
      background: white;
      padding: 16px 28px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 20px 35px;
      margin: 30px 0 40px;
      border: 2px solid var(--dark);
      box-shadow: 6px 6px 0 var(--accent);
    }

    .trust-item {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 600;
      color: var(--dark);
    }

    .trust-item i {
      color: var(--primary);
      font-size: 1.4rem;
    }

    /* ----- SECTION TITLES (fresh) ----- */
    .section-title {
      text-align: center;
      font-size: clamp(2.2rem, 6vw, 3rem);
      margin: 60px 0 20px;
      position: relative;
    }

    .section-title span {
      background: var(--primary);
      color: white;
      padding: 0 12px 4px 12px;
      display: inline-block;
      transform: rotate(-1deg);
      font-style: italic;
    }

    .subhead {
      text-align: center;
      color: var(--gray);
      max-width: 600px;
      margin: 0 auto 40px;
      font-size: 1.2rem;
      border-bottom: 2px dashed var(--gray-light);
      padding-bottom: 20px;
    }

    /* ----- PROCESS STEPS (bold cards) ----- */
    .process-steps {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
      margin: 30px 0 50px;
    }

    .step {
      background: white;
      border: 2px solid var(--dark);
      padding: 30px 20px;
      flex: 1 1 170px;
      min-width: 170px;
      max-width: 220px;
      box-shadow: 8px 8px 0 var(--primary);
      transition: 0.2s;
    }

    .step:hover {
      transform: translate(-4px, -4px);
      box-shadow: 14px 14px 0 var(--accent);
    }

    .step-number {
      background: var(--accent);
      color: white;
      width: 48px;
      height: 48px;
      font-size: 1.8rem;
      font-weight: 800;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 20px;
      border: 2px solid var(--dark);
    }

    .step h4 {
      font-size: 1.4rem;
      margin-bottom: 8px;
      font-family: 'Playfair Display', serif;
    }

    .step p {
      color: var(--gray);
      font-size: 0.95rem;
    }

    /* ----- TESTIMONIAL (inverted) ----- */
    .testimonial {
      background: var(--dark);
      border: 3px solid var(--primary);
      padding: 50px 40px;
      margin: 60px 0;
      display: flex;
      flex-wrap: wrap;
      gap: 35px;
      align-items: center;
      box-shadow: 18px 18px 0 var(--accent);
    }

    .testimonial-content {
      flex: 2 1 260px;
      color: #f0eae4;
    }

    .testimonial-content i {
      font-size: 4rem;
      color: var(--primary);
      opacity: 0.6;
    }

    .testimonial-content p {
      font-size: 1.4rem;
      font-weight: 300;
      margin: 15px 0 20px;
      line-height: 1.4;
    }

    .client-info h5 {
      font-size: 1.3rem;
      color: white;
      font-family: 'Playfair Display', serif;
    }

    .avatar-placeholder {
      background: var(--gray-light);
      width: 140px;
      height: 140px;
      border-radius: 0px;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 4px solid var(--primary);
      transform: rotate(3deg);
    }

    .avatar-placeholder i {
      font-size: 4rem;
      color: var(--accent);
    }

    /* ----- CTA (bold) ----- */
    .cta-section {
      background: var(--soft-bg);
      border: 3px solid var(--dark);
      padding: 60px 40px;
      text-align: center;
      margin: 60px 0;
      box-shadow: 14px 14px 0 var(--primary);
    }

    .cta-section h2 {
      font-size: clamp(2rem, 6vw, 3rem);
      color: var(--dark);
    }

    .btn-large {
      font-size: 1.2rem;
      padding: 16px 48px;
      margin-top: 25px;
    }

    /* ----- FOOTER (structured) ----- */
    footer {
      border-top: 3px solid var(--dark);
      padding: 40px 0 30px;
      margin-top: 40px;
    }

    .footer-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: flex-start;
      gap: 30px;
    }

    .contact-info {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 12px;
      color: var(--dark);
    }

    .contact-item i {
      color: var(--primary);
      font-size: 1.2rem;
      width: 24px;
    }

    .contact-item a {
      color: var(--dark);
      text-decoration: none;
      border-bottom: 1px dashed var(--gray);
    }

    .contact-item a:hover {
      color: var(--primary);
      border-bottom-style: solid;
    }

    .socials {
      display: flex;
      gap: 25px;
    }

    .socials a {
      color: var(--dark);
      font-size: 1.6rem;
      transition: 0.2s;
    }

    .socials a:hover {
      color: var(--primary);
      transform: translateY(-4px);
    }

    .copyright {
      margin-top: 30px;
      text-align: center;
      color: var(--gray);
      font-size: 0.95rem;
      border-top: 1px solid var(--gray-light);
      padding-top: 25px;
    }

    /* responsive */
    @media (max-width: 600px) {
      .header {
        flex-direction: column;
        align-items: stretch;
      }
      .nav-links {
        justify-content: center;
      }
      .btn {
        width: 100%;
        text-align: center;
      }
      .hero-buttons .btn {
        width: auto;
      }
      .trust-bar {
        flex-direction: column;
        align-items: flex-start;
      }
      .footer-grid {
        flex-direction: column;
      }
    }

    @media (max-width: 400px) {
      .container {
        padding: 0 18px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    
    <div class="header">
      <div class="logo">
        <i class="fas fa-cube"></i>
        <span><span class="pixel">Pixel</span>Web</span>
      </div>
      <div class="nav-links">
      
      </div>
      <a href="tel:+919137182075" class="btn">Browse sites</a>
    </div>

  
    <div class="hero">
      <div class="hero-content">
        <h1>pixel perfect websites, <span>ready to buy</span> -- instantly.</h1>
        <p>PixelWeb offers high-end, launch-ready websites. Find the perfect site and make it yours today.</p>
        <div class="hero-buttons">
          <a href="tel:+919137182075" class="btn"><i class="fas fa-bolt" style="margin-right:8px;"></i>Browse marketplace</a>
          <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i> Live preview</a>
        </div>
   

    
    <div class="trust-bar">
      <div class="trust-item"><i class="fas fa-cubes"></i> 1,450+ sites sold</div>
      <div class="trust-item"><i class="fas fa-face-smile"></i> 920+ happy clients</div>
      <div class="trust-item"><i class="fas fa-bolt"></i> onlyday</div>
    </div>

    
    <h2 class="section-title"><span>how to</span> get your site</h2>
    <p class="subhead">four simple steps -- no complicated stuff</p>
    
    <div class="process-steps">
      <div class="step"><div class="step-number">1</div><h4>Choose name</h4><p>Browse our collection.</p></div>
      <div class="step"><div class="step-number">2</div><h4>Secure checkout</h4><p>Fast & encrypted.</p></div>
      <div class="step"><div class="step-number">3</div><h4>Instant files</h4><p>Get full source.</p></div>
      <div class="step"><div class="step-number">4</div><h4>Launch</h4><p>Go live 5 or 6 days.</p></div>
    </div>

   
    <div class="testimonial">
      <div class="testimonial-content">
        <i class="fas fa-quote-right"></i>
        <p>I bought website and had it running in one evening. The code is clean, the design is stunning -- exactly what I needed.</p>
        <div class="client-info">
          <h5>bites2brands</h5>
        </div>
      </div>
      <div class="testimonial-avatar">
        <div class="avatar-placeholder">
          <i class="fas fa-user-astronaut"></i>
        </div>
      </div>
    </div>

   
    <div class="cta-section">
      <h2>Ready to own a professional website?</h2>
      <p style="font-size:1.2rem; color:var(--gray); max-width:550px; margin:20px auto;">Join thousands of happy PixelWeb owners. Instant download after purchase.</p>
      <a href="tel:+919137182075" class="btn btn-large" style="background:var(--dark); border-color:var(--dark); box-shadow:8px 8px 0 var(--primary);">Start browsing <i class="fas fa-arrow-right" style="margin-left:8px;"></i></a>
      <p style="margin-top: 30px; color:var(--gray);"><i class="fas fa-circle-check" style="color:var(--primary);"></i> 30‑day money‑back guarantee</p>
    </div>

   
    <footer>
      <div class="footer-grid">
        <div class="contact-info">
          <div class="contact-item">
            <i class="fas fa-envelope"></i>
            <a href="mailto:mseshan45@gmail.com">mseshan45@gmail.com</a>
          </div>
          <div class="contact-item">
            <i class="fab fa-instagram"></i>
            <a href="https://instagram.com/unome7366" target="_blank">@unome7366</a>
          </div>
          <div class="contact-item">
            <i class="fas fa-phone"></i>
            <a href="tel:+919137182075">+91 9137182075</a>
          </div>
        </div>
        <div class="socials">
          <a href="https://instagram.com/unome7366" target="_blank"><i class="fab fa-instagram"></i></a>
          <a href="mailto:mseshan45@gmail.com"><i class="fas fa-envelope"></i></a>
        </div>
      </div>
      <div class="copyright">
        © 2025 PixelWeb -- buy premium websites.
      </div>
    </footer>
  </div>
</body>
</html>
