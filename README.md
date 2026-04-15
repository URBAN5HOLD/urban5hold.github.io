<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Privée</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { 
            margin: 0; padding: 0; box-sizing: border-box; 
            outline: none !important; border: none !important; 
            text-decoration: none !important; background: none !important;
            -webkit-tap-highlight-color: transparent;
        }

        html, body { 
            width: 100%; background-color: #000 !important; 
            scroll-snap-type: y mandatory; scroll-behavior: smooth; 
            font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden;
        }

        .logo-fixed { 
            position: fixed; top: 25px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; 
            letter-spacing: 10px; color: #fff !important; pointer-events: none;
        }

        /* السهم الجديد في منتصف الشاشة بدون دوارة */
        .scroll-trigger { 
            position: fixed; top: 50%; right: 20px; transform: translateY(-50%);
            width: 40px; height: 40px; z-index: 2000; cursor: pointer;
            display: flex; align-items: center; justify-content: center;
        }
        .arrow-icon { 
            width: 18px; height: 18px; 
            border-right: 3px solid var(--current-arrow-color, #fff) !important; 
            border-bottom: 3px solid var(--current-arrow-color, #fff) !important; 
            transform: rotate(45deg); animation: bounce 2s infinite;
            transition: 0.5s ease;
        }
        @keyframes bounce { 0%, 100% { transform: translateX(0) rotate(45deg); } 50% { transform: translateX(-5px) rotate(45deg); } }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        
        /* ضبابة مركزية خلف الزجاجة */
        .glow-center { 
            position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); 
            width: 500px; height: 500px; 
            background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 70%) !important; 
            opacity: 0.35; z-index: 0; pointer-events: none;
        }

        .v-header-sauvage { width: 85%; margin: 0 auto; position: relative; z-index: 1; line-height: 0; }
        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 40px 0; position: relative; z-index: 2; }
        .img-bottle { width: 32%; max-width: 130px; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff !important; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        /* تأثير الضبابة خلف النصوص */
        .text-glow-box {
            position: relative; padding: 25px; border-radius: 10px;
            background: radial-gradient(circle at center, var(--glow-color) 0%, rgba(0,0,0,0) 100%) !important;
            z-index: 2;
        }

        .row { display: flex; align-items: center; width: 100%; padding: 50px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 2px; display: block; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        
        .txt-box { width: 55%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.4rem; margin-bottom: 20px; color: var(--color) !important; letter-spacing: 2px; }
        .txt-box p { font-size: 0.95rem; line-height: 1.8; color: #eee !important; font-weight: 300; margin-bottom: 12px; }
        .highlight { color: var(--color) !important; font-weight: 600; text-transform: uppercase; font-size: 0.8rem; margin-right: 5px; }
        
        .purchase-area { 
            max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 40px; 
            border: 1px solid rgba(255,255,255,0.1) !important; width: 90%; 
            background: rgba(255,255,255,0.03) !important; position: relative; z-index: 2;
        }
        .mini-thumb { width: 90px; height: 90px; object-fit: cover; }
        .size-container { display: flex; gap: 15px; margin-top: 15px; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2) !important; text-align: center; cursor: pointer; transition: 0.3s; color: #fff; }
        .size-box span { display: block; font-size: 9px; color: #888; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.08) !important; }

        input { width: 100%; padding: 18px 0; margin-bottom: 15px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.3) !important; }
        .order-btn { width: 100%; padding: 22px; background-color: #fff !important; color: #000 !important; font-weight: 800; cursor: pointer; letter-spacing: 4px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 25px; }
        }

        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.4); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.4); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.4); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.4); }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="glow-center"></div>
        <div class="v-header-sauvage"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>LA FRAGRANCE</h3>
                <p>Une concentration inouïe où la fraîcheur emblématique de Sauvage s'enivre d'un cœur d'épices.</p>
                <p><span class="highlight">Caractère :</span> Puissant, Noble et Sauvage<br>
                <span class="highlight">Famille :</span> Aromatique Épicé</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>NOTES OFFICIELLES</h3>
                <p><span class="highlight">Tête :</span> Pamplemousse & Épices (Cannelle, Cardamome)<br>
                <span class="highlight">Cœur :</span> Essence de Lavande de Nyons AOP<br>
                <span class="highlight">Fond :</span> Bois de Santal & Réglisse</p>
                <p><span class="highlight">Performance :</span> Sillage extrême, tenue +12h.</p>
            </div></div>
        </div>
        </section>

    <section class="product-section stron-t" id="sec2">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>LA FRAGRANCE</h3>
                <p>Un parfum qui communique avec sensualité. L'alliance d'une vanille fumée et d'un accord marron glacé.</p>
                <p><span class="highlight">Style :</span> Moderne, Magnétique, Chaleureux.<br>
                <span class="highlight">Famille :</span> Fougère Oriental.</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>NOTES OFFICIELLES</h3>
                <p><span class="highlight">Tête :</span> Poivre Rose & Essence de Cardamome<br>
                <span class="highlight">Cœur :</span> Sauge Sclarée & Lavande<br>
                <span class="highlight">Fond :</span> Vanille & Châtaigne.</p>
            </div></div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE INTENSE</h1>
            <div class="perfume-sub">EAU DE PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>LA FRAGRANCE</h3>
                <p>La tension entre la lavande de France et la fleur d'oranger du Maroc poussée à son paroxysme.</p>
                <p><span class="highlight">Tempérament :</span> Royale et Audacieuse<br>
                <span class="highlight">Usage :</span> Soirées de Luxe</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-box">
                <h3>NOTES OFFICIELLES</h3>
                <p><span class="highlight">Tête :</span> Bergamote & Mandarine<br>
                <span class="highlight">Cœur :</span> Fleur d'Oranger & Orchidée Royale<br>
                <span class="highlight">Fond :</span> Vanille de Madagascar & Ambre Gris</p>
                <p><span class="highlight">Tenue :</span> Sillage puissant, reste actif jusqu'à 10h.</p>
            </div></div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-left.jpg"></div> <div class="txt-box"><div class="text-glow-box">
                <h3>LA FRAGRANCE</h3>
                <p>Un parfum audacieux et sophistiqué, inspiré par la vision unique de la dualité de la femme moderne.</p>
                <p><span class="highlight">Vibe :</span> Séductrice et Puissante<br>
                <span class="highlight">Famille :</span> Ambré Floral</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-right.jpg"></div> <div class="txt-box"><div class="text-glow-box">
                <h3>NOTES OFFICIELLES</h3>
                <p><span class="highlight">Note de Tête :</span> Amande (Éclat immédiat)<br>
                <span class="highlight">Note de Cœur :</span> Jasmin Sambac & Tubéreuse<br>
                <span class="highlight">Note de Fond :</span> Fève Tonka & Cacao (Sillage profond)</p>
                <p><span class="highlight">Évolution :</span> Note de fond qui dure jusqu'à 6h sur la peau.</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">GOOD GIRL</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/gg-thumb.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input placeholder="NOM COMPLET"><input placeholder="TÉLÉPHONE"><input placeholder="VILLE"><button type="button" class="order-btn">COMMANDER | 319 DH</button></form></div>
        </div>
    </section>

    <script>
        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerText = `COMMANDER | ${price} DH`;
        }

        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        const colors = ['#4A90E2', '#CD7F32', '#D4AF37', '#1a4d99'];
        let currentIdx = 0;

        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -300 && rect.top <= 300) {
                    currentIdx = index;
                    document.documentElement.style.setProperty('--current-arrow-color', colors[index]);
                }
            });
        });

        document.getElementById('scrollBtn').onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView({ behavior: 'smooth' });
        };
    </script>
</body>
</html>
