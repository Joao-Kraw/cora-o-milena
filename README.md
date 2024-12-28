<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EU TE AMO, FELIZ ANIVERSÁRIO MOCRÉIA</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #ffe6f2;
            overflow: hidden;
            font-family: 'Arial', sans-serif;
        }

        h1 {
            color: red;
            font-size: 4rem;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        }

        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: red;
            transform: rotate(-45deg);
            animation: float 5s infinite ease-in-out;
        }

        .heart::before,
        .heart::after {
            content: "";
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: red;
            border-radius: 50%;
        }

        .heart::before {
            top: -25px;
            left: 0;
        }

        .heart::after {
            left: 25px;
            top: 0;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(-45deg);
                opacity: 1;
            }
            100% {
                transform: translateY(0) rotate(-45deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <h1>EU TE AMO, FELIZ ANIVERSÁRIO MOCRÉIA!!!</h1>
    <div class="hearts"></div>

    <script>
        function createHeart() {
            const heartsContainer = document.querySelector('.hearts');
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = 2 + Math.random() * 3 + 's';
            heartsContainer.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        setInterval(createHeart, 300);
    </script>
</body>
</html>

