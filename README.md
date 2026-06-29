<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أورانتوس | شركة تقنية قابضة سورية</title>
    <meta name="description" content="أورانتوس هي منظومة تقنية سورية مكرسة لبناء وامتلاك منصات رقمية مبتكرة، وبنية تحتية مالية، وشبكات ذكاء اصطناعي متطورة.">
    
    <!-- خطوط بريميوم تدعم العربية -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Tajawal:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <!-- أيقونة التبويب للموقع (Favicon) -->
<link rel="icon" type="image/png" href="logos/orantos-main.png">
    <!-- نظام أيقونات لوكيد -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        /* --- العمارة التصميمية والمتغيرات المستوحاة من الشعار --- */
        :root {
            --font-sans: 'Tajawal', 'Plus Jakarta Sans', sans-serif;
            
            /* لوحة ألوان أورانتوس الفاخرة - الوضع المضيء (مستوحاة من image_d9c7be_2.jpg) */
            --bg-main: #ffffff;
            --bg-surface: #f4f7fa;
            --bg-card: rgba(255, 255, 255, 0.8);
            --border-color: rgba(10, 53, 124, 0.08);
            --text-primary: #0a357c; /* الأزرق الداكن الملكي من الشعار */
            --text-secondary: #334e68;
            --text-muted: #627d98;
            --primary: #0a357c;
            --accent: #00b4b4; /* الأزرق الفيروزي / المضيء من الشعار */
            --glass-bg: rgba(255, 255, 255, 0.85);
            --glass-border: rgba(10, 53, 124, 0.06);
            --shadow: 0 4px 6px -1px rgba(10, 53, 124, 0.05), 0 20px 40px -12px rgba(10, 53, 124, 0.08);
            --gradient-text: linear-gradient(135deg, #0a357c 0%, #00b4b4 100%);
        }

        [data-theme="dark"] {
            /* لوحة ألوان أورانتوس الفاخرة - الوضع الداكن السيبراني */
            --bg-main: #040b14;
            --bg-surface: #071526;
            --bg-card: rgba(7, 21, 38, 0.5);
            --border-color: rgba(255, 255, 255, 0.05);
            --text-primary: #f0f4f8;
            --text-secondary: #9fb3c8;
            --text-muted: #627d98;
            --primary: #f0f4f8;
            --accent: #00b4b4;
            --glass-bg: rgba(4, 11, 20, 0.85);
            --glass-border: rgba(255, 255, 255, 0.05);
            --shadow: 0 25px 60px -15px rgba(0, 0, 0, 0.5);
            --gradient-text: linear-gradient(135deg, #ffffff 0%, #00b4b4 100%);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            transition: background-color 0.4s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        html {
            scroll-behavior: smooth;
            font-family: var(--font-sans);
            background-color: var(--bg-main);
            color: var(--text-primary);
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        body {
            line-height: 1.8;
        }

        section {
            padding: 140px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        /* --- الأنماط الطبوغرافية --- */
        h1, h2, h3, h4 {
            font-weight: 700;
            letter-spacing: -0.02em;
            line-height: 1.25;
        }

        p {
            color: var(--text-secondary);
            font-size: 1.05rem;
        }

        .text-accent {
            color: var(--accent);
            text-transform: uppercase;
            font-size: 0.9rem;
            font-weight: 700;
            letter-spacing: 0.1em;
            margin-bottom: 15px;
            display: inline-block;
        }

        .section-intro {
            max-width: 750px;
            margin-bottom: 70px;
        }

        .section-intro h2 {
            font-size: 2.8rem;
            background: var(--gradient-text);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
        }

        /* --- عناصر واجهة المستخدم الممتازة --- */
        .btn {
            display: inline-flex;
            align-items: center;
            padding: 14px 32px;
            font-weight: 600;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.95rem;
            cursor: pointer;
            gap: 10px;
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .btn-primary {
            background-color: var(--primary);
            color: var(--bg-main);
            border: 1px solid var(--primary);
        }

        .btn-primary:hover {
            opacity: 0.9;
            transform: translateY(-1px);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--text-primary);
            border: 1px solid var(--border-color);
        }

        .btn-secondary:hover {
            background-color: var(--bg-surface);
            border-color: var(--text-primary);
        }

        .glass-panel {
            background: var(--bg-card);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            border-radius: 12px;
            box-shadow: var(--shadow);
            padding: 40px;
            transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        /* --- نظام حركات التمرير --- */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 1s cubic-bezier(0.16, 1, 0.3, 1), transform 1s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- شريط التنقل الثابت --- */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: var(--glass-bg);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border-bottom: 1px solid var(--glass-border);
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--text-primary);
            text-decoration: none;
            letter-spacing: -0.02em;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        /* تم تحديث هيكل الشعار البرمجي ليطابق الروح الدائرية والانسيابية في صورة الشعار */
        .logo-mark {
            width: 28px;
            height: 28px;
            border: 3px solid var(--text-primary);
            border-top-color: var(--accent);
            border-bottom-color: var(--accent);
            border-radius: 50%;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .logo-mark::after {
            content: '';
            width: 14px;
            height: 3px;
            background: var(--gradient-text);
            position: absolute;
            transform: rotate(-30deg);
            border-radius: 2px;
        }

        .nav-links {
            display: flex;
            gap: 40px;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-secondary);
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        .nav-actions {
            display: flex;
            align-items: center;
            gap: 24px;
        }

        .theme-toggle {
            background: none;
            border: none;
            color: var(--text-primary);
            cursor: pointer;
            padding: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* --- واجهة هيرو (Hero Section) --- */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            padding-top: 140px;
            background: radial-gradient(circle at 20% 30%, rgba(0, 180, 180, 0.05) 0%, transparent 50%);
        }

        .hero-layout {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 80px;
            align-items: center;
            width: 100%;
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 800;
            line-height: 1.15;
            margin-bottom: 30px;
            background: var(--gradient-text);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-content p {
            font-size: 1.25rem;
            color: var(--text-secondary);
            margin-bottom: 45px;
            font-weight: 400;
            max-width: 680px;
            line-height: 1.7;
        }

        .hero-actions {
            display: flex;
            gap: 20px;
        }

        /* محاكاة بصرية تجريدية مستوحاة من انسيابية شعار الشركة المعطى */
        .hero-visual {
            display: flex;
            justify-content: center;
            position: relative;
        }

        .sphere-container {
            width: 380px;
            height: 380px;
            border: 1px solid var(--border-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            animation: slowRotate 30s linear infinite;
        }

        .sphere-inner {
            width: 260px;
            height: 260px;
            border: 2px dashed var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .sphere-core {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #0a357c 0%, #00b4b4 100%);
            border-radius: 50%;
            box-shadow: 0 0 40px rgba(0, 180, 180, 0.3);
        }

        @keyframes slowRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* --- نبذة عن الشركة والعمارة الهيكلية --- */
        .briefing-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 100px;
            align-items: start;
        }

        .briefing-statement {
            font-size: 1.6rem;
            font-weight: 600;
            line-height: 1.5;
            color: var(--text-primary);
        }

        .briefing-metrics {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .metric-item h3 {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--accent);
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 10px;
            margin-bottom: 15px;
        }

        /* --- منظومة الشركات والمنصات التابعة --- */
        .ecosystem-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
        }

        .product-card {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 340px;
        }

        .product-card:hover {
            transform: translateY(-4px);
            border-color: var(--accent);
        }

        .product-meta h3 {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 12px;
        }

        .product-card .icon-wrapper {
            width: 48px;
            height: 48px;
            border-radius: 8px;
            background: var(--bg-surface);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent);
            margin-bottom: 24px;
            border: 1px solid var(--border-color);
        }

        .product-link {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--accent);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            margin-top: auto;
        }

        /* --- قطاع الحوسبة والذكاء الاصطناعي --- */
        .intel-section {
            background-color: var(--bg-surface);
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
        }

        .intel-layout {
            display: grid;
            grid-template-columns: 0.9fr 1.1fr;
            gap: 100px;
            align-items: center;
        }

        .intel-features {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .intel-feature-item {
            display: flex;
            gap: 20px;
            align-items: start;
        }

        .intel-feature-item i {
            color: var(--accent);
            margin-top: 4px;
        }

        /* --- القيم الجوهرية والمبادئ التشغيلية --- */
        .values-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px 24px;
        }

        .value-card h3 {
            font-size: 1.25rem;
            margin-bottom: 10px;
            color: var(--text-primary);
        }

        .value-card p {
            font-size: 0.95rem;
            color: var(--text-muted);
        }

        /* --- قطاع رأس المال البشري والوظائف --- */
        .careers-panel {
            background: linear-gradient(135deg, #0a357c 0%, #031430 100%);
            color: #ffffff;
            border-radius: 16px;
            padding: 80px;
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 60px;
            align-items: center;
        }

        .careers-panel h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: #ffffff;
        }

        .careers-panel p {
            color: #e0f4f8;
            opacity: 0.9;
            font-size: 1.15rem;
        }

        .careers-action {
            display: flex;
            justify-content: flex-end;
        }

        .careers-action .btn {
            background: #ffffff;
            color: #0a357c;
            border: none;
        }
        
        .careers-action .btn:hover {
            background: var(--accent);
            color: white;
        }

        /* --- التذييل والامتثال والمؤسسية --- */
        footer {
            border-top: 1px solid var(--border-color);
            padding: 100px 5% 50px 5%;
            background-color: var(--bg-main);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr repeat(3, 1fr);
            gap: 60px;
            margin-bottom: 80px;
        }

        .footer-brand p {
            margin-top: 20px;
            max-width: 320px;
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .footer-column h4 {
            font-size: 0.95rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            margin-bottom: 25px;
            color: var(--text-primary);
        }

        .footer-column ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .footer-column a {
            text-decoration: none;
            color: var(--text-secondary);
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .footer-column a:hover {
            color: var(--accent);
        }

        .footer-bottom {
            border-top: 1px solid var(--border-color);
            padding-top: 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        .footer-meta-links {
            display: flex;
            gap: 30px;
        }

        .footer-meta-links a {
            color: var(--text-muted);
            text-decoration: none;
        }
        
        .footer-meta-links a:hover {
            color: var(--text-primary);
        }

        /* --- نقاط الاستجابة البرمجية للشاشات والأجهزة المتنوعة --- */
        @media (max-width: 1100px) {
            .ecosystem-grid { grid-template-columns: repeat(2, 1fr); }
            .values-grid { grid-template-columns: repeat(2, 1fr); }
            .hero-layout, .briefing-grid, .intel-layout, .careers-panel { 
                grid-template-columns: 1fr; 
                gap: 50px;
            }
            .careers-action { justify-content: flex-start; }
            .hero-visual { order: -1; margin-bottom: 30px; }
            .footer-grid { grid-template-columns: 1fr 1fr; }
        }

        @media (max-width: 768px) {
            section { padding: 90px 5%; }
            .hero-content h1 { font-size: 2.8rem; }
            .section-intro h2 { font-size: 2rem; }
            .ecosystem-grid { grid-template-columns: 1fr; }
            .briefing-metrics { grid-template-columns: 1fr; }
            .nav-links { display: none; }
            .careers-panel { padding: 40px; }
            .footer-grid { grid-template-columns: 1fr; gap: 40px; }
            .footer-bottom { flex-direction: column; gap: 20px; align-items: flex-start; }
        }
    </style>
</head>
<body data-theme="dark">

    <!-- نظام الملاحة الرأسي -->
    <nav class="navbar">
        <a href="#" class="logo" style="display: flex; align-items: center; gap: 15px;">
            <div style="width: 40px; height: 40px; display: flex; align-items: center; justify-content: center;">
                <img src="logos/orantos-main.png" alt="Orantos Logo" style="width: 100%; height: 100%; object-fit: contain;" onerror="this.style.display='none';">
            </div>
            ORANTOS
        </a>
        <ul class="nav-links">
            <li><a href="#about">المنظومة</a></li>
            <li><a href="#portfolio">شركاتنا</a></li>
            <li><a href="#governance">الحوكمة</a></li>
            <li><a href="#careers">الوظائف</a></li>
        </ul>
        <div class="nav-actions">
            <button class="theme-toggle" id="themeToggle" aria-label="تبديل الوضع اللوني">
                <i data-lucide="sun" id="themeIcon"></i>
            </button>
            <a href="#contact" class="btn btn-secondary" style="padding: 10px 20px; font-size: 0.85rem; border-radius: 4px;">استفسار مؤسسي</a>
        </div>
    </nav>

    <!-- قسم الواجهة الرئيسية (Hero Section) -->
    <section class="hero">
        <div class="hero-layout">
            <div class="hero-content reveal">
                <span class="text-accent">شركة تقنية قابضة سورية</span>
                <h1>هندسة البنية التحتية الرقمية التي تمكّن المجتمعات</h1>
                <p>تقوم أورانتوس ببناء وتوسيع وإدارة عائلة متكاملة من المنصات الرقمية المستقلة في مجالات التجارة المتقدمة، اللوجستيات الذكية، الأدوات المالية السيادية، والحوسبة المعرفية.</p>
                <div class="hero-actions">
                    <a href="#portfolio" class="btn btn-primary">استكشاف الشركات</a>
                    <a href="#about" class="btn btn-secondary">الملف المؤسسي</a>
                </div>
            </div>
            <div class="hero-visual reveal">
                <div class="sphere-container">
                    <div class="sphere-inner">
                        <div class="sphere-core"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- النبذة التنفيذية -->
    <section id="about" class="reveal">
        <span class="text-accent">إيجاز تنفيذي</span>
        <div class="section-intro">
            <h2>هيكلية القدرات المشتركة</h2>
        </div>
        <div class="briefing-grid">
            <div class="briefing-statement">
                "بدلاً من عزل التطورات التقنية، تعمل أورانتوس كقاعدة مرجعية عابرة للصناعات. نحن نهندس أنظمة موحدة تحول العمليات اليومية إلى شبكة رقمية سورية أكثر مرونة وأماناً."
            </div>
            <div class="briefing-metrics">
                <div class="metric-item">
                    <h3>07</h3>
                    <p>صناعات جوهرية نقود فيها التحول الرقمي الكامل</p>
                </div>
                <div class="metric-item">
                    <h3>متكاملة</h3>
                    <p>أنظمة مالية وحوسبة سحابية قابلة للتوافق البيني</p>
                </div>
            </div>
        </div>
    </section>

    <!-- محفظة الشركات والمنصات القابضة -->
    <section id="portfolio" class="reveal">
        <span class="text-accent">شركات المنظومة</span>
        <div class="section-intro">
            <h2>منصاتنا العاملة عالمياً</h2>
            <p>شركات مستقلة إستراتيجياً، متصلة تقنياً وقائمة على الابتكار المشترك تحت قيادة تقنية موحدة.</p>
        </div>
        <div class="ecosystem-grid">
            
            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/trendat.png" alt="Trendat Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>Trendat (تريندات)</h3>
                        <p>منصة تجارة إلكترونية ذكية تربط العملاء بالشركات وتحسن كفاءة المعاملات عبر سوق رقمي متطور.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/tplus.png" alt="T+ Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>T+</h3>
                        <p>منصة خدمات لوجستية وتوصيل ذكي فوري عند الطلب، تعتمد على التوجيه الذكي للمسارات التجارية المختلفة.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/al-oqab.png" alt="Al-Oqab Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>العقاب (Al-Oqab)</h3>
                        <p>بنية تحتية مالية رقمية آمنة لمعالجة المدفوعات، التحويلات، المحافظ الرقمية والتقنيات النقدية المستقبلية.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/wardi.png" alt="Wardi Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>وردي (Wardi)</h3>
                        <p>تطبيق إنتاجية يومي معرفي مصمم لإدارة المهام والتخطيط، التقييم الشخصي وتتبع العادات الفردية والمؤسسية.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/al-sabeel.png" alt="Al-Sabeel Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>السبيل (Al-Sabeel)</h3>
                        <p>منصة سفر متكاملة لحجز الرحلات، الفنادق، وتنظيم التجارب السياحية بالاعتماد على تحليلات البيانات الضخمة.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

            <div class="glass-panel product-card">
                <div>
                    <div class="icon-wrapper" style="background: transparent; border: none; width: 64px; height: 64px;">
                        <img src="logos/khaliyah.png" alt="Khaliyah Logo" style="width: 100%; height: 100%; object-fit: contain;">
                    </div>
                    <div class="product-meta" style="margin-top: 15px;">
                        <h3>خلية (Khaliyah)</h3>
                        <p>منصة تواصل اجتماعي من الجيل الجديد تركز على المجتمعات الحقيقية، الإبداع والخصوصية المطلقة المشفرة.</p>
                    </div>
                </div>
                <a href="#" class="product-link">استعراض البنية التحتية <i data-lucide="arrow-left"></i></a>
            </div>

        </div>
    </section>
    <!-- محرك الحوسبة والذكاء الاصطناعي المركزي -->
    <section class="intel-section reveal">
        <div class="intel-layout">
            <div>
                <div style="width: 80px; height: 80px; margin-bottom: 25px;">
                    <img src="logos/hakim-ai.png" alt="Hakim AI Logo" style="width: 100%; height: 100%; object-fit: contain;">
                </div>
                
                <span class="text-accent">نواة الحوسبة المتقدمة</span>
                <h2>حكيم للذكاء الاصطناعي (Hakim AI)</h2>
                <p style="margin-bottom: 30px; font-size: 1.2rem;">المحرك الإدراكي التشغيلي الذي يدعم كافة التفاعلات والمنصات لشبكة أورانتوس.</p>
                <p style="margin-bottom: 40px;">يوفر Hakim AI معالجة ذكية للبيانات، بروتوكولات الأتمتة الصناعية، أنظمة إدارة المعرفة، والنماذج الخوارزمية الفائقة المستخدمة بالكامل في خطوط الإنتاج والحلول البرمجية التابعة لشركاتنا.</p>
                <a href="#" class="btn btn-primary">مراجعة وثائق الأبحاث</a>
            </div>
            <div class="intel-features">
                
                <div class="glass-panel intel-feature-item" style="display: flex; align-items: center; gap: 20px;">
                    <div style="min-width: 48px; width: 48px; height: 48px; flex-shrink: 0;">
                        <img src="logos/hakim-feature1.png" alt="Feature 1" style="width: 100%; height: 100%; object-fit: contain;" onerror="this.style.display='none';">
                        </div>
                    <div>
                        <h4>أنظمة الإستراتيجية الآلية</h4>
                        <p>تقديم نماذج اتخاذ القرار الفوري عالي التزامن مباشرة إلى التطبيقات والشبكات.</p>
                    </div>
                </div>
                
                <div class="glass-panel intel-feature-item" style="display: flex; align-items: center; gap: 20px;">
                    <div style="min-width: 48px; width: 48px; height: 48px; flex-shrink: 0;">
                        <img src="logos/hakim-feature2.png" alt="Feature 2" style="width: 100%; height: 100%; object-fit: contain;" onerror="this.style.display='none';">
                        </div>
                    <div>
                        <h4>نماذج البيانات السيادية</h4>
                        <p>طبقات بيانات معزولة تماماً تضمن بقاء الأصول المعرفية والفكرية للمؤسسات محمية بشكل كامل.</p>
                    </div>
                </div>
                
            </div>
        </div>
    </section>

    <!-- قيم الحوكمة والمبادئ المؤسسية -->
    <section id="governance" class="reveal">
        <span class="text-accent">إطار العمل التشغيلي</span>
        <div class="section-intro">
            <h2>ركائزنا الجوهرية الثابتة</h2>
        </div>
        <div class="values-grid">
            <div class="value-card">
                <h3>الابتكار</h3>
                <p>نشر آليات حوسبة متطورة تسبق الحلول التقليدية الموروثة للمؤسسات.</p>
            </div>
            <div class="value-card">
                <h3>الثقة</h3>
                <p>تنفيذ استمرارية هيكلية يعتمد عليها ملايين الأفراد والشركات يومياً لدعم المنصات الحيوية.</p>
            </div>
            <div class="value-card">
                <h3>الخصوصية</h3>
                <p>تطبيق نماذج عزل بيانات صارمة لضمان حماية أمن المستخدم وتأمين اتصالاته.</p>
            </div>
            <div class="value-card">
                <h3>البساطة</h3>
                <p>تفكيك الطبقات اللوجستية المعقدة إلى واجهات واضحة ومباشرة مبنية للاستخدام السلس.</p>
            </div>
            <div class="value-card">
                <h3>الأمان</h3>
                <p>دمج عمليات التحقق والتشفير من نوع (Zero-Trust) في أعمق طبقات أطر عمل منتجاتنا.</p>
            </div>
            <div class="value-card">
                <h3>التصميم المتمحور حول الإنسان</h3>
                <p>هندسة أطر عمل رقمية مصممة خصيصاً لتعزيز الكفاءة الواقعية وتحفيز الفاعلية الإنسانية.</p>
            </div>
            <div class="value-card">
                <h3>التميز</h3>
                <p>فرض ممارسات اختبار صارمة لضمان أعلى جودة في أنظمة قواعد البيانات الضخمة.</p>
            </div>
            <div class="value-card">
                <h3>التفكير بعيد المدى</h3>
                <p>توجيه الاستثمارات الرأسمالية نحو المشاريع المصممة لخدمة الأجيال الرقمية القادمة لعقود.</p>
            </div>
        </div>
    </section>

    <!-- قطاع التوظيف ورأس المال البشري -->
    <section id="careers" class="reveal">
        <div class="careers-panel">
            <div>
                <h2>شكل ملامح الأفق الرقمي القادم</h2>
                <p>تستقبل أورانتوس باستمرار طلبات الانضمام من كبار المهندسين والمطورين، خبراء التشفير والأنظمة الأمنية، وقادة المنتجات المتميزين من حول العالم.</p>
            </div>
            <div class="careers-action">
                <a href="#" class="btn">عرض الفرص المتاحة <i data-lucide="arrow-up-left"></i></a>
            </div>
        </div>
    </section>

    <!-- التواصل المؤسسي والإستراتيجي -->
    <section id="contact" class="reveal" style="padding-top: 40px; text-align: center;">
        <div style="max-width: 600px; margin: 0 auto;">
            <span class="text-accent">العلاقات المؤسسية</span>
            <h2 style="font-size: 2.5rem; margin-bottom: 20px;">المقر سورية / حماة</h2>
            <p style="color: var(--text-muted); margin-bottom: 40px;">للاستفسارات الإستراتيجية، العلاقات الحكومية، أو تحالفات منصات العمليات الكبرى، يرجى التنسيق عبر مكتب العلاقات والتبادل المؤسسي.</p>
            <a href="mailto:relations@orantos.com" class="btn btn-secondary">contact@orantos.com</a>
        </div>
    </section>

    <!-- تذييل المجموعة القابضة -->
    <footer>
        <div class="footer-grid">
            <div class="footer-brand">
                <a href="#" class="logo" style="display: flex; align-items: center; gap: 12px; text-decoration: none;">
                    <div style="width: 35px; height: 35px; display: flex; align-items: center; justify-content: center;">
                        <img src="logos/orantos-main.png" alt="Orantos Logo" style="width: 100%; height: 100%; object-fit: contain;" onerror="this.style.display='none';">
                    </div>
                    ORANTOS
                </a>
                <p>كيان مؤسسي سورية / حماة يدير منصات بخرائط برمجية وبنية تحتية سيادية مصممة لتحقيق الاستدامة التكنولوجية الطويلة.</p>
            </div>
            <div class="footer-column">
                <h4>هيكل المجموعة</h4>
                <ul>
                    <li><a href="#about">نظرة عامة على المنظومة</a></li>
                    <li><a href="#portfolio">المحافظ التشغيلية</a></li>
                    <li><a href="#governance">الحوكمة المؤسسية</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>المنصات التابعة</h4>
                <ul>
                    <li><a href="#">تريندات للتجارة الرقمية</a></li>
                    <li><a href="#">لوجستيات شبكة T+</a></li>
                    <li><a href="#">البنية التحتية الماليّة لـ العقاب</a></li>
                    <li><a href="#">أبحاث حكيم للذكاء الاصطناعي</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>الامتثال والخصوصية</h4>
                <ul>
                    <li><a href="#">علاقات المستثمرين</a></li>
                    <li><a href="#">نشرات وتقارير الأمن السيبراني</a></li>
                    <li><a href="#">سياسات التشفير المعتمدة</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 أورانتوس. جميع الحقوق المؤسسية محفوظة.</p>
            <div class="footer-meta-links">
                <a href="#"> الإفصاح التنظيمي</a>
                <a href="#">إطار حماية الخصوصية</a>
            </div>
        </div>
    </footer>

    <!-- محرك التفاعلات للواجهة -->
    <script>
        // تركيب أيقونات النظام
        lucide.createIcons();

        // --- نظام التبديل اللوني الديناميكي للوضع الداكن/المضيء ---
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = document.getElementById('themeIcon');
        const body = document.body;

        themeToggle.addEventListener('click', () => {
            const activeTheme = body.getAttribute('data-theme');
            if (activeTheme === 'dark') {
                body.setAttribute('data-theme', 'light');
                themeIcon.setAttribute('data-lucide', 'moon');
            } else {
                body.setAttribute('data-theme', 'dark');
                themeIcon.setAttribute('data-lucide', 'sun');
            }
            lucide.createIcons(); // مزامنة المتجهات الرسومية الفورية
        });

        // --- محرك مراقبة عناصر الصفحة لإضافة تأثيرات التمرير الفاخرة ---
        const structuralElements = document.querySelectorAll('.reveal');
        const layoutObserver = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('active');
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.1, rootMargin: "0px 0px -50px 0px" });

        structuralElements.forEach(el => layoutObserver.observe(el));
    </script>
</body>
</html>
