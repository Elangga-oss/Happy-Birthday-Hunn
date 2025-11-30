<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surprise untuk Wan Natasya Nabila</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fecfef, #ffecd2);
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .container {
            max-width: 600px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            animation: fadeIn 2s ease-in-out;
        }
        h1 {
            font-size: 2.5em;
            color: #e91e63;
            margin-bottom: 20px;
        }
        p {
            font-size: 1.2em;
            line-height: 1.6;
            margin: 20px 0;
        }
        .surprise-btn {
            background: #4caf50;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            border-radius: 10px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .surprise-btn:hover {
            background: #45a049;
        }
        .hidden {
            display: none;
        }
        .reveal {
            animation: slideUp 1s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
        .heart {
            position: absolute;
            color: #ff4081;
            font-size: 2em;
            animation: float 3s infinite ease-in-out;
        }
        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="hearts" id="hearts"></div>
    <div class="container">
        <h1>Happy Birthday, Wan Natasya Nabila! 🎉</h1>
        <p>Klik tombol di bawah untuk membuka surprise spesial dariku, pacarmu yang selalu mencintaimu. #masdiki</p>
        <button class="surprise-btn" onclick="revealSurprise()">Buka Surprise!</button>
        <div id="surprise" class="hidden">
            <h2>Surprise! 💖</h2>
            <p>Wan Natasya Nabila, hari ini adalah hari spesialmu. Kamu adalah cahaya dalam hidupku, sumber kebahagiaanku, dan cinta sejati yang membuat dunia ini lebih indah. Setiap detik bersamamu adalah hadiah yang tak ternilai. Terima kasih telah menjadi pacarku, temanku, dan inspirasiku. Semoga tahun ini penuh dengan kebahagiaan, kesehatan, dan impian yang tercapai. Aku mencintaimu lebih dari kata-kata bisa ungkapkan. Selamat ulang tahun, sayang! 🌟</p>
            <p>Dengan cinta abadi,<br>Teman Pacarmu #masdiki</p>
        </div>
    </div>

    <script>
        function revealSurprise() {
            document.getElementById('surprise').classList.remove('hidden');
            document.getElementById('surprise').classList.add('reveal');
            createHearts();
        }

        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            for (let i = 0; i < 20; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDelay = Math.random() * 3 + 's';
                heartsContainer.appendChild(heart);
                setTimeout(() => heart.remove(), 3000);
            }
        }
    </script>
</body>
</html>
