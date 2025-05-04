<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday My Love</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            color: #333;
            overflow-x: hidden;
        }
        
        /* Header with Animation */
        .header {
            text-align: center;
            padding: 2rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .header h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 4rem;
            color: #fff;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            margin-bottom: 1rem;
            animation: fadeInDown 1.5s ease;
        }
        
        .header p {
            font-size: 1.2rem;
            color: #fff;
            max-width: 600px;
            margin: 0 auto;
            animation: fadeIn 2s ease;
        }
        
        /* Floating Hearts Animation */
        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .heart {
            position: absolute;
            opacity: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="%23ff6b6b"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>') no-repeat center center;
            background-size: contain;
            animation: float 6s ease-in infinite;
        }
        
        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        /* Birthday Card */
        .card {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            margin-bottom: 3rem;
            transform-style: preserve-3d;
            transition: all 0.5s ease;
            animation: fadeInUp 1s ease;
        }
        
        .card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }
        
        .card h2 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: #ff6b6b;
            margin-bottom: 1rem;
            text-align: center;
        }
        
        .card p {
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
            text-align: center;
        }
        
        /* Photo Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin: 3rem 0;
        }
        
        .gallery-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            height: 250px;
            transition: all 0.3s ease;
        }
        
        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        /* Music Player */
        .music-player {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 1.5rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            text-align: center;
            margin: 2rem 0;
            animation: fadeIn 2s ease;
        }
        
        .music-player h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #ff6b6b;
            margin-bottom: 1rem;
        }
        
        .player-controls {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .player-controls button {
            background: #ff6b6b;
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .player-controls button:hover {
            background: #ff4757;
            transform: scale(1.1);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem;
            color: white;
            font-size: 1.1rem;
        }
        
        .footer p {
            margin-bottom: 0.5rem;
        }
        
        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8rem;
            color: white;
            margin-top: 1rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 3rem;
            }
            
            .card h2 {
                font-size: 2rem;
            }
            
            .gallery {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Floating Hearts Background -->
    <div class="hearts" id="hearts"></div>
    
    <!-- Header -->
    <header class="header">
        <h1>Happy Birthday My Love</h1>
        <p>Pada hari istimewa ini, aku ingin merayakanmu dan semua kebahagiaan yang kau bawa ke dalam hidupku.</p>
    </header>
    
    <div class="container">
        <!-- Birthday Card -->
        <div class="card">
            <h2>Kepada Orang Yang Paling Menakjubkan</h2>
            <p>Hari ini menandai satu tahun lagi perjalanan luar biasamu, dan aku merasa sangat beruntung menjadi bagian darinya. Senyummu mencerahkan hari-hari tergelapku, tawamu adalah melodi favoritku, dan cintamu adalah harta terbesarku.</p>
            <p>Semoga tahun ini membawa kebahagiaan tak berujung, kesuksesan dalam segala upaya, dan impian yang terwujud. Anda layak mendapatkan semua keindahan yang ditawarkan dunia ini dan lebih dari itu.</p>
            <p>Aku menghargai setiap momen bersamamu dan berharap dapat menciptakan kenangan yang tak terhitung jumlahnya bersama. Selamat ulang tahun untuk orang yang memegang hatiku.</p>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="footer">
        <p>Dengan seluruh cintaku, di hari spesialmu</p>
        <p>Semoga ulang tahunmu seindah dirimu</p>
        <div class="signature">Forever Yours</div>
    </footer>
    
    <script>
        // Floating Hearts Animation
        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const heartCount = 30;
            
            for (let i = 0; i < heartCount; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart');
                
                // Random size between 20px and 40px
                const size = Math.random() * 20 + 20;
                heart.style.width = `${size}px`;
                heart.style.height = `${size}px`;
                
                // Random position
                heart.style.left = `${Math.random() * 100}vw`;
                heart.style.top = `${Math.random() * 100}vh`;
                
                // Random animation duration between 5s and 10s
                heart.style.animationDuration = `${Math.random() * 5 + 5}s`;
                
                // Random delay
                heart.style.animationDelay = `${Math.random() * 5}s`;
                
                heartsContainer.appendChild(heart);
            }
        }

        // Initialize
        window.onload = function() {
            createHearts();
        };
    </script>
</body>
</html>