# shyw.github.io
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Xã Bình Lợi - Khám Phá Vùng Đất Xanh Tươi</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Be+Vietnam+Pro:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --green-dark: #1a3a2a;
    --green-mid: #2d6a4f;
    --green-light: #52b788;
    --green-pale: #d8f3dc;
    --gold: #b5832a;
    --gold-light: #e9c46a;
    --cream: #faf8f2;
    --brown: #6b4226;
    --text-dark: #1a1a1a;
    --text-muted: #6b7280;
    --white: #ffffff;
    --shadow: 0 4px 24px rgba(0,0,0,0.10);
    --radius: 16px;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Be Vietnam Pro', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ===== NAVBAR ===== */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 1000;
    background: rgba(26,58,42,0.97);
    backdrop-filter: blur(8px);
    padding: 0 40px;
    display: flex; align-items: center; justify-content: space-between;
    height: 68px;
    border-bottom: 1px solid rgba(82,183,136,0.15);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    color: var(--gold-light);
    font-size: 22px; font-weight: 700;
    letter-spacing: 0.5px;
    text-decoration: none;
  }
  .nav-logo span { color: var(--green-light); }
  .nav-links { display: flex; gap: 8px; align-items: center; }
  .nav-links a {
    color: rgba(255,255,255,0.85);
    text-decoration: none;
    font-size: 14px; font-weight: 400;
    padding: 8px 14px;
    border-radius: 8px;
    transition: all 0.2s;
  }
  .nav-links a:hover { background: rgba(82,183,136,0.15); color: var(--green-light); }
  .nav-btn {
    background: var(--gold) !important;
    color: white !important;
    font-weight: 600 !important;
    padding: 8px 20px !important;
    border-radius: 8px !important;
  }
  .nav-btn:hover { background: var(--gold-light) !important; color: var(--text-dark) !important; }

  /* ===== HERO ===== */
  .hero {
    height: 100vh; min-height: 650px;
    background: linear-gradient(160deg, #0d2818 0%, #1a4d30 35%, #2d6a4f 70%, #40916c 100%);
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
    padding-top: 68px;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background-image:
      radial-gradient(ellipse 60% 50% at 80% 50%, rgba(82,183,136,0.12) 0%, transparent 70%),
      radial-gradient(circle 300px at 20% 70%, rgba(181,131,42,0.08) 0%, transparent 70%);
  }
  .hero-pattern {
    position: absolute; inset: 0; opacity: 0.04;
    background-image: repeating-linear-gradient(45deg, #fff 0, #fff 1px, transparent 0, transparent 50%);
    background-size: 20px 20px;
  }
  .hero-content { position: relative; text-align: center; max-width: 780px; padding: 0 24px; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 6px;
    background: rgba(82,183,136,0.15);
    border: 1px solid rgba(82,183,136,0.3);
    color: var(--green-light);
    font-size: 13px; font-weight: 500;
    padding: 6px 16px; border-radius: 40px;
    margin-bottom: 24px;
    animation: fadeDown 0.6s ease both;
  }
  .hero-badge::before { content: "●"; font-size: 8px; }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(38px, 6vw, 72px);
    font-weight: 700; color: white;
    line-height: 1.1; margin-bottom: 16px;
    animation: fadeDown 0.7s 0.1s ease both;
  }
  .hero h1 span { color: var(--gold-light); }
  .hero p {
    font-size: 18px; color: rgba(255,255,255,0.75);
    line-height: 1.7; margin-bottom: 36px;
    animation: fadeDown 0.7s 0.2s ease both;
  }
  .hero-actions {
    display: flex; gap: 12px; justify-content: center; flex-wrap: wrap;
    animation: fadeDown 0.7s 0.3s ease both;
  }
  .btn-primary {
    background: var(--gold);
    color: white;
    padding: 14px 32px; border-radius: 10px;
    font-size: 15px; font-weight: 600;
    text-decoration: none; cursor: pointer; border: none;
    transition: all 0.2s; display: inline-block;
  }
  .btn-primary:hover { background: var(--gold-light); color: var(--text-dark); transform: translateY(-2px); }
  .btn-outline {
    background: transparent;
    color: white; border: 1px solid rgba(255,255,255,0.35);
    padding: 14px 32px; border-radius: 10px;
    font-size: 15px; font-weight: 500;
    text-decoration: none; cursor: pointer;
    transition: all 0.2s; display: inline-block;
  }
  .btn-outline:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.6); }
  .hero-stats {
    position: absolute; bottom: 36px; left: 0; right: 0;
    display: flex; justify-content: center; gap: 40px;
    animation: fadeUp 0.7s 0.5s ease both;
  }
  .hero-stat { text-align: center; }
  .hero-stat .num { font-size: 28px; font-weight: 700; color: var(--gold-light); font-family: 'Playfair Display', serif; }
  .hero-stat .lbl { font-size: 12px; color: rgba(255,255,255,0.55); margin-top: 2px; }

  /* ===== SECTIONS ===== */
  section { padding: 80px 40px; }
  .section-label {
    font-size: 12px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase;
    color: var(--green-mid); margin-bottom: 10px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 3.5vw, 44px); font-weight: 700;
    line-height: 1.2; margin-bottom: 16px;
    color: var(--green-dark);
  }
  .section-title span { color: var(--gold); }
  .section-sub { font-size: 16px; color: var(--text-muted); line-height: 1.7; max-width: 560px; }
  .container { max-width: 1180px; margin: 0 auto; }

  /* ===== ABOUT ===== */
  .about { background: white; }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: center; }
  .about-image {
    background: linear-gradient(135deg, #1a4d30 0%, #2d6a4f 50%, #52b788 100%);
    border-radius: 20px; height: 420px;
    position: relative; overflow: hidden;
    display: flex; align-items: center; justify-content: center;
  }
  .about-image-inner { text-align: center; color: white; }
  .about-image-inner .icon-big { font-size: 80px; display: block; margin-bottom: 16px; }
  .about-image-inner p { font-size: 15px; opacity: 0.8; }
  .about-map-overlay {
    position: absolute; bottom: 0; left: 0; right: 0;
    background: linear-gradient(transparent, rgba(0,0,0,0.5));
    padding: 20px;
  }
  .about-map-text { color: white; font-size: 13px; }
  .about-features { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 28px; }
  .about-feature {
    background: var(--green-pale);
    padding: 16px; border-radius: 12px;
    border-left: 3px solid var(--green-light);
  }
  .about-feature h4 { font-size: 14px; font-weight: 600; color: var(--green-dark); margin-bottom: 4px; }
  .about-feature p { font-size: 13px; color: var(--text-muted); line-height: 1.5; }

  /* ===== DESTINATIONS ===== */
  .destinations { background: var(--cream); }
  .dest-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 48px; }
  .dest-card {
    background: white; border-radius: var(--radius);
    overflow: hidden; box-shadow: var(--shadow);
    transition: transform 0.25s, box-shadow 0.25s;
    cursor: pointer;
  }
  .dest-card:hover { transform: translateY(-6px); box-shadow: 0 12px 40px rgba(0,0,0,0.14); }
  .dest-img {
    height: 200px;
    display: flex; align-items: center; justify-content: center;
    font-size: 56px; position: relative;
  }
  .dest-img-1 { background: linear-gradient(135deg, #1a4d30, #52b788); }
  .dest-img-2 { background: linear-gradient(135deg, #6b4226, #b5832a); }
  .dest-img-3 { background: linear-gradient(135deg, #134e4a, #0d9488); }
  .dest-img-4 { background: linear-gradient(135deg, #1e3a5f, #3b82f6); }
  .dest-img-5 { background: linear-gradient(135deg, #4a1942, #9333ea); }
  .dest-img-6 { background: linear-gradient(135deg, #451a03, #ea580c); }
  .dest-tag {
    position: absolute; top: 12px; right: 12px;
    background: rgba(0,0,0,0.4);
    color: white; font-size: 11px; font-weight: 500;
    padding: 4px 10px; border-radius: 20px;
  }
  .dest-body { padding: 20px; }
  .dest-body h3 { font-size: 17px; font-weight: 600; margin-bottom: 6px; color: var(--green-dark); }
  .dest-body p { font-size: 13px; color: var(--text-muted); line-height: 1.6; margin-bottom: 14px; }
  .dest-meta { display: flex; align-items: center; justify-content: space-between; }
  .dest-stars { color: var(--gold); font-size: 13px; }
  .dest-link { font-size: 13px; font-weight: 600; color: var(--green-mid); text-decoration: none; }
  .dest-link:hover { color: var(--green-light); }

  /* ===== TOURS ===== */
  .tours { background: var(--green-dark); }
  .tours .section-label { color: var(--green-light); }
  .tours .section-title { color: white; }
  .tours .section-sub { color: rgba(255,255,255,0.6); }
  .tours-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 48px; }
  .tour-card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(82,183,136,0.2);
    border-radius: var(--radius);
    padding: 28px;
    transition: all 0.25s; cursor: pointer;
    position: relative; overflow: hidden;
  }
  .tour-card:hover { background: rgba(255,255,255,0.1); border-color: var(--green-light); transform: translateY(-4px); }
  .tour-card.featured {
    border-color: var(--gold);
    background: rgba(181,131,42,0.08);
  }
  .tour-badge {
    position: absolute; top: 0; right: 0;
    background: var(--gold); color: white;
    font-size: 11px; font-weight: 600;
    padding: 6px 14px;
    border-radius: 0 var(--radius) 0 12px;
  }
  .tour-icon { font-size: 36px; margin-bottom: 16px; display: block; }
  .tour-card h3 { font-size: 18px; font-weight: 600; color: white; margin-bottom: 8px; }
  .tour-card p { font-size: 13px; color: rgba(255,255,255,0.6); line-height: 1.6; margin-bottom: 20px; }
  .tour-info { display: flex; gap: 16px; margin-bottom: 20px; flex-wrap: wrap; }
  .tour-info-item { font-size: 12px; color: var(--green-light); }
  .tour-info-item strong { display: block; color: white; font-size: 13px; }
  .tour-price { font-family: 'Playfair Display', serif; font-size: 24px; color: var(--gold-light); font-weight: 700; }
  .tour-price small { font-size: 13px; color: rgba(255,255,255,0.5); font-family: 'Be Vietnam Pro', sans-serif; font-weight: 400; }
  .tour-book {
    display: block; width: 100%; margin-top: 16px;
    background: var(--green-light); color: white;
    border: none; padding: 12px; border-radius: 10px;
    font-size: 14px; font-weight: 600; cursor: pointer;
    transition: background 0.2s;
    text-align: center; text-decoration: none;
  }
  .tour-book:hover { background: var(--green-mid); }

  /* ===== PROMOTIONS ===== */
  .promos { background: white; }
  .promo-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-top: 48px; }
  .promo-card {
    border-radius: var(--radius); padding: 32px;
    display: flex; gap: 20px; align-items: flex-start;
    position: relative; overflow: hidden;
    border: 1px solid rgba(0,0,0,0.06);
  }
  .promo-card-1 { background: linear-gradient(135deg, #f0fdf4, #dcfce7); border-color: #86efac; }
  .promo-card-2 { background: linear-gradient(135deg, #fffbeb, #fef3c7); border-color: #fcd34d; }
  .promo-card-3 { background: linear-gradient(135deg, #eff6ff, #dbeafe); border-color: #93c5fd; }
  .promo-card-4 { background: linear-gradient(135deg, #fff1f2, #ffe4e6); border-color: #fca5a5; }
  .promo-icon { font-size: 40px; flex-shrink: 0; }
  .promo-content h3 { font-size: 18px; font-weight: 700; margin-bottom: 6px; color: var(--green-dark); }
  .promo-content p { font-size: 13px; color: var(--text-muted); line-height: 1.6; margin-bottom: 14px; }
  .promo-discount {
    display: inline-block;
    background: var(--gold); color: white;
    font-size: 13px; font-weight: 700;
    padding: 4px 14px; border-radius: 20px;
  }
  .promo-valid { font-size: 11px; color: var(--text-muted); margin-top: 6px; display: block; }

  /* ===== BOOKING ===== */
  .booking { background: linear-gradient(135deg, #1a3a2a 0%, #2d6a4f 100%); }
  .booking .section-label { color: var(--green-light); }
  .booking .section-title { color: white; }
  .booking .section-sub { color: rgba(255,255,255,0.6); }
  .booking-form {
    background: white; border-radius: 20px;
    padding: 40px; margin-top: 40px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.2);
  }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 20px; }
  .form-row-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 20px; margin-bottom: 20px; }
  .form-group { display: flex; flex-direction: column; gap: 6px; }
  .form-group label { font-size: 13px; font-weight: 600; color: var(--green-dark); }
  .form-group input, .form-group select, .form-group textarea {
    padding: 12px 16px; border: 1.5px solid #e5e7eb;
    border-radius: 10px; font-size: 14px; font-family: inherit;
    transition: border-color 0.2s; outline: none; background: white;
    color: var(--text-dark);
  }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
    border-color: var(--green-light);
  }
  .form-group textarea { resize: vertical; min-height: 100px; }
  .form-submit {
    background: var(--green-mid); color: white;
    border: none; padding: 16px 40px; border-radius: 10px;
    font-size: 16px; font-weight: 600; cursor: pointer;
    transition: all 0.2s; margin-top: 8px;
    width: 100%;
  }
  .form-submit:hover { background: var(--green-dark); transform: translateY(-2px); }
  .form-note { font-size: 12px; color: var(--text-muted); margin-top: 10px; text-align: center; }

  /* ===== PAYMENT ===== */
  .payment { background: var(--cream); }
  .payment-methods { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 40px; }
  .payment-method {
    background: white; border-radius: var(--radius);
    padding: 24px 16px; text-align: center;
    border: 1.5px solid #e5e7eb;
    transition: all 0.2s; cursor: pointer;
  }
  .payment-method:hover { border-color: var(--green-light); transform: translateY(-3px); box-shadow: var(--shadow); }
  .payment-method .pm-icon { font-size: 36px; margin-bottom: 10px; display: block; }
  .payment-method h4 { font-size: 14px; font-weight: 600; margin-bottom: 4px; color: var(--green-dark); }
  .payment-method p { font-size: 12px; color: var(--text-muted); }
  .payment-secure {
    background: var(--green-pale); border-radius: 12px;
    padding: 20px 24px; margin-top: 24px;
    display: flex; align-items: center; gap: 12px;
  }
  .payment-secure span { font-size: 28px; }
  .payment-secure p { font-size: 13px; color: var(--green-dark); line-height: 1.5; }
  .payment-secure strong { font-weight: 600; }

  /* ===== SUPPORT ===== */
  .support { background: white; }
  .support-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; align-items: start; margin-top: 40px; }
  .support-channels { display: grid; gap: 16px; }
  .support-channel {
    background: var(--cream); border-radius: 14px;
    padding: 20px; display: flex; gap: 16px; align-items: center;
    border: 1px solid #e5e7eb; transition: all 0.2s; cursor: pointer;
  }
  .support-channel:hover { border-color: var(--green-light); background: var(--green-pale); }
  .support-ch-icon {
    width: 52px; height: 52px; border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 24px; flex-shrink: 0;
  }
  .ch-1 { background: #e0f7e9; }
  .ch-2 { background: #fff3e0; }
  .ch-3 { background: #e3f2fd; }
  .ch-4 { background: #fce4ec; }
  .support-ch-info h4 { font-size: 15px; font-weight: 600; color: var(--green-dark); }
  .support-ch-info p { font-size: 13px; color: var(--text-muted); margin-top: 3px; }
  .support-ch-info a { color: var(--green-mid); font-weight: 600; text-decoration: none; }
  .support-faq h3 { font-size: 20px; font-weight: 700; color: var(--green-dark); margin-bottom: 20px; font-family: 'Playfair Display', serif; }
  .faq-item {
    border-bottom: 1px solid #e5e7eb; padding: 16px 0; cursor: pointer;
  }
  .faq-q { font-size: 14px; font-weight: 600; color: var(--green-dark); display: flex; justify-content: space-between; align-items: center; }
  .faq-a { font-size: 13px; color: var(--text-muted); margin-top: 10px; line-height: 1.7; display: none; }
  .faq-item.open .faq-a { display: block; }
  .faq-item.open .faq-arrow { transform: rotate(180deg); }
  .faq-arrow { transition: transform 0.2s; font-size: 12px; color: var(--green-mid); }

  /* ===== TESTIMONIALS ===== */
  .testimonials { background: var(--cream); }
  .testi-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 48px; }
  .testi-card {
    background: white; border-radius: var(--radius);
    padding: 24px; box-shadow: var(--shadow);
  }
  .testi-stars { color: var(--gold); font-size: 14px; margin-bottom: 12px; }
  .testi-text { font-size: 14px; color: var(--text-muted); line-height: 1.7; margin-bottom: 16px; font-style: italic; }
  .testi-author { display: flex; align-items: center; gap: 10px; }
  .testi-avatar {
    width: 40px; height: 40px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px; font-weight: 700; color: white;
    flex-shrink: 0;
  }
  .av-1 { background: var(--green-mid); }
  .av-2 { background: var(--gold); }
  .av-3 { background: var(--brown); }
  .testi-author h5 { font-size: 14px; font-weight: 600; color: var(--green-dark); }
  .testi-author p { font-size: 12px; color: var(--text-muted); }

  /* ===== FOOTER ===== */
  footer {
    background: var(--green-dark);
    color: rgba(255,255,255,0.7);
    padding: 60px 40px 30px;
  }
  .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 48px; margin-bottom: 40px; max-width: 1180px; margin-left: auto; margin-right: auto; }
  .footer-brand .logo { font-family: 'Playfair Display', serif; color: var(--gold-light); font-size: 24px; font-weight: 700; margin-bottom: 14px; display: block; }
  .footer-brand p { font-size: 14px; line-height: 1.7; }
  .footer-col h4 { color: white; font-size: 15px; font-weight: 600; margin-bottom: 16px; }
  .footer-col a { display: block; font-size: 13px; color: rgba(255,255,255,0.6); text-decoration: none; margin-bottom: 10px; transition: color 0.2s; }
  .footer-col a:hover { color: var(--green-light); }
  .footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.1);
    padding-top: 20px; text-align: center;
    font-size: 13px; max-width: 1180px; margin: 0 auto;
  }
  .social-links { display: flex; gap: 10px; margin-top: 20px; }
  .social-link {
    width: 38px; height: 38px; border-radius: 8px;
    background: rgba(255,255,255,0.08); display: flex; align-items: center; justify-content: center;
    font-size: 16px; text-decoration: none; transition: background 0.2s;
  }
  .social-link:hover { background: var(--green-mid); }

  /* ===== MODAL ===== */
  .modal-overlay {
    position: fixed; inset: 0; background: rgba(0,0,0,0.5);
    display: none; align-items: center; justify-content: center;
    z-index: 2000; padding: 20px;
  }
  .modal-overlay.open { display: flex; }
  .modal {
    background: white; border-radius: 20px;
    padding: 40px; max-width: 500px; width: 100%;
    max-height: 90vh; overflow-y: auto;
  }
  .modal h2 { font-family: 'Playfair Display', serif; font-size: 26px; color: var(--green-dark); margin-bottom: 8px; }
  .modal p { font-size: 14px; color: var(--text-muted); margin-bottom: 24px; line-height: 1.6; }
  .modal-close {
    position: absolute; top: 16px; right: 20px; background: none; border: none;
    font-size: 22px; cursor: pointer; color: var(--text-muted);
  }
  .modal-close:hover { color: var(--text-dark); }
  .modal-actions { display: flex; gap: 12px; margin-top: 20px; }
  .btn-green {
    background: var(--green-mid); color: white;
    border: none; padding: 12px 24px; border-radius: 10px;
    font-size: 14px; font-weight: 600; cursor: pointer; flex: 1;
    transition: background 0.2s;
  }
  .btn-green:hover { background: var(--green-dark); }
  .btn-gray {
    background: #f3f4f6; color: var(--text-dark);
    border: none; padding: 12px 24px; border-radius: 10px;
    font-size: 14px; font-weight: 500; cursor: pointer;
    transition: background 0.2s;
  }
  .btn-gray:hover { background: #e5e7eb; }
  .success-msg {
    background: var(--green-pale); border: 1px solid var(--green-light);
    border-radius: 10px; padding: 16px; font-size: 14px; color: var(--green-dark);
    margin-top: 16px; display: none;
  }

  /* ===== ANIMATIONS ===== */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .fade-in { opacity: 0; transform: translateY(20px); transition: opacity 0.6s ease, transform 0.6s ease; }
  .fade-in.visible { opacity: 1; transform: translateY(0); }

  /* ===== SCROLL PROGRESS ===== */
  .progress-bar {
    position: fixed; top: 68px; left: 0; height: 3px;
    background: var(--gold); z-index: 999;
    width: 0%; transition: width 0.1s;
  }

  /* ===== CHAT WIDGET ===== */
  .chat-widget {
    position: fixed; bottom: 24px; right: 24px; z-index: 1500;
  }
  .chat-btn {
    width: 58px; height: 58px; border-radius: 50%;
    background: var(--green-mid); border: none; cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    font-size: 24px; box-shadow: 0 4px 20px rgba(45,106,79,0.4);
    transition: transform 0.2s, background 0.2s;
  }
  .chat-btn:hover { transform: scale(1.08); background: var(--green-dark); }
  .chat-badge {
    position: absolute; top: 0; right: 0;
    width: 18px; height: 18px; border-radius: 50%;
    background: red; color: white; font-size: 11px; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    border: 2px solid white;
  }
  .chat-popup {
    position: absolute; bottom: 70px; right: 0;
    width: 300px; background: white; border-radius: 16px;
    box-shadow: 0 12px 40px rgba(0,0,0,0.18);
    padding: 20px; display: none;
  }
  .chat-popup.open { display: block; }
  .chat-popup h4 { font-size: 15px; font-weight: 700; color: var(--green-dark); margin-bottom: 4px; }
  .chat-popup p { font-size: 13px; color: var(--text-muted); margin-bottom: 14px; }
  .chat-quick-btns { display: flex; flex-direction: column; gap: 8px; }
  .chat-quick-btn {
    background: var(--green-pale); color: var(--green-dark);
    border: none; padding: 10px 14px; border-radius: 8px;
    font-size: 13px; font-weight: 500; cursor: pointer; text-align: left;
    transition: background 0.2s;
  }
  .chat-quick-btn:hover { background: #b7e4c7; }

  /* ===== BACK TO TOP ===== */
  .back-top {
    position: fixed; bottom: 24px; left: 24px;
    width: 44px; height: 44px; border-radius: 12px;
    background: var(--green-dark); color: white;
    border: none; cursor: pointer; font-size: 18px;
    display: flex; align-items: center; justify-content: center;
    opacity: 0; pointer-events: none; transition: opacity 0.3s;
    z-index: 500;
  }
  .back-top.visible { opacity: 1; pointer-events: auto; }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 900px) {
    nav { padding: 0 20px; }
    .nav-links { display: none; }
    section { padding: 60px 20px; }
    .about-grid, .dest-grid, .tours-grid, .promo-grid, .testi-grid,
    .support-grid, .footer-grid { grid-template-columns: 1fr; }
    .form-row, .form-row-3 { grid-template-columns: 1fr; }
    .payment-methods { grid-template-columns: repeat(2, 1fr); }
    .hero-stats { gap: 20px; }
    footer { padding: 40px 20px 20px; }
  }
</style>
</head>
<body>

<!-- SCROLL PROGRESS -->
<div class="progress-bar" id="progressBar"></div>

<!-- NAVBAR -->
<nav>
  <a class="nav-logo" href="#">🌿 Bình Lợi <span>Du Lịch</span></a>
  <div class="nav-links">
    <a href="#about">Giới Thiệu</a>
    <a href="#destinations">Địa Điểm</a>
    <a href="#tours">Tour</a>
    <a href="#promos">Ưu Đãi</a>
    <a href="#booking">Đặt Vé</a>
    <a href="#payment">Thanh Toán</a>
    <a href="#support">Hỗ Trợ</a>
    <a href="#booking" class="nav-btn">Đặt Ngay</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-pattern"></div>
  <div class="hero-content">
    <div class="hero-badge">Xã Bình Lợi · Bình Chánh · TP.HCM</div>
    <h1>Khám Phá <span>Vùng Xanh</span><br>Bình Lợi Tươi Đẹp</h1>
    <p>Trải nghiệm cuộc sống nông thôn yên bình, hệ thống kênh rạch đặc trưng Nam Bộ<br>và văn hóa bản địa chỉ cách trung tâm Sài Gòn 22km.</p>
    <div class="hero-actions">
      <a href="#tours" class="btn-primary">🗺️ Xem Tour Du Lịch</a>
      <a href="#booking" class="btn-outline">📅 Đặt Vé Ngay</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="hero-stat">
      <div class="num">54km²</div>
      <div class="lbl">Diện Tích</div>
    </div>
    <div class="hero-stat">
      <div class="num">47K+</div>
      <div class="lbl">Dân Số</div>
    </div>
    <div class="hero-stat">
      <div class="num">22km</div>
      <div class="lbl">Cách Trung Tâm</div>
    </div>
    <div class="hero-stat">
      <div class="num">6+</div>
      <div class="lbl">Điểm Tham Quan</div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="container">
    <div class="about-grid fade-in">
      <div class="about-image">
        <div class="about-image-inner">
          <span class="icon-big">🌾</span>
          <p style="font-size:18px; font-weight:600;">Xã Bình Lợi</p>
          <p>Vùng đất nông thôn xanh tươi</p>
          <p style="margin-top:12px; font-size:13px;">Huyện Bình Chánh · TP. Hồ Chí Minh</p>
        </div>
        <div class="about-map-overlay">
          <div class="about-map-text">📍 Phía Tây Nam TP.HCM · Giáp Long An & Tây Ninh</div>
        </div>
      </div>
      <div>
        <div class="section-label">Về Bình Lợi</div>
        <h2 class="section-title">Vùng Đất Nông Nghiệp <span>Trù Phú</span></h2>
        <p class="section-sub">Xã Bình Lợi nằm ở phía Tây Nam TP.HCM, cách trung tâm khoảng 22km. Vùng đất này mang đậm nét đặc trưng của miền Nam Bộ với hệ thống kênh rạch chằng chịt, cánh đồng xanh mướt và không khí trong lành.</p>
        <p style="font-size:14px; color:var(--text-muted); line-height:1.7; margin-top:14px;">Sau sáp nhập ngày 01/07/2025, xã Bình Lợi được thành lập từ xã Lê Minh Xuân và xã Bình Lợi cũ, có diện tích 54.18 km² với hơn 47.000 cư dân. Đây là điểm đến hấp dẫn cho những ai muốn thoát khỏi sự ồn ào đô thị và hòa mình vào thiên nhiên.</p>
        <div class="about-features">
          <div class="about-feature">
            <h4>🌊 Kênh Rạch Đặc Trưng</h4>
            <p>Hệ thống kênh rạch chằng chịt tạo nên cảnh quan thiên nhiên độc đáo Nam Bộ</p>
          </div>
          <div class="about-feature">
            <h4>🌾 Nông Nghiệp Phong Phú</h4>
            <p>Đất đai màu mỡ, vườn cây ăn trái, ruộng lúa và ao cá thịnh vượng</p>
          </div>
          <div class="about-feature">
            <h4>🏛️ Di Tích Lịch Sử</h4>
            <p>Nhiều di tích kháng chiến và công trình tín ngưỡng truyền thống quý giá</p>
          </div>
          <div class="about-feature">
            <h4>🚗 Giao Thông Thuận Tiện</h4>
            <p>Kết nối qua Tỉnh lộ 10, QL1A và đường Nguyễn Văn Linh dễ dàng</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DESTINATIONS -->
<section class="destinations" id="destinations">
  <div class="container">
    <div class="fade-in">
      <div class="section-label">Điểm Đến Nổi Bật</div>
      <h2 class="section-title">Khám Phá <span>Những Địa Danh</span> Đặc Sắc</h2>
      <p class="section-sub">Từ những ngôi chùa linh thiêng đến khu sinh thái xanh mướt, Bình Lợi mang đến trải nghiệm du lịch phong phú và đa dạng.</p>
    </div>
    <div class="dest-grid fade-in">
      <div class="dest-card" onclick="openDestModal('chua')">
        <div class="dest-img dest-img-1">
          🛕
          <div class="dest-tag">Tâm Linh</div>
        </div>
        <div class="dest-body">
          <h3>Chùa Bát Bửu Phật Đài</h3>
          <p>Chùa Phật Cô Đơn nổi tiếng với kiến trúc bát giác độc đáo, tượng Phật cao 7m, khuôn viên hơn 30ha giữa rừng bạch đàn xanh mát.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★★</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
      <div class="dest-card" onclick="openDestModal('langnhe')">
        <div class="dest-img dest-img-2">
          🕯️
          <div class="dest-tag">Làng Nghề</div>
        </div>
        <div class="dest-body">
          <h3>Làng Nghề Se Nhang</h3>
          <p>Làng nghề làm nhang truyền thống Lê Minh Xuân, một trong 100 điều thú vị của TP.HCM, nơi lưu giữ nghề thủ công hàng trăm năm tuổi.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★☆</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
      <div class="dest-card" onclick="openDestModal('langlebau')">
        <div class="dest-img dest-img-3">
          🦅
          <div class="dest-tag">Lịch Sử</div>
        </div>
        <div class="dest-body">
          <h3>Khu Di Tích Láng Le Bàu Cò</h3>
          <p>Di tích lịch sử kháng chiến quan trọng, không gian xanh mát với nhiều cây cổ thụ, lý tưởng để tham quan và tìm hiểu lịch sử.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★☆</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
      <div class="dest-card" onclick="openDestModal('home')">
        <div class="dest-img dest-img-4">
          🌻
          <div class="dest-tag">Sinh Thái</div>
        </div>
        <div class="dest-body">
          <h3>Springfield Cottage</h3>
          <p>Homestay phong cách "hương đồng gió nội" độc đáo với chòi nổi trên mặt nước, chèo thuyền hái sen và trải nghiệm cuộc sống quê hương.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★★</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
      <div class="dest-card" onclick="openDestModal('dinh')">
        <div class="dest-img dest-img-5">
          🏯
          <div class="dest-tag">Văn Hóa</div>
        </div>
        <div class="dest-body">
          <h3>Đình Tân Túc & Đình Bình Trường</h3>
          <p>Công trình tín ngưỡng lâu đời gắn liền với đời sống văn hóa, tinh thần của người dân Bình Chánh qua nhiều thế hệ.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★☆</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
      <div class="dest-card" onclick="openDestModal('sinhthai')">
        <div class="dest-img dest-img-6">
          🎣
          <div class="dest-tag">Ẩm Thực</div>
        </div>
        <div class="dest-body">
          <h3>Khu Ẩm Thực Sinh Thái Xuân Hương</h3>
          <p>Khu du lịch sinh thái kết hợp câu cá giải trí và ẩm thực đồng quê Nam Bộ, lý tưởng cho cả gia đình cuối tuần vui chơi.</p>
          <div class="dest-meta">
            <span class="dest-stars">★★★★☆</span>
            <a href="#booking" class="dest-link">Đặt Tour →</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TOURS -->
<section class="tours" id="tours">
  <div class="container">
    <div class="fade-in">
      <div class="section-label">Gói Tour</div>
      <h2 class="section-title" style="color:white;">Chọn <span>Tour Phù Hợp</span> Với Bạn</h2>
      <p class="section-sub">Đa dạng gói tour từ tham quan nhanh đến trải nghiệm toàn diện, phù hợp mọi nhu cầu và ngân sách.</p>
    </div>
    <div class="tours-grid fade-in">
      <div class="tour-card">
        <span class="tour-icon">🌅</span>
        <h3>Tour Ngày – Khám Phá Nhanh</h3>
        <p>Tham quan chùa Phật Cô Đơn, làng nghề se nhang và khu sinh thái trong một ngày đầy đủ trải nghiệm.</p>
        <div class="tour-info">
          <div class="tour-info-item"><strong>1 ngày</strong>Thời gian</div>
          <div class="tour-info-item"><strong>Xe đưa đón</strong>Phương tiện</div>
          <div class="tour-info-item"><strong>10 người</strong>Nhóm tối đa</div>
        </div>
        <div class="tour-price">350.000đ <small>/người</small></div>
        <a href="#booking" class="tour-book">Đặt Tour Này</a>
      </div>
      <div class="tour-card featured">
        <div class="tour-badge">🔥 PHỔ BIẾN</div>
        <span class="tour-icon">🌿</span>
        <h3>Tour 2 Ngày 1 Đêm – Trọn Vẹn Bình Lợi</h3>
        <p>Trải nghiệm toàn diện: chùa chiền, làng nghề, chèo xuồng kênh rạch, ngủ homestay và thưởng thức ẩm thực Nam Bộ.</p>
        <div class="tour-info">
          <div class="tour-info-item"><strong>2 ngày 1 đêm</strong>Thời gian</div>
          <div class="tour-info-item"><strong>Homestay</strong>Lưu trú</div>
          <div class="tour-info-item"><strong>15 người</strong>Nhóm tối đa</div>
        </div>
        <div class="tour-price">850.000đ <small>/người</small></div>
        <a href="#booking" class="tour-book">Đặt Tour Này</a>
      </div>
      <div class="tour-card">
        <span class="tour-icon">🎒</span>
        <h3>Tour Gia Đình – Cuối Tuần Vui</h3>
        <p>Gói đặc biệt dành cho gia đình với nhiều hoạt động trải nghiệm nông nghiệp, hái trái cây, câu cá và picnic sinh thái.</p>
        <div class="tour-info">
          <div class="tour-info-item"><strong>1 ngày</strong>Thời gian</div>
          <div class="tour-info-item"><strong>Bao Bữa ăn</strong>Tiện ích</div>
          <div class="tour-info-item"><strong>Gia đình</strong>Đối tượng</div>
        </div>
        <div class="tour-price">280.000đ <small>/người</small></div>
        <a href="#booking" class="tour-book">Đặt Tour Này</a>
      </div>
    </div>
  </div>
</section>

<!-- PROMOTIONS -->
<section class="promos" id="promos">
  <div class="container">
    <div class="fade-in">
      <div class="section-label">Khuyến Mãi Đặc Biệt</div>
      <h2 class="section-title">Ưu Đãi <span>Không Thể Bỏ Lỡ</span></h2>
      <p class="section-sub">Săn ngay những gói khuyến mãi hấp dẫn để tiết kiệm chi phí và có chuyến đi đáng nhớ.</p>
    </div>
    <div class="promo-grid fade-in">
      <div class="promo-card promo-card-1">
        <div class="promo-icon">👨👩👧👦</div>
        <div class="promo-content">
          <h3>Gói Gia Đình Hè 2025</h3>
          <p>Đặt tour cho nhóm từ 4 người trở lên được giảm ngay. Bao gồm bữa ăn trưa và quà lưu niệm đặc biệt.</p>
          <span class="promo-discount">GIẢM 20%</span>
          <span class="promo-valid">Áp dụng đến 31/08/2025</span>
        </div>
      </div>
      <div class="promo-card promo-card-2">
        <div class="promo-icon">🌙</div>
        <div class="promo-content">
          <h3>Early Bird – Đặt Sớm Giá Tốt</h3>
          <p>Đặt tour trước 7 ngày được nhận ưu đãi đặc biệt. Áp dụng cho tất cả các gói tour trong tuần.</p>
          <span class="promo-discount">GIẢM 15%</span>
          <span class="promo-valid">Áp dụng quanh năm</span>
        </div>
      </div>
      <div class="promo-card promo-card-3">
        <div class="promo-icon">🎓</div>
        <div class="promo-content">
          <h3>Ưu Đãi Học Sinh – Sinh Viên</h3>
          <p>Xuất trình thẻ học sinh/sinh viên hợp lệ để nhận ưu đãi đặc biệt. Cơ hội học hỏi về lịch sử và văn hóa địa phương.</p>
          <span class="promo-discount">GIẢM 25%</span>
          <span class="promo-valid">Áp dụng quanh năm với thẻ hợp lệ</span>
        </div>
      </div>
      <div class="promo-card promo-card-4">
        <div class="promo-icon">🎁</div>
        <div class="promo-content">
          <h3>Combo Tour + Homestay</h3>
          <p>Đặt trọn gói tour 2 ngày 1 đêm kết hợp homestay Springfield Cottage được giá cực ưu đãi.</p>
          <span class="promo-discount">TIẾT KIỆM 200K</span>
          <span class="promo-valid">Áp dụng đến hết năm 2025</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- BOOKING -->
<section class="booking" id="booking">
  <div class="container">
    <div class="fade-in" style="text-align:center;">
      <div class="section-label">Đặt Vé Du Lịch</div>
      <h2 class="section-title">Lên Kế Hoạch <span style="color:var(--gold-light);">Chuyến Đi</span> Ngay Hôm Nay</h2>
      <p class="section-sub" style="margin:0 auto;">Điền thông tin bên dưới, đội ngũ tư vấn sẽ liên hệ trong vòng 2 giờ để xác nhận và hỗ trợ bạn.</p>
    </div>
    <div class="booking-form fade-in">
      <div class="form-row">
        <div class="form-group">
          <label>Họ và tên *</label>
          <input type="text" placeholder="Nguyễn Văn A" id="f_name">
        </div>
        <div class="form-group">
          <label>Số điện thoại *</label>
          <input type="tel" placeholder="0901 234 567" id="f_phone">
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Email</label>
          <input type="email" placeholder="email@example.com" id="f_email">
        </div>
        <div class="form-group">
          <label>Gói Tour *</label>
          <select id="f_tour">
            <option value="">-- Chọn gói tour --</option>
            <option>Tour Ngày – Khám Phá Nhanh (350.000đ)</option>
            <option>Tour 2 Ngày 1 Đêm – Trọn Vẹn Bình Lợi (850.000đ)</option>
            <option>Tour Gia Đình – Cuối Tuần Vui (280.000đ)</option>
            <option>Tour Tùy Chỉnh Theo Yêu Cầu</option>
          </select>
        </div>
      </div>
      <div class="form-row-3">
        <div class="form-group">
          <label>Ngày khởi hành *</label>
          <input type="date" id="f_date">
        </div>
        <div class="form-group">
          <label>Số người lớn</label>
          <select id="f_adults">
            <option>1 người</option>
            <option>2 người</option>
            <option selected>3–5 người</option>
            <option>6–10 người</option>
            <option>Trên 10 người</option>
          </select>
        </div>
        <div class="form-group">
          <label>Số trẻ em</label>
          <select id="f_kids">
            <option selected>Không có</option>
            <option>1 trẻ</option>
            <option>2 trẻ</option>
            <option>3+ trẻ</option>
          </select>
        </div>
      </div>
      <div class="form-group" style="margin-bottom:20px;">
        <label>Yêu cầu đặc biệt / Ghi chú</label>
        <textarea placeholder="Ăn chay, xe lăn, địa điểm muốn thăm thêm..."></textarea>
      </div>
      <button class="form-submit" onclick="submitBooking()">✈️ Gửi Yêu Cầu Đặt Tour</button>
      <p class="form-note">🔒 Thông tin của bạn được bảo mật tuyệt đối · Phản hồi trong vòng 2 giờ</p>
      <div class="success-msg" id="bookingSuccess">
        ✅ <strong>Đặt tour thành công!</strong> Đội ngũ tư vấn sẽ liên hệ bạn trong vòng 2 giờ qua số điện thoại đã đăng ký. Cảm ơn bạn đã tin tưởng chọn Bình Lợi Du Lịch!
      </div>
    </div>
  </div>
</section>

<!-- PAYMENT -->
<section class="payment" id="payment">
  <div class="container">
    <div class="fade-in">
      <div class="section-label">Phương Thức Thanh Toán</div>
      <h2 class="section-title">Thanh Toán <span>An Toàn & Tiện Lợi</span></h2>
      <p class="section-sub">Hỗ trợ đa dạng phương thức thanh toán để bạn đặt vé nhanh chóng và tiện lợi nhất.</p>
    </div>
    <div class="payment-methods fade-in">
      <div class="payment-method" onclick="showPaymentInfo('cash')">
        <span class="pm-icon">💵</span>
        <h4>Tiền Mặt</h4>
        <p>Thanh toán trực tiếp tại văn phòng hoặc khi lên xe</p>
      </div>
      <div class="payment-method" onclick="showPaymentInfo('bank')">
        <span class="pm-icon">🏦</span>
        <h4>Chuyển Khoản</h4>
        <p>VietcomBank · MB Bank · Techcombank</p>
      </div>
      <div class="payment-method" onclick="showPaymentInfo('ewallet')">
        <span class="pm-icon">📱</span>
        <h4>Ví Điện Tử</h4>
        <p>MoMo · ZaloPay · VNPay · ShopeePay</p>
      </div>
      <div class="payment-method" onclick="showPaymentInfo('card')">
        <span class="pm-icon">💳</span>
        <h4>Thẻ Ngân Hàng</h4>
        <p>Visa · Mastercard · JCB · ATM nội địa</p>
      </div>
    </div>
    <div class="payment-secure fade-in">
      <span>🔐</span>
      <p><strong>Bảo Mật Tuyệt Đối:</strong> Mọi giao dịch thanh toán được mã hóa SSL 256-bit. Chính sách hoàn tiền 100% nếu hủy trước 48 giờ. Hỗ trợ thanh toán trả góp 0% lãi suất cho tour từ 2 triệu đồng trở lên qua thẻ tín dụng.</p>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="testimonials">
  <div class="container">
    <div class="fade-in" style="text-align:center;">
      <div class="section-label">Đánh Giá Khách Hàng</div>
      <h2 class="section-title">Khách Hàng <span>Nói Gì</span> Về Chúng Tôi</h2>
    </div>
    <div class="testi-grid fade-in">
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"Chuyến đi thật tuyệt vời! Không ngờ gần Sài Gòn mà lại có nơi yên bình đến vậy. Hướng dẫn viên nhiệt tình, cảnh vật đẹp, ẩm thực ngon. Nhất định sẽ quay lại!"</p>
        <div class="testi-author">
          <div class="testi-avatar av-1">TL</div>
          <div>
            <h5>Trần Minh Lộc</h5>
            <p>Quận 1, TP.HCM · Tour 2 Ngày</p>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"Mình đưa cả gia đình đi tour cuối tuần, các con rất thích được tát mương bắt cá và hái trái cây. Giá hợp lý, dịch vụ chu đáo. Xứng đáng 5 sao!"</p>
        <div class="testi-author">
          <div class="testi-avatar av-2">NH</div>
          <div>
            <h5>Nguyễn Thị Hoa</h5>
            <p>Bình Thạnh · Tour Gia Đình</p>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★☆</div>
        <p class="testi-text">"Làng nghề se nhang rất thú vị, được tận mắt xem quá trình thủ công truyền thống. Chùa Phật Cô Đơn trang nghiêm và linh thiêng. Rất đáng để ghé thăm."</p>
        <div class="testi-author">
          <div class="testi-avatar av-3">PV</div>
          <div>
            <h5>Phạm Thanh Vân</h5>
            <p>Gò Vấp · Tour Ngày</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SUPPORT -->
<section class="support" id="support">
  <div class="container">
    <div class="fade-in">
      <div class="section-label">Hỗ Trợ Khách Hàng</div>
      <h2 class="section-title">Chúng Tôi Luôn <span>Sẵn Sàng</span> Hỗ Trợ</h2>
      <p class="section-sub">Đội ngũ tư vấn viên nhiệt tình sẵn sàng giải đáp mọi thắc mắc và hỗ trợ bạn lên kế hoạch chuyến đi tốt nhất.</p>
    </div>
    <div class="support-grid fade-in">
      <div class="support-channels">
        <div class="support-channel" onclick="showChatPopup()">
          <div class="support-ch-icon ch-1">💬</div>
          <div class="support-ch-info">
            <h4>Chat Trực Tuyến</h4>
            <p>Phản hồi trong vài phút · <span style="color:var(--green-mid); font-weight:600;">● Đang hoạt động</span></p>
          </div>
        </div>
        <div class="support-channel">
          <div class="support-ch-icon ch-2">📞</div>
          <div class="support-ch-info">
            <h4>Hotline Tư Vấn</h4>
            <p>📞 <a href="tel:19001234">1900 1234</a> · 7:00 – 21:00 mỗi ngày</p>
          </div>
        </div>
        <div class="support-channel">
          <div class="support-ch-icon ch-3">📧</div>
          <div class="support-ch-info">
            <h4>Email Hỗ Trợ</h4>
            <p><a href="mailto:info@binhloitourist.vn">info@binhloitourist.vn</a> · Phản hồi trong 24h</p>
          </div>
        </div>
        <div class="support-channel">
          <div class="support-ch-icon ch-4">📍</div>
          <div class="support-ch-info">
            <h4>Văn Phòng</h4>
            <p>1060 Đường Vườn Thơm, Xã Bình Lợi, Bình Chánh</p>
          </div>
        </div>
      </div>
      <div class="support-faq">
        <h3>Câu Hỏi Thường Gặp</h3>
        <div class="faq-item" onclick="toggleFaq(this)">
          <div class="faq-q">Đặt tour tối thiểu bao nhiêu người? <span class="faq-arrow">▼</span></div>
          <div class="faq-a">Bạn có thể đặt tour từ 1 người. Tuy nhiên, để tiết kiệm chi phí và có trải nghiệm vui vẻ hơn, chúng tôi khuyến khích nhóm từ 4-6 người. Nhóm trên 10 người được giảm thêm 10%.</div>
        </div>
        <div class="faq-item" onclick="toggleFaq(this)">
          <div class="faq-q">Có thể hủy tour và hoàn tiền không? <span class="faq-arrow">▼</span></div>
          <div class="faq-a">Hoàn tiền 100% nếu hủy trước 48 giờ. Hủy trong 24-48 giờ hoàn 50%. Hủy dưới 24 giờ không hoàn tiền nhưng có thể đổi ngày trong vòng 30 ngày.</div>
        </div>
        <div class="faq-item" onclick="toggleFaq(this)">
          <div class="faq-q">Tour có bao gồm bữa ăn không? <span class="faq-arrow">▼</span></div>
          <div class="faq-a">Tour ngày 1 ngày bao gồm bữa trưa và snack. Tour 2 ngày 1 đêm bao gồm đầy đủ các bữa ăn. Có thể yêu cầu thực đơn chay hoặc theo khẩu phần đặc biệt.</div>
        </div>
        <div class="faq-item" onclick="toggleFaq(this)">
          <div class="faq-q">Đi từ trung tâm TP.HCM mất bao lâu? <span class="faq-arrow">▼</span></div>
          <div class="faq-a">Từ trung tâm TP.HCM (Quận 1) đến xã Bình Lợi khoảng 40-50 phút đi xe tùy giờ. Tour có xe đưa đón tập trung tại điểm hẹn ở Quận 1 hoặc Bình Chánh.</div>
        </div>
        <div class="faq-item" onclick="toggleFaq(this)">
          <div class="faq-q">Trẻ em dưới bao nhiêu tuổi được miễn phí? <span class="faq-arrow">▼</span></div>
          <div class="faq-a">Trẻ em dưới 5 tuổi miễn phí hoàn toàn. Trẻ từ 5-12 tuổi được giảm 50% giá vé người lớn. Từ 12 tuổi trở lên tính giá người lớn.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <span class="logo">🌿 Bình Lợi Du Lịch</span>
      <p>Khám phá vẻ đẹp bình dị và văn hóa đặc sắc của xã Bình Lợi – vùng nông thôn xanh tươi gần Sài Gòn nhất. Chúng tôi mang đến những trải nghiệm chân thực và đáng nhớ.</p>
      <div class="social-links">
        <a class="social-link" href="#">📘</a>
        <a class="social-link" href="#">📸</a>
        <a class="social-link" href="#">▶️</a>
        <a class="social-link" href="#">💬</a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Khám Phá</h4>
      <a href="#destinations">Địa Điểm Du Lịch</a>
      <a href="#tours">Gói Tour</a>
      <a href="#promos">Khuyến Mãi</a>
      <a href="#">Blog Du Lịch</a>
      <a href="#">Bản Đồ</a>
    </div>
    <div class="footer-col">
      <h4>Dịch Vụ</h4>
      <a href="#booking">Đặt Vé Online</a>
      <a href="#payment">Thanh Toán</a>
      <a href="#">Thuê Xe</a>
      <a href="#">Đặt Homestay</a>
      <a href="#">Tour Tùy Chỉnh</a>
    </div>
    <div class="footer-col">
      <h4>Liên Hệ</h4>
      <a href="#">📞 1900 1234</a>
      <a href="#">✉️ info@binhloitourist.vn</a>
      <a href="#">📍 Xã Bình Lợi, Bình Chánh</a>
      <a href="#">🕐 7:00 – 21:00</a>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 Bình Lợi Du Lịch · Xã Bình Lợi, Huyện Bình Chánh, TP. Hồ Chí Minh · Giấy phép KDLH số 79-123/TCDL · Thiết kế với ❤️ cho vùng đất Bình Lợi</p>
  </div>
</footer>

<!-- CHAT WIDGET -->
<div class="chat-widget">
  <div class="chat-popup" id="chatPopup">
    <h4>💬 Tư Vấn Nhanh</h4>
    <p>Xin chào! Bạn cần hỗ trợ gì về tour Bình Lợi?</p>
    <div class="chat-quick-btns">
      <button class="chat-quick-btn" onclick="quickChat('Tôi muốn hỏi về giá tour')">💰 Hỏi về giá tour</button>
      <button class="chat-quick-btn" onclick="quickChat('Tôi muốn đặt tour ngay')">📅 Đặt tour ngay</button>
      <button class="chat-quick-btn" onclick="quickChat('Có ưu đãi gì không?')">🎁 Xem ưu đãi</button>
    </div>
  </div>
  <button class="chat-btn" onclick="toggleChat()">💬
    <div class="chat-badge">1</div>
  </button>
</div>

<!-- BACK TO TOP -->
<button class="back-top" id="backTop" onclick="scrollToTop()">↑</button>

<!-- DESTINATION MODAL -->
<div class="modal-overlay" id="destModal">
  <div class="modal" style="position:relative;">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 id="modal-title">Địa Điểm</h2>
    <p id="modal-desc">Mô tả chi tiết...</p>
    <div style="background:var(--green-pale); border-radius:12px; padding:16px; margin-bottom:16px;">
      <p id="modal-details" style="font-size:13px; color:var(--green-dark); line-height:1.7;"></p>
    </div>
    <div class="modal-actions">
      <button class="btn-green" onclick="location.href='#booking'; closeModal();">📅 Đặt Tour Ghé Thăm</button>
      <button class="btn-gray" onclick="closeModal()">Đóng</button>
    </div>
  </div>
</div>

<!-- PAYMENT MODAL -->
<div class="modal-overlay" id="payModal">
  <div class="modal" style="position:relative;">
    <button class="modal-close" onclick="document.getElementById('payModal').classList.remove('open')">✕</button>
    <h2 id="pay-title">Thanh Toán</h2>
    <p id="pay-desc">Thông tin thanh toán...</p>
    <div style="background:#f0fdf4; border-radius:12px; padding:16px; margin-bottom:16px; border:1px solid #86efac;">
      <p id="pay-details" style="font-size:13px; color:var(--green-dark); line-height:1.8;"></p>
    </div>
    <div class="modal-actions">
      <button class="btn-green" onclick="document.getElementById('payModal').classList.remove('open'); location.href='#booking'">✈️ Đặt Tour Ngay</button>
      <button class="btn-gray" onclick="document.getElementById('payModal').classList.remove('open')">Đóng</button>
    </div>
  </div>
</div>

<script>
  // Scroll effects
  window.addEventListener('scroll', () => {
    const p = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
    document.getElementById('progressBar').style.width = p + '%';
    document.getElementById('backTop').classList.toggle('visible', window.scrollY > 400);
    document.querySelectorAll('.fade-in').forEach(el => {
      const r = el.getBoundingClientRect();
      if (r.top < window.innerHeight - 80) el.classList.add('visible');
    });
  });
  window.dispatchEvent(new Event('scroll'));

  function scrollToTop() { window.scrollTo({ top: 0, behavior: 'smooth' }); }

  // FAQ
  function toggleFaq(item) {
    item.classList.toggle('open');
  }

  // Booking form
  function submitBooking() {
    const name = document.getElementById('f_name').value.trim();
    const phone = document.getElementById('f_phone').value.trim();
    const tour = document.getElementById('f_tour').value;
    if (!name || !phone || !tour) {
      alert('Vui lòng điền đầy đủ thông tin bắt buộc: Họ tên, Số điện thoại và Gói tour!');
      return;
    }
    const s = document.getElementById('bookingSuccess');
    s.style.display = 'block';
    s.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    setTimeout(() => s.style.display = 'none', 6000);
    document.getElementById('f_name').value = '';
    document.getElementById('f_phone').value = '';
    document.getElementById('f_email').value = '';
  }

  // Destination modal data
  const destinations = {
    chua: {
      title: '🛕 Chùa Bát Bửu Phật Đài (Chùa Phật Cô Đơn)',
      desc: 'Một trong những địa điểm tâm linh nổi tiếng nhất tại huyện Bình Chánh.',
      details: '📍 Địa chỉ: 22 đường Mai Bá Hương, xã Lê Minh Xuân, Bình Chánh\n🕐 Giờ mở cửa: 6:00 – 18:00 hằng ngày\n🎟️ Vé vào cửa: Miễn phí\n🌳 Diện tích: Hơn 30ha khuôn viên\n⛪ Điểm nổi bật: Phật đài hình bát giác cao 3m, tượng Phật Thích Ca 7m nặng 4 tấn điêu khắc năm 1957\n🚗 Cách trung tâm TP.HCM: ~35 phút'
    },
    langnhe: {
      title: '🕯️ Làng Nghề Se Nhang Lê Minh Xuân',
      desc: 'Một trong 100 điều thú vị của TP.HCM – làng nghề thủ công truyền thống hàng trăm năm.',
      details: '📍 Địa chỉ: Xã Lê Minh Xuân (nay là xã Bình Lợi), Bình Chánh\n🕐 Tham quan: Sáng sớm để xem quy trình làm nhang thủ công\n🎨 Trải nghiệm: Tự tay se nhang cùng nghệ nhân địa phương\n📸 Chụp ảnh: Màu sắc rực rỡ của những bó nhang phơi nắng\n🎁 Mua quà: Nhang thủ công làm quà lưu niệm ý nghĩa'
    },
    langlebau: {
      title: '🦅 Khu Di Tích Lịch Sử Láng Le Bàu Cò',
      desc: 'Di tích lịch sử kháng chiến quan trọng, nay là không gian xanh mát để tham quan và học tập.',
      details: '📍 Địa chỉ: Khu vực Láng Le Bàu Cò, Bình Chánh\n🏛️ Ý nghĩa: Di tích kháng chiến thời kỳ chống Mỹ\n🌳 Không gian: Nhiều cây cổ thụ xanh mát, thoáng đãng\n📚 Giá trị giáo dục: Lý tưởng cho học sinh, sinh viên tham quan\n🦅 Đặc điểm: Địa danh gắn liền với lịch sử hào hùng địa phương'
    },
    home: {
      title: '🌻 Springfield Cottage – Homestay Sinh Thái',
      desc: 'Khu homestay phong cách "hương đồng gió nội" độc đáo với chòi nổi trên mặt nước.',
      details: '📍 Địa chỉ: Xã Bình Lợi, Huyện Bình Chánh\n🛖 Loại hình: Homestay chòi nổi trên mặt nước\n🚣 Hoạt động: Chèo thuyền hái sen, ngắm cá bơi, dạo bộ trong rừng xanh\n❄️ Tiện nghi: Quạt tự nhiên – không gian mát mẻ nhờ thiên nhiên\n⏰ Cách TP.HCM: Chỉ ~40 phút lái xe, cảm giác như miền Tây'
    },
    dinh: {
      title: '🏯 Đình Tân Túc & Đình Bình Trường',
      desc: 'Công trình tín ngưỡng lâu đời, bảo tồn giá trị văn hóa dân gian Nam Bộ qua nhiều thế hệ.',
      details: '📍 Vị trí: Thị trấn Tân Túc và các khu vực lân cận Bình Chánh\n🏛️ Kiến trúc: Truyền thống Việt Nam, chạm khắc tinh xảo mang dấu ấn thời gian\n📅 Lễ hội: Các dịp lễ lớn trong năm có hoạt động cúng lễ sôi nổi\n🙏 Văn hóa: Nơi gìn giữ tín ngưỡng và sinh hoạt cộng đồng địa phương\n📸 Chụp ảnh: Không gian cổ kính, trang nghiêm rất đẹp'
    },
    sinhthai: {
      title: '🎣 Khu Ẩm Thực Sinh Thái Câu Cá Xuân Hương',
      desc: 'Khu du lịch kết hợp ẩm thực đồng quê và câu cá giải trí, lý tưởng cho cả gia đình.',
      details: '📍 Địa chỉ: Khu vực Bình Chánh, gần xã Bình Lợi\n🎣 Câu cá: Ao cá rộng, đủ loại cá nước ngọt tươi ngon\n🍽️ Ẩm thực: Đặc sản Nam Bộ được chế biến ngay tại chỗ từ cá tự câu\n👨👩👧 Phù hợp: Cả gia đình, nhóm bạn, tiệc cuối tuần\n🕐 Giờ hoạt động: 8:00 – 21:00 hằng ngày'
    }
  };

  function openDestModal(key) {
    const d = destinations[key];
    document.getElementById('modal-title').textContent = d.title;
    document.getElementById('modal-desc').textContent = d.desc;
    document.getElementById('modal-details').innerHTML = d.details.replace(/\n/g, '<br>');
    document.getElementById('destModal').classList.add('open');
  }

  function closeModal() { document.getElementById('destModal').classList.remove('open'); }

  // Payment info
  const payInfo = {
    cash: { title: '💵 Thanh Toán Tiền Mặt', desc: 'Phương thức truyền thống, thanh toán trực tiếp tại văn phòng.', details: '📍 Tại văn phòng: 1060 Đường Vườn Thơm, Xã Bình Lợi\n🚌 Thanh toán khi lên xe: Đối với nhóm đã xác nhận đặt tour\n💰 Đặt cọc: 30% giá tour khi đặt, còn lại thanh toán trước ngày khởi hành\n🕐 Giờ làm việc: 7:00 – 19:00 · Thứ 2 đến Chủ nhật' },
    bank: { title: '🏦 Chuyển Khoản Ngân Hàng', desc: 'Nhanh chóng, an toàn với các ngân hàng lớn tại Việt Nam.', details: '🏦 Vietcombank: 1234567890 - CONG TY TNHH BINH LOI TOURIST\n🏦 MB Bank: 0987654321 - CONG TY TNHH BINH LOI TOURIST\n🏦 Techcombank: 1122334455 - CONG TY TNHH BINH LOI TOURIST\n📝 Nội dung chuyển: [Họ tên] - [Số điện thoại] - [Tên tour]\n⏰ Xác nhận tự động trong vòng 15 phút' },
    ewallet: { title: '📱 Ví Điện Tử', desc: 'Phương thức thanh toán hiện đại, nhanh nhất trong vài giây.', details: '📱 MoMo: 0901 234 567 - Bình Lợi Tourist\n💙 ZaloPay: 0901 234 567\n🔴 VNPay: Quét mã QR tại trang thanh toán\n🟠 ShopeePay: ID: binhloi.tourist\n⚡ Xác nhận ngay lập tức sau khi thanh toán thành công' },
    card: { title: '💳 Thẻ Ngân Hàng', desc: 'Hỗ trợ tất cả thẻ quốc tế và nội địa, trả góp 0% lãi suất.', details: '💳 Visa / Mastercard / JCB: Thanh toán qua cổng VNPay\n🏧 ATM nội địa: Tất cả ngân hàng tại Việt Nam\n💰 Trả góp 0% lãi suất: Tour từ 2.000.000đ trở lên\n🔐 Bảo mật SSL 256-bit, không lưu thông tin thẻ\n📲 Thanh toán qua link gửi qua SMS/Zalo' }
  };

  function showPaymentInfo(type) {
    const p = payInfo[type];
    document.getElementById('pay-title').textContent = p.title;
    document.getElementById('pay-desc').textContent = p.desc;
    document.getElementById('pay-details').innerHTML = p.details.replace(/\n/g, '<br>');
    document.getElementById('payModal').classList.add('open');
  }

  // Chat widget
  let chatOpen = false;
  function toggleChat() {
    chatOpen = !chatOpen;
    document.getElementById('chatPopup').classList.toggle('open', chatOpen);
    document.querySelector('.chat-badge').style.display = chatOpen ? 'none' : 'flex';
  }
  function showChatPopup() {
    chatOpen = true;
    document.getElementById('chatPopup').classList.add('open');
  }
  function quickChat(msg) {
    document.getElementById('chatPopup').classList.remove('open');
    chatOpen = false;
    if (msg.includes('giá tour') || msg.includes('ưu đãi')) {
      location.href = '#tours';
    } else if (msg.includes('đặt tour')) {
      location.href = '#booking';
    }
  }

  // Close modals on overlay click
  document.querySelectorAll('.modal-overlay').forEach(o => {
    o.addEventListener('click', e => {
      if (e.target === o) o.classList.remove('open');
    });
  });
</script>
</body>
</html>
