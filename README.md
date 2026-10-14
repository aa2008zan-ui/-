<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>هلو | خدمات التواصل الاجتماعي والآيفون بلس والترويج</title>
  <!-- Google Fonts & FontAwesome Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    :root {
      --bg-color: #0b0f19;
      --card-bg: rgba(22, 28, 45, 0.7);
      --card-border: rgba(255, 255, 255, 0.08);
      --text-main: #f3f4f6;
      --text-muted: #9ca3af;
      --accent-insta: linear-gradient(135deg, #833ab4, #fd1d1d, #fcb045);
      --accent-telegram: linear-gradient(135deg, #2aabee, #229ed9);
      --accent-snap: linear-gradient(135deg, #fffc00, #f8d000);
      --accent-apple: linear-gradient(135deg, #ffd700, #ffa500);
      --accent-promo: linear-gradient(135deg, #10b981, #059669);
      --accent-whatsapp: #25d366;
      --radius: 16px;
      --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Cairo', sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-main);
      min-height: 100vh;
      line-height: 1.6;
      background-image: 
        radial-gradient(circle at 10% 20%, rgba(131, 58, 180, 0.15) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(34, 158, 217, 0.15) 0%, transparent 40%),
        radial-gradient(circle at 50% 50%, rgba(16, 185, 129, 0.08) 0%, transparent 50%);
      background-attachment: fixed;
      padding-bottom: 50px;
    }

    .container {
      width: 100%;
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 20px;
    }

    header {
      background: rgba(11, 15, 25, 0.85);
      backdrop-filter: blur(12px);
      position: sticky;
      top: 0;
      z-index: 1000;
      border-bottom: 1px solid var(--card-border);
      padding: 15px 0;
    }

    .nav-wrapper {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 28px;
      font-weight: 900;
      background: linear-gradient(135deg, #fff, #9ca3af);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .logo span {
      background: var(--accent-insta);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    #toast-container {
      position: fixed;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 9999;
      pointer-events: none;
    }

    .toast {
      background: rgba(30, 41, 59, 0.95);
      color: #fff;
      padding: 12px 24px;
      border-radius: 50px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 10px;
      opacity: 0;
      transform: translateY(-20px);
      transition: var(--transition);
    }

    .toast.show {
      opacity: 1;
      transform: translateY(0);
    }

    .hero {
      text-align: center;
      padding: 50px 0 30px;
    }

    .hero-badge {
      display: inline-block;
      padding: 6px 16px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--card-border);
      border-radius: 50px;
      font-size: 14px;
      margin-bottom: 20px;
      color: #38bdf8;
    }

    .hero h1 {
      font-size: 42px;
      font-weight: 800;
      margin-bottom: 15px;
      line-height: 1.2;
    }

    .hero p {
      color: var(--text-muted);
      font-size: 18px;
      max-width: 650px;
      margin: 0 auto 30px;
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 15px;
      margin-bottom: 40px;
    }

    .feature-item {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid var(--card-border);
      padding: 18px;
      border-radius: var(--radius);
      text-align: center;
    }

    .feature-item i {
      font-size: 26px;
      color: #38bdf8;
      margin-bottom: 10px;
    }

    .feature-item h4 {
      font-size: 16px;
      margin-bottom: 5px;
    }

    .feature-item p {
      font-size: 13px;
      color: var(--text-muted);
    }

    .section-title {
      font-size: 24px;
      font-weight: 700;
      margin-bottom: 25px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .experts-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-bottom: 50px;
    }

    .expert-card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: var(--radius);
      padding: 24px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      position: relative;
      overflow: hidden;
      backdrop-filter: blur(10px);
    }

    .expert-avatar {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      background: linear-gradient(135deg, #1e293b, #0f172a);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      margin-bottom: 15px;
      border: 2px solid rgba(255, 255, 255, 0.1);
      color: #38bdf8;
    }

    .expert-name {
      font-size: 20px;
      font-weight: 700;
      margin-bottom: 5px;
    }

    .expert-role {
      color: var(--text-muted);
      font-size: 14px;
      margin-bottom: 15px;
    }

    .expert-phone {
      direction: ltr;
      font-weight: 700;
      letter-spacing: 1px;
      margin-bottom: 15px;
      color: #25d366;
    }

    .btn-group {
      display: flex;
      gap: 10px;
      width: 100%;
    }

    .btn-whatsapp {
      flex: 2;
      background: #25d366;
      color: #000;
      font-weight: 700;
      padding: 10px;
      border-radius: 10px;
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      transition: var(--transition);
    }

    .btn-whatsapp:hover {
      background: #20ba5a;
      transform: translateY(-2px);
    }

    .btn-copy {
      flex: 1;
      background: rgba(255, 255, 255, 0.1);
      color: #fff;
      border: none;
      padding: 10px;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 600;
      transition: var(--transition);
    }

    .btn-copy:hover {
      background: rgba(255, 255, 255, 0.2);
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      margin-bottom: 50px;
    }

    .service-card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: var(--radius);
      padding: 25px;
      backdrop-filter: blur(10px);
      transition: var(--transition);
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .service-card:hover {
      transform: translateY(-5px);
      border-color: rgba(255, 255, 255, 0.2);
    }

    .badge-pop {
      position: absolute;
      top: -12px;
      left: 20px;
      background: #ef4444;
      color: #fff;
      font-size: 11px;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 50px;
      box-shadow: 0 4px 12px rgba(239, 68, 68, 0.4);
    }

    .service-header {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 20px;
    }

    .service-icon {
      width: 50px;
      height: 50px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
    }

    .icon-insta { background: var(--accent-insta); color: #fff; }
    .icon-telegram { background: var(--accent-telegram); color: #fff; }
    .icon-snap { background: var(--accent-snap); color: #000; }
    .icon-apple { background: var(--accent-apple); color: #000; }
    .icon-promo { background: var(--accent-promo); color: #fff; }

    .service-title {
      font-size: 20px;
      font-weight: 700;
    }

    .price-list {
      list-style: none;
      margin-bottom: 20px;
      flex-grow: 1;
    }

    .price-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px 0;
      border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    }

    .price-item:last-child {
      border-bottom: none;
    }

    .price-name {
      color: #e5e7eb;
      font-size: 15px;
    }

    .price-tag {
      font-weight: 700;
      color: #38bdf8;
      background: rgba(56, 189, 248, 0.1);
      padding: 4px 10px;
      border-radius: 6px;
      font-size: 14px;
    }

    .price-tag-gold {
      color: #ffd700;
      background: rgba(255, 215, 0, 0.1);
    }

    .price-tag-green {
      color: #10b981;
      background: rgba(16, 185, 129, 0.1);
    }

    .payments-box {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: var(--radius);
      padding: 25px;
      text-align: center;
      margin-bottom: 50px;
    }

    .payment-badge-group {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
      margin-top: 15px;
    }

    .pay-tag {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--card-border);
      padding: 10px 20px;
      border-radius: 10px;
      font-weight: 600;
      font-size: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .order-section {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: var(--radius);
      padding: 30px;
      backdrop-filter: blur(10px);
      max-width: 700px;
      margin: 0 auto 50px;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      margin-bottom: 8px;
      font-weight: 600;
      color: #d1d5db;
    }

    .form-control {
      width: 100%;
      padding: 12px 16px;
      background: rgba(0, 0, 0, 0.3);
      border: 1px solid var(--card-border);
      border-radius: 10px;
      color: #fff;
      font-size: 15px;
      outline: none;
      transition: var(--transition);
    }

    .form-control:focus {
      border-color: #38bdf8;
    }

    select.form-control option {
      background-color: #0f172a;
      color: #fff;
    }

    .btn-submit-group {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
      margin-top: 25px;
    }

    .btn-submit {
      padding: 14px;
      border-radius: 10px;
      border: none;
      font-weight: 700;
      font-size: 15px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      transition: var(--transition);
      color: #000;
    }

    .btn-abbas { background: #25d366; }
    .btn-ghaith { background: #38bdf8; }

    .btn-submit:hover {
      opacity: 0.9;
      transform: translateY(-2px);
    }

    footer {
      text-align: center;
      padding: 20px 0;
      color: var(--text-muted);
      border-top: 1px solid var(--card-border);
      font-size: 14px;
    }

    @media (max-width: 600px) {
      .hero h1 { font-size: 30px; }
      .btn-submit-group { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <div id="toast-container">
    <div id="toast" class="toast">
      <i class="fa-solid fa-circle-check" style="color: #25d366;"></i>
      <span id="toast-msg">تم النسخ بنجاح!</span>
    </div>
  </div>

  <header>
    <div class="container nav-wrapper">
      <div class="logo">
        <i class="fa-solid fa-bolt"></i> هلو <span>.HELLO</span>
      </div>
    </div>
  </header>

  <div class="container">
    <section class="hero">
      <span class="hero-badge"><i class="fa-solid fa-shield-halved"></i> المنصة الأولى لخدمات السوشيال ميديا والترويج وتطبيقات بلس</span>
      <h1>خدمات السوشيال ميديا والترويج الممول</h1>
      <p>استرجاع حسابات، توثيق، إعلانات وترويج ممول، اشتراكات تليجرام، سناب شات، وباقات بلس آيفون VIP بأسعار تنافسية.</p>
    </section>

    <div class="features-grid">
      <div class="feature-item">
        <i class="fa-solid fa-bolt-lightning"></i>
        <h4>تنفيذ سريع</h4>
        <p>تفعيل وترويج بأقصر وقت ممكن</p>
      </div>
      <div class="feature-item">
        <i class="fa-solid fa-user-shield"></i>
        <h4>ضمان وأمان</h4>
        <p>حماية معلوماتك وخصوصيتك 100%</p>
      </div>
      <div class="feature-item">
        <i class="fa-solid fa-headset"></i>
        <h4>دعم متواصل</h4>
        <p>مختصون جاهزون للرد والإجابة</p>
      </div>
    </div>

    <h2 class="section-title"><i class="fa-solid fa-headset" style="color: #25d366;"></i> التواصل المباشر مع المختصين</h2>
    <div class="experts-grid">
      <div class="expert-card">
        <div class="expert-avatar">
          <i class="fa-solid fa-user-gear"></i>
        </div>
        <div class="expert-name">المختص عباس</div>
        <div class="expert-role">دعم فني واسترجاع الحسابات والترويج</div>
        <div class="expert-phone">07744144831</div>
        <div class="btn-group">
          <a href="javascript:void(0)" onclick="openWhatsApp('9647744144831', 'مرحباً مختص عباس، أود الاستفسار عن الخدمات')" class="btn-whatsapp">
            <i class="fa-brands fa-whatsapp"></i> مراسلة
          </a>
          <button onclick="copyToClipboard('07744144831')" class="btn-copy">
            <i class="fa-regular fa-copy"></i> نسخ
          </button>
        </div>
      </div>

      <div class="expert-card">
        <div class="expert-avatar">
          <i class="fa-solid fa-user-check"></i>
        </div>
        <div class="expert-name">المختص غيث</div>
        <div class="expert-role">خدمات التوثيق والاشتراكات والترويج</div>
        <div class="expert-phone">07726874272</div>
        <div class="btn-group">
          <a href="javascript:void(0)" onclick="openWhatsApp('9647726874272', 'مرحباً مختص غيث، أود الاستفسار عن الخدمات')" class="btn-whatsapp">
            <i class="fa-brands fa-whatsapp"></i> مراسلة
          </a>
          <button onclick="copyToClipboard('07726874272')" class="btn-copy">
            <i class="fa-regular fa-copy"></i> نسخ
          </button>
        </div>
      </div>
    </div>

    <h2 class="section-title"><i class="fa-solid fa-list-check" style="color: #38bdf8;"></i> قائمة الخدمات والأسعار</h2>
    <div class="services-grid">
      
      <!-- Instagram Services -->
      <div class="service-card">
        <span class="badge-pop">الأكثر طلباً</span>
        <div class="service-header">
          <div class="service-icon icon-insta">
            <i class="fa-brands fa-instagram"></i>
          </div>
          <div class="service-title">خدمات إنستغرام</div>
        </div>
        <ul class="price-list">
          <li class="price-item">
            <span class="price-name">استرجاع حسابات (جميع الأنواع)</span>
            <span class="price-tag">حسب الحالة</span>
          </li>
          <li class="price-item">
            <span class="price-name">توثيق إنستغرام (3 أشهر)</span>
            <span class="price-tag">30,000 د.ع</span>
          </li>
          <li class="price-item">
            <span class="price-name">اشتراك بلس زيادة المشاهدات (شهري)</span>
            <span class="price-tag">5,000 د.ع</span>
          </li>
        </ul>
      </div>

      <!-- Paid Ads & Promotion -->
      <div class="service-card">
        <div class="service-header">
          <div class="service-icon icon-promo">
            <i class="fa-solid fa-bullhorn"></i>
          </div>
          <div class="service-title">خدمات الترويج الممول</div>
        </div>
        <ul class="price-list">
          <li class="price-item">
            <span class="price-name">ترويج ممول (إنستغرام)</span>
            <span class="price-tag price-tag-green">4 - 10 آلاف / يومياً</span>
          </li>
          <li class="price-item">
            <span class="price-name">ترويج ممول (فيسبوك)</span>
            <span class="price-tag price-tag-green">4 - 10 آلاف / يومياً</span>
          </li>
          <li class="price-item">
            <span class="price-name">ترويج ممول (تيك توك)</span>
            <span class="price-tag price-tag-green">4 - 10 آلاف / يومياً</span>
          </li>
          <li class="price-item">
            <span class="price-name">ترويج ممول (تليجرام)</span>
            <span class="price-tag price-tag-green">4 - 10 آلاف / يومياً</span>
          </li>
        </ul>
      </div>

      <!-- Telegram Services -->
      <div class="service-card">
        <div class="service-header">
          <div class="service-icon icon-telegram">
            <i class="fa-brands fa-telegram"></i>
          </div>
          <div class="service-title">تليجرام بريميوم</div>
        </div>
        <ul class="price-list">
          <li class="price-item">
            <span class="price-name">تفعيل اشتراك شهر</span>
            <span class="price-tag">8,000 د.ع</span>
          </li>
          <li class="price-item">
            <span class="price-name">إهداء 3 أشهر</span>
            <span class="price-tag">24,000 د.ع</span>
          </li>
          <li class="price-item">
            <span class="price-name">إهداء 6 أشهر</span>
            <span class="price-tag">30,000 د.ع</span>
          </li>
          <li class="price-item">
            <span class="price-name">إهداء سنوي (12 شهر)</span>
            <span class="price-tag">50,000 د.ع</span>
          </li>
        </ul>
      </div>

      <!-- Snapchat Services -->
      <div class="service-card">
        <div class="service-header">
          <div class="service-icon icon-snap">
            <i class="fa-brands fa-snapchat"></i>
          </div>
          <div class="service-title">توثيق سناب شات</div>
        </div>
        <ul class="price-list">
          <li class="price-item">
            <span class="price-name">تفعيل توثيق (اشتراك شهر)</span>
            <span class="price-tag">5,000 د.ع</span>
          </li>
          <li class="price-item">
            <span class="price-name">تفعيل توثيق (اشتراك سنوي)</span>
            <span class="price-tag">15,000 د.ع</span>
          </li>
        </ul>
      </div>

      <!-- iPhone Plus Services -->
      <div class="service-card">
        <div class="service-header">
          <div class="service-icon icon-apple">
            <i class="fa-brands fa-apple"></i>
          </div>
          <div class="service-title">تطبيقات بلس آيفون VIP</div>
        </div>
        <ul class="price-list">
          <li class="price-item">
            <span class="price-name">اشتراك بلس آيفون VIP (سنوي)</span>
            <span class="price-tag price-tag-gold">35,000 د.ع</span>
          </li>
        </ul>
      </div>

    </div>

    <div class="payments-box">
      <h3><i class="fa-solid fa-wallet" style="color: #25d366;"></i> طرق الدفع المقبولة</h3>
      <div class="payment-badge-group">
        <div class="pay-tag"><i class="fa-solid fa-mobile-screen" style="color: #e11d48;"></i> زين كاش (ZainCash)</div>
        <div class="pay-tag"><i class="fa-solid fa-sim-card" style="color: #0284c7;"></i> كارتات آسياسيل</div>
        <div class="pay-tag"><i class="fa-solid fa-credit-card" style="color: #f59e0b;"></i> ماستركارد / كي كارد</div>
      </div>
    </div>

    <section class="order-section">
      <h2 class="section-title" style="justify-content: center; margin-bottom: 20px;">
        <i class="fa-solid fa-paper-plane" style="color: #25d366;"></i> إرسال طلب سريع
      </h2>
      <form id="orderForm" onsubmit="event.preventDefault();">
        <div class="form-group">
          <label>اسمك الكامل / اللقب</label>
          <input type="text" id="custName" class="form-control" placeholder="أدخل اسمك الكريم" required>
        </div>

        <div class="form-group">
          <label>اختر الخدمة المطلوبة</label>
          <select id="custService" class="form-control" required>
            <option value="" disabled selected>-- اختر الخدمة --</option>
            <option value="استرجاع حساب إنستغرام">إنستغرام: استرجاع حساب</option>
            <option value="توثيق إنستغرام (3 أشهر - 30 ألف)">إنستغرام: توثيق 3 أشهر (30,000 د.ع)</option>
            <option value="إنستغرام بلس زيادة المشاهدات (شهر - 5 آلاف)">إنستغرام: بلس زيادة المشاهدات (5,000 د.ع)</option>
            <option value="ترويج ممول إنستغرام (4 - 10 آلاف/يوم)">ترويج ممول: إنستغرام (4,000 - 10,000 د.ع/يومياً)</option>
            <option value="ترويج ممول فيسبوك (4 - 10 آلاف/يوم)">ترويج ممول: فيسبوك (4,000 - 10,000 د.ع/يومياً)</option>
            <option value="ترويج ممول تيك توك (4 - 10 آلاف/يوم)">ترويج ممول: تيك توك (4,000 - 10,000 د.ع/يومياً)</option>
            <option value="ترويج ممول تليجرام (4 - 10 آلاف/يوم)">ترويج ممول: تليجرام (4,000 - 10,000 د.ع/يومياً)</option>
            <option value="تليجرام بريميوم شهر (8 آلاف)">تليجرام: بريميوم شهر (8,000 د.ع)</option>
            <option value="تليجرام بريميوم 3 أشهر (24 ألف)">تليجرام: إهداء 3 أشهر (24,000 د.ع)</option>
            <option value="تليجرام بريميوم 6 أشهر (30 ألف)">تليجرام: إهداء 6 أشهر (30,000 د.ع)</option>
            <option value="تليجرام بريميوم سنوي (50 ألف)">تليجرام: إهداء سنوي (50,000 د.ع)</option>
            <option value="سناب شات توثيق شهر (5 آلاف)">سناب شات: توثيق شهر (5,000 د.ع)</option>
            <option value="سناب شات توثيق سنوي (15 ألف)">سناب شات: توثيق سنوي (15,000 د.ع)</option>
            <option value="آيفون بلس VIP سنوي (35 ألف)">آيفون بلس VIP: اشتراك سنوي (35,000 د.ع)</option>
          </select>
        </div>

        <div class="form-group">
          <label>يوزر الحساب / رقم الهاتف</label>
          <input type="text" id="custHandle" class="form-control" placeholder="مثال: @username أو رقم الموبايل" required>
        </div>

        <div class="form-group">
          <label>ملاحظات إضافية (اختياري)</label>
          <textarea id="custNotes" class="form-control" rows="3" placeholder="أكتب أي تفاصيل إضافية أو مدة الترويج المطلوبة..."></textarea>
        </div>

        <div class="btn-submit-group">
          <button type="button" onclick="sendOrder('9647744144831')" class="btn-submit btn-abbas">
            <i class="fa-brands fa-whatsapp"></i> إرسال للمختص عباس
          </button>
          <button type="button" onclick="sendOrder('9647726874272')" class="btn-submit btn-ghaith">
            <i class="fa-brands fa-whatsapp"></i> إرسال للمختص غيث
          </button>
        </div>
      </form>
    </section>

  </div>

  <footer>
    <p>جميع الحقوق محفوظة &copy; 2026 موقع **هلو (HELLO)** لخدمات التواصل الاجتماعي والترويج وتطبيقات بلس</p>
  </footer>

  <script>
    function openWhatsApp(phone, text) {
      const url = `https://api.whatsapp.com/send?phone=${phone}&text=${encodeURIComponent(text)}`;
      window.open(url, '_blank');
    }

    function copyToClipboard(text) {
      navigator.clipboard.writeText(text).then(() => {
        showToast("تم نسخ الرقم: " + text);
      }).catch(err => {
        showToast("الرقم: " + text);
      });
    }

    function showToast(message) {
      const toast = document.getElementById("toast");
      const toastMsg = document.getElementById("toast-msg");
      toastMsg.innerText = message;
      toast.classList.add("show");
      setTimeout(() => {
        toast.classList.remove("show");
      }, 3000);
    }

    function sendOrder(phoneTarget) {
      const name = document.getElementById("custName").value.trim();
      const service = document.getElementById("custService").value;
      const handle = document.getElementById("custHandle").value.trim();
      const notes = document.getElementById("custNotes").value.trim();

      if (!name || !service || !handle) {
        showToast("يرجى ملء جميع الحقول المطلوبة قبل إرسال الطلب!");
        return;
      }

      let msg = `*طلب جديد من الموقع:* %0A%0A`;
      msg += `👤 *الاسم:* ${name}%0A`;
      msg += `📌 *الخدمة:* ${service}%0A`;
      msg += `🔗 *اليوزر/الهاتف:* ${handle}%0A`;
      if (notes) {
        msg += `📝 *ملاحظات:* ${notes}%0A`;
      }

      openWhatsApp(phoneTarget, msg);
    }
  </script>
</body>
</html>
