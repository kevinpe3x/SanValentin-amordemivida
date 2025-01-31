<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín 💖</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffccdc;
            margin: 50px;
        }
        h1 {
            color: #d63384;
        }
        .container {
            margin-top: 50px;
        }
        .btn {
            font-size: 20px;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            margin: 10px;
            border-radius: 5px;
            transition: 0.3s;
        }
        .yes {
            background-color: #ff4081;
            color: white;
        }
        .no {
            background-color: #888;
            color: white;
            position: absolute;
        }
        .message {
            display: none;
            font-size: 24px;
            margin-top: 20px;
            color: #d63384;
            font-weight: bold;
            animation: fadeIn 1s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
    </style>
</head>
<body>

    <h1>¿Quieres ser mi San Valentín? 💘</h1>

    <div class="container">
        <button class="btn yes" onclick="aceptar()">Sí 💖</button>
        <button class="btn no" onmouseover="moverNo()">No ❌</button>
    </div>

    <div class="message" id="mensaje">
        🥰 ¡Sabía que dirías que sí! Eres lo mejor que me ha pasado. 💕
    </div>

    <script>
        function aceptar() {
            document.getElementById("mensaje").style.display = "block";
        }

        function moverNo() {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            document.querySelector(".no").style.left = x + "px";
            document.querySelector(".no").style.top = y + "px";
        }
    </script>

</body>
</html>
