<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MultiÁrea Digital 2.0</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(180deg, #0a0a1a 0%, #0d0d2b 100%);
            color: #fff;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            overflow-x: hidden;
        }
        .main-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px 20px;
            max-width: 900px;
            width: 100%;
            margin: auto;
            justify-content: center;
        }
        .header-main {
            width: 100%;
            background: linear-gradient(90deg, #2a5298, #1e3c72);
            color: #fff;
            padding: 20px;
            border-radius: 15px;
            margin-bottom: 20px;
            box-shadow: 0 4px 15px rgba(30, 60, 114, 0.4);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .header-main h1 {
            font-size: 2rem;
            margin: 0;
            font-weight: 700;
        }
        .header-main p {
            font-size: 1rem;
            margin: 5px 0 0;
            color: #b0b0b0;
        }

            /* Sidebar layout */
            .app-layout {
                display: flex;
                gap: 20px;
                align-items: flex-start;
                width: 100%;
                max-width: 1200px;
                margin: 0 auto;
                padding: 20px;
            }

            .sidebar {
                width: 220px;
                background: linear-gradient(180deg,#0f1724,#0b2540);
                border-radius: 12px;
                padding: 16px;
                box-shadow: 0 6px 18px rgba(0,0,0,0.4);
                display: flex;
                flex-direction: column;
                gap: 10px;
            }

            .side-button {
                background: transparent;
                color: #dbeafe;
                border: 1px solid rgba(255,255,255,0.04);
                padding: 10px 12px;
                border-radius: 8px;
                text-align: left;
                cursor: pointer;
                font-weight: 600;
            }

            .side-button:hover { background: rgba(255,255,255,0.02); }

            .side-button.selected {
                outline: 2px solid rgba(30,144,255,0.9);
                background: linear-gradient(90deg,#0b3b61,#123a6a);
                color: #fff;
                transform: translateY(-1px);
            }

            .admin-btn { color: #ffd6d6; border-color: rgba(255,100,100,0.12); }

            /* Ajuste para área principal dentro del layout */
            .main-container {
                flex: 1;
                max-width: none;
                width: auto;
                margin: 0;
                padding: 0 10px;
            }

            @media (max-width: 900px) {
                .app-layout { flex-direction: column; padding: 12px; }
                .sidebar { width: 100%; flex-direction: row; justify-content: center; }
                .side-button { flex: 1; }
            }
        .tab-menu {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 20px;
            width: 100%;
            flex-wrap: wrap;
        }
        .tab-button {
            background-color: #333;
            color: #fff;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s;
            font-size: 1rem;
            font-weight: 600;
        }
        .tab-button:hover {
            background-color: #555;
            transform: translateY(-2px);
        }
        .tab-button.active {
            background-color: #1e90ff;
            box-shadow: 0 4px 10px rgba(30, 144, 255, 0.5);
        }
        /* Estilos para secciones de contenido */
        .content-section {
            display: none;
            padding: 20px;
            max-width: 900px;
            margin: 20px auto;
            text-align: left;
            width: 100%;
        }
        .content-section.active {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .content-section h1,
        .content-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #f0f0f0;
            text-align: center;
        }
        .authors {
            font-size: 1rem;
            margin-top: 10px;
            color: rgba(255, 255, 255, 0.8);
            text-align: center;
            margin-bottom: 30px;
        }
        #result, #geoResult, #mathResult, #langResult, #physResult, #quizResult {
            margin-top: 25px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            text-align: left;
            width: 100%;
        }
        .animal-info {
            font-weight: bold;
            background: rgba(255, 255, 255, 0.8);
            padding: 4px 8px;
            border-radius: 4px;
            display: inline-block;
            color: #000;
        }
        .animal-image {
            max-width: 100%;
            max-height: 300px;
            margin-top: 10px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .info-card {
            background: rgba(255, 255, 255, 0.15);
            padding: 12px;
            border-radius: 8px;
            margin: 8px 0;
        }
        .info-title {
            font-weight: bold;
            margin-bottom: 5px;
            color: #fff;
            font-size: 1rem;
        }
        .taxonomy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 8px;
            margin-top: 8px;
        }
        .taxonomy-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 6px;
            border-radius: 4px;
            font-size: 0.85rem;
            text-align: center;
        }
        .search-container {
            margin: 20px auto;
            max-width: 500px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            width: 100%;
        }
        .search-input {
            padding: 12px 20px;
            width: 100%;
            border-radius: 25px;
            border: none;
            font-size: 1rem;
            outline: none;
            background: rgba(255, 255, 255, 0.9);
            color: #333;
        }
        .search-button {
            padding: 12px 25px;
            background: #FF9800;
            color: white;
            border-radius: 25px;
            cursor: pointer;
            border: none;
            transition: all 0.3s;
        }
        .search-button:hover {
            background: #F57C00;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .search-results {
            margin-top: 15px;
            text-align: left;
            width: 100%;
            max-width: 500px;
        }
        .search-item {
            padding: 10px 15px;
            margin: 5px 0;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s;
        }
        .search-item:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        /* Estilos para el explorador espacial */
        .space-header {
            padding: 30px 20px;
            background: rgba(18, 18, 51, 0.8);
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 0 25px rgba(0, 243, 255, 0.4);
            border: 1px solid #00f3ff;
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
            width: 100%;
            max-width: 800px;
        }
        .space-header h2 {
            color: #00f3ff;
            text-shadow: 0 0 10px #00f3ff, 0 0 20px #00f3ff;
            margin-bottom: 10px;
            font-size: 2.5rem;
            letter-spacing: 2px;
        }
        .space-subtitle {
            color: #00f3ff;
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        .planetas-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 40px;
            width: 100%;
            max-width: 1000px;
            margin: 0 auto;
        }
        .planeta-btn {
            padding: 20px 15px;
            border: none;
            background: linear-gradient(145deg, rgba(18, 18, 51, 0.8), rgba(10, 10, 35, 0.8));
            color: white;
            border-radius: 15px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 6px 12px rgba(0, 191, 255, 0.4);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 130px;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(0, 243, 255, 0.3);
        }
        .planeta-btn:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 12px 20px rgba(0, 191, 255, 0.6);
        }
        .planet-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 12px;
            font-size: 30px;
            background: rgba(0, 0, 0, 0.2);
            box-shadow: 0 0 15px currentColor;
            transition: all 0.3s;
        }
        .planeta-btn:hover .planet-icon {
            transform: scale(1.2) rotate(10deg);
        }
        .space-info {
            margin-top: 40px;
            background: linear-gradient(to right, rgba(13, 27, 42, 0.9), rgba(27, 38, 53, 0.9));
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 0 25px #00f3ff;
            text-align: left;
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 255, 255, 0.3);
        }
        .space-info h3 {
            color: #00f3ff;
            border-bottom: 2px solid #00f3ff;
            padding-bottom: 15px;
            margin-top: 0;
            text-align: center;
            font-size: 2rem;
            margin-bottom: 25px;
        }
        .space-datos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 25px;
        }
        .space-dato {
            background-color: rgba(0, 191, 255, 0.15);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid #00f3ff;
            transition: all 0.3s;
            backdrop-filter: blur(5px);
        }
        .space-dato:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 191, 255, 0.3);
        }
        .space-dato h4 {
            margin-top: 0;
            color: #00f3ff;
            font-size: 1.25rem;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .animal-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .animal-detail-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 15px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: left;
        }
        .animal-detail-card h4 {
            color: #ffc837;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            padding-bottom: 8px;
            margin-top: 0;
        }
        /* Estilos para quizzes */
        .quiz-container {
            max-width: 600px;
            margin: auto;
        }
        .quiz-question {
            margin-bottom: 20px;
        }
        .quiz-option {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px;
            margin: 5px 0;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .quiz-option:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        .quiz-result {
            margin-top: 20px;
            font-weight: bold;
        }
        /* Estilos para el juego de matemáticas */
        #matematicas {
            background: rgba(255,255,255,0.05);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.4);
        }
        #matematicas h2 {
            color: #1e90ff;
            margin-bottom: 25px;
            font-size: 2rem;
        }
        #pregunta {
            font-size: 3.5rem;
            font-weight: 700;
            margin: 40px 0;
            color: #fff;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }
        .opciones {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            max-width: 700px;
            margin: 0 auto 40px;
        }
        .boton {
            background: linear-gradient(145deg, #2a5298, #1e3c72);
            color: white;
            border: none;
            padding: 30px;
            font-size: 2rem;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 6px 15px rgba(0,0,0,0.4);
        }
        .boton:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(30,144,255,0.5);
        }
        .boton.correcto {
            background: linear-gradient(145deg, #28a745, #1e8c3a) !important;
            animation: pulso 0.6s;
        }
        .boton.incorrecto {
            background: linear-gradient(145deg, #dc3545, #a71d2a) !important;
            animation: shake 0.5s;
        }
        @keyframes pulso {
            0% { transform: scale(1); }
            50% { transform: scale(1.08); }
            100% { transform: scale(1); }
        }
        @keyframes shake {
            0%,100% { transform: translateX(0); }
            25% { transform: translateX(-12px); }
            75% { transform: translateX(12px); }
        }
        #resultado {
            font-size: 2rem;
            margin: 30px 0;
            min-height: 60px;
            font-weight: bold;
        }
        #puntuacion, #record {
            font-size: 1.6rem;
            margin: 15px 0;
        }
        #progreso {
            height: 25px;
            background: rgba(255,255,255,0.1);
            border-radius: 12px;
            overflow: hidden;
            margin: 25px 0;
        }
        #barra {
            height: 100%;
            width: 0%;
            background: #1e90ff;
            transition: width 0.5s ease;
        }
        .nueva-pregunta-btn {
            padding: 18px 50px;
            background: #ff9800;
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.4rem;
            cursor: pointer;
            margin-top: 30px;
            transition: all 0.3s;
        }
        .nueva-pregunta-btn:hover {
            background: #f57c00;
            transform: translateY(-3px);
        }
        /* Buscador de fórmulas */
        .buscador {
            text-align: center;
            margin: 40px 0;
        }
        .buscador input {
            padding: 16px 16px 16px 50px;
            width: 80%;
            max-width: 600px;
            font-size: 1.2rem;
            border: 3px solid #1e90ff;
            border-radius: 50px;
            background: rgba(255,255,255,0.95);
            color: #333;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="%231e90ff" stroke-width="3"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>');
            background-size: 28px;
            background-position: 15px center;
            background-repeat: no-repeat;
        }
        .formula {
            background: rgba(255,255,255,0.1);
            padding: 25px;
            margin: 20px 0;
            border-radius: 15px;
            font-size: 1.4rem;
            text-align: center;
            border: 1px solid rgba(30,144,255,0.3);
            transition: all 0.3s;
        }
        .formula.oculta {
            display: none;
        }
        .formula strong {
            color: #1e90ff;
            font-size: 1.6rem;
        }
        .formula small {
            color: #b0b0b0;
            display: block;
            margin-top: 10px;
        }
        /* Estilos responsivos */
        @media (max-width: 768px) {
            .header-main h1 {
                font-size: 2rem;
            }
            .tab-menu {
                flex-direction: column;
            }
            .tab-button {
                width: 100%;
            }
            .content-section h1,
            .space-header h2 {
                font-size: 2rem;
            }
            .planetas-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .space-datos {
                grid-template-columns: 1fr;
            }
            .animal-details {
                grid-template-columns: 1fr;
            }
            .opciones {
                grid-template-columns: 1fr;
            }
            #pregunta {
                font-size: 2.8rem;
            }
            .boton {
                padding: 25px;
                font-size: 1.8rem;
            }
        }
        @media (max-width: 480px) {
            .planetas-grid {
                grid-template-columns: 1fr;
            }
            .search-container {
                flex-direction: column;
            }
            #animalSearch, #geoSearch, #mathSearch, #langSearch, #physSearch {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="app-layout">
        <aside class="sidebar">
            <button class="side-button" onclick="showSection('animales')">Contenido</button>
            <button class="side-button admin-btn" onclick="enterAdmin()">Admin</button>
        </aside>
        <div class="main-container">
        <div class="header-main">
            <h1>MultiÁrea Digital</h1>
            <p>Explora, descubre y aprende con nuestras herramientas</p>
        </div>
        <div class="tab-menu">
            <button class="tab-button active" onclick="showSection('animales')">Identificador de Animales</button>
            <button class="tab-button" onclick="showSection('geografia')">Geografía</button>
            <button class="tab-button" onclick="showSection('espacio')">Explorador del Sistema Solar</button>
            <button class="tab-button" onclick="showSection('matematicas')">Matemáticas</button>
            <button class="tab-button" onclick="showSection('lengua')">Lengua y Literatura</button>
            <button class="tab-button" onclick="showSection('fisica')">Física</button>
            <button class="tab-button" onclick="showSection('quizzes')">Quizzes Interactivos</button>
        </div>
        <div id="animales" class="content-section active">
            <h1>Identificador de Animales</h1>
            <div class="authors">Por Rodrigo Mesis, Carlos Mendoza y Ariel Flores</div>
            <div class="search-container">
                <input type="text" class="search-input" id="animalSearch" placeholder="Buscar animal por nombre...">
                <button class="search-button" id="searchButton">Buscar</button>
            </div>
            <div id="searchResults" class="search-results"></div>
            <div id="result"></div>
        </div>
        <div id="geografia" class="content-section">
            <h1>Identificador de Geografía</h1>
            <div class="authors">Por Rodrigo Mesis, Carlos Mendoza y Ariel Flores</div>
            <div class="search-container">
                <input type="text" class="search-input" id="geoSearch" placeholder="Buscar país, capital o lugar...">
                <button class="search-button" id="geoSearchButton">Buscar</button>
            </div>
            <div id="geoResults" class="search-results"></div>
            <div id="geoResult"></div>
        </div>
        <div id="espacio" class="content-section">
            <div class="space-header">
                <h2>Explorador del Sistema Solar</h2>
                <p class="space-subtitle">DESCUBRE LOS PLANETAS DE NUESTRO SISTEMA SOLAR</p>
                <p>Creado por <strong>Carlos Mendoza</strong> y <strong>Rodrigo Mesis</strong></p>
            </div>
            <div class="planetas-grid">
                <button class="planeta-btn" onclick="mostrarInfoPlaneta('tierra')">
                    <div class="planet-icon" style="color: #2f6aae;"><i class="fas fa-globe-americas"></i></div>
                    <div class="planeta-nombre">Tierra</div>
                </button>
                <button class="planeta-btn" onclick="mostrarInfoPlaneta('marte')">
                    <div class="planet-icon" style="color: #c1440e;"><i class="fas fa-mountain"></i></div>
                    <div class="planeta-nombre">Marte</div>
                </button>
                <button class="planeta-btn" onclick="mostrarInfoPlaneta('jupiter')">
                    <div class="planet-icon" style="color: #d8ca9d;"><i class="fas fa-wind"></i></div>
                    <div class="planeta-nombre">Júpiter</div>
                </button>
            </div>
            <div id="info-planeta" class="space-info">
                <h3>Bienvenido al Explorador del Sistema Solar</h3>
                <p class="descripcion">Selecciona un planeta para conocer información detallada sobre él, incluyendo su tamaño, composición, características únicas y datos curiosos.</p>
            </div>
        </div>
        <div id="matematicas" class="content-section">
            <h1>Matemáticas</h1>
            <div class="authors">Por Rodrigo Mesis, Carlos Mendoza y Ariel Flores</div>
            <div id="juego-matematicas">
                <h2>¡Práctica Divertida!</h2>
                <div id="puntuacion">Puntuación: 0</div>
                <div id="record">Récord: 0</div>
                <div id="progreso"><div id="barra"></div></div>

                <div id="pregunta">¿Preparado?</div>

                <div class="opciones">
                    <button class="boton"></button>
                    <button class="boton"></button>
                    <button class="boton"></button>
                    <button class="boton"></button>
                </div>

                <div id="resultado"></div>

                <button class="nueva-pregunta-btn" onclick="nuevaPregunta()">¡Nueva pregunta!</button>
            </div>

            <!-- Buscador de fórmulas -->
            <div class="buscador">
                <input type="text" id="buscarFormula" placeholder="🔍 Busca una fórmula (pitágoras, círculo, cuadrática...)">
            </div>

            <div class="formula" data-nombre="pitagoras teorema triangulo">
                <strong>Teorema de Pitágoras</strong><br>
                a² + b² = c²<br>
                <small>(En triángulos rectángulos)</small>
            </div>
            <div class="formula" data-nombre="cuadratica ecuacion">
                <strong>Fórmula cuadrática</strong><br>
                x = [-b ± √(b² - 4ac)] / (2a)<br>
                <small>(Para ax² + bx + c = 0)</small>
            </div>
            <div class="formula" data-nombre="circulo area perimetro">
                <strong>Área del círculo</strong><br>
                A = π r²<br>
                <strong>Circunferencia</strong><br>
                C = 2 π r
            </div>
            <div class="formula" data-nombre="aureo phi golden">
                <strong>Número áureo</strong><br>
                φ = (1 + √5)/2 ≈ 1.618<br>
                <small>Proporción perfecta en arte y naturaleza</small>
            </div>
            <div class="formula" data-nombre="rectangulo area perimetro">
                <strong>Rectángulo</strong><br>
                Área = largo × ancho<br>
                Perímetro = 2(largo + ancho)
            </div>
            <div class="formula" data-nombre="pendiente recta">
                <strong>Pendiente de una recta</strong><br>
                m = (y₂ - y₁)/(x₂ - x₁)
            </div>
            <div class="formula" data-nombre="distancia puntos">
                <strong>Distancia entre dos puntos</strong><br>
                d = √[(x₂ - x₁)² + (y₂ - y₁)²]
            </div>
        </div>
        <div id="lengua" class="content-section">
            <h1>Lengua y Literatura</h1>
            <div class="authors">Por Rodrigo Mesis, Carlos Mendoza y Ariel Flores</div>
            <div class="search-container">
                <input type="text" class="search-input" id="langSearch" placeholder="Buscar autor o obra...">
                <button class="search-button" id="langSearchButton">Buscar</button>
            </div>
            <div id="langResults" class="search-results"></div>
            <div id="langResult"></div>
        </div>
        <div id="fisica" class="content-section">
            <h1>Física (Tabla Periódica Simplificada)</h1>
            <div class="authors">Por Rodrigo Mesis, Carlos Mendoza y Ariel Flores</div>
            <div class="search-container">
                <input type="text" class="search-input" id="physSearch" placeholder="Buscar elemento químico...">
                <button class="search-button" id="physSearchButton">Buscar</button>
            </div>
            <div id="physResults" class="search-results"></div>
            <div id="physResult"></div>
        </div>
        <div id="quizzes" class="content-section">
            <h1>Quizzes Interactivos</h1>
            <div class="register" style="margin-bottom:12px;">
                <h3>Registro de Estudiante (opcional)</h3>
                <input id="regNombre" type="text" placeholder="Nombre y apellidos" style="width:60%;padding:6px;margin:4px 0;">
                <input id="regEdad" type="number" placeholder="Edad" style="width:20%;padding:6px;margin:4px 8px 4px 0;">
                <input id="regGrado" type="text" placeholder="Grado" style="width:15%;padding:6px;margin:4px 0;">
                <div style="margin-top:6px;">
                    <button class="tab-button" onclick="registerUser()">Registrar</button>
                    <button class="tab-button" onclick="clearRegistration()">Cerrar sesión</button>
                </div>
                <div id="regStatus" style="margin-top:8px;color:#0a0;"></div>
            </div>
            <div class="tab-menu" style="margin-bottom: 20px;">
                <button class="tab-button active" onclick="showQuiz('animales')">Animales</button>
                <button class="tab-button" onclick="showQuiz('geografia')">Geografía</button>
                <button class="tab-button" onclick="showQuiz('espacio')">Espacio</button>
                <button class="tab-button" onclick="showQuiz('matematicas')">Matemáticas</button>
                <button class="tab-button" onclick="showQuiz('lengua')">Lengua</button>
                <button class="tab-button" onclick="showQuiz('fisica')">Física</button>
            </div>
            <div id="quizResult"></div>
        </div>
        <div id="admin" class="content-section">
            <h1>Panel Admin</h1>
            <div class="authors">Área administrativa</div>
            <div class="info-card" style="margin-top:16px;">
                <h3>Acceso administrador</h3>
                <p>Acceso concedido. Aquí puedes agregar funciones administrativas.</p>
                <button class="tab-button" onclick="showSection('animales')">Volver</button>
            </div>
            <div style="margin-top:16px;">
                <h3>Usuarios registrados</h3>
                <div id="adminUsers" style="max-height:200px;overflow:auto;padding:8px;background:#fff;border-radius:6px;margin-bottom:12px;"></div>
                <h3>Resultados de Quizzes</h3>
                <div id="adminSubmissions" style="max-height:300px;overflow:auto;padding:8px;background:#fff;border-radius:6px;"></div>
            </div>
        </div>
    </div>
    <script>
        const sections = ['animales', 'geografia', 'espacio', 'matematicas', 'lengua', 'fisica', 'quizzes', 'admin'];
        const tabButtons = document.querySelectorAll('.tab-menu .tab-button');
        const sidebarButtons = document.querySelectorAll('.sidebar .side-button');
        const adminPassword = '0401090';
        // Registro y envíos a Admin
        const REG_USER_KEY = 'registeredUser';
        const REG_USERS_LIST_KEY = 'registeredUsers';
        const QUIZ_SUBMISSIONS_KEY = 'quizSubmissions';

        function showSection(sectionId) {
            sections.forEach(id => {
                const section = document.getElementById(id);
                if (section) section.classList.remove('active');
            });
            tabButtons.forEach(button => {
                button.classList.remove('active');
                if (button.getAttribute('onclick') && button.getAttribute('onclick').includes(sectionId)) button.classList.add('active');
            });
            // sidebar selection: mark 'Contenido' for non-admin, 'Admin' for admin
            sidebarButtons.forEach(b => b.classList.remove('selected'));
            if (sectionId === 'admin') {
                const adminBtn = document.querySelector('.sidebar .admin-btn');
                if (adminBtn) adminBtn.classList.add('selected');
            } else {
                const contentBtn = document.querySelector('.sidebar .side-button');
                if (contentBtn) contentBtn.classList.add('selected');
            }

            const targetSection = document.getElementById(sectionId);
            if (targetSection) targetSection.classList.add('active');
            window.scrollTo(0, 0);
        }

        function enterAdmin() {
            const pw = prompt('Ingrese contraseña de administrador:');
            if (pw === adminPassword) {
                showSection('admin');
                // refrescar datos mostrados en el panel admin al entrar
                if (typeof renderAdminPanel === 'function') renderAdminPanel();
            } else if (pw !== null) {
                alert('Contraseña incorrecta.');
            }
        }

        document.addEventListener('DOMContentLoaded', () => showSection('animales'));
        // Base de datos reducida
        const animalDatabase = {
            "perro": {
                nombre: "Perro (Canis lupus familiaris)",
                tipo: "Mamífero doméstico",
                info: "El perro es un mamífero carnívoro de la familia de los cánidos. Es una subespecie del lobo.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Global (domesticado)",
                caracteristicas: "Excelente olfato, social.",
                curiosidades: "Pueden entender hasta 250 palabras.",
                esperanza_vida: "10-13 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No en peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Canidae",
                    genero: "Canis",
                    especie: "C. lupus familiaris"
                }
            },
            "gato": {
                nombre: "Gato (Felis catus)",
                tipo: "Mamífero doméstico",
                info: "El gato es un mamífero carnívoro de la familia Felidae.",
                alimentacion: "Carnívoro estricto",
                clasificacion: "Mamífero",
                habitat: "Global (domesticado)",
                caracteristicas: "Excelente visión nocturna.",
                curiosidades: "Pasan 2/3 del día durmiendo.",
                esperanza_vida: "12-15 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No en peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Felis",
                    especie: "F. catus"
                }
            },
            "león": {
                nombre: "León (Panthera leo)",
                tipo: "Mamífero carnívoro",
                info: "El león es un gran felino carnívoro, conocido como el 'rey de la selva'.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Sabanas de África",
                caracteristicas: "Depredador ápice, vive en manadas.",
                curiosidades: "Las leonas hacen la mayor parte de la caza.",
                esperanza_vida: "10-14 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Panthera",
                    especie: "P. leo"
                }
            },
            "Tigre": {
                nombre: "Tigre (Panthera tigris)",
                tipo: "Mamífero carnívoro",
                info: "El tigre es el felino más grande del mundo, conocido por sus rayas distintivas.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques de Asia",
                caracteristicas: "Nadador fuerte, solitario.",
                curiosidades: "Cada tigre tiene un patrón único de rayas.",
                esperanza_vida: "8-10 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Panthera",
                    especie: "P. tigris"
                }
            },
            "Elefante": {
                nombre: "Elefante (Loxodonta africana)",
                tipo: "Mamífero herbívoro",
                info: "El elefante es el mamífero terrestre más grande, conocido por su trompa y colmillos.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Sabana y bosques de África",
                caracteristicas: "Gran memoria, social.",
                curiosidades: "Pueden comunicarse a largas distancias con infrasonidos.",
                esperanza_vida: "60-70 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Proboscidea",
                    familia: "Elephantidae",
                    genero: "Loxodonta",
                    especie: "L. africana"
                }
            },
            "Jirafa": {
                nombre: "Jirafa (Giraffa camelopardalis)",
                tipo: "Mamífero herbívoro",
                info: "La jirafa es el animal terrestre más alto, conocida por su largo cuello.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Sabana africana",
                caracteristicas: "Cuello largo, lengua prensil.",
                curiosidades: "Pueden correr hasta 60 km/h.",
                esperanza_vida: "25 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Giraffidae",
                    genero: "Giraffa",
                    especie: "G. camelopardalis"
                }
            },
            "Cebra": {
                nombre: "Cebra (Equus quagga)",
                tipo: "Mamífero herbívoro",
                info: "La cebra es un mamífero conocido por sus rayas blancas y negras.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Sabana africana",
                caracteristicas: "Rayas únicas, social.",
                curiosidades: "Las rayas ayudan a repeler insectos.",
                esperanza_vida: "20-30 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Perissodactyla",
                    familia: "Equidae",
                    genero: "Equus",
                    especie: "E. quagga"
                }
            },
            "Hipopotamo": {
                nombre: "Hipopótamo (Hippopotamus amphibius)",
                tipo: "Mamífero herbívoro",
                info: "El hipopótamo es un gran mamífero semiacuático conocido por su tamaño y fuerza.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Ríos y lagos de África",
                caracteristicas: "Semiacuático, agresivo.",
                curiosidades: "Pueden cerrar sus fosas nasales bajo el agua.",
                esperanza_vida: "40-50 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Hippopotamidae",
                    genero: "Hippopotamus",
                    especie: "H. amphibius"
                }
            },
            "Rinoceronte": {
                nombre: "Rinoceronte (Rhinocerotidae)",
                tipo: "Mamífero herbívoro",
                info: "El rinoceronte es un gran mamífero conocido por su cuerno distintivo.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Sabana y bosques de África y Asia",
                caracteristicas: "Piel gruesa, territorial.",
                curiosidades: "Su cuerno está hecho de queratina.",
                esperanza_vida: "35-50 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Perissodactyla",
                    familia: "Rhinocerotidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Gorila": {
                nombre: "Gorila (Gorilla gorilla)",
                tipo: "Mamífero primate",
                info: "El gorila es el primate más grande, conocido por su fuerza y comportamiento social.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques de África central",
                caracteristicas: "Fuerza impresionante, social.",
                curiosidades: "Comparten el 98% de su ADN con los humanos.",
                esperanza_vida: "35-40 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Primates",
                    familia: "Hominidae",
                    genero: "Gorilla",
                    especie: "G. gorilla"
                }
            },
            "chimpanse": {
                nombre: "Chimpancé (Pan troglodytes)",
                tipo: "Mamífero primate",
                info: "El chimpancé es un primate conocido por su inteligencia y uso de herramientas.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques de África central y occidental",
                caracteristicas: "Inteligente, social.",
                curiosidades: "Pueden aprender lenguaje de señas.",
                esperanza_vida: "40-50 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Primates",
                    familia: "Hominidae",
                    genero: "Pan",
                    especie: "P. troglodytes"
                }
            },
            "Orangutan": {
                nombre: "Orangután (Pongo pygmaeus)",
                tipo: "Mamífero primate",
                info: "El orangután es un primate conocido por su pelaje rojo y comportamiento arbóreo.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques de Borneo y Sumatra",
                caracteristicas: "Inteligente, arbóreo.",
                curiosidades: "Pasan la mayor parte del tiempo en los árboles.",
                esperanza_vida: "30-40 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro crítico",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Primates",
                    familia: "Hominidae",
                    genero: "Pongo",
                    especie: "P. pygmaeus"
                }
            },
            "Oso polar": {
                nombre: "Oso polar (Ursus maritimus)",
                tipo: "Mamífero carnívoro",
                info: "El oso polar es un gran mamífero adaptado al frío extremo del Ártico.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Regiones árticas",
                caracteristicas: "Aislante térmico, nadador fuerte.",
                curiosidades: "Su piel es negra debajo del pelaje blanco.",
                esperanza_vida: "20-25 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Ursidae",
                    genero: "Ursus",
                    especie: "U. maritimus"
                }
            },
            "Osos pardo": {
                nombre: "Oso pardo (Ursus arctos)",
                tipo: "Mamífero omnívoro",
                info: "El oso pardo es un gran mamífero conocido por su fuerza y adaptabilidad.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques y montañas de América del Norte, Europa y Asia",
                caracteristicas: "Fuerza impresionante, buen olfato.",
                curiosidades: "Pueden correr hasta 56 km/h.",
                esperanza_vida: "20-30 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Ursidae",
                    genero: "Ursus",
                    especie: "U. arctos"
                }
            },
            "Koala": {
                nombre: "Koala (Phascolarctos cinereus)",
                tipo: "Marsupial herbívoro",
                info: "El koala es un marsupial conocido por su dieta exclusiva de hojas de eucalipto.",
                alimentacion: "Herbívoro",
                clasificacion: "Marsupial",
                habitat: "Bosques de eucaliptos en Australia",
                caracteristicas: "Dormilón, trepador experto.",
                curiosidades: "Pasan hasta 20 horas al día durmiendo.",
                esperanza_vida: "10-15 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo (marsupial)",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Diprotodontia",
                    familia: "Phascolarctidae",
                    genero: "Phascolarctos",
                    especie: "P. cinereus"
                }
            },
            "Canguro rojo": {
                nombre: "Canguro rojo (Macropus rufus)",
                tipo: "Marsupial herbívoro",
                info: "El canguro rojo es el marsupial más grande, conocido por su capacidad de salto.",
                alimentacion: "Herbívoro",
                clasificacion: "Marsupial",
                habitat: "Zonas áridas y semiáridas de Australia",
                caracteristicas: "Gran saltador, social.",
                curiosidades: "Pueden saltar hasta 3 veces su altura.",
                esperanza_vida: "6-8 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo (marsupial)",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Diprotodontia",
                    familia: "Macropodidae",
                    genero: "Macropus",
                    especie: "M. rufus"
                }
            },
            "Lobo gris": {
                nombre: "Lobo gris (Canis lupus)",
                tipo: "Mamífero carnívoro",
                info: "El lobo gris es un depredador social conocido por vivir y cazar en manadas.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques, tundras y montañas del hemisferio norte",
                caracteristicas: "Depredador ápice, social.",
                curiosidades: "Pueden recorrer hasta 50 km en una noche.",
                esperanza_vida: "6-8 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Canidae",
                    genero: "Canis",
                    especie: "C. lupus"
                }
            },
            "Zorro rojo": {
                nombre: "Zorro rojo (Vulpes vulpes)",
                tipo: "Mamífero omnívoro",
                info: "El zorro rojo es un mamífero conocido por su astucia y adaptabilidad.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques, praderas y áreas urbanas de Eurasia y América del Norte",
                caracteristicas: "Astuto, adaptable.",
                curiosidades: "Pueden trepar árboles y nadar.",
                esperanza_vida: "3-4 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Canidae",
                    genero: "Vulpes",
                    especie: "V. vulpes"
                }
            },
            "Jaguar": {
                nombre: "Jaguar (Panthera onca)",
                tipo: "Mamífero carnívoro",
                info: "El jaguar es un gran felino conocido por su fuerza y habilidades de natación.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Selvas y bosques de América Central y del Sur",
                caracteristicas: "Fuerza impresionante, buen nadador.",
                curiosidades: "Tienen la mordida más fuerte entre los felinos.",
                esperanza_vida: "12-15 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Casi amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Panthera",
                    especie: "P. onca"
                }
            },
            "Leopardo": {
                nombre: "Leopardo (Panthera pardus)",
                tipo: "Mamífero carnívoro",
                info: "El leopardo es un gran felino conocido por su agilidad y adaptabilidad a diversos hábitats.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques, sabanas y montañas de África y Asia",
                caracteristicas: "Ágil, buen trepador.",
                curiosidades: "Pueden arrastrar presas más pesadas que ellos mismos a los árboles.",
                esperanza_vida: "12-15 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Panthera",
                    especie: "P. pardus"
                }
            },
            "Guepardo": {
                nombre: "Guepardo (Acinonyx jubatus)",
                tipo: "Mamífero carnívoro",
                info: "El guepardo es el animal terrestre más rápido, conocido por sus habilidades de caza a alta velocidad.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Sabanas y llanuras de África",
                caracteristicas: "Velocidad extrema, cuerpo aerodinámico.",
                curiosidades: "Pueden alcanzar velocidades de hasta 112 km/h.",
                esperanza_vida: "10-12 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Acinonyx",
                    especie: "A. jubatus"
                }
            },
            "Lince ibérico": {
                nombre: "Lince ibérico (Lynx pardinus)",
                tipo: "Mamífero carnívoro",
                info: "El lince ibérico es un felino endémico de la península ibérica, conocido por sus orejas puntiagudas y manchas en el pelaje.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques mediterráneos de España y Portugal",
                caracteristicas: "Orejas con pinceles, excelente cazador.",
                curiosidades: "Es uno de los felinos más amenazados del mundo.",
                esperanza_vida: "10-12 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro crítico",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Felidae",
                    genero: "Lynx",
                    especie: "L. pardinus"
                }
            },
            "Delfin": {
                nombre: "Delfín (Delphinidae)",
                tipo: "Mamífero marino",
                info: "El delfín es un mamífero acuático conocido por su inteligencia y habilidades sociales.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Océanos y mares de todo el mundo",
                caracteristicas: "Inteligente, social.",
                curiosidades: "Pueden comunicarse mediante sonidos y ecolocación.",
                esperanza_vida: "20-60 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Cetacea",
                    familia: "Delphinidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Ballena azul": {
                nombre: "Ballena azul (Balaenoptera musculus)",
                tipo: "Mamífero marino",
                info: "La ballena azul es el animal más grande que ha existido en la Tierra.",
                alimentacion: "Carnívoro (krill)",
                clasificacion: "Mamífero",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Gigante, migratoria.",
                curiosidades: "Puede alcanzar longitudes de hasta 30 metros.",
                esperanza_vida: "70-90 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Cetacea",
                    familia: "Balaenopteridae",
                    genero: "Balaenoptera",
                    especie: "B. musculus"
                }
            },
            "Orca": {
                nombre: "Orca (Orcinus orca)",
                tipo: "Mamífero marino",
                info: "La orca, también conocida como ballena asesina, es un depredador ápice en los océanos.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Depredador social, inteligente.",
                curiosidades: "Viven en grupos familiares llamados manadas.",
                esperanza_vida: "50-80 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Cetacea",
                    familia: "Delphinidae",
                    genero: "Orcinus",
                    especie: "O. orca"
                }
            },
            "Tiburon blanco": {
                nombre: "Tiburón blanco (Carcharodon carcharias)",
                tipo: "Pez cartilaginoso",
                info: "El tiburón blanco es un depredador marino conocido por su tamaño y fuerza.",
                alimentacion: "Carnívoro",
                clasificacion: "Pez",
                habitat: "Océanos costeros y mar abierto",
                caracteristicas: "Depredador ápice, excelente nadador.",
                curiosidades: "Pueden detectar una gota de sangre en 25 galones de agua.",
                esperanza_vida: "70 años",
                esqueleto: "Aparejo cartilaginoso",
                reproduccion: "Ovovivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Chondrichthyes",
                    orden: "Lamniformes",
                    familia: "Lamnidae",
                    genero: "Carcharodon",
                    especie: "C. carcharias"
                }
            },
            "Aguila calva": {
                nombre: "Águila calva (Haliaeetus leucocephalus)",
                tipo: "Ave rapaz",
                info: "El águila calva es un ave rapaz conocida por ser el símbolo nacional de Estados Unidos.",
                alimentacion: "Carnívoro",
                clasificacion: "Ave",
                habitat: "Cerca de cuerpos de agua en América del Norte",
                caracteristicas: "Vista aguda, volador poderoso.",
                curiosidades: "Pueden ver hasta 8 veces mejor que los humanos.",
                esperanza_vida: "20-30 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Accipitriformes",
                    familia: "Accipitridae",
                    genero: "Haliaeetus",
                    especie: "H. leucocephalus"
                }
            },
            "Buho real": {
                nombre: "Búho real (Bubo bubo)",
                tipo: "Ave rapaz nocturna",
                info: "El búho real es una de las especies de búhos más grandes y poderosas.",
                alimentacion: "Carnívoro",
                clasificacion: "Ave",
                habitat: "Bosques, montañas y áreas abiertas de Eurasia y el norte de África",
                caracteristicas: "Vista y oído agudos, cazador nocturno.",
                curiosidades: "Pueden girar su cabeza hasta 270 grados.",
                esperanza_vida: "20 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Strigiformes",
                    familia: "Strigidae",
                    genero: "Bubo",
                    especie: "B. bubo"
                }
            },
            "Colibri": {
                nombre: "Colibrí (Trochilidae)",
                tipo: "Ave pequeña",
                info: "El colibrí es un ave conocida por su pequeño tamaño y capacidad de vuelo estacionario.",
                alimentacion: "Néctar y pequeños insectos",
                clasificacion: "Ave",
                habitat: "América desde Alaska hasta Tierra del Fuego",
                caracteristicas: "Vuelo rápido, colores brillantes.",
                curiosidades: "Pueden batir sus alas hasta 80 veces por segundo.",
                esperanza_vida: "3-5 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Apodiformes",
                    familia: "Trochilidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Pinguino emperador": {
                nombre: "Pingüino emperador (Aptenodytes forsteri)",
                tipo: "Ave marina",
                info: "El pingüino emperador es la especie de pingüino más grande y es conocido por su adaptación al frío extremo.",
                alimentacion: "Peces, calamares y krill",
                clasificacion: "Ave",
                habitat: "Antártida",
                caracteristicas: "Nadador experto, resistente al frío.",
                curiosidades: "Pueden sumergirse hasta 500 metros en busca de alimento.",
                esperanza_vida: "15-20 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Casi amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Sphenisciformes",
                    familia: "Spheniscidae",
                    genero: "Aptenodytes",
                    especie: "A. forsteri"
                }
            },
            "Flamenco": {
                nombre: "Flamenco (Phoenicopteridae)",
                tipo: "Ave zancuda",
                info: "El flamenco es un ave conocida por su plumaje rosado y patas largas.",
                alimentacion: "Algas, crustáceos y pequeños invertebrados",
                clasificacion: "Ave",
                habitat: "Lagos salados y lagunas de África, América y Europa",
                caracteristicas: "Patas largas, filtro alimenticio.",
                curiosidades: "El color rosado proviene de su dieta rica en carotenoides.",
                esperanza_vida: "20-30 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Phoenicopteriformes",
                    familia: "Phoenicopteridae",
                    genero: "Phoenicopterus",
                    especie: "Varias especies"
                }
            },
            "Loro gris africano": {
                nombre: "Loro gris africano (Psittacus erithacus)",
                tipo: "Ave psitácida",
                info: "El loro gris africano es conocido por su inteligencia y capacidad para imitar sonidos humanos.",
                alimentacion: "Frutas, semillas y nueces",
                clasificacion: "Ave",
                habitat: "Bosques de África occidental y central",
                caracteristicas: "Inteligente, buen imitador.",
                curiosidades: "Puede aprender hasta 100 palabras y frases.",
                esperanza_vida: "50-60 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "En peligro",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Psittaciformes",
                    familia: "Psittacidae",
                    genero: "Psittacus",
                    especie: "P. erithacus"
                }
            },
            "Tucan": {
                nombre: "Tucán (Ramphastidae)",
                tipo: "Ave tropical",
                info: "El tucán es conocido por su gran pico colorido y su hábitat en las selvas tropicales.",
                alimentacion: "Frutas, insectos y pequeños vertebrados",
                clasificacion: "Ave",
                habitat: "Selvas tropicales de América Central y del Sur",
                caracteristicas: "Pico grande, colores brillantes.",
                curiosidades: "El pico puede medir hasta un tercio de la longitud total del ave.",
                esperanza_vida: "15-20 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Piciformes",
                    familia: "Ramphastidae",
                    genero: "Ramphastos",
                    especie: "Varias especies"
                }
            },
            "Cuervo": {
                nombre: "Cuervo (Corvus corax)",
                tipo: "Ave passeriforme",
                info: "El cuervo es conocido por su inteligencia y adaptabilidad a diversos hábitats.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Bosques, montañas y áreas urbanas de todo el mundo",
                caracteristicas: "Inteligente, adaptable.",
                curiosidades: "Pueden resolver problemas complejos y usar herramientas.",
                esperanza_vida: "10-15 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Passeriformes",
                    familia: "Corvidae",
                    genero: "Corvus",
                    especie: "C. corax"
                }
            },
            "Gorrion común": {
                nombre: "Gorrión común (Passer domesticus)",
                tipo: "Ave passeriforme",
                info: "El gorrión común es un ave pequeña y adaptable que se encuentra en áreas urbanas y rurales.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Áreas urbanas, rurales y agrícolas de todo el mundo",
                caracteristicas: "Pequeño, social.",
                curiosidades: "Se ha adaptado bien a vivir cerca de los humanos.",
                esperanza_vida: "3-5 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Passeriformes",
                    familia: "Passeridae",
                    genero: "Passer",
                    especie: "P. domesticus"
                }
            },
            "Paloma bravía": {
                nombre: "Paloma bravía (Columba livia)",
                tipo: "Ave urbana",
                info: "La paloma bravía es una especie común en áreas urbanas de todo el mundo.",
                alimentacion: "Granívoro",
                clasificacion: "Ave",
                habitat: "Áreas urbanas y rurales de todo el mundo",
                caracteristicas: "Adaptable, social.",
                curiosidades: "Fue domesticada hace miles de años.",
                esperanza_vida: "3-5 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Columbiformes",
                    familia: "Columbidae",
                    genero: "Columba",
                    especie: "C. livia"
                }
            },
            "Cocodrilo": {
                nombre: "Cocodrilo (Crocodylinae)",
                tipo: "Reptil acuático",
                info: "El cocodrilo es un reptil grande y poderoso conocido por su mandíbula fuerte y comportamiento agresivo.",
                alimentacion: "Carnívoro",
                clasificacion: "Reptil",
                habitat: "Ríos, lagos y humedales de África, Asia, América y Australia",
                caracteristicas: "Mandíbulas fuertes, piel escamosa.",
                curiosidades: "Pueden vivir hasta 70 años.",
                esperanza_vida: "50-70 años",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Crocodylia",
                    familia: "Crocodylidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Serpieente Piton": {
                nombre: "Serpiente Pitón (Pythonidae)",
                tipo: "Reptil constrictor",
                info: "La pitón es una serpiente grande conocida por su método de caza por constricción.",
                alimentacion: "Carnívoro",
                clasificacion: "Reptil",
                habitat: "Selvas, sabanas y áreas rocosas de África, Asia y Australia",
                caracteristicas: "Constrictor, sin veneno.",
                curiosidades: "Pueden medir hasta 10 metros de longitud.",
                esperanza_vida: "20-30 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Pythonidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Camaleon": {
                nombre: "Camaleón (Chamaeleonidae)",
                tipo: "Reptil",
                info: "El camaleón es conocido por su capacidad para cambiar de color y su lengua larga y pegajosa.",
                alimentacion: "Insectívoro",
                clasificacion: "Reptil",
                habitat: "Bosques y desiertos de África, Madagascar y Asia",
                caracteristicas: "Cambio de color, lengua larga.",
                curiosidades: "Pueden mover sus ojos de forma independiente.",
                esperanza_vida: "5-7 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Chamaeleonidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Tortuga marina": {
                nombre: "Tortuga marina (Cheloniidae)",
                tipo: "Reptil marino",
                info: "La tortuga marina es un reptil adaptado a la vida en el océano, conocido por sus largas migraciones.",
                alimentacion: "Omnívoro",
                clasificacion: "Reptil",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Caparazón duro, nadadora experta.",
                curiosidades: "Pueden vivir más de 100 años.",
                esperanza_vida: "50-100 años",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Testudines",
                    familia: "Cheloniidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Iguana verde": {
                nombre: "Iguana verde (Iguana iguana)",
                tipo: "Reptil herbívoro",
                info: "La iguana verde es un reptil conocido por su color verde brillante y su dieta herbívora.",
                alimentacion: "Herbívoro",
                clasificacion: "Reptil",
                habitat: "Bosques tropicales de América Central y del Sur",
                caracteristicas: "Color verde, buen trepador.",
                curiosidades: "Pueden nadar largas distancias.",
                esperanza_vida: "15-20 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Preocupación menor",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Iguanidae",
                    genero: "Iguana",
                    especie: "I. iguana"
                }
            },
            "Rana": {
                nombre: "Rana (Anura)",
                tipo: "Anfibio",
                info: "La rana es un anfibio conocido por su capacidad de vivir tanto en agua como en tierra.",
                alimentacion: "Carnívoro",
                clasificacion: "Anfibio",
                habitat: "Diversos hábitats acuáticos y terrestres en todo el mundo",
                caracteristicas: "Piel permeable, saltadora.",
                curiosidades: "Pueden respirar a través de su piel.",
                esperanza_vida: "4-15 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Amphibia",
                    orden: "Anura",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Sapo": {
                nombre: "Sapo (Bufonidae)",
                tipo: "Anfibio",
                info: "El sapo es un anfibio conocido por su piel rugosa y glándulas venenosas.",
                alimentacion: "Carnívoro",
                clasificacion: "Anfibio",
                habitat: "Diversos hábitats terrestres y acuáticos en todo el mundo",
                caracteristicas: "Piel rugosa, glándulas venenosas.",
                curiosidades: "Pueden inflar su cuerpo para parecer más grandes.",
                esperanza_vida: "10-12 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Amphibia",
                    orden: "Anura",
                    familia: "Bufonidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Salamandra": {
                nombre: "Salamandra (Caudata)",
                tipo: "Anfibio",
                info: "La salamandra es un anfibio conocido por su cuerpo alargado y cola.",
                alimentacion: "Carnívoro",
                clasificacion: "Anfibio",
                habitat: "Bosques húmedos y áreas acuáticas en todo el mundo",
                caracteristicas: "Cuerpo alargado, cola.",
                curiosidades: "Pueden regenerar extremidades perdidas.",
                esperanza_vida: "10-20 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Amphibia",
                    orden: "Caudata",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Ajaolote": {
                nombre: "Ajolote (Ambystoma mexicanum)",
                tipo: "Anfibio neoténico",
                info: "El ajolote es un anfibio conocido por su capacidad de regeneración y su apariencia única.",
                alimentacion: "Carnívoro",
                clasificacion: "Anfibio",
                habitat: "Lagos y canales de Xochimilco, México",
                caracteristicas: "Neoténico, regenerativo.",
                curiosidades: "Puede regenerar órganos completos.",
                esperanza_vida: "10-15 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "En peligro crítico",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Amphibia",
                    orden: "Caudata",
                    familia: "Ambystomatidae",
                    genero: "Ambystoma",
                    especie: "A. mexicanum"
                }
            },
            "Salmon": {
                nombre: "Salmón (Salmo salar)",
                tipo: "Pez óseo",
                info: "El salmón es un pez conocido por su migración desde el océano hasta los ríos para reproducirse.",
                alimentacion: "Omnívoro",
                clasificacion: "Pez",
                habitat: "Océanos y ríos del hemisferio norte",
                caracteristicas: "Migratorio, resistente.",
                curiosidades: "Pueden saltar obstáculos de hasta 3 metros de altura.",
                esperanza_vida: "4-6 años",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la población",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Actinopterygii",
                    orden: "Salmoniformes",
                    familia: "Salmonidae",
                    genero: "Salmo",
                    especie: "S. salar"
                }
            },
            "Ajolote": {
                nombre: "Ajolote (Ambystoma mexicanum)",
                tipo: "Anfibio neoténico",
                info: "El ajolote es un anfibio conocido por su capacidad de regeneración y su apariencia única.",
                alimentacion: "Carnívoro",
                clasificacion: "Anfibio",
                habitat: "Lagos y canales de Xochimilco, México",
                caracteristicas: "Neoténico, regenerativo.",
                curiosidades: "Puede regenerar órganos completos.",
                esperanza_vida: "10-15 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "En peligro crítico",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Amphibia",
                    orden: "Caudata",
                    familia: "Ambystomatidae",
                    genero: "Ambystoma",
                    especie: "A. mexicanum"
                }
            },
            "Salmon": {
                nombre: "Salmón (Salmo salar)",
                tipo: "Pez óseo",
                info: "El salmón es un pez conocido por su migración desde el océano hasta los ríos para reproducirse.",
                alimentacion: "Omnívoro",
                clasificacion: "Pez",
                habitat: "Océanos y ríos del hemisferio norte",
                caracteristicas: "Migratorio, resistente.",
                curiosidades: "Pueden saltar obstáculos de hasta 3 metros de altura.",
                esperanza_vida: "4-6 años",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la población",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Actinopterygii",
                    orden: "Salmoniformes",
                    familia: "Salmonidae",
                    genero: "Salmo",
                    especie: "S. salar"
                }
            },
            "Tiburón martillo": {
                nombre: "Tiburón martillo (Sphyrnidae)",
                tipo: "Pez cartilaginoso",
                info: "El tiburón martillo es conocido por la forma distintiva de su cabeza en forma de 'T'.",
                alimentacion: "Carnívoro",
                clasificacion: "Pez",
                habitat: "Océanos cálidos y templados de todo el mundo",
                caracteristicas: "Cabeza en forma de 'T', buen nadador.",
                curiosidades: "Utilizan su cabeza para detectar presas.",
                esperanza_vida: "20-30 años",
                esqueleto: "Aparejo cartilaginoso",
                reproduccion: "Vivíparo",
                conservacion: "Vulnerable",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Chondrichthyes",
                    orden: "Carcharhiniformes",
                    familia: "Sphyrnidae",
                    genero: "Sphyrna",
                    especie: "Varias especies"
                }
            },
            "Pulpo": {
                nombre: "Pulpo (Octopoda)",
                tipo: "Molusco",
                info: "El pulpo es un molusco conocido por su inteligencia y capacidad para cambiar de color.",
                alimentacion: "Carnívoro",
                clasificacion: "Molusco",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Ocho brazos, camuflaje.",
                curiosidades: "Pueden resolver problemas complejos.",
                esperanza_vida: "1-2 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Mollusca",
                    clase: "Cephalopoda",
                    orden: "Octopoda",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Calamar gigante": {
                nombre: "Calamar gigante (Architeuthis dux)",
                tipo: "Molusco",
                info: "El calamar gigante es una de las criaturas más grandes del océano, conocido por su tamaño impresionante.",
                alimentacion: "Carnívoro",
                clasificacion: "Molusco",
                habitat: "Océanos profundos de todo el mundo",
                caracteristicas: "Gran tamaño, tentáculos largos.",
                curiosidades: "Pueden alcanzar longitudes de hasta 13 metros.",
                esperanza_vida: "5 años aproximadamente",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Desconocida",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Mollusca",
                    clase: "Cephalopoda",
                    orden: "Teuthida",
                    familia: "Architeuthidae",
                    genero: "Architeuthis",
                    especie: "A. dux"
                }
            },
            "medusa": {
                nombre: "Medusa (Scyphozoa)",
                tipo: "Cnidario",
                info: "La medusa es un cnidario conocido por su cuerpo gelatinoso y tentáculos urticantes.",
                alimentacion: "Carnívoro",
                clasificacion: "Cnidario",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Cuerpo gelatinoso, tentáculos urticantes.",
                curiosidades: "Pueden bioluminiscentes.",
                esperanza_vida: "Varía según la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Cnidaria",
                    clase: "Scyphozoa",
                    orden: "Varios órdenes",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Estrella de mar": {
                nombre: "Estrella de mar (Asteroidea)",
                tipo: "Equinodermo",
                info: "La estrella de mar es un equinodermo conocido por su forma de estrella y capacidad de regeneración.",
                alimentacion: "Carnívoro",
                clasificacion: "Equinodermo",
                habitat: "Océanos de todo el mundo",
                caracteristicas: "Forma de estrella, regenerativa.",
                curiosidades: "Pueden regenerar brazos perdidos.",
                esperanza_vida: "5-35 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Echinodermata",
                    clase: "Asteroidea",
                    orden: "Varios órdenes",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "caracol": {
                nombre: "Caracol (Gastropoda)",
                tipo: "Molusco",
                info: "El caracol es un molusco conocido por su concha espiral y movimiento lento.",
                alimentacion: "Herbívoro",
                clasificacion: "Molusco",
                habitat: "Diversos hábitats terrestres y acuáticos en todo el mundo",
                caracteristicas: "Concha espiral, movimiento lento.",
                curiosidades: "Pueden retraer su cuerpo dentro de la concha para protección.",
                esperanza_vida: "2-5 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Mollusca",
                    clase: "Gastropoda",
                    orden: "Varios órdenes",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Babosa": {
                nombre: "Babosa (Pulmonata)",
                tipo: "Molusco",
                info: "La babosa es un molusco conocido por su cuerpo blando y sin concha o con concha reducida.",
                alimentacion: "Herbívoro",
                clasificacion: "Molusco",
                habitat: "Diversos hábitats terrestres y acuáticos en todo el mundo",
                caracteristicas: "Cuerpo blando, sin concha o concha reducida.",
                curiosidades: "Producen moco para facilitar el movimiento.",
                esperanza_vida: "1-2 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Mollusca",
                    clase: "Gastropoda",
                    orden: "Pulmonata",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Ostra": {
                nombre: "Ostra (Ostreidae)",
                tipo: "Molusco bivalvo",
                info: "La ostra es un molusco conocido por su concha dura y su capacidad para producir perlas.",
                alimentacion: "Filtrador",
                clasificacion: "Molusco",
                habitat: "Aguas marinas y salobres de todo el mundo",
                caracteristicas: "Concha dura, filtrador.",
                curiosidades: "Pueden producir perlas como defensa contra irritantes.",
                esperanza_vida: "20 años aproximadamente",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Mollusca",
                    clase: "Bivalvia",
                    orden: "Ostreoida",
                    familia: "Ostreidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Langosta": {
                nombre: "Langosta (Nephropidae)",
                tipo: "Crustáceo",
                info: "La langosta es un crustáceo conocido por su sabor y valor culinario.",
                alimentacion: "Omnívoro",
                clasificacion: "Crustáceo",
                habitat: "Fondos marinos rocosos de océanos de todo el mundo",
                caracteristicas: "Caparazón duro, pinzas grandes.",
                curiosidades: "Pueden regenerar extremidades perdidas.",
                esperanza_vida: "50 años o más",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la población",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Malacostraca",
                    orden: "Decapoda",
                    familia: "Nephropidae",
                    genero: "Homarus",
                    especie: "Varias especies"
                }
            },
            "Cangrejo": {
                nombre: "Cangrejo (Brachyura)",
                tipo: "Crustáceo",
                info: "El cangrejo es un crustáceo conocido por su caparazón duro y patas adaptadas para caminar de lado.",
                alimentacion: "Omnívoro",
                clasificacion: "Crustáceo",
                habitat: "Diversos hábitats acuáticos y terrestres en todo el mundo",
                caracteristicas: "Caparazón duro, patas para caminar de lado.",
                curiosidades: "Pueden regenerar extremidades perdidas.",
                esperanza_vida: "3-4 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Malacostraca",
                    orden: "Decapoda",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Araña": {
                nombre: "Araña (Araneae)",
                tipo: "Arácnido",
                info: "La araña es un arácnido conocido por su capacidad para tejer telas de seda.",
                alimentacion: "Carnívoro",
                clasificacion: "Arácnido",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Ocho patas, tejedora de telas.",
                curiosidades: "Producen seda para construir telas y capturar presas.",
                esperanza_vida: "1-2 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Arachnida",
                    orden: "Araneae",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Escorpión": {
                nombre: "Escorpión (Scorpiones)",
                tipo: "Arácnido",
                info: "El escorpión es un arácnido conocido por su aguijón venenoso en la cola.",
                alimentacion: "Carnívoro",
                clasificacion: "Arácnido",
                habitat: "Desiertos y áreas cálidas de todo el mundo",
                caracteristicas: "Aguijón venenoso, nocturno.",
                curiosidades: "Pueden sobrevivir largos períodos sin comida.",
                esperanza_vida: "3-8 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Arachnida",
                    orden: "Scorpiones",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Mosca": {
                nombre: "Mosca (Diptera)",
                tipo: "Insecto",
                info: "La mosca es un insecto conocido por su capacidad de vuelo y su presencia común en diversos entornos.",
                alimentacion: "Omnívoro",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Capacidad de vuelo, ojos compuestos.",
                curiosidades: "Pueden detectar movimientos rápidos.",
                esperanza_vida: "15-30 días dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Diptera",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Abeja": {
                nombre: "Abeja (Apidae)",
                tipo: "Insecto",
                info: "La abeja es un insecto conocido por su papel en la polinización y la producción de miel.",
                alimentacion: "Néctar y polen",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Polinizadora, productora de miel.",
                curiosidades: "Pueden comunicarse mediante danzas.",
                esperanza_vida: "5-6 semanas para obreras, varios años para reinas",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Hymenoptera",
                    familia: "Apidae",
                    genero: "Apis",
                    especie: "Varias especies"
                }
            },
            "Hormiga": {
                nombre: "Hormiga (Formicidae)",
                tipo: "Insecto",
                info: "La hormiga es un insecto conocido por su organización social y trabajo en equipo.",
                alimentacion: "Omnívoro",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Organización social, trabajadora.",
                curiosidades: "Pueden levantar objetos muchas veces su peso.",
                esperanza_vida: "Varía según la casta y especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Hymenoptera",
                    familia: "Formicidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Mariposa": {
                nombre: "Mariposa (Lepidoptera)",
                tipo: "Insecto",
                info: "La mariposa es un insecto conocido por sus coloridas alas y metamorfosis.",
                alimentacion: "Néctar",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Alas coloridas, metamorfosis completa.",
                curiosidades: "Algunas especies migran largas distancias.",
                esperanza_vida: "Varía según la especie, desde días hasta meses",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Lepidoptera",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Escarabajo": {
                nombre: "Escarabajo (Coleoptera)",
                tipo: "Insecto",
                info: "El escarabajo es un insecto conocido por su caparazón duro y diversidad de especies.",
                alimentacion: "Varía según la especie",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Caparazón duro, antenas.",
                curiosidades: "Es el grupo más grande de insectos.",
                esperanza_vida: "Varía según la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Coleoptera",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Libélula": {
                nombre: "Libélula (Odonata)",
                tipo: "Insecto",
                info: "La libélula es un insecto conocido por su vuelo ágil y ojos compuestos grandes.",
                alimentacion: "Carnívoro",
                clasificacion: "Insecto",
                habitat: "Cerca de cuerpos de agua en todo el mundo",
                caracteristicas: "Vuelo ágil, ojos compuestos grandes.",
                curiosidades: "Pueden volar hacia atrás.",
                esperanza_vida: "Varía según la especie, desde semanas hasta meses",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Odonata",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Grillo": {
                nombre: "Grillo (Gryllidae)",
                tipo: "Insecto",
                info: "El grillo es un insecto conocido por su canto característico producido al frotar sus alas.",
                alimentacion: "Omnívoro",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Canto característico, antenas largas.",
                curiosidades: "Pueden saltar grandes distancias.",
                esperanza_vida: "2-3 meses dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Orthoptera",
                    familia: "Gryllidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Cigarra": {
                nombre: "Cigarra (Cicadidae)",
                tipo: "Insecto",
                info: "La cigarra es un insecto conocido por su canto fuerte producido por órganos especiales llamados timbales.",
                alimentacion: "Fitófago",
                clasificacion: "Insecto",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Canto fuerte, ciclo de vida largo.",
                curiosidades: "Algunas especies tienen ciclos de vida de hasta 17 años.",
                esperanza_vida: "Varía según la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Arthropoda",
                    clase: "Insecta",
                    orden: "Hemiptera",
                    familia: "Cicadidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Lombriz de tierra": {
                nombre: "Lombriz de tierra (Lumbricina)",
                tipo: "Anélido",
                info: "La lombriz de tierra es un anélido conocido por su papel en la aireación del suelo y descomposición de materia orgánica.",
                alimentacion: "Detritívoro",
                clasificacion: "Anélido",
                habitat: "Suelos húmedos en todo el mundo",
                caracteristicas: "Cuerpo segmentado, sin patas.",
                curiosidades: "Pueden regenerar partes de su cuerpo.",
                esperanza_vida: "4-8 años dependiendo de la especie",
                esqueleto: "Invertebrado",
                reproduccion: "Hermafrodita",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Annelida",
                    clase: "Clitellata",
                    orden: "Opistopora",
                    familia: "Lumbricidae",
                    genero: "Lumbricus",
                    especie: "Varias especies"
                }
            },
            "ciervo": {
                nombre: "Ciervo (Cervidae)",
                tipo: "Mamífero",
                info: "El ciervo es un mamífero conocido por sus astas ramificadas y agilidad.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques y praderas en todo el mundo",
                caracteristicas: "Astas ramificadas, agilidad.",
                curiosidades: "Los machos mudan sus astas anualmente.",
                esperanza_vida: "10-20 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Cervidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Cabra montés": {
                nombre: "Cabra montés (Capra aegagrus)",
                tipo: "Mamífero",
                info: "La cabra montés es un mamífero conocido por su habilidad para escalar terrenos rocosos.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Zonas montañosas de Europa, Asia y África",
                caracteristicas: "Habilidad para escalar, cuernos curvados.",
                curiosidades: "Pueden saltar grandes distancias entre rocas.",
                esperanza_vida: "10-15 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Casi amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Bovidae",
                    genero: "Capra",
                    especie: "C. aegagrus"
                }
            },
            "Conejo": {
                nombre: "Conejo (Oryctolagus cuniculus)",
                tipo: "Mamífero",
                info: "El conejo es un mamífero conocido por sus largas orejas y capacidad de reproducción rápida.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Diversos hábitats terrestres en todo el mundo",
                caracteristicas: "Largas orejas, patas traseras fuertes.",
                curiosidades: "Pueden reproducirse varias veces al año.",
                esperanza_vida: "8-12 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Lagomorpha",
                    familia: "Leporidae",
                    genero: "Oryctolagus",
                    especie: "O. cuniculus"
                }
            },
            "Ardilla": {
                nombre: "Ardilla (Sciuridae)",
                tipo: "Mamífero",
                info: "La ardilla es un mamífero conocido por su agilidad y hábito de almacenar alimentos.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques, parques y áreas urbanas en todo el mundo",
                caracteristicas: "Agilidad, cola peluda.",
                curiosidades: "Pueden recordar la ubicación de cientos de escondites de comida.",
                esperanza_vida: "6-12 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Rodentia",
                    familia: "Sciuridae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Erizo": {
                nombre: "Erizo (Erinaceidae)",
                tipo: "Mamífero",
                info: "El erizo es un mamífero conocido por sus espinas protectoras y comportamiento nocturno.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Diversos hábitats terrestres en Europa, Asia y África",
                caracteristicas: "Espinas protectoras, comportamiento nocturno.",
                curiosidades: "Se enrollan en una bola para protegerse.",
                esperanza_vida: "3-7 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Erinaceomorpha",
                    familia: "Erinaceidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Murciélago": {
                nombre: "Murciélago (Chiroptera)",
                tipo: "Mamífero",
                info: "El murciélago es un mamífero conocido por su capacidad de vuelo y ecolocación.",
                alimentacion: "Varía según la especie",
                clasificacion: "Mamífero",
                habitat: "Diversos hábitats en todo el mundo",
                caracteristicas: "Capacidad de vuelo, ecolocación.",
                curiosidades: "Son los únicos mamíferos capaces de vuelo sostenido.",
                esperanza_vida: "5-30 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Chiroptera",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Nutria": {
                nombre: "Nutria (Lutrinae)",
                tipo: "Mamífero",
                info: "La nutria es un mamífero semiacuático conocido por su agilidad en el agua y comportamiento juguetón.",
                alimentacion: "Carnívoro",
                clasificacion: "Mamífero",
                habitat: "Ríos, lagos y costas en todo el mundo",
                caracteristicas: "Agilidad en el agua, comportamiento juguetón.",
                curiosidades: "Utilizan herramientas para abrir conchas.",
                esperanza_vida: "8-15 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Mustelidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Tejon": {
                nombre: "Tejón (Meles meles)",
                tipo: "Mamífero",
                info: "El tejón es un mamífero conocido por su cuerpo robusto y hábitos excavadores.",
                alimentacion: "Omnívoro",
                clasificacion: "Mamífero",
                habitat: "Bosques, praderas y áreas rurales en Europa y Asia",
                caracteristicas: "Cuerpo robusto, hábitos excavadores.",
                curiosidades: "Viven en madrigueras complejas llamadas setts.",
                esperanza_vida: "14 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Carnivora",
                    familia: "Mustelidae",
                    genero: "Meles",
                    especie: "M. meles"
                }
            },
            "castor": {
                nombre: "Castor (Castor canadensis)",
                tipo: "Mamífero",
                info: "El castor es un mamífero conocido por su habilidad para construir presas y lodges.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Ríos y lagos en América del Norte y Eurasia",
                caracteristicas: "Habilidad para construir presas, dientes incisivos grandes.",
                curiosidades: "Pueden cambiar el curso de ríos con sus construcciones.",
                esperanza_vida: "10-12 años en la naturaleza",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Rodentia",
                    familia: "Castoridae",
                    genero: "Castor",
                    especie: "C. canadensis"
                }
            },
            "camello": {
                nombre: "Camello (Camelus)",
                tipo: "Mamífero",
                info: "El camello es un mamífero conocido por su capacidad para sobrevivir en ambientes desérticos.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Desiertos de África y Asia",
                caracteristicas: "Jorobas para almacenar grasa, resistencia al calor.",
                curiosidades: "Pueden beber grandes cantidades de agua en una sola vez.",
                esperanza_vida: "40-50 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Doméstico, no amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Camelidae",
                    genero: "Camelus",
                    especie: "Varias especies"
                }
            },
            "Llama": {
                nombre: "Llama (Lama glama)",
                tipo: "Mamífero",
                info: "La llama es un mamífero domesticado conocido por su lana y uso como animal de carga.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Regiones montañosas de América del Sur",
                caracteristicas: "Lana gruesa, uso como animal de carga.",
                curiosidades: "Pueden escupir como mecanismo de defensa.",
                esperanza_vida: "15-25 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Doméstico, no amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Camelidae",
                    genero: "Lama",
                    especie: "L. glama"
                }
            },
            "alpaca": {
                nombre: "Alpaca (Vicugna pacos)",
                tipo: "Mamífero",
                info: "La alpaca es un mamífero domesticado conocido por su lana suave y fina.",
                alimentacion: "Herbívoro",
                clasificacion: "Mamífero",
                habitat: "Regiones montañosas de América del Sur",
                caracteristicas: "Lana suave, tamaño pequeño.",
                curiosidades: "Son parientes cercanos de las llamas.",
                esperanza_vida: "15-20 años",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "Doméstico, no amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Mammalia",
                    orden: "Artiodactyla",
                    familia: "Camelidae",
                    genero: "Vicugna",
                    especie: "V. pacos"
                }
            },
            "Pabo real": {
                nombre: "Pavo real (Pavo cristatus)",
                tipo: "Ave",
                info: "El pavo real es un ave conocida por su plumaje colorido y exhibiciones de cortejo.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Bosques y áreas abiertas en el sur de Asia",
                caracteristicas: "Plumaje colorido, exhibiciones de cortejo.",
                curiosidades: "El macho despliega su cola para atraer a la hembra.",
                esperanza_vida: "15-20 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "No amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Galliformes",
                    familia: "Phasianidae",
                    genero: "Pavo",
                    especie: "P. cristatus"
                }
            },
            "Avestrus": {
                nombre: "Avestruz (Struthio camelus)",
                tipo: "Ave",
                info: "El avestruz es un ave conocida por ser la más grande y rápida en tierra.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Sabana y desiertos de África",
                caracteristicas: "Gran tamaño, velocidad en tierra.",
                curiosidades: "No pueden volar, pero corren hasta 70 km/h.",
                esperanza_vida: "30-40 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "No amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Struthioniformes",
                    familia: "Struthionidae",
                    genero: "Struthio",
                    especie: "S. camelus"
                }
            },
            "kiwi": {
                nombre: "Kiwi (Apteryx)",
                tipo: "Ave",
                info: "El kiwi es un ave nocturna y no voladora originaria de Nueva Zelanda.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Bosques y áreas rurales de Nueva Zelanda",
                caracteristicas: "No voladora, pico largo.",
                curiosidades: "Tiene un sentido del olfato muy desarrollado.",
                esperanza_vida: "25-50 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Apterygiformes",
                    familia: "Apterygidae",
                    genero: "Apteryx",
                    especie: "Varias especies"
                }
            },
            "Condor": {
                nombre: "Cóndor (Vultur gryphus)",
                tipo: "Ave",
                info: "El cóndor es un ave carroñera conocida por su gran envergadura y vuelo majestuoso.",
                alimentacion: "Carroñero",
                clasificacion: "Ave",
                habitat: "Montañas y áreas abiertas de América del Sur",
                caracteristicas: "Gran envergadura, vuelo majestuoso.",
                curiosidades: "Puede volar a altitudes de hasta 5,500 metros.",
                esperanza_vida: "50-70 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Casi amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Accipitriformes",
                    familia: "Cathartidae",
                    genero: "Vultur",
                    especie: "V. gryphus"
                }
            },
            "Halcon": {
                nombre: "Halcón (Falco)",
                tipo: "Ave",
                info: "El halcón es un ave rapaz conocida por su velocidad y habilidades de caza.",
                alimentacion: "Carnívoro",
                clasificacion: "Ave",
                habitat: "Diversos hábitats en todo el mundo",
                caracteristicas: "Velocidad, habilidades de caza.",
                curiosidades: "El halcón peregrino es el animal más rápido del mundo.",
                esperanza_vida: "13-20 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Falconiformes",
                    familia: "Falconidae",
                    genero: "Falco",
                    especie: "Varias especies"
                }
            },
            "Buitre": {
                nombre: "Buitre (Accipitridae)",
                tipo: "Ave",
                info: "El buitre es un ave carroñera conocida por su papel en el ecosistema como limpiador de cadáveres.",
                alimentacion: "Carroñero",
                clasificacion: "Ave",
                habitat: "Diversos hábitats en todo el mundo",
                caracteristicas: "Carroñero, buen sentido de la vista.",
                curiosidades: "Pueden volar grandes distancias en busca de alimento.",
                esperanza_vida: "10-30 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Accipitriformes",
                    familia: "Accipitridae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "cigueña": {
                nombre: "Cigüeña (Ciconia ciconia)",
                tipo: "Ave",
                info: "La cigüeña es un ave conocida por su migración anual y asociación cultural con el nacimiento de bebés.",
                alimentacion: "Carnívoro",
                clasificacion: "Ave",
                habitat: "Zonas húmedas y áreas abiertas en Europa, África y Asia",
                caracteristicas: "Migratoria, pico largo.",
                curiosidades: "Viajan miles de kilómetros durante la migración.",
                esperanza_vida: "20-30 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Ciconiiformes",
                    familia: "Ciconiidae",
                    genero: "Ciconia",
                    especie: "C. ciconia"
                }
            },
            "Pelicano": {
                nombre: "Pelícano (Pelecanus)",
                tipo: "Ave",
                info: "El pelícano es un ave conocida por su gran pico y bolsa para capturar peces.",
                alimentacion: "Carnívoro",
                clasificacion: "Ave",
                habitat: "Zonas costeras y cuerpos de agua en todo el mundo",
                caracteristicas: "Gran pico, bolsa para peces.",
                curiosidades: "Pueden almacenar grandes cantidades de agua en su bolsa.",
                esperanza_vida: "10-25 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Pelecaniformes",
                    familia: "Pelecanidae",
                    genero: "Pelecanus",
                    especie: "Varias especies"
                }
            },
            "Gaviota": {
                nombre: "Gaviota (Laridae)",
                tipo: "Ave",
                info: "La gaviota es un ave costera conocida por su adaptabilidad y comportamiento oportunista.",
                alimentacion: "Omnívoro",
                clasificacion: "Ave",
                habitat: "Zonas costeras y cuerpos de agua en todo el mundo",
                caracteristicas: "Adaptabilidad, comportamiento oportunista.",
                curiosidades: "Pueden beber agua salada gracias a glándulas especiales.",
                esperanza_vida: "10-15 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Aves",
                    orden: "Charadriiformes",
                    familia: "Laridae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Anaconda": {
                nombre: "Anaconda (Eunectes)",
                tipo: "Reptil",
                info: "La anaconda es una serpiente gigante conocida por su tamaño y fuerza.",
                alimentacion: "Carnívoro",
                clasificacion: "Reptil",
                habitat: "Ríos y pantanos de América del Sur",
                caracteristicas: "Gran tamaño, fuerza constrictora.",
                curiosidades: "Puede crecer hasta 9 metros de longitud.",
                esperanza_vida: "10-30 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo",
                conservacion: "No amenazada",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Boidae",
                    genero: "Eunectes",
                    especie: "Varias especies"
                }
            },
            "Cobra": {
                nombre: "Cobra (Naja)",
                tipo: "Reptil",
                info: "La cobra es una serpiente venenosa conocida por su capucha característica.",
                alimentacion: "Carnívoro",
                clasificacion: "Reptil",
                habitat: "Diversos hábitats en Asia y África",
                caracteristicas: "Capucha característica, veneno potente.",
                curiosidades: "Puede erguirse y expandir su capucha cuando se siente amenazada.",
                esperanza_vida: "20 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Elapidae",
                    genero: "Naja",
                    especie: "Varias especies"
                }
            },
            "Vivora": {
                nombre: "Víbora (Viperidae)",
                tipo: "Reptil",
                info: "La víbora es una serpiente venenosa conocida por sus colmillos largos y curvados.",
                alimentacion: "Carnívoro",
                clasificacion: "Reptil",
                habitat: "Diversos hábitats en todo el mundo",
                caracteristicas: "Colmillos largos, veneno potente.",
                curiosidades: "Sus colmillos pueden plegarse cuando no están en uso.",
                esperanza_vida: "10-20 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Vivíparo u ovíparo según la especie",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Squamata",
                    familia: "Viperidae",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Tortuga": {
                nombre: "Tortuga (Testudines)",
                tipo: "Reptil",
                info: "La tortuga es un reptil conocido por su caparazón duro y longevidad.",
                alimentacion: "Varía según la especie",
                clasificacion: "Reptil",
                habitat: "Diversos hábitats en todo el mundo",
                caracteristicas: "Caparazón duro, longevidad.",
                curiosidades: "Algunas especies pueden vivir más de 100 años.",
                esperanza_vida: "50-150 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Reptilia",
                    orden: "Testudines",
                    familia: "Varios familias",
                    genero: "Varios géneros",
                    especie: "Varias especies"
                }
            },
            "Pez payaso": {
                nombre: "Pez payaso (Amphiprioninae)",
                tipo: "Pez",
                info: "El pez payaso es un pez conocido por su colorido y simbiosis con anémonas de mar.",
                alimentacion: "Omnívoro",
                clasificacion: "Pez",
                habitat: "Arrecifes de coral en el Indo-Pacífico",
                caracteristicas: "Colorido, simbiosis con anémonas.",
                curiosidades: "Puede cambiar de sexo durante su vida.",
                esperanza_vida: "6-10 años en cautiverio",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo",
                conservacion: "No amenazado",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Actinopterygii",
                    orden: "Perciformes",
                    familia: "Pomacentridae",
                    genero: "Amphiprion",
                    especie: "Varias especies"
                }
            },
            "caballito de mar": {
                nombre: "Caballito de mar (Hippocampus)",
                tipo: "Pez",
                info: "El caballito de mar es un pez conocido por su forma única y reproducción donde el macho lleva los huevos.",
                alimentacion: "Carnívoro",
                clasificacion: "Pez",
                habitat: "Aguas costeras y arrecifes en todo el mundo",
                caracteristicas: "Forma única, reproducción con macho portador.",
                curiosidades: "El macho lleva los huevos en una bolsa hasta que eclosionan.",
                esperanza_vida: "1-5 años dependiendo de la especie",
                esqueleto: "Vertebrado",
                reproduccion: "Ovíparo con macho portador",
                conservacion: "Varía según la especie",
                taxonomia: {
                    reino: "Animalia",
                    filo: "Chordata",
                    clase: "Actinopterygii",
                    orden: "Syngnathiformes",
                    familia: "Syngnathidae",
                    genero: "Hippocampus",
                    especie: "Varias especies"
                }
            },
            
            

        };
        const geoDatabase = {
            "españa": {
                nombre: "España",
                capital: "Madrid",
                continente: "Europa",
                poblacion: "47 millones",
                info: "País del sur de Europa con rica historia.",
                curiosidades: "Tiene 17 comunidades autónomas."
            },
            "méxico": {
                nombre: "México",
                capital: "Ciudad de México",
                continente: "América",
                poblacion: "126 millones",
                info: "País de gran diversidad cultural.",
                curiosidades: "Cuna de los mayas y aztecas."
            },
            "perú": {
                nombre: "Perú",
                capital: "Lima",
                continente: "América",
                poblacion: "33 millones",
                info: "Conocido por Machu Picchu.",
                curiosidades: "Centro del Imperio Inca."
            }
        };
        const infoPlanetas = {
            tierra: {
                nombre: "Tierra",
                info: "Nuestro hogar, único con vida conocida.",
                datos: {
                    'Diámetro': '12,742 km',
                    'Distancia al Sol': '150 millones de km',
                    'Temperatura media': '15°C'
                },
                icono: '<i class="fas fa-globe-americas"></i>'
            },
            marte: {
                nombre: "Marte",
                info: "El 'planeta rojo', con evidencia de agua.",
                datos: {
                    'Diámetro': '6,779 km',
                    'Distancia al Sol': '228 millones de km',
                    'Temperatura media': '-63°C'
                },
                icono: '<i class="fas fa-mountain"></i>'
            },
            jupiter: {
                nombre: "Júpiter",
                info: "El planeta más grande, gigante gaseoso.",
                datos: {
                    'Diámetro': '139,820 km',
                    'Distancia al Sol': '778 millones de km',
                    'Temperatura media': '-145°C'
                },
                icono: '<i class="fas fa-wind"></i>'
            }
        };
        const langDatabase = {
            "shakespeare": {
                nombre: "William Shakespeare",
                info: "Autor inglés de obras como Romeo y Julieta.",
                obras: "Hamlet, Macbeth"
            },
            "cervantes": {
                nombre: "Miguel de Cervantes",
                info: "Autor español de Don Quijote.",
                obras: "Don Quijote de la Mancha"
            },
            "garcia marquez": {
                nombre: "Gabriel García Márquez",
                info: "Autor colombiano de realismo mágico.",
                obras: "Cien Años de Soledad"
            }
        };
        const physDatabase = {
            "hidrogeno": {
                nombre: "Hidrógeno (H)",
                numero_atomico: "1",
                masa_atomica: "1.008",
                info: "El elemento más ligero."
            },
            "oxigeno": {
                nombre: "Oxígeno (O)",
                numero_atomico: "8",
                masa_atomica: "15.999",
                info: "Esencial para la respiración."
            },
            "carbono": {
                nombre: "Carbono (C)",
                numero_atomico: "6",
                masa_atomica: "12.011",
                info: "Base de la vida orgánica."
            }
        };
        const quizzes = {
            animales: [
                { pregunta: "¿Qué animal es conocido como el rey de la selva?", opciones: ["Perro", "Gato", "León"], correcta: 2 },
                { pregunta: "¿Qué animal ronronea?", opciones: ["Perro", "Gato", "León"], correcta: 1 },
                { pregunta: "¿Qué animal ladra?", opciones: ["Perro", "Gato", "León"], correcta: 0 }
            ],
            geografia: [
                { pregunta: "¿Capital de España?", opciones: ["Madrid", "Lima", "Ciudad de México"], correcta: 0 },
                { pregunta: "¿Capital de México?", opciones: ["Madrid", "Lima", "Ciudad de México"], correcta: 2 },
                { pregunta: "¿Capital de Perú?", opciones: ["Madrid", "Lima", "Ciudad de México"], correcta: 1 }
            ],
            espacio: [
                { pregunta: "¿Planeta rojo?", opciones: ["Tierra", "Marte", "Júpiter"], correcta: 1 },
                { pregunta: "¿Planeta con vida?", opciones: ["Tierra", "Marte", "Júpiter"], correcta: 0 },
                { pregunta: "¿Planeta más grande?", opciones: ["Tierra", "Marte", "Júpiter"], correcta: 2 }
            ],
            matematicas: [
                { pregunta: "2 + 3 = ?", opciones: ["5", "6", "4"], correcta: 0 },
                { pregunta: "5 - 2 = ?", opciones: ["2", "3", "4"], correcta: 1 },
                { pregunta: "2 * 3 = ?", opciones: ["5", "4", "6"], correcta: 2 }
            ],
            lengua: [
                { pregunta: "¿Autor de Romeo y Julieta?", opciones: ["Shakespeare", "Cervantes", "García Márquez"], correcta: 0 },
                { pregunta: "¿Autor de Don Quijote?", opciones: ["Shakespeare", "Cervantes", "García Márquez"], correcta: 1 },
                { pregunta: "¿Autor de Cien Años de Soledad?", opciones: ["Shakespeare", "Cervantes", "García Márquez"], correcta: 2 }
            ],
            fisica: [
                { pregunta: "¿Elemento con número atómico 1?", opciones: ["Hidrógeno", "Oxígeno", "Carbono"], correcta: 0 },
                { pregunta: "¿Elemento con número atómico 8?", opciones: ["Hidrógeno", "Oxígeno", "Carbono"], correcta: 1 },
                { pregunta: "¿Elemento con número atómico 6?", opciones: ["Hidrógeno", "Oxígeno", "Carbono"], correcta: 2 }
            ]
        };
        // Función general para búsquedas (insensible a mayúsculas y tildes)
        function normalizeText(str) {
            if (!str) return '';
            return str.normalize('NFD').replace(/[\u0300-\u036f]/g, '').toLowerCase();
        }

        function buscar(db, query, resultsDiv, resultDiv, mostrarFn) {
            const q = query || '';
            if (q.length < 2) {
                resultDiv.innerHTML = '<p class="error-message">Ingrese al menos 2 letras.</p>';
                return;
            }
            const qNorm = normalizeText(q);
            const encontrados = Object.keys(db).filter(key => {
                const keyNorm = normalizeText(key);
                const nameNorm = normalizeText(db[key] && db[key].nombre ? db[key].nombre : '');
                return keyNorm.includes(qNorm) || nameNorm.includes(qNorm);
            });
            if (encontrados.length > 0) {
                encontrados.forEach(key => {
                    const div = document.createElement('div');
                    div.className = 'search-item';
                    div.textContent = (db[key] && db[key].nombre) ? db[key].nombre : (key.charAt(0).toUpperCase() + key.slice(1));
                    div.addEventListener('click', () => mostrarFn(key));
                    resultsDiv.appendChild(div);
                });
            } else {
                resultDiv.innerHTML = '<p class="error-message">No encontrado.</p>';
            }
        }
        // Para animales
        const animalSearch = document.getElementById('animalSearch');
        const searchButton = document.getElementById('searchButton');
        const searchResults = document.getElementById('searchResults');
        const resultDiv = document.getElementById('result');
        function mostrarInformacion(nombreAnimal) {
            const animal = animalDatabase[nombreAnimal];
            searchResults.innerHTML = '';
            const htmlContent = `
                <div class="info-card">
                    <img src="https://source.unsplash.com/400x300/?${nombreAnimal}" alt="${animal.nombre}" class="animal-image">
                    <h2 style="color: #ffc837; text-align: center; margin-top: 10px;">${animal.nombre}</h2>
                    <p><strong>Tipo:</strong> ${animal.tipo}</p>
                    <p><strong>Info:</strong> ${animal.info}</p>
                    <p><strong>Alimentación:</strong> ${animal.alimentacion}</p>
                    <p><strong>Habitat:</strong> ${animal.habitat}</p>
                    <p><strong>Curiosidades:</strong> ${animal.curiosidades}</p>
                    <div class="animal-details">
                        <div class="animal-detail-card">
                            <h4>Taxonomía</h4>
                            <p><strong>Reino:</strong> ${animal.taxonomia.reino}</p>
                            <p><strong>Clase:</strong> ${animal.taxonomia.clase}</p>
                        </div>
                    </div>
                </div>
            `;
            resultDiv.innerHTML = htmlContent;
        }
        searchButton.addEventListener('click', () => {
            const query = animalSearch.value.toLowerCase().trim();
            resultDiv.innerHTML = '';
            searchResults.innerHTML = '';
            buscar(animalDatabase, query, searchResults, resultDiv, mostrarInformacion);
        });
        animalSearch.addEventListener('keyup', (event) => {
            if (event.key === 'Enter') {
                const query = animalSearch.value.toLowerCase().trim();
                resultDiv.innerHTML = '';
                searchResults.innerHTML = '';
                buscar(animalDatabase, query, searchResults, resultDiv, mostrarInformacion);
            }
        });
        // Para geografía
        const geoSearch = document.getElementById('geoSearch');
        const geoSearchButton = document.getElementById('geoSearchButton');
        const geoResults = document.getElementById('geoResults');
        const geoResultDiv = document.getElementById('geoResult');
        function mostrarInformacionGeo(key) {
            const item = geoDatabase[key];
            geoResults.innerHTML = '';
            const html = `
                <div class="info-card">
                    <img src="https://source.unsplash.com/600x360/?${encodeURIComponent(item.nombre)}" alt="${item.nombre}" class="animal-image">
                    <h2 style="color:#ffc837; text-align:center; margin-top:10px;">${item.nombre}</h2>
                    <p><strong>Capital:</strong> ${item.capital}</p>
                    <p><strong>Continente:</strong> ${item.continente}</p>
                    <p><strong>Población:</strong> ${item.poblacion}</p>
                    <p><strong>Descripción:</strong> ${item.info}</p>
                    <p><strong>Curiosidades:</strong> ${item.curiosidades}</p>
                </div>
            `;
            geoResultDiv.innerHTML = html;
        }
        geoSearchButton.addEventListener('click', () => {
            const query = geoSearch.value.toLowerCase().trim();
            geoResultDiv.innerHTML = '';
            geoResults.innerHTML = '';
            buscar(geoDatabase, query, geoResults, geoResultDiv, mostrarInformacionGeo);
        });
        geoSearch.addEventListener('keyup', (e) => { if (e.key === 'Enter') {
            const query = geoSearch.value.toLowerCase().trim();
            geoResultDiv.innerHTML = '';
            geoResults.innerHTML = '';
            buscar(geoDatabase, query, geoResults, geoResultDiv, mostrarInformacionGeo);
        } });
        // Para espacio
        const infoPlanetaDiv = document.getElementById('info-planeta');
        function mostrarInfoPlaneta(planeta) {
            const info = infoPlanetas[planeta];
            const datosHTML = Object.entries(info.datos).map(([key, value]) => `
                <div class="space-dato">
                    <h4>${info.icono} ${key}</h4>
                    <p>${value}</p>
                </div>
            `).join('');
            infoPlanetaDiv.innerHTML = `
                <h3>${info.nombre}</h3>
                <p class="descripcion">${info.info}</p>
                <div class="space-datos">${datosHTML}</div>
            `;
        }
        // Para lengua
        const langSearch = document.getElementById('langSearch');
        const langSearchButton = document.getElementById('langSearchButton');
        const langResults = document.getElementById('langResults');
        const langResultDiv = document.getElementById('langResult');
        function mostrarInformacionLang(key) {
            const item = langDatabase[key];
            langResults.innerHTML = '';
            const html = `
                <div class="info-card">
                    <h2 style="color:#ffc837; text-align:center;">${item.nombre}</h2>
                    <p><strong>Info:</strong> ${item.info}</p>
                    <p><strong>Obras:</strong> ${item.obras}</p>
                </div>
            `;
            langResultDiv.innerHTML = html;
        }
        langSearchButton.addEventListener('click', () => {
            const query = langSearch.value.toLowerCase().trim();
            langResultDiv.innerHTML = '';
            langResults.innerHTML = '';
            buscar(langDatabase, query, langResults, langResultDiv, mostrarInformacionLang);
        });
        langSearch.addEventListener('keyup', (e) => { if (e.key === 'Enter') {
            const query = langSearch.value.toLowerCase().trim();
            langResultDiv.innerHTML = '';
            langResults.innerHTML = '';
            buscar(langDatabase, query, langResults, langResultDiv, mostrarInformacionLang);
        } });
        // Para física
        const physSearch = document.getElementById('physSearch');
        const physSearchButton = document.getElementById('physSearchButton');
        const physResults = document.getElementById('physResults');
        const physResultDiv = document.getElementById('physResult');
        function mostrarInformacionPhys(key) {
            const item = physDatabase[key];
            physResults.innerHTML = '';
            const html = `
                <div class="info-card">
                    <h2 style="color:#ffc837; text-align:center;">${item.nombre}</h2>
                    <p><strong>Número Atómico:</strong> ${item.numero_atomico}</p>
                    <p><strong>Masa Atómica:</strong> ${item.masa_atomica}</p>
                    <p><strong>Info:</strong> ${item.info}</p>
                </div>
            `;
            physResultDiv.innerHTML = html;
        }
        physSearchButton.addEventListener('click', () => {
            const query = physSearch.value.toLowerCase().trim();
            physResultDiv.innerHTML = '';
            physResults.innerHTML = '';
            buscar(physDatabase, query, physResults, physResultDiv, mostrarInformacionPhys);
        });
        physSearch.addEventListener('keyup', (e) => { if (e.key === 'Enter') {
            const query = physSearch.value.toLowerCase().trim();
            physResultDiv.innerHTML = '';
            physResults.innerHTML = '';
            buscar(physDatabase, query, physResults, physResultDiv, mostrarInformacionPhys);
        } });
        // Para quizzes
        const quizTabButtons = document.querySelectorAll('#quizzes .tab-button');
        const quizResultDiv = document.getElementById('quizResult');
        let currentQuiz = null;
        let currentQuizArea = null;
        let quizIndex = 0;
        let score = 0;
        function showQuiz(area) {
            quizTabButtons.forEach(button => button.classList.remove('active'));
            quizTabButtons.forEach(button => {
                if (button.getAttribute('onclick').includes(area)) button.classList.add('active');
            });
            currentQuiz = quizzes[area];
            currentQuizArea = area;
            quizIndex = 0;
            score = 0;
            renderQuizQuestion();
        }
        function renderQuizQuestion() {
            if (quizIndex >= currentQuiz.length) {
                quizResultDiv.innerHTML = `<p class="quiz-result">Puntuación: ${score} / ${currentQuiz.length}</p>`;
                handleQuizCompletion();
                return;
            }
            const q = currentQuiz[quizIndex];
            const optionsHTML = q.opciones.map((opt, i) => `
                <div class="quiz-option" onclick="checkAnswer(${i})">${opt}</div>
            `).join('');
            quizResultDiv.innerHTML = `
                <div class="quiz-question">
                    <h3>${q.pregunta}</h3>
                    ${optionsHTML}
                </div>
            `;
        }
        function checkAnswer(selected) {
            if (selected === currentQuiz[quizIndex].correcta) score++;
            quizIndex++;
            renderQuizQuestion();
        }

        function handleQuizCompletion() {
            const user = getRegisteredUser();
            const total = currentQuiz ? currentQuiz.length : 0;
            if (user) {
                const submission = {
                    name: user.nombre,
                    edad: user.edad,
                    grado: user.grado,
                    area: currentQuizArea,
                    score: score,
                    total: total,
                    timestamp: new Date().toISOString()
                };
                addSubmission(submission);
                renderAdminPanel();
                const status = document.getElementById('regStatus');
                if (status) status.innerText = `Resultado enviado al panel admin: ${score}/${total}`;
            } else {
                const status = document.getElementById('regStatus');
                if (status) status.innerText = `Has obtenido ${score}/${total} — regístrate para enviar resultados al admin.`;
            }
        }

        function registerUser() {
            const nombre = (document.getElementById('regNombre')||{}).value || '';
            const edad = (document.getElementById('regEdad')||{}).value || '';
            const grado = (document.getElementById('regGrado')||{}).value || '';
            if (!nombre.trim() || !edad || !grado.trim()) {
                const status = document.getElementById('regStatus');
                if (status) { status.style.color = '#a00'; status.innerText = 'Completa todos los campos para registrar.'; }
                return;
            }
            const user = { nombre: nombre.trim(), edad: parseInt(edad), grado: grado.trim(), registeredAt: new Date().toISOString() };
            localStorage.setItem(REG_USER_KEY, JSON.stringify(user));
            // add to users list
            const list = JSON.parse(localStorage.getItem(REG_USERS_LIST_KEY) || '[]');
            list.push(user);
            localStorage.setItem(REG_USERS_LIST_KEY, JSON.stringify(list));
            const status = document.getElementById('regStatus');
            if (status) { status.style.color = '#0a0'; status.innerText = 'Registro guardado. Tus resultados se enviarán al admin.'; }
            renderAdminPanel();
        }

        function clearRegistration() {
            localStorage.removeItem(REG_USER_KEY);
            const status = document.getElementById('regStatus');
            if (status) { status.style.color = '#444'; status.innerText = 'Sesión cerrada. Ya no se enviarán resultados.'; }
        }

        function getRegisteredUser() {
            try { return JSON.parse(localStorage.getItem(REG_USER_KEY)); } catch(e) { return null; }
        }

        function addSubmission(sub) {
            const arr = JSON.parse(localStorage.getItem(QUIZ_SUBMISSIONS_KEY) || '[]');
            arr.unshift(sub);
            localStorage.setItem(QUIZ_SUBMISSIONS_KEY, JSON.stringify(arr));
        }

        function renderAdminPanel() {
            // users
            const usersDiv = document.getElementById('adminUsers');
            const users = JSON.parse(localStorage.getItem(REG_USERS_LIST_KEY) || '[]');
            if (usersDiv) {
                if (users.length === 0) usersDiv.innerHTML = '<em>No hay usuarios registrados.</em>';
                else usersDiv.innerHTML = users.map(u => `<div style="padding:6px;border-bottom:1px solid #eee">${u.nombre} — ${u.edad} años — ${u.grado}</div>`).join('');
            }
            // submissions
            const subsDiv = document.getElementById('adminSubmissions');
            const subs = JSON.parse(localStorage.getItem(QUIZ_SUBMISSIONS_KEY) || '[]');
            if (subsDiv) {
                if (subs.length === 0) subsDiv.innerHTML = '<em>No hay resultados enviados.</em>';
                else subsDiv.innerHTML = subs.map(s => `<div style="padding:6px;border-bottom:1px solid #eee"><strong>${s.name}</strong> (${s.edad} - ${s.grado}) — <em>${s.area}</em> — ${s.score}/${s.total} <br><small>${new Date(s.timestamp).toLocaleString()}</small></div>`).join('');
            }
        }

        // Inicializar vista admin al cargar
        document.addEventListener('DOMContentLoaded', () => {
            renderAdminPanel();
        });
        // Juego de Matemáticas
        let puntuacion = 0;
        let record = localStorage.getItem('recordMatematicas') || 0;
        let respuestaCorrecta;
        const mensajesCorrectos = ["¡Genial!", "¡Excelente!", "¡Eres un crack!", "¡Sigue así!", "¡Perfecto!"];
        const mensajesIncorrectos = ["¡Casi!", "¡Mejor la próxima!", "¡Ups!", "¡No pasa nada!"];

        document.getElementById('record').innerText = 'Récord: ' + record;

        function reproducirSonido(id) {
            const audio = document.getElementById(id);
            if (audio) {
                audio.currentTime = 0;
                audio.play().catch(() => {});
            }
        }

        function confeti() {
            confetti({ particleCount: 120, spread: 70, origin: { y: 0.6 } });
        }

        function generarPregunta() {
            const ops = ['+', '-', '×', '÷'];
            const op = ops[Math.floor(Math.random() * ops.length)];
            let a = Math.floor(Math.random() * 30) + 1;
            let b = Math.floor(Math.random() * 20) + 1;

            if (op === '÷') { a = b * (Math.floor(Math.random() * 10) + 1); }
            if (op === '-') { if (a < b) [a, b] = [b, a]; }

            let correcta;
            switch(op) {
                case '+': correcta = a + b; break;
                case '-': correcta = a - b; break;
                case '×': correcta = a * b; break;
                case '÷': correcta = (a / b).toFixed(1); correcta = parseFloat(correcta); break;
            }

            document.getElementById('pregunta').innerText = `${a} ${op} ${b} = ?`;
            respuestaCorrecta = correcta;

            let opciones = [correcta];
            while (opciones.length < 4) {
                let falsa = correcta + Math.floor(Math.random() * 20 - 10);
                if (falsa > 0 && !opciones.includes(falsa)) opciones.push(falsa);
            }
            opciones.sort(() => Math.random() - 0.5);

            const botones = document.querySelectorAll('.boton');
            botones.forEach((btn, i) => {
                btn.innerText = opciones[i];
                btn.classList.remove('correcto', 'incorrecto');
                btn.disabled = false;
                btn.onclick = () => responder(opciones[i], btn);
            });

            document.getElementById('resultado').innerHTML = '';
            actualizarBarra();
        }

        function responder(res, boton) {
            document.querySelectorAll('.boton').forEach(b => b.disabled = true);

            if (res === respuestaCorrecta) {
                boton.classList.add('correcto');
                const msg = mensajesCorrectos[Math.floor(Math.random() * mensajesCorrectos.length)];
                document.getElementById('resultado').innerHTML = `<span style="color:#28a745;">${msg} ✓</span>`;
                confeti();
                puntuacion++;
                if (puntuacion > record) {
                    record = puntuacion;
                    localStorage.setItem('recordMatematicas', record);
                    document.getElementById('record').innerText = '¡Nuevo récord: ' + record + '! 🎉';
                }
            } else {
                boton.classList.add('incorrecto');
                const msg = mensajesIncorrectos[Math.floor(Math.random() * mensajesIncorrectos.length)];
                document.getElementById('resultado').innerHTML = `<span style="color:#dc3545;">${msg} ✗<br>La respuesta era ${respuestaCorrecta}</span>`;
                puntuacion = 0;
            }

            document.getElementById('puntuacion').innerText = 'Puntuación: ' + puntuacion;
            actualizarBarra();
        }

        function actualizarBarra() {
            const porcentaje = Math.min(puntuacion * 8, 100);
            document.getElementById('barra').style.width = porcentaje + '%';
        }

        function nuevaPregunta() {
            generarPregunta();
        }

        // Buscador de fórmulas
        document.getElementById('buscarFormula').addEventListener('input', function() {
            const texto = this.value.toLowerCase().trim();
            document.querySelectorAll('.formula').forEach(formula => {
                const nombre = formula.getAttribute('data-nombre').toLowerCase();
                if (texto === '' || nombre.includes(texto)) {
                    formula.classList.remove('oculta');
                } else {
                    formula.classList.add('oculta');
                }
            });
        });

        // Iniciar juego al cargar la sección
        document.querySelector('[onclick="showSection(\'matematicas\')"]').addEventListener('click', () => {
            setTimeout(generarPregunta, 300);
        });

        // Iniciar la primera pregunta al cargar la página si es la sección activa
        if (document.getElementById('matematicas').classList.contains('active')) {
            generarPregunta();
        }
    </script>
</body>
</html>

