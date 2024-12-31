<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy New Year 2025 - Future Computer Coaching</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            background: linear-gradient(45deg, #ff6a00, #ffcc00, #ff6600, #ff0000);
            background-size: 400% 400%;
            animation: gradient-animation 10s ease infinite;
            overflow: hidden;
        }

        @keyframes gradient-animation {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        .container {
            z-index: 2;
            position: relative;
            color: white;
        }

        h1 {
            font-size: 4em;
            margin: 20px;
            color: #fff;
            text-transform: uppercase;
            font-weight: bold;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
        }

        h2 {
            font-size: 2.5em;
            color: #ffcc00;
            margin-bottom: 20px;
        }

        p {
            font-size: 1.5em;
            color: #f0f0f0;
            margin: 10px 0;
        }

        .button {
            font-size: 1.5em;
            padding: 15px 30px;
            margin-top: 30px;
            background-color: #ff6600;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 30px;
            transition: all 0.3s ease-in-out;
        }

        .button:hover {
            background-color: #ff4500;
            transform: scale(1.1);
        }

        .fireworks {
            position: absolute;
            top: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            opacity: 0.2;
        }

        .firework {
            position: absolute;
            border-radius: 50%;
            background-color: #ffffff;
            animation: fireworks-animation 1s ease-out infinite;
        }

        @keyframes fireworks-animation {
            0% {
                transform: scale(0);
                opacity: 1;
            }
            50% {
                transform: scale(2);
                opacity: 0.8;
            }
            100% {
                transform: scale(0);
                opacity: 0;
            }
        }

        .confetti {
            position: absolute;
            background-color: #ffcc00;
            height: 8px;
            width: 8px;
            opacity: 0;
            animation: confetti-fall 3s linear infinite;
        }

        @keyframes confetti-fall {
            0% {
                transform: translateY(-50px) rotate(0deg);
                opacity: 0;
            }
            100% {
                transform: translateY(500px) rotate(360deg);
                opacity: 1;
            }
        }

    </style>
</head>
<body>

    <div class="container">
        <h1>Happy New Year 2025!</h1>
        <h2>Future Computer Coaching</h2>
        <p>We wish you a year of growth, innovation, and success in the world of technology!</p>
        <p>Let's start 2025 with new opportunities, learning, and achievements.</p>
        <button class="button" onclick="showMessage()">Join Us Today</button>
        <div id="message"></div>
    </div>

    <canvas id="fireworks" class="fireworks"></canvas>

    <script>
        // Fireworks animation logic
        const canvas = document.getElementById('fireworks');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        // Create fireworks
        function createFireworks() {
            for (let i = 0; i < 5; i++) {
                const x = Math.random() * window.innerWidth;
                const y = Math.random() * window.innerHeight;
                const size = Math.random() * 10 + 10;
                const speed = Math.random() * 2 + 2;
                const opacity = Math.random() * 0.3 + 0.3;

                const firework = {
                    x,
                    y,
                    size,
                    speed,
                    opacity,
                    angle: Math.random() * 2 * Math.PI,
                    direction: Math.random() > 0.5 ? 1 : -1,
                };

                drawFirework(firework);
            }
        }

        function drawFirework(firework) {
            const { x, y, size, speed, opacity, angle, direction } = firework;
            const dx = Math.cos(angle) * speed;
            const dy = Math.sin(angle) * speed;

            ctx.beginPath();
            ctx.arc(x, y, size, 0, 2 * Math.PI);
            ctx.fillStyle = `rgba(255, 255, 255, ${opacity})`; // Firework color
            ctx.fill();

            firework.x += dx * direction;
            firework.y += dy * direction;

            if (opacity > 0) {
                setTimeout(() => drawFirework(firework), 30);
            }
        }

        setInterval(createFireworks, 1500);

        // Confetti animation logic
        function createConfetti() {
            const confetti = document.createElement('div');
            confetti.classList.add('confetti');
            confetti.style.left = `${Math.random() * window.innerWidth}px`;
            confetti.style.animationDuration = `${Math.random() * 2 + 3}s`;
            document.body.appendChild(confetti);

            setTimeout(() => {
                confetti.remove();
            }, 5000);
        }

        setInterval(createConfetti, 100);

        // Function to show a message when button is clicked
        function showMessage() {
            const messageElement = document.getElementById('message');
            messageElement.innerHTML = `
                <p>Welcome to Future  Computer Coaching!</p>
                <p>🎉 Happy New Year 2025! 🎉</p>
<p>
May this year bring immense success and learning opportunities for all our students at Future Computer Coaching! 🌟</p>
<p>
✨ Here's to mastering new skills, achieving your dreams, and building a brighter future through technology. Let's make 2025 a year of growth, innovation, and excellence in education! 🚀</p>
            `;
            messageElement.style.color = '#FFD700';  // Golden color
            messageElement.style.fontSize = '1.5em';
            messageElement.style.marginTop = '20px';
        }

    </script>

</body>
</html>
</body>
</html>
</html>
