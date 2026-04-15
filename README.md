<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Decants</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:wght@700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; padding-bottom: 80px; }
        .v-header { width: 100%; height: 50vw; max-height: 65vh; overflow: hidden; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }

        /* المستطيل التفاعلي */
        .decant-card { 
            max-width: 950px; margin: -50px auto 40px; 
            background: #0a0a0a; 
            border: 1px solid rgba(255,255,255,0.1) !important;
            display: flex; border-radius: 12px; overflow: hidden;
            position: relative; z-index: 10; box-shadow: 0 20px 40px rgba(0,0,0,0.5);
        }

        /* جهة اليمين: صورة اليد والمعلومات */
        .side-info { 
            width: 45%; background: rgba(255,255,255,0.02); 
            padding: 30px; text-align: center; border-right: 1px solid rgba(255,255,255,0.1) !important;
        }
        .side-info img { width: 100%; border-radius: 8px; margin-bottom: 15px; transition: 0.3s; cursor: zoom-in; }
        .side-info h4 { font-family: 'Cinzel', serif; color: var(--color); font-size: 1.2rem; margin-bottom: 10px; letter-spacing: 2px; }
        .side-info p { font-size: 0.85rem; color: #bbb; line-height: 1.5; }

        /* جهة اليسار: الفورم والاختيارات */
        .side-form { width: 55%; padding: 40px; }
        
        .size-grid { display: flex; gap: 15px; margin-bottom: 30px; }
        .size-box { 
            flex: 1; padding: 20px; border: 1px solid rgba(255,255,255,0.1) !important; 
            text-align: center; cursor: pointer; border-radius: 6px; transition: 0.4s;
        }
        .size-box.active { border-color: var(--color) !important; background: rgba(255,255,255,0.05); box-shadow: 0 0 15px var(--glow); }
        .size-box span { display: block; font-weight: 700; font-size: 1.4rem; color: #fff; }
        .size-box small { font-size: 0.75rem; color: var(--color); font-weight: 600; }

        .in-f { width: 100%; padding: 18px; margin-bottom: 15px; background: rgba(255,255,255,0.08); color: #fff; border-radius: 4px; text-align: center; font-size: 1rem; }
        .btn-f { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; cursor: pointer; border-radius: 4px; font-size: 1.1rem; transition: 0.3s; }
        .btn-f:hover { background: var(--color); color: #fff; }

        @media (max-width: 900px) {
            .decant-card { flex-direction: column; margin: -30px 15px 40px; }
            .side-info, .side-form { width: 100%; border-right: none !important; }
            .v-header { height: 70vw; }
        }

        /* Themes الألوان */
        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="decant-card">
            <div class="side-info">
                <img src="assets/sauvage-hand.jpg" alt="Sauvage Decant">
                <h4>SAUVAGE ELIXIR</h4>
                <p>Format voyage premium. 100% jus authentique extrait du flacon original.</p>
            </div>
            <div class="side-form">
                <div class="size-grid">
                    <div class="size-box" onclick="selectSize(this, '5ml', 'sauvage-size')"><span>5ML</span><small>~ 75 RASHAT</small></div>
                    <div class="size-box active" onclick="selectSize(this, '10ml', 'sauvage-size')"><span>10ML</span><small>~ 150 RASHAT</small></div>
                </div>
                <form>
                    <input type="hidden" id="sauvage-size" value="10ml">
                    <input type="text" placeholder="Nom Complet" class="in-f" required>
                    <input type="tel" placeholder="Numéro de Téléphone" class="in-f" required>
                    <input type="text" placeholder="Ville" class="in-f" required>
                    <button type="submit" class="btn-f">COMMANDER | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="decant-card">
            <div class="side-info">
                <img src="assets/stronger-hand.jpg" alt="Stronger Decant">
                <h4>STRONGER WITH YOU</h4>
                <p>L'intensité magnétique dans un format pratique et élégant.</p>
            </div>
            <div class="side-form">
                <div class="size-grid">
                    <div class="size-box" onclick="selectSize(this, '5ml', 'stronger-size')"><span>5ML</span><small>~ 75 RASHAT</small></div>
                    <div class="size-box active" onclick="selectSize(this, '10ml', 'stronger-size')"><span>10ML</span><small>~ 150 RASHAT</small></div>
                </div>
                <form>
                    <input type="hidden" id="stronger-size" value="10ml">
                    <input type="text" placeholder="Nom Complet" class="in-f" required>
                    <input type="tel" placeholder="Numéro" class="in-f" required>
                    <input type="text" placeholder="Ville" class="in-f" required>
                    <button type="submit" class="btn-f">COMMANDER | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="decant-card">
            <div class="side-info">
                <img src="assets/libre-hand.jpg" alt="Libre Decant">
                <h4>YSL LIBRE EDP</h4>
                <p>Le luxe de la liberté, maintenant accessible partout avec vous.</p>
            </div>
            <div class="side-form">
                <div class="size-grid">
                    <div class="size-box" onclick="selectSize(this, '5ml', 'libre-size')"><span>5ML</span><small>~ 75 RASHAT</small></div>
                    <div class="size-box active" onclick="selectSize(this, '10ml', 'libre-size')"><span>10ML</span><small>~ 150 RASHAT</small></div>
                </div>
                <form>
                    <input type="hidden" id="libre-size" value="10ml">
                    <input type="text" placeholder="Nom Complet" class="in-f" required>
                    <input type="tel" placeholder="Numéro" class="in-f" required>
                    <input type="text" placeholder="Ville" class="in-f" required>
                    <button type="submit" class="btn-f">COMMANDER | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="decant-card">
            <div class="side-info">
                <img src="assets/goodgirl-hand.jpg" alt="Good Girl Decant">
                <h4>CH GOOD GIRL</h4>
                <p>L'élégance du talon emblématique en format decant collector.</p>
            </div>
            <div class="side-form">
                <div class="size-grid">
                    <div class="size-box" onclick="selectSize(this, '5ml', 'gg-size')"><span>5ML</span><small>~ 75 RASHAT</small></div>
                    <div class="size-box active" onclick="selectSize(this, '10ml', 'gg-size')"><span>10ML</span><small>~ 150 RASHAT</small></div>
                </div>
                <form>
                    <input type="hidden" id="gg-size" value="10ml">
                    <input type="text" placeholder="Nom Complet" class="in-f" required>
                    <input type="tel" placeholder="Numéro" class="in-f" required>
                    <input type="text" placeholder="Ville" class="in-f" required>
                    <button type="submit" class="btn-f">COMMANDER | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <script>
        function selectSize(element, size, inputId) {
            // كيحيد active من المربعات ديال نفس القسم فقط
            element.parentElement.querySelectorAll('.size-box').forEach(opt => opt.classList.remove('active'));
            // كيزيد active للمربع اللي تبرك عليه
            element.classList.add('active');
            // كيدخل القيمة فـ input المخفي الخاص بداك العطر
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
