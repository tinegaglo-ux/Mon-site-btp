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
