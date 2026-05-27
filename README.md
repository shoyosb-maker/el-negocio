<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>CareerForge | Outsourcing + Capacitación Profesional</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=Poppins:wght@500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #fafcff;
            color: #111827;
            overflow-x: hidden;
            width: 100%;
        }

        h1, h2, h3, .logo {
            font-family: 'Poppins', sans-serif;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 20px;
            width: 100%;
        }

        /* Header / Navbar - Responsive */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 0;
            flex-wrap: wrap;
            gap: 16px;
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 800;
            background: linear-gradient(135deg, #0B2B5E, #1E4A7A);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-decoration: none;
            cursor: pointer;
            letter-spacing: -0.5px;
        }
        
        .logo span {
            background: linear-gradient(135deg, #F59E0B, #F59E0B);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .nav-links button {
            background: none;
            border: none;
            margin-left: 16px;
            font-weight: 600;
            color: #1f2937;
            font-size: 0.95rem;
            cursor: pointer;
            transition: 0.2s;
            font-family: 'Inter', sans-serif;
            padding: 8px 0;
        }

        .nav-links button:first-child {
            margin-left: 0;
        }

        .nav-links button:hover, .nav-links button.active {
            color: #F59E0B;
        }

        .btn-login-nav {
            background: #0B2B5E !important;
            color: white !important;
            padding: 8px 20px !important;
            border-radius: 40px !important;
            margin-left: 16px !important;
        }

        .btn-login-nav:hover {
            background: #F59E0B !important;
            color: #0B2B5E !important;
        }

        .user-avatar {
            display: flex;
            align-items: center;
            gap: 8px;
            background: #0B2B5E;
            padding: 6px 16px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            margin-left: 16px;
            transition: 0.2s;
            font-size: 0.9rem;
        }

        .user-avatar:hover {
            background: #F59E0B;
            color: #0B2B5E;
        }

        /* Pages */
        .page {
            display: none;
            animation: fadeIn 0.3s ease;
        }

        .page.active-page {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Botones responsivos */
        .btn-primary, .btn-secondary {
            padding: 12px 24px;
            font-size: 0.95rem;
        }

        .btn-primary {
            background: #25D366;
            color: white;
            border-radius: 40px;
            font-weight: 700;
            border: none;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: transform 0.2s;
            box-shadow: 0 8px 20px rgba(37,211,102,0.25);
        }

        .btn-primary:hover {
            transform: scale(1.02);
            background: #20b859;
        }

        .btn-secondary {
            background: white;
            border: 2px solid #0B2B5E;
            color: #0B2B5E;
            border-radius: 40px;
            font-weight: 700;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-secondary:hover {
            background: #0B2B5E;
            color: white;
        }

        /* Hero responsive */
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            padding: 40px 0 30px;
            gap: 30px;
        }

        .hero-left {
            flex: 1;
            min-width: 280px;
        }

        .hero-left h1 {
            font-size: 2.5rem;
            line-height: 1.2;
            font-weight: 800;
            background: linear-gradient(135deg, #0B2B5E, #2C3E66);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero-left p {
            font-size: 1rem;
            margin: 20px 0;
            color: #4b5563;
        }

        .hero-right {
            flex: 1;
            min-width: 260px;
            background: linear-gradient(145deg, #EFF3FC, #FFFFFF);
            padding: 25px;
            border-radius: 32px;
            text-align: center;
        }

        .btn-group {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        /* Jobs section responsive */
        .jobs-section {
            background: white;
            border-radius: 28px;
            padding: 30px 20px;
            margin: 40px 0;
            border: 1px solid #eef2f9;
        }

        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 12px;
            text-align: center;
        }

        .career-selector {
            display: flex;
            justify-content: center;
            gap: 12px;
            flex-wrap: wrap;
            margin-bottom: 28px;
        }

        .career-btn {
            background: #f0f4fa;
            border: none;
            padding: 8px 20px;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            font-size: 0.9rem;
        }

        .jobs-list {
            display: flex;
            flex-direction: column;
            gap: 14px;
            max-height: 400px;
            overflow-y: auto;
        }

        .job-card {
            background: #f9fafc;
            border-left: 4px solid #F59E0B;
            padding: 14px 16px;
            border-radius: 16px;
        }

        .job-title {
            font-weight: 800;
            font-size: 1.05rem;
        }

        /* Servicios grid responsive */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 24px;
            margin: 40px 0;
        }

        .service-card {
            background: white;
            border-radius: 24px;
            padding: 24px 20px;
            text-align: center;
            box-shadow: 0 12px 28px rgba(0,0,0,0.05);
            transition: 0.25s;
        }

        .service-card i {
            font-size: 2.5rem;
            color: #F59E0B;
            margin-bottom: 16px;
        }

        /* Premium materials responsive */
        .premium-materials {
            background: linear-gradient(135deg, #0B2B5E, #1E4A7A);
            border-radius: 28px;
            padding: 30px 20px;
            margin: 40px 0;
            color: white;
        }

        .premium-header {
            text-align: center;
            margin-bottom: 28px;
        }

        .premium-header i {
            font-size: 2.5rem;
            color: #F59E0B;
            margin-bottom: 12px;
        }

        .materials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
        }

        .material-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 20px;
            transition: 0.3s;
            cursor: pointer;
        }

        .material-card i {
            font-size: 1.8rem;
            color: #F59E0B;
            margin-bottom: 12px;
        }

        .material-card h4 {
            font-size: 1.1rem;
            margin-bottom: 6px;
        }

        .material-card p {
            font-size: 0.85rem;
            opacity: 0.9;
            margin-bottom: 12px;
        }

        .material-badge {
            display: inline-block;
            background: #F59E0B;
            color: #0B2B5E;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 700;
        }

        .login-required-message {
            text-align: center;
            padding: 50px 20px;
            background: #f0f4fa;
            border-radius: 28px;
            margin: 40px 0;
        }

        .login-required-message i {
            font-size: 3rem;
            color: #F59E0B;
            margin-bottom: 16px;
        }

        /* Pricing responsive */
        .pricing-card {
            background: white;
            border-radius: 36px;
            padding: 32px 24px;
            text-align: center;
            max-width: 450px;
            margin: 40px auto;
            border: 1px solid #e2edf7;
        }

        .price {
            font-size: 2.8rem;
            font-weight: 800;
            color: #0B2B5E;
            margin: 16px 0;
        }

        .btn-pay {
            background: #0B2B5E;
            color: white;
            width: 100%;
            padding: 14px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1rem;
            border: none;
            cursor: pointer;
        }

        /* Contacto responsive */
        .contact-box {
            background: white;
            border-radius: 40px;
            padding: 35px 25px;
            margin: 50px auto;
            max-width: 600px;
            text-align: center;
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
            padding: 14px 32px;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 800;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            border: none;
            cursor: pointer;
        }

        /* Social section responsive */
        .social-section {
            background: linear-gradient(135deg, #0B2B5E, #1E4A7A);
            border-radius: 28px;
            padding: 30px 20px;
            margin: 40px 0;
            text-align: center;
            color: white;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .social-icon {
            width: 52px;
            height: 52px;
            background: rgba(255,255,255,0.15);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
            text-decoration: none;
            transition: 0.2s;
        }

        /* Modal Login Responsive */
        .login-modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.7);
            align-items: center;
            justify-content: center;
            z-index: 1001;
            padding: 16px;
        }

        .login-container {
            background: white;
            border-radius: 32px;
            width: 100%;
            max-width: 420px;
            padding: 32px 24px;
            position: relative;
        }

        .login-tabs {
            display: flex;
            gap: 12px;
            margin-bottom: 24px;
            border-bottom: 2px solid #eef2f9;
        }

        .login-tab {
            flex: 1;
            text-align: center;
            padding: 10px;
            font-weight: 700;
            cursor: pointer;
        }

        .input-group input {
            padding: 12px 14px;
            border: 1px solid #ddd;
            border-radius: 12px;
            font-size: 0.95rem;
            width: 100%;
        }

        .login-btn {
            background: #0B2B5E;
            color: white;
            padding: 12px;
            border-radius: 40px;
            font-weight: 700;
            cursor: pointer;
            width: 100%;
        }

        .close-modal {
            position: absolute;
            top: 16px;
            right: 20px;
            font-size: 1.3rem;
            cursor: pointer;
        }

        /* Footer responsive */
        footer {
            background: #0B2B5E;
            color: white;
            padding: 32px 0 20px;
            margin-top: 50px;
        }

        .footer-content {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #FFFFFF, #E0E7FF);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-decoration: none;
        }
        
        .footer-logo span {
            background: linear-gradient(135deg, #F59E0B, #FBBF24);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .footer-social {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .footer-social a {
            color: white;
            font-size: 1.3rem;
            transition: 0.2s;
        }

        .footer-social a:hover {
            color: #F59E0B;
        }

        .footer-copy {
            text-align: center;
            padding-top: 20px;
            margin-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.75rem;
        }

        .badge-hard {
            text-align: center;
            margin: 20px auto 30px;
        }
        .badge-hard span {
            background: #F59E0B;
            padding: 5px 20px;
            border-radius: 50px;
            font-weight: 800;
            font-size: 0.8rem;
            display: inline-block;
        }

        /* Modal pago */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            align-items: center;
            justify-content: center;
            z-index: 1000;
            padding: 16px;
        }

        .modal-content {
            background: white;
            max-width: 380px;
            width: 100%;
            border-radius: 28px;
            padding: 28px;
            text-align: center;
        }

        /* Botones flotantes responsive */
        .float-buttons {
            position: fixed;
            bottom: 20px;
            right: 20px;
            display: flex;
            flex-direction: column;
            gap: 12px;
            z-index: 99;
        }

        .whatsapp-float, .chatbot-float {
            width: 52px;
            height: 52px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6rem;
            color: white;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            transition: transform 0.2s;
        }

        .whatsapp-float { background: #25D366; }
        .chatbot-float { background: #0B2B5E; }

        /* Chatbot responsive */
        .chatbot-widget {
            position: fixed;
            bottom: 100px;
            right: 20px;
            width: 340px;
            max-width: calc(100vw - 40px);
            background: white;
            border-radius: 24px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            display: none;
            flex-direction: column;
            z-index: 100;
            overflow: hidden;
        }

        .chatbot-widget.open { display: flex; }

        .chatbot-header {
            background: #0B2B5E;
            color: white;
            padding: 14px 18px;
            display: flex;
            justify-content: space-between;
        }

        .chat-messages {
            height: 320px;
            overflow-y: auto;
            padding: 14px;
            background: #f9fafc;
        }

        .message {
            max-width: 85%;
            padding: 10px 12px;
            border-radius: 18px;
            margin-bottom: 10px;
            font-size: 0.85rem;
        }

        .message.user {
            background: #0B2B5E;
            color: white;
            margin-left: auto;
        }

        .message.bot {
            background: white;
            border: 1px solid #eef2f9;
        }

        .chat-input-area {
            display: flex;
            padding: 10px;
            gap: 8px;
        }

        .chat-input-area input {
            flex: 1;
            padding: 10px 12px;
            border: 1px solid #ddd;
            border-radius: 40px;
            font-size: 0.85rem;
        }

        .chat-input-area button {
            background: #F59E0B;
            border: none;
            border-radius: 40px;
            padding: 0 16px;
            color: white;
            cursor: pointer;
        }

        /* ========== MEDIA QUERIES RESPONSIVAS ========== */
        @media (max-width: 768px) {
            .container {
                padding: 0 16px;
            }
            
            .navbar {
                flex-direction: column;
                text-align: center;
            }
            
            .nav-links {
                justify-content: center;
            }
            
            .nav-links button {
                margin: 0 8px;
                font-size: 0.85rem;
            }
            
            .btn-login-nav {
                margin-left: 8px !important;
                padding: 6px 16px !important;
            }
            
            .user-avatar {
                margin-left: 8px;
                padding: 5px 12px;
                font-size: 0.85rem;
            }
            
            .hero-left h1 {
                font-size: 1.8rem;
            }
            
            .hero-left p {
                font-size: 0.9rem;
            }
            
            .hero {
                padding: 30px 0 20px;
                gap: 24px;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
            
            .services-grid {
                gap: 16px;
            }
            
            .service-card {
                padding: 20px 16px;
            }
            
            .premium-materials {
                padding: 24px 16px;
            }
            
            .materials-grid {
                gap: 16px;
            }
            
            .material-card {
                padding: 16px;
            }
            
            .pricing-card {
                padding: 28px 20px;
                margin: 30px auto;
            }
            
            .price {
                font-size: 2.2rem;
            }
            
            .contact-box {
                padding: 30px 20px;
                margin: 40px auto;
            }
            
            .whatsapp-btn {
                padding: 12px 24px;
                font-size: 1rem;
            }
            
            .social-icon {
                width: 45px;
                height: 45px;
                font-size: 1.3rem;
            }
            
            .footer-content {
                flex-direction: column;
                text-align: center;
                gap: 16px;
            }
            
            .footer-social {
                justify-content: center;
            }
            
            .float-buttons {
                bottom: 16px;
                right: 16px;
            }
            
            .whatsapp-float, .chatbot-float {
                width: 48px;
                height: 48px;
                font-size: 1.4rem;
            }
            
            .chatbot-widget {
                width: 320px;
                bottom: 90px;
                right: 16px;
            }
        }

        @media (max-width: 480px) {
            .hero-left h1 {
                font-size: 1.6rem;
            }
            
            .btn-primary, .btn-secondary {
                padding: 10px 18px;
                font-size: 0.85rem;
            }
            
            .section-title {
                font-size: 1.3rem;
            }
            
            .career-btn {
                padding: 6px 14px;
                font-size: 0.8rem;
            }
            
            .job-card {
                padding: 12px 14px;
            }
            
            .job-title {
                font-size: 0.95rem;
            }
            
            .service-card h3 {
                font-size: 1rem;
            }
            
            .service-card p {
                font-size: 0.8rem;
            }
            
            .login-container {
                padding: 28px 20px;
            }
            
            .chatbot-widget {
                width: 300px;
            }
        }

        @media (min-width: 1280px) {
            .hero-left h1 {
                font-size: 3.2rem;
            }
            
            .container {
                padding: 0 32px;
            }
        }
    </style>
</head>
<body>

<div class="float-buttons">
    <div class="whatsapp-float" id="whatsappFloatBtn"><i class="fab fa-whatsapp"></i></div>
    <div class="chatbot-float" id="chatbotFloatBtn"><i class="fas fa-robot"></i></div>
</div>

<!-- Modal Login -->
<div id="loginModal" class="login-modal">
    <div class="login-container">
        <span class="close-modal" id="closeLoginModal">&times;</span>
        <div class="login-tabs">
            <button class="login-tab active" data-tab="login">Iniciar Sesión</button>
            <button class="login-tab" data-tab="register">Registrarse</button>
        </div>
        <form id="loginForm" class="login-form">
            <div class="input-group"><label>Correo</label><input type="email" id="loginEmail" placeholder="tu@email.com" required></div>
            <div class="input-group"><label>Contraseña</label><input type="password" id="loginPassword" placeholder="••••••••" required></div>
            <button type="submit" class="login-btn">Ingresar</button>
            <p style="text-align:center; font-size:0.75rem; margin-top:12px;">Demo: cualquier email/contraseña (min 4 caracteres)</p>
        </form>
        <form id="registerForm" class="login-form hidden">
            <div class="input-group"><label>Nombre</label><input type="text" id="regName" placeholder="Juan Pérez" required></div>
            <div class="input-group"><label>Correo</label><input type="email" id="regEmail" placeholder="tu@email.com" required></div>
            <div class="input-group"><label>Contraseña</label><input type="password" id="regPassword" placeholder="mínimo 4 caracteres" required></div>
            <button type="submit" class="login-btn">Crear cuenta</button>
        </form>
    </div>
</div>

<!-- Chatbot -->
<div class="chatbot-widget" id="chatbotWidget">
    <div class="chatbot-header"><h3 style="font-size:0.95rem;"><i class="fas fa-brain"></i> CareerForge AI</h3><button class="close-chat" id="closeChatBtn" style="background:none; border:none; color:white; font-size:1.2rem;">&times;</button></div>
    <div class="chat-messages" id="chatMessages"><div class="message bot">👋 ¡Hola! Soy el asistente de CareerForge. ¿En qué puedo ayudarte?</div></div>
    <div class="chat-input-area"><input type="text" id="chatInput" placeholder="Escribe tu mensaje..."><button id="sendChatBtn"><i class="fas fa-paper-plane"></i></button></div>
</div>

<div class="container">
    <nav class="navbar">
        <a href="javascript:void(0)" class="logo" id="navInicioBtn">Career<span>Forge</span></a>
        <div class="nav-links">
            <button id="navTrabajosBtn">Trabajos</button>
            <button id="navCapacitacionBtn">Capacitación</button>
            <button id="navPlanesBtn">Planes</button>
            <button id="navContactoBtn">Contacto</button>
            <button id="loginNavBtn" class="btn-login-nav"><i class="fas fa-user"></i> Iniciar Sesión</button>
            <div id="userMenu" style="display:none;" class="user-avatar"><i class="fas fa-user-circle"></i><span id="userNameDisplay">Usuario</span><i class="fas fa-chevron-down"></i></div>
        </div>
    </nav>

    <!-- INICIO -->
    <div id="page-inicio" class="page active-page">
        <div class="hero">
            <div class="hero-left">
                <h1>Domina tu futuro<br>Consigue el trabajo que mereces</h1>
                <p>Capacitación intensiva + optimización de HV + preparación para entrevistas. Te convertimos en el candidato imparable que toda empresa quiere contratar.</p>
                <div class="btn-group">
                    <button class="btn-primary" id="heroWhatsappBtn"><i class="fab fa-whatsapp"></i> Quiero mi asesoría</button>
                    <button class="btn-secondary" id="heroToJobsBtn"><i class="fas fa-briefcase"></i> Ver trabajos</button>
                </div>
            </div>
            <div class="hero-right">
                <i class="fas fa-chalkboard-user" style="font-size:2.8rem; color:#F59E0B; margin-bottom:12px;"></i>
                <h3 style="font-size:1.2rem;">+300 colocaciones exitosas</h3>
                <p style="font-size:0.9rem;">Top 1% en acompañamiento profesional</p>
                <div style="margin-top:12px;">★★★★★ 5.0 (289 reseñas)</div>
            </div>
        </div>
        <div class="badge-hard"><span>🔥 SOMOS LOS MÁS DUROS DEL MERCADO 🔥</span></div>
    </div>

    <!-- TRABAJOS -->
    <div id="page-trabajos" class="page">
        <div class="jobs-section">
            <h2 class="section-title"><i class="fab fa-linkedin" style="color:#0A66C2;"></i> Ofertas destacadas LinkedIn</h2>
            <div class="career-selector" id="careerSelector">
                <button class="career-btn active" data-career="tecnologia">💻 Tecnología & IT</button>
                <button class="career-btn" data-career="marketing">📊 Marketing & Ventas</button>
                <button class="career-btn" data-career="finanzas">💰 Finanzas & Administración</button>
            </div>
            <div id="jobsContainer" class="jobs-list"><div style="text-align:center; padding:30px;"><i class="fas fa-spinner fa-pulse"></i> Cargando oportunidades...</div></div>
        </div>
    </div>

    <!-- CAPACITACIÓN -->
    <div id="page-capacitacion" class="page">
        <h2 class="section-title" style="margin-top:30px;">📚 Potencia tu perfil profesional</h2>
        <div style="text-align:center; margin:12px 0;"><span style="background:#0B2B5E; color:white; padding:5px 18px; border-radius:50px; font-size:0.8rem;">METODOLOGÍA CERTIFICADA</span></div>
        <div class="services-grid">
            <div class="service-card"><i class="fas fa-file-alt"></i><h3>Revisión HV con IA</h3><p>Análisis ATS + optimización automática.</p></div>
            <div class="service-card"><i class="fas fa-comments"></i><h3>Entrevistas Mock</h3><p>Simulaciones con feedback experto.</p></div>
            <div class="service-card"><i class="fas fa-chart-line"></i><h3>Outsourcing Élite</h3><p>Te postulamos a +50 vacantes por mes.</p></div>
            <div class="service-card"><i class="fas fa-brain"></i><h3>Mentalidad Ganadora</h3><p>Negociación y storytelling.</p></div>
        </div>
        
        <div id="premiumMaterialsContainer"></div>
        
        <div style="text-align:center; margin:30px 0;"><button class="btn-primary" id="capacitacionToPlanesBtn"><i class="fas fa-rocket"></i> ACCEDER A PLAN COMPLETO</button></div>
    </div>

    <!-- PLANES -->
    <div id="page-planes" class="page">
        <div class="pricing-card">
            <i class="fas fa-crown" style="font-size:2.2rem; color:#F59E0B;"></i>
            <h2 style="margin:12px 0;">Plan Élite Insourcing</h2>
            <p>Capacitación completa + IA de postulación + acompañamiento personalizado.</p>
            <div class="price">$49 <span style="font-size:1rem;">/mes</span></div>
            <button id="openPaymentModal" class="btn-pay"><i class="fas fa-credit-card"></i> Acceder Ahora</button>
        </div>
    </div>

    <!-- CONTACTO -->
    <div id="page-contacto" class="page">
        <div class="contact-box">
            <i class="fas fa-headset" style="font-size:3rem; color:#F59E0B;"></i>
            <h1 style="margin:16px 0; font-size:1.6rem;">¿Listo para transformar tu carrera?</h1>
            <button id="contactWhatsappBtn" class="whatsapp-btn"><i class="fab fa-whatsapp"></i> CHATEAR AHORA</button>
        </div>
        <div class="social-section">
            <div class="social-title" style="font-size:1.3rem;"><i class="fas fa-share-alt"></i> Conéctate con nosotros</div>
            <div class="social-icons">
                <a href="#" class="social-icon" id="socialLinkedin"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-icon" id="socialInstagram"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-icon" id="socialFacebook"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="social-icon" id="socialTwitter"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-icon" id="socialYoutube"><i class="fab fa-youtube"></i></a>
            </div>
        </div>
    </div>
</div>

<footer>
    <div class="footer-content">
        <a href="javascript:void(0)" class="footer-logo" id="footerLogoBtn">Career<span>Forge</span></a>
        <div class="footer-social">
            <a href="#" id="footerLinkedin"><i class="fab fa-linkedin-in"></i></a>
            <a href="#" id="footerInstagram"><i class="fab fa-instagram"></i></a>
            <a href="#" id="footerFacebook"><i class="fab fa-facebook-f"></i></a>
            <a href="#" id="footerTwitter"><i class="fab fa-twitter"></i></a>
            <a href="#" id="footerYoutube"><i class="fab fa-youtube"></i></a>
        </div>
    </div>
    <div class="footer-copy"><p>© 2025 CareerForge — Outsourcing & Career Accelerator. Potenciamos tu talento.</p></div>
</footer>

<div id="paymentModal" class="modal"><div class="modal-content"><i class="fas fa-lock" style="font-size:2rem;"></i><h3 style="margin:12px 0;">Pago seguro</h3><button id="mockPayBtn" class="btn-pay" style="margin:12px 0;">Simular Pago Exitoso</button><button id="closeModalBtn" class="btn-secondary" style="width:100%;">Cancelar</button></div></div>

<script>
    // WHATSAPP
    const WHATSAPP_NUMBER = "573001234567";
    function sendWhatsApp(msg = "Hola! Quiero impulsar mi carrera con CareerForge") {
        window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(msg)}`, '_blank');
    }
    document.getElementById('heroWhatsappBtn')?.addEventListener('click',()=>sendWhatsApp());
    document.getElementById('contactWhatsappBtn')?.addEventListener('click',()=>sendWhatsApp());
    document.getElementById('whatsappFloatBtn')?.addEventListener('click',()=>sendWhatsApp());
    
    // REDES SOCIALES
    const SOCIAL = { linkedin:"https://linkedin.com/company/careerforge", instagram:"https://instagram.com/careerforge", facebook:"https://facebook.com/careerforge", twitter:"https://twitter.com/careerforge", youtube:"https://youtube.com/@careerforge" };
    ['socialLinkedin','footerLinkedin'].forEach(id=>document.getElementById(id)?.setAttribute('href',SOCIAL.linkedin));
    ['socialInstagram','footerInstagram'].forEach(id=>document.getElementById(id)?.setAttribute('href',SOCIAL.instagram));
    ['socialFacebook','footerFacebook'].forEach(id=>document.getElementById(id)?.setAttribute('href',SOCIAL.facebook));
    ['socialTwitter','footerTwitter'].forEach(id=>document.getElementById(id)?.setAttribute('href',SOCIAL.twitter));
    ['socialYoutube','footerYoutube'].forEach(id=>document.getElementById(id)?.setAttribute('href',SOCIAL.youtube));
    
    // NAVEGACIÓN
    const pages = { inicio:document.getElementById('page-inicio'), trabajos:document.getElementById('page-trabajos'), capacitacion:document.getElementById('page-capacitacion'), planes:document.getElementById('page-planes'), contacto:document.getElementById('page-contacto') };
    function showPage(pageId) { Object.values(pages).forEach(p=>p.classList.remove('active-page')); pages[pageId].classList.add('active-page'); ['navTrabajosBtn','navCapacitacionBtn','navPlanesBtn','navContactoBtn'].forEach(id=>document.getElementById(id)?.classList.remove('active')); if(pageId!=='inicio') document.getElementById(`nav${pageId.charAt(0).toUpperCase()+pageId.slice(1)}Btn`)?.classList.add('active'); }
    document.getElementById('navTrabajosBtn')?.addEventListener('click',()=>showPage('trabajos'));
    document.getElementById('navCapacitacionBtn')?.addEventListener('click',()=>showPage('capacitacion'));
    document.getElementById('navPlanesBtn')?.addEventListener('click',()=>showPage('planes'));
    document.getElementById('navContactoBtn')?.addEventListener('click',()=>showPage('contacto'));
    document.getElementById('navInicioBtn')?.addEventListener('click',()=>showPage('inicio'));
    document.getElementById('footerLogoBtn')?.addEventListener('click',()=>showPage('inicio'));
    document.getElementById('heroToJobsBtn')?.addEventListener('click',()=>showPage('trabajos'));
    document.getElementById('capacitacionToPlanesBtn')?.addEventListener('click',()=>showPage('planes'));
    
    // JOBS
    const jobsDB = { tecnologia:[{title:"Ingeniero Software Senior", company:"LinkedIn Corp", location:"Remoto"},{title:"Data Scientist", company:"Google", location:"CDMX"}], marketing:[{title:"Growth Manager", company:"HubSpot", location:"Bogotá"}], finanzas:[{title:"Financial Analyst", company:"JP Morgan", location:"Bogotá"}] };
    function fetchJobs(career) { const container = document.getElementById('jobsContainer'); container.innerHTML = '<div style="text-align:center; padding:30px;"><i class="fas fa-spinner fa-pulse"></i> Cargando...</div>'; setTimeout(()=>{ const jobs = jobsDB[career]; container.innerHTML = jobs.map(job=>`<div class="job-card"><div class="job-title">${job.title}</div><div class="job-company"><i class="fab fa-linkedin"></i> ${job.company}</div><div class="job-location">📍 ${job.location}</div><div style="margin-top:10px;"><button class="btn-secondary" style="padding:6px 14px; font-size:0.8rem;" onclick="sendWhatsApp('Me interesa ${job.title}')">Aplicar</button></div></div>`).join(''); },300); }
    document.querySelectorAll('.career-btn').forEach(btn=>{ btn.addEventListener('click',function(){ document.querySelectorAll('.career-btn').forEach(b=>b.classList.remove('active')); this.classList.add('active'); fetchJobs(this.dataset.career); }); }); fetchJobs('tecnologia');
    
    // MATERIAL PREMIUM
    const premiumMaterials = [
        { icon:"fas fa-video", title:"Masterclass: Cómo pasar un ATS", desc:"Optimiza tu HV para filtros automatizados", type:"Video", duration:"45 min" },
        { icon:"fas fa-file-pdf", title:"Guía de entrevista por competencias", desc:"Preguntas frecuentes y cómo responderlas", type:"PDF", pages:"28 páginas" },
        { icon:"fas fa-chalkboard", title:"Webinar: Negociación salarial", desc:"Técnicas para aumentar tu oferta", type:"Webinar", duration:"60 min" }
    ];
    function renderPremiumMaterials() {
        const container = document.getElementById('premiumMaterialsContainer');
        const isLoggedIn = localStorage.getItem('careerforge_user') !== null;
        if(!container) return;
        if(isLoggedIn) {
            const user = JSON.parse(localStorage.getItem('careerforge_user'));
            container.innerHTML = `<div class="premium-materials"><div class="premium-header"><i class="fas fa-gem"></i><h2 style="font-size:1.3rem;">🎓 Material Exclusivo para ${user.name.split(' ')[0]}</h2><p style="font-size:0.85rem;">Contenido premium desbloqueado</p></div><div class="materials-grid">${premiumMaterials.map(mat => `<div class="material-card" onclick="alert('🔓 Contenido exclusivo: ${mat.title}')"><i class="${mat.icon}"></i><h4>${mat.title}</h4><p>${mat.desc}</p><span class="material-badge">${mat.type} · ${mat.duration || mat.pages}</span></div>`).join('')}</div><div style="text-align:center; margin-top:24px;"><button class="btn-secondary" id="accessAllMaterialsBtn" style="background:#F59E0B; color:#0B2B5E; border:none; padding:10px 20px;">Descargar recursos</button></div></div>`;
            document.getElementById('accessAllMaterialsBtn')?.addEventListener('click', () => { alert("📚 Enlace enviado a tu correo."); sendWhatsApp("Quiero acceder al material premium."); });
        } else {
            container.innerHTML = `<div class="login-required-message"><i class="fas fa-lock"></i><h3 style="font-size:1.2rem;">🔒 Contenido Exclusivo</h3><p>Accede a masterclasses, guías y webinars exclusivos.</p><button id="unlockMaterialsBtn" class="btn-primary" style="margin-top:16px;"><i class="fas fa-sign-in-alt"></i> Iniciar Sesión</button></div>`;
            document.getElementById('unlockMaterialsBtn')?.addEventListener('click', () => { document.getElementById('loginModal').style.display = 'flex'; });
        }
    }
    
    // LOGIN
    const loginModal = document.getElementById('loginModal');
    const loginNavBtn = document.getElementById('loginNavBtn');
    const closeLoginModal = document.getElementById('closeLoginModal');
    const userMenu = document.getElementById('userMenu');
    const userNameDisplay = document.getElementById('userNameDisplay');
    const loginTab = document.querySelector('[data-tab="login"]');
    const registerTab = document.querySelector('[data-tab="register"]');
    const loginFormElem = document.getElementById('loginForm');
    const registerFormElem = document.getElementById('registerForm');
    
    loginTab?.addEventListener('click',()=>{ loginTab.classList.add('active'); registerTab.classList.remove('active'); loginFormElem.classList.remove('hidden'); registerFormElem.classList.add('hidden'); });
    registerTab?.addEventListener('click',()=>{ registerTab.classList.add('active'); loginTab.classList.remove('active'); loginFormElem.classList.add('hidden'); registerFormElem.classList.remove('hidden'); });
    
    function updateUI() {
        const user = localStorage.getItem('careerforge_user');
        if(user) {
            const userData = JSON.parse(user);
            loginNavBtn.style.display = 'none';
            userMenu.style.display = 'flex';
            userNameDisplay.textContent = userData.name.split(' ')[0];
            renderPremiumMaterials();
        } else {
            loginNavBtn.style.display = 'block';
            userMenu.style.display = 'none';
            renderPremiumMaterials();
        }
    }
    
    loginNavBtn?.addEventListener('click',()=>loginModal.style.display='flex');
    closeLoginModal?.addEventListener('click',()=>loginModal.style.display='none');
    window.addEventListener('click',(e)=>{ if(e.target===loginModal) loginModal.style.display='none'; });
    
    document.getElementById('loginForm')?.addEventListener('submit',(e)=>{ e.preventDefault(); const email = document.getElementById('loginEmail').value; const password = document.getElementById('loginPassword').value; if(email && password.length>=1){ const stored = localStorage.getItem('careerforge_user'); if(stored){ const u=JSON.parse(stored); if(u.email===email && u.password===password){ alert(`✅ ¡Bienvenido ${u.name}!`); loginModal.style.display='none'; updateUI(); } else alert('❌ Credenciales incorrectas'); } else alert('❌ Regístrate primero'); } else alert('Completa los campos'); });
    
    document.getElementById('registerForm')?.addEventListener('submit',(e)=>{ e.preventDefault(); const name=document.getElementById('regName').value; const email=document.getElementById('regEmail').value; const password=document.getElementById('regPassword').value; if(name && email && password.length>=4){ localStorage.setItem('careerforge_user',JSON.stringify({name,email,password})); alert(`✅ Cuenta creada, ${name}! Ahora inicia sesión.`); loginTab.click(); document.getElementById('loginEmail').value=email; } else alert('Completa todos los campos (mín 4 caracteres)'); });
    
    userMenu?.addEventListener('click',()=>{ if(confirm('¿Cerrar sesión?')){ localStorage.removeItem('careerforge_user'); updateUI(); alert('Sesión cerrada'); } });
    
    // MODAL PAGO
    const modal = document.getElementById('paymentModal');
    document.getElementById('openPaymentModal')?.addEventListener('click',()=>modal.style.display='flex');
    document.getElementById('closeModalBtn')?.addEventListener('click',()=>modal.style.display='none');
    document.getElementById('mockPayBtn')?.addEventListener('click',()=>{ modal.style.display='none'; alert("✅ Pago exitoso"); sendWhatsApp("Acabo de pagar el Plan Élite"); });
    window.onclick = e=>{ if(e.target===modal) modal.style.display='none'; };
    
    // CHATBOT
    const chatbotWidget = document.getElementById('chatbotWidget');
    const chatMessages = document.getElementById('chatMessages');
    const chatInput = document.getElementById('chatInput');
    document.getElementById('chatbotFloatBtn')?.addEventListener('click',()=>chatbotWidget.classList.toggle('open'));
    document.getElementById('closeChatBtn')?.addEventListener('click',()=>chatbotWidget.classList.remove('open'));
    function addMessage(text,isUser){ const div=document.createElement('div'); div.className=`message ${isUser?'user':'bot'}`; div.innerHTML=text; chatMessages.appendChild(div); chatMessages.scrollTop=chatMessages.scrollHeight; }
    function sendChat(){ const msg=chatInput.value.trim(); if(!msg) return; addMessage(msg,true); chatInput.value=''; addMessage("✨ Un asesor te contactará pronto. Revisa nuestro material exclusivo al iniciar sesión. 🚀",false); }
    document.getElementById('sendChatBtn')?.addEventListener('click',sendChat);
    chatInput?.addEventListener('keypress',e=>{if(e.key==='Enter') sendChat();});
    
    updateUI();
</script>
</body>
</html>
