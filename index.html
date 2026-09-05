# LE NOIR — Complete Project (Frontend + Backend, one file)

This single file contains everything: the website, and the full Node.js
backend (payments, security, WhatsApp). Each section below is one file —
when you're ready to deploy, save each code block out using the filename
shown in its heading.

**Folder layout to recreate:**
```
le-noir/
├── le-noir-website.html
└── backend/
    ├── package.json
    ├── .env.example
    ├── .gitignore
    ├── server.js
    ├── README.md
    └── src/
        ├── db.js
        ├── services/
        │   ├── catalog.js
        │   ├── razorpay.js
        │   └── whatsapp.js
        └── routes/
            ├── bookings.js
            ├── webhook.js
            └── admin.js
```

---

## 1. `le-noir-website.html` (the site — Razorpay checkout wired in)

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LE NOIR — Salon &amp; Grooming House</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0a0908;
    --charcoal:#151109;
    --charcoal-2:#1c1610;
    --gold:#c9a227;
    --gold-light:#e9cc6e;
    --bronze:#7c5a34;
    --ivory:#f1e9d8;
    --ivory-dim:#a89f8c;
    --line:rgba(201,162,39,0.25);
    --maxw:1180px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--ivory);
    font-family:'Manrope',sans-serif;
    font-size:16px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.serif{
    font-family:'Fraunces',serif;
    font-weight:500;
    margin:0;
    color:var(--ivory);
  }
  a{color:inherit;text-decoration:none;}
  img{max-width:100%;display:block;}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 32px;}
  section{position:relative;}
  ::selection{background:var(--gold);color:var(--ink);}
  :focus-visible{outline:2px solid var(--gold-light);outline-offset:3px;}

  /* ---------- Nav ---------- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    padding:22px 0;
    transition:background .4s ease, padding .4s ease, border-color .4s ease;
    border-bottom:1px solid transparent;
  }
  header.scrolled{
    background:rgba(10,9,8,0.92);
    backdrop-filter:blur(10px);
    padding:14px 0;
    border-bottom:1px solid var(--line);
  }
  nav.wrap{display:flex;align-items:center;justify-content:space-between;}
  .brand{display:flex;align-items:center;gap:10px;font-family:'Fraunces',serif;font-size:1.35rem;letter-spacing:0.06em;color:var(--ivory);}
  .brand svg{width:30px;height:30px;flex:none;}
  .nav-links{display:flex;align-items:center;gap:36px;}
  .nav-links a{font-size:0.92rem;color:var(--ivory-dim);transition:color .25s ease;position:relative;}
  .nav-links a:not(.btn):after{
    content:'';position:absolute;left:0;right:0;bottom:-6px;height:1px;background:var(--gold);
    transform:scaleX(0);transform-origin:left;transition:transform .3s ease;
  }
  .nav-links a:not(.btn):hover{color:var(--ivory);}
  .nav-links a:not(.btn):hover:after{transform:scaleX(1);}
  .btn{
    display:inline-flex;align-items:center;justify-content:center;
    padding:12px 26px;border:1px solid var(--gold);border-radius:2px;
    font-size:0.88rem;letter-spacing:0.03em;color:var(--gold-light);
    transition:background .3s ease,color .3s ease,border-color .3s ease;
    cursor:pointer;background:transparent;font-family:'Manrope',sans-serif;font-weight:600;
  }
  .btn:hover{background:var(--gold);color:var(--ink);}
  .btn-solid{background:var(--gold);color:var(--ink);}
  .btn-solid:hover{background:var(--gold-light);border-color:var(--gold-light);}
  .menu-toggle{display:none;background:none;border:none;color:var(--ivory);font-size:1.6rem;cursor:pointer;}

  /* ---------- Hero ---------- */
  .hero{
    min-height:100vh;display:flex;align-items:flex-end;
    background:
      linear-gradient(180deg, rgba(10,9,8,0.35) 0%, rgba(10,9,8,0.55) 55%, rgba(10,9,8,0.97) 100%),
      url('https://images.unsplash.com/photo-1759134248487-e8baaf31e33e?w=2200&q=80&auto=format&fit=crop') center/cover no-repeat;
    padding-top:140px;
  }
  .hero-inner{padding-bottom:70px;}
  .hero h1{
    font-size:clamp(2.6rem, 6vw, 5rem);
    line-height:1.04;
    max-width:820px;
    font-weight:500;
  }
  .hero h1 em{font-style:italic;color:var(--gold-light);}
  .hero p.lede{
    max-width:480px;color:var(--ivory-dim);font-size:1.05rem;margin-top:22px;
  }
  .hero-ctas{display:flex;gap:18px;margin-top:38px;flex-wrap:wrap;}
  .hero-stats{
    display:flex;gap:0;margin-top:64px;border-top:1px solid var(--line);padding-top:26px;flex-wrap:wrap;
  }
  .hero-stats div{padding-right:48px;margin-right:48px;border-right:1px solid var(--line);}
  .hero-stats div:last-child{border-right:none;margin-right:0;padding-right:0;}
  .hero-stats .num{font-family:'Fraunces',serif;font-size:1.4rem;color:var(--gold-light);}
  .hero-stats .lbl{font-size:0.82rem;color:var(--ivory-dim);margin-top:2px;}

  .reveal{opacity:0;transform:translateY(22px);animation:rise .9s ease forwards;}
  .r1{animation-delay:.1s;} .r2{animation-delay:.28s;} .r3{animation-delay:.46s;} .r4{animation-delay:.64s;}
  @keyframes rise{to{opacity:1;transform:translateY(0);}}
  @media (prefers-reduced-motion:reduce){
    .reveal{animation:none;opacity:1;transform:none;}
    html{scroll-behavior:auto;}
  }

  /* ---------- Ticker ---------- */
  .ticker{
    background:var(--charcoal);border-top:1px solid var(--line);border-bottom:1px solid var(--line);
    overflow:hidden;padding:16px 0;
  }
  .ticker-track{display:flex;width:max-content;animation:scroll 32s linear infinite;}
  .ticker-track span{
    font-family:'Fraunces',serif;font-style:italic;font-size:1.05rem;color:var(--ivory-dim);
    padding:0 28px;white-space:nowrap;display:flex;align-items:center;gap:28px;
  }
  .ticker-track span:after{content:'◆';color:var(--gold);font-size:0.5rem;font-style:normal;}
  @keyframes scroll{from{transform:translateX(0);}to{transform:translateX(-50%);}}

  /* ---------- Section heading ---------- */
  .kicker{color:var(--gold);font-size:0.9rem;margin-bottom:14px;font-family:'Fraunces',serif;font-style:italic;}
  .section-head{max-width:640px;margin-bottom:56px;}
  .section-head h2{font-size:clamp(1.9rem,3.4vw,2.7rem);}
  section{padding:110px 0;}

  /* ---------- Philosophy ---------- */
  .philosophy{display:grid;grid-template-columns:1.1fr 0.9fr;gap:70px;align-items:center;}
  .philosophy img{border-radius:2px;filter:saturate(0.9);}
  .philosophy p{color:var(--ivory-dim);max-width:460px;}
  blockquote{
    font-family:'Fraunces',serif;font-style:italic;font-size:1.3rem;line-height:1.5;
    color:var(--ivory);margin:30px 0 0;padding-left:24px;border-left:2px solid var(--gold);
  }
  blockquote cite{display:block;font-family:'Manrope',sans-serif;font-style:normal;font-size:0.82rem;color:var(--ivory-dim);margin-top:12px;}

  /* ---------- Services ---------- */
  .services{background:var(--charcoal);}
  .service-row{
    display:grid;grid-template-columns:1fr auto;gap:8px 40px;
    padding:30px 0;border-top:1px solid var(--line);align-items:baseline;
  }
  .services .service-row:last-of-type{border-bottom:1px solid var(--line);}
  .service-row .name{font-family:'Fraunces',serif;font-size:1.5rem;transition:color .25s ease;}
  .service-row:hover .name{color:var(--gold-light);}
  .service-row .price{font-family:'Fraunces',serif;font-size:1.5rem;color:var(--gold);white-space:nowrap;}
  .service-row .desc{grid-column:1/2;color:var(--ivory-dim);font-size:0.94rem;max-width:520px;}
  .service-note{margin-top:36px;color:var(--ivory-dim);font-size:0.9rem;}

  /* ---------- Gallery ---------- */
  .gallery-grid{
    display:grid;grid-template-columns:repeat(4,1fr);grid-auto-rows:160px;gap:14px;
  }
  .gallery-grid figure{margin:0;position:relative;overflow:hidden;border-radius:2px;}
  .gallery-grid img{width:100%;height:100%;object-fit:cover;transition:transform .6s ease;}
  .gallery-grid figure:hover img{transform:scale(1.06);}
  .gallery-grid figcaption{
    position:absolute;left:0;right:0;bottom:0;padding:14px 16px;
    background:linear-gradient(0deg, rgba(0,0,0,0.75), transparent);
    font-family:'Fraunces',serif;font-style:italic;font-size:0.95rem;color:var(--ivory);
  }
  .g1{grid-column:span 2;grid-row:span 2;}
  .g2{grid-column:span 2;grid-row:span 1;}
  .g3{grid-column:span 1;grid-row:span 1;}
  .g4{grid-column:span 1;grid-row:span 1;}

  /* ---------- Testimonials ---------- */
  .testimonials{background:var(--charcoal-2);}
  .t-wrap{max-width:720px;margin:0 auto;text-align:center;}
  .t-mark{font-family:'Fraunces',serif;font-size:3.4rem;color:var(--gold);line-height:1;margin-bottom:10px;}
  .t-quote{font-family:'Fraunces',serif;font-style:italic;font-size:1.5rem;line-height:1.5;min-height:150px;}
  .t-name{margin-top:26px;color:var(--ivory-dim);font-size:0.9rem;}
  .t-dots{display:flex;justify-content:center;gap:10px;margin-top:34px;}
  .t-dots button{
    width:8px;height:8px;border-radius:50%;border:1px solid var(--gold);background:transparent;
    cursor:pointer;padding:0;
  }
  .t-dots button.active{background:var(--gold);}

  /* ---------- Reserve ---------- */
  .reserve{display:grid;grid-template-columns:1fr 1fr;gap:60px;}
  .reserve-info h2{font-size:clamp(1.9rem,3.4vw,2.6rem);margin-bottom:18px;}
  .reserve-info p{color:var(--ivory-dim);max-width:420px;}
  .info-list{margin-top:36px;display:flex;flex-direction:column;gap:22px;}
  .info-list div{border-top:1px solid var(--line);padding-top:16px;}
  .info-list .lbl{font-size:0.82rem;color:var(--gold);margin-bottom:4px;font-family:'Fraunces',serif;font-style:italic;}
  form{background:var(--charcoal);padding:40px;border-radius:2px;border:1px solid var(--line);}
  .field{margin-bottom:20px;}
  .field label{display:block;font-size:0.82rem;color:var(--ivory-dim);margin-bottom:8px;}
  .field input,.field select,.field textarea{
    width:100%;background:transparent;border:none;border-bottom:1px solid var(--line);
    color:var(--ivory);font-family:'Manrope',sans-serif;font-size:0.98rem;padding:10px 2px;
    transition:border-color .25s ease;
  }
  .field select option{background:var(--charcoal);}
  .field input:focus,.field select:focus,.field textarea:focus{border-color:var(--gold);outline:none;}
  .field-row{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
  form .btn-solid{width:100%;margin-top:8px;padding:15px;font-size:0.92rem;}
  .form-success{
    display:none;text-align:center;padding:30px 10px;font-family:'Fraunces',serif;font-style:italic;color:var(--gold-light);
  }
  .form-error{
    display:none;color:#e07a6b;font-size:0.85rem;margin-top:14px;text-align:center;
  }
  form .btn-solid[disabled]{opacity:0.6;cursor:not-allowed;}

  /* ---------- Footer ---------- */
  footer{border-top:1px solid var(--line);padding:60px 0 34px;}
  .footer-top{display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:30px;margin-bottom:46px;}
  .footer-nav{display:flex;gap:30px;flex-wrap:wrap;}
  .footer-nav a{color:var(--ivory-dim);font-size:0.9rem;}
  .footer-nav a:hover{color:var(--gold-light);}
  .social{display:flex;gap:16px;}
  .social a{width:34px;height:34px;border:1px solid var(--line);border-radius:50%;display:flex;align-items:center;justify-content:center;transition:border-color .25s ease;}
  .social a:hover{border-color:var(--gold);}
  .social svg{width:15px;height:15px;fill:var(--ivory-dim);}
  .social a:hover svg{fill:var(--gold-light);}
  .footer-bottom{display:flex;justify-content:space-between;color:var(--ivory-dim);font-size:0.82rem;flex-wrap:wrap;gap:10px;}

  /* ---------- Responsive ---------- */
  @media (max-width:920px){
    .philosophy{grid-template-columns:1fr;gap:36px;}
    .reserve{grid-template-columns:1fr;}
    .gallery-grid{grid-template-columns:repeat(2,1fr);grid-auto-rows:180px;}
    .g1{grid-column:span 2;grid-row:span 2;}
    .g2{grid-column:span 2;}
    .nav-links{
      position:fixed;top:0;right:0;height:100vh;width:min(78vw,320px);
      background:var(--charcoal);flex-direction:column;justify-content:center;align-items:flex-start;
      padding:0 40px;gap:28px;transform:translateX(100%);transition:transform .4s ease;
      border-left:1px solid var(--line);
    }
    .nav-links.open{transform:translateX(0);}
    .menu-toggle{display:block;}
    .field-row{grid-template-columns:1fr;}
    .hero-stats div{margin-right:28px;padding-right:28px;}
  }
  @media (max-width:600px){
    .wrap{padding:0 22px;}
    section{padding:80px 0;}
    .service-row{grid-template-columns:1fr;}
    .service-row .price{grid-row:1;justify-self:end;}
    form{padding:26px;}
  }
</style>
</head>
<body>

<header id="site-header">
  <nav class="wrap">
    <a href="#top" class="brand">
      <svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="19" stroke="#C9A227" stroke-width="1"/>
        <path d="M13 27V13h3.2l3.8 9 3.8-9H27v14h-2.5V17.2L20.8 27h-1.6l-3.7-9.8V27H13z" fill="#C9A227"/>
      </svg>
      LE NOIR
    </a>
    <button class="menu-toggle" id="menuToggle" aria-label="Toggle menu">☰</button>
    <div class="nav-links" id="navLinks">
      <a href="#services">Services</a>
      <a href="#gallery">Gallery</a>
      <a href="#testimonials">Reviews</a>
      <a href="#reserve">Contact</a>
      <a href="#reserve" class="btn">Book Now</a>
    </div>
  </nav>
</header>

<section class="hero" id="top">
  <div class="wrap hero-inner">
    <h1 class="reveal r1">Where every detail<br>becomes <em>a ritual.</em></h1>
    <p class="lede reveal r2">LE NOIR is a private grooming house for the modern gentleman and woman — precision cuts, traditional shaves and quiet luxury, by appointment only.</p>
    <div class="hero-ctas reveal r3">
      <a href="#reserve" class="btn btn-solid">Reserve a Chair</a>
      <a href="#services" class="btn">View Services</a>
    </div>
    <div class="hero-stats reveal r4">
      <div><div class="num">Est. 2024</div><div class="lbl">Chennai</div></div>
      <div><div class="num">06</div><div class="lbl">Signature services</div></div>
      <div><div class="num">By appointment</div><div class="lbl">Only, no walk-ins</div></div>
    </div>
  </div>
</section>

<div class="ticker">
  <div class="ticker-track" id="tickerTrack">
    <span>Precision Cuts</span><span>Traditional Shaves</span><span>Beard Sculpting</span><span>Facial Therapy</span><span>Signature Massage</span>
    <span>Precision Cuts</span><span>Traditional Shaves</span><span>Beard Sculpting</span><span>Facial Therapy</span><span>Signature Massage</span>
  </div>
</div>

<section id="philosophy">
  <div class="wrap philosophy">
    <div>
      <div class="kicker">The house philosophy</div>
      <h2 style="font-size:clamp(1.9rem,3.4vw,2.6rem);margin-bottom:20px;">Grooming, done the unhurried way.</h2>
      <p>LE NOIR was built on a simple belief — grooming isn't a transaction, it's a ritual worth doing properly. Every chair, blade and towel is chosen with the same care as the cut itself. We keep our books small so every appointment gets full attention, not a rushed slot between two others.</p>
      <blockquote>"A good barber remembers your name. A great one remembers how you like your fade."<cite>— The House Motto</cite></blockquote>
    </div>
    <img src="https://images.unsplash.com/photo-1682989356229-a244c8903492?w=1000&q=80&auto=format&fit=crop" alt="Barber giving a precision haircut at LE NOIR">
  </div>
</section>

<section id="services" class="services">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">What we offer</div>
      <h2>Six services, one standard.</h2>
    </div>

    <div class="service-row">
      <div class="name">Signature Haircut</div>
      <div class="price">₹500</div>
      <div class="desc">Consultation, wash, precision cut and style finish tailored to your face shape.</div>
    </div>
    <div class="service-row">
      <div class="name">Beard Grooming</div>
      <div class="price">₹400</div>
      <div class="desc">Shape, line-up and condition for a beard that holds its form.</div>
    </div>
    <div class="service-row">
      <div class="name">Classic Hot Shave</div>
      <div class="price">₹300</div>
      <div class="desc">Straight-razor shave with hot towels and pre-shave oil, the old way.</div>
    </div>
    <div class="service-row">
      <div class="name">Revitalising Facial</div>
      <div class="price">₹800</div>
      <div class="desc">Deep cleanse, steam and mask suited to your skin type.</div>
    </div>
    <div class="service-row">
      <div class="name">Signature Massage</div>
      <div class="price">₹600</div>
      <div class="desc">Head, neck and shoulder release to finish the appointment properly.</div>
    </div>
    <div class="service-row">
      <div class="name">The Full House Package</div>
      <div class="price">₹1,500</div>
      <div class="desc">Haircut, beard grooming, hot shave and facial in one unhurried sitting.</div>
    </div>

    <p class="service-note">Prices shown are indicative for a standard visit and may vary with add-ons. All services are by appointment.</p>
  </div>
</section>

<section id="gallery">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Inside the house</div>
      <h2>A quiet room, done properly.</h2>
    </div>
    <div class="gallery-grid">
      <figure class="g1">
        <img src="https://images.unsplash.com/photo-1759134248487-e8baaf31e33e?w=1200&q=80&auto=format&fit=crop" alt="LE NOIR salon interior">
        <figcaption>The Chair</figcaption>
      </figure>
      <figure class="g2">
        <img src="https://images.unsplash.com/photo-1621607512026-ba3e0857c6f4?w=900&q=80&auto=format&fit=crop" alt="Barber scissors and tools">
        <figcaption>The Instruments</figcaption>
      </figure>
      <figure class="g3">
        <img src="https://images.unsplash.com/photo-1682989356229-a244c8903492?w=700&q=80&auto=format&fit=crop" alt="Precision haircut in progress">
        <figcaption>The Cut</figcaption>
      </figure>
      <figure class="g4">
        <img src="https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=700&q=80&auto=format&fit=crop" alt="Facial treatment at LE NOIR">
        <figcaption>The Finish</figcaption>
      </figure>
    </div>
  </div>
</section>

<section id="testimonials" class="testimonials">
  <div class="wrap t-wrap">
    <div class="t-mark">"</div>
    <div class="t-quote" id="tQuote">I've had my hair cut in four cities. This is the first place that asked what I actually wanted before touching the clippers.</div>
    <div class="t-name" id="tName">Arjun R. — Regular since 2024</div>
    <div class="t-dots" id="tDots">
      <button class="active" data-i="0" aria-label="Testimonial 1"></button>
      <button data-i="1" aria-label="Testimonial 2"></button>
      <button data-i="2" aria-label="Testimonial 3"></button>
    </div>
  </div>
</section>

<section id="reserve">
  <div class="wrap reserve">
    <div class="reserve-info">
      <div class="kicker">By appointment</div>
      <h2>Reserve your chair.</h2>
      <p>Tell us what you're after and we'll confirm your slot by phone or WhatsApp within the day. Walk-ins are seated only if the book allows it.</p>
      <div class="info-list">
        <div><div class="lbl">Address</div>Update with your salon's street address, area and city.</div>
        <div><div class="lbl">Hours</div>Tue – Sun, 10:00 AM – 8:00 PM · Closed Mondays</div>
        <div><div class="lbl">Phone / WhatsApp</div>+91 95660 31143</div>
      </div>
    </div>
    <div>
      <form id="bookingForm">
        <div class="field">
          <label for="fname">Full name</label>
          <input id="fname" type="text" required placeholder="Your name">
        </div>
        <div class="field-row">
          <div class="field">
            <label for="fphone">Phone number</label>
            <input id="fphone" type="tel" required placeholder="+91">
          </div>
          <div class="field">
            <label for="fservice">Service</label>
            <select id="fservice" required>
              <option value="">Choose a service</option>
              <option value="haircut">Signature Haircut — ₹500</option>
              <option value="beard">Beard Grooming — ₹400</option>
              <option value="shave">Classic Hot Shave — ₹300</option>
              <option value="facial">Revitalising Facial — ₹800</option>
              <option value="massage">Signature Massage — ₹600</option>
              <option value="fullhouse">The Full House Package — ₹1,500</option>
            </select>
          </div>
        </div>
        <div class="field-row">
          <div class="field">
            <label for="fdate">Preferred date</label>
            <input id="fdate" type="date">
          </div>
          <div class="field">
            <label for="ftime">Preferred time</label>
            <input id="ftime" type="time">
          </div>
        </div>
        <div class="field">
          <label for="fnotes">Notes (optional)</label>
          <textarea id="fnotes" rows="2" placeholder="Anything we should know"></textarea>
        </div>
        <button type="submit" class="btn btn-solid" id="bookBtn">Pay &amp; Confirm Reservation</button>
        <div class="form-error" id="formError"></div>
        <div class="form-success" id="formSuccess">Payment received — your reservation is confirmed. Look out for a WhatsApp confirmation.</div>
      </form>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div class="footer-top">
      <a href="#top" class="brand">
        <svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="20" cy="20" r="19" stroke="#C9A227" stroke-width="1"/>
          <path d="M13 27V13h3.2l3.8 9 3.8-9H27v14h-2.5V17.2L20.8 27h-1.6l-3.7-9.8V27H13z" fill="#C9A227"/>
        </svg>
        LE NOIR
      </a>
      <div class="footer-nav">
        <a href="#services">Services</a>
        <a href="#gallery">Gallery</a>
        <a href="#testimonials">Reviews</a>
        <a href="#reserve">Reserve</a>
      </div>
      <div class="social">
        <a href="#" aria-label="Instagram"><svg viewBox="0 0 24 24"><path d="M12 2c2.7 0 3 .01 4.1.06 1.1.05 1.8.22 2.4.46.7.27 1.2.6 1.7 1.1.5.5.9 1 1.1 1.7.24.6.4 1.3.46 2.4.05 1.1.06 1.4.06 4.1s-.01 3-.06 4.1c-.05 1.1-.22 1.8-.46 2.4-.27.7-.6 1.2-1.1 1.7-.5.5-1 .9-1.7 1.1-.6.24-1.3.4-2.4.46-1.1.05-1.4.06-4.1.06s-3-.01-4.1-.06c-1.1-.05-1.8-.22-2.4-.46-.7-.27-1.2-.6-1.7-1.1-.5-.5-.9-1-1.1-1.7-.24-.6-.4-1.3-.46-2.4C2.01 15 2 14.7 2 12s.01-3 .06-4.1c.05-1.1.22-1.8.46-2.4.27-.7.6-1.2 1.1-1.7.5-.5 1-.9 1.7-1.1.6-.24 1.3-.4 2.4-.46C9 2.01 9.3 2 12 2zm0 5a5 5 0 100 10 5 5 0 000-10zm0 8.2a3.2 3.2 0 110-6.4 3.2 3.2 0 010 6.4zm5.4-8.4a1.2 1.2 0 100-2.4 1.2 1.2 0 000 2.4z"/></svg></a>
        <a href="#" aria-label="WhatsApp"><svg viewBox="0 0 24 24"><path d="M17.5 14.4c-.3-.1-1.7-.8-2-.9-.3-.1-.5-.1-.6.1-.2.3-.7.9-.9 1-.2.2-.3.2-.6.1-.3-.1-1.2-.4-2.3-1.4-.8-.7-1.4-1.6-1.6-1.9-.2-.3 0-.5.1-.6l.4-.5c.1-.1.2-.3.2-.4.1-.1 0-.3 0-.4-.1-.1-.6-1.4-.8-1.9-.2-.5-.4-.4-.6-.4h-.5c-.2 0-.4.1-.6.3-.2.3-.8.8-.8 1.9 0 1.1.8 2.2.9 2.4.1.1 1.6 2.5 3.9 3.4.5.2 1 .4 1.3.5.5.2 1 .1 1.4.1.4-.1 1.3-.5 1.5-1 .2-.5.2-.9.1-1zM12 2a10 10 0 00-8.6 15L2 22l5.1-1.3A10 10 0 1012 2zm0 18.2c-1.5 0-3-.4-4.2-1.1l-.3-.2-3 .8.8-2.9-.2-.3a8.2 8.2 0 1114.7-4.9 8.2 8.2 0 01-7.8 8.6z"/></svg></a>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 LE NOIR Salon &amp; Grooming House.</span>
      <span>Precision. Patience. Presentation.</span>
    </div>
  </div>
</footer>

<script src="https://checkout.razorpay.com/v1/checkout.js"></script>
<script>
  // Sticky header
  const header = document.getElementById('site-header');
  window.addEventListener('scroll', () => {
    header.classList.toggle('scrolled', window.scrollY > 40);
  });

  // Mobile menu
  const menuToggle = document.getElementById('menuToggle');
  const navLinks = document.getElementById('navLinks');
  menuToggle.addEventListener('click', () => navLinks.classList.toggle('open'));
  navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

  // Testimonials
  const testimonials = [
    { quote: "I've had my hair cut in four cities. This is the first place that asked what I actually wanted before touching the clippers.", name: "Arjun R. — Regular since 2024" },
    { quote: "The hot shave alone is worth the visit. I leave feeling like I fixed something more than my face.", name: "Karthik M. — Member" },
    { quote: "Booked the Full House Package for my wedding morning. Calmest I've felt all week.", name: "Vishal S. — Client" }
  ];
  const tQuote = document.getElementById('tQuote');
  const tName = document.getElementById('tName');
  const dots = document.querySelectorAll('#tDots button');
  dots.forEach(btn => {
    btn.addEventListener('click', () => {
      const i = +btn.dataset.i;
      tQuote.textContent = testimonials[i].quote;
      tName.textContent = testimonials[i].name;
      dots.forEach(d => d.classList.remove('active'));
      btn.classList.add('active');
    });
  });

  // Booking + payment flow, backed by the LE NOIR Node.js service
  // (see the le-noir-backend project: create-order -> Razorpay Checkout ->
  // verify-payment). Update BACKEND_URL once your backend is deployed.
  const BACKEND_URL = 'https://api.yourdomain.com'; // <-- set this to your deployed backend

  const form = document.getElementById('bookingForm');
  const success = document.getElementById('formSuccess');
  const errorBox = document.getElementById('formError');
  const bookBtn = document.getElementById('bookBtn');

  function showError(msg) {
    errorBox.textContent = msg;
    errorBox.style.display = 'block';
  }

  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    errorBox.style.display = 'none';

    const name = document.getElementById('fname').value.trim();
    const phone = document.getElementById('fphone').value.trim();
    const serviceKey = document.getElementById('fservice').value;
    const date = document.getElementById('fdate').value;
    const time = document.getElementById('ftime').value;
    const notes = document.getElementById('fnotes').value.trim();

    if (!name || !phone || !serviceKey) {
      showError('Please fill in your name, phone number and choose a service.');
      return;
    }

    bookBtn.disabled = true;
    bookBtn.textContent = 'Processing…';

    try {
      // Step 1: ask the backend to create a Razorpay order at the
      // server-authoritative price for the chosen service.
      const orderRes = await fetch(`${BACKEND_URL}/api/bookings/create-order`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ name, phone, serviceKey, date, time, notes }),
      });
      const orderData = await orderRes.json();
      if (!orderRes.ok) throw new Error(orderData.error || 'Could not start payment.');

      // Step 2: open Razorpay's own hosted checkout — card/UPI/wallet details
      // are entered on Razorpay's page, never on this site or server.
      const rzp = new Razorpay({
        key: orderData.keyId,
        amount: orderData.amount,
        currency: orderData.currency,
        order_id: orderData.orderId,
        name: 'LE NOIR',
        description: 'Appointment booking',
        prefill: { name, contact: phone },
        theme: { color: '#c9a227' },
        handler: async function (response) {
          // Step 3: hand the payment id + signature to the backend, which
          // verifies them cryptographically before confirming the booking.
          try {
            const verifyRes = await fetch(`${BACKEND_URL}/api/bookings/verify-payment`, {
              method: 'POST',
              headers: { 'Content-Type': 'application/json' },
              body: JSON.stringify({
                razorpay_order_id: response.razorpay_order_id,
                razorpay_payment_id: response.razorpay_payment_id,
                razorpay_signature: response.razorpay_signature,
              }),
            });
            const verifyData = await verifyRes.json();
            if (!verifyRes.ok) throw new Error(verifyData.error || 'Payment verification failed.');

            form.style.display = 'none';
            success.style.display = 'block';
          } catch (err) {
            showError(err.message);
          } finally {
            bookBtn.disabled = false;
            bookBtn.textContent = 'Pay & Confirm Reservation';
          }
        },
        modal: {
          ondismiss: function () {
            bookBtn.disabled = false;
            bookBtn.textContent = 'Pay & Confirm Reservation';
          },
        },
      });

      rzp.on('payment.failed', function () {
        showError('Payment failed or was cancelled. Please try again.');
        bookBtn.disabled = false;
        bookBtn.textContent = 'Pay & Confirm Reservation';
      });

      rzp.open();
    } catch (err) {
      showError(err.message || 'Something went wrong. Please try again.');
      bookBtn.disabled = false;
      bookBtn.textContent = 'Pay & Confirm Reservation';
    }
  });
</script>

</body>
</html>
```

---

## 2. `backend/package.json`

```json
{
  "name": "le-noir-backend",
  "version": "1.0.0",
  "description": "Booking + payment + WhatsApp notification backend for LE NOIR salon website",
  "main": "server.js",
  "type": "commonjs",
  "scripts": {
    "start": "node server.js",
    "dev": "node --watch server.js"
  },
  "dependencies": {
    "better-sqlite3": "^11.3.0",
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.21.0",
    "express-rate-limit": "^7.4.0",
    "express-validator": "^7.2.0",
    "helmet": "^7.1.0",
    "morgan": "^1.10.0",
    "razorpay": "^2.9.4",
    "axios": "^1.7.7",
    "jsonwebtoken": "^9.0.2",
    "bcryptjs": "^2.4.3"
  }
}
```

---

## 3. `backend/.env.example` (copy to `.env` and fill with real values)

```bash
# ===== Server =====
PORT=4000
NODE_ENV=production
# Comma-separated list of domains allowed to call this API
ALLOWED_ORIGINS=https://www.yourdomain.com,https://yourdomain.com

# ===== Razorpay =====
# From https://dashboard.razorpay.com/app/keys — NEVER commit real values
RAZORPAY_KEY_ID=rzp_live_xxxxxxxxxxxx
RAZORPAY_KEY_SECRET=xxxxxxxxxxxxxxxxxxxxxxxx
# From Razorpay Dashboard > Settings > Webhooks (set a strong random secret there too)
RAZORPAY_WEBHOOK_SECRET=xxxxxxxxxxxxxxxxxxxxxxxx

# ===== Owner notification number =====
OWNER_WHATSAPP_NUMBER=919566031143

# ===== WhatsApp provider: "meta" or "twilio" =====
WHATSAPP_PROVIDER=meta

# --- Meta WhatsApp Cloud API (business.facebook.com) ---
WHATSAPP_TOKEN=your_meta_permanent_access_token
WHATSAPP_PHONE_NUMBER_ID=your_meta_phone_number_id
WHATSAPP_TEMPLATE_NAME=booking_confirmation
WHATSAPP_TEMPLATE_LANG=en

# --- Twilio WhatsApp (alternative, if WHATSAPP_PROVIDER=twilio) ---
TWILIO_ACCOUNT_SID=ACxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
TWILIO_AUTH_TOKEN=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
TWILIO_WHATSAPP_FROM=whatsapp:+14155238886

# ===== Admin dashboard login =====
# Generate a bcrypt hash for your chosen password (see README) — never store plaintext
ADMIN_USERNAME=owner
ADMIN_PASSWORD_HASH=$2a$10$replace_with_a_real_bcrypt_hash
JWT_SECRET=change_this_to_a_long_random_string
```

---

## 4. `backend/.gitignore`

```bash
node_modules/
.env
lenoir.db
lenoir.db-*
*.log
```

---

## 5. `backend/server.js`

```javascript
require('dotenv').config();
const express = require('express');
const helmet = require('helmet');
const cors = require('cors');
const morgan = require('morgan');
const rateLimit = require('express-rate-limit');

const bookingsRoutes = require('./src/routes/bookings');
const webhookRoutes = require('./src/routes/webhook');
const adminRoutes = require('./src/routes/admin');

// Fail fast and loud if critical secrets are missing, rather than silently
// running an insecure server.
const REQUIRED_ENV = [
  'RAZORPAY_KEY_ID',
  'RAZORPAY_KEY_SECRET',
  'RAZORPAY_WEBHOOK_SECRET',
  'JWT_SECRET',
  'ADMIN_PASSWORD_HASH',
];
const missing = REQUIRED_ENV.filter((k) => !process.env[k]);
if (missing.length) {
  console.error(`Missing required environment variables: ${missing.join(', ')}`);
  console.error('Copy .env.example to .env and fill in real values before starting.');
  process.exit(1);
}

const app = express();
app.set('trust proxy', 1); // needed for correct client IPs behind a reverse proxy (Nginx, etc.)

// ---- Security headers ----
app.use(
  helmet({
    contentSecurityPolicy: {
      directives: {
        defaultSrc: ["'self'"],
        scriptSrc: ["'self'", 'https://checkout.razorpay.com'],
        frameSrc: ["'self'", 'https://api.razorpay.com'],
        connectSrc: ["'self'", 'https://api.razorpay.com'],
        imgSrc: ["'self'", 'data:', 'https:'],
        styleSrc: ["'self'", "'unsafe-inline'", 'https://fonts.googleapis.com'],
        fontSrc: ["'self'", 'https://fonts.gstatic.com'],
      },
    },
    crossOriginEmbedderPolicy: false,
  })
);

// ---- CORS: only your real site domains may call this API ----
const allowedOrigins = (process.env.ALLOWED_ORIGINS || '').split(',').map((s) => s.trim()).filter(Boolean);
app.use(
  cors({
    origin(origin, callback) {
      if (!origin || allowedOrigins.includes(origin)) return callback(null, true);
      callback(new Error('Not allowed by CORS'));
    },
  })
);

app.use(morgan(process.env.NODE_ENV === 'production' ? 'combined' : 'dev'));

// Global rate limit as a backstop, in addition to the per-route limits below.
app.use(
  rateLimit({
    windowMs: 15 * 60 * 1000,
    max: 300,
    standardHeaders: true,
    legacyHeaders: false,
  })
);

// The Razorpay webhook needs the RAW request body for signature verification,
// so it's mounted BEFORE express.json() with its own raw parser.
app.use('/api/webhook', express.raw({ type: '*/*', limit: '1mb' }), webhookRoutes);

app.use(express.json({ limit: '100kb' })); // small limit — this API never needs large payloads

app.use('/api/bookings', bookingsRoutes);
app.use('/api/admin', adminRoutes);

app.get('/api/health', (req, res) => res.json({ ok: true }));

// Never leak stack traces or internals to clients.
app.use((err, req, res, next) => {
  console.error(err);
  if (err.message === 'Not allowed by CORS') {
    return res.status(403).json({ error: 'Origin not allowed' });
  }
  res.status(500).json({ error: 'Internal server error' });
});

const port = process.env.PORT || 4000;
app.listen(port, () => console.log(`LE NOIR backend listening on port ${port}`));
```

---

## 6. `backend/src/db.js`

```javascript
const Database = require('better-sqlite3');
const path = require('path');

const db = new Database(path.join(__dirname, '..', 'lenoir.db'));
db.pragma('journal_mode = WAL');

db.exec(`
  CREATE TABLE IF NOT EXISTS bookings (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    phone TEXT NOT NULL,
    service_key TEXT NOT NULL,
    service_name TEXT NOT NULL,
    amount_paise INTEGER NOT NULL,
    pref_date TEXT,
    pref_time TEXT,
    notes TEXT,
    status TEXT NOT NULL DEFAULT 'pending_payment',
    razorpay_order_id TEXT UNIQUE,
    razorpay_payment_id TEXT UNIQUE,
    created_at TEXT NOT NULL DEFAULT (datetime('now'))
  );

  CREATE INDEX IF NOT EXISTS idx_bookings_order ON bookings(razorpay_order_id);
  CREATE INDEX IF NOT EXISTS idx_bookings_payment ON bookings(razorpay_payment_id);
`);

// All access below uses parameterized/prepared statements — no string-concatenated
// SQL anywhere in this project, which is what prevents SQL injection.
module.exports = {
  raw: db,

  insertPendingBooking: db.prepare(`
    INSERT INTO bookings (name, phone, service_key, service_name, amount_paise, pref_date, pref_time, notes, status, razorpay_order_id)
    VALUES (@name, @phone, @service_key, @service_name, @amount_paise, @pref_date, @pref_time, @notes, 'pending_payment', @razorpay_order_id)
  `),

  getBookingByOrderId: db.prepare(`SELECT * FROM bookings WHERE razorpay_order_id = ?`),

  getBookingById: db.prepare(`SELECT * FROM bookings WHERE id = ?`),

  markPaid: db.prepare(`
    UPDATE bookings
    SET status = 'confirmed', razorpay_payment_id = ?
    WHERE razorpay_order_id = ? AND status != 'confirmed'
  `),

  listBookings: db.prepare(`SELECT * FROM bookings ORDER BY created_at DESC LIMIT 200`),
};
```

---

## 7. `backend/src/services/catalog.js`

```javascript
// SECURITY NOTE:
// Prices live here, on the server, ONLY. The frontend sends a "service key"
// (e.g. "haircut"), never an amount. If you priced things off whatever the
// browser sends, anyone could open devtools and "buy" a ₹1,500 package for ₹1.
// Every amount that goes to Razorpay is looked up from this table server-side.

const SERVICES = {
  haircut:    { name: 'Signature Haircut',        amountRupees: 500 },
  beard:      { name: 'Beard Grooming',           amountRupees: 400 },
  shave:      { name: 'Classic Hot Shave',        amountRupees: 300 },
  facial:     { name: 'Revitalising Facial',      amountRupees: 800 },
  massage:    { name: 'Signature Massage',        amountRupees: 600 },
  fullhouse:  { name: 'The Full House Package',   amountRupees: 1500 },
};

function getService(key) {
  const svc = SERVICES[key];
  if (!svc) return null;
  return { key, name: svc.name, amountPaise: svc.amountRupees * 100 };
}

module.exports = { SERVICES, getService };
```

---

## 8. `backend/src/services/razorpay.js`

```javascript
const Razorpay = require('razorpay');
const crypto = require('crypto');

const razorpay = new Razorpay({
  key_id: process.env.RAZORPAY_KEY_ID,
  key_secret: process.env.RAZORPAY_KEY_SECRET,
});

async function createOrder({ amountPaise, receipt, notes }) {
  return razorpay.orders.create({
    amount: amountPaise,
    currency: 'INR',
    receipt,
    notes,
  });
}

// Verifies the signature Razorpay's Checkout returns to the browser after payment.
// This is what stops someone from faking a "payment success" callback client-side.
function verifyPaymentSignature({ orderId, paymentId, signature }) {
  const expected = crypto
    .createHmac('sha256', process.env.RAZORPAY_KEY_SECRET)
    .update(`${orderId}|${paymentId}`)
    .digest('hex');
  return timingSafeEqual(expected, signature);
}

// Verifies webhooks sent server-to-server by Razorpay (belt-and-braces in case
// the browser tab is closed before the frontend can confirm the payment itself).
function verifyWebhookSignature({ rawBody, signature }) {
  const expected = crypto
    .createHmac('sha256', process.env.RAZORPAY_WEBHOOK_SECRET)
    .update(rawBody)
    .digest('hex');
  return timingSafeEqual(expected, signature);
}

function timingSafeEqual(a, b) {
  const bufA = Buffer.from(a || '', 'utf8');
  const bufB = Buffer.from(b || '', 'utf8');
  if (bufA.length !== bufB.length) return false;
  return crypto.timingSafeEqual(bufA, bufB);
}

module.exports = { razorpay, createOrder, verifyPaymentSignature, verifyWebhookSignature };
```

---

## 9. `backend/src/services/whatsapp.js`

```javascript
const axios = require('axios');

// IMPORTANT REAL-WORLD LIMITATION (read this before you assume messages will
// "just work"):
// WhatsApp's Business Platform does not let a business send free-form
// messages to a customer out of the blue. A business-initiated message
// (like a booking confirmation) MUST use a pre-approved message TEMPLATE,
// unless the customer messaged you first within the last 24 hours. This is
// a WhatsApp policy, not a limitation of this code — it exists to stop
// businesses from spamming people, and there's no way to route around it.
//
// To make the code below actually deliver messages you need to:
//  1. Set up a WhatsApp Business Platform account (Meta) or a Twilio WhatsApp
//     sender, and verify the OWNER_WHATSAPP_NUMBER as your business number.
//  2. Get a message template approved (e.g. "booking_confirmation" with
//     variables for name/service/date/time) — approval usually takes a few
//     hours to a day.
//  3. Put the resulting credentials in .env (see .env.example).
// Until that's done, sendBookingWhatsApp() will throw/log a clear error
// instead of silently pretending to have sent something.

async function sendBookingWhatsApp({ toCustomerPhone, booking }) {
  const provider = process.env.WHATSAPP_PROVIDER || 'meta';
  const ownerPhone = process.env.OWNER_WHATSAPP_NUMBER; // 919566031143

  const customerText =
    `Hi ${booking.name}, your appointment at LE NOIR is confirmed.\n` +
    `Service: ${booking.service_name}\n` +
    `Date/Time: ${booking.pref_date || 'TBC'} ${booking.pref_time || ''}\n` +
    `Amount paid: Rs.${(booking.amount_paise / 100).toFixed(0)}\n` +
    `See you soon!`;

  const ownerText =
    `New paid booking received.\n` +
    `Customer: ${booking.name} (${booking.phone})\n` +
    `Service: ${booking.service_name}\n` +
    `Date/Time: ${booking.pref_date || 'TBC'} ${booking.pref_time || ''}\n` +
    `Amount: Rs.${(booking.amount_paise / 100).toFixed(0)}\n` +
    `Notes: ${booking.notes || '-'}`;

  if (provider === 'twilio') {
    await Promise.all([
      sendViaTwilio(toCustomerPhone, customerText),
      sendViaTwilio(ownerPhone, ownerText),
    ]);
    return;
  }

  // Default: Meta WhatsApp Cloud API, using an approved template for the
  // business-initiated customer message, and a plain text message to the
  // owner's number (fine, since a plain "utility" text to your own verified
  // number is commonly allowed within your own tested/opted-in number set —
  // check current Meta policy for your account before relying on this).
  await Promise.all([
    sendViaMetaTemplate(toCustomerPhone, booking),
    sendViaMetaText(ownerPhone, ownerText),
  ]);
}

async function sendViaMetaTemplate(toPhone, booking) {
  const url = `https://graph.facebook.com/v20.0/${process.env.WHATSAPP_PHONE_NUMBER_ID}/messages`;
  const payload = {
    messaging_product: 'whatsapp',
    to: toPhone,
    type: 'template',
    template: {
      name: process.env.WHATSAPP_TEMPLATE_NAME || 'booking_confirmation',
      language: { code: process.env.WHATSAPP_TEMPLATE_LANG || 'en' },
      components: [
        {
          type: 'body',
          parameters: [
            { type: 'text', text: booking.name },
            { type: 'text', text: booking.service_name },
            { type: 'text', text: `${booking.pref_date || 'TBC'} ${booking.pref_time || ''}`.trim() },
          ],
        },
      ],
    },
  };
  return callMeta(url, payload);
}

async function sendViaMetaText(toPhone, text) {
  const url = `https://graph.facebook.com/v20.0/${process.env.WHATSAPP_PHONE_NUMBER_ID}/messages`;
  const payload = {
    messaging_product: 'whatsapp',
    to: toPhone,
    type: 'text',
    text: { body: text },
  };
  return callMeta(url, payload);
}

async function callMeta(url, payload) {
  try {
    await axios.post(url, payload, {
      headers: {
        Authorization: `Bearer ${process.env.WHATSAPP_TOKEN}`,
        'Content-Type': 'application/json',
      },
      timeout: 10000,
    });
  } catch (err) {
    // Never let a notification failure break the booking itself — the payment
    // already succeeded, so we log and move on rather than throwing.
    console.error('WhatsApp (Meta) send failed:', err.response?.data || err.message);
  }
}

async function sendViaTwilio(toPhone, text) {
  const sid = process.env.TWILIO_ACCOUNT_SID;
  const token = process.env.TWILIO_AUTH_TOKEN;
  const from = process.env.TWILIO_WHATSAPP_FROM;
  const url = `https://api.twilio.com/2010-04-01/Accounts/${sid}/Messages.json`;

  try {
    await axios.post(
      url,
      new URLSearchParams({
        From: from,
        To: `whatsapp:+${toPhone}`,
        Body: text,
      }),
      { auth: { username: sid, password: token }, timeout: 10000 }
    );
  } catch (err) {
    console.error('WhatsApp (Twilio) send failed:', err.response?.data || err.message);
  }
}

module.exports = { sendBookingWhatsApp };
```

---

## 10. `backend/src/routes/bookings.js`

```javascript
const express = require('express');
const rateLimit = require('express-rate-limit');
const { body, validationResult } = require('express-validator');

const db = require('../db');
const { getService, SERVICES } = require('../services/catalog');
const { createOrder, verifyPaymentSignature } = require('../services/razorpay');
const { sendBookingWhatsApp } = require('../services/whatsapp');

const router = express.Router();

// Throttle booking creation hard — this is the endpoint most worth abusing
// (order-creation spam, scraping, brute forcing). 20 requests / 15 min / IP.
const createOrderLimiter = rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 20,
  standardHeaders: true,
  legacyHeaders: false,
  message: { error: 'Too many requests, please try again later.' },
});

const verifyLimiter = rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 30,
  standardHeaders: true,
  legacyHeaders: false,
});

// Basic Indian mobile number check; adjust if you take international clients.
const phoneRule = body('phone')
  .trim()
  .matches(/^\+?[0-9]{10,13}$/)
  .withMessage('Enter a valid phone number');

// STEP 1: create a Razorpay order for the (server-priced) service the
// customer picked, and store a "pending_payment" booking row.
router.post(
  '/create-order',
  createOrderLimiter,
  [
    body('name').trim().isLength({ min: 2, max: 80 }).escape(),
    phoneRule,
    body('serviceKey').trim().isIn(Object.keys(SERVICES)).withMessage('Invalid service selected'),
    body('date').optional({ checkFalsy: true }).isISO8601(),
    body('time').optional({ checkFalsy: true }).matches(/^\d{2}:\d{2}$/),
    body('notes').optional({ checkFalsy: true }).trim().isLength({ max: 500 }).escape(),
  ],
  async (req, res) => {
    const errors = validationResult(req);
    if (!errors.isEmpty()) {
      return res.status(400).json({ error: errors.array()[0].msg });
    }

    const { name, phone, serviceKey, date, time, notes } = req.body;
    const service = getService(serviceKey);
    if (!service) return res.status(400).json({ error: 'Invalid service' });

    try {
      const receipt = `lenoir_${Date.now()}`;
      const order = await createOrder({
        amountPaise: service.amountPaise,
        receipt,
        notes: { service: service.name, phone },
      });

      db.insertPendingBooking.run({
        name,
        phone,
        service_key: service.key,
        service_name: service.name,
        amount_paise: service.amountPaise,
        pref_date: date || null,
        pref_time: time || null,
        notes: notes || null,
        razorpay_order_id: order.id,
      });

      res.json({
        orderId: order.id,
        amount: order.amount,
        currency: order.currency,
        keyId: process.env.RAZORPAY_KEY_ID, // publishable key — safe to expose
      });
    } catch (err) {
      console.error('create-order failed:', err);
      res.status(502).json({ error: 'Could not initiate payment. Please try again.' });
    }
  }
);

// STEP 2: browser calls this after Razorpay Checkout succeeds, with the
// payment id + signature Razorpay handed back. We NEVER trust "payment
// succeeded" from the client alone — the signature is cryptographically
// verified against your key secret before anything is marked paid.
router.post(
  '/verify-payment',
  verifyLimiter,
  [
    body('razorpay_order_id').trim().notEmpty(),
    body('razorpay_payment_id').trim().notEmpty(),
    body('razorpay_signature').trim().notEmpty(),
  ],
  async (req, res) => {
    const errors = validationResult(req);
    if (!errors.isEmpty()) return res.status(400).json({ error: 'Missing payment fields' });

    const { razorpay_order_id, razorpay_payment_id, razorpay_signature } = req.body;

    const valid = verifyPaymentSignature({
      orderId: razorpay_order_id,
      paymentId: razorpay_payment_id,
      signature: razorpay_signature,
    });

    if (!valid) {
      console.warn('Signature mismatch on verify-payment — possible tampering attempt.');
      return res.status(400).json({ error: 'Payment verification failed' });
    }

    const booking = db.getBookingByOrderId.get(razorpay_order_id);
    if (!booking) return res.status(404).json({ error: 'Booking not found' });

    db.markPaid.run(razorpay_payment_id, razorpay_order_id);
    const updated = db.getBookingById.get(booking.id);

    // Fire WhatsApp notifications — failures here never block the response,
    // since the payment itself already succeeded.
    sendBookingWhatsApp({ toCustomerPhone: updated.phone, booking: updated }).catch(() => {});

    res.json({ ok: true, bookingId: updated.id, status: updated.status });
  }
);

module.exports = router;
```

---

## 11. `backend/src/routes/webhook.js`

```javascript
const express = require('express');
const db = require('../db');
const { verifyWebhookSignature } = require('../services/razorpay');
const { sendBookingWhatsApp } = require('../services/whatsapp');

const router = express.Router();

// This route is mounted with express.raw() in server.js (NOT express.json())
// because signature verification must run against the exact raw bytes
// Razorpay sent — re-serialized JSON will not match the signature and this
// is a common way people accidentally break webhook security.
router.post('/razorpay', (req, res) => {
  const signature = req.headers['x-razorpay-signature'];
  const valid = verifyWebhookSignature({ rawBody: req.body, signature });

  if (!valid) {
    console.warn('Rejected webhook with invalid signature.');
    return res.status(400).send('Invalid signature');
  }

  const event = JSON.parse(req.body.toString('utf8'));

  if (event.event === 'payment.captured') {
    const payment = event.payload.payment.entity;
    const booking = db.getBookingByOrderId.get(payment.order_id);
    if (booking && booking.status !== 'confirmed') {
      db.markPaid.run(payment.id, payment.order_id);
      const updated = db.getBookingById.get(booking.id);
      sendBookingWhatsApp({ toCustomerPhone: updated.phone, booking: updated }).catch(() => {});
    }
  }

  // Always 200 quickly so Razorpay doesn't retry-storm the endpoint.
  res.status(200).send('ok');
});

module.exports = router;
```

---

## 12. `backend/src/routes/admin.js`

```javascript
const express = require('express');
const jwt = require('jsonwebtoken');
const bcrypt = require('bcryptjs');
const rateLimit = require('express-rate-limit');
const db = require('../db');

const router = express.Router();

const loginLimiter = rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 10, // slow down brute-forcing the admin password
  standardHeaders: true,
  legacyHeaders: false,
});

router.post('/login', loginLimiter, async (req, res) => {
  const { username, password } = req.body || {};
  if (
    !username ||
    !password ||
    username !== process.env.ADMIN_USERNAME ||
    !(await bcrypt.compare(password, process.env.ADMIN_PASSWORD_HASH || ''))
  ) {
    // Same generic error either way — never reveal whether the username or
    // password was the wrong part.
    return res.status(401).json({ error: 'Invalid credentials' });
  }

  const token = jwt.sign({ role: 'admin' }, process.env.JWT_SECRET, { expiresIn: '12h' });
  res.json({ token });
});

function requireAdmin(req, res, next) {
  const header = req.headers.authorization || '';
  const token = header.startsWith('Bearer ') ? header.slice(7) : null;
  if (!token) return res.status(401).json({ error: 'Missing token' });

  try {
    jwt.verify(token, process.env.JWT_SECRET);
    next();
  } catch {
    res.status(401).json({ error: 'Invalid or expired token' });
  }
}

router.get('/bookings', requireAdmin, (req, res) => {
  res.json(db.listBookings.all());
});

module.exports = router;
```

---

## 13. `backend/README.md` (full setup guide)

```markdown
# LE NOIR — Booking, Payment & WhatsApp Backend

Real Node.js/Express backend for the LE NOIR site: Razorpay payments, a
SQLite booking store, and WhatsApp notifications to the customer and the
owner (`9566031143`) once a booking is paid for.

## 1. Install

```bash
npm install
cp .env.example .env
```

Fill in `.env` with real values (see below). **Never commit `.env`.**

## 2. Razorpay setup

1. Create/log into your Razorpay account → Dashboard → Settings → API Keys.
   Generate a Key Id + Key Secret. Put them in `RAZORPAY_KEY_ID` / `RAZORPAY_KEY_SECRET`.
2. Dashboard → Settings → Webhooks → Add a webhook pointing to
   `https://yourdomain.com/api/webhook/razorpay`, subscribe to `payment.captured`,
   and set a webhook secret — put that in `RAZORPAY_WEBHOOK_SECRET`.
3. Start in Test Mode first (`rzp_test_...` keys) and use Razorpay's test
   cards before switching to live keys.

## 3. WhatsApp setup (read this — there's no way around it)

WhatsApp will not let a business send an unprompted "your booking is
confirmed" message as free text. Business-initiated messages must use a
**pre-approved template**. Two ways to get set up:

**Option A — Meta WhatsApp Cloud API (recommended, official, free tier)**
1. Create a Meta Business account and a WhatsApp Business Platform app at
   business.facebook.com.
2. Add and verify your business phone number.
3. In WhatsApp Manager, create a message template (e.g. `booking_confirmation`)
   with body text like:
   `Hi {{1}}, your appointment for {{2}} is confirmed for {{3}}. See you at LE NOIR!`
   Submit it for approval (usually hours, sometimes up to a day).
4. Generate a permanent access token and copy your Phone Number ID.
5. Set `WHATSAPP_PROVIDER=meta`, `WHATSAPP_TOKEN`, `WHATSAPP_PHONE_NUMBER_ID`,
   `WHATSAPP_TEMPLATE_NAME` in `.env`.

**Option B — Twilio WhatsApp**
Simpler to prototype with (Twilio's sandbox lets you test quickly), but the
same "approved template for business-initiated messages" rule applies once
you go to production with your own number. Set `WHATSAPP_PROVIDER=twilio`
and the `TWILIO_*` variables.

The owner number `9566031143` goes in `OWNER_WHATSAPP_NUMBER=919566031143`
(with country code, no `+`, no spaces).

Until templates are approved, the code logs a clear error instead of
pretending a message was sent — check your server logs.

## 4. Admin login

Generate a bcrypt hash for whatever password you want to log into `/api/admin`
with:

```bash
node -e "console.log(require('bcryptjs').hashSync('your-real-password', 10))"
```

Put the output in `ADMIN_PASSWORD_HASH`. Set `JWT_SECRET` to a long random
string (e.g. `openssl rand -hex 32`).

`POST /api/admin/login` with `{ "username": "...", "password": "..." }`
returns a JWT. Use it as `Authorization: Bearer <token>` on
`GET /api/admin/bookings` to see all bookings.

## 5. Run it

```bash
npm start
```

The server refuses to start if any required secret is missing, so you can't
accidentally run it half-configured.

## 6. Deploy it securely

- **Always run behind HTTPS.** Put this behind Nginx/Caddy with a free
  Let's Encrypt certificate, or behind a platform (Render, Railway, Fly.io)
  that terminates TLS for you. Razorpay Checkout requires HTTPS in production.
- **Set `ALLOWED_ORIGINS`** to your real domain(s) only — this is what stops
  another website from calling your booking API from a stranger's browser.
- Keep `.env` out of git (already in `.gitignore`) and out of any public
  hosting bucket.
- Consider putting the whole API behind a Web Application Firewall /
  Cloudflare proxy for extra protection against scraping and DDoS — this
  backend's own rate limits are a floor, not a ceiling.
- Back up `lenoir.db` regularly if you rely on it as your booking record.

## What's already hardened in the code

- **No trusting client-sent prices.** The browser only ever sends a service
  *key*; the amount charged is looked up server-side (`src/services/catalog.js`).
- **Cryptographic payment verification.** A payment is only marked "confirmed"
  after its Razorpay signature is verified with HMAC-SHA256 against your key
  secret (`src/services/razorpay.js`) — a fake "success" from a tampered
  browser request is rejected.
- **Webhook signature verification** on the raw request body, as a second,
  independent confirmation path.
- **SQL injection isn't possible** — every query is a prepared statement
  (`src/db.js`); nothing is string-concatenated into SQL.
- **Input validation** on every field (`express-validator`), with length caps
  and HTML-escaping on free-text fields.
- **Rate limiting** on booking creation, payment verification, and admin
  login, to blunt brute-force and spam.
- **Helmet** security headers + a Content-Security-Policy that only allows
  Razorpay's own domains to load/run.
- **CORS locked to your domain(s)** — no wildcard origin.
- **Admin routes require a JWT**; the password is stored as a bcrypt hash,
  never plaintext, and login attempts are rate-limited.
- **No stack traces or internals ever reach the client** — errors are logged
  server-side and a generic message is returned.

No backend can promise to be "unhackable" — the points above cover the
common, concrete risks for a site like this (price tampering, fake payment
confirmations, SQL injection, brute force, and leaking secrets/errors). Keep
dependencies updated (`npm audit`) and don't skip the HTTPS step.
```

---

