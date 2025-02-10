<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Angie querés ser mi San Valentín</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?love,romantic') no-repeat center center fixed;
            background-size: cover;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            position: relative;
        }
        h1 {
            color: #ff3366;
            background: rgba(255, 255, 255, 0.8);
            padding: 10px;
            border-radius: 10px;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        .yes {
            background-color: #ff3366;
            color: white;
        }
        .no {
            background-color: #ccc;
            color: black;
            position: absolute;
        }
        .heart, .bear {
            position: absolute;
            font-size: 50px;
            animation: float 2s infinite ease-in-out;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            50% { transform: translateY(-20px); opacity: 0.7; }
            100% { transform: translateY(-40px); opacity: 0; }
        }
    </style>
    <script>
        function moveNoButton() {
            let noButton = document.getElementById("no");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            noButton.style.left = `${x}px`;
            noButton.style.top = `${y}px`;
        }
        function showLoveMessage() {
            document.body.innerHTML = '<h1>Sabía que ibas a decir que sí amor 💖</h1><p style="font-size: 18px;">Aunque a veces me hacés estresar y no me entendés te amo che 💕</p>';
            document.body.style.background = "url('/mnt/data/WhatsApp Image 2025-02-08 at 17.40.51.jpeg') no-repeat center center fixed";
            document.body.style.backgroundSize = "cover";
            for (let i = 0; i < 50; i++) {
                let heart = document.createElement("div");
                heart.innerHTML = "❤️";
                heart.className = "heart";
                heart.style.left = Math.random() * window.innerWidth + "px";
                heart.style.top = Math.random() * window.innerHeight + "px";
                heart.style.animationDuration = Math.random() * 3 + 1 + "s";
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 3000);
            }
            for (let i = 0; i < 10; i++) {
                let bear = document.createElement("div");
                bear.innerHTML = "🐻";
                bear.className = "bear";
                bear.style.left = Math.random() * window.innerWidth + "px";
                bear.style.top = Math.random() * window.innerHeight + "px";
                bear.style.animationDuration = Math.random() * 3 + 1 + "s";
                document.body.appendChild(bear);
                setTimeout(() => bear.remove(), 3000);
            }
        }
    </script>
</head>
<body>
    <h1>Angie querés ser mi San Valentín 💘</h1>
    <div class="buttons">
        <button class="yes" onclick="showLoveMessage()">Obvio mi amor 💕</button>
        <button class="no" id="no" onmouseover="moveNoButton()">Ni loco 😢</button>
    </div>
</body>
</html>
