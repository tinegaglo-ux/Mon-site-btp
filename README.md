<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Giotino's BTP Building | Bâtissons pour demain</title>
    <!-- Google Fonts pour une typographie professionnelle -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome pour les icônes -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- STYLES GÉNÉRAUX --- */
        :root {
            --primary-color: #0f4c81; /* Bleu construction */
            --secondary-color: #f4b41a; /* Jaune sécurité / accent */
            --dark-color: #1a1a1a;
            --light-grey: #f8f9fa;
            --text-color: #4a4a4a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            scroll-behavior: smooth;
        }

        h1, h2, h3 {
            color: var(--dark-color);
            font-weight: 700;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 0;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn:hover {
            background-color: #0b365e;
            transform: translateY(-2px);
        }

        .btn-whatsapp {
            background-color: #25D366;
        }

        .btn-whatsapp:hover {
            background-color: #128C7E;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background-color: var(--secondary-color);
            margin: 10px auto 0 auto;
            border-radius: 2px;
        }

        /* --- HEADER & NAVIGATION --- */
        header {
            background-color: #fff;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 5%;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        .logo span {
            color: var(--dark-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* --- HERO SECTION --- */
        #home {
            background: linear-gradient(rgba(15, 76, 129, 0.7), rgba(26, 26, 26, 0.8)), url('https://images.unsplash.com/photo-1541888946425-d81bb19240f5?q=80&w=1200') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding-top: 80px;
        }

        .hero-content h1 {
            color: #fff;
            font-size: 3.5rem;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }

        .hero-content p {
            font-size: 1.5rem;
            font-style: italic;
            margin-bottom: 30px;
            color: #f0f0f0;
        }

        /* --- SECTION A PROPOS --- */
        #about {
            background-color: #fff;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .about-img img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        /* --- SECTION SERVICES --- */
        #services {
            background-color: var(--light-grey);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background-color: #fff;
            padding: 40px 30px;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .service-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .service-card h3 {
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        /* --- SECTION PORTFOLIO --- */
        #portfolio {
            background-color: #fff;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .portfolio-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            height: 250px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(15, 76, 129, 0.9);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff;
            opacity: 0;
            transition: opacity 0.3s ease;
            padding: 20px;
            text-align: center;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-overlay h4 {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        /* --- SECTION CONTACT --- */
        #contact {
            background-color: var(--light-grey);
            text-align: center;
        }

        .contact-box {
            background-color: #fff;
            max-width: 600px;
            margin: 0 auto;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .contact-box p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .contact-info {
            margin-top: 30px;
            font-weight: 600;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--dark-color);
            color: #fff;
            text-align: center;
            padding: 30px 0;
            font-size: 0.9rem;
        }

        /* --- RESPONSIVE MOBILE --- */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .hero-content h1 {
                font-size: 2.3rem;
            }
            .hero-content p {
                font-size: 1.1rem;
            }
            .about-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- BARRE DE NAVIGATION -->
    <header>
        <nav>
            <div class="logo">Giotino's <span>BTP Building</span></div>
            <ul class="nav-links">
                <li><a href="#home">Accueil</a></li>
                <li><a href="#about">À Propos</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Réalisations</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- SECTION ACCUEIL (HERO) -->
    <section id="home">
        <div class="hero-content">
            <h1>Giotino's BTP Building</h1>
            <p>« Bâtissons pour demain »</p>
            <a href="#contact" class="btn">Discutons de votre projet</a>
        </div>
    </section>

    <!-- SECTION À PROPOS -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">À Propos de Nous</h2>
            <div class="about-grid">
                <div class="about-text">
                    <h3>Votre partenaire de confiance en Génie Civil</h3>
                    <p>Basé au Togo, <strong>Giotino's BTP Building</strong> met son expertise technique au service de vos projets de construction et d'aménagement.</p>
                    <p>Qu'il s'agisse de concevoir des plans détaillés, de sécuriser vos structures grâce à des calculs de ferraillage précis ou d'assurer le suivi rigoureux de vos chantiers, nous veillons au respect des normes et à la qualité d'exécution à chaque étape.</p>
                </div>
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?q=80&w=600" alt="Chantier de génie civil">
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION SERVICES -->
    <section id="services">
        <div class="container">
            <h2 class="section-title">Nos Services</h2>
            <div class="services-grid">
                <!-- Service 1 -->
                <div class="service-card">
                    <i class="fa-solid fa-layer-group"></i>
                    <h3>Conception 2D / 3D</h3>
                    <p>Modélisation de plans de bâtiments modernes, fonctionnels et sur-mesure selon vos exigences et votre budget.</p>
                </div>
                <!-- Service 2 -->
                <div class="service-card">
                    <i class="fa-solid fa-calculator"></i>
                    <h3>Structure & Ferraillage</h3>
                    <p>Calculs de structures en béton armé pour garantir la solidité, la durabilité et la sécurité absolue de vos ouvrages.</p>
                </div>
                <!-- Service 3 -->
                <div class="service-card">
                    <i class="fa-solid fa-helmet-safety"></i>
                    <h3>Suivi de Chantier</h3>
                    <p>Pilotage, gestion technique et supervision des travaux sur le terrain pour s'assurer de la bonne exécution des plans.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION RÉALISATIONS (PORTFOLIO) -->
    <section id="portfolio">
        <div class="container">
            <h2 class="section-title">Nos Réalisations</h2>
            <div class="portfolio-grid">
                <!-- Élément 1 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=400" alt="Plan 3D">
                    <div class="portfolio-overlay">
                        <h4>Modélisation & Conception 3D</h4>
                        <p>Plans architecturaux de villas modernes</p>
                    </div>
                </div>
                <!-- Élément 2 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1590069261209-f8e9b8642343?q=80&w=400" alt="Ferraillage structure">
                    <div class="portfolio-overlay">
                        <h4>Étude de Structure</h4>
                        <p>Plans de ferraillage et coulage de dalle</p>
                    </div>
                </div>
                <!-- Élément 3 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1531834685032-c34bf0d84c77?q=80&w=400" alt="Suivi de chantier">
                    <div class="portfolio-overlay">
                        <h4>Suivi Technique</h4>
                        <p>Supervision active de chantiers à Lomé</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION CONTACT -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Contactez-nous</h2>
            <div class="contact-box">
                <p>Vous avez un projet de construction ou besoin d'une étude technique ? Envoyez-nous directement un message pour obtenir un devis ou planifier un rendez-vous.</p>
                
                <!-- Lien WhatsApp direct mis à jour avec le numéro +228 96770819 -->
                <a href="https://wa.me/22896770819" target="_blank" class="btn btn-whatsapp">
                    <i class="fa-brands fa-whatsapp"></i> Contactez-nous sur WhatsApp
                </a>
                
                <div class="contact-info">
                    <p><i class="fa-solid fa-phone"></i> WhatsApp : +228 96 77 08 19</p>
                    <p><i class="fa-solid fa-location-dot"></i> Lomé, Togo</p>
                </div>
            </div>
        </div>
    </section>

    <!-- PIED DE PAGE -->
    <footer>
        <div class="container-footer">
            <p>&copy; 2026 Giotino's BTP Building. Tous droits réservés.</p>
        </div>
    </footer>

</body>
</html>
# Mon-site-btp
Mon site btp
index.html<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Giotino's BTP Building - Ingénierie & Construction au Togo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: { 600: '#0284c7', 900: '#0c4a6e' },
                        accent: { 500: '#f59e0b' }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-slate-50 text-slate-800">

    <!-- HEADER -->
    <header class="bg-white shadow-sm sticky top-0 z-50 p-6 flex justify-between items-center">
        <div>
            <span class="text-xl font-extrabold text-brand-900 block">GIOTINO'S</span>
            <span class="text-xs font-semibold text-accent-500">BTP BUILDING</span>
        </div>
        <a href="#contact" class="bg-brand-600 text-white px-6 py-2 rounded-xl font-bold">Contact</a>
    </header>

    <main>
        <!-- HERO -->
        <section class="bg-brand-900 text-white py-20 px-6 text-center">
            <h1 class="text-4xl font-extrabold mb-6">Bâtissons l'avenir avec rigueur</h1>
            <p class="mb-8 text-slate-300">Conception, structure et suivi de chantier à Lomé.</p>
            <a href="https://wa.me/22896770819" class="bg-emerald-600 text-white px-8 py-4 rounded-xl font-bold">Contactez-nous sur WhatsApp</a>
        </section>

        <!-- CONTACT INFO -->
        <section id="contact" class="py-20 px-6">
            <h2 class="text-2xl font-bold mb-8 text-center">Nos coordonnées</h2>
            <div class="max-w-md mx-auto space-y-4">
                <div class="bg-white p-4 rounded-xl border border-slate-200">
                    <i class="fa-brands fa-whatsapp text-emerald-600 mr-2"></i> WhatsApp: +228 96 77 08 19
                </div>
                <div class="bg-white p-4 rounded-xl border border-slate-200">
                    <i class="fa-solid fa-envelope text-brand-600 mr-2"></i> Email: tinegaglo@gmail.com
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer class="bg-brand-950 text-slate-400 py-10 text-center text-sm">
        &copy; 2026 Giotino's BTP Building.
    </footer>
</body>
</html>
