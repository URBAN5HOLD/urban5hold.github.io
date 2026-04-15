<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Officielle</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* التنظيف الشامل - منع أي بياض أو خطوط نهائيا */
        * { 
            margin: 0; padding: 0; box-sizing: border-box; 
            outline: none !important; border: none !important; 
            text-decoration: none !important; box-shadow: none !important;
            background: none !important; -webkit-tap-highlight-color: transparent;
        }

        html, body { 
            width: 100%; background-color: #000 !important; 
            scroll-snap-type: y mandatory; scroll-behavior: smooth; 
            font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden;
        }

        /* الشعار نقي 100% */
        .logo-fixed { 
            position: fixed; top: 25px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; 
            letter-spacing: 10px; color: #fff !important; pointer-events: none;
        }

        /* السهم الجانبي */
        .scroll-trigger { position: fixed; bottom: 8%; right: 25px; width: 50px; height: 50px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; background: rgba(255,255,255,0.05) !important; border-radius: 50%; }
        .arrow-icon { width: 15px; height: 15px; border-right: 3px solid var(--color) !important; border-bottom: 3px solid var(--color) !important; transform: rotate(45deg); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }

        /* الأقسام والضباب */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding-bottom: 100px; background-color: #000 !important; }
        
        .glow-overlay {
            position: absolute; top: 35%; left: 50%; transform: translate(-50%, -50%);
            width: 550px; height: 550px;
            background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 75%) !important;
            opacity: 0.4; z-index: 0; pointer-events: none;
        }

        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .v-header-sauvage { width: 85%; margin: 0 auto; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 50px 0; position: relative; z-index: 2; }
        .img-bottle { width: 35%; max-width: 150px; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.9)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.3rem; color: #fff !important; letter-spacing: 7px; margin: 15px 0; }
        .perfume-sub { font-size: 0.75rem; color: var(--color) !important; letter-spacing: 5px; text-transform: uppercase; font-weight: 600; }

        /* الصفوف وتوزيع الصور والمعلومات */
        .row { display: flex; align-items: center; width: 100%; padding: 70px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; }
        .img-box img { width: 100%; border-radius: 3px; display: block; }
        
        .txt-box { width: 50%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.4rem; margin-bottom: 25px; color: var(--color) !important; letter-spacing: 2px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .txt-box p { font-size: 0.95rem; line-height: 1.8; color: #ccc !important; font-weight: 300; margin-bottom: 18px; }
        .highlight { color: #fff !important; font-weight: 600; margin-right: 6px; text-transform: uppercase; font-size: 0.85rem; }
        
        /* شراء */
        .purchase-area { 
            max-width: 1100px; margin: 60px auto; display: flex; gap: 50px; padding: 50px; 
            border: 1px solid rgba(255,255,255,0.08) !important; width: 90%; 
            background: rgba(255,255,255,0.03) !important; position: relative; z-index: 2;
        }
        .mini-thumb { width: 110px; height: 110px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1) !important; }
        
        .size-container { display: flex; gap: 15px; margin-top: 25px; }
        .size-box { flex: 1; padding: 20px; border: 1px solid rgba(255,255,255,0.1) !important; text-align: center; cursor: pointer; transition: 0.4s; color: #fff; }
        .size-box span { display: block; font-size: 10px; color: #777; margin-top: 5px; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.07) !important; }

        input { width: 100%; padding: 22px 0; margin-bottom: 20px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.2) !important; }
        .order-btn { width: 100%; padding: 25px; background-color: #fff !important; color: #000 !important; font-weight: 800; font-size: 1.2rem; cursor: pointer; letter-spacing: 5px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 8%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 30px; }
        }

        /* COLORS */
        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.45); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.45); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.45); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.45); }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="glow-overlay"></div>
        <div class="v-header-sauvage"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>Sauvage Elixir réinterprète la signature iconique de Sauvage avec une concentration inouïه.</p>
                <p><span class="highlight">Pour :</span> Lui<br>
                   <span class="highlight">Il est :</span> Puissant et Noble<br>
                   <span class="highlight">Occasion :</span> Soirées d'Exception<br>
                   <span class="highlight">Famille :</span> AROMATIQUE Épicée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box">
                <h3>Notes Olfactives</h3>
                <p><span class="highlight">Notes de Tête :</span> Pamplemousse & Épices<br>
                   <span class="highlight">Notes de Cœur :</span> Lavande de Nyons AOP<br>
                   <span class="highlight">Notes de Fond :</span> Bois de Santal & Réglisse</p>
                <p><span class="highlight">Sillage :</span> Très puissant (Reste actif plus de 10h)</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0">SAUVAGE ELIXIR</h4><p style="color:#555; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/sauvage-thumb.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input placeholder="NOM COMPLET"><input placeholder="TÉLÉPHONE"><input placeholder="VILLE"><button type="button" class="order-btn">COMMANDER | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="glow-overlay"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>Un parfum boisé et ambré d'une sensualité irrésistible. Captivant et Audacieux.</p>
                <p><span class="highlight">Pour :</span> Lui<br><span class="highlight">Il est :</span> Mystérieux</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box">
                <h3>Notes Olfactives</h3>
                <p><span class="highlight">Tête :</span> Poivre Rose<br><span class="highlight">Cœur :</span> Sauge & Lavande<br><span class="highlight">Fond :</span> Vanille & Châtaigne</p>
                <p><span class="highlight">Sillage :</span> Intense et Durable</p>
            </div>
        </div>
        </section>

    <section class="product-section libre-t" id="sec3">
        <div class="glow-overlay"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE INTENSE</h1>
            <div class="perfume-sub">EAU DE PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>Libre Intense célèbre la liberté d’une femme audacieuse.</p>
                <p><span class="highlight">Pour :</span> Elle<br>
                   <span class="highlight">Elle est :</span> Royale & Audacieuse<br>
                   <span class="highlight">Occasion :</span> Luxe & Soirée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Mandarine & Bergamote<br>
                   <span class="highlight">Notes de Cœur :</span> Lavande & Fleur d'Oranger du Maroc<br>
                   <span class="highlight">Notes de Fond :</span> Vanille de Madagascar & Ambre Gris</p>
                <p><span class="highlight">Tenue :</span> Jusqu'à 10h de sillage puissant</p>
            </div>
        </div>
        </section>

    <section class="product-section gg-t" id="sec4">
        <div class="glow-overlay"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>La douceur du jasmin et l'énivrante fève tonka révèlent le côté mystérieux.</p>
                <p><span class="highlight">Pour :</span> Elle<br>
                   <span class="highlight">Elle est :</span> Séductrice et Puissante<br>
                   <span class="highlight">Occasion :</span> Le jour et la nuit<br>
                   <span class="highlight">Famille :</span> AMBRÉE Florale</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-right.jpg"></div>
            <div class="txt-box">
                <h3>Notes Olfactives</h3>
                <p><span class="highlight">Note de Tête :</span> Amande (5-15 min)<br>
                   <span class="highlight">Note de Cœur :</span> Jasmin & Tubéreuse (20-60 min)<br>
                   <span class="highlight">Note de Fond :</span> Fève Tonka & Cacao (jusqu'à 6h)</p>
                <p><span class="highlight">Ingrédients :</span> Tubéreuse d’Inde & Jasmin d’Arabie</p>
            </div>
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
        let currentIdx = 0;
        document.getElementById('scrollBtn').onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView({ behavior: 'smooth' });
        };
    </script>
</body>
</html>
