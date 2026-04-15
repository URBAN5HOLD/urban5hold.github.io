<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Privée</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --bg: #000; --gold: #D4AF37; }
        html, body { width: 100%; margin: 0; padding: 0; overflow-x: hidden; background-color: var(--bg); scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { box-sizing: border-box; outline: none; -webkit-tap-highlight-color: transparent; }

        /* اللوغو ثابت في الفوق */
        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 10px; color: #fff; text-shadow: 0 0 15px rgba(0,0,0,0.8); }

        /* سهم التنقل بين العطور */
        .scroll-trigger { position: fixed; bottom: 5%; right: 30px; width: 50px; height: 50px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; background: rgba(255,255,255,0.05); border-radius: 50%; backdrop-filter: blur(5px); }
        .arrow-icon { width: 12px; height: 12px; border-right: 2px solid #fff; border-bottom: 2px solid #fff; transform: rotate(45deg); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }

        /* التصميم العام للأقسام */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding: 120px 0 80px 0; border-bottom: 1px solid rgba(255,255,255,0.05); }
        
        /* القسم الأساسي: صورة كبيرة + معلومات */
        .main-display { display: flex; align-items: center; justify-content: center; width: 90%; margin: 0 auto; gap: 60px; }
        .perfume-img-main { width: 45%; max-width: 480px; transition: transform 0.8s ease; filter: drop-shadow(0 20px 50px rgba(0,0,0,0.5)); }
        
        /* لوحة المعلومات - ستايل الصور المرسلة */
        .info-panel { width: 45%; color: #fff; }
        .info-panel h2 { font-family: 'Cinzel', serif; font-size: 1.4rem; color: var(--gold); letter-spacing: 3px; margin-bottom: 25px; text-transform: uppercase; border: none; background: transparent; }
        .info-panel p { font-family: 'Montserrat', sans-serif; font-size: 0.95rem; line-height: 1.9; color: #ddd; margin-bottom: 20px; font-weight: 300; }
        
        .detail-row { margin-bottom: 12px; font-size: 0.9rem; font-family: 'Montserrat'; display: flex; gap: 10px; }
        .detail-label { font-weight: 700; color: #fff; min-width: 100px; }
        .detail-value { color: #aaa; }

        /* قسم المكونات */
        .ingredients-container { display: flex; width: 90%; margin: 80px auto; gap: 50px; align-items: flex-start; }
        .ing-text-side { flex: 1; color: #fff; }
        .ing-img-side { flex: 1; max-width: 600px; border-radius: 2px; opacity: 0.9; }

        /* منطقة الاختيار و الشراء */
        .purchase-zone { max-width: 1100px; margin: 60px auto; width: 90%; display: flex; gap: 50px; padding: 50px; border-top: 1px solid rgba(255,255,255,0.1); background: rgba(255,255,255,0.02); }
        
        .size-selector { flex: 1; }
        .size-options { display: flex; gap: 15px; margin-top: 15px; }
        .option-card { flex: 1; padding: 25px; border: 1px solid rgba(255,255,255,0.1); text-align: center; cursor: pointer; transition: 0.4s; color: #fff; }
        /* كلمة Sprays بدون رموز */
        .option-card span { display: block; font-size: 0.7rem; color: #666; margin-top: 10px; letter-spacing: 2px; }
        .option-card.active { border-color: var(--gold); background: rgba(212, 175, 55, 0.08); }
        .option-card.active span { color: var(--gold); }

        /* فورم الطلب */
        .form-side { flex: 1.3; }
        .form-side input { 
            width: 100%; padding: 22px 0; margin-bottom: 20px; 
            background: transparent !important; color: #fff; 
            border: none !important; border-bottom: 1px solid rgba(255,255,255,0.15) !important; 
            font-family: 'Montserrat'; font-size: 0.9rem; letter-spacing: 1.5px;
        }
        .form-side input:focus { border-bottom-color: var(--gold) !important; }
        
        .btn-order { 
            width: 100%; padding: 25px; background: #fff; color: #000; 
            font-family: 'Montserrat'; font-weight: 800; font-size: 1.1rem; 
            cursor: pointer; letter-spacing: 4px; border: none; margin-top: 20px; 
            transition: 0.4s; text-transform: uppercase;
        }
        .btn-order:hover { background: var(--gold); color: #fff; transform: translateY(-3px); }

        /* نوتات الشرح في الأسفل */
        .explanation-notes { width: 90%; margin: 20px auto; color: #555; font-size: 0.75rem; line-height: 1.6; font-family: 'Montserrat'; }

        /* Responsive */
        @media (max-width: 900px) {
            .main-display, .ingredients-container, .purchase-zone { flex-direction: column; text-align: center; }
            .perfume-img-main, .info-panel, .ing-img-side { width: 100%; max-width: 100%; }
            .detail-row { justify-content: center; }
            .purchase-zone { padding: 30px 15px; }
        }

        /* متغيرات الألوان لكل قسم */
        .sec-sauvage { --gold: #4A90E2; }
        .sec-stronger { --gold: #CD7F32; }
        .sec-libre { --gold: #D4AF37; }
        .sec-goodgirl { --gold: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA BEAUTY</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sec-sauvage" id="sec1">
        <div class="main-display">
            <img src="assets/sauvage-main.png" class="perfume-img-main">
            <div class="info-panel">
                <h2>La Fragrance</h2>
                <p>Sauvage Elixir est un parfum d'une concentration hors du commun, une fragrance où la fraîcheur emblématique de Sauvage s'enivre d'un cœur d'épices.</p>
                <div class="detail-row"><span class="detail-label">Pour :</span> <span class="detail-value">Lui</span></div>
                <div class="detail-row"><span class="detail-label">Il est :</span> <span class="detail-value">Puissant et Noble</span></div>
                <div class="detail-row"><span class="detail-label">Occasion :</span> <span class="detail-value">Soirées d'Exception</span></div>
            </div>
        </div>
        <div class="ingredients-container">
            <div class="ing-text-side">
                <h2>Ingrédients & Notes</h2>
                <div class="detail-row"><span class="detail-label">Notes de Tête :</span> <span class="detail-value">Pamplemousse & Cannelle</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Cœur :</span> <span class="detail-value">Lavande de Nyons</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Fond :</span> <span class="detail-value">Bois de Santal & Réglisse</span></div>
            </div>
            <img src="assets/sauvage-ing.jpg" class="ing-img-side">
        </div>
        <div class="purchase-zone">
            <div class="size-selector">
                <div class="size-options">
                    <div class="option-card" onclick="updateOrder(this, 199, 'sec1')">5ML<span>80 SPRAYS</span></div>
                    <div class="option-card active" onclick="updateOrder(this, 319, 'sec1')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-side">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button class="btn-order">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section sec-stronger" id="sec2">
        <div class="main-display">
            <img src="assets/stronger-main.png" class="perfume-img-main">
            <div class="info-panel">
                <h2>La Fragrance</h2>
                <p>Ce parfum raconte l'histoire d'un amour intense. Une fragrance vibrante et audacieuse, pour un homme qui ne recule devant rien.</p>
                <div class="detail-row"><span class="detail-label">Pour :</span> <span class="detail-value">Lui</span></div>
                <div class="detail-row"><span class="detail-label">Il est :</span> <span class="detail-value">Addictif et Chaleureux</span></div>
                <div class="detail-row"><span class="detail-label">Occasion :</span> <span class="detail-value">Hiver & Rendez-vous</span></div>
            </div>
        </div>
        <div class="ingredients-container">
            <div class="ing-text-side">
                <h2>Ingrédients & Notes</h2>
                <div class="detail-row"><span class="detail-label">Notes de Tête :</span> <span class="detail-value">Poivre Rose & Baies</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Cœur :</span> <span class="detail-value">Cannelle & Sauge</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Fond :</span> <span class="detail-value">Vanille & Ambre</span></div>
            </div>
            <img src="assets/stronger-ing.jpg" class="ing-img-side">
        </div>
        <div class="purchase-zone">
            <div class="size-selector">
                <div class="size-options">
                    <div class="option-card" onclick="updateOrder(this, 199, 'sec2')">5ML<span>80 SPRAYS</span></div>
                    <div class="option-card active" onclick="updateOrder(this, 319, 'sec2')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-side">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button class="btn-order">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section sec-libre" id="sec3">
        <div class="main-display">
            <img src="assets/libre-main.png" class="perfume-img-main">
            <div class="info-panel">
                <h2>La Fragrance</h2>
                <p>Libre Intense célèbre la liberté d’une femme audacieuse. Une dualité florale brûlante entre la lavande de France et la fleur d'oranger du Maroc.</p>
                <div class="detail-row"><span class="detail-label">Pour :</span> <span class="detail-value">Elle</span></div>
                <div class="detail-row"><span class="detail-label">Elle est :</span> <span class="detail-value">Audacieuse et Royale</span></div>
                <div class="detail-row"><span class="detail-label">Occasion :</span> <span class="detail-value">Luxe & Soirée</span></div>
            </div>
        </div>
        <div class="ingredients-container">
            <div class="ing-text-side">
                <h2>Ingrédients & Notes</h2>
                <div class="detail-row"><span class="detail-label">Notes de Tête :</span> <span class="detail-value">Mandarine & Bergamote</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Cœur :</span> <span class="detail-value">Lavande & Fleur d'Oranger</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Fond :</span> <span class="detail-value">Sillage puissant, reste actif jusqu'à 10h.</span></div>
            </div>
            <img src="assets/libre-ing.jpg" class="ing-img-side">
        </div>
        <div class="purchase-zone">
            <div class="size-selector">
                <div class="size-options">
                    <div class="option-card" onclick="updateOrder(this, 199, 'sec3')">5ML<span>80 SPRAYS</span></div>
                    <div class="option-card active" onclick="updateOrder(this, 319, 'sec3')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-side">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button class="btn-order">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section sec-goodgirl" id="sec4">
        <div class="main-display">
            <img src="assets/gg-main.png" class="perfume-img-main">
            <div class="info-panel">
                <h2>La Fragrance</h2>
                <p>La douceur و le pouvoir de séduction du jasmin renforcent l’éclat de Good Girl. Le côté mystérieux est révélé grâce au cacao riche.</p>
                <div class="detail-row"><span class="detail-label">Pour :</span> <span class="detail-value">Elle</span></div>
                <div class="detail-row"><span class="detail-label">Elle est :</span> <span class="detail-value">Séductrice et Puissante</span></div>
                <div class="detail-row"><span class="detail-label">Occasion :</span> <span class="detail-value">Le jour et la nuit</span></div>
            </div>
        </div>
        <div class="ingredients-container">
            <div class="ing-text-side">
                <h2>Ingrédients & Notes</h2>
                <div class="detail-row"><span class="detail-label">Famille Olfactive :</span> <span class="detail-value">AMBRÉE Ambrée Florale</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Tête :</span> <span class="detail-value">Amande</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Cœur :</span> <span class="detail-value">Jasmin & Tubéreuse</span></div>
                <div class="detail-row"><span class="detail-label">Notes de Fond :</span> <span class="detail-value">Fève Tonka & Cacao</span></div>
            </div>
            <img src="assets/gg-ing.jpg" class="ing-img-side">
        </div>
        <div class="purchase-zone">
            <div class="size-selector">
                <div class="size-options">
                    <div class="option-card" onclick="updateOrder(this, 199, 'sec4')">5ML<span>80 SPRAYS</span></div>
                    <div class="option-card active" onclick="updateOrder(this, 319, 'sec4')">10ML<span>160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-side">
                <form><input type="text" placeholder="NOM COMPLET" required><input type="tel" placeholder="TÉLÉPHONE" required><input type="text" placeholder="VILLE" required><button class="btn-order">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <div class="explanation-notes">
        * Notes de tête : Première impression d'un parfum, dure entre 5 et 15 minutes.<br>
        * Notes de cœur : Commencent à ressortir lorsque les notes de tête s’estompent.<br>
        * Notes de fond : La senteur sous-jacente durant le port du parfum. Note qui reste le plus longtemps.
    </div>

    <script>
        function updateOrder(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.option-card').forEach(b => b.classList.remove('active'));
            element.classList.add('active');
            section.querySelector('.btn-order').innerText = `COMMANDER | ${price} DH`;
        }

        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        let currentIdx = 0;
        document.getElementById('scrollBtn').onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView({ behavior: 'smooth' });
        };

        window.onscroll = () => {
            const scrollPos = window.scrollY + window.innerHeight / 2;
            sections.forEach((id, index) => {
                const el = document.getElementById(id);
                if (el && scrollPos >= el.offsetTop && scrollPos < el.offsetTop + el.offsetHeight) {
                    currentIdx = index;
                }
            });
        };
    </script>
</body>
</html>
