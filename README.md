# libro_dinosaurio
libro datos dinosaurios
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dinoamigos - Landing Page del Libro</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;800&family=Nunito+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Paleta de colores cálida y vibrante con armonía análoga inspirada en la maqueta */
        :root {
            --bg-main: #1b2e24; /* Verde oscuro de fondo de tu maqueta */
            --accent-orange: #ff7a45; /* Naranja vibrante del botón de acción */
            --accent-yellow: #d1cc7b; /* Amarillo verdoso de los bloques principales */
            --btn-blue: #9cb1e6; /* Azul claro de los botones secundarios */
            --btn-purple: #9592b3; /* Lila de los botones secundarios */
            --btn-green: #a7bfa4; /* Verde suave de los botones secundarios */
            --text-light: #f4f7f5;
            --text-dark: #111111;
            --card-bg: rgba(255, 255, 255, 0.08);
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Nunito Sans', sans-serif;
            background-color: var(--bg-main);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, .font-inter {
            font-family: 'Inter', sans-serif;
            font-weight: 700;
        }

        /* Header / Navegación */
        header {
            background-color: rgba(27, 46, 36, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }

        .nav-table {
            width: 100%;
            border-collapse: collapse;
        }

        .nav-table td {
            vertical-align: middle;
        }

        .logo {
            font-size: 24px;
            color: var(--accent-yellow);
            text-decoration: none;
            font-weight: 800;
            letter-spacing: 1px;
        }

        .nav-links {
            text-align: right;
        }

        .nav-links a {
            color: var(--text-light);
            text-decoration: none;
            margin-left: 20px;
            font-weight: 600;
            font-size: 14px;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent-orange);
        }

        /* Hero Section (Replicando el esquema exacto de tu wireframe) */
        .hero {
            padding: 140px 20px 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero-table {
            width: 100%;
            border-collapse: collapse;
        }

        .hero-left {
            width: 45%;
            padding-right: 40px;
            vertical-align: top;
        }

        .hero-right {
            width: 55%;
            vertical-align: top;
            padding-left: 20px;
        }

        /* Contenedor Orgánico de la Imagen del Dinosaurio */
        .mockup-image-container {
            width: 100%;
            border-radius: 35px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
            border: 4px solid var(--accent-yellow);
            background: #2a4035;
        }

        .mockup-image-placeholder {
            width: 100%;
            height: 480px;
            background: linear-gradient(135deg, #426b53, #2a4035);
            display: block;
            position: relative;
        }

        .dino-badge {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 80px;
            opacity: 0.8;
        }

        /* Formas y Elementos Superiores de la Maqueta */
        .shapes-row {
            margin-bottom: 25px;
        }

        .circle-shape {
            display: inline-block;
            width: 60px;
            height: 60px;
            background-color: var(--btn-blue);
            border-radius: 50%;
            margin-right: 15px;
            opacity: 0.8;
            vertical-align: middle;
        }

        .double-circle {
            display: inline-block;
            width: 100px;
            height: 60px;
            background-color: var(--btn-blue);
            border-radius: 30px;
            margin-right: 15px;
            opacity: 0.8;
            vertical-align: middle;
        }

        .espacio-badge {
            display: inline-block;
            background-color: var(--accent-yellow);
            color: var(--text-dark);
            padding: 12px 35px;
            border-radius: 30px;
            font-size: 22px;
            font-weight: 700;
            letter-spacing: 2px;
            vertical-align: middle;
        }

        /* Título del Libro y Botón de Acción Naranja */
        .main-title-box {
            background-color: var(--accent-yellow);
            color: var(--text-dark);
            padding: 22px 40px;
            border-radius: 40px;
            font-size: 44px;
            font-weight: 800;
            display: inline-block;
            width: 78%;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            vertical-align: middle;
            text-transform: uppercase;
        }

        .action-circle-btn {
            display: inline-block;
            width: 75px;
            height: 75px;
            background-color: var(--accent-orange);
            border-radius: 50%;
            color: white;
            text-align: center;
            line-height: 75px;
            font-size: 32px;
            text-decoration: none;
            font-weight: bold;
            margin-left: 15px;
            box-shadow: 0 10px 25px rgba(255, 122, 69, 0.4);
            transition: transform 0.3s, background-color 0.3s;
            vertical-align: middle;
        }

        .action-circle-btn:hover {
            transform: scale(1.1);
            background-color: #ff9166;
        }

        /* Grid de Botones Inferiores Estilo Wireframe */
        .maqueta-grid {
            margin-top: 35px;
            width: 100%;
            border-collapse: separate;
            border-spacing: 15px;
        }

        .maqueta-grid td {
            width: 50%;
        }

        .grid-btn {
            display: block;
            padding: 16px 20px;
            border-radius: 25px;
            text-align: center;
            text-decoration: none;
            font-weight: 700;
            font-size: 16px;
            color: var(--text-dark);
            transition: opacity 0.3s, transform 0.2s;
        }

        .grid-btn:hover {
            transform: translateY(-2px);
            opacity: 0.9;
        }

        .btn-intro { background-color: var(--accent-yellow); }
        .btn-datos { background-color: var(--btn-blue); }
        .btn-prehistoria { background-color: var(--btn-green); }
        .btn-fosiles { background-color: var(--btn-purple); }
        .btn-nuevos { background-color: #7b91e6; color: white; }
        .btn-extincion { background-color: #8fa38c; }

        /* Secciones de Contenido */
        section {
            padding: 90px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 32px;
            color: var(--accent-yellow);
            margin-bottom: 40px;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-left: 5px solid var(--accent-orange);
            padding-left: 15px;
        }

        .content-table {
            width: 100%;
            border-collapse: collapse;
        }

        .content-table td {
            vertical-align: top;
            width: 50%;
        }

        .padding-right { padding-right: 40px; }
        .padding-left { padding-left: 40px; }

        .synopsis-text {
            font-size: 18px;
            color: #e0e8e3;
            margin-bottom: 25px;
        }

        .highlight-box {
            background-color: var(--card-bg);
            border-right: 4px solid var(--accent-orange);
            padding: 30px;
            border-radius: 20px;
        }

        .highlight-box h3 {
            color: var(--accent-yellow);
            margin-bottom: 15px;
        }

        /* Proceso Creativo */
        .process-step {
            margin-bottom: 25px;
            background: var(--card-bg);
            padding: 25px;
            border-radius: 20px;
            border-left: 4px solid var(--btn-blue);
        }

        .process-step h3 {
            color: var(--accent-yellow);
            margin-bottom: 10px;
            font-size: 20px;
        }

        /* Galería e Imágenes del Producto */
        .gallery-container {
            width: 100%;
        }
        
        .gallery-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 20px;
        }

        .gallery-cell {
            width: 33.33%;
            background: var(--card-bg);
            border-radius: 25px;
            padding: 15px;
            text-align: center;
            border: 2px dashed rgba(255,255,255,0.15);
        }

        .img-placeholder {
            width: 100%;
            height: 240px;
            background: #233b2e;
            border-radius: 18px;
            display: block;
            margin-bottom: 15px;
            position: relative;
        }

        .img-placeholder::after {
            content: "📸 Foto del Libro Real";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: rgba(255,255,255,0.35);
            font-size: 14px;
        }

        .img-placeholder.empaque::after {
            content: "📦 Prototipo de Empaque";
        }

        /* Footer y Redes Sociales de la Autora */
        footer {
            background-color: #111e17;
            padding: 70px 20px;
            text-align: center;
            border-top: 4px solid var(--accent-yellow);
        }

        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .author-name {
            font-size: 26px;
            color: var(--accent-yellow);
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .social-links {
            margin: 30px 0;
        }

        .social-btn {
            display: inline-block;
            background-color: var(--card-bg);
            color: var(--text-light);
            padding: 12px 30px;
            border-radius: 25px;
            text-decoration: none;
            margin: 0 10px;
            font-weight: 600;
            transition: background-color 0.3s, color 0.3s;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .social-btn:hover {
            background-color: var(--accent-orange);
            color: white;
            border-color: transparent;
        }

        .copyright {
            font-size: 14px;
            color: #6b8274;
            margin-top: 25px;
        }

        /* CONFIGURACIÓN RESPONSIVA MÓVIL (MEDIA QUERIES) */
        @media (max-width: 950px) {
            /* Transforma las celdas de las tablas en filas completas independientes */
            .hero-table, .hero-left, .hero-right,
            .content-table, .content-table td,
            .gallery-table, .gallery-cell {
                display: block;
                width: 100% !important;
                padding-left: 0 !important;
                padding-right: 0 !important;
            }

            .hero-right {
                margin-top: 40px;
            }

            .main-title-box {
                width: 78%;
                font-size: 34px;
                padding: 18px 25px;
            }

            .gallery-cell {
                margin-bottom: 25px;
            }

            .nav-links {
                text-align: center;
                margin-top: 15px;
            }
            
            .nav-links a {
                margin: 0 12px;
                display: inline-block;
            }
        }

        @media (max-width: 550px) {
            .maqueta-grid, .maqueta-grid td {
                display: block;
                width: 100%;
            }
            
            .maqueta-grid td {
                margin-bottom: -5px;
            }

            .main-title-box {
                width: 100%;
                display: block;
                text-align: center;
                margin-bottom: 15px;
            }

            .action-circle-btn {
                display: block;
                margin: 0 auto;
            }

            .shapes-row {
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="nav-container">
            <table class="nav-table">
                <tr>
                    <td>
                        <a href="#" class="logo">DINOAMIGOS</a>
                    </td>
                    <td class="nav-links">
                        <a href="#sinopsis">Sinopsis</a>
                        <a href="#proceso">Proceso</a>
                        <a href="#empaque">Empaque</a>
                        <a href="#galeria">Fotografías</a>
                    </td>
                </tr>
            </table>
        </div>
    </header>

    <section class="hero">
        <table class="hero-table">
            <tr>
                <td class="hero-left">
                    <div class="mockup-image-container">
                        <div class="mockup-image-placeholder">
                            <div class="dino-badge">🦖</div>
                        </div>
                    </div>
                </td>
                
                <td class="hero-right">
                    <div class="shapes-row">
                        <div class="double-circle"></div>
                        <div class="circle-shape"></div>
                        <div class="espacio-badge">ESPACIO</div>
                    </div>
                    
                    <div style="width: 100%;">
                        <div class="main-title-box">
                            Dinosauros
                        </div>
                        <a href="#sinopsis" class="action-circle-btn">&gt;</a>
                    </div>

                    <table class="maqueta-grid">
                        <tr>
                            <td><a href="#sinopsis" class="grid-btn btn-intro">Introducción</a></td>
                            <td><a href="#galeria" class="grid-btn btn-datos">Datos curiosos</a></td>
                        </tr>
                        <tr>
                            <td><a href="#proceso" class="grid-btn btn-prehistoria">Prehistoria</a></td>
                            <td><a href="#empaque" class="grid-btn btn-fosiles">Fósiles</a></td>
                        </tr>
                        <tr>
                            <td><a href="#proceso" class="grid-btn btn-nuevos">Nuevos descubrimientos</a></td>
                            <td><a href="#empaque" class="grid-btn btn-extincion">Extinción</a></td>
                        </tr>
                    </table>
                </td>
            </tr>
        </table>
    </section>

    <section id="sinopsis" style="background-color: rgba(0,0,0,0.15); border-radius: 35px; margin-bottom: 20px;">
        <h2 class="section-title">Sinopsis de "Dinoamigos"</h2>
        <table class="content-table">
            <tr>
                <td class="padding-right">
                    <p class="synopsis-text">
                        <strong>"Dinoamigos"</strong> es un viaje ilustrado que redefine la prehistoria para los lectores más jóvenes. A través de relatos llenos de calidez y un universo visual extraordinario, el libro explora la vida de entrañables dinosaurios en el descubrimiento de la empatía, la biodiversidad y el valor del entorno.
                    </p>
                    <p class="synopsis-text">
                        Una obra interactiva pensada para fomentar la curiosidad científica nativa a la vez que se consolida un espacio para la lectura lúdica en el hogar.
                    </p>
                </td>
                <td class="padding-left">
                    <div class="highlight-box">
                        <h3>¿Qué incluye la edición?</h3>
                        <p style="margin-bottom: 10px;">• Narrativas enfocadas en el desarrollo creativo y emocional.</p>
                        <p style="margin-bottom: 10px;">• Guías visuales de especies adaptadas de forma amigable.</p>
                        <p>• Apartados con los últimos descubrimientos paleontológicos.</p>
                    </div>
                </td>
            </tr>
        </table>
    </section>

    <section id="proceso">
        <h2 class="section-title">El Proceso Creativo</h2>
        <table class="content-table">
            <tr>
                <td class="padding-right">
                    <div class="process-step">
                        <h3>1. Conceptualización del Universo</h3>
                        <p>Planteamiento de personajes basados en la anatomía real de especies prehistóricas, simplificados mediante formas orgánicas y suaves amigables para niños.</p>
                    </div>
                    <div class="process-step">
                        <h3>2. Paleta de Color Análoga</h3>
                        <p>Selección exhaustiva de tonalidades cálidas y terrosas, garantizando un ambiente armónico y envolvente en cada página del libro.</p>
                    </div>
                </td>
                <td class="padding-left">
                    <div class="process-step" style="border-left-color: var(--accent-orange);">
                        <h3>3. Documentación Científica</h3>
                        <p>Integración de nuevos descubrimientos fósiles traducidos a un lenguaje visual claro, dinámico y lleno de datos de interés.</p>
                    </div>
                    <div class="process-step" style="border-left-color: var(--accent-orange);">
                        <h3>4. Pruebas de Lectura</h3>
                        <p>Validación directa del ritmo narrativo con pequeños lectores para pulir el impacto del clímax y los giros de la historia.</p>
                    </div>
                </td>
            </tr>
        </table>
    </section>

    <section id="empaque" style="background-color: rgba(0,0,0,0.15); border-radius: 35px; margin-bottom: 20px;">
        <h2 class="section-title">Diseño de Empaque & Concepto Fósil</h2>
        <table class="content-table">
            <tr>
                <td class="padding-right">
                    <p class="synopsis-text">
                        Cada ejemplar se entrega dentro de un empaque conceptual exclusivo. Inspirado en el proceso de excavación de fósiles, la experiencia de apertura invita al lector a convertirse en un auténtico explorador.
                    </p>
                    <div class="highlight-box" style="border-right-color: var(--btn-blue);">
                        <h3>Sostenibilidad:</h3>
                        <p>Fabricado con cartón reciclado prensado y tintas de origen orgánico que protegen el medio ambiente, alineándose a los valores del propio libro.</p>
                    </div>
                </td>
                <td class="padding-left">
                    <div class="img-placeholder empaque" style="height: 260px;"></div>
                </td>
            </tr>
        </table>
    </section>

    <section id="galeria">
        <h2 class="section-title">Fotografías del Producto</h2>
        <div class="gallery-container">
            <table class="gallery-table">
                <tr>
                    <td class="gallery-cell">
                        <div class="img-placeholder"></div>
                        <h4 style="color: var(--accent-yellow);">Portada en Relieve</h4>
                        <p style="font-size: 14px; opacity: 0.7; margin-top: 5px;">Detalle de los acabados texturizados de la tapa dura.</p>
                    </td>
                    <td class="gallery-cell">
                        <div class="img-placeholder"></div>
                        <h4 style="color: var(--accent-yellow);">Interiores</h4>
                        <p style="font-size: 14px; opacity: 0.7; margin-top: 5px;">Calidad cromática vibrante en papel mate texturizado.</p>
                    </td>
                    <td class="gallery-cell">
                        <div class="img-placeholder"></div>
                        <h4 style="color: var(--accent-yellow);">Set Coleccionable</h4>
                        <p style="font-size: 14px; opacity: 0.7; margin-top: 5px;">El libro junto al kit de postales prehistóricas.</p>
                    </td>
                </tr>
            </table>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <p class="author-name">Autora & Creativa</p>
            <p style="color: #a7bfa4; margin-bottom: 20px;">Sigue de cerca los próximos proyectos, lanzamientos y procesos de ilustración en canales oficiales.</p>
            
            <div class="social-links">
                <a href="#" class="social-btn">Instagram</a>
                <a href="#" class="social-btn">Behance</a>
                <a href="#" class="social-btn">LinkedIn</a>
            </div>
            
            <p class="copyright">&copy; 2026 Dinoamigos. Inspirado en el diseño estructural de la maqueta original.</p>
        </div>
    </footer>

</body>
</html>
