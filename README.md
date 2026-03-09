<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BrightSmile Dental | professional multi-page website</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    }

    body {
      background: #ffffff;
      color: #1b2f3c;
      line-height: 1.5;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 32px;
    }

    /* header (same on all pages) */
    .header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 0;
      flex-wrap: wrap;
      border-bottom: 2px solid #e0f0ef;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 2rem;
      font-weight: 700;
      color: #0a6e6b;
    }

    .logo i {
      background: #dcf2f1;
      padding: 10px;
      border-radius: 20px;
    }

    .nav-links {
      display: flex;
      gap: 32px;
      font-weight: 500;
      align-items: center;
      flex-wrap: wrap;
    }

    .nav-links a {
      text-decoration: none;
      color: #1e4a5c;
      transition: 0.2s;
      font-size: 1.05rem;
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: #0a6e6b;
      font-weight: 600;
    }

    .btn-header {
      background: #0a6e6b;
      color: white !important;
      padding: 10px 26px;
      border-radius: 40px;
      font-weight: 600;
    }

    .btn-header:hover {
      background: #0d8884;
    }

    /* footer (same on all pages) */
    .footer {
      background: #effaf8;
      border-radius: 48px 48px 0 0;
      padding: 56px 0 24px;
      margin-top: 70px;
    }

    .footer-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 40px;
    }

    .footer-col p {
      max-width: 280px;
      color: #2a5a6b;
      margin: 16px 0 20px;
    }

    .footer-links {
      display: flex;
      gap: 70px;
      flex-wrap: wrap;
    }

    .footer-links a {
      display: block;
      color: #2a5a6b;
      text-decoration: none;
      margin-bottom: 12px;
    }

    .footer-links a:hover {
      color: #0a6e6b;
    }

    .social-icons {
      display: flex;
      gap: 28px;
      font-size: 1.9rem;
      margin-top: 16px;
    }

    .social-icons a {
      color: #0a6e6b;
    }

    .copyright {
      text-align: center;
      padding: 32px 0 0;
      color: #578494;
      border-top: 1px solid #c0e2df;
      margin-top: 48px;
    }

    /* buttons */
    .btn {
      background: #0a6e6b;
      color: white;
      padding: 14px 38px;
      border-radius: 60px;
      font-weight: 600;
      font-size: 1.1rem;
      border: none;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      box-shadow: 0 10px 20px rgba(10,110,107,0.25);
      transition: 0.2s;
    }

    .btn-outline {
      background: transparent;
      border: 2px solid #0a6e6b;
      color: #0a6e6b;
      box-shadow: none;
    }

    .btn-outline:hover {
      background: #e0f4f2;
    }

    /* active page detection */
    .active-page {
      font-weight: 700;
      color: #0a6e6b !important;
      border-bottom: 3px solid #f3b33d;
    }

    /* homepage components */
    .hero {
      display: flex;
      align-items: center;
      gap: 50px;
      padding: 50px 0 40px;
      flex-wrap: wrap;
    }

    .hero-content {
      flex: 1 1 380px;
    }

    .hero-content h1 {
      font-size: 3.5rem;
      font-weight: 800;
      line-height: 1.2;
      color: #14313e;
    }

    .hero-content h1 span {
      color: #0a6e6b;
      border-bottom: 5px solid #f3b33d;
    }

    .hero-content p {
      font-size: 1.25rem;
      color: #2a5a6b;
      margin: 24px 0 32px;
    }

    .hero-gallery {
      flex: 1 1 380px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }

    .gallery-item {
      background: #dcf2f1;
      border-radius: 40px;
      padding: 24px 16px;
      text-align: center;
      box-shadow: 0 18px 25px -10px rgba(10,110,107,0.3);
    }

    .gallery-item i {
      font-size: 5rem;
      color: #0a6e6b;
    }

    .gallery-item.large {
      grid-column: span 2;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 20px;
      background: #c3eae8;
    }

    .gallery-item.large i {
      font-size: 4rem;
    }

    /* services section homepage */
    .section-header {
      text-align: center;
      margin: 70px 0 40px;
    }

    .section-header h2 {
      font-size: 2.8rem;
      color: #12343e;
    }

    .section-header p {
      color: #346978;
      font-size: 1.2rem;
      max-width: 700px;
      margin: 12px auto 0;
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 28px;
    }

    .service-card {
      background: white;
      border-radius: 40px;
      padding: 38px 24px;
      text-align: center;
      box-shadow: 0 12px 28px -10px rgba(10,110,107,0.1);
      border: 1px solid #d2eeed;
      transition: 0.2s;
    }

    .service-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 25px 35px -12px #0a6e6b40;
    }

    .service-card i {
      font-size: 3.2rem;
      background: #dcf2f1;
      padding: 18px;
      border-radius: 34px;
      color: #0a6e6b;
      margin-bottom: 22px;
    }

    /* about + image row */
    .about-row {
      display: flex;
      gap: 50px;
      margin: 70px 0;
      align-items: center;
      flex-wrap: wrap;
    }

    .about-text {
      flex: 1 1 350px;
    }

    .about-text h3 {
      font-size: 2.4rem;
      color: #12343e;
    }

    .about-text p {
      color: #2a5a6b;
      font-size: 1.1rem;
      margin: 20px 0 30px;
    }

    .about-highlight {
      display: flex;
      gap: 25px;
      margin-top: 25px;
    }

    .about-highlight div {
      background: #e5f6f5;
      border-radius: 40px;
      padding: 18px 26px;
      font-weight: 600;
    }

    .about-images {
      flex: 1 1 350px;
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .about-images img {
      width: 160px;
      height: 160px;
      object-fit: cover;
      border-radius: 40px;
      background: #b7dfdd;
      box-shadow: 0 18px 25px -10px #0a6e6b;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      color: #0a6e6b;
    }

    .img-placeholder {
      background: #b7dfdd;
      width: 160px;
      height: 160px;
      border-radius: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      color: #0a6e6b;
      font-weight: 600;
    }

    /* stats bar */
    .stats-bar {
      background: #0a6e6b;
      color: white;
      border-radius: 80px;
      padding: 48px 40px;
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      gap: 30px;
      margin: 60px 0;
    }

    .stat-item {
      text-align: center;
    }

    .stat-number {
      font-size: 3rem;
      font-weight: 800;
      line-height: 1.2;
    }

    .stat-label {
      font-size: 1.2rem;
      opacity: 0.9;
    }

    /* testimonials */
    .testimonial-grid {
      display: flex;
      gap: 30px;
      flex-wrap: wrap;
      margin: 50px 0;
    }

    .testimonial-card {
      background: #f4fcfb;
      border-radius: 40px;
      padding: 36px 28px;
      flex: 1 1 280px;
      border: 1px solid #bae3e1;
      box-shadow: 0 12px 18px -8px rgba(0,90,90,0.1);
    }

    .testimonial-card i {
      color: #f3b33d;
      font-size: 2.2rem;
      margin-bottom: 16px;
    }

    .testimonial-card p {
      font-style: italic;
      color: #1b4a5a;
      margin-bottom: 20px;
    }

    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .testimonial-author .avatar {
      width: 56px;
      height: 56px;
      background: #b7dfdd;
      border-radius: 30px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #0a6e6b;
      font-weight: bold;
      font-size: 1.6rem;
    }

    /* insurance / partners */
    .insurance-row {
      display: flex;
      align-items: center;
      justify-content: space-around;
      background: #e6f4f3;
      border-radius: 80px;
      padding: 38px 32px;
      flex-wrap: wrap;
      gap: 30px;
      margin: 60px 0;
    }

    .insurance-item {
      font-size: 1.8rem;
      font-weight: 600;
      color: #0a6e6b;
    }

    .insurance-item i {
      margin-right: 10px;
      background: white;
      padding: 12px;
      border-radius: 50%;
    }

    /* contact section on homepage */
    .home-contact {
      display: flex;
      gap: 40px;
      background: #f0f9f8;
      border-radius: 70px;
      padding: 48px 48px;
      margin: 60px 0;
      flex-wrap: wrap;
      align-items: center;
    }

    .home-contact .info {
      flex: 1 1 280px;
    }

    .home-contact .info h3 {
      font-size: 2.2rem;
      color: #12343e;
    }

    .home-contact .info p {
      margin: 16px 0;
      color: #1e5b6b;
      font-size: 1.1rem;
    }

    .home-contact .contact-form-simple {
      flex: 2 1 360px;
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
    }

    .contact-form-simple input {
      flex: 1 1 200px;
      padding: 18px 24px;
      border: none;
      border-radius: 60px;
      font-size: 1rem;
      background: white;
    }

    .contact-form-simple button {
      padding: 18px 36px;
      border-radius: 60px;
      border: none;
      background: #0a6e6b;
      color: white;
      font-weight: 700;
      cursor: pointer;
    }

    /* other pages styling (services, team, contact, book) */
    .cards-grid, .team-grid, .booking-card, .contact-row {
      margin: 40px 0;
    }

    .service-card-full, .team-member, .contact-info, .contact-form {
      background: #f9fdfe;
      border-radius: 40px;
      padding: 30px;
      border: 1px solid #cdebea;
    }

    /* responsive */
    @media (max-width: 700px) {
      .header {
        flex-direction: column;
        gap: 16px;
      }
      .hero-content h1 {
        font-size: 2.7rem;
      }
    }

    /* page visibility */
    .page { display: none; }
    .page.active-page-content { display: block; }
  </style>
</head>
<body>

  <!-- ========== HEADER ========== -->
  <div class="container">
    <div class="header">
      <div class="logo">
        <i class="fas fa-tooth"></i>
        <span>BrightSmile</span>
      </div>
      <div class="nav-links">
        <a href="#home" class="page-link" data-page="home">Home</a>
        <a href="#services" class="page-link" data-page="services">Services</a>
        <a href="#team" class="page-link" data-page="team">Our Team</a>
        <a href="#contact" class="page-link" data-page="contact">Contact</a>
        <a href="#book" class="page-link btn-header" data-page="book">Book online</a>
      </div>
    </div>
  </div>

  <!-- ========== PAGE CONTAINER ========== -->
  <div class="container" id="page-content">
    <!-- HOMEPAGE (detailed) -->
    <div id="home-page" class="page active-page-content">
      <!-- hero with images -->
      <div class="hero">
        <div class="hero-content">
          <h1>Where <span>healthy smiles</span> begin</h1>
          <p>Experience modern, gentle dentistry in a warm and friendly environment. Your comfort is our priority.</p>
          <div>
            <a href="#book" class="btn" style="margin-right:16px;">Book now</a>
            <a href="#services" class="btn btn-outline">Explore services</a>
          </div>
        </div>
        <div class="hero-gallery">
          <div class="gallery-item"><i class="fas fa-tooth"></i><br> Preventive</div>
          <div class="gallery-item"><i class="fas fa-crown"></i><br> Crowns</div>
          <div class="gallery-item large"><i class="fas fa-teeth"></i> <span style="font-weight:600;">Advanced technology</span></div>
        </div>
      </div>

      <!-- stats bar -->
      <div class="stats-bar">
        <div class="stat-item"><span class="stat-number">15+</span> <div class="stat-label">years experience</div></div>
        <div class="stat-item"><span class="stat-number">8.5k+</span> <div class="stat-label">happy patients</div></div>
        <div class="stat-item"><span class="stat-number">4.9★</span> <div class="stat-label">google rating</div></div>
        <div class="stat-item"><span class="stat-number">24/7</span> <div class="stat-label">emergency care</div></div>
      </div>

      <!-- services preview -->
      <div class="section-header">
        <h2>Our dental services</h2>
        <p>Comprehensive care for the whole family, from prevention to restoration.</p>
      </div>
      <div class="service-grid">
        <div class="service-card"><i class="fas fa-tooth"></i><h3>Checkups</h3><p>Regular exams & cleanings</p></div>
        <div class="service-card"><i class="fas fa-brush"></i><h3>Whitening</h3><p>Professional smile brightening</p></div>
        <div class="service-card"><i class="fas fa-crown"></i><h3>Crowns & bridges</h3><p>Restore damaged teeth</p></div>
        <div class="service-card"><i class="fas fa-child"></i><h3>Pediatric care</h3><p>Gentle, fun visits</p></div>
      </div>

      <!-- about + images -->
      <div class="about-row">
        <div class="about-text">
          <h3>Advanced & comfortable dentistry</h3>
          <p>We combine expertise with modern technology to give you the best care. Digital scanners, laser dentistry, and sedation options for a stress‑free experience.</p>
          <div class="about-highlight">
            <div><i class="fas fa-laptop"></i> Digital impressions</div>
            <div><i class="fas fa-shield-alt"></i> Sterile safety</div>
          </div>
        </div>
        <div class="about-images">
          <div class="img-placeholder"><i class="fas fa-x-ray"></i></div>
          <div class="img-placeholder"><i class="fas fa-user-md"></i></div>
          <div class="img-placeholder"><i class="fas fa-teeth-open"></i></div>
          <div class="img-placeholder"><i class="fas fa-laugh-beam"></i></div>
        </div>
      </div>

      <!-- testimonials section -->
      <div class="section-header">
        <h2>What our patients say</h2>
        <p>Real stories from happy smiles</p>
      </div>
      <div class="testimonial-grid">
        <div class="testimonial-card">
          <i class="fas fa-quote-left"></i>
          <p>Finally a dentist I actually look forward to visiting! The team is so caring and gentle.</p>
          <div class="testimonial-author">
            <div class="avatar">LK</div> <div><strong>Linda K.</strong> ⭐⭐⭐⭐⭐</div>
          </div>
        </div>
        <div class="testimonial-card">
          <i class="fas fa-quote-left"></i>
          <p>My kids love coming here – they call it the happy tooth place. Thank you, Dr. Sarah!</p>
          <div class="testimonial-author">
            <div class="avatar">MP</div> <div><strong>Mike P.</strong> ⭐⭐⭐⭐⭐</div>
          </div>
        </div>
        <div class="testimonial-card">
          <i class="fas fa-quote-left"></i>
          <p>Quick, painless and very professional. The new crown feels perfect. Highly recommended.</p>
          <div class="testimonial-author">
            <div class="avatar">DR</div> <div><strong>Diana R.</strong> ⭐⭐⭐⭐⭐</div>
          </div>
        </div>
      </div>

      <!-- insurance & payment -->
      <div class="insurance-row">
        <div class="insurance-item"><i class="fas fa-building"></i> Delta Dental</div>
        <div class="insurance-item"><i class="fas fa-heartbeat"></i> Cigna</div>
        <div class="insurance-item"><i class="fas fa-truck"></i> Aetna</div>
        <div class="insurance-item"><i class="fas fa-credit-card"></i> MetLife</div>
        <div class="insurance-item"><i class="fas fa-shield"></i> UnitedHealthcare</div>
      </div>

      <!-- contact section right on homepage -->
      <div class="home-contact">
        <div class="info">
          <h3>Have questions? Contact us</h3>
          <p><i class="fas fa-phone-alt" style="margin-right:10px;"></i>(212) 555 0149</p>
          <p><i class="fas fa-map-pin" style="margin-right:10px;"></i>123 Main Street, NY</p>
          <div class="social-icons" style="margin-top:0;">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-x-twitter"></i></a>
          </div>
        </div>
        <div class="contact-form-simple">
          <input type="text" placeholder="Your name">
          <input type="email" placeholder="Email address">
          <button>Send</button>
        </div>
      </div>
    </div>

    <!-- SERVICES PAGE (simplified but present) -->
    <div id="services-page" class="page">
      <div class="section-header"><h2>Our dental services</h2><p>Comprehensive treatments for all ages</p></div>
      <div class="service-grid">
        <div class="service-card"><i class="fas fa-tooth"></i><h3>Preventive care</h3><p>Cleanings, exams, fluoride</p></div>
        <div class="service-card"><i class="fas fa-brush"></i><h3>Cosmetic</h3><p>Whitening, veneers, bonding</p></div>
        <div class="service-card"><i class="fas fa-crown"></i><h3>Restorative</h3><p>Crowns, bridges, implants</p></div>
        <div class="service-card"><i class="fas fa-baby"></i><h3>Pediatric</h3><p>Gentle care for kids</p></div>
        <div class="service-card"><i class="fas fa-teeth"></i><h3>Orthodontics</h3><p>Braces & clear aligners</p></div>
        <div class="service-card"><i class="fas fa-clock"></i><h3>Emergency</h3><p>Same-day visits</p></div>
      </div>
    </div>

    <!-- TEAM PAGE -->
    <div id="team-page" class="page">
      <div class="section-header"><h2>Your smile specialists</h2><p>Experienced & compassionate</p></div>
      <div class="team-grid" style="display:flex; gap:30px; flex-wrap:wrap; justify-content:center;">
        <div class="team-member" style="background:#f9fdfe; border-radius:40px; padding:36px 26px; flex:1 1 200px; text-align:center;"><i class="fas fa-user-md" style="font-size:4rem; background:#dcf2f1; padding:22px; border-radius:50%;"></i><h4>Dr. Emily Chen</h4><div style="color:#0a6e6b;">orthodontist</div></div>
        <div class="team-member" style="background:#f9fdfe; border-radius:40px; padding:36px 26px; flex:1 1 200px; text-align:center;"><i class="fas fa-user-nurse" style="font-size:4rem; background:#dcf2f1; padding:22px; border-radius:50%;"></i><h4>Dr. Marcus Velez</h4><div style="color:#0a6e6b;">implantologist</div></div>
        <div class="team-member" style="background:#f9fdfe; border-radius:40px; padding:36px 26px; flex:1 1 200px; text-align:center;"><i class="fas fa-child" style="font-size:4rem; background:#dcf2f1; padding:22px; border-radius:50%;"></i><h4>Dr. Sarah Njoroge</h4><div style="color:#0a6e6b;">pediatric dentist</div></div>
        <div class="team-member" style="background:#f9fdfe; border-radius:40px; padding:36px 26px; flex:1 1 200px; text-align:center;"><i class="fas fa-teeth" style="font-size:4rem; background:#dcf2f1; padding:22px; border-radius:50%;"></i><h4>Dr. James Park</h4><div style="color:#0a6e6b;">prosthodontist</div></div>
      </div>
    </div>

    <!-- CONTACT PAGE -->
    <div id="contact-page" class="page">
      <div class="section-header"><h2>Get in touch</h2><p>We're here to help</p></div>
      <div class="contact-row" style="display:flex; gap:40px; flex-wrap:wrap;">
        <div class="contact-info" style="flex:1; background:#f0f9f8; border-radius:50px; padding:40px;">
          <div style="display:flex; align-items:center; gap:20px; margin:20px 0;"><i class="fas fa-map-pin"></i> 123 Main Street, NY</div>
          <div style="display:flex; align-items:center; gap:20px; margin:20px 0;"><i class="fas fa-phone"></i> (212) 555 0149</div>
          <div style="display:flex; align-items:center; gap:20px; margin:20px 0;"><i class="fas fa-envelope"></i> hello@brightsmile.demo</div>
        </div>
        <div class="contact-form" style="flex:2; background:white; border-radius:50px; padding:40px; border:1px solid #cdebea;">
          <div class="form-group"><input type="text" placeholder="Name" style="width:100%; padding:18px; border-radius:60px; border:1px solid #c4e0df;"></div>
          <div class="form-group"><input type="email" placeholder="Email" style="width:100%; padding:18px; border-radius:60px;"></div>
          <div class="form-group"><textarea rows="4" placeholder="Message" style="width:100%; padding:18px; border-radius:30px;"></textarea></div>
          <button class="btn">Send message</button>
        </div>
      </div>
    </div>

    <!-- BOOK PAGE -->
    <div id="book-page" class="page">
      <div class="section-header"><h2>Book your appointment</h2><p>online in 2 minutes</p></div>
      <div class="booking-card" style="max-width:700px; margin:0 auto; background:#f9fdfe; border-radius:70px; padding:50px;">
        <div class="form-group"><input type="text" placeholder="Full name" style="width:100%; padding:18px; border-radius:60px;"></div>
        <div class="form-group"><input type="tel" placeholder="Phone" style="width:100%; padding:18px;"></div>
        <div class="form-group"><select style="width:100%; padding:18px; border-radius:60px;"><option>Checkup</option><option>Consultation</option></select></div>
        <div class="form-group"><input type="date" style="width:100%; padding:18px;"></div>
        <button class="btn" style="width:100%;">Confirm booking</button>
      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-col">
          <div class="logo"><i class="fas fa-tooth"></i> BrightSmile</div>
          <p>123 Main Street, Suite 100, New York, NY 10001<br>contact@brightsmile.demo</p>
          <div class="social-icons">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-x-twitter"></i></a>
          </div>
        </div>
        <div class="footer-links">
          <div><strong>Quick links</strong><br><br><a href="#home" class="page-link" data-page="home">Home</a><a href="#services" class="page-link" data-page="services">Services</a><a href="#team" class="page-link" data-page="team">Team</a></div>
          <div><strong>Support</strong><br><br><a href="#contact" class="page-link" data-page="contact">Contact</a><a href="#book" class="page-link" data-page="book">Book online</a><a href="#">Privacy</a></div>
        </div>
      </div>
      <div class="copyright">© 2025 BrightSmile Dental Clinic – professional multi-page demo</div>
    </div>
  </div>

  <!-- JS for multi-page navigation -->
  <script>
    (function() {
      const pages = {
        home: document.getElementById('home-page'),
        services: document.getElementById('services-page'),
        team: document.getElementById('team-page'),
        contact: document.getElementById('contact-page'),
        book: document.getElementById('book-page')
      };
      const navLinks = document.querySelectorAll('.page-link');
      
      function showPage(pageId) {
        Object.values(pages).forEach(p => { if (p) p.classList.remove('active-page-content'); });
        if (pages[pageId]) pages[pageId].classList.add('active-page-content');
        
        navLinks.forEach(link => {
          const linkPage = link.getAttribute('data-page');
          if (linkPage === pageId) link.classList.add('active');
          else link.classList.remove('active');
        });
        history.pushState(null, null, '#'+pageId);
      }

      navLinks.forEach(link => {
        link.addEventListener('click', (e) => {
          e.preventDefault();
          const page = link.getAttribute('data-page');
          if (page) showPage(page);
        });
      });

      function routeFromHash() {
        const hash = window.location.hash.replace('#', '') || 'home';
        if (pages[hash]) showPage(hash);
        else showPage('home');
      }
      window.addEventListener('hashchange', routeFromHash);
      window.addEventListener('load', routeFromHash);
    })();
  </script>
  <style>.page-link.active { font-weight:700; color:#0a6e6b !important; border-bottom:3px solid #f3b33d; }</style>
</body>
</html>
