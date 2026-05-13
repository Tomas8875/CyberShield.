# CyberShield.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CyberShield | Ciberseguridad Profesional</title>

    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            scroll-behavior:smooth;
        }

        body{
            font-family:'Montserrat',sans-serif;
            background:#ffffff;
            color:#111;
            overflow-x:hidden;
        }

        /* ===== ANIMACIONES FADE ===== */

        .fade{
            opacity:0;
            transform:translateY(40px);
            transition:all 1s ease;
        }

        .fade.show{
            opacity:1;
            transform:translateY(0);
        }

        /* ===== NAVBAR ===== */

        header{
            width:100%;
            padding:20px 8%;
            display:flex;
            justify-content:space-between;
            align-items:center;
            position:fixed;
            top:0;
            left:0;
            background:rgba(255,255,255,0.95);
            backdrop-filter:blur(10px);
            z-index:1000;
            border-bottom:1px solid #eee;
        }

        /* ===== LOGO ARRIBA IZQUIERDA ===== */

        .logo-container{
            display:flex;
            align-items:center;
            gap:12px;
        }

        .logo-container img{
            width:55px;
            height:55px;
            object-fit:contain;
        }

        .logo{
            font-size:28px;
            font-weight:700;
            background:linear-gradient(90deg,#00cfff,#7a3cff);
            -webkit-background-clip:text;
            -webkit-text-fill-color:transparent;
        }

        nav a{
            text-decoration:none;
            color:#222;
            margin-left:30px;
            font-weight:500;
            transition:0.3s;
        }

        nav a:hover{
            color:#7a3cff;
        }

        /* ===== HERO ===== */

        .hero{
            min-height:100vh;
            display:flex;
            align-items:center;
            justify-content:center;
            padding:120px 8%;
            position:relative;
            overflow:hidden;
        }

        .hero::before{
            content:'';
            position:absolute;
            width:700px;
            height:700px;
            background:radial-gradient(circle,#00cfff33,#7a3cff22,transparent);
            border-radius:50%;
            top:-200px;
            right:-200px;
        }

        .hero-content{
            max-width:700px;
            z-index:2;
        }

        .hero h1{
            font-size:64px;
            line-height:1.1;
            margin-bottom:25px;
        }

        .gradient{
            background:linear-gradient(90deg,#00cfff,#7a3cff);
            -webkit-background-clip:text;
            -webkit-text-fill-color:transparent;
        }

        .hero p{
            font-size:20px;
            color:#555;
            margin-bottom:40px;
            line-height:1.7;
        }

        /* ===== BOTONES CON GLOW ===== */

        .buttons{
            display:flex;
            gap:20px;
            flex-wrap:wrap;
        }

        .btn{
            padding:15px 30px;
            border:none;
            border-radius:50px;
            cursor:pointer;
            font-size:16px;
            font-weight:600;
            transition:0.4s;
        }

        .btn-primary{
            background:linear-gradient(90deg,#00cfff,#7a3cff);
            color:white;
            box-shadow:0 0 15px rgba(0,207,255,0.3);
        }

        .btn-primary:hover{
            transform:translateY(-3px);
            box-shadow:
                0 0 20px rgba(0,207,255,0.7),
                0 0 40px rgba(122,60,255,0.5);
        }

        .btn-secondary{
            background:white;
            border:2px solid #00cfff;
            color:#00cfff;
        }

        .btn-secondary:hover{
            background:#00cfff;
            color:white;
            box-shadow:0 0 20px rgba(0,207,255,0.5);
        }

        /* ===== STATS ===== */

        .stats{
            padding:80px 8%;
            display:grid;
            grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
            gap:30px;
            text-align:center;
        }

        .stat-card{
            padding:40px;
            border-radius:20px;
            background:white;
            box-shadow:0 5px 20px rgba(0,0,0,0.05);
            transition:0.4s;
        }

        /* ===== MOVIMIENTO SUAVE ===== */

        .stat-card:hover{
            transform:translateY(-8px);
        }

        .stat-card h2{
            font-size:42px;
            margin-bottom:10px;
            background:linear-gradient(90deg,#00cfff,#7a3cff);
            -webkit-background-clip:text;
            -webkit-text-fill-color:transparent;
        }

        /* ===== SERVICES ===== */

        .services{
            padding:100px 8%;
            background:#f8fbff;
        }

        .section-title{
            text-align:center;
            margin-bottom:70px;
        }

        .section-title h2{
            font-size:48px;
            margin-bottom:20px;
        }

        .section-title p{
            color:#666;
            font-size:18px;
        }

        .service-grid{
            display:grid;
            grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
            gap:30px;
        }

        .service-card{
            background:white;
            padding:35px;
            border-radius:25px;
            transition:0.4s;
            border:1px solid #eee;
        }

        /* ===== MOVIMIENTO SUAVE EN CARDS ===== */

        .service-card:hover{
            transform:translateY(-10px);
            box-shadow:0 15px 35px rgba(0,0,0,0.08);
        }

        .service-icon{
            font-size:42px;
            margin-bottom:20px;
        }

        .service-card h3{
            margin-bottom:15px;
            font-size:24px;
        }

        .service-card p{
            color:#666;
            line-height:1.7;
        }

        /* ===== CTA ===== */

        .cta{
            padding:120px 8%;
            text-align:center;
            background:linear-gradient(135deg,#00cfff,#7a3cff);
            color:white;
        }

        .cta h2{
            font-size:52px;
            margin-bottom:25px;
        }

        .cta p{
            font-size:20px;
            margin-bottom:35px;
        }

        /* ===== FOOTER ===== */

        footer{
            background:#111;
            color:white;
            padding:40px 8%;
            text-align:center;
        }

        footer p{
            color:#aaa;
        }

        /* ===== MOBILE ===== */

        @media(max-width:768px){

            .hero h1{
                font-size:46px;
            }

            nav{
                display:none;
            }

            .cta h2{
                font-size:38px;
            }

            .section-title h2{
                font-size:38px;
            }

        }

    </style>
</head>

<body>

    <!-- NAVBAR -->

    <header>

        <!-- LOGO AÑADIDO -->

        <div class="logo-container">

            <!-- CAMBIA "logo.png" POR TU LOGO -->
            <img src="logo.png" alt="CyberShield Logo">

            <div class="logo">
                CyberShield
            </div>

        </div>

        <nav>
            <a href="#inicio">Inicio</a>
            <a href="#servicios">Servicios</a>
            <a href="#contacto">Contacto</a>
        </nav>

    </header>

    <!-- HERO -->

    <section class="hero fade" id="inicio">

        <div class="hero-content">

            <h1>
                Protegemos tu mundo <span class="gradient">digital</span>
            </h1>

            <p>
                Soluciones avanzadas de ciberseguridad para empresas,
                profesionales y organizaciones modernas.
            </p>

            <div class="buttons">

                <button class="btn btn-primary">
                    Solicitar Auditoría
                </button>

                <button class="btn btn-secondary">
                    Ver Servicios
                </button>

            </div>

        </div>

    </section>

    <!-- STATS -->

    <section class="stats fade">

        <div class="stat-card">
            <h2>24/7</h2>
            <p>Monitorización continua</p>
        </div>

        <div class="stat-card">
            <h2>100%</h2>
            <p>Compromiso y confidencialidad</p>
        </div>

        <div class="stat-card">
            <h2>+50</h2>
            <p>Sistemas analizados</p>
        </div>

    </section>

    <!-- SERVICES -->

    <section class="services fade" id="servicios">

        <div class="section-title">

            <h2>
                Nuestros Servicios
            </h2>

            <p>
                Seguridad avanzada adaptada a las amenazas actuales.
            </p>

        </div>

        <div class="service-grid">

            <div class="service-card">
                <div class="service-icon">🛡️</div>
                <h3>Auditoría</h3>
                <p>
                    Detectamos vulnerabilidades críticas antes que los atacantes.
                </p>
            </div>

            <div class="service-card">
                <div class="service-icon">💻</div>
                <h3>Pentesting</h3>
                <p>
                    Simulación de ataques reales para fortalecer tus sistemas.
                </p>
            </div>

            <div class="service-card">
                <div class="service-icon">🔒</div>
                <h3>Monitorización</h3>
                <p>
                    Protección activa y vigilancia continua de tu infraestructura.
                </p>
            </div>

            <div class="service-card">
                <div class="service-icon">📊</div>
                <h3>Consultoría</h3>
                <p>
                    Estrategias de ciberseguridad adaptadas a cada empresa.
                </p>
            </div>

            <div class="service-card">
                <div class="service-icon">🎓</div>
                <h3>Formación</h3>
                <p>
                    Capacitación contra phishing, malware y amenazas digitales.
                </p>
            </div>

            <div class="service-card">
                <div class="service-icon">⚡</div>
                <h3>Respuesta a Incidentes</h3>
                <p>
                    Actuación rápida ante ataques o brechas de seguridad.
                </p>
            </div>

        </div>

    </section>

    <!-- CTA -->

    <section class="cta fade" id="contacto">

        <h2>
            ¿Tu empresa está realmente protegida?
        </h2>

        <p>
            Solicita una evaluación gratuita de seguridad.
        </p>

        <button class="btn btn-secondary">
            Contactar Ahora
        </button>

    </section>

    <!-- FOOTER -->

    <footer>

        <h2 class="logo">
            CyberShield
        </h2>

        <br>

        <p>
            © 2026 CyberShield — Todos los derechos reservados
        </p>

    </footer>

    <!-- SCRIPT FADE IN -->

    <script>

        const fades = document.querySelectorAll('.fade');

        const observer = new IntersectionObserver(entries => {

            entries.forEach(entry => {

                if(entry.isIntersecting){
                    entry.target.classList.add('show');
                }

            });

        });

        fades.forEach(fade => {
            observer.observe(fade);
        });

    </script>

</body>
</html>
