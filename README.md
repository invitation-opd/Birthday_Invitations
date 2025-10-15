# Birthday_Invitations

<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Ulang Tahun Lita 32 - Black Owl Surabaya</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* ========================================================== */
        /* CSS STYLES (GAYA) - Disesuaikan dengan Gambar */
        /* ========================================================== */

        :root {
            --color-black: #000000;
            --color-dark-grey: #1a1a1a;
            --color-gold: #FFD700; /* Warna emas dasar */
            --color-light-gold: #FFEA9F; /* Untuk variasi partikel */
            --color-cream: #FFFDD0; /* Untuk variasi partikel */
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
        /* Background Animasi Partikel Emas Lebih Banyak Warna */
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
            background-color: var(--color-black); /* Pastikan latar belakang dasar hitam */
        }

        .particle {
            position: absolute;
            border-radius: 50%;
            opacity: 0.8;
            animation: moveParticles linear infinite;
            filter: blur(0.5px); /* Memberi efek lembut seperti glitter */
        }

        @keyframes moveParticles {
            0% { transform: translateY(100vh) scale(0); opacity: 0; }
            20% { opacity: 0.6; }
            50% { opacity: 0.9; }
            80% { opacity: 0.6; }
            100% { transform: translateY(-10vh) scale(1); opacity: 0; }
        }

        /* ---------------------------------------------------------- */
        /* Container dan Border Persegi Panjang */
        /* ---------------------------------------------------------- */
        .container {
            position: relative;
            z-index: 10;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center; /* Pusatkan vertikal */
            min-height: 100vh;
            text-align: center;
            padding: 20px;
        }

        .invitation-frame {
            background: rgba(0, 0, 0, 0.85); /* Sedikit transparan agar partikel terlihat */
            border: 4px solid var(--color-gold); /* Border tebal seperti gambar */
            padding: 40px 30px; /* Padding untuk konten di dalamnya */
            max-width: 500px;
            width: 90%; /* Lebar responsif */
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.6); /* Efek glow emas */
            border-radius: 5px; /* Sedikit lengkungan pada border */
            position: relative;
        }

        /* Dekorasi Sudut Border (seperti di gambar) */
        .invitation-frame::before,
        .invitation-frame::after {
            content: '';
            position: absolute;
            background: var(--color-gold);
            width: 30px; /* Ukuran dekorasi */
            height: 4px;
        }
        .invitation-frame::before { top: -4px; left: -4px; } /* Sudut kiri atas */
        .invitation-frame::after { top: -4px; right: -4px; } /* Sudut kanan atas */

        .invitation-frame > :first-child { margin-top: 0; }
        .invitation-frame > :last-child { margin-bottom: 0; }

        /* Garis melengkung di sudut (menggunakan pseudo-elements lain) */
        .invitation-frame .corner-deco.top-left {
            position: absolute;
            top: -20px;
            left: -20px;
            width: 50px;
            height: 50px;
            border-top: 2px solid var(--color-gold);
            border-left: 2px solid var(--color-gold);
            border-top-left-radius: 20px;
            transform: rotate(45deg); /* Rotasi agar terlihat melengkung */
        }
         .invitation-frame .corner-deco.top-right {
            position: absolute;
            top: -20px;
            right: -20px;
            width: 50px;
            height: 50px;
            border-top: 2px solid var(--color-gold);
            border-right: 2px solid var(--color-gold);
            border-top-right-radius: 20px;
            transform: rotate(-45deg);
        }
        /* Tambahkan untuk bawah jika diperlukan */

        /* ---------------------------------------------------------- */
        /* Header Teks (Undangan Ulang Tahun, Lita, 32) */
        /* ---------------------------------------------------------- */
        .header-content {
            margin-bottom: 30px;
        }

        .title-sub {
            font-size: 1em; /* Lebih kecil seperti di gambar */
            letter-spacing: 2px;
            color: white; /* Putih/Cream seperti di gambar */
            margin-bottom: 5px;
            font-weight: 300;
        }

        .title-name {
            font-family: var(--font-script);
            font-size: 5em; /* Disesuaikan agar pas di frame */
            line-height: 1.1;
            color: var(--color-gold);
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
            margin: 0; /* Hapus margin default h1 */
        }

        .title-age {
            font-size: 3.5em; /* Disesuaikan */
            color: white;
            line-height: 0.9;
            margin-top: -10px; /* Lebih dekat ke nama */
            font-weight: 700;
        }

        /* ---------------------------------------------------------- */
        /* Detail Acara & Countdown */
        /* ---------------------------------------------------------- */
        .details-section {
            margin-top: 20px;
        }

        .detail-item {
            margin: 10px 0;
            font-size: 1.05em;
            color: white;
            line-height: 1.4;
        }

        .detail-label {
            display: block;
            color: var(--color-gold);
            font-weight: 700;
            margin-bottom: 2px;
            font-size: 0.9em;
        }
        
        .dresscode {
            font-size: 1.2em;
            font-weight: 700;
            color: white; /* Dresscode putih seperti di gambar */
            margin-top: 25px;
        }
        .dresscode span {
             color: var(--color-gold); /* Highlight BLACK GOLD */
        }

        #countdown {
            margin: 30px 0 20px;
            padding: 15px 0;
            border-top: 1px dashed rgba(255, 215, 0, 0.5); /* Garis pemisah tipis */
            border-bottom: 1px dashed rgba(255, 215, 0, 0.5);
        }

        #countdown div {
            display: inline-block;
            margin: 0 8px;
        }

        .time-value {
            display: block;
            font-size: 2em; /* Lebih kecil agar pas */
            font-weight: 700;
            color: var(--color-gold);
            text-shadow: 0 0 8px rgba(255, 215, 0, 0.4);
        }

        .time-label {
            font-size: 0.7em;
            color: white;
        }
        
        /* ---------------------------------------------------------- */
        /* Lokasi & Peta */
        /* ---------------------------------------------------------- */
        .location-section {
            width: 100%;
            margin-top: 30px;
        }

        .map-container {
            border: 2px solid var(--color-gold);
            height: 250px;
            margin-top: 15px;
            overflow: hidden;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.4);
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
            padding: 10px 20px;
            font-size: 1em;
            font-weight: 700;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            text-decoration: none;
            display: inline-block;
            transition: background 0.3s, transform 0.2s;
        }

        .cta-button:hover {
            background: var(--color-light-gold);
            transform: translateY(-2px);
        }

        .rsvp-section {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px dashed rgba(255, 215, 0, 0.3);
        }
        .rsvp-section button {
            margin: 5px;
        }


        /* ---------------------------------------------------------- */
        /* Responsiveness */
        /* ---------------------------------------------------------- */
        @media (max-width: 600px) {
            .title-name {
                font-size: 4em;
            }
            .title-age {
                font-size: 2.5em;
            }
            .invitation-frame {
                padding: 30px 20px;
            }
            .time-value {
                font-size: 1.8em;
            }
            #countdown div {
                margin: 0 3px;
            }
            .detail-item {
                font-size: 1em;
            }
            .cta-button {
                padding: 10px 18px;
                font-size: 0.9em;
            }
        }

        @media (max-width: 400px) {
            .title-name {
                font-size: 3.5em;
            }
            .title-age {
                font-size: 2em;
            }
             .invitation-frame {
                padding: 25px 15px;
            }
            .time-value {
                font-size: 1.5em;
            }
            .dresscode {
                font-size: 1.1em;
            }
        }
    </style>
</head>
<body>

    <div class="particle-bg" id="particle-bg"></div>

    <div class="container">
        <div class="invitation-frame">
            <div class="corner-deco top-left"></div>
            <div class="corner-deco top-right"></div>
            <div class="header-content">
                <p class="title-sub">Undangan Ulang Tahun</p>
                <h1 class="title-name">Lita</h1>
                <h2 class="title-age">32</h2>
            </div>

            <div class="details-section">
                <p style="margin-top:0; font-size: 0.9em; color: rgba(255,255,255,0.9);">
                    Kami berbahagia mengundang Anda untuk merayakan hari spesial ini.
                </p>
                
                <div class="detail-item">
                    Sabtu, 28 Oktober 2025
                </div>

                <div class="detail-item">
                    Pukul 19.00 WIB
                </div>
                
                <div class="detail-item">
                    Black Owl Surabaya
                    <br>
                    <span style="font-size:0.8em; opacity:0.8;">[Alamat Lengkap Black Owl Surabaya]</span>
                </div>

                <p class="dresscode">Dresscode: <span>BLACK GOLD</span></p>
            </div>
            
            <h3 style="color:var(--color-gold); font-size:1.1em; margin-bottom:10px;">Waktu Menuju Acara</h3>
            <div id="countdown">
                <div><span class="time-value" id="days">00</span><span class="time-label">Hari</span></div>
                <div><span class="time-value" id="hours">00</span><span class="time-label">Jam</span></div>
                <div><span class="time-value" id="minutes">00</span><span class="time-label">Menit</span></div>
                <div><span class="time-value" id="seconds">00</span><span class="time-label">Detik</span></div>
            </div>

            <div class="location-section">
                <h3 style="color:var(--color-gold); font-size:1.1em;">Peta Lokasi</h3>
                
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3957.5401340656045!2d112.73030281477543!3d-7.291702094770806!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd7fb773990b7a7%3A0x1d7c3d7e5d7d7d7!2sBlack%20Owl%20Surabaya!5e0!3m2!1sid!2sid!4v1678901234567!5m2!1sid!2sid" 
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>
                </div>
                
                <a href="https://maps.app.goo.gl/YourBlackOwlLocationLink" target="_blank" class="cta-button">
                    Arahkan ke Lokasi (Google Maps)
                </a>
            </div>
            
            <div class="rsvp-section">
                <h3 style="color:var(--color-gold); font-size:1.1em;">Konfirmasi Kehadiran (RSVP)</h3>
                <p style="font-size:0.9em; opacity:0.9;">Mohon konfirmasi kehadiran Anda:</p>
                <button class="cta-button" onclick="alert('Terima kasih! RSVP Anda telah diterima.');">Saya Hadir</button>
                <button class="cta-button" style="background: white; color: black; margin-left: 10px;" onclick="alert('Kami akan merindukan kehadiran Anda!');">Maaf, Tidak Bisa Hadir</button>
            </div>
            
        </div>
        
        <p style="margin-top: 40px; font-size: 0.8em; color: #aaa; opacity:0.7;">Sampai bertemu di Black Owl!</p>

    </div>


    <script>
        // ----------------------------------------------------------
        // 1. Countdown Timer
        // ----------------------------------------------------------
        // Ganti dengan tanggal dan waktu acara Anda
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
                document.getElementById("countdown").innerHTML = "<h3 style='color:var(--color-gold);'>ACARA SEDANG BERLANGSUNG!</h3>";
            }
        }, 1000);
        
        // ----------------------------------------------------------
        // 2. Background Animasi Partikel Emas Lebih Banyak Warna
        // ----------------------------------------------------------
        const particleContainer = document.getElementById('particle-bg');
        const numParticles = 80; // Jumlah partikel diperbanyak
        const particleColors = [
            'var(--color-gold)', 
            'var(--color-light-gold)', 
            'var(--color-cream)',
            'rgba(255, 255, 255, 0.7)' // Sedikit warna putih/perak
        ];

        for (let i = 0; i < numParticles; i++) {
            const particle = document.createElement('div');
            particle.classList.add('particle');
            
            const size = Math.random() * 4 + 1; // Ukuran 1px sampai 5px
            const left = Math.random() * 100; // Posisi 0% sampai 100%
            const duration = Math.random() * 20 + 10; // Durasi 10s sampai 30s
            const delay = Math.random() * 20; // Delay 0s sampai 20s
            const color = particleColors[Math.floor(Math.random() * particleColors.length)];

            particle.style.width = `${size}px`;
            particle.style.height = `${size}px`;
            particle.style.left = `${left}vw`;
            particle.style.animationDuration = `${duration}s`;
            particle.style.animationDelay = `${delay}s`;
            particle.style.backgroundColor = color;
            particle.style.opacity = Math.random() * 0.6 + 0.3; // Opacity bervariasi

            particleContainer.appendChild(particle);
        }
    </script>
</body>
</html>
            
