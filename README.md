<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gondviselés Gyógyszertár - Orgovány</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body { font-family: 'Segoe UI', Arial, sans-serif; line-height: 1.6; color: #333; padding-top: 60px; }

        /* --- NAVIGÁCIÓ --- */
        nav {
            background-color: #1a1a1a;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
            height: 60px;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
        }

        .logo { font-size: 1.1rem; font-weight: bold; color: white; text-decoration: none; }
        .nav-links { display: flex; list-style: none; }
        .nav-links li { margin-left: 20px; }
        .nav-links a { color: white; text-decoration: none; font-size: 0.95rem; transition: 0.3s; }
        .nav-links a:hover { color: #4CAF50; }
        .hamburger { display: none; cursor: pointer; font-size: 1.5rem; color: white; }

        /* --- FEJLÉC (HERO) --- */
        .hero {
            height: 65vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 20px;
            /* Biztonsági sötétzöld háttér + a Te képed közvetlen linkkel */
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://i.ibb.co/G4VhqZVY/20250731-141420.jpg') no-repeat center center/cover;
            background-color: #1b4d3e; 
        }

        .hero h1 { font-size: 3rem; text-shadow: 2px 2px 10px rgba(0,0,0,0.5); margin-bottom: 10px; }
        .hero p { font-size: 1.2rem; }

        /* --- SZEKCIÓK --- */
        section { padding: 80px 5%; max-width: 1100px; margin: 0 auto; text-align: center; }
        .section-title { font-size: 2.2rem; margin-bottom: 30px; color: #1a1a1a; }

        /* --- TÉRKÉP SZEKCIÓ --- */
        #terkep { background-color: #f8f9fa; }
        .map-container {
            width: 100%;
            max-width: 900px;
            margin: 0 auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
            background-color: #eee;
        }
        .map-container iframe {
            width: 100%;
            height: 450px;
            border: 0;
            display: block;
        }

        .address-box { margin-top: 25px; font-weight: 600; font-size: 1.2rem; }

        /* --- FACEBOOK --- */
        .facebook-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 70px;
            height: 70px;
            background-color: #1877F2;
            color: white;
            font-size: 35px;
            border-radius: 18px;
            text-decoration: none;
            margin-top: 20px;
            transition: 0.3s;
        }
        .facebook-link:hover { transform: translateY(-5px); }

        /* --- MOBIL --- */
        @media screen and (max-width: 768px) {
            .hamburger { display: block; }
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px;
                right: 0;
                background-color: #1a1a1a;
                width: 100%;
                padding: 30px 0;
            }
            .nav-links.active { display: flex; }
            .nav-links li { margin: 15px 0; }
            .hero h1 { font-size: 2.2rem; }
            .map-container iframe { height: 350px; }
        }
    </style>
</head>
<body>

    <nav>
        <a href="#" class="logo">Gondviselés Gyógyszertár</a>
        <div class="hamburger" onclick="toggleMenu()">
            <i class="fas fa-bars"></i>
        </div>
        <ul class="nav-links" id="menuList">
            <li><a href="#szolgaltatasok" onclick="toggleMenu()">Szolgáltatások</a></li>
            <li><a href="#rolunk" onclick="toggleMenu()">Rólunk</a></li>
            <li><a href="#terkep" onclick="toggleMenu()">Térkép</a></li>
            <li><a href="#kapcsolat" onclick="toggleMenu()">Kapcsolat</a></li>
        </ul>
    </nav>

    <header class="hero">
        <h1>Gondviselés Gyógyszertár</h1>
        <p>Szakértelem és gondoskodás Orgovány szívében.</p>
    </header>

    <section id="szolgaltatasok">
        <h2 class="section-title">Szolgáltatások</h2>
        <p>Hamarosan itt találja részletes kínálatunkat.</p>
    </section>

    <section id="rolunk">
        <h2 class="section-title">Rólunk</h2>
        <p>Patikánk elkötelezett a helyi közösség egészsége mellett.</p>
    </section>

    <section id="terkep">
        <h2 class="section-title">Itt találsz minket</h2>
        <div class="map-container">
            <iframe 
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2745.289136365416!2d19.4636906!3d46.7592477!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47417e33c7ebf717%3A0x225c909c04ee2586!2sGondvisel%C3%A9s%20Gy%C3%B3gyszert%C3%A1r!5e0!3m2!1shu!2shu!4v1700000000000!5m2!1shu!2shu" 
                allowfullscreen="" 
                loading="lazy">
            </iframe>
        </div>
        <div class="address-box">
            <p><i class="fas fa-map-marker-alt" style="color: #e74c3c;"></i> 6077 Orgovány, Kossuth Lajos u. 65.</p>
        </div>
    </section>

    <section id="kapcsolat">
        <h2 class="section-title">Kapcsolat</h2>
        <p>Kövessen minket Facebook oldalunkon:</p>
        <a href="https://www.facebook.com/gondviselesgyogyszertar/" target="_blank" class="facebook-link">
            <i class="fab fa-facebook-f"></i>
        </a>
    </section>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('menuList');
            if (window.innerWidth <= 768) {
                menu.classList.toggle('active');
            }
        }
    </script>

</body>
</html>
