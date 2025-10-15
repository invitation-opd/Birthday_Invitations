<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lita's 30th Birthday Invitation - Black Owl Surabaya</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* ========================================================== */
        /* CSS STYLES */
        /* ========================================================== */

        :root {
            --color-black: #000000;
            --color-gold: #FFD700;
            --color-light-gold: #FFEA9F;
            --color-cream: #FFFDD0;
            --font-script: 'Great Vibes', cursive;
            --font-main: 'Poppins', sans-serif;
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--color-black);
            color: white;
            font-family: var(--font-main);
            overflow-x: hidden;
        }
        
        /* ---------------------------------------------------------- */
        /* Landing Page (Halaman Depan) */
        /* ---------------------------------------------------------- */
        #landing-page {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--color-black);
            z-index: 99; /* Pastikan di atas semua elemen lain */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: opacity 1s ease-in-out;
            text-align: center;
        }

        #landing-page .intro-text {
            color: white;
            font-size: 1.5em;
            margin-bottom: 20px;
            font-weight: 300;
        }
        
        #landing-page .intro-name {
            font-family: var(--font-script);
            font-size: 4em;
            color: var(--color-gold);
            margin-bottom: 50px;
        }

        /* Tombol Utama (Invitation) */
        .main-cta-button {
            background: var(--color-gold);
            color: var(--color-black);
            border: none;
            padding: 15px 40px;
            font-size: 1.4em;
            font-weight: 700;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            transition: background 0.3s, transform 0.2s;
        }
        .main-cta-button:hover {
            background: var(--color-light-gold);
            transform: translateY(-2px);
        }

        /* ---------------------------------------------------------- */
        /* Background Animasi */
        /* ---------------------------------------------------------- */
        .particle-bg {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; overflow: hidden; z-index: 1; background-color: var(--color-black);
        }

        .particle { position: absolute; border-radius: 50%; opacity: 0.8; animation: moveParticles linear infinite; filter: blur(0.5px); }
        @keyframes moveParticles { 0% { transform: translateY(100vh) scale(0); opacity: 0; } 20% { opacity: 0.6; } 50% { opacity: 0.9; } 80% { opacity: 0.6; } 100% { transform: translateY(-10vh) scale(1); opacity: 0; } }

        /* ---------------------------------------------------------- */
        /* Konten Utama (Tersembunyi Awalnya) */
        /* ---------------------------------------------------------- */
        .container {
            position: relative; z-index: 10; display: none; /* Awalnya disembunyikan */
            flex-direction: column; align-items: center; justify-content: center; min-height: 100vh; text-align: center; padding: 20px;
        }

        /* Sisa CSS Undangan (Frame, Teks Lita 30, Countdown, dll.) */
        .invitation-frame { background: rgba(0, 0, 0, 0.85); border: 4px solid var(--color-gold); padding: 40px 30px; max-width: 500px; width: 90%; box-shadow: 0 0 30px rgba(255, 215, 0, 0.6); border-radius: 5px; position: relative; }
        .invitation-frame::before, .invitation-frame::after { content: ''; position: absolute; background: var(--color-gold); width: 30px; height: 4px; }
        .invitation-frame::before { top: -4px; left: -4px; }
        .invitation-frame::after { top: -4px; right: -4px; }
        .invitation-frame .corner-deco { position: absolute; width: 50px; height: 50px; border: 2px solid var(--color-gold); border-radius: 20px; }
        .invitation-frame .corner-deco.top-left { top: -20px; left: -20px; border-bottom: none; border-right: none; transform: rotate(45deg); }
        .invitation-frame .corner-deco.top-right { top: -20px; right: -20px; border-bottom: none; border-left: none; transform: rotate(-45deg); }

        .header-content { margin-bottom: 30px; }
        .title-sub { font-size: 1em; letter-spacing: 2px; color: white; margin-bottom: 5px; font-weight: 300; }
        .title-name { font-family: var(--font-script); font-size: 8em; line-height: 1; color: var(--color-gold); text-shadow: 0 0 15px rgba(255, 215, 0, 0.7); margin: 0; }
        .title-age { font-size: 8em; color: white; line-height: 0.8; margin-top: -30px; font-weight: 700; }
        .details-section { margin-top: 20px; }
        .detail-item { margin: 10px 0; font-size: 1.05em; color: white; line-height: 1.4; }
        .dresscode { font-size: 1.2em; font-weight: 700; color: white; margin-top: 25px; }
        .dresscode span { color: var(--color-gold); }
        #countdown { margin: 30px 0 20px; padding: 15px 0; }
        #countdown div { display: inline-block; margin: 0 8px; }
        .time-value { display: block; font-size: 2em; font-weight: 700; color: var(--color-gold); text-shadow: 0 0 8px rgba(255, 215, 0, 0.4); }
        .time-label { font-size: 0.7em; color: white; }
        .location-section { width: 100%; margin-top: 30px; }
        .map-container { border: 2px solid var(--color-gold); height: 250px; margin-top: 15px; overflow: hidden; box-shadow: 0 0 10px rgba(255, 215, 0, 0.4); }
        .map-container iframe { width: 100%; height: 100%; border: none; }
        .cta-button { background: var(--color-gold); color: var(--color-black); border: none; padding: 10px 20px; font-size: 1em; font-weight: 700; border-radius: 5px; cursor: pointer; margin-top: 20px; text-decoration: none; display: inline-block; transition: background 0.3s, transform 0.2s; }
        .cta-button:hover { background: var(--color-light-gold); transform: translateY(-2px); }
        .rsvp-section { margin-top: 40px; padding-top: 20px; border-top: 1px dashed rgba(255, 215, 0, 0.3); }
        .rsvp-section button { margin: 5px; }
        #music-button { position: fixed; bottom: 20px; right: 20px; z-index: 100; background: rgba(255, 215, 0, 0.9); border: none; border-radius: 50%; width: 50px; height: 50px; line-height: 50px; text-align: center; font-size: 1.5em; cursor: pointer; box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3); }

        @media (max-width: 600px) { .title-name, .title-age { font-size: 5em; } .invitation-frame { padding: 30px 20px; } #landing-page .intro-name { font-size: 3em; } }
        @media (max-width: 400px) { .title-name, .title-age { font-size: 4em; } .invitation-frame { padding: 25px 15px; } }
    </style>
</head>
<body>
    
    <audio id="party-music" loop>
        <source src="[URL_FILE_LAGU_PARTY_ANDA.mp3]" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <div id="landing-page">
        <p class="intro-text">You are invited to the birthday celebration of</p>
        <h1 class="intro-name">Lita</h1>
        <button class="main-cta-button" onclick="openInvitation()">Invitation</button>
    </div>

    <div class="particle-bg" id="particle-bg"></div>

    <div class="container" id="main-invitation">
        <div class="invitation-frame">
            
            <div class="corner-deco top-left"></div>
            <div class="corner-deco top-right"></div>
            
            <div class="header-content">
                <p class="title-sub">Birthday Invitation</p>
                <h1 class="title-name">Lita</h1>
                <h2 class="title-age">30</h2>
            </div>

            <div class="details-section">
                <p style="margin-top:0; font-size: 0.9em; color: rgba(255,255,255,0.9);">
                    We are thrilled to invite you to celebrate this special day!
                </p>
                
                <div class="detail-item">
                    Saturday, October 28, 2025
                </div>

                <div class="detail-item">
                    7.00 PM WIB - Finish
                </div>
                
                <div class="detail-item">
                    Black Owl Surabaya
                    <br>
                    <span style="font-size:0.8em; opacity:0.8;">[Full Address of Black Owl Surabaya]</span>
                </div>

                <p class="dresscode">Dresscode: <span>BLACK GOLD</span></p>
            </div>
            
            <h3 style="color:var(--color-gold); font-size:1.1em; margin-bottom:10px;">Countdown to the Event</h3>
            <div id="countdown">
                <div><span class="time-value" id="days">00</span><span class="time-label">Days</span></div>
                <div><span class="time-value" id="hours">00</span><span class="time-label">Hours</span></div>
                <div><span class="time-value" id="minutes">00</span><span class="time-label">Minutes</span></div>
                <div><span class="time-value" id="seconds">00</span><span class="time-label">Seconds</span></div>
            </div>

            <div class="location-section">
                <h3 style="color:var(--color-gold); font-size:1.1em;">Location Map</h3>
                
                <div class="map-container">
                    <iframe 
                        src="http://googleusercontent.com/maps.google.com/9" 
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>
                </div>
                
                <a href="https://maps.app.goo.gl/ContohLinkGoogleMapsBlackOwl0" target="_blank" class="cta-button">
                    Get Directions (Google Maps)
                </a>
            </div>
            
            <div class="rsvp-section">
                <h3 style="color:var(--color-gold); font-size:1.1em;">RSVP</h3>
                <p style="font-size:0.9em; opacity:0.9;">Kindly confirm your attendance:</p>
                <button class="cta-button rsvp-button" onclick="playMusicAndRsvp('attend');">I Will Attend</button>
                <button class="cta-button rsvp-button" style="background: white; color: black; margin-left: 10px;" onclick="playMusicAndRsvp('decline');">Regretfully Decline</button>
            </div>
            
        </div>
        
        <p style="margin-top: 40px; font-size: 0.8em; color: #aaa; opacity:0.7;">See you at Black Owl!</p>

    </div>

    <button id="music-button" onclick="toggleMusic()" style="display: none;">&#9835;</button> 

    <script>
        // ==========================================================
        // JAVASCRIPT LOGIC
        // ==========================================================

        const music = document.getElementById('party-music');
        const musicButton = document.getElementById('music-button');
        const landingPage = document.getElementById('landing-page');
        const mainInvitation = document.getElementById('main-invitation');
        let musicPlaying = false;

        // Fungsi untuk membuka undangan (dipanggil dari tombol "Invitation")
        function openInvitation() {
            // 1. Coba putar musik
            music.play().then(() => {
                musicPlaying = true;
                musicButton.innerHTML = '&#9833;'; // Ganti ikon ke pause
                musicButton.style.display = 'block'; // Tampilkan tombol kontrol musik
            }).catch(error => {
                console.warn("Autoplay was prevented. Music will start upon next interaction.");
                // Jika autoplay diblokir, tombol kontrol musik tetap ditampilkan
                musicButton.style.display = 'block';
            });

            // 2. Hilangkan landing page dengan transisi fade out
            landingPage.style.opacity = '0';
            setTimeout(() => {
                landingPage.style.display = 'none';
                mainInvitation.style.display = 'flex'; // Tampilkan konten utama
            }, 1000); // Waktu harus sama dengan transisi CSS (1s)
        }

        // Fungsi untuk mengontrol musik (Play/Pause)
        function toggleMusic() {
            if (musicPlaying) {
                music.pause();
                musicButton.innerHTML = '&#9835;';
                musicPlaying = false;
            } else {
                music.play().catch(error => {
                    console.error("Playback failed:", error);
                });
                musicButton.innerHTML = '&#9833;';
                musicPlaying = true;
            }
        }

        // Fungsi RSVP yang juga memastikan musik berbunyi
        function playMusicAndRsvp(status) {
            if (!musicPlaying) {
                 music.play().catch(error => {
                    console.warn("Music starts now.");
                });
                musicButton.innerHTML = '&#9833;';
                musicPlaying = true;
            }

            if (status === 'attend') {
                alert('Thank you! Your RSVP has been received.');
            } else {
                alert('We will miss you!');
            }
        }
        
        // ----------------------------------------------------------
        // Countdown Timer & Background Animation (SAMA SEPERTI SEBELUMNYA)
        // ----------------------------------------------------------
        const targetDate = new Date("Oct 28, 2025 19:00:00").getTime(); 
        const countdownFunction = setInterval(function() {
            const now = new Date().getTime();
            const distance = targetDate - now;
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            document.getElementById("days").innerHTML = days < 10 ? '0' + days : days;
            document.getElementById("hours").innerHTML = hours < 10 ? '0' + hours : hours;
            document.getElementById("minutes").innerHTML = minutes < 10 ? '0' + minutes : minutes;
            document.getElementById("seconds").innerHTML = seconds < 10 ? '0' + seconds : seconds;
            if (distance < 0) {
                clearInterval(countdownFunction);
                document.getElementById("countdown").innerHTML = "<h3 style='color:var(--color-gold);'>THE PARTY IS LIVE!</h3>";
            }
        }, 1000);
        
        const particleContainer = document.getElementById('particle-bg');
        const numParticles = 80;
        const particleColors = [
            'var(--color-gold)', 'var(--color-light-gold)', 'var(--color-cream)', 'rgba(255, 255, 255, 0.7)'
        ];

        for (let i = 0; i < numParticles; i++) {
            const particle = document.createElement('div');
            particle.classList.add('particle');
            const size = Math.random() * 4 + 1;
            const left = Math.random() * 100;
            const duration = Math.random() * 20 + 10;
            const delay = Math.random() * 20;
            const color = particleColors[Math.floor(Math.random() * particleColors.length)];
            particle.style.width = `${size}px`;
            particle.style.height = `${size}px`;
            particle.style.left = `${left}vw`;
            particle.style.animationDuration = `${duration}s`;
            particle.style.animationDelay = `${delay}s`;
            particle.style.backgroundColor = color;
            particle.style.opacity = Math.random() * 0.6 + 0.3;
            particleContainer.appendChild(particle);
        }
    </script>
</body>
</html>
