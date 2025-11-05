<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta property="og:title" content="NovaTrack - Soluciones de Seguridad Vehicular">
    <meta property="og:description" content="Seguridad y seguimiento para tu vehículo, siempre a tu lado. Servicios especializados de protección vehicular en Colombia.">
    <meta property="og:site_name" content="NovaTrack">
    <meta name="description" content="NovaTrack ofrece soluciones integrales de seguridad y tecnología electrónica para la protección vehicular en Colombia.">
    <title>NovaTrack - Soluciones de Seguridad Vehicular</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #0a1929;
            color: #e0e0e0;
            position: relative;
            overflow-x: hidden;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(218, 165, 32, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(30, 58, 138, 0.2) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
        }

        .content-wrapper {
            position: relative;
            z-index: 1;
        }

        .header {
            background: linear-gradient(135deg, #1e3a8a 0%, #0f172a 100%);
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 20px rgba(218, 165, 32, 0.2);
            border-bottom: 2px solid rgba(218, 165, 32, 0.3);
        }

        .logo {
            font-size: 32px;
            font-weight: bold;
            background: linear-gradient(135deg, #daa520, #ffd700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 20px rgba(218, 165, 32, 0.5);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav {
            display: flex;
            gap: 30px;
        }

        .nav a {
            color: #e0e0e0;
            text-decoration: none;
            font-size: 16px;
            transition: all 0.3s;
            padding: 10px 20px;
            border-radius: 8px;
            border: 1px solid transparent;
            font-weight: 500;
        }

        .nav a:hover {
            background: rgba(218, 165, 32, 0.1);
            border: 1px solid rgba(218, 165, 32, 0.5);
            color: #daa520;
            transform: translateY(-2px);
        }

        .hero {
            text-align: center;
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(218, 165, 32, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            z-index: -1;
        }

        .hero h1 {
            font-size: 56px;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #daa520, #ffd700, #daa520);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 30px rgba(218, 165, 32, 0.3);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 10px rgba(218, 165, 32, 0.3)); }
            to { filter: drop-shadow(0 0 20px rgba(218, 165, 32, 0.6)); }
        }

        .hero p {
            font-size: 22px;
            margin-bottom: 40px;
            color: #9ca3af;
            font-weight: 300;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 16px 45px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .btn:hover::before {
            width: 300px;
            height: 300px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #daa520, #b8860b);
            color: #0a1929;
            box-shadow: 0 4px 15px rgba(218, 165, 32, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(218, 165, 32, 0.6);
        }

        .btn-secondary {
            background: transparent;
            color: #daa520;
            border: 2px solid #daa520;
        }

        .btn-secondary:hover {
            background: rgba(218, 165, 32, 0.1);
            transform: translateY(-3px);
        }

        .section {
            max-width: 1200px;
            margin: 60px auto;
            padding: 50px 20px;
            background: linear-gradient(135deg, rgba(30, 58, 138, 0.2), rgba(15, 23, 42, 0.4));
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(218, 165, 32, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
        }

        .section h2 {
            font-size: 42px;
            margin-bottom: 40px;
            text-align: center;
            background: linear-gradient(135deg, #daa520, #ffd700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .info-card {
            background: linear-gradient(135deg, rgba(30, 58, 138, 0.3), rgba(15, 23, 42, 0.5));
            padding: 30px;
            border-radius: 15px;
            transition: all 0.3s;
            border: 1px solid rgba(218, 165, 32, 0.1);
            position: relative;
            overflow: hidden;
        }

        .info-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(218, 165, 32, 0.1), transparent);
            transition: left 0.5s;
        }

        .info-card:hover::before {
            left: 100%;
        }

        .info-card:hover {
            transform: translateY(-8px);
            border-color: rgba(218, 165, 32, 0.5);
            box-shadow: 0 10px 30px rgba(218, 165, 32, 0.2);
        }

        .info-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #daa520;
        }

        .info-card p {
            line-height: 1.8;
            color: #b0b0b0;
        }

        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .service-card {
            background: linear-gradient(135deg, rgba(30, 58, 138, 0.4), rgba(15, 23, 42, 0.6));
            padding: 35px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.4s;
            border: 1px solid rgba(218, 165, 32, 0.2);
            position: relative;
            overflow: hidden;
        }

        .service-card::after {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(218, 165, 32, 0.1) 0%, transparent 70%);
            transition: all 0.6s;
            opacity: 0;
        }

        .service-card:hover::after {
            opacity: 1;
            top: -100%;
            right: -100%;
        }

        .service-card:hover {
            transform: scale(1.05);
            border-color: rgba(218, 165, 32, 0.6);
            box-shadow: 0 15px 40px rgba(218, 165, 32, 0.3);
        }

        .service-icon {
            font-size: 56px;
            margin-bottom: 20px;
            filter: drop-shadow(0 0 10px rgba(218, 165, 32, 0.5));
        }

        .service-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #daa520;
        }

        .service-card p {
            color: #b0b0b0;
            margin: 8px 0;
        }

        .service-card strong {
            color: #ffd700;
            font-size: 22px;
        }

        .contact-info {
            background: linear-gradient(135deg, rgba(15, 23, 42, 0.6), rgba(30, 58, 138, 0.3));
            padding: 40px;
            border-radius: 15px;
            margin-top: 30px;
            border: 1px solid rgba(218, 165, 32, 0.2);
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 20px;
            margin: 25px 0;
            font-size: 18px;
            padding: 15px;
            background: rgba(30, 58, 138, 0.2);
            border-radius: 10px;
            border-left: 3px solid #daa520;
            transition: all 0.3s;
        }

        .contact-item:hover {
            background: rgba(30, 58, 138, 0.3);
            transform: translateX(10px);
        }

        .contact-item span {
            font-size: 28px;
            filter: drop-shadow(0 0 5px rgba(218, 165, 32, 0.5));
        }

        .social-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 40px;
        }

        .social-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, rgba(30, 58, 138, 0.5), rgba(15, 23, 42, 0.7));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            transition: all 0.3s;
            text-decoration: none;
            color: #e0e0e0;
            border: 2px solid rgba(218, 165, 32, 0.3);
        }

        .social-icon:hover {
            background: linear-gradient(135deg, #daa520, #b8860b);
            border-color: #daa520;
            transform: scale(1.15) rotate(5deg);
            box-shadow: 0 5px 20px rgba(218, 165, 32, 0.5);
        }

        .footer {
            text-align: center;
            padding: 40px;
            background: linear-gradient(135deg, #1e3a8a, #0f172a);
            margin-top: 60px;
            border-top: 2px solid rgba(218, 165, 32, 0.3);
        }

        .footer p {
            color: #9ca3af;
            margin: 10px 0;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 36px;
            }

            .nav {
                flex-direction: column;
                gap: 10px;
            }

            .header {
                flex-direction: column;
                gap: 20px;
                padding: 20px;
            }

            .section h2 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    <div class="content-wrapper">
        <header class="header">
            <div class="logo">
                <span>🔒</span>
                NOVATRACK
            </div>
            <nav class="nav">
                <a href="#inicio">Inicio</a>
                <a href="#servicios">Servicios</a>
                <a href="#informacion">Información</a>
                <a href="#contacto">Contacto</a>
            </nav>
        </header>

        <section id="inicio" class="hero">
            <h1>NovaTrack</h1>
            <p>Seguridad y seguimiento para tu vehículo, siempre a tu lado</p>
            <div class="cta-buttons">
                <a href="#servicios" class="btn btn-primary">Comprar ahora</a>
                <a href="#informacion" class="btn btn-secondary">Más información</a>
            </div>
        </section>

        <section id="informacion" class="section">
            <h2>Nuestra Empresa</h2>
            
            <div class="info-grid">
                <div class="info-card">
                    <h3>🎯 Misión</h3>
                    <p>Prestar servicios especializados para la protección y gestión de bienes y personas usando tecnología de punta, garantizando eficiencia, seguridad y satisfacción a sus clientes.</p>
                </div>

                <div class="info-card">
                    <h3>🔭 Visión</h3>
                    <p>Consolidarse para 2026 como líder en Colombia en soluciones integrales de seguridad y tecnología electrónica, que generen confianza y tranquilidad a clientes, empleados, proveedores y aliados.</p>
                </div>

                <div class="info-card">
                    <h3>⭐ Política de Calidad</h3>
                    <p>Mejora continua de procesos, satisfacción del cliente, rentabilidad y desarrollo humano.</p>
                </div>

                <div class="info-card">
                    <h3>🎓 Objetivos de Calidad</h3>
                    <p>Aumentar la eficacia operativa, garantizar la calidad del servicio e impulsar la participación del personal.</p>
                </div>
            </div>
        </section>

        <section id="servicios" class="section">
            <h2>Nuestros Servicios</h2>
            
            <div class="services">
                <div class="service-card">
                    <div class="service-icon">🛡️</div>
                    <h3>Security Package</h3>
                    <p>2 horas de servicio</p>
                    <p><strong>200,00 COP</strong></p>
                    <p>Avenida 4 Norte</p>
                    <button class="btn btn-primary" style="margin-top: 20px;">Reservar</button>
                </div>

                <div class="service-card">
                    <div class="service-icon">🔍</div>
                    <h3>Theft Recovery</h3>
                    <p>1h 30 min de servicio</p>
                    <p><strong>150,00 COP</strong></p>
                    <p>Avenida 4 Norte</p>
                    <button class="btn btn-primary" style="margin-top: 20px;">Reservar</button>
                </div>

                <div class="service-card">
                    <div class="service-icon">📍</div>
                    <h3>Rastreo GPS</h3>
                    <p>Monitoreo 24/7</p>
                    <p><strong>Desde 100,00 COP</strong></p>
                    <p>Servicio continuo</p>
                    <button class="btn btn-primary" style="margin-top: 20px;">Reservar</button>
                </div>
            </div>
        </section>

        <section id="contacto" class="section">
            <h2>Contacto</h2>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span>📞</span>
                    <div>
                        <strong style="color: #daa520;">Teléfono:</strong><br>
                        +573183354209
                    </div>
                </div>

                <div class="contact-item">
                    <span>📍</span>
                    <div>
                        <strong style="color: #daa520;">Ubicación:</strong><br>
                        Av. 4 Nte. # 9 NORTE-47 a 9, Granada, Cali
                    </div>
                </div>

                <div class="contact-item">
                    <span>🔖</span>
                    <div>
                        <strong style="color: #daa520;">Código de invitación:</strong><br>
                        OXOLET
                    </div>
                </div>

                <div style="text-align: center; margin-top: 30px;">
                    <button class="btn btn-primary">Enviar Mensaje</button>
                </div>
            </div>

            <div class="social-links">
                <a href="https://www.facebook.com" target="_blank" class="social-icon" title="Facebook">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                    </svg>
                </a>
                <a href="https://www.instagram.com" target="_blank" class="social-icon" title="Instagram">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                    </svg>
                </a>
            </div>
        </section>

        <footer class="footer">
            <p>&copy; 2025 NovaTrack. Todos los derechos reservados.</p>
            <p>Soluciones integrales de seguridad y tecnología electrónica en Colombia</p>
        </footer>
    </div>

    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
