<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nuestra Historia</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f7f1e3;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
            width: 80%;
            max-width: 800px;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .story {
            display: none;
        }

        .story.active {
            display: block;
        }

        button {
            padding: 10px 20px;
            background-color: #ff6b81;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #ff4757;
        }

        h1 {
            color: #ff6b81;
        }

        p {
            font-size: 18px;
            line-height: 1.6;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="story active" id="page1">
        <h1>Nuestra Historia</h1>
        <p>Desde el principio, sabíamos que lo nuestro era especial. Cada sonrisa, cada mirada, hacía que el tiempo se detuviera.</p>
        <button onclick="nextPage(2)">Siguiente</button>
    </div>

    <div class="story" id="page2">
        <h1>Los Retos</h1>
        <p>No todo fue fácil. Los obstáculos aparecieron en nuestro camino, y a veces pensamos en rendirnos. El dolor y la incertidumbre nos desafiaron constantemente.</p>
        <button onclick="nextPage(3)">Siguiente</button>
    </div>

    <div class="story" id="page3">
        <h1>La Fuerza del Amor</h1>
        <p>Pero el amor que sentíamos el uno por el otro fue más fuerte que cualquier dificultad. Encontramos en nosotros mismos la fuerza para seguir adelante, juntos.</p>
        <button onclick="nextPage(4)">Siguiente</button>
    </div>

    <div class="story" id="page4">
        <h1>Superando la Adversidad</h1>
        <p>Cada reto que superamos nos unió más. Aprendimos a confiar, a apoyarnos y a nunca perder la esperanza. Juntos, superamos lo que parecía imposible.</p>
        <button onclick="nextPage(5)">Siguiente</button>
    </div>

    <div class="story" id="page5">
        <h1>Siempre te elegiría a ti</h1>
        <p>Al final, después de todo lo vivido, si tuviera que volver a elegir, siempre te elegiría a ti. Eres mi razón, mi fuerza y mi amor eterno.</p>
    </div>
</div>

<script>
    function nextPage(page) {
        document.querySelectorAll('.story').forEach(function (el) {
            el.classList.remove('active');
        });
        document.getElementById('page' + page).classList.add('active');
    }
</script>

</body>
</html>
