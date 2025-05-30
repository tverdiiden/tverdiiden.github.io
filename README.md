<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kozhemyakoff | Мастерская эксклюзивных кожаных ремней | Ульяновск</title>
    <meta name="description" content="Ручное изготовление премиальных кожаных ремней по индивидуальным меркам. Натуральная кожа, эксклюзивная фурнитура, пожизненная гарантия.">
    
    <!-- Премиальные шрифты -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Marcellus&family=Marcellus+SC&family=Cormorant+Garamond:wght@400;500;600;700&family=EB+Garamond:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Основные стили -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css">

    <style>
        /* Основные переменные */
        :root {
            --primary: #2a1a0f;
            --secondary: #5d3a21;
            --light: #f8f4ee;
            --dark: #1a120b;
            --accent: #b78b5f;
            --gold: #d4af6b;
            --font-heading: 'Marcellus SC', serif;
            --font-subheading: 'Marcellus', serif;
            --font-body: 'Cormorant Garamond', serif;
        }

        /* Базовые стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            color: var(--dark);
            line-height: 1.8;
            background-color: var(--light);
            background-image: url('https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80');
            background-attachment: fixed;
            background-size: cover;
            background-position: center;
            background-blend-mode: overlay;
            font-family: var(--font-body);
            font-size: 1.2rem;
            font-weight: 400;
            overflow-x: hidden;
            margin: 0;
            padding: 0;
        }

        h1, h2, h3, h4 {
            font-family: var(--font-heading);
            font-weight: 400;
            letter-spacing: 1px;
            color: var(--primary);
            text-transform: uppercase;
        }

        h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
        }

        h2 {
            font-size: 2.8rem;
            position: relative;
            display: inline-block;
            margin-bottom: 3rem;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, var(--primary), var(--gold), transparent);
        }

        h3 {
            font-size: 1.8rem;
            font-family: var(--font-subheading);
            margin-bottom: 1rem;
        }

        /* Липкий хедер */
        header.sticky {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(248, 244, 238, 0.98);
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            animation: fadeInDown 0.5s ease;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Навигация */
        #header {
            background-color: var(--light);
            padding: 1rem 0;
            position: relative;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }

        .nav-menu {
            display: flex;
            list-style: none;
        }

        .nav-item {
            margin-left: 2rem;
        }

        .nav-link {
            color: var(--primary);
            text-decoration: none;
            font-family: var(--font-subheading);
            font-size: 1.1rem;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }

        .nav-link:hover {
            color: var(--accent);
        }

        .nav-link i {
            margin-right: 8px;
        }

        .mobile-menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary);
        }

        /* Главный баннер */
        .hero {
            height: 100vh;
            min-height: 800px;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(26, 18, 11, 0.8), rgba(26, 18, 11, 0.6));
            z-index: -1;
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 1;
        }

        .hero p {
            font-family: var(--font-subheading);
            font-size: 1.5rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }

        /* Кнопки */
        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 0;
            font-family: var(--font-heading);
            font-size: 1rem;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-decoration: none;
            cursor: pointer;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            color: white;
        }

        .btn:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: all 0.6s ease;
        }

        .btn:hover:before {
            left: 100%;
        }

        /* Секции */
        .section {
            padding: 6rem 0;
            position: relative;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* О нас */
        .about-content {
            display: flex;
            align-items: center;
            gap: 4rem;
        }

        .about-text {
            flex: 1;
        }

        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            line-height: 1.8;
        }

        .about-image {
            flex: 1;
            position: relative;
        }

        .about-image img {
            width: 100%;
            height: auto;
            border-radius: 5px;
            box-shadow: 20px 20px 0 var(--accent);
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.02);
        }

        /* Коллекция */
        .belts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .belt-card {
            background: white;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
        }

        .belt-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .belt-image {
            height: 400px;
            overflow: hidden;
            position: relative;
        }

        .belt-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }

        .belt-card:hover .belt-image img {
            transform: scale(1.05);
        }

        .belt-info {
            padding: 2rem;
            border-top: 1px solid rgba(0,0,0,0.05);
        }

        .belt-title {
            font-family: var(--font-subheading);
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .belt-price {
            font-family: var(--font-heading);
            font-size: 1.4rem;
            color: var(--gold);
            margin-bottom: 1.5rem;
        }

        /* Процесс создания */
        .process-steps {
            display: grid;
            gap: 3rem;
            margin-top: 3rem;
        }

        .process-step {
            display: flex;
            gap: 3rem;
            align-items: center;
        }

        .step-image {
            flex: 1;
        }

        .step-image img {
            width: 100%;
            border-radius: 5px;
            box-shadow: 15px 15px 0 var(--accent);
        }

        .step-content {
            flex: 1;
        }

        .step-content h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .step-content p {
            font-size: 1.2rem;
            line-height: 1.8;
        }

        /* Контакты */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-info {
            display: grid;
            gap: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-top: 0.3rem;
        }

        .contact-text h3 {
            margin-bottom: 0.5rem;
            font-family: var(--font-subheading);
        }

        .contact-text a {
            color: var(--primary);
            text-decoration: none;
            border-bottom: 1px dotted var(--accent);
            transition: all 0.3s ease;
        }

        .contact-text a:hover {
            color: var(--accent);
            border-bottom: 1px solid var(--accent);
        }

        .contact-map {
            height: 500px;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 20px 20px 0 var(--accent);
        }

        .contact-map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        /* Форма */
        .form-container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            border-radius: 5px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-family: var(--font-subheading);
            color: var(--primary);
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 3px;
            font-family: var(--font-body);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(183, 139, 95, 0.1);
        }

        .form-group textarea {
            min-height: 150px;
        }

        /* Подвал */
        footer {
            background-color: var(--primary);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-logo {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            color: white;
            margin-bottom: 1.5rem;
            display: inline-block;
            text-decoration: none;
        }

        .footer-about p {
            margin-bottom: 1.5rem;
            opacity: 0.8;
            line-height: 1.8;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            color: white;
            border-radius: 50%;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        .footer-links h3 {
            color: white;
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.8rem;
        }

        .footer-links a {
            color: rgba(255,255,255,0.8);
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }

        /* Анимации */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            opacity: 0;
            animation: fadeIn 1s ease forwards;
        }

        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }

        /* Адаптивность */
        @media (max-width: 992px) {
            .about-content,
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .about-image,
            .contact-map {
                margin-top: 3rem;
            }
            
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
        }

        @media (max-width: 768px) {
            .header-container {
                padding: 1rem;
            }
            
            .nav-menu {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: var(--light);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: all 0.5s ease;
            }
            
            .nav-menu.active {
                left: 0;
            }
            
            .nav-item {
                margin: 1rem 0;
            }
            
            .mobile-menu-toggle {
                display: block;
            }
            
            .hero {
                min-height: 600px;
                padding-top: 80px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 4rem 0;
            }
            
            .belt-image {
                height: 300px;
            }
            
            .process-step {
                flex-direction: column;
            }
        }

        @media (max-width: 576px) {
            h1 {
                font-size: 1.8rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .btn {
                padding: 0.8rem 1.5rem;
                font-size: 0.9rem;
            }
            
            .belts-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header id="header">
        <div class="header-container">
            <div class="logo-wrapper">
                <a href="#" class="logo">
                    <span class="logo-icon"><i class="fas fa-hammer"></i></span>
                    <span class="logo-text">Kozhemyakoff</span>
                    <span class="logo-sublogo">Leather Atelier</span>
                </a>
            </div>
            
            <nav class="main-nav">
                <ul class="nav-menu" id="navMenu">
                    <li class="nav-item">
                        <a href="#about" class="nav-link">
                            <span class="nav-icon"><i class="fas fa-user-tie"></i></span>
                            <span class="nav-text">О Мастере</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#collection" class="nav-link">
                            <span class="nav-icon"><i class="fas fa-belt"></i></span>
                            <span class="nav-text">Коллекция</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#process" class="nav-link">
                            <span class="nav-icon"><i class="fas fa-tools"></i></span>
                            <span class="nav-text">Процесс</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#contact" class="nav-link">
                            <span class="nav-icon"><i class="fas fa-envelope"></i></span>
                            <span class="nav-text">Контакты</span>
                        </a>
                    </li>
                    <li class="nav-item cart-item">
                        <a href="#order" class="nav-link cart-link">
                            <span class="nav-icon"><i class="fas fa-shopping-bag"></i></span>
                            <span class="cart-count">0</span>
                        </a>
                    </li>
                </ul>
            </nav>
            
            <div class="mobile-menu-toggle" id="menuToggle">
                <i class="fas fa-bars"></i>
            </div>
        </div>
        
        <div class="header-divider">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 100" preserveAspectRatio="none">
                <path fill="var(--light)" d="M0,0V100H1440V0S1220,40 1000,40 720,20 360,20 0,40 0,40Z"></path>
            </svg>
        </div>
    </header>

    <!-- Главный баннер -->
    <section class="hero">
        <div class="hero-content">
            <h1 class="fade-in">Эксклюзивные кожаные ремни</h1>
            <p class="fade-in delay-1">Ручная работа из отборной кожи с пожизненной гарантией</p>
            <a href="#collection" class="btn fade-in delay-2">Открыть коллекцию</a>
        </div>
    </section>

    <!-- О нас -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title fade-in">О Мастере</h2>
            
            <div class="about-content">
                <div class="about-text fade-in">
                    <h3>Искусство кожевенного дела</h3>
                    <p>Мастерская Kozhemyakoff создает эксклюзивные кожаные ремни в Ульяновске с 2015 года. Каждое изделие - это воплощение традиций европейского кожевенного дела с вниманием к деталям.</p>
                    <p>Мы используем только натуральную кожу высшего качества толщиной 3.5-4 мм от проверенных поставщиков Италии и Франции. Все ремни прошиваются вручную армированными нитями с пропиткой из пчелиного воска.</p>
                    <p>Наши ремни - это не просто аксессуар, а вещь, которая будет служить вам годами, приобретая благородную патину времени. Мы даем пожизненную гарантию на швы и фурнитуру.</p>
                </div>
                
                <div class="about-image fade-in delay-1">
                    <img src="https://images.unsplash.com/photo-1606813907291-d86efa9b94db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80" alt="Мастер за работой" loading="lazy">
                </div>
            </div>
        </div>
    </section>

    <!-- Коллекция -->
    <section id="collection" class="section">
        <div class="container">
            <h2 class="section-title fade-in">Коллекция</h2>
            
            <div class="belts-grid">
                <!-- Ремень 1 -->
                <div class="belt-card fade-in">
                    <div class="belt-image">
                        <img src="https://images.unsplash.com/photo-1591047139829-d91aecb6caea?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=736&q=80" alt="Ремень Heritage из воловьей кожи" loading="lazy">
                    </div>
                    <div class="belt-info">
                        <h3 class="belt-title">Heritage</h3>
                        <div class="belt-price">14 800 руб.</div>
                        <p>Классический ремень из цельного куска воловьей кожи, ручная прошивка</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
                
                <!-- Ремень 2 -->
                <div class="belt-card fade-in delay-1">
                    <div class="belt-image">
                        <img src="https://images.unsplash.com/photo-1601924638867-346dc4b53d5c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="Ремень Noble из кожи крокодила" loading="lazy">
                    </div>
                    <div class="belt-info">
                        <h3 class="belt-title">Noble</h3>
                        <div class="belt-price">24 500 руб.</div>
                        <p>Эксклюзивный ремень из кожи крокодила с позолоченной фурнитурой</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
                
                <!-- Ремень 3 -->
                <div class="belt-card fade-in delay-2">
                    <div class="belt-image">
                        <img src="https://images.unsplash.com/photo-1618932260643-eee4a2f652a1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Ремень Rustic из состаренной кожи" loading="lazy">
                    </div>
                    <div class="belt-info">
                        <h3 class="belt-title">Rustic</h3>
                        <div class="belt-price">12 200 руб.</div>
                        <p>Ремень из состаренной кожи с эффектом патины, ручная гравировка</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Процесс создания -->
    <section id="process" class="section">
        <div class="container">
            <h2 class="section-title fade-in">Процесс создания</h2>
            
            <div class="process-steps">
                <!-- Шаг 1 -->
                <div class="process-step fade-in">
                    <div class="step-image">
                        <img src="https://images.unsplash.com/photo-1604176354204-9268737828e4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Отбор кожи" loading="lazy">
                    </div>
                    <div class="step-content">
                        <h3>1. Отбор кожи</h3>
                        <p>Каждый ремень начинается с тщательного отбора кожи. Мы используем только лучшие куски толщиной 3.5-4 мм от проверенных поставщиков.</p>
                    </div>
                </div>
                
                <!-- Шаг 2 -->
                <div class="process-step fade-in delay-1">
                    <div class="step-image">
                        <img src="https://images.unsplash.com/photo-1603904587315-48f8f6f66804?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Раскрой" loading="lazy">
                    </div>
                    <div class="step-content">
                        <h3>2. Раскрой</h3>
                        <p>Каждый ремень выкраивается вручную с учетом направления волокон кожи для максимальной прочности и долговечности.</p>
                    </div>
                </div>
                
                <!-- Шаг 3 -->
                <div class="process-step fade-in delay-2">
                    <div class="step-image">
                        <img src="https://images.unsplash.com/photo-1601924994980-3a2d5d2adf4f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Ручная прошивка" loading="lazy">
                    </div>
                    <div class="step-content">
                        <h3>3. Ручная прошивка</h3>
                        <p>Все ремни прошиваются вручную вощеными нитями с двойной прострочкой для максимальной надежности.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Контакты -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title fade-in">Контакты</h2>
            
            <div class="contact-grid">
                <div class="contact-info fade-in">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Адрес мастерской</h3>
                            <p>г. Ульяновск, ул. Гончарова, 30</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Телефон</h3>
                            <p><a href="tel:+79170592443">+7 (917) 059-24-43</a></p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fab fa-vk"></i>
                        </div>
                        <div class="contact-text">
                            <h3>ВКонтакте</h3>
                            <p><a href="https://vk.com/kozhemyakoff" target="_blank">vk.com/kozhemyakoff</a></p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Часы работы</h3>
                            <p>Пн-Пт: 10:00 - 19:00<br>Сб: 11:00 - 16:00<br>Вс: выходной</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-map fade-in delay-1">
                    <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3A1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p&amp;source=constructor" loading="lazy" frameborder="0"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Форма заказа -->
    <section id="order" class="section">
        <div class="container">
            <div class="form-container fade-in">
                <h2 class="section-title">Оформить заказ</h2>
                
                <form id="orderForm">
                    <div class="form-group">
                        <label for="name">Ваше имя</label>
                        <input type="text" id="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">Телефон</label>
                        <input type="tel" id="phone" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email">
                    </div>
                    
                    <div class="form-group">
                        <label for="model">Модель ремня</label>
                        <select id="model" required>
                            <option value="">Выберите модель</option>
                            <option value="Heritage">Heritage - 14 800 руб.</option>
                            <option value="Noble">Noble - 24 500 руб.</option>
                            <option value="Rustic">Rustic - 12 200 руб.</option>
                            <option value="Individual">Индивидуальный пошив</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="size">Размер (см)</label>
                        <input type="number" id="size" min="70" max="130" placeholder="От 70 до 130 см">
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Дополнительные пожелания</label>
                        <textarea id="message" placeholder="Цвет кожи, особенности пряжки и т.д."></textarea>
                    </div>
                    
                    <div class="form-group">
                        <input type="checkbox" id="privacy" required>
                        <label for="privacy">Я согласен на обработку персональных данных</label>
                    </div>
                    
                    <button type="submit" class="btn">Отправить заявку</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Подвал -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-about">
                    <a href="#" class="footer-logo">Kozhemyakoff</a>
                    <p>Мастерская эксклюзивных кожаных ремней ручной работы в Ульяновске. Изготавливаем с 2015 года с любовью к деталям.</p>
                    <div class="social-links">
                        <a href="https://vk.com/kozhemyakoff" target="_blank"><i class="fab fa-vk"></i></a>
                        <a href="https://wa.me/79170592443" target="_blank"><i class="fab fa-whatsapp"></i></a>
                        <a href="https://t.me/kozhemyakoff" target="_blank"><i class="fab fa-telegram"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>Меню</h3>
                    <ul>
                        <li><a href="#about">О Мастере</a></li>
                        <li><a href="#collection">Коллекция</a></li>
                        <li><a href="#process">Процесс</a></li>
                        <li><a href="#contact">Контакты</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Каталог</h3>
                    <ul>
                        <li><a href="#collection">Heritage</a></li>
                        <li><a href="#collection">Noble</a></li>
                        <li><a href="#collection">Rustic</a></li>
                        <li><a href="#order">Индивидуальный пошив</a></li>
                    </ul>
                </div>
                
                <div class="footer-contact">
                    <h3>Контакты</h3>
                    <p><i class="fas fa-phone-alt"></i> +7 (917) 059-24-43</p>
                    <p><i class="fas fa-envelope"></i> kozhemyakoff.ul@mail.ru</p>
                    <p><i class="fas fa-map-marker-alt"></i> г. Ульяновск, ул. Гончарова, 30</p>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2023 Kozhemyakoff. Все права защищены.
            </div>
        </div>
    </footer>

    <!-- Основные библиотеки -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/js/lightbox.min.js"></script>

    <!-- Кастомные скрипты -->
    <script>
        // Основные функции
        document.addEventListener('DOMContentLoaded', function() {
            // Мобильное меню
            const menuToggle = document.getElementById('menuToggle');
            const navMenu = document.getElementById('navMenu');
            
            menuToggle.addEventListener('click', function() {
                navMenu.classList.toggle('active');
                this.innerHTML = navMenu.classList.contains('active') ? 
                    '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
            });

            // Плавная прокрутка
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        window.scrollTo({
                            top: target.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });

            // Липкий хедер
            window.addEventListener('scroll', function() {
                const header = document.getElementById('header');
                if (window.scrollY > 100) {
                    header.classList.add('sticky');
                } else {
                    header.classList.remove('sticky');
                }
            });

            // Инициализация слайдера
            if (document.querySelector('.swiper')) {
                new Swiper('.swiper', {
                    loop: true,
                    autoplay: {
                        delay: 5000,
                    },
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,
                    },
                });
            }

            // Корзина
            const cart = JSON.parse(localStorage.getItem('cart')) || [];
            updateCart();

            function updateCart() {
                const cartCount = document.querySelector('.cart-count');
                const cartTotal = document.querySelector('.cart-total span');
                let total = 0;
                
                cart.forEach(item => {
                    total += item.price * item.quantity;
                });
                
                cartCount.textContent = cart.length;
                if (cartTotal) cartTotal.textContent = total;
                
                localStorage.setItem('cart', JSON.stringify(cart));
            }

            // Обработка форм
            document.querySelectorAll('form').forEach(form => {
                form.addEventListener('submit', function(e) {
                    e.preventDefault();
                    // Здесь должна быть AJAX-отправка
                    alert('Форма отправлена! Мы свяжемся с вами в ближайшее время.');
                    this.reset();
                });
            });
        });

        // Lazy Load для изображений
        if ('IntersectionObserver' in window) {
            const lazyImages = document.querySelectorAll('img[loading="lazy"]');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const img = entry.target;
                        img.src = img.dataset.src;
                        observer.unobserve(img);
                    }
                });
            });
            
            lazyImages.forEach(img => observer.observe(img));
        }
    </script>
</body>
</html>
