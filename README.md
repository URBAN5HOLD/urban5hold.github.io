<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Official Collection</title>
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

        /* Smart Arrow: 75% down, no circle */
        .scroll-trigger { 
            position: fixed; top: 75%; right: 25px; 
            transform: translateY(-50%);
            width: 40px; height: 40px; z-index: 2000; cursor: pointer;
            display: flex; align-items: center; justify-content: center;
        }
        .arrow-icon { 
            width: 20px; height: 20px; 
            border-right: 3px solid var(--current-arrow-color, #fff) !important; 
            border-bottom: 3px solid var(--current-arrow-color, #fff) !important; 
            transform: rotate(45deg); animation: bounce 2s infinite;
            transition: 0.5s ease;
        }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        
        .glow-center { 
            position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); 
            width: 600px; height: 600px; 
            background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 75%) !important; 
            opacity: 0.3; z-index: 0; pointer-events: none;
        }

        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 40px 0; position: relative; z-index: 2; }
        .img-bottle { width: 32%; max-width: 130px; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff !important; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        /* Free Glow Effect */
        .text-glow-free {
            position: relative; z-index: 2; padding: 25px;
            background: radial-gradient(ellipse at center, var(--glow-color) 0%, rgba(0,0,0,0) 85%) !important;
        }

        .row { display: flex; align-items: center; width: 100%; padding: 50px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 4px; display: block; }
        
        .txt-box { width: 55%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.5rem; margin-bottom: 20px; color: var(--color) !important; letter-spacing: 2px; }
        .txt-box p { font-size: 0.95rem; line-height: 1.9; color: #f0f0f0 !important; font-weight: 300; margin-bottom: 12px; }
        .highlight { color: var(--color) !important; font-weight: 600; font-size: 0.85rem; margin-right: 5px; }
        
        .purchase-area { 
            max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 40px; 
            border-top: 1px solid rgba(255,255,255,0.1) !important; 
            border-bottom: 1px solid rgba(255,255,255,0.1) !important;
            width: 90%; position: relative; z-index: 2;
        }
        .mini-thumb { width: 100px; height: 100px; object-fit: cover; }
        .size-container { display: flex; gap: 15px; margin-top: 15px; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2) !important; text-align: center; cursor: pointer; color: #fff; }
        .size-box span { display: block; font-size: 9px; color: #888; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05) !important; }

        input { width: 100%; padding: 18px 0; margin-bottom: 15px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.3) !important; font-family: 'Montserrat'; }
        .order-btn { width: 100%; padding: 22px; background-color: #fff !important; color: #000 !important; font-weight: 800; cursor: pointer; letter-spacing: 4px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 25px; }
        }

        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.35); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.35); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.35); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.35); }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/image_25f332.png"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>THE FRAGRANCE</h3>
                <p>An extraordinary concentration. A wild freshness that intoxicates a custom-made heart of spices.</p>
                <p><span class="highlight">Gender:</span> Men<br><span class="highlight">Vibe:</span> Powerful and Noble</p>
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
            <div class="img-box"><img src="assets/stronger-left.png"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>THE FRAGRANCE</h3>
                <p>A woody and amber fragrance with magnetic sensuality. Captivating and bold.</p>
                <p><span class="highlight">Top:</span> Pink Pepper<br><span class="highlight">Base:</span> Smoky Vanilla</p>
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
            <div class="img-box"><img src="assets/image_26d833.png"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>THE FRAGRANCE</h3>
                <p>A burning floral duality. Freedom pushed to its extreme.</p>
                <p><span class="highlight">Notes:</span> French Lavender & Moroccan Orange Blossom</p>
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
            <div class="img-box"><img src="assets/image_2651c6.png"></div> <div class="txt-box"><div class="text-glow-free">
                <h3>THE FRAGRANCE</h3>
                <p>The sweetness of jasmine and the intoxicating tonka bean reveal the mysterious side of Good Girl.</p>
                <p><span class="highlight">Family:</span> Amber Floral<br><span class="highlight">Vibe:</span> Seductive & Powerful</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/image_26688e.png"></div> <div class="txt-box"><div class="text-glow-free">
                <h3>OLFACTORY NOTES</h3>
                <p><span class="highlight">Top:</span> Almond<br><span class="highlight">Heart:</span> Tuberose & Jasmine<br><span class="highlight">Base:</span> Tonka Bean & Cocoa</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">GOOD GIRL</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/gg-thumb.png" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input placeholder="FULL NAME"><input placeholder="PHONE NUMBER"><input placeholder="CITY"><button type="button" class="order-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </section>

    <script>
        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerText = `ORDER NOW | ${price} DH`;
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
