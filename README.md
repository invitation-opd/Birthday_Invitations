# Birthday_Invitations
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Ulang Tahun Lita 32 - Black Owl Surabaya</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* ========================================================== */
        /* CSS STYLES (GAYA) */
        /* ========================================================== */

        :root {
            --color-black: #000000;
            --color-gold: #FFD700;
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
        /* Background Animasi Partikel Emas */
        /* ---------------------------------------------------------- */
        .particle-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 1;
            /* Tambahkan efek gelap tipis agar teks lebih menonjol */
            background: rgba(0, 0, 0, 0.2); 
        }

        .particle {
            position: absolute;
            background: var(--color-gold);
            border-radius: 50%;
            opacity: 0.8;
            animation: moveParticles linear infinite;
        }

        @keyframes moveParticles {
            0% { transform: translateY(100vh) scale(0); opacity: 0; }
            50% { opacity: 0.8; }
            100% { transform: translateY(-10vh) scale(1); opacity: 0; }
        }

        /* JavaScript akan membuat partikel dan menambahkan style individual */


        /* ---------------------------------------------------------- */
        /* Konten Utama */
        /* ---------------------------------------------------------- */

        .container {
            position: relative;
            z-index: 10; /* Pastikan konten di atas background */
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 40px 20px;
        }

        .header {
            margin-bottom: 50px;
        }

        .title-sub {
            font-size: 1.2em;
            letter-spacing: 2px;
            color: var(--color-gold);
            margin-bottom: -10px;
        }

        .title-name {
            font-family: var(--font-script);
            font-size: 8em;
            line-height: 1;
            color: var(--color-gold);
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }

        .title-age {
            font-size: 4em;
            color: white;
            line-height: 0.8;
            margin-top: -30px;
        }

        /* ---------------------------------------------------------- */
        /* Detail Acara & Countdown */
        /* ---------------------------------------------------------- */

        .details-box {
            background: rgba(0, 0, 0, 0.7);
            border: 1px solid var(--color-gold);
            padding: 30px 40px;
            border-radius: 10px;
            max-width: 450px;
            margin-bottom: 40px;
        }

        .detail-item {
            margin: 15px 0;
            font-size: 1.1em;
        }

        .detail-label {
            display: block;
            color: var(--color-gold);
            font-weight: 700;
            margin-bottom: 5px;
        }

        #countdown {
            margin: 20px 0;
            border: 2px solid var(--color-gold);
            padding: 15px;
            border-radius: 5px;
        }

        #countdown div {
            display: inline-block;
            margin: 0 10px;
        }

        .time-value {
            display: block;
            font-size: 2.5em;
            font-weight: 700;
            color: var(--color-gold);
        }

        .time-label {
            font-size: 0.8em;
            color: white;
        }
        
        .dresscode {
            font-size: 1.3em;
            font-weight: 700;
            color: var(--color-gold);
            margin-top: 20px;
        }

        /* ---------------------------------------------------------- */
        /* Lokasi & Peta */
        /* ---------------------------------------------------------- */

        .location-section {
            width: 100%;
            max-width: 600px;
            margin-top: 30px;
        }

        .map-container {
            border: 3px solid var(--color-gold);
            height: 300px;
            margin-top: 15px;
            overflow: hidden;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        .cta-button {
            background: var(--color-gold);
            color: var(--color-black);
            border: none;
            padding: 12px 25px;
            font-size: 1.1em;
            font-weight: 700;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            text-decoration: none;
            display: inline-block;
            transition: background 0.3s;
        }

        .cta-button:hover {
            background: #e6c300;
        }


        /* ---------------------------------------------------------- */
        /* Responsiveness */
        /* ---------------------------------------------------------- */
        @media (max-width: 600px) {
            .title-name {
                font-size: 5em;
            }
            .title-age {
                font-size: 3em;
            }
            .details-box {
                padding: 20px;
            }
            .time-value {
                font-size: 2em;
            }
            #countdown div {
                margin: 0 5px;
            }
        }
    </style>
</head>
<body>

    <div class="particle-bg" id="particle-bg"></div>

    <div class="container">
        
        <div class="header">
            <p class="title-sub">Undangan Ulang Tahun</p>
            <h1 class="title-name">Lita</h1>
            <h2 class="title-age">32</h2>
        </div>

        <div class="details-box">
            <p style="margin-top:0;">Kami mengundang Anda untuk merayakan hari spesial ini bersama kami!</p>
            
            <div class="detail-item">
                <span class="detail-label">Hari, Tanggal</span>
                Sabtu, 28 Oktober 2025
            </div>

            <div class="detail-item">
                <span class="detail-label">Waktu</span>
                19.00 WIB - Selesai
            </div>
            
            <div class="detail-item">
                <span class="detail-label">Lokasi</span>
                Black Owl Surabaya
            </div>

            <p class="dresscode">Dresscode: BLACK GOLD</p>
        </div>
        
        <h3 style="color:var(--color-gold);">Waktu Menuju Acara</h3>
        <div id="countdown">
            <div><span class="time-value" id="days">00</span><span class="time-label">Hari</span></div>
            <div><span class="time-value" id="hours">00</span><span class="time-label">Jam</span></div>
            <div><span class="time-value" id="minutes">00</span><span class="time-label">Menit</span></div>
            <div><span class="time-value" id="seconds">00</span><span class="time-label">Detik</span></div>
        </div>

        <div class="location-section">
            <h3 style="color:var(--color-gold);">Peta Lokasi</h3>
            
            <div class="map-container">
                <iframe 
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3957.546747230495!2d112.73031121477543!3d-7.291703094723143!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd7f917208d249f%3A0x6b4c10a3e811370!2sBlack%20Owl%20Dining%20%26%20Lounge%20Surabaya!5e0!3m2!1sid!2sid!4v1678822600000" 
                    allowfullscreen="" 
                    loading="lazy" 
                    referrerpolicy="no-referrer-when-downgrade">
                </iframe>
            </div>
            
            <a href="https://maps.app.goo.gl/ContohLinkGoogleMapsBlackOwl" target="_blank" class="cta-button">
                Arahkan ke Lokasi (Google Maps)
            </a>
        </div>
        
        <div style="margin-top: 50px;">
            <h3 style="color:var(--color-gold);">Konfirmasi Kehadiran (RSVP)</h3>
            <p>Mohon konfirmasi kehadiran Anda:</p>
            <button class="cta-button" onclick="alert('Terima kasih! RSVP Anda telah diterima.');">Saya Hadir</button>
            <button class="cta-button" style="background: white; color: black; margin-left: 10px;" onclick="alert('Kami akan merindukan kehadiran Anda!');">Maaf, Tidak Bisa Hadir</button>
        </div>
        
        <p style="margin-top: 80px; font-size: 0.9em; color: #aaa;">Sampai bertemu di Black Owl, 28 Oktober 2025!</p>

    </div>


    <script>
        // ----------------------------------------------------------
        // 1. Countdown Timer
        // ----------------------------------------------------------
        const targetDate = new Date("Oct 28, 2025 19:00:00").getTime();

        const countdownFunction = setInterval(function() {
            const now = new Date().getTime();
            const distance = targetDate - now;

            // Perhitungan waktu
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            // Tampilkan hasil di elemen
            document.getElementById("days").innerHTML = days < 10 ? '0' + days : days;
            document.getElementById("hours").innerHTML = hours < 10 ? '0' + hours : hours;
            document.getElementById("minutes").innerHTML = minutes < 10 ? '0' + minutes : minutes;
            document.getElementById("seconds").innerHTML = seconds < 10 ? '0' + seconds : seconds;

            // Jika hitungan selesai
            if (distance < 0) {
                clearInterval(countdownFunction);
                document.getElementById("countdown").innerHTML = "<h3 style='color:var(--color-gold);'>ACARA SEDANG BERLANGSUNG!</h3>";
            }
        }, 1000);
        
        // ----------------------------------------------------------
        // 2. Background Animasi Partikel Emas
        // ----------------------------------------------------------
        const particleContainer = document.getElementById('particle-bg');
        const numParticles = 50; // Jumlah partikel

        for (let i = 0; i < numParticles; i++) {
            const particle = document.createElement('div');
            particle.classList.add('particle');
            
            // Posisi acak di sumbu X dan ukuran acak
            const size = Math.random() * 5 + 1; // Ukuran 1px sampai 6px
            const left = Math.random() * 100; // Posisi 0% sampai 100%
            const duration = Math.random() * 15 + 10; // Durasi 10s sampai 25s
            const delay = Math.random() * 15; // Delay 0s sampai 15s

            particle.style.width = `${size}px`;
            particle.style.height = `${size}px`;
            particle.style.left = `${left}vw`;
            particle.style.animationDuration = `${duration}s`;
            particle.style.animationDelay = `${delay}s`;

            particleContainer.appendChild(particle);
        }
    </script>
</body>
</html>
