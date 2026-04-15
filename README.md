<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Officielle</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* تنظيف شامل لمنع البياض والخطوط */
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

        .logo-fixed { 
            position: fixed; top: 25px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; 
            letter-spacing: 10px; color: #fff !important; pointer-events: none;
        }

        /* السهم الذكي اللي كيتبدل لونو */
        .scroll-trigger { 
            position: fixed; bottom: 5%; right: 25px; width: 50px; height: 50px; 
            z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; 
            background: rgba(255,255,255,0.05) !important; border-radius: 50%;
            transition: 0.5s ease;
        }
        .arrow-icon { 
            width: 15px; height: 15px; 
            border-right: 3px solid var(--current-arrow-color, #fff) !important; 
            border-bottom: 3px solid var(--current-arrow-color, #fff) !important; 
            transform: rotate(45deg); animation: bounce 2s infinite; 
        }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }

        /* الأقسام والضباب الملون */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        
        /* الضباب ورا القرعة وفي بلاصة التفاصيل */
        .glow-bg {
            position: absolute; width: 100%; height: 100%; top: 0; left: 0; z-index: 0; pointer-events: none;
        }
        .glow-center { position: absolute; top: 35%; left: 50%; transform: translate(-50%, -50%); width: 500px; height: 500px; background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 70%) !important; opacity: 0.4; }
        .glow-details { position: absolute; width: 40%; height: 40%; background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 80%) !important; opacity: 0.25; z-index: -1; }

        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .v-header-sauvage { width: 85%; margin: 0 auto; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 50px 0; position: relative; z-index: 2; }
        .img-bottle { width: 35%; max-width: 140px; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.9)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff !important; letter-spacing: 6px; margin: 15px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        /* الصفوف والمعلومات */
        .row { display: flex; align-items: center; width: 100%; padding: 60px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; position: relative; }
        .img-box img { width: 100%; border-radius: 2px; display: block; }
        
        .txt-box { width: 50%; text-align: left; position: relative; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.3rem; margin-bottom: 25px; color: var(--color) !important; letter-spacing: 2px; }
        .txt-box p { font-size: 0.9rem; line-height: 1.8; color: #ccc !important; font-weight: 300; margin-bottom: 15px; }
        .highlight { color: #fff !important; font-weight: 600; margin-right: 5px; }
        
        /* منطقة الشراء */
        .purchase-area { 
            max-width: 1100px; margin: 50px auto; display: flex; gap: 40px; padding: 45px; 
            border: 1px solid rgba(255,255,255,0.08) !important; width: 90%; 
            background: rgba(255,255,255,0.02) !important; position: relative; z-index: 2;
        }
        .mini-thumb { width: 100px; height: 100px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1) !important; }
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-box { flex: 1; padding: 18px; border: 1px solid rgba(255,255,255,0.1) !important; text-align: center; cursor: pointer; color: #fff; }
        .size-box span { display: block; font-size: 9px; color: #666; margin-top: 4px; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05) !important; }

        input { width: 100%; padding: 20px 0; margin-bottom: 15px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.2) !important; background: transparent !important; }
        .order-btn { width: 100%; padding: 22px; background-color: #fff !important; color: #000 !important; font-weight: 800; font-size: 1.1rem; cursor: pointer; letter-spacing: 4px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 8%; gap: 40px; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 25px; }
        }

        /* COLORS */
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
        <div class="glow-bg"><div class="glow-center"></div></div>
        <div class="v-header-sauvage"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="top:-10%; left:-10%;"></div>
                <h3>LA FRAGRANCE</h3>
                <p>Sauvage Elixir réinterprète la signature iconique de Sauvage avec une concentration inouïe.</p>
                <p><span class="highlight">Pour :</span> Lui<br><span class="highlight">Il est :</span> Puissant et Noble</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="bottom:-10%; right:-10%;"></div>
                <h3>NOTES OLFACTIVES</h3>
                <p><span class="highlight">Tête :</span> Pamplemousse & Épices<br><span class="highlight">Cœur :</span> Lavande de Nyons AOP<br><span class="highlight">Fond :</span> Bois de Santal & Réglisse</p>
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
        <div class="glow-bg"><div class="glow-center"></div></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="top:-10%; left:-10%;"></div>
                <h3>LA FRAGRANCE</h3>
                <p>Un parfum boisé et ambré d'une sensualité irrésistible. Captivant et Audacieux.</p>
                <p><span class="highlight">Pour :</span> Lui<br><span class="highlight">Sillage :</span> Intense</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="bottom:-10%; right:-10%;"></div>
                <h3>NOTES OLFACTIVES</h3>
                <p><span class="highlight">Tête :</span> Poivre Rose<br><span class="highlight">Cœur :</span> Sauge & Lavande<br><span class="highlight">Fond :</span> Vanille & Châtaigne</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0">STRONGER WITH YOU</h4><p style="color:#555; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/stronger-thumb.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec2')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec2')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input placeholder="NOM COMPLET"><input placeholder="TÉLÉPHONE"><input placeholder="VILLE"><button type="button" class="order-btn">COMMANDER | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="glow-bg"><div class="glow-center"></div></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE INTENSE</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="top:-10%; left:-10%;"></div>
                <h3>LA FRAGRANCE</h3>
                <p>Libre Intense célèbre la liberté d’une femme audacieuse.</p>
                <p><span class="highlight">Elle est :</span> Royale & Audacieuse<br><span class="highlight">Occasion :</span> Luxe & Soirée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-details" style="bottom:-10%; right:-10%;"></div>
                <h3>NOTES OLFACTIVES</h3>
                <p><span class="highlight">Cœur :</span> Lavande & Fleur d'Oranger du Maroc<br><span class="highlight">Fond :</span> Vanille de Madagascar & Ambre Gris<br><span class="highlight">Tenue :</span> Jusqu'à 10h</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0">LIBRE INTENSE</h4><p style="color:#555; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/libre-thumb.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec3')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec3')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input placeholder="NOM COMPLET"><input placeholder="TÉLÉPHONE"><input placeholder="VILLE"><button type="button" class="order-btn">COMMANDER | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="glow-bg"><div class="glow-center"></div></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-left.jpg"></div> <div class="txt-box">
                <div class="glow-details" style="top:-10%; left:-10%;"></div>
                <h3>LA FRAGRANCE</h3>
                <p>La douceur du jasmin et l’énivrante fève tonka révèlent le côté mystérieux.</p>
                <p><span class="highlight">Elle est :</span> Séductrice et Puissante<br>
                   <span class="highlight">Occasion :</span> Le jour et la nuit<br>
                   <span class="highlight">Famille :</span> AMBRÉE Florale</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-right.jpg"></div> <div class="txt-box">
                <div class="glow-details" style="bottom:-10%; right:-10%;"></div>
                <h3>NOTES OLFACTIVES</h3>
                <p><span class="highlight">Tête :</span> Amande (5-15 min)<br>
                   <span class="highlight">Cœur :</span> Jasmin & Tubéreuse (20-60 min)<br>
                   <span class="highlight">Fond :</span> Fève Tonka & Cacao (jusqu'à 6h)</p>
                <p><span class="highlight">Ingrédients :</span> Tubéreuse d'Inde & Jasmin d'Arabie</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0">GOOD GIRL</h4><p style="color:#555; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/gg-thumb.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>± 80 RASHAT</span></div> <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>± 160 RASHAT</span></div> </div>
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

        // وظيفة تحديث السهم مع السكرول
        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -200 && rect.top <= 200) {
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
