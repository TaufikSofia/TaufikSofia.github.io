<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Untuk Pacarku ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #ffafbd, #ffc3a0);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            width: 100%;
            max-width: 800px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            position: relative;
        }
        
        .page {
            padding: 40px;
            display: none;
        }
        
        .active {
            display: block;
            animation: fadeIn 0.8s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        h1 {
            color: #e84393;
            text-align: center;
            margin-bottom: 30px;
            font-size: 2.2rem;
        }
        
        h2 {
            color: #fd79a8;
            text-align: center;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .question-container {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .question {
            font-size: 1.5rem;
            color: #e84393;
            margin-bottom: 15px;
        }
        
        .options {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .btn {
            padding: 12px 25px;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .yes-btn {
            background-color: #fd79a8;
            color: white;
            box-shadow: 0 4px 15px rgba(253, 121, 168, 0.4);
        }
        
        .yes-btn:hover {
            background-color: #e84393;
            transform: translateY(-3px);
        }
        
        .no-btn {
            background-color: #636e72;
            color: white;
            box-shadow: 0 4px 15px rgba(99, 110, 114, 0.4);
        }
        
        .no-btn:hover {
            background-color: #2d3436;
            transform: translateY(-3px);
        }
        
        .pantun {
            background-color: #ffeaa7;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            font-size: 1.4rem;
            color: #e17055;
            margin: 30px 0;
            font-style: italic;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .menu-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }
        
        .menu-item {
            background: linear-gradient(135deg, #a29bfe, #74b9ff);
            border-radius: 15px;
            padding: 25px 15px;
            text-align: center;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .menu-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .menu-title {
            font-size: 1.3rem;
            font-weight: bold;
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .photo {
            width: 100%;
            height: 150px;
            border-radius: 10px;
            object-fit: cover;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .photo:hover {
            transform: scale(1.05);
        }
        
        .music-player {
            background-color: #ffeaa7;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            margin-top: 20px;
        }
        
        .music-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
        }
        
        .music-btn {
            background-color: #fd79a8;
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .music-btn:hover {
            background-color: #e84393;
            transform: scale(1.1);
        }
        
        .destination-list {
            list-style-type: none;
            margin-top: 20px;
        }
        
        .destination-item {
            background-color: #dfe6e9;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 10px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .destination-item:hover {
            background-color: #b2bec3;
            transform: translateX(10px);
        }
        
        .destination-icon {
            color: #e84393;
            font-size: 1.5rem;
        }
        
        .letter-container {
            background: linear-gradient(135deg, #f9f9f9, #ffffff);
            padding: 40px;
            border-radius: 10px;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            border: 2px solid #fd79a8;
        }
        
        .letter-photo {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin: 0 auto 20px;
            display: block;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            border: 3px solid #fd79a8;
        }
        
        .letter-text {
            font-size: 1.2rem;
            line-height: 1.6;
            color: #333;
            text-align: justify;
        }
        
        .back-btn {
            position: absolute;
            top: 20px;
            left: 20px;
            background-color: #636e72;
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .back-btn:hover {
            background-color: #2d3436;
            transform: scale(1.1);
        }
        
        .heart {
            color: #e84393;
            animation: heartbeat 1.5s infinite;
        }
        
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        @media (max-width: 600px) {
            .menu-container {
                grid-template-columns: 1fr;
            }
            
            .gallery {
                grid-template-columns: repeat(2, 1fr);
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .page {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Halaman Pertanyaan -->
        <div id="question-page" class="page active">
            <h1>Hai Sayangku! <span class="heart">❤</span></h1>
            
            <div class="question-container">
                <div class="question">Kamu kangen aku atau tidak?</div>
                <div class="options">
                    <button class="btn yes-btn" onclick="answerQuestion(true, 'kangen')">Iya, Kangen</button>
                    <button class="btn no-btn" onmouseover="moveNoButton(this)">Tidak</button>
                </div>
                
                <div class="question">Kamu sayang aku atau tidak?</div>
                <div class="options">
                    <button class="btn yes-btn" onclick="answerQuestion(true, 'sayang')">Iya, Sayang</button>
                    <button class="btn no-btn" onmouseover="moveNoButton(this)">Tidak</button>
                </div>
            </div>
            
            <div class="pantun">
                Jeruk nipis jeruk mandarin,<br>
                Hai manis lagi ngapain?
            </div>
        </div>
        
        <!-- Halaman Menu Utama -->
        <div id="home-page" class="page">
            <button class="back-btn" onclick="showPage('question-page')">←</button>
            <h1>Menu Utama <span class="heart">❤</span></h1>
            
            <div class="menu-container">
                <div class="menu-item" onclick="showPage('photo-page')">
                    <div class="menu-icon">📸</div>
                    <div class="menu-title">Foto Kenangan</div>
                </div>
                
                <div class="menu-item" onclick="showPage('music-page')">
                    <div class="menu-icon">🎵</div>
                    <div class="menu-title">Lagu Favorit</div>
                </div>
                
                <div class="menu-item" onclick="showPage('dream-page')">
                    <div class="menu-icon">✈️</div>
                    <div class="menu-title">Cita-cita Kita</div>
                </div>
                
                <div class="menu-item" onclick="showPage('letter-page')">
                    <div class="menu-icon">💌</div>
                    <div class="menu-title">Surat Untukmu</div>
                </div>
            </div>
        </div>
        
        <!-- Halaman Foto -->
        <div id="photo-page" class="page">
            <button class="back-btn" onclick="showPage('home-page')">←</button>
            <h2>Foto Kenangan Kita <span class="heart">❤</span></h2>
            
            <div class="gallery">
                <!-- 20 foto placeholder - ganti dengan foto asli -->
                <img src="https://picsum.photos/150/150?random=1" alt="Foto Kenangan 1" class="photo">
                <img src="https://picsum.photos/150/150?random=2" alt="Foto Kenangan 2" class="photo">
                <img src="https://picsum.photos/150/150?random=3" alt="Foto Kenangan 3" class="photo">
                <img src="https://picsum.photos/150/150?random=4" alt="Foto Kenangan 4" class="photo">
                <img src="https://picsum.photos/150/150?random=5" alt="Foto Kenangan 5" class="photo">
                <img src="https://picsum.photos/150/150?random=6" alt="Foto Kenangan 6" class="photo">
                <img src="https://picsum.photos/150/150?random=7" alt="Foto Kenangan 7" class="photo">
                <img src="https://picsum.photos/150/150?random=8" alt="Foto Kenangan 8" class="photo">
                <img src="https://picsum.photos/150/150?random=9" alt="Foto Kenangan 9" class="photo">
                <img src="https://picsum.photos/150/150?random=10" alt="Foto Kenangan 10" class="photo">
                <img src="https://picsum.photos/150/150?random=11" alt="Foto Kenangan 11" class="photo">
                <img src="https://picsum.photos/150/150?random=12" alt="Foto Kenangan 12" class="photo">
                <img src="https://picsum.photos/150/150?random=13" alt="Foto Kenangan 13" class="photo">
                <img src="https://picsum.photos/150/150?random=14" alt="Foto Kenangan 14" class="photo">
                <img src="https://picsum.photos/150/150?random=15" alt="Foto Kenangan 15" class="photo">
                <img src="https://picsum.photos/150/150?random=16" alt="Foto Kenangan 16" class="photo">
                <img src="https://picsum.photos/150/150?random=17" alt="Foto Kenangan 17" class="photo">
                <img src="https://picsum.photos/150/150?random=18" alt="Foto Kenangan 18" class="photo">
                <img src="https://picsum.photos/150/150?random=19" alt="Foto Kenangan 19" class="photo">
                <img src="https://picsum.photos/150/150?random=20" alt="Foto Kenangan 20" class="photo">
            </div>
        </div>
        
        <!-- Halaman Musik -->
        <div id="music-page" class="page">
            <button class="back-btn" onclick="showPage('home-page')">←</button>
            <h2>Lagu Favorit Kita <span class="heart">❤</span></h2>
            
            <div class="music-player">
                <h3>Lagu Khusus Untuk Kita</h3>
                <div class="music-controls">
                    <button class="music-btn" onclick="playMusic()">▶️</button>
                    <button class="music-btn" onclick="pauseMusic()">⏸️</button>
                    <button class="music-btn" onclick="stopMusic()">⏹️</button>
                </div>
                <audio id="bg-music" loop>
                    <!-- Ganti dengan URL lagu favorit kalian -->
                    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
                    Browser Anda tidak mendukung elemen audio.
                </audio>
            </div>
        </div>
        
        <!-- Halaman Cita-cita -->
        <div id="dream-page" class="page">
            <button class="back-btn" onclick="showPage('home-page')">←</button>
            <h2>Cita-cita Kita <span class="heart">❤</span></h2>
            
            <ul class="destination-list">
                <li class="destination-item"><span class="destination-icon">🕋</span> Mekkah, Arab Saudi</li>
                <li class="destination-item"><span class="destination-icon">🕌</span> Madinah, Arab Saudi</li>
                <li class="destination-item"><span class="destination-icon">🎈</span> Turki</li>
                <li class="destination-item"><span class="destination-icon">🏔️</span> Swiss</li>
                <li class="destination-item"><span class="destination-icon">⛰️</span> Switzerland</li>
                <li class="destination-item"><span class="destination-icon">🐫</span> Mesir</li>
                <li class="destination-item"><span class="destination-icon">💃</span> Spanyol</li>
            </ul>
        </div>
        
        <!-- Halaman Surat -->
        <div id="letter-page" class="page">
            <button class="back-btn" onclick="showPage('home-page')">←</button>
            <h2>Surat Untukmu <span class="heart">❤</span></h2>
            
            <div class="letter-container">
                <!-- Ganti dengan foto kalian berdua -->
                <img src="https://picsum.photos/200/200?random=21" alt="Foto Kita" class="letter-photo">
                
                <div class="letter-text">
                    Sayangku yang tersayang,<br><br>
                    
                    Setiap hari bersamamu adalah anugerah terindah dalam hidupku. Aku bersyukur memiliki seseorang seperti kamu yang selalu membuatku tersenyum, bahkan di hari-hari terberat sekalipun.<br><br>
                    
                    Aku berjanji akan selalu ada untukmu, dalam suka dan duka. Aku akan menjadi pelindungmu, teman terbaikmu, dan orang yang paling mencintaimu sepanjang hidupku.<br><br>
                    
                    Terima kasih sudah menjadi bagian dari hidupku. Aku tak sabar untuk menjelajahi dunia bersamamu dan mewujudkan semua impian kita.<br><br>
                    
                    Selamanya milikmu,<br>
                    <span style="font-weight: bold; color: #e84393;">[Nama Kamu]</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        let answers = {
            kangen: false,
            sayang: false
        };
        
        function answerQuestion(answer, type) {
            answers[type] = answer;
            
            // Jika kedua pertanyaan sudah dijawab dengan "Iya"
            if (answers.kangen && answers.sayang) {
                setTimeout(() => {
                    showPage('home-page');
                }, 500);
            }
        }
        
        function moveNoButton(button) {
            // Menggerakkan tombol "Tidak" secara acak saat dihover
            const x = Math.random() * 200 - 100;
            const y = Math.random() * 100 - 50;
            button.style.transform = `translate(${x}px, ${y}px)`;
        }
        
        function showPage(pageId) {
            // Menyembunyikan semua halaman
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Menampilkan halaman yang dipilih
            document.getElementById(pageId).classList.add('active');
            
            // Jika pindah ke halaman musik, otomatis memutar musik
            if (pageId === 'music-page') {
                playMusic();
            } else {
                pauseMusic();
            }
        }
        
        function playMusic() {
            document.getElementById('bg-music').play();
        }
        
        function pauseMusic() {
            document.getElementById('bg-music').pause();
        }
        
        function stopMusic() {
            const music = document.getElementById('bg-music');
            music.pause();
            music.currentTime = 0;
        }
    </script>
</body>
</html>
