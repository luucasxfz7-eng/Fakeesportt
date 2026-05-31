# Fakeesportt
FAKE ESPORT  HOME
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAKE Esport - Team Official</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0e27;
            color: white;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
        }

        /* Navegación */
        nav {
            background: #c00000;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(192, 0, 0, 0.5);
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
            gap: 30px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
            cursor: pointer;
        }

        nav a:hover {
            color: #ffd700;
            text-shadow: 0 0 10px #ffd700;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #c00000 0%, #8b0000 100%);
            padding: 60px 20px;
            text-align: center;
            border-bottom: 3px solid #ffd700;
        }

        header h1 {
            font-size: 3.5em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8);
            margin-bottom: 10px;
            letter-spacing: 3px;
        }

        header p {
            font-size: 1.2em;
            color: #ffd700;
        }

        /* Secciones */
        section {
            display: none;
            padding: 40px 20px;
            min-height: 600px;
        }

        section.active {
            display: block;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Roster */
        .jugadores {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .card {
            background: linear-gradient(135deg, #1a1f3a 0%, #0f1629 100%);
            border: 2px solid #c00000;
            width: 220px;
            text-align: center;
            border-radius: 10px;
            padding: 15px;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(192, 0, 0, 0.5);
            border-color: #ffd700;
        }

        .card img {
            width: 100%;
            height: 200px;
            border-radius: 10px;
            object-fit: cover;
            margin-bottom: 10px;
        }

        .card h2 {
            color: #ffd700;
            margin-bottom: 5px;
        }

        .card p {
            color: #c00000;
            font-weight: bold;
            font-size: 1.1em;
        }

        /* Sobre Nosotros */
        .about-content {
            max-width: 900px;
            margin: 0 auto;
            background: #1a1f3a;
            padding: 30px;
            border-radius: 10px;
            border-left: 4px solid #c00000;
        }

        .about-content h2 {
            color: #ffd700;
            margin-bottom: 20px;
            font-size: 2em;
        }

        .about-content p {
            margin-bottom: 15px;
            line-height: 1.8;
        }

        /* Resultados */
        .matches {
            max-width: 900px;
            margin: 0 auto;
        }

        .match {
            background: #1a1f3a;
            border: 2px solid #c00000;
            padding: 20px;
            margin-bottom: 15px;
            border-radius: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: 0.3s;
        }

        .match:hover {
            box-shadow: 0 5px 20px rgba(192, 0, 0, 0.3);
        }

        .team {
            flex: 1;
            text-align: center;
        }

        .score {
            flex: 1;
            text-align: center;
            font-size: 1.5em;
            color: #ffd700;
            font-weight: bold;
        }

        .match-status {
            color: #c00000;
            font-size: 0.9em;
        }

        /* Galería */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .gallery-item {
            background: #1a1f3a;
            border: 2px solid #c00000;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
            cursor: pointer;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(192, 0, 0, 0.5);
        }

        .gallery-item img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .gallery-item p {
            padding: 15px;
            color: #ffd700;
            text-align: center;
        }

        /* Contacto */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: #1a1f3a;
            padding: 30px;
            border-radius: 10px;
            border: 2px solid #c00000;
        }

        .contact-form h2 {
            color: #ffd700;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #ffd700;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            background: #0a0e27;
            border: 1px solid #c00000;
            color: white;
            border-radius: 5px;
            font-family: Arial;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ffd700;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }

        .submit-btn {
            background: #c00000;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            width: 100%;
        }

        .submit-btn:hover {
            background: #8b0000;
            box-shadow: 0 5px 15px rgba(192, 0, 0, 0.5);
        }

        /* Footer */
        footer {
            background: #0a0e27;
            border-top: 2px solid #c00000;
            padding: 20px;
            text-align: center;
            color: #ffd700;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }

            nav ul {
                gap: 15px;
            }

            .jugadores {
                gap: 15px;
            }

            .card {
                width: 180px;
            }

            .match {
                flex-direction: column;
                gap: 15px;
            }
        }
    </style>
</head>
<body>

<nav>
    <ul>
        <li><a onclick="mostrarSeccion('inicio')">Inicio</a></li>
        <li><a onclick="mostrarSeccion('sobre')">Sobre Nosotros</a></li>
        <li><a onclick="mostrarSeccion('resultados')">Resultados</a></li>
        <li><a onclick="mostrarSeccion('galeria')">Galería</a></li>
        <li><a onclick="mostrarSeccion('contacto')">Contacto</a></li>
    </ul>
</nav>

<header>
    <h1>⚡ FAKE ESPORT ⚡</h1>
    <p>El equipo más competitivo de esports</p>
</header>

<!-- INICIO -->
<section id="inicio" class="active">
    <h2 style="text-align: center; color: #ffd700; margin-bottom: 30px; font-size: 2em;">Nuestro Equipo</h2>
    <div class="jugadores">
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Lucas" alt="Lucas">
            <h2>FAKE Lucas</h2>
            <p>L1</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Luciano" alt="Luciano">
            <h2>FAKE Luciano</h2>
            <p>L1</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Benja" alt="Benja">
            <h2>FAKE Benja</h2>
            <p>L2</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Silva" alt="Silva">
            <h2>FAKE Silva</h2>
            <p>L2</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Thiago" alt="Thiago">
            <h2>FAKE Thiago</h2>
            <p>Flex</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Nacho" alt="Nacho">
            <h2>FAKE Nacho</h2>
            <p>Soporte</p>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/220x200?text=Lauta" alt="Lauta">
            <h2>FAKE Lauta</h2>
            <p>Soporte</p>
        </div>
    </div>
</section>

<!-- SOBRE NOSOTROS -->
<section id="sobre">
    <div class="about-content">
        <h2>Sobre FAKE Esport</h2>
        <p>
            FAKE Esport es un equipo profesional de esports dedicado a competir en los más altos niveles del juego competitivo. 
            Nuestro equipo está formado por 7 jugadores talentosos, cada uno con habilidades únicas y experiencia en el competitivo.
        </p>
        <p>
            Con un enfoque en el trabajo en equipo, la estrategia y la mejora continua, nos esforzamos por ser los mejores. 
            Cada miembro del equipo aporta su dedicación y pasión para lograr objetivos ambiciosos.
        </p>
        <h3 style="color: #ffd700; margin-top: 25px; margin-bottom: 15px;">Nuestra Misión</h3>
        <p>
            Representar a nuestro equipo con honor, competir al más alto nivel y demostrar que el trabajo en equipo, 
            la disciplina y la dedicación son las claves del éxito en el esports profesional.
        </p>
        <h3 style="color: #ffd700; margin-top: 25px; margin-bottom: 15px;">Valores</h3>
        <p>
            ✓ Profesionalismo<br>
            ✓ Trabajo en Equipo<br>
            ✓ Excelencia<br>
            ✓ Respeto<br>
            ✓ Innovación
        </p>
    </div>
</section>

<!-- RESULTADOS -->
<section id="resultados">
    <h2 style="text-align: center; color: #ffd700; margin-bottom: 30px; font-size: 2em;">Últimos Resultados</h2>
    <div class="matches">
        <div class="match">
            <div class="team">
                <h3>FAKE Esport</h3>
                <p style="font-size: 0.9em; color: #999;">vs</p>
            </div>
            <div class="score">2 - 1</div>
            <div class="team">
                <h3>Team Alpha</h3>
                <p class="match-status">Ganado - 31/05/2026</p>
            </div>
        </div>

        <div class="match">
            <div class="team">
                <h3>FAKE Esport</h3>
                <p style="font-size: 0.9em; color: #999;">vs</p>
            </div>
            <div class="score">3 - 2</div>
            <div class="team">
                <h3>Dragon Gaming</h3>
                <p class="match-status">Ganado - 30/05/2026</p>
            </div>
        </div>

        <div class="match">
            <div class="team">
                <h3>FAKE Esport</h3>
                <p style="font-size: 0.9em; color: #999;">vs</p>
            </div>
            <div class="score">1 - 2</div>
            <div class="team">
                <h3>Pro Legends</h3>
                <p class="match-status">Perdido - 28/05/2026</p>
            </div>
        </div>

        <div class="match">
            <div class="team">
                <h3>FAKE Esport</h3>
                <p style="font-size: 0.9em; color: #999;">vs</p>
            </div>
            <div class="score">2 - 0</div>
            <div class="team">
                <h3>Shadow Team</h3>
                <p class="match-status">Ganado - 25/05/2026</p>
            </div>
        </div>
    </div>
</section>

<!-- GALERÍA -->
<section id="galeria">
    <h2 style="text-align: center; color: #ffd700; margin-bottom: 30px; font-size: 2em;">Galería</h2>
    <div class="gallery">
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=Torneo+2026" alt="Torneo">
            <p>Torneo Regional 2026</p>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=Celebración" alt="Celebración">
            <p>Celebración de Victoria</p>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=Entrenamiento" alt="Entrenamiento">
            <p>Sesión de Entrenamiento</p>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=Equipo" alt="Equipo">
            <p>Foto del Equipo</p>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=LAN+Event" alt="LAN">
            <p>Evento LAN</p>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x250?text=Streamers" alt="Stream">
            <p>Sesión en Vivo</p>
        </div>
    </div>
</section>

<!-- CONTACTO -->
<section id="contacto">
    <h2 style="text-align: center; color: #ffd700; margin-bottom: 30px; font-size: 2em;">Contáctanos</h2>
    <div class="contact-form">
        <h2>Envía tu Mensaje</h2>
        <form onsubmit="enviarMensaje(event)">
            <div class="form-group">
                <label for="nombre">Nombre</label>
                <input type="text" id="nombre" name="nombre" required>
            </div>
            <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="asunto">Asunto</label>
                <input type="text" id="asunto" name="asunto" required>
            </div>
            <div class="form-group">
                <label for="mensaje">Mensaje</label>
                <textarea id="mensaje" name="mensaje" required></textarea>
            </div>
            <button type="submit" class="submit-btn">Enviar Mensaje</button>
        </form>
    </div>
</section>

<footer>
    <p>&copy; 2026 FAKE Esport. Todos los derechos reservados.</p>
    <p>Síguenos en nuestras redes sociales</p>
</footer>

<script>
    function mostrarSeccion(id) {
        // Ocultar todas las secciones
        const secciones = document.querySelectorAll('section');
        secciones.forEach(sec => sec.classList.remove('active'));

        // Mostrar la sección seleccionada
        document.getElementById(id).classList.add('active');

        // Scroll hacia arriba
        window.scrollTo(0, 0);
    }

    function enviarMensaje(event) {
        event.preventDefault();
        const nombre = document.getElementById('nombre').value;
        alert(`¡Gracias ${nombre}! Tu mensaje ha sido enviado. Nos pondremos en contacto pronto.`);
        document.querySelector('form').reset();
    }
</script>

</body>
</html>
