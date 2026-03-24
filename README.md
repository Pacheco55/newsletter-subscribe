
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Suscríbete al newsletter de PIXELBITS Studio y recibe notificaciones de nuevos proyectos en GitHub">
    <meta name="keywords" content="PIXELBITS, newsletter, GitHub, ESP32, IoT, desarrollo, software engineering">
    <meta name="author" content="PIXELBITS Studio - Julio César Pacheco Rojas">
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:title" content="🚀 Newsletter PIXELBITS - Proyectos GitHub">
    <meta property="og:description" content="Recibe notificaciones automáticas de nuevos proyectos">
    <meta property="og:image" content="https://via.placeholder.com/1200x630/000000/10b981?text=PIXELBITS+NEWSLETTER">
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:title" content="🚀 Newsletter PIXELBITS">
    <meta property="twitter:description" content="Recibe notificaciones de nuevos proyectos en GitHub">
    <title>🚀 Newsletter PIXELBITS - Suscripción</title>
    <!-- Fuentes -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            /* Paleta PIXELBITS: Verde Esmeralda, Negro, Blanco */
            --emerald-primary: #10b981;
            --emerald-light: #34d399;
            --emerald-dark: #059669;
            --emerald-glow: rgba(16, 185, 129, 0.5);
            --gold-accent: #fbbf24;
            --purple-accent: #a855f7;
            --black-bg: #000000;
            --black-surface: #0a0a0a;
            --black-card: #111111;
            --white-primary: #ffffff;
            --white-text: #f3f4f6;
            --gray-text: #9ca3af;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Rajdhani', sans-serif;
            background: var(--black-bg);
            color: var(--white-primary);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow-x: hidden;
            position: relative;
        }
        .tech-grid {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(16, 185, 129, 0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(16, 185, 129, 0.05) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridScroll 20s linear infinite;
            z-index: 0;
        }
        @keyframes gridScroll {
            0% { transform: translateY(0); }
            100% { transform: translateY(50px); }
        }
        .particles {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: 1;
            pointer-events: none;
        }
        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: var(--emerald-primary);
            border-radius: 50%;
            opacity: 0.7;
            animation: float 15s infinite;
            box-shadow: 0 0 8px var(--emerald-glow);
        }
        @keyframes float {
            0%, 100% { transform: translateY(0) translateX(0); opacity: 0.7; }
            25% { transform: translateY(-100px) translateX(50px); opacity: 1; }
            50% { transform: translateY(-200px) translateX(-30px); opacity: 0.5; }
            75% { transform: translateY(-100px) translateX(-50px); opacity: 1; }
        }
        .container {
            position: relative;
            z-index: 10;
            max-width: 600px;
            width: 90%;
            background: linear-gradient(135deg, var(--black-surface) 0%, var(--black-card) 100%);
            border-radius: 20px;
            padding: 50px 40px;
            box-shadow: 
                0 0 80px rgba(16, 185, 129, 0.4),
                inset 0 0 40px rgba(16, 185, 129, 0.03);
            border: 2px solid rgba(16, 185, 129, 0.4);
            backdrop-filter: blur(10px);
        }
        .container::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, 
                var(--emerald-primary), 
                var(--emerald-light), 
                var(--gold-accent),
                var(--purple-accent),
                var(--emerald-primary));
            border-radius: 20px;
            z-index: -1;
            opacity: 0.4;
            filter: blur(15px);
            background-size: 400% 400%;
            animation: glowPulse 4s ease-in-out infinite, gradientShift 8s ease infinite;
        }
        @keyframes glowPulse {
            0%, 100% { opacity: 0.4; }
            50% { opacity: 0.7; }
        }
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        .form-header {
            text-align: center;
            margin-bottom: 40px;
        }
        .logo-icon {
            font-size: 70px;
            margin-bottom: 15px;
            display: block;
            animation: iconFloat 3s ease-in-out infinite;
            filter: drop-shadow(0 0 20px var(--emerald-glow));
        }
        @keyframes iconFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 36px;
            font-weight: 900;
            background: linear-gradient(135deg, var(--emerald-light) 0%, var(--emerald-primary) 50%, var(--gold-accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 3px;
            animation: titleGlow 3s ease-in-out infinite;
        }
        @keyframes titleGlow {
            0%, 100% { filter: drop-shadow(0 0 10px var(--emerald-glow)); }
            50% { filter: drop-shadow(0 0 25px var(--emerald-glow)); }
        }
        .subtitle {
            font-size: 18px;
            color: var(--gray-text);
            font-weight: 300;
            line-height: 1.6;
        }
        .benefits {
            margin: 30px 0;
            padding: 25px;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.05) 0%, rgba(168, 85, 247, 0.05) 100%);
            border-left: 4px solid var(--emerald-primary);
            border-radius: 10px;
            box-shadow: inset 0 0 20px rgba(16, 185, 129, 0.1);
        }
        .benefit-item {
            display: flex;
            align-items: center;
            margin: 12px 0;
            font-size: 16px;
            color: var(--white-text);
            transition: all 0.3s ease;
        }
        .benefit-item:hover {
            transform: translateX(5px);
            color: var(--emerald-light);
        }
        .benefit-item::before {
            content: '▸';
            color: var(--emerald-primary);
            font-size: 24px;
            margin-right: 15px;
            font-weight: bold;
            text-shadow: 0 0 10px var(--emerald-glow);
        }
        .form-group {
            margin-bottom: 25px;
        }
        label {
            display: block;
            font-family: 'Orbitron', sans-serif;
            font-size: 14px;
            font-weight: 700;
            color: var(--emerald-light);
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-shadow: 0 0 10px var(--emerald-glow);
        }
        input[type="email"],
        input[type="text"] {
            width: 100%;
            padding: 18px 20px;
            font-size: 16px;
            font-family: 'Rajdhani', sans-serif;
            background: var(--black-card);
            border: 2px solid rgba(16, 185, 129, 0.3);
            border-radius: 12px;
            color: var(--white-primary);
            transition: all 0.3s ease;
            outline: none;
        }
        input[type="email"]:focus,
        input[type="text"]:focus {
            border-color: var(--emerald-primary);
            box-shadow: 
                0 0 25px var(--emerald-glow),
                inset 0 0 15px rgba(16, 185, 129, 0.1);
            transform: translateY(-2px);
            background: var(--black-surface);
        }
        input::placeholder {
            color: #4b5563;
        }
        .submit-btn {
            width: 100%;
            padding: 20px;
            font-family: 'Orbitron', sans-serif;
            font-size: 18px;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--black-bg);
            background: linear-gradient(135deg, var(--emerald-primary) 0%, var(--emerald-light) 50%, var(--gold-accent) 100%);
            border: none;
            border-radius: 12px;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            box-shadow: 
                0 8px 25px var(--emerald-glow),
                inset 0 0 20px rgba(255, 255, 255, 0.1);
        }
        .submit-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            transition: left 0.5s;
        }
        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 
                0 12px 40px var(--emerald-glow),
                inset 0 0 30px rgba(255, 255, 255, 0.2);
        }
        .submit-btn:hover::before {
            left: 100%;
        }
        .submit-btn:active {
            transform: translateY(-1px);
        }
        .submit-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }
        .success-message {
            display: none;
            padding: 20px;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.15) 0%, rgba(5, 150, 105, 0.15) 100%);
            border: 2px solid var(--emerald-primary);
            border-radius: 12px;
            text-align: center;
            margin-top: 25px;
            animation: slideIn 0.5s ease;
            box-shadow: 0 0 30px var(--emerald-glow);
        }
        .success-message.show {
            display: block;
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .success-icon {
            font-size: 50px;
            margin-bottom: 10px;
            animation: successPulse 1s ease-in-out infinite;
        }
        @keyframes successPulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        .success-text {
            font-size: 18px;
            font-weight: 700;
            color: var(--emerald-light);
            text-shadow: 0 0 10px var(--emerald-glow);
        }
        .success-detail {
            color: var(--gray-text);
            margin-top: 10px;
            font-size: 15px;
        }
        .form-footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 25px;
            border-top: 1px solid rgba(16, 185, 129, 0.2);
        }
        .footer-text {
            font-size: 13px;
            color: #6b7280;
            margin-bottom: 10px;
        }
        .footer-link {
            color: var(--emerald-primary);
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s;
            text-shadow: 0 0 5px var(--emerald-glow);
        }
        .footer-link:hover {
            color: var(--emerald-light);
            text-decoration: underline;
            text-shadow: 0 0 15px var(--emerald-glow);
        }
        @media (max-width: 768px) {
            .container {
                padding: 35px 25px;
            }
            h1 {
                font-size: 28px;
            }
            .subtitle {
                font-size: 16px;
            }
            .logo-icon {
                font-size: 50px;
            }
        }
        .deco-line {
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--emerald-primary), var(--gold-accent), var(--purple-accent), transparent);
            margin: 30px 0;
            position: relative;
            animation: lineShimmer 3s ease-in-out infinite;
        }
        @keyframes lineShimmer {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }
        .deco-line::before,
        .deco-line::after {
            content: '';
            position: absolute;
            width: 8px;
            height: 8px;
            background: var(--emerald-primary);
            border-radius: 50%;
            top: -2.5px;
            box-shadow: 0 0 15px var(--emerald-glow);
            animation: dotPulse 2s ease-in-out infinite;
        }
        @keyframes dotPulse {
            0%, 100% { box-shadow: 0 0 15px var(--emerald-glow); }
            50% { box-shadow: 0 0 25px var(--emerald-glow); }
        }
        .deco-line::before { left: 0; }
        .deco-line::after { right: 0; }
        .accent-gold {
            color: var(--gold-accent);
        }
        .accent-purple {
            color: var(--purple-accent);
        }
    </style>
</head>
<body>
    <div class="tech-grid"></div>
    <div class="particles" id="particles"></div>
    <div class="container">
        <div class="form-header">
            <span class="logo-icon">🚀</span>
            <h1>PIXELBITS<br>Newsletter</h1>
            <p class="subtitle">Recibe actualizaciones exclusivas de mis últimos proyectos en GitHub</p>
        </div>
        <div class="deco-line"></div>
        <div class="benefits">
            <div class="benefit-item">Notificaciones instantáneas de nuevos proyectos</div>
            <div class="benefit-item">Código fuente y documentación completa</div>
            <div class="benefit-item">Tecnologías emergentes <span class="accent-gold">(ESP32, IoT, Mobile Dev)</span></div>
            <div class="benefit-item">Proyectos de <span class="accent-purple">software engineering</span> innovadores</div>
        </div>
        <form id="subscription-form">
            <div class="form-group">
                <label for="email">📧 Email</label>
                <input type="email" id="email" name="email" placeholder="tu@email.com" required autocomplete="email">
            </div>
            <div class="form-group">
                <label for="name">👤 Nombre (opcional)</label>
                <input type="text" id="name" name="name" placeholder="Tu nombre" autocomplete="name">
            </div>
            <button type="submit" class="submit-btn" id="submit-btn">🚀 Activar Suscripción</button>
        </form>
        <div class="success-message" id="success-message">
            <div class="success-icon">✅</div>
            <div class="success-text">¡Bienvenido a PIXELBITS!</div>
            <p class="success-detail">Revisa tu email para confirmar tu suscripción</p>
        </div>
        <div class="form-footer">
            <p class="footer-text">Desarrollado por <a href="https://github.com/Pacheco55" class="footer-link" target="_blank">@Pacheco55</a></p>
            <p class="footer-text">Universidad Politécnica de Tecámac • Software Engineering</p>
        </div>
    </div>
    <script>
        const MAILERLITE_GROUP_ID = '182851929351653079';
        const FORM_ID = '182853995210999171';
        const particlesContainer = document.getElementById('particles');
        const colors = ['#10b981', '#34d399', '#fbbf24', '#a855f7'];
        for (let i = 0; i < 25; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 10 + 's';
            particle.style.animationDuration = (15 + Math.random() * 10) + 's';
            particle.style.background = colors[Math.floor(Math.random() * colors.length)];
            particlesContainer.appendChild(particle);
        }
        document.getElementById('subscription-form').addEventListener('submit', async function(e) {
            e.preventDefault();
            const submitBtn = document.getElementById('submit-btn');
            const email = document.getElementById('email').value;
            const name = document.getElementById('name').value;
            submitBtn.disabled = true;
            submitBtn.textContent = '⏳ Procesando...';
            try {
                const response = await fetch(`https://assets.mailerlite.com/jsonp/2218445/forms/${FORM_ID}/subscribe`, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/x-www-form-urlencoded',
                    },
                    body: new URLSearchParams({
                        'fields[email]': email,
                        'fields[name]': name || '',
                        'ml-submit': '1'
                    })
                });
                document.getElementById('success-message').classList.add('show');
                document.getElementById('subscription-form').reset();
                setTimeout(function() {
                    document.getElementById('success-message').classList.remove('show');
                    submitBtn.disabled = false;
                    submitBtn.textContent = '🚀 Activar Suscripción';
                }, 10000);
            } catch (error) {
                console.error('Error:', error);
                alert('Hubo un error al procesar tu suscripción. Por favor intenta de nuevo.');
                submitBtn.disabled = false;
                submitBtn.textContent = '🚀 Activar Suscripción';
            }
        });
    </script>
</body>
</html>
