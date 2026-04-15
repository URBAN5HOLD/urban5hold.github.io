<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Officielle</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* 1. RESET القاسي لحل مشكل البياض والخطوط */
        * { 
            margin: 0; padding: 0; box-sizing: border-box; 
            outline: none; border: none !important; 
            text-decoration: none !important; box-shadow: none !important;
            -webkit-tap-highlight-color: transparent;
        }

        :root { --bg: #000; --current-color: #fff; }
        
        html, body { 
            width: 100%; background-color: #000 !important; 
            scroll-snap-type: y mandatory; scroll-behavior: smooth; 
            font-family: 'Montserrat', sans-serif; color: #fff;
            overflow-x: hidden;
        }

        /* 2. الشعار (VELOORIA) بدون أي خلفية أو خطوط */
        .logo-fixed { 
            position: fixed; top: 20px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; 
            letter-spacing: 8px; color: #fff; background: transparent !important;
            pointer-events: none;
        }

        /* 3. سهم التنقل */
        .scroll-trigger { position: fixed; bottom: 10%; right: 25px; width: 50px; height: 50px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; }
        .arrow-icon { width: 18px; height: 18px; border-right: 2.5px solid var(--current-color) !important; border-bottom: 2.5px solid var(--current-color) !important; transform: rotate(45deg); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 100% { transform: translateY(0) rotate(45deg); } 50% { transform: translateY(10px) rotate(45deg); } }

        /* 4. هيكل الأقسام */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding-bottom: 80px; background: #000; overflow: hidden; }
        .v-header { width: 100%; line-height: 0; }
        .v-header-sauvage { width: 85%; margin: 0 auto; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 40px 0; }
        .img-bottle { width: 35%; max-width: 140px; margin: 0 auto; display: block; filter: drop-shadow(0 10px 20px rgba(0,0,0,0.5)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; letter-spacing: 6px; margin: 15px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        .row { display: flex; align-items: center; width: 100%; padding: 60px 10%; gap: 60px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; }
        .img-box img { width: 100%; border-radius: 2px; display: block; }
        
        .txt-box { width: 50%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.3rem; margin-bottom: 25px; color: var(--color); letter-spacing: 2px; }
        .txt-box p { font-size: 0.9rem; line-height: 1.8; color: #ccc; font-weight: 300; margin-bottom: 15px; }
        .highlight { color: #fff; font-weight: 600; }
        
        /* 5. منطقة الشراء */
        .purchase-area { max-width: 1100px; margin: 50px auto; display: flex; gap: 50px; padding: 45px; border-top: 1px solid rgba(255,255,255,0.08) !important; width: 90%; background: rgba(255,255,255,0.02); }
        .mini-thumb { width: 100px; height: 100px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1) !important; }
        
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-box { flex: 1; padding: 18px; border: 1px solid rgba(255,255,255,0.1) !important; text-align: center; cursor: pointer; transition: 0.4s; }
        .size-box span { display: block; font-size: 0.6rem; color: #888; margin-top: 8px; letter-spacing: 1px; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05); }

        input { width: 100%; padding: 22px 0; margin-bottom: 18px; background: transparent !important; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.2) !important; font-family: 'Montserrat'; font-size: 0.85rem; border-radius: 0; }
        .order-btn { width: 100%; padding: 24px; background: #fff; color: #000; font-family: 'Montserrat'; font-weight: 800; font-size: 1.1rem; cursor: pointer; letter-spacing: 4px; margin-top: 15px; transition: 0.3s; }
        .order-btn:hover { background: var(--color); color: #fff; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 8%; gap: 40px; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 25px; gap: 30px; }
            .brand-logo { font-size: 1.6rem; }
            .v-header-sauvage { width: 95%; }
        }

        /* ألوان الهوية لكل عطر */
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
                <p>Sauvage Elixir réinterprète la signature iconique de Sauvage avec une concentration inouïe. Une fraîcheur poussée à l'extrême qui se mêle à un cœur d'épices sur mesure.</p>
                <p><span class="highlight">Pour :</span> Lui<br>
                <span class="highlight">Il est :</span> Puissant et Noble<br>
                <span class="highlight">Occasion :</span> Soirées d'Exception<br>
                <span class="highlight">Famille :</span> AROMATIQUE Épicée</p>
                <h3>Le flacon</h3>
                <p>Le flacon en verre laqué d'un bleu nuit profond est aussi précieux qu'une pièce de joاillerie.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0; font-size:1.2rem">SAUVAGE ELIXIR</h4><p style="color:#555; font-size:11px; letter-spacing:1px">EXTRAIT DE PARFUM</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button type="button" class="order-btn">COMMANDER | 319 DH</button></form>
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
                <p>Cette fragrance raconte l’histoire d’un homme fort, épris d’une passion vibrante. Un parfum boisé et ambré d'une sensualية irrésistible.</p>
                <p><span class="highlight">Pour :</span> Lui<br><span class="highlight">Il est :</span> Captivant et Audacieux</p>
                <h3>Le flacon</h3>
                <p>Un design aux lignes épurées et masculines, surmonté du bouchon iconique enlacé.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0; font-size:1.2rem">STRONGER WITH YOU</h4><p style="color:#555; font-size:11px; letter-spacing:1px">EAU DE PARFUM</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec2')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec2')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button type="button" class="order-btn">COMMANDER | 319 DH</button></form>
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
                <p>Libre Intense célèbre la liberté d’une femme audacieuse. Une dualité florale brûlante.</p>
                <p><span class="highlight">Pour :</span> Elle<br>
                <span class="highlight">Elle est :</span> Royale<br>
                <span class="highlight">Occasion :</span> Luxe & Soirée</p>
                <h3>Notes Olfactives</h3>
                <p><span class="highlight">Notes de Tête :</span> Mandarine & Bergamote<br>
                <span class="highlight">Notes de Cœur :</span> Lavande & Fleur d'Oranger<br>
                <span class="highlight">Notes de Fond :</span> Sillage puissant, reste actif jusqu'à 10h.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0; font-size:1.2rem">LIBRE INTENSE</h4><p style="color:#555; font-size:11px; letter-spacing:1px">EAU DE PARFUM</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec3')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec3')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button type="button" class="order-btn">COMMANDER | 319 DH</button></form>
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
                <p>La douceur et le pouvoir de séduction du jasmin renforcent encore l’éclat de Good Girl. Le côté mystérieux est révélé grâce au cacao riche en arômes et à l’enivrante fève tonka.</p>
                <p><span class="highlight">Pour :</span> Elle<br>
                <span class="highlight">Elle est :</span> Séductrice et Puissante<br>
                <span class="highlight">Occasion :</span> Le jour et la nuit<br>
                <span class="highlight">Famille olfactive :</span> AMBRÉE Ambrée Florale</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-ingredients.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Ingrédients Principaux :</span> Jasmin, Tubéreuse, Fève Tonka<br>
                <span class="highlight">Notes de Tête :</span> Amande<br>
                <span class="highlight">Notes de Cœur :</span> Jasmin d’Arabie & Tubéreuse<br>
                <span class="highlight">Notes de Fond :</span> Fève Tonka & Cacao</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:20px">
                    <div><h4 style="font-family:'Cinzel'; margin:0; font-size:1.2rem">GOOD GIRL</h4><p style="color:#555; font-size:11px; letter-spacing:1px">EAU DE PARFUM</p></div>
                    <img src="assets/gg-hand.jpg" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>± 80 RASHAT</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>± 160 RASHAT</span></div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button type="button" class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <script>
        // دالة تحديث الحجم والثمن
        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerText = `COMMANDER | ${price} DH`;
        }

        // دالة التمرير (Scrolling)
        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        let currentIdx = 0;
        document.getElementById('scrollBtn').onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView({ behavior: 'smooth' });
        };

        // تحديث لون السهم حسب القسم
        window.onscroll = () => {
            const scrollPos = window.scrollY + window.innerHeight / 2;
            sections.forEach((id, index) => {
                const el = document.getElementById(id);
                if (el && scrollPos >= el.offsetTop && scrollPos < el.offsetTop + el.offsetHeight) {
                    const color = getComputedStyle(el).getPropertyValue('--color');
                    document.documentElement.style.setProperty('--current-color', color);
                    currentIdx = index;
                }
            });
        };
    </script>
</body>
</html>
