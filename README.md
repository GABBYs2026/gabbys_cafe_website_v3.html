# gabbys_cafe_website_v3.html [gabbys_cafe_website_v3.html](https://github.com/user-attachments/files/28764405/gabbys_cafe_website_v3.html)
[gabbys_cafe_website_v3.html](https://github.com/user-attachments/files/28764347/gabbys_cafe_website_v3.html)
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GABBY's | Global Café & Social Club</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a1a1a;
            --secondary: #241316;
            --accent: #9B2335;
            --accent-light: #C41E3A;
            --text: #f0f0f0;
            --text-muted: #a0a0a0;
            --success: #4caf50;
            --danger: #e74c3c;
            --card-bg: #2a1a1c;
            --border: #3a1f23;
            --wc-green: #1a472a;
            --wc-green-dark: #0d3320;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--primary);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        body[dir="rtl"] {
            font-family: 'Cairo', sans-serif;
        }

        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--primary);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--accent);
            border-radius: 4px;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--border);
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent-light);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
            list-style: none;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: var(--accent-light);
        }

        .nav-actions {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .lang-toggle, .cart-btn {
            background: var(--secondary);
            border: 1px solid var(--border);
            color: var(--text);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            cursor: pointer;
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .lang-toggle:hover, .cart-btn:hover {
            background: var(--accent);
            color: white;
        }

        .cart-btn {
            position: relative;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--accent-light);
            color: white;
            font-size: 0.75rem;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 8rem 5% 4rem;
            background: linear-gradient(135deg, rgba(26,26,26,0.92) 0%, rgba(36,19,22,0.85) 100%), url('https://images.unsplash.com/photo-1501339847302-ac426a4a7cbb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
            position: relative;
        }

        .hero-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4rem;
            color: var(--accent-light);
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-content .tagline {
            font-size: 1.3rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .hero-btns {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .btn {
            padding: 0.9rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-family: 'Cairo', sans-serif;
            font-size: 1rem;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--accent);
            color: white;
        }

        .btn-primary:hover {
            background: var(--accent-light);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(155, 35, 53, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text);
            border: 2px solid var(--accent);
        }

        .btn-secondary:hover {
            background: var(--accent);
            color: white;
        }

        .btn-instagram {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            color: white;
            border: none;
        }

        .btn-instagram:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(220, 39, 67, 0.4);
        }

        .info-bar {
            background: var(--secondary);
            padding: 2rem 5%;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            border-bottom: 1px solid var(--border);
        }

        .info-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background: var(--card-bg);
            border-radius: 15px;
            border: 1px solid var(--border);
        }

        .info-item i {
            font-size: 1.5rem;
            color: var(--accent-light);
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(155, 35, 53, 0.15);
            border-radius: 12px;
        }

        .info-item h3 {
            font-size: 1rem;
            color: var(--text);
            margin-bottom: 0.2rem;
        }

        .info-item p {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        section {
            padding: 5rem 5%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: var(--accent-light);
            margin-bottom: 0.5rem;
        }

        .section-title p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        /* World Cup Section - Now on Homepage */
        .worldcup-section {
            background: linear-gradient(135deg, var(--wc-green) 0%, var(--wc-green-dark) 100%);
            border: 2px solid var(--accent);
            border-radius: 20px;
            padding: 3rem;
            margin: 3rem 5%;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .worldcup-section::before {
            content: '⚽';
            position: absolute;
            font-size: 15rem;
            opacity: 0.05;
            top: -2rem;
            right: -2rem;
        }

        .worldcup-section h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            color: var(--accent-light);
            margin-bottom: 1rem;
        }

        .worldcup-section p {
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 2rem;
        }

        .offers-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .offer-card {
            background: rgba(255,255,255,0.05);
            border-radius: 15px;
            padding: 1.5rem;
            border: 1px solid rgba(155, 35, 53, 0.3);
            transition: transform 0.3s;
        }

        .offer-card:hover {
            transform: translateY(-5px);
            background: rgba(255,255,255,0.08);
        }

        .offer-card .emoji {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .offer-card h3 {
            color: var(--accent-light);
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
        }

        .offer-card p {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        .instagram-reserve-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            padding: 1rem 2.5rem;
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            margin-top: 2rem;
            transition: all 0.3s;
        }

        .instagram-reserve-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(220, 39, 67, 0.4);
        }

        .menu-categories {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .category-btn {
            padding: 0.6rem 1.5rem;
            background: var(--card-bg);
            border: 1px solid var(--border);
            color: var(--text);
            border-radius: 25px;
            cursor: pointer;
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
            transition: all 0.3s;
        }

        .category-btn.active, .category-btn:hover {
            background: var(--accent);
            color: white;
            border-color: var(--accent);
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .menu-item {
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid var(--border);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
        }

        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
            border-color: var(--accent);
        }

        .menu-item-img {
            height: 180px;
            background: linear-gradient(135deg, #2a1a1c 0%, #1a1a1a 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            position: relative;
            overflow: hidden;
        }

        .menu-item-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .menu-item-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .menu-item-header {
            display: flex;
            justify-content: space-between;
            align-items: start;
            margin-bottom: 0.5rem;
        }

        .menu-item h3 {
            font-size: 1.1rem;
            color: var(--text);
            font-weight: 700;
        }

        .menu-item .price {
            color: var(--accent-light);
            font-weight: 800;
            font-size: 1.1rem;
            white-space: nowrap;
        }

        .menu-item .desc {
            color: var(--text-muted);
            font-size: 0.85rem;
            margin-bottom: 1rem;
            flex-grow: 1;
        }

        .add-to-cart {
            width: 100%;
            padding: 0.7rem;
            background: var(--accent);
            color: white;
            border: none;
            border-radius: 12px;
            font-weight: 700;
            cursor: pointer;
            font-family: 'Cairo', sans-serif;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .add-to-cart:hover {
            background: var(--accent-light);
        }

        .cart-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
        }

        .cart-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -450px;
            width: 100%;
            max-width: 450px;
            height: 100%;
            background: var(--secondary);
            z-index: 2001;
            transition: right 0.4s ease;
            display: flex;
            flex-direction: column;
            border-left: 1px solid var(--border);
        }

        body[dir="rtl"] .cart-sidebar {
            right: auto;
            left: -450px;
            border-left: none;
            border-right: 1px solid var(--border);
        }

        .cart-sidebar.active {
            right: 0;
        }

        body[dir="rtl"] .cart-sidebar.active {
            left: 0;
            right: auto;
        }

        .cart-header {
            padding: 1.5rem;
            border-bottom: 1px solid var(--border);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .cart-header h2 {
            color: var(--accent-light);
            font-family: 'Playfair Display', serif;
        }

        .close-cart {
            background: none;
            border: none;
            color: var(--text);
            font-size: 1.5rem;
            cursor: pointer;
        }

        .cart-items {
            flex-grow: 1;
            overflow-y: auto;
            padding: 1rem;
        }

        .cart-item {
            display: flex;
            gap: 1rem;
            padding: 1rem;
            background: var(--card-bg);
            border-radius: 15px;
            margin-bottom: 1rem;
            border: 1px solid var(--border);
        }

        .cart-item-info {
            flex-grow: 1;
        }

        .cart-item h4 {
            font-size: 1rem;
            margin-bottom: 0.3rem;
        }

        .cart-item .item-price {
            color: var(--accent-light);
            font-weight: 700;
        }

        .qty-controls {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }

        .qty-btn {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            border: 1px solid var(--border);
            background: var(--secondary);
            color: var(--text);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .remove-item {
            color: var(--danger);
            cursor: pointer;
            font-size: 1.2rem;
            align-self: center;
        }

        .cart-footer {
            padding: 1.5rem;
            border-top: 1px solid var(--border);
            background: var(--card-bg);
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--accent-light);
        }

        .checkout-btn {
            width: 100%;
            padding: 1rem;
            background: var(--success);
            color: white;
            border: none;
            border-radius: 15px;
            font-weight: 700;
            font-size: 1.1rem;
            cursor: pointer;
            font-family: 'Cairo', sans-serif;
            transition: all 0.3s;
        }

        .checkout-btn:hover {
            background: #45a049;
        }

        .empty-cart {
            text-align: center;
            padding: 3rem;
            color: var(--text-muted);
        }

        .empty-cart i {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        footer {
            background: var(--secondary);
            padding: 4rem 5% 2rem;
            border-top: 1px solid var(--border);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-section h3 {
            color: var(--accent-light);
            font-family: 'Playfair Display', serif;
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .footer-section p, .footer-section a {
            color: var(--text-muted);
            text-decoration: none;
            line-height: 2;
            display: block;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: var(--accent-light);
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--card-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text);
            border: 1px solid var(--border);
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--accent);
            color: white;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid var(--border);
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .toast {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background: var(--accent);
            color: white;
            padding: 1rem 2rem;
            border-radius: 50px;
            font-weight: 700;
            z-index: 3000;
            opacity: 0;
            transition: all 0.4s ease;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .toast.show {
            opacity: 1;
            transform: translateX(-50%) translateY(0);
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .mobile-menu {
                display: block;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .section-title h2 {
                font-size: 1.8rem;
            }
            .worldcup-section {
                padding: 2rem 1rem;
                margin: 2rem 3%;
            }
        }
    </style>
</head>
<body>
    <nav>
        <a href="#" class="logo">
            <span>GABBY's</span>
        </a>
        <ul class="nav-links">
            <li><a href="#home" data-en="Home" data-ar="الرئيسية">Home</a></li>
            <li><a href="#menu" data-en="Menu" data-ar="القائمة">Menu</a></li>
            <li><a href="#worldcup" data-en="World Cup" data-ar="كأس العالم">World Cup</a></li>
            <li><a href="#reservation" data-en="Reserve" data-ar="حجز">Reserve</a></li>
            <li><a href="#contact" data-en="Contact" data-ar="تواصل">Contact</a></li>
        </ul>
        <div class="nav-actions">
            <button class="lang-toggle" onclick="toggleLanguage()">
                <i class="fas fa-globe"></i>
                <span id="lang-text">العربية</span>
            </button>
            <button class="cart-btn" onclick="toggleCart()">
                <i class="fas fa-shopping-bag"></i>
                <span data-en="Cart" data-ar="السلة">Cart</span>
                <span class="cart-count" id="cart-count">0</span>
            </button>
        </div>
        <div class="mobile-menu" onclick="toggleMobileMenu()">
            <i class="fas fa-bars"></i>
        </div>
    </nav>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>GABBY's</h1>
            <p class="tagline" data-en="Where East meets West in every cup. More than just a café — it's a connection." data-ar="حيث يلتقي الشرق بالغرب في كل كوب. أكثر من مجرد مقهى — إنه تواصل.">
                Where East meets West in every cup. More than just a café — it's a connection.
            </p>
            <div class="hero-btns">
                <a href="#menu" class="btn btn-primary">
                    <i class="fas fa-utensils"></i>
                    <span data-en="Order Now" data-ar="اطلب الآن">Order Now</span>
                </a>
                <a href="https://www.instagram.com/gabbys.social_club?igsh=MWp5bGw2amdzbjZrdg==" target="_blank" class="btn btn-instagram">
                    <i class="fab fa-instagram"></i>
                    <span data-en="Reserve on Instagram" data-ar="احجز على انستغرام">Reserve on Instagram</span>
                </a>
            </div>
        </div>
    </section>

    <div class="info-bar">
        <div class="info-item">
            <i class="fas fa-map-marker-alt"></i>
            <div>
                <h3 data-en="Location" data-ar="الموقع">Location</h3>
                <p data-en="Lattakia, West Coast Street, Syria" data-ar="اللاذقية، شارع الساحل الغربي، سوريا">Lattakia, West Coast Street, Syria</p>
            </div>
        </div>
        <div class="info-item">
            <i class="fas fa-clock"></i>
            <div>
                <h3 data-en="Open Hours" data-ar="ساعات العمل">Open Hours</h3>
                <p data-en="Daily 11:00 AM - 11:55 PM" data-ar="يومياً 11:00 ص - 11:55 م">Daily 11:00 AM - 11:55 PM</p>
            </div>
        </div>
        <div class="info-item">
            <i class="fas fa-phone"></i>
            <div>
                <h3 data-en="Contact" data-ar="التواصل">Contact</h3>
                <p>WhatsApp / Phone</p>
            </div>
        </div>
        <div class="info-item">
            <i class="fas fa-motorcycle"></i>
            <div>
                <h3 data-en="Services" data-ar="الخدمات">Services</h3>
                <p data-en="Pickup & Delivery (Cash)" data-ar="استلام وتوصيل (كاش)">Pickup & Delivery (Cash)</p>
            </div>
        </div>
    </div>

    <!-- World Cup Section - Now on Homepage -->
    <div class="worldcup-section" id="worldcup">
        <h2 data-en="⚽ World Cup 2026 Specials ⚽" data-ar="⚽ عروض كأس العالم 2026 ⚽">⚽ World Cup 2026 Specials ⚽</h2>
        <p data-en="Cheer for your team with exclusive match-day deals!" data-ar="شجّع فريقك مع عروض حصرية أيام المباريات!">Cheer for your team with exclusive match-day deals!</p>
        <div class="offers-grid">
            <div class="offer-card">
                <div class="emoji">🍔⚽</div>
                <h3 data-en="Full Time Combo" data-ar="عرض الشوطين">Full Time Combo</h3>
                <p data-en="2 Drinks + 1 Appetizer = 15% OFF" data-ar="مشروبين + طبق مقبلات = خصم 15%">2 Drinks + 1 Appetizer = 15% OFF</p>
            </div>
            <div class="offer-card">
                <div class="emoji">🎯</div>
                <h3 data-en="Predict & Win" data-ar="توقع واربح">Predict & Win</h3>
                <p data-en="Guess the score before kickoff & get a free dessert!" data-ar="توقع النتيجة قبل البداية واحصل على حلوى مجانية!">Guess the score before kickoff & get a free dessert!</p>
            </div>
            <div class="offer-card">
                <div class="emoji">👥</div>
                <h3 data-en="Group Squad Deal" data-ar="عرض المجموعة">Group Squad Deal</h3>
                <p data-en="Groups of 6+ get 20% OFF + reserved big table" data-ar="مجموعات 6+ أشخاص خصم 20% + طاولة كبيرة محجوزة">Groups of 6+ get 20% OFF + reserved big table</p>
            </div>
            <div class="offer-card">
                <div class="emoji">🏆</div>
                <h3 data-en="Champion's Drink" data-ar="مشروب البطل">Champion's Drink</h3>
                <p data-en="Team-colored layered drinks (Brazil, Argentina, Spain...)" data-ar="مشروبات بطبقات بألوان الفرق (البرازيل، الأرجنتين، إسبانيا...)">Team-colored layered drinks (Brazil, Argentina, Spain...)</p>
            </div>
            <div class="offer-card">
                <div class="emoji">🍟</div>
                <h3 data-en="Penalty Shootout Snacks" data-ar="وجبات ركلات الترجيح">Penalty Shootout Snacks</h3>
                <p data-en="Every goal = free refill on selected drinks" data-ar="كل هدف = تعبئة مجانية على مشروبات مختارة">Every goal = free refill on selected drinks</p>
            </div>
            <div class="offer-card">
                <div class="emoji">🎫</div>
                <h3 data-en="Final Match Ticket" data-ar="تذكرة المباراة النهائية">Final Match Ticket</h3>
                <p data-en="Reserve your spot for the final — limited seats!" data-ar="احجز مكانك للنهائي — مقاعد محدودة!">Reserve your spot for the final — limited seats!</p>
            </div>
        </div>
        <a href="https://www.instagram.com/gabbys.social_club?igsh=MWp5bGw2amdzbjZrdg==" target="_blank" class="instagram-reserve-btn">
            <i class="fab fa-instagram"></i>
            <span data-en="Reserve Your Table via Instagram" data-ar="احجز طاولتك عبر انستغرام">Reserve Your Table via Instagram</span>
        </a>
    </div>

    <section id="menu">
        <div class="section-title">
            <h2 data-en="Our Menu" data-ar="قائمتنا">Our Menu</h2>
            <p data-en="From classic coffee to creative specialties" data-ar="من القهوة الكلاسيكية إلى المشروبات الإبداعية">From classic coffee to creative specialties</p>
        </div>
        <div class="menu-categories">
            <button class="category-btn active" onclick="filterMenu('all', this)" data-en="All" data-ar="الكل">All</button>
            <button class="category-btn" onclick="filterMenu('hot', this)" data-en="Hot Coffee" data-ar="قهوة ساخنة">Hot Coffee</button>
            <button class="category-btn" onclick="filterMenu('cold', this)" data-en="Cold Coffee" data-ar="قهوة باردة">Cold Coffee</button>
            <button class="category-btn" onclick="filterMenu('smoothie', this)" data-en="Smoothies & Shakes" data-ar="سموذي وشيك">Smoothies & Shakes</button>
            <button class="category-btn" onclick="filterMenu('special', this)" data-en="Special Drinks" data-ar="مشروبات خاصة">Special Drinks</button>
            <button class="category-btn" onclick="filterMenu('fresh', this)" data-en="Fresh Juices" data-ar="عصائر طبيعية">Fresh Juices</button>
            <button class="category-btn" onclick="filterMenu('hookah', this)" data-en="Hookah" data-ar="أركيلة">Hookah</button>
        </div>
        <div class="menu-grid" id="menu-grid"></div>
    </section>

    <section id="reservation">
        <div class="section-title">
            <h2 data-en="Reserve Your Table" data-ar="احجز طاولتك">Reserve Your Table</h2>
            <p data-en="For dates, groups, or World Cup match nights" data-ar="للمواعيد، المجموعات، أو ليالي مباريات كأس العالم">For dates, groups, or World Cup match nights</p>
        </div>
        <div style="text-align: center; max-width: 600px; margin: 0 auto 3rem;">
            <p style="color: var(--text-muted); font-size: 1.1rem; margin-bottom: 2rem;" data-en="All reservations are now handled through our Instagram page. Send us a DM and we'll confirm your booking!" data-ar="جميع الحجوزات تتم الآن عبر صفحة الانستغرام. ارسل لنا رسالة خاصة وسنؤكد حجزك!">
                All reservations are now handled through our Instagram page. Send us a DM and we'll confirm your booking!
            </p>
            <a href="https://www.instagram.com/gabbys.social_club?igsh=MWp5bGw2amdzbjZrdg==" target="_blank" class="btn btn-instagram" style="font-size: 1.2rem; padding: 1rem 3rem;">
                <i class="fab fa-instagram"></i>
                <span data-en="Reserve on Instagram" data-ar="احجز على انستغرام">Reserve on Instagram</span>
            </a>
        </div>
    </section>

    <footer id="contact">
        <div class="footer-content">
            <div class="footer-section">
                <h3>GABBY's</h3>
                <p data-en="Global Café & Social Club. Where East meets West in every cup." data-ar="مقهى ونادي اجتماعي عالمي. حيث يلتقي الشرق بالغرب في كل كوب.">
                    Global Café & Social Club. Where East meets West in every cup.
                </p>
                <div class="social-links">
                    <a href="https://instagram.com/gabbys.social_club" target="_blank"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="https://wa.me/963985482175" target="_blank"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            <div class="footer-section">
                <h3 data-en="Quick Links" data-ar="روابط سريعة">Quick Links</h3>
                <a href="#menu" data-en="Menu" data-ar="القائمة">Menu</a>
                <a href="#worldcup" data-en="World Cup Offers" data-ar="عروض كأس العالم">World Cup Offers</a>
                <a href="#reservation" data-en="Reservations" data-ar="الحجوزات">Reservations</a>
            </div>
            <div class="footer-section">
                <h3 data-en="Contact Info" data-ar="معلومات التواصل">Contact Info</h3>
                <p><i class="fas fa-map-marker-alt"></i> <span data-en="West Coast Street, Lattakia, Syria" data-ar="شارع الساحل الغربي، اللاذقية، سوريا">West Coast Street, Lattakia, Syria</span></p>
                <p><i class="fas fa-clock"></i> <span data-en="11:00 AM - 11:55 PM Daily" data-ar="11:00 ص - 11:55 م يومياً">11:00 AM - 11:55 PM Daily</span></p>
                <p><i class="fas fa-phone"></i> <span>+963 985 482 175</span></p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© 2026 GABBY's Café. <span data-en="All rights reserved." data-ar="جميع الحقوق محفوظة.">All rights reserved.</span></p>
        </div>
    </footer>

    <div class="cart-overlay" id="cart-overlay" onclick="toggleCart()"></div>
    <div class="cart-sidebar" id="cart-sidebar">
        <div class="cart-header">
            <h2 data-en="Your Order" data-ar="طلبك">Your Order</h2>
            <button class="close-cart" onclick="toggleCart()"><i class="fas fa-times"></i></button>
        </div>
        <div class="cart-items" id="cart-items">
            <div class="empty-cart">
                <i class="fas fa-shopping-basket"></i>
                <p data-en="Your cart is empty" data-ar="سلتك فارغة">Your cart is empty</p>
            </div>
        </div>
        <div class="cart-footer" id="cart-footer" style="display: none;">
            <div class="cart-total">
                <span data-en="Total" data-ar="المجموع">Total</span>
                <span id="cart-total">0 SYP</span>
            </div>
            <button class="checkout-btn" onclick="checkout()">
                <i class="fab fa-whatsapp"></i>
                <span data-en="Order via WhatsApp" data-ar="اطلب عبر واتساب">Order via WhatsApp</span>
            </button>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <script>
        const menuData = [
            { id: 1, name: { en: "Dark Mocha", ar: "دارك موكا" }, category: "hot", price: 27000, desc: { en: "Rich dark chocolate meets espresso", ar: "شوكولا داكنة غنية مع الإسبريسو" }, emoji: "☕" },
            { id: 2, name: { en: "Spanish Latte", ar: "سبانيش لاتيه" }, category: "hot", price: 28500, desc: { en: "Sweet condensed milk latte", ar: "لاتيه بحليب مكثف محلى" }, emoji: "☕" },
            { id: 3, name: { en: "Turkish Coffee", ar: "تركوكا / قهوة تركية" }, category: "hot", price: 33000, desc: { en: "Traditional Turkish style coffee", ar: "قهوة تركية تقليدية" }, emoji: "☕" },
            { id: 4, name: { en: "Corn Coffee", ar: "كورن" }, category: "hot", price: 25000, desc: { en: "Special house blend", ar: "خلطة خاصة من البيت" }, emoji: "🌽" },
            { id: 5, name: { en: "Cappuccino", ar: "كبتشينو" }, category: "hot", price: 27000, desc: { en: "Classic Italian cappuccino", ar: "كبتشينو إيطالي كلاسيكي" }, emoji: "☕" },
            { id: 6, name: { en: "Antoccino", ar: "انتويي" }, category: "hot", price: 25000, desc: { en: "Equal parts espresso and steamed milk", ar: "نسب متساوية من الإسبريسو والحليب المبخر" }, emoji: "☕" },
            { id: 7, name: { en: "Iced Dark Mocha", ar: "دارك موكا مثلج" }, category: "cold", price: 27000, desc: { en: "Iced chocolate espresso delight", ar: "إسبريسو شوكولا مثلج" }, emoji: "🧊" },
            { id: 8, name: { en: "Iced Spanish Latte", ar: "سبانيش لاتيه مثلج" }, category: "cold", price: 28500, desc: { en: "Sweet iced latte", ar: "لاتيه مثلج محلى" }, emoji: "🧊" },
            { id: 9, name: { en: "Iced Turkish Coffee", ar: "تركوكا مثلج" }, category: "cold", price: 33000, desc: { en: "Cold brew Turkish style", ar: "قهوة تركية باردة" }, emoji: "🧊" },
            { id: 10, name: { en: "Iced Cappuccino", ar: "كبتشينو مثلج" }, category: "cold", price: 27000, desc: { en: "Frosty cappuccino", ar: "كبتشينو مثلج" }, emoji: "🧊" },
            { id: 11, name: { en: "Iced Antoccino", ar: "انتويي مثلج" }, category: "cold", price: 25000, desc: { en: "Balanced iced coffee", ar: "قهوة مثلجة متوازنة" }, emoji: "🧊" },
            { id: 12, name: { en: "Strawberry Smoothie", ar: "سموذي / فريز" }, category: "smoothie", price: 25000, desc: { en: "Fresh strawberry blend", ar: "خلطة فراولة طازجة" }, emoji: "🍓" },
            { id: 13, name: { en: "Berry Smoothie", ar: "سموذي / توت" }, category: "smoothie", price: 29000, desc: { en: "Mixed berry explosion", ar: "انفجار التوت المختلط" }, emoji: "🫐" },
            { id: 14, name: { en: "Milo Smoothie", ar: "ميلو" }, category: "smoothie", price: 25000, desc: { en: "Chocolate malt favorite", ar: "الشوكولا المالت المفضلة" }, emoji: "🍫" },
            { id: 15, name: { en: "Chocolate Milkshake", ar: "ميلك شيك / شوكولا" }, category: "smoothie", price: 36000, desc: { en: "Thick creamy chocolate shake", ar: "ميلك شيك شوكولا كريمي ثقيل" }, emoji: "🥤" },
            { id: 16, name: { en: "Strawberry Milkshake", ar: "ميلك شيك / فريز" }, category: "smoothie", price: 35000, desc: { en: "Sweet strawberry shake", ar: "ميلك شيك فراولة حلو" }, emoji: "🥤" },
            { id: 17, name: { en: "Iced Milo", ar: "ايس ميلو" }, category: "smoothie", price: 37000, desc: { en: "Iced chocolate malt", ar: "ميلو شوكولا مثلج" }, emoji: "🍫" },
            { id: 18, name: { en: "Vanilla Milkshake", ar: "ميلك شيك / فانيلا" }, category: "smoothie", price: 34000, desc: { en: "Classic vanilla shake", ar: "ميلك شيك فانيلا كلاسيكي" }, emoji: "🥤" },
            { id: 19, name: { en: "Cheesecake Milkshake", ar: "ميلك شيك / تشيز كيك" }, category: "smoothie", price: 37000, desc: { en: "Cheesecake in a glass", ar: "تشيز كيك في كوب" }, emoji: "🍰" },
            { id: 20, name: { en: "Mango Special", ar: "مانشا / مشروب سبيشل" }, category: "special", price: 25000, desc: { en: "Mango layered special", ar: "مشروب مانجو بطبقات" }, emoji: "🥭" },
            { id: 21, name: { en: "Lotus Special", ar: "لوتس / مشروب سبيشل" }, category: "special", price: 31000, desc: { en: "Lotus biscuit inspired drink", ar: "مشروب مستوحى من بسكويت اللوتس" }, emoji: "🍪" },
            { id: 22, name: { en: "Pistachio Special", ar: "بستاشيو / مشروب سبيشل" }, category: "special", price: 29000, desc: { en: "Nutty pistachio delight", ar: "متعة البستاشيو المكسراتية" }, emoji: "🌰" },
            { id: 23, name: { en: "Spiritak Special", ar: "سبيريتاك / مشروب سبيشل" }, category: "special", price: 24000, desc: { en: "House signature special", ar: "مشروب خاص بتوقيع البيت" }, emoji: "✨" },
            { id: 24, name: { en: "Pomegranate Juice", ar: "رمان / عصائر موسمية" }, category: "fresh", price: 20000, desc: { en: "Fresh squeezed pomegranate", ar: "رمان طازج معصور" }, emoji: "🍷" },
            { id: 25, name: { en: "Orange Juice", ar: "برتقال / عصائر موسمية" }, category: "fresh", price: 18000, desc: { en: "Vitamin C boost", ar: "جرعة فيتامين سي" }, emoji: "🍊" },
            { id: 26, name: { en: "Berry Juice", ar: "توت / عصائر موسمية" }, category: "fresh", price: 33000, desc: { en: "Mixed berry juice", ar: "عصير توت مختلط" }, emoji: "🫐" },
            { id: 27, name: { en: "Mango Juice", ar: "مانجا / عصائر موسمية" }, category: "fresh", price: 17000, desc: { en: "Tropical mango juice", ar: "عصير مانجو استوائي" }, emoji: "🥭" },
            { id: 28, name: { en: "Diet Juice", ar: "دايت" }, category: "fresh", price: 12000, desc: { en: "Low-calorie fresh blend", ar: "خلطة طازجة قليلة السعرات" }, emoji: "🥗" },
            { id: 29, name: { en: "Polo Juice", ar: "بولو / عصائر موسمية" }, category: "fresh", price: 22000, desc: { en: "Refreshing house blend", ar: "خلطة منعشة من البيت" }, emoji: "🍹" },
            { id: 30, name: { en: "Zanbouril", ar: "زنبورل" }, category: "fresh", price: 26500, desc: { en: "Special citrus mix", ar: "مزيج حمضيات خاص" }, emoji: "🐝" },
            { id: 31, name: { en: "Cold Lotus", ar: "لوت / بارد" }, category: "cold", price: 24000, desc: { en: "Iced lotus drink", ar: "مشروب لوتس بارد" }, emoji: "🧊" },
            { id: 32, name: { en: "Cold Gint", ar: "جنت / بارد" }, category: "cold", price: 24000, desc: { en: "Refreshing gint cooler", ar: "مشروب جنت المنعش" }, emoji: "🧊" },
            { id: 33, name: { en: "Two Apples Hookah", ar: "تفاحين / أركيلة" }, category: "hookah", price: 24000, desc: { en: "Classic double apple", ar: "تفاحتين كلاسيكية" }, emoji: "🍎" },
            { id: 34, name: { en: "Musk Hookah", ar: "مسكة / أركيلة" }, category: "hookah", price: 24000, desc: { en: "Sweet musk flavor", ar: "نكهة المسكة الحلوة" }, emoji: "🌸" },
        ];

        let cart = JSON.parse(localStorage.getItem('gabbys_cart')) || [];
        let currentLang = localStorage.getItem('gabbys_lang') || 'en';

        document.addEventListener('DOMContentLoaded', () => {
            setLanguage(currentLang, false);
            renderMenu('all');
            updateCartUI();
            setupScrollAnimations();
            setupFormPlaceholders();
        });

        function toggleLanguage() {
            currentLang = currentLang === 'en' ? 'ar' : 'en';
            setLanguage(currentLang, true);
        }

        function setLanguage(lang, save) {
            currentLang = lang;
            document.documentElement.lang = lang;
            document.body.dir = lang === 'ar' ? 'rtl' : 'ltr';

            document.querySelectorAll('[data-en][data-ar]').forEach(el => {
                if (el.tagName === 'INPUT' || el.tagName === 'TEXTAREA') {
                    if (el.hasAttribute('placeholder')) {
                        const ph = el.getAttribute('data-' + lang + '-placeholder');
                        if (ph) el.placeholder = ph;
                    }
                } else {
                    el.textContent = el.getAttribute('data-' + lang);
                }
            });

            document.getElementById('lang-text').textContent = lang === 'en' ? 'العربية' : 'English';

            if (save) {
                localStorage.setItem('gabbys_lang', lang);
            }

            const activeBtn = document.querySelector('.category-btn.active');
            const category = activeBtn ? activeBtn.getAttribute('onclick').match(/'([^']+)'/)[1] : 'all';
            renderMenu(category);
            updateCartUI();
        }

        function setupFormPlaceholders() {
            document.querySelectorAll('[data-en-placeholder]').forEach(el => {
                if (currentLang === 'ar' && el.hasAttribute('data-ar-placeholder')) {
                    el.placeholder = el.getAttribute('data-ar-placeholder');
                } else {
                    el.placeholder = el.getAttribute('data-en-placeholder');
                }
            });
        }

        function renderMenu(category) {
            const grid = document.getElementById('menu-grid');
            const items = category === 'all' ? menuData : menuData.filter(i => i.category === category);

            grid.innerHTML = items.map(item => `
                <div class="menu-item fade-in">
                    <div class="menu-item-img">
                        <span style="font-size: 4rem;">${item.emoji}</span>
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <h3>${item.name[currentLang]}</h3>
                            <span class="price">${item.price.toLocaleString()} SYP</span>
                        </div>
                        <p class="desc">${item.desc[currentLang]}</p>
                        <button class="add-to-cart" onclick="addToCart(${item.id})">
                            <i class="fas fa-plus"></i>
                            <span data-en="Add" data-ar="إضافة">Add</span>
                        </button>
                    </div>
                </div>
            `).join('');

            setTimeout(() => {
                document.querySelectorAll('.fade-in').forEach(el => el.classList.add('visible'));
            }, 50);
        }

        function filterMenu(category, btn) {
            document.querySelectorAll('.category-btn').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
            renderMenu(category);
        }

        function addToCart(id) {
            const item = menuData.find(i => i.id === id);
            const existing = cart.find(c => c.id === id);

            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...item, qty: 1 });
            }

            saveCart();
            updateCartUI();
            showToast(currentLang === 'ar' ? 'تمت الإضافة إلى السلة!' : 'Added to cart!');
        }

        function removeFromCart(id) {
            cart = cart.filter(c => c.id !== id);
            saveCart();
            updateCartUI();
        }

        function updateQty(id, delta) {
            const item = cart.find(c => c.id === id);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    removeFromCart(id);
                    return;
                }
                saveCart();
                updateCartUI();
            }
        }

        function saveCart() {
            localStorage.setItem('gabbys_cart', JSON.stringify(cart));
        }

        function updateCartUI() {
            const count = cart.reduce((sum, c) => sum + c.qty, 0);
            document.getElementById('cart-count').textContent = count;

            const itemsContainer = document.getElementById('cart-items');
            const footer = document.getElementById('cart-footer');

            if (cart.length === 0) {
                itemsContainer.innerHTML = `
                    <div class="empty-cart">
                        <i class="fas fa-shopping-basket"></i>
                        <p>${currentLang === 'ar' ? 'سلتك فارغة' : 'Your cart is empty'}</p>
                    </div>
                `;
                footer.style.display = 'none';
            } else {
                itemsContainer.innerHTML = cart.map(item => `
                    <div class="cart-item">
                        <div class="cart-item-info">
                            <h4>${item.name[currentLang]}</h4>
                            <span class="item-price">${(item.price * item.qty).toLocaleString()} SYP</span>
                            <div class="qty-controls">
                                <button class="qty-btn" onclick="updateQty(${item.id}, -1)">-</button>
                                <span>${item.qty}</span>
                                <button class="qty-btn" onclick="updateQty(${item.id}, 1)">+</button>
                            </div>
                        </div>
                        <span class="remove-item" onclick="removeFromCart(${item.id})"><i class="fas fa-trash"></i></span>
                    </div>
                `).join('');

                const total = cart.reduce((sum, c) => sum + (c.price * c.qty), 0);
                document.getElementById('cart-total').textContent = total.toLocaleString() + ' SYP';
                footer.style.display = 'block';
            }
        }

        function toggleCart() {
            document.getElementById('cart-overlay').classList.toggle('active');
            document.getElementById('cart-sidebar').classList.toggle('active');
        }

        function checkout() {
            if (cart.length === 0) return;

            let message = currentLang === 'ar' ? '*طلب جديد من GABBY\'s*%0A%0A' : '*New Order from GABBY\'s*%0A%0A';

            cart.forEach(item => {
                message += `• ${item.name[currentLang]} x${item.qty} = ${(item.price * item.qty).toLocaleString()} SYP%0A`;
            });

            const total = cart.reduce((sum, c) => sum + (c.price * c.qty), 0);
            message += `%0A*${currentLang === 'ar' ? 'المجموع' : 'Total'}: ${total.toLocaleString()} SYP*%0A`;
            message += `%0A${currentLang === 'ar' ? 'الاسم:' : 'Name:'} __%0A`;
            message += `${currentLang === 'ar' ? 'العنوان:' : 'Address:'} __%0A`;
            message += `${currentLang === 'ar' ? 'نوع الطلب:' : 'Order Type:'} ${currentLang === 'ar' ? 'توصيل / استلام' : 'Delivery / Pickup'}%0A`;

            window.open(`https://wa.me/963985482175?text=${message}`, '_blank');
        }

        function showToast(msg) {
            const toast = document.getElementById('toast');
            toast.textContent = msg;
            toast.classList.add('show');
            setTimeout(() => toast.classList.remove('show'), 3000);
        }

        function setupScrollAnimations() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
        }

        function toggleMobileMenu() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
            navLinks.style.position = 'absolute';
            navLinks.style.top = '70px';
            navLinks.style.left = '0';
            navLinks.style.right = '0';
            navLinks.style.flexDirection = 'column';
            navLinks.style.background = 'var(--primary)';
            navLinks.style.padding = '2rem';
            navLinks.style.borderBottom = '1px solid var(--border)';
        }

        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                document.getElementById('cart-overlay').classList.remove('active');
                document.getElementById('cart-sidebar').classList.remove('active');
            }
        });
    </script>
</body>
</html>
