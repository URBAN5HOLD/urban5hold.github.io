<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Officielle</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --bg: #000; }
        html, body { width: 100%; margin: 0; padding: 0; overflow-x: hidden; background-color: var(--bg); scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { box-sizing: border-box; outline: none; -webkit-tap-highlight-color: transparent; }

        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 8px; color: #fff; }

        .scroll-trigger { position: fixed; bottom: 15%; right: 25px; width: 50px; height: 50px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; }
        .arrow-icon { width: 20px; height: 20px; border-right: 2.5px solid var(--current-color); border-bottom: 2.5px solid var(--current-color); transform: rotate(45deg); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 100% { transform: rotate(45deg) translate(0,0); } 50% { transform: rotate(45deg) translate(5px,5px); } }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding-bottom: 60px; }
        .v-header-sauvage { width: 85%; margin: 0 auto; line-height: 0; }
        .v-header { width: 100%; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 30px 0; }
        .img-bottle { width: 40%; max-width: 150px; margin: 0 auto; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; letter-spacing: 6px; margin: 10px 0; border: none !important; }
        .perfume-sub { font-size: 0.7rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; }

        .row { display: flex; align-items: flex-start; width: 100%; padding: 25px 8%; gap: 40px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 2px; }
        
        /* حيدت المربعات البيضاء نهائيا */
        .txt-box { width: 55%; color: #fff; text-align: left; background: transparent !important; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1rem; margin-bottom: 15px; color: var(--color); letter-spacing: 1px; border: none !important; background: transparent !important; }
        .txt-box p { font-size: 0.8rem; line-height: 1.6; color: #ccc; font-weight: 300; margin-bottom: 12px; background: transparent !important; }
        .txt-box ul { padding-left: 15px; margin: 10px 0; list-style-type: none; background: transparent !important; }
        .txt-box li { font-size: 0.75rem; color: #aaa; margin-bottom: 8px; line-height: 1.4; background: transparent !important; }
        .highlight { color: #fff; font-weight: 600; background: transparent !important; }

        /* منطقة الشراء المصلحة */
        .purchase-area { max-width: 1000px; margin: 30px auto; display: flex; gap: 30px; padding: 30px; border-top: 1px solid rgba(255,255,255,0.05); width: 90%; }
        .mini-thumb { width: 85px; height: 85px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1); }
        
        .size-container { display: flex; gap: 10px; margin-top: 10px; }
        .size-box { flex: 1; padding: 12px; border: 1px solid rgba(255,255,255,0.1); text-align: center; color: #fff; cursor: pointer; transition: 0.3s; }
        /* كلمة Sprays بدون رموز */
        .size-box span { display: block; font-size: 0.6rem; color: #888; margin-top: 4px; text-transform: uppercase; }
        .active-size { border-color: var(--color); background: rgba(255,255,255,0.05); }
        .active-size span { color: var(--color); }

        /* حيدت الخطوط الزرقاء الجانبية وزدت في وضوح الكتابة */
        input { 
            width: 100%; padding: 18px 0; margin-bottom: 10px; 
            background: transparent !important; color: #fff; 
            border: none !important; border-bottom: 1px solid rgba(255,255,255,0.2) !important; 
            font-family: 'Montserrat'; font-size: 0.9rem; border-radius: 0;
        }
        input::placeholder { color: #aaa; text-transform: uppercase; letter-spacing: 1px; }
        
        .order-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-family: 'Montserrat'; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 2px; border: none; margin-top: 10px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 20px 8%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; }
        }

        .sauv-t { --color: #4A90E2; }
        .stron-t { --color: #CD7F32; }
        .libre-t { --color: #D4AF37; }
        .gg-t { --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
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
                <p>La force et la noblesse d’une fraîcheur poussée à l’extrême. Sauvage Elixir réinterprète la signature iconique de Sauvage.</p>
                <p><span class="highlight">Pour :</span> Lui | <span class="highlight">Il est :</span> Puissant<br>
                <span class="highlight">Occasion :</span> Soirées d'exception<br>
                <span class="highlight">Famille :</span> AROMATIQUE Épicée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Pamplemousse & Épices<br>
                <span class="highlight">Notes de Cœur :</span> Lavande de Nyons<br>
                <span class="highlight">Notes de Fond :</span> Sillage intense, tenue exceptionnelle (12h+).</p>
                <ul>
                    <li><span class="highlight">Notes de tête :</span> Première impression (5-15 min).</li>
                    <li><span class="highlight">Notes de fond :</span> Signature longue durée qui reste sur la peau.</li>
                </ul>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'; margin:0">SAUVAGE ELIXIR</h4><p style="color:#555; font-size:10px">EXTRAIT DE PARFUM</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML<span>80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">INTENSELY / EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>L'intensité d'un amour vibrant. Stronger With You Intensely est une fragrance addictive et boisée.</p>
                <p><span class="highlight">Pour :</span> Lui | <span class="highlight">Il est :</span> Captivant<br>
                <span class="highlight">Occasion :</span> Quotidien & Rendez-vous<br>
                <span class="highlight">Famille :</span> AMBRÉE Boisée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Poivre Rose & Genévrier<br>
                <span class="highlight">Notes de Cœur :</span> Lavande & Sauge<br>
                <span class="highlight">Notes de Fond :</span> Sillage sucré et chaud, tenue longue durée (8h+).</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'; margin:0">STRONGER WITH YOU</h4><p style="color:#555; font-size:10px">EAU DE PARFUM</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec2')">5ML<span>80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec2')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
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
                <p>Libre Intense célèbre la liberté d'une femme audacieuse. Une dualité florale brûlante.</p>
                <p><span class="highlight">Pour :</span> Elle | <span class="highlight">Elle est :</span> Royale<br>
                <span class="highlight">Occasion :</span> Luxe & Soirée</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Mandarine & Bergamote<br>
                <span class="highlight">Notes de Cœur :</span> Lavande & Fleur d'Oranger<br>
                <span class="highlight">Notes de Fond :</span> Sillage puissant, reste actif jusqu'à 10h.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'; margin:0">LIBRE INTENSE</h4><p style="color:#555; font-size:10px">EAU DE PARFUM</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec3')">5ML<span>80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec3')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>La douceur du jasmin renforce l’éclat de Good Girl. Le côté mystérieux est révélé par le cacao.</p>
                <p><span class="highlight">Pour :</span> Elle | <span class="highlight">Elle est :</span> Puissante</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Amande<br>
                <span class="highlight">Notes de Cœur :</span> Jasmin & Tubéreuse<br>
                <span class="highlight">Notes de Fond :</span> Sillage sensuel, reste perceptible pendant 7h+.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'; margin:0">GOOD GIRL</h4><p style="color:#555; font-size:10px">EAU DE PARFUM</p></div>
                    <img src="assets/gg-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <script>
        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerHTML = `COMMANDER | ${price} DH`;
        }

        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        let currentIdx = 0;
        document.getElementById('scrollBtn').onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView();
        };

        window.onscroll = () => {
            const scrollPos = window.scrollY + window.innerHeight / 2;
            sections.forEach((id, index) => {
                const el = document.getElementById(id);
                if (scrollPos >= el.offsetTop && scrollPos < el.offsetTop + el.offsetHeight) {
                    const color = getComputedStyle(el).getPropertyValue('--color');
                    document.documentElement.style.setProperty('--current-color', color);
                    currentIdx = index;
                }
            });
        };
    </script>
</body>
</html>
