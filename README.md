<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PMR SMPN 6 CIMAHI - JURESIX</title>
    <!-- Google Fonts: Poppins & Fredoka untuk kesan ramah anak dan lucu -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome untuk Icon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-blue: #2A7B9B;
            --light-blue: #E8F4F8;
            --dark-blue: #1E566E;
            --primary-green: #68B04D;
            --light-green: #EDF7E7;
            --dark-green: #467E30;
            --orange-accent: #FF9F43;
            --text-dark: #2C3E50;
            --text-muted: #7F8C8D;
            --white: #FFFFFF;
            --card-radius: 20px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light-blue);
            color: var(--text-dark);
            overflow-x: hidden;
            line-height: 1.6;
        }

        h1, h2, h3, .brand-title {
            font-family: 'Fredoka', sans-serif;
            font-weight: 600;
        }

        /* --- NAVBAR --- */
        .navbar {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 15px 5%;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.05);
            border-bottom: 4px solid var(--primary-green);
        }

        .nav-logo-container {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .nav-logo-container i {
            font-size: 2rem;
            color: var(--primary-green);
        }

        .brand-text .brand-title {
            font-size: 1.5rem;
            color: var(--primary-blue);
            line-height: 1.2;
        }

        .brand-text .brand-subtitle {
            font-size: 0.85rem;
            color: var(--primary-green);
            font-weight: 600;
            letter-spacing: 1px;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 25px;
            align-items: center;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            transition: all 0.3s ease;
            padding: 8px 16px;
            border-radius: 12px;
        }

        .nav-link:hover {
            background-color: var(--light-green);
            color: var(--dark-green);
        }

        .btn-join-nav {
            background-color: var(--orange-accent);
            color: var(--white);
            padding: 10px 20px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-family: 'Fredoka', sans-serif;
            box-shadow: 0 4px 10px rgba(255, 159, 67, 0.3);
            transition: transform 0.2s;
        }

        .btn-join-nav:hover {
            transform: scale(1.05);
        }

        /* --- HERO SECTION --- */
        .hero {
            position: relative;
            background: linear-gradient(135deg, #A8E6CF 0%, #DCEDC1 100%);
            padding: 80px 5% 120px 5%;
            text-align: center;
            border-bottom-left-radius: 50px;
            border-bottom-right-radius: 50px;
            overflow: hidden;
        }

        /* Animasi Dinosaurus Lucu */
        .dino-mascot {
            font-size: 5rem;
            color: var(--dark-green);
            animation: bounce 3s infinite ease-in-out;
            margin-bottom: 20px;
            display: inline-block;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-15px) rotate(5deg); }
        }

        .hero h1 {
            font-size: 3rem;
            color: var(--dark-blue);
            margin-bottom: 15px;
            text-shadow: 2px 2px var(--white);
        }

        .hero p {
            font-size: 1.2rem;
            color: #4A5568;
            max-width: 700px;
            margin: 0 auto 30px auto;
        }

        .hero-badges {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .hero-badge {
            background: rgba(255, 255, 255, 0.85);
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            color: var(--dark-blue);
            border: 2px solid var(--white);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .hero-badge.pmi i { color: #E74C3C; }
        .hero-badge.juresix i { color: var(--primary-green); }

        /* --- LAYOUT CONTAINER --- */
        .main-container {
            max-width: 1200px;
            margin: -50px auto 60px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            position: relative;
            z-index: 10;
        }

        @media (max-width: 992px) {
            .main-container {
                grid-template-columns: 1fr;
            }
        }

        .content-left, .content-right {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        /* --- CARDS --- */
        .card {
            background-color: var(--white);
            border-radius: var(--card-radius);
            padding: 35px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.03);
            border: 4px solid var(--white);
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--light-blue);
        }

        .card-title-container {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            border-bottom: 3px dashed var(--light-blue);
            padding-bottom: 15px;
        }

        .card-title-container i {
            font-size: 2rem;
            color: var(--primary-blue);
        }

        .card-title {
            font-size: 1.8rem;
            color: var(--dark-blue);
        }

        /* --- LOGO DISPLAY --- */
        .logo-display {
            display: flex;
            gap: 20px;
            margin-top: 25px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .logo-box {
            background-color: var(--light-green);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            flex: 1;
            min-width: 150px;
            border: 2px dashed var(--primary-green);
        }

        .logo-box i {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .logo-box.pmi-box i { color: #E74C3C; }
        .logo-box.juresix-box i { color: var(--primary-blue); }

        .logo-box h4 {
            font-family: 'Fredoka', sans-serif;
            font-size: 1.1rem;
            color: var(--text-dark);
        }

        /* --- MANFAAT PMR --- */
        .manfaat-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .manfaat-item {
            background-color: var(--light-green);
            padding: 20px;
            border-radius: 15px;
            border-left: 5px solid var(--primary-green);
            transition: all 0.2s;
        }

        .manfaat-item:hover {
            background-color: var(--white);
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .manfaat-header {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 10px;
        }

        .manfaat-header i {
            color: var(--dark-green);
            font-size: 1.3rem;
        }

        .manfaat-header h4 {
            font-family: 'Fredoka', sans-serif;
            color: var(--dark-green);
            font-size: 1.1rem;
        }

        /* --- PENANGANAN PERTAMA --- */
        .firstaid-list {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .firstaid-item {
            background: var(--light-blue);
            border-radius: 15px;
            padding: 20px;
            border: 2px solid rgba(42, 123, 155, 0.1);
        }

        .firstaid-toggle h4 {
            font-family: 'Fredoka', sans-serif;
            color: var(--dark-blue);
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .firstaid-toggle h4 i {
            color: var(--primary-blue);
        }

        .firstaid-content {
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px dashed rgba(42, 123, 155, 0.2);
            color: #576574;
        }

        .firstaid-content ol {
            margin-left: 20px;
            margin-top: 8px;
        }

        .rice-box {
            background-color: var(--white);
            padding: 15px;
            border-radius: 10px;
            margin-top: 10px;
            border-left: 4px solid var(--orange-accent);
        }

        /* --- STRUKTUR ORGANISASI --- */
        .structure-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
            align-items: center;
        }

        .structure-row {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            width: 100%;
        }

        .member-card {
            background: var(--light-green);
            border: 2px solid var(--primary-green);
            border-radius: 15px;
            padding: 15px;
            text-align: center;
            min-width: 160px;
            flex: 1;
            max-width: 200px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.02);
        }

        .member-card.core {
            background: var(--light-blue);
            border-color: var(--primary-blue);
            max-width: 220px;
        }

        .member-avatar {
            width: 70px;
            height: 70px;
            background-color: var(--white);
            border-radius: 50%;
            margin: 0 auto 10px auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: var(--text-muted);
            border: 3px solid var(--white);
            box-shadow: 0 3px 8px rgba(0,0,0,0.1);
        }

        .member-card.core .member-avatar {
            color: var(--primary-blue);
        }

        .member-role {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-muted);
            font-weight: 600;
        }

        .member-name {
            font-family: 'Fredoka', sans-serif;
            font-size: 1.1rem;
            color: var(--text-dark);
            margin-top: 2px;
        }

        /* --- FORM REGISTRASI --- */
        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--dark-blue);
        }

        .form-control {
            width: 100%;
            padding: 12px;
            border: 2px solid var(--light-blue);
            border-radius: 10px;
            font-family: inherit;
            font-size: 0.95rem;
            transition: border-color 0.2s;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary-blue);
        }

        .btn-submit {
            width: 100%;
            background-color: var(--primary-green);
            color: var(--white);
            border: none;
            padding: 14px;
            border-radius: 10px;
            font-family: 'Fredoka', sans-serif;
            font-size: 1.1rem;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(104, 176, 77, 0.3);
            transition: background-color 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .btn-submit:hover {
            background-color: var(--dark-green);
        }

        .btn-submit:disabled {
            background-color: var(--text-muted);
            cursor: not-allowed;
            box-shadow: none;
        }

        /* Alert Status Custom */
        .form-status {
            margin-top: 15px;
            padding: 12px;
            border-radius: 10px;
            font-size: 0.9rem;
            font-weight: 600;
            text-align: center;
            display: none;
        }
        .form-status.success {
            background-color: var(--light-green);
            color: var(--dark-green);
            border: 1px solid var(--primary-green);
        }
        .form-status.error {
            background-color: #FCE8E6;
            color: #C53929;
            border: 1px solid #E74C3C;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--dark-blue);
            color: var(--white);
            padding: 40px 5% 20px 5%;
            border-top-left-radius: 40px;
            border-top-right-radius: 40px;
            margin-top: 50px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            padding-bottom: 30px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .footer-col h3 {
            margin-bottom: 15px;
            color: #A8E6CF;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 8px;
        }

        .footer-links a {
            color: rgba(255,255,255,0.8);
            text-decoration: none;
            transition: color 0.2s;
        }

        .footer-links a:hover {
            color: var(--orange-accent);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            font-size: 0.9rem;
            color: rgba(255,255,255,0.6);
        }

        /* Dino Floating Action */
        .dino-deco {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--white);
            padding: 12px;
            border-radius: 50%;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            z-index: 999;
            font-size: 1.6rem;
            color: var(--primary-green);
            cursor: pointer;
            animation: mini-bounce 2s infinite ease-in-out;
        }

        @keyframes mini-bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-6px); }
        }

    </style>
</head>
<body>

    <!-- Ornamen Dinosaurus Kecil Floating -->
    <div class="dino-deco" onclick="alert('Rawrr! Salam Kemanusiaan dari Dino Juresix!')" title="Hai Relawan Juresix!"><i class="fas fa-dragon"></i></div>

    <!-- NAVBAR -->
    <nav class="navbar">
        <div class="nav-logo-container">
            <i class="fas fa-kit-medical"></i>
            <div class="brand-text">
                <div class="brand-title">JURESIX</div>
                <div class="brand-subtitle">PMR SMPN 6 CIMAHI</div>
            </div>
        </div>
        <ul class="nav-menu">
            <li><a href="#tentang" class="nav-link">Tentang</a></li>
            <li><a href="#manfaat" class="nav-link">Manfaat</a></li>
            <li><a href="#penanganan" class="nav-link">First Aid</a></li>
            <li><a href="#struktur" class="nav-link">Struktur</a></li>
            <li><a href="#daftar" class="btn-join-nav">Gabung!</a></li>
        </ul>
    </nav>

    <!-- HERO SECTION -->
    <header class="hero">
        <div class="dino-mascot">
            <i class="fas fa-dragon"></i>
        </div>
        <h1>Selamat Datang di Website Resmi JURESIX</h1>
        <p>Wadah kreativitas, aksi kemানুsiaan, dan persaudaraan anggota Palang Merah Remaja (PMR) Madya di SMP Negeri 6 Cimahi. Berbakti dan mengabdi dengan ceria!</p>
        
        <div class="hero-badges">
            <div class="hero-badge pmi">
                <i class="fas fa-heartpulse"></i> Palang Merah Indonesia
            </div>
            <div class="hero-badge juresix">
                <i class="fas fa-shield-cat"></i> Interama Caritas PMR
            </div>
        </div>
    </header>

    <!-- MAIN CONTAINER -->
    <div class="main-container">
        
        <!-- KOLOM KIRI (KONTEN UTAMA) -->
        <div class="content-left">
            
            <!-- TENTANG JURESIX -->
            <section id="tentang" class="card">
                <div class="card-title-container">
                    <i class="fas fa-id-card-clip"></i>
                    <h2 class="card-title">Tentang Juresix</h2>
                </div>
                <div style="color: #576574; text-align: justify;">
                    <p><strong>JURESIX</strong> (Junior Red Cross Six) merupakan nama identitas resmi dari ekstrakurikuler Palang Merah Remaja (PMR) tingkat Madya di SMP Negeri 6 Cimahi. Mengusung semboyan kebanggaan <em>"Interama Caritas PMR"</em>, kami berkomitmen membentuk generasi muda yang responsif, tangguh, berjiwa sosial tinggi, terampil dalam medis dasar pertolongan pertama, serta menanamkan empati mendalam sejak dini.</p>
                </div>
                
                <div class="logo-display">
                    <div class="logo-box pmi-box">
                        <i class="fas fa-notes-medical"></i>
                        <h4>PMI Indonesia</h4>
                    </div>
                    <div class="logo-box juresix-box">
                        <i class="fas fa-paw"></i>
                        <h4>Maskot Juresix</h4>
                    </div>
                </div>
            </section>

            <!-- MANFAAT PMR -->
            <section id="manfaat" class="card">
                <div class="card-title-container">
                    <i class="fas fa-star" style="color: var(--orange-accent);"></i>
                    <h2 class="card-title">Manfaat Mengikuti PMR</h2>
                </div>
                <div class="manfaat-grid">
                    <div class="manfaat-item">
                        <div class="manfaat-header">
                            <i class="fas fa-hand-holding-hand"></i>
                            <h4>Jiwa Sosial & Empati</h4>
                        </div>
                        <p style="font-size: 0.95rem; color: #576574;">Membentuk karakter yang peduli pada sesama manusia dan kebersihan lingkungan sesuai Tri Bakti PMR.</p>
                    </div>
                    <div class="manfaat-item">
                        <div class="manfaat-header">
                            <i class="fas fa-users-gear"></i>
                            <h4>Kepemimpinan</h4>
                        </div>
                        <p style="font-size: 0.95rem; color: #576574;">Melatih kemampuan manajemen kelompok, berkomunikasi, serta kerja sama tim dalam situasi kritis.</p>
                    </div>
                    <div class="manfaat-item">
                        <div class="manfaat-header">
                            <i class="fas fa-user-shield"></i>
                            <h4>Rasa Percaya Diri</h4>
                        </div>
                        <p style="font-size: 0.95rem; color: #576574;">Mengikis kepanikan sehingga menjadi pribadi yang tenang dan sigap saat memberikan bantuan.</p>
                    </div>
                    <div class="manfaat-item">
                        <div class="manfaat-header">
                            <i class="fas fa-stethoscope"></i>
                            <h4>Bekal Masa Depan</h4>
                        </div>
                        <p style="font-size: 0.95rem; color: #576574;">Memiliki landasan teori dasar medis yang kuat jika ingin melangkah ke jenjang profesi kesehatan.</p>
                    </div>
                </div>
            </section>

            <!-- PENANGANAN PERTAMA -->
            <section id="penanganan" class="card">
                <div class="card-title-container">
                    <i class="fas fa-kit-medical" style="color: #E74C3C;"></i>
                    <h2 class="card-title">Panduan Penanganan Pertama (First Aid)</h2>
                </div>
                <div class="firstaid-list">
                    
                    <div class="firstaid-item">
                        <div class="firstaid-toggle">
                            <h4><i class="fas fa-fire-burner"></i> 1. Luka Bakar Ringan (Tingkat I)</h4>
                        </div>
                        <div class="firstaid-content">
                            <p>Kulit luar tampak memerah dan terasa perih/panas akibat kontak fisik dengan objek panas.</p>
                            <ol>
                                <li>Guyur daerah yang terluka menggunakan air mengalir bersih selama minimal 10–15 menit.</li>
                                <li><strong>Dilarang keras</strong> mengoleskan pasta gigi (odol), mentega, kecap, karena berisiko memerangkap panas dan memicu infeksi bakteri.</li>
                                <li>Tutup area luka secara longgar menggunakan kain kasa steril.</li>
                            </ol>
                        </div>
                    </div>

                    <div class="firstaid-item">
                        <div class="firstaid-toggle">
                            <h4><i class="fas fa-droplet"></i> 2. Mimisan (Epistaksis)</h4>
                        </div>
                        <div class="firstaid-content">
                            <p>Pecahnya pembuluh darah kapiler di dalam hidung akibat kelelahan atau suhu ekstrem.</p>
                            <ol>
                                <li>Dudukkan korban secara tegak dan instruksikan **condong ke depan** (jangan menengadah agar darah tidak menyumbat saluran napas).</li>
                                <li>Pencet cuping hidung secara rapat selama 5–10 menit memakai jari.</li>
                                <li>Minta korban bernapas lewat mulut. Kompres es di area pangkal hidung bagian atas jika diperlukan.</li>
                            </ol>
                        </div>
                    </div>

                    <div class="firstaid-item">
                        <div class="firstaid-toggle">
                            <h4><i class="fas fa-bed-pulse"></i> 3. Pingsan (Sinkop)</h4>
                        </div>
                        <div class="firstaid-content">
                            <p>Penurunan tingkat kesadaran sementara karena berkurangnya suplai oksigen ke otak.</p>
                            <ol>
                                <li>Bawa korban ke area yang teduh, sejuk, aman, dan memiliki ventilasi udara yang longgar.</li>
                                <li>Baringkan secara telentang, lalu **tinggikan posisi kaki korban** sekitar 20–30 cm guna melancarkan darah balik ke kepala.</li>
                                <li>Longgarkan pakaian yang ketat seperti kerah kancing, dasi, atau sabuk.</li>
                                <li>Jangan berikan cairan apa pun saat belum sadar penuh. Beri air hangat ketika sudah siuman.</li>
                            </ol>
                        </div>
                    </div>

                    <div class="firstaid-item">
                        <div class="firstaid-toggle">
                            <h4><i class="fas fa-bone"></i> 4. Keseleo / Terkilir (Sprain)</h4>
                        </div>
                        <div class="firstaid-content">
                            <p>Cedera ligamen sendi. Tangani segera dengan metode emas PMR, yakni **R.I.C.E.**:</p>
                            <div class="rice-box">
                                <strong>• Rest (Istirahat):</strong> Istirahatkan area sendi yang cedera, jangan dipakai menahan berat beban.<br>
                                <strong>• Ice (Es):</strong> Kompres dingin dibalut kain tipis selama 15 menit pada area bengkak.<br>
                                <strong>• Compression (Tekan):</strong> Bebat menggunakan perban elastis secara merata, pastikan tidak terlalu kencang.<br>
                                <strong>• Elevation (Tinggikan):</strong> Posisikan sendi yang cedera lebih tinggi/sejajar posisi jantung ketika berbaring.
                            </div>
                        </div>
                    </div>

                </div>
            </section>

            <!-- STRUKTUR ORGANISASI -->
            <section id="struktur" class="card">
                <div class="card-title-container">
                    <i class="fas fa-sitemap" style="color: var(--primary-green);"></i>
                    <h2 class="card-title">Struktur Organisasi Juresix (2025-2026)</h2>
                </div>
                <div class="structure-container">
                    
                    <!-- Pelatih -->
                    <div class="structure-row">
                        <div class="member-card core">
                            <div class="member-avatar"><i class="fas fa-user-tie"></i></div>
                            <div class="member-role">Pelatih</div>
                            <div class="member-name">Annisa Zakiya</div>
                        </div>
                    </div>

                    <!-- Komandan -->
                    <div class="structure-row">
                        <div class="member-card core">
                            <div class="member-avatar"><i class="fas fa-user-shield"></i></div>
                            <div class="member-role">Ketua Komandan</div>
                            <div class="member-name">Millati</div>
                        </div>
                        <div class="member-card core">
                            <div class="member-avatar"><i class="fas fa-user-shield"></i></div>
                            <div class="member-role">Wakil Komandan</div>
                            <div class="member-name">Alesha</div>
                        </div>
                    </div>

                    <!-- Administrasi & Usaha -->
                    <div class="structure-row">
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-signature"></i></div>
                            <div class="member-role">Sekretaris 1 & 2</div>
                            <div class="member-name">Adelia / Qiala</div>
                        </div>
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-wallet"></i></div>
                            <div class="member-role">Bendahara 1 & 2</div>
                            <div class="member-name">Khansa J. / Aurora</div>
                        </div>
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-shop"></i></div>
                            <div class="member-role">Danusan</div>
                            <div class="member-name">Syifa / Nazwa / Riska</div>
                        </div>
                    </div>

                    <!-- Divisi Teknis -->
                    <div class="structure-row">
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-camera"></i></div>
                            <div class="member-role">Dokumentasi</div>
                            <div class="member-name">Sultan / Juli / Zara / Caya</div>
                        </div>
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-bullhorn"></i></div>
                            <div class="member-role">Humas</div>
                            <div class="member-name">Nayla / Ghaitsa</div>
                        </div>
                        <div class="member-card">
                            <div class="member-avatar"><i class="fas fa-lightbulb"></i></div>
                            <div class="member-role">Tim Kreatif</div>
                            <div class="member-name">Tiara / Geisha</div>
                        </div>
                    </div>

                </div>
            </section>

        </div>

        <!-- KOLOM KANAN (SIDEBAR REGISTRASI) -->
        <div class="content-right">
            <section id="daftar" class="card" style="border-color: var(--orange-accent); position: sticky; top: 90px;">
                <div class="card-title-container" style="border-bottom-color: var(--light-green);">
                    <i class="fas fa-user-plus" style="color: var(--orange-accent);"></i>
                    <h2 class="card-title">Pendaftaran</h2>
                </div>
                <p style="margin-bottom: 20px; font-size: 0.9rem; color: var(--text-muted);">Mari bergabung menjadi bagian dari agen relawan kemanusiaan muda Juresix! Isi formulir singkat di bawah ini:</p>
                
                <!-- FORM OTOMATIS BERBASIS AJAX -->
                <form id="regForm">
                    <input type="hidden" name="_subject" value="Pendaftaran Anggota Baru PMR JURESIX!">
                    <input type="hidden" name="_captcha" value="false">

                    <div class="form-group">
                        <label for="nama">Nama Lengkap</label>
                        <input type="text" id="nama" name="Nama Lengkap" class="form-control" placeholder="Contoh: Mochamad Sultan Agenta" required>
                    </div>
                    <div class="form-group">
                        <label for="kelas">Kelas</label>
                        <select id="kelas" name="Kelas" class="form-control" required>
                            <option value="">-- Pilih Kelas --</option>
                            <option value="7">Kelas 7</option>
                            <option value="8">Kelas 8</option>
                            <option value="9">Kelas 9</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="alasan">Motivasi Bergabung</label>
                        <textarea id="alasan" name="Motivasi/Alasan" class="form-control" rows="4" placeholder="Tuliskan alasan atau harapanmu masuk PMR..." required></textarea>
                    </div>
                    <button type="submit" id="submitBtn" class="btn-submit">
                        <span>Kirim Formulir</span> <i class="fas fa-paper-plane"></i>
                    </button>
                    
                    <!-- Kotak Status Notifikasi Otomatis -->
                    <div id="formStatus" class="form-status"></div>
                </form>
            </section>
        </div>

    </div>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-col">
                <h3>PMR JURESIX</h3>
                <p>Unit kegiatan ekstrakurikuler Palang Merah Remaja Madya SMP Negeri 6 Cimahi. Senantiasa mengabdi secara tulus, ceria, dan bersahabat.</p>
            </div>
            <div class="footer-col">
                <h3>Menu Navigasi</h3>
                <ul class="footer-links">
                    <li><a href="#tentang">Tentang Kami</a></li>
                    <li><a href="#manfaat">Manfaat PMR</a></li>
                    <li><a href="#penanganan">Panduan First Aid</a></li>
                    <li><a href="#struktur">Struktur Anggota</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Sekretariat</h3>
                <p><i class="fas fa-map-location-dot"></i>Jl. Jenderal Gatot Subroto No.19, Kelurahan Karangmekar, Kecamatan Cimahi Tengah, Kota Cimahi, Jawa Barat 40523 .</p>
                <p style="margin-top: 10px;">
                    <a href="https://www.instagram.com/juresixx?igsh=MTlrb3VpdXE4M3J2bw==" target="_blank" style="color: white; text-decoration: none;">
                        <i class="fab fa-instagram"></i> @juresixx
                    </a>
                </p>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2026 PMR JURESIX SMPN 6 CIMAHI. Dikembangkan dengan tema <i class="fas fa-heart" style="color: #E74C3C;"></i> Kemanusiaan & <i class="fas fa-dragon"></i> Dinosaurus Lucu.
        </div>
    </footer>

    <!-- JAVASCRIPT UNTUK PENGIRIMAN OTOMATIS DI BELAKANG LAYAR -->
    <script>
        document.getElementById('regForm').addEventListener('submit', function(e) {
            e.preventDefault(); // Mencegah halaman reload atau pindah website

            const form = this;
            const submitBtn = document.getElementById('submitBtn');
            const statusDiv = document.getElementById('formStatus');

            // Mengubah status tombol menjadi sedang memproses
            submitBtn.disabled = true;
            submitBtn.querySelector('span').innerText = 'Mengirim...';
            statusDiv.style.display = 'none';

            // Mengambil semua data inputan dari formulir
            const formData = new FormData(form);

            // Mengirim data menggunakan Fetch API secara asinkronus ke FormSubmit
            fetch('https://formsubmit.co/ajax/juresixx6@gmail.com', {
                method: 'POST',
                body: formData,
                headers: {
                    'Accept': 'application/json'
                }
            })
            .then(response => {
                if (response.ok) {
                    // Notifikasi jika berhasil dikirim
                    statusDiv.className = 'form-status success';
                    statusDiv.innerHTML = '<i class="fas fa-circle-check"></i> Pendaftaran berhasil terkirim secara otomatis!';
                    statusDiv.style.display = 'block';
                    form.reset(); // Mengosongkan kembali form isi
                } else {
                    throw new Error('Gagal mengirim');
                }
            })
            .catch(error => {
                // Notifikasi jika terjadi gangguan koneksi/sistem
                statusDiv.className = 'form-status error';
                statusDiv.innerHTML = '<i class="fas fa-circle-xmark"></i> Terjadi kesalahan, coba lagi nanti.';
                statusDiv.style.display = 'block';
            })
            .finally(() => {
                // Mengembalikan keadaan tombol seperti semula
                submitBtn.disabled = false;
                submitBtn.querySelector('span').innerText = 'Kirim Formulir';
            });
        });
    </script>

</body>
</html>
