[file.html](https://github.com/user-attachments/files/28174585/file.html)
# airo<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AIRO — Air. Comfort. Elevated.</title>
  <script src="[cdn.tailwindcss.com](https://cdn.tailwindcss.com)"></script>
  <link href="[fonts.googleapis.com](https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@400;500;600;700&display=swap)" rel="stylesheet" />
  <link rel="stylesheet" href="[cdnjs.cloudflare.com](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css)" />
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    :root {
      --charcoal: #0d0d0f;
      --dark: #111114;
      --panel: #161619;
      --card: #1a1a1e;
      --border: rgba(255,255,255,0.07);
      --silver: #c0c0c8;
      --silver-light: #e8e8f0;
      --beige: #f5f0eb;
      --accent: #d4d0cc;
      --gold-soft: #c8bfb0;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--charcoal);
      color: #e8e8ec;
      overflow-x: hidden;
    }

    /* ─── SCROLLBAR ─── */
    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: var(--dark); }
    ::-webkit-scrollbar-thumb { background: #333; border-radius: 2px; }

    /* ─── NAVBAR ─── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      padding: 0 48px;
      height: 72px;
      display: flex; align-items: center; justify-content: space-between;
      background: rgba(13,13,15,0.82);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
      transition: all 0.3s ease;
    }

    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 22px;
      font-weight: 700;
      letter-spacing: 6px;
      background: linear-gradient(135deg, #ffffff 0%, #c0c0c8 50%, #888898 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .nav-links { display: flex; gap: 36px; align-items: center; }
    .nav-links a {
      font-size: 13px;
      font-weight: 500;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: #9090a0;
      text-decoration: none;
      transition: color 0.25s;
    }
    .nav-links a:hover { color: #e8e8f0; }

    .nav-cta {
      background: linear-gradient(135deg, #ffffff15, #ffffff08);
      border: 1px solid rgba(255,255,255,0.15);
      color: #e8e8f0 !important;
      padding: 9px 22px;
      border-radius: 50px;
      font-size: 12px !important;
      letter-spacing: 1.5px;
      transition: all 0.3s ease !important;
    }
    .nav-cta:hover {
      background: linear-gradient(135deg, #ffffff25, #ffffff12) !important;
      border-color: rgba(255,255,255,0.3) !important;
      color: #fff !important;
      transform: translateY(-1px);
    }

    /* ─── HERO ─── */
    #hero {
      min-height: 100vh;
      padding: 0 48px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      gap: 80px;
      position: relative;
      overflow: hidden;
      background: radial-gradient(ellipse 80% 60% at 70% 50%, #1e1e28 0%, #0d0d0f 60%);
    }

    #hero::before {
      content: '';
      position: absolute;
      top: -20%;
      right: -10%;
      width: 700px; height: 700px;
      background: radial-gradient(circle, rgba(180,180,220,0.04) 0%, transparent 70%);
      border-radius: 50%;
      pointer-events: none;
    }

    #hero::after {
      content: '';
      position: absolute;
      bottom: 10%;
      left: 5%;
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(200,191,176,0.03) 0%, transparent 70%);
      border-radius: 50%;
      pointer-events: none;
    }

    .hero-left { padding-top: 72px; position: relative; z-index: 2; }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 50px;
      padding: 6px 16px;
      font-size: 11px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #9090a8;
      margin-bottom: 32px;
    }
    .hero-badge-dot {
      width: 6px; height: 6px;
      background: #c8bfb0;
      border-radius: 50%;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.5; transform: scale(0.85); }
    }

    .hero-headline {
      font-size: clamp(42px, 5.5vw, 80px);
      font-weight: 800;
      line-height: 1.05;
      letter-spacing: -2px;
      margin-bottom: 24px;
    }
    .hero-headline-line1 { color: #f0f0f4; display: block; }
    .hero-headline-line2 {
      display: block;
      background: linear-gradient(135deg, #c0c0c8 0%, #888898 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero-sub {
      font-size: 16px;
      font-weight: 400;
      color: #70708080;
      line-height: 1.7;
      max-width: 380px;
      margin-bottom: 48px;
      color: #808090;
    }

    .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }

    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: linear-gradient(135deg, #e8e8f0 0%, #c0c0cc 100%);
      color: #0d0d0f;
      font-size: 13px;
      font-weight: 700;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      padding: 16px 32px;
      border-radius: 50px;
      border: none;
      cursor: pointer;
      text-decoration: none;
      transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      box-shadow: 0 8px 32px rgba(192,192,200,0.2);
    }
    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 16px 48px rgba(192,192,200,0.35);
      background: linear-gradient(135deg, #ffffff 0%, #d8d8e8 100%);
    }

    .btn-secondary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: transparent;
      color: #9090a8;
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      padding: 16px 32px;
      border-radius: 50px;
      border: 1px solid rgba(255,255,255,0.12);
      cursor: pointer;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    .btn-secondary:hover {
      color: #e8e8f0;
      border-color: rgba(255,255,255,0.25);
      background: rgba(255,255,255,0.04);
      transform: translateY(-2px);
    }

    .hero-stats {
      display: flex;
      gap: 40px;
      margin-top: 64px;
      padding-top: 40px;
      border-top: 1px solid var(--border);
    }
    .hero-stat-num {
      font-size: 28px;
      font-weight: 800;
      color: #e8e8f0;
      letter-spacing: -1px;
    }
    .hero-stat-label {
      font-size: 11px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: #606070;
      margin-top: 4px;
    }

    /* ─── HERO PRODUCT CARD ─── */
    .hero-right {
      display: flex;
      justify-content: center;
      align-items: center;
      padding-top: 72px;
      position: relative;
      z-index: 2;
    }

    .hero-product-card {
      position: relative;
      width: 100%;
      max-width: 480px;
      background: linear-gradient(145deg, #1e1e24 0%, #16161a 50%, #121216 100%);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 32px;
      padding: 48px 40px;
      box-shadow:
        0 0 0 1px rgba(255,255,255,0.03),
        0 40px 100px rgba(0,0,0,0.6),
        0 0 80px rgba(180,180,220,0.04);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }
    .hero-product-card:hover {
      transform: translateY(-8px) rotateX(2deg);
      box-shadow:
        0 0 0 1px rgba(255,255,255,0.06),
        0 60px 120px rgba(0,0,0,0.7),
        0 0 100px rgba(180,180,220,0.08);
    }

    .hero-product-card::before {
      content: '';
      position: absolute;
      top: 0; left: 20%; right: 20%; height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
    }

    .hero-card-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(200,191,176,0.1);
      border: 1px solid rgba(200,191,176,0.2);
      color: #c8bfb0;
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 5px 14px;
      border-radius: 50px;
      margin-bottom: 24px;
    }

    .hero-card-img-wrap {
      width: 100%;
      height: 220px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(ellipse at center, rgba(255,255,255,0.04) 0%, transparent 70%);
      border-radius: 20px;
      margin-bottom: 32px;
      position: relative;
      overflow: hidden;
    }

    .fan-svg-container {
      position: relative;
      width: 160px;
      height: 160px;
    }

    .fan-svg-container svg {
      width: 100%;
      height: 100%;
      filter: drop-shadow(0 0 30px rgba(200,200,220,0.15));
    }

    @keyframes spin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }

    .fan-blades {
      transform-origin: 50% 50%;
      animation: spin 3s linear infinite;
    }

    .hero-card-name {
      font-size: 22px;
      font-weight: 700;
      color: #f0f0f4;
      letter-spacing: -0.5px;
      margin-bottom: 6px;
    }
    .hero-card-sub {
      font-size: 13px;
      color: #606070;
      letter-spacing: 1px;
      margin-bottom: 24px;
    }

    .hero-card-price-row {
      display: flex;
      align-items: baseline;
      gap: 12px;
      margin-bottom: 28px;
    }
    .price-current {
      font-size: 32px;
      font-weight: 800;
      color: #f0f0f4;
      letter-spacing: -1px;
    }
    .price-original {
      font-size: 18px;
      color: #40404a;
      text-decoration: line-through;
      font-weight: 500;
    }
    .price-badge {
      background: rgba(200,191,176,0.12);
      border: 1px solid rgba(200,191,176,0.2);
      color: #c8bfb0;
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 1px;
      padding: 3px 10px;
      border-radius: 50px;
    }

    .hero-card-features {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 28px;
    }
    .hero-card-feature-pill {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
      color: #808090;
      font-size: 11px;
      letter-spacing: 0.5px;
      padding: 5px 12px;
      border-radius: 50px;
    }

    .btn-glow {
      display: block;
      width: 100%;
      text-align: center;
      background: linear-gradient(135deg, #e8e8f0 0%, #c0c0cc 100%);
      color: #0d0d0f;
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 16px;
      border-radius: 16px;
      border: none;
      cursor: pointer;
      text-decoration: none;
      transition: all 0.3s ease;
      box-shadow: 0 8px 32px rgba(192,192,200,0.2);
      position: relative;
      overflow: hidden;
    }
    .btn-glow::before {
      content: '';
      position: absolute;
      top: -50%; left: -100%;
      width: 60%; height: 200%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
      transform: skewX(-20deg);
      transition: left 0.5s ease;
    }
    .btn-glow:hover::before { left: 150%; }
    .btn-glow:hover {
      transform: translateY(-2px);
      box-shadow: 0 16px 48px rgba(192,192,200,0.35);
    }

    /* ─── SECTION COMMON ─── */
    .section-label {
      font-size: 10px;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: #505060;
      margin-bottom: 16px;
    }
    .section-title {
      font-size: clamp(32px, 4vw, 52px);
      font-weight: 800;
      letter-spacing: -1.5px;
      line-height: 1.1;
      color: #f0f0f4;
    }
    .section-title span {
      background: linear-gradient(135deg, #c0c0c8 0%, #808090 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* ─── FEATURED PRODUCT ─── */
    #featured {
      padding: 120px 48px;
      background: var(--dark);
      position: relative;
      overflow: hidden;
    }
    #featured::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
    }

    .featured-grid {
      max-width: 1280px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4px;
      border-radius: 28px;
      overflow: hidden;
      box-shadow: 0 40px 120px rgba(0,0,0,0.6);
    }

    .featured-img-panel {
      background: linear-gradient(145deg, #1a1a20, #141418);
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 80px 60px;
      position: relative;
      overflow: hidden;
      min-height: 560px;
    }
    .featured-img-panel::before {
      content: '';
      position: absolute;
      width: 500px; height: 500px;
      background: radial-gradient(circle, rgba(200,200,240,0.05) 0%, transparent 70%);
      border-radius: 50%;
    }

    .featured-fan-large {
      position: relative;
      z-index: 2;
      width: 280px;
      height: 280px;
      filter: drop-shadow(0 0 60px rgba(200,200,220,0.12));
    }
    .featured-fan-large svg {
      width: 100%;
      height: 100%;
    }

    .featured-details-panel {
      background: #111114;
      padding: 72px 64px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      border-left: 1px solid var(--border);
    }

    .features-list {
      list-style: none;
      margin: 40px 0;
      display: flex;
      flex-direction: column;
      gap: 18px;
    }
    .feature-item {
      display: flex;
      align-items: center;
      gap: 16px;
      padding: 16px 20px;
      background: rgba(255,255,255,0.02);
      border: 1px solid rgba(255,255,255,0.05);
      border-radius: 14px;
      transition: all 0.25s ease;
    }
    .feature-item:hover {
      background: rgba(255,255,255,0.04);
      border-color: rgba(255,255,255,0.1);
      transform: translateX(4px);
    }
    .feature-check {
      width: 28px; height: 28px;
      background: rgba(200,191,176,0.12);
      border: 1px solid rgba(200,191,176,0.2);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      color: #c8bfb0;
      font-size: 11px;
    }
    .feature-text {
      font-size: 14px;
      font-weight: 500;
      color: #c0c0c8;
      letter-spacing: 0.5px;
    }

    .featured-price-row {
      display: flex;
      align-items: baseline;
      gap: 16px;
      margin-bottom: 36px;
    }

    .featured-price-current {
      font-size: 48px;
      font-weight: 900;
      color: #f0f0f4;
      letter-spacing: -2px;
    }
    .featured-price-original {
      font-size: 24px;
      color: #303038;
      text-decoration: line-through;
      font-weight: 500;
    }
    .featured-price-save {
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 1px;
      background: rgba(200,191,176,0.12);
      border: 1px solid rgba(200,191,176,0.2);
      color: #c8bfb0;
      padding: 4px 12px;
      border-radius: 50px;
    }

    /* ─── COMING SOON ─── */
    #coming-soon {
      padding: 120px 48px;
      background: var(--charcoal);
      position: relative;
    }
    #coming-soon::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.05), transparent);
    }

    .coming-soon-header {
      text-align: center;
      margin-bottom: 72px;
      max-width: 560px;
      margin-left: auto;
      margin-right: auto;
    }
    .coming-soon-header p {
      font-size: 16px;
      color: #606070;
      line-height: 1.7;
      margin-top: 20px;
    }

    .coming-soon-grid {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }

    .coming-card {
      background: linear-gradient(145deg, #161619, #121215);
      border: 1px solid rgba(255,255,255,0.06);
      border-radius: 28px;
      padding: 56px 40px;
      text-align: center;
      position: relative;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }
    .coming-card:hover {
      transform: translateY(-8px);
      border-color: rgba(255,255,255,0.12);
      box-shadow: 0 32px 80px rgba(0,0,0,0.5);
    }
    .coming-card::before {
      content: '';
      position: absolute;
      top: 0; left: 15%; right: 15%; height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.08), transparent);
    }

    .coming-icon {
      width: 72px; height: 72px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 32px;
      font-size: 28px;
      color: #606070;
      transition: all 0.3s ease;
    }
    .coming-card:hover .coming-icon {
      background: rgba(200,191,176,0.08);
      border-color: rgba(200,191,176,0.15);
      color: #c8bfb0;
    }

    .coming-card-title {
      font-size: 20px;
      font-weight: 700;
      color: #d0d0d8;
      letter-spacing: -0.5px;
      margin-bottom: 12px;
    }
    .coming-card-sub {
      font-size: 13px;
      color: #505060;
      line-height: 1.6;
      margin-bottom: 32px;
    }

    .coming-soon-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
      color: #606070;
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 7px 18px;
      border-radius: 50px;
    }

    /* ─── REVIEWS ─── */
    #reviews {
      padding: 120px 48px;
      background: var(--dark);
      position: relative;
      overflow: hidden;
    }
    #reviews::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
    }

    .reviews-header {
      text-align: center;
      margin-bottom: 72px;
    }
    .reviews-header p {
      font-size: 16px;
      color: #606070;
      margin-top: 16px;
    }

    .reviews-grid {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }

    .review-card {
      background: rgba(255,255,255,0.03);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255,255,255,0.07);
      border-radius: 24px;
      padding: 40px 36px;
      transition: all 0.35s ease;
      position: relative;
      overflow: hidden;
    }
    .review-card:hover {
      background: rgba(255,255,255,0.05);
      border-color: rgba(255,255,255,0.12);
      transform: translateY(-6px);
      box-shadow: 0 24px 60px rgba(0,0,0,0.4);
    }
    .review-card::before {
      content: '';
      position: absolute;
      top: 0; left: 15%; right: 15%; height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
    }

    .review-stars {
      display: flex;
      gap: 4px;
      margin-bottom: 20px;
    }
    .review-stars i { color: #c8bfb0; font-size: 13px; }

    .review-text {
      font-size: 15px;
      color: #909098;
      line-height: 1.7;
      margin-bottom: 28px;
      font-style: italic;
    }

    .reviewer {
      display: flex;
      align-items: center;
      gap: 14px;
    }
    .reviewer-avatar {
      width: 40px; height: 40px;
      border-radius: 50%;
      background: linear-gradient(135deg, #2a2a32, #1e1e26);
      border: 1px solid rgba(255,255,255,0.08);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 15px;
      font-weight: 700;
      color: #808090;
    }
    .reviewer-name {
      font-size: 14px;
      font-weight: 600;
      color: #d0d0d8;
    }
    .reviewer-tag {
      font-size: 11px;
      color: #505060;
      margin-top: 2px;
      letter-spacing: 0.5px;
    }
    .reviewer-verified {
      margin-left: auto;
      font-size: 10px;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #c8bfb0;
      background: rgba(200,191,176,0.08);
      border: 1px solid rgba(200,191,176,0.15);
      padding: 3px 10px;
      border-radius: 50px;
    }

    /* ─── BUSINESS ─── */
    #business {
      padding: 120px 48px;
      background: linear-gradient(180deg, var(--charcoal) 0%, #0a0a0d 100%);
      position: relative;
      overflow: hidden;
    }
    #business::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.05), transparent);
    }
    #business::after {
      content: '';
      position: absolute;
      bottom: -20%;
      right: -5%;
      width: 600px; height: 600px;
      background: radial-gradient(circle, rgba(200,191,176,0.02) 0%, transparent 70%);
      border-radius: 50%;
      pointer-events: none;
    }

    .business-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: center;
    }

    .business-left .section-label { margin-bottom: 20px; }

    .business-desc {
      font-size: 16px;
      color: #606070;
      line-height: 1.8;
      margin: 24px 0 48px;
    }

    .business-sectors {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-bottom: 48px;
    }
    .business-sector {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 14px 18px;
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(255,255,255,0.06);
      border-radius: 12px;
      font-size: 13px;
      color: #909098;
      transition: all 0.25s ease;
    }
    .business-sector:hover {
      background: rgba(255,255,255,0.05);
      color: #c0c0c8;
      transform: translateX(3px);
    }
    .business-sector i { color: #505060; font-size: 14px; width: 16px; }

    .business-right {
      background: linear-gradient(145deg, #161619, #121215);
      border: 1px solid rgba(255,255,255,0.07);
      border-radius: 28px;
      padding: 56px 48px;
      position: relative;
      overflow: hidden;
    }
    .business-right::before {
      content: '';
      position: absolute;
      top: 0; left: 15%; right: 15%; height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
    }

    .business-right h3 {
      font-size: 26px;
      font-weight: 800;
      color: #f0f0f4;
      letter-spacing: -0.5px;
      margin-bottom: 12px;
    }
    .business-right p {
      font-size: 14px;
      color: #606070;
      line-height: 1.7;
      margin-bottom: 36px;
    }

    .business-perks {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 14px;
      margin-bottom: 40px;
    }
    .business-perk {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 14px;
      color: #909098;
    }
    .business-perk i { color: #c8bfb0; font-size: 12px; }

    .btn-outline-silver {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: transparent;
      color: #e8e8f0;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 16px 32px;
      border-radius: 14px;
      border: 1px solid rgba(255,255,255,0.15);
      cursor: pointer;
      text-decoration: none;
      transition: all 0.3s ease;
      width: 100%;
      justify-content: center;
    }
    .btn-outline-silver:hover {
      background: rgba(255,255,255,0.04);
      border-color: rgba(255,255,255,0.3);
      box-shadow: 0 8px 32px rgba(0,0,0,0.3);
      transform: translateY(-2px);
    }

    /* ─── CHECKOUT ─── */
    #checkout {
      padding: 120px 48px;
      background: var(--dark);
      position: relative;
      overflow: hidden;
    }
    #checkout::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
    }

    .checkout-inner {
      max-width: 560px;
      margin: 0 auto;
    }
    .checkout-header {
      text-align: center;
      margin-bottom: 48px;
    }
    .checkout-header p {
      font-size: 15px;
      color: #606070;
      margin-top: 16px;
    }

    .checkout-card {
      background: linear-gradient(145deg, #161619, #121215);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 28px;
      overflow: hidden;
      box-shadow: 0 40px 100px rgba(0,0,0,0.5);
      position: relative;
    }
    .checkout-card::before {
      content: '';
      position: absolute;
      top: 0; left: 15%; right: 15%; height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
    }

    .checkout-top {
      padding: 40px 40px 32px;
      border-bottom: 1px solid rgba(255,255,255,0.06);
      display: flex;
      align-items: center;
      gap: 24px;
    }
