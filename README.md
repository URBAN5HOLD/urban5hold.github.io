<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Exclusive Decants</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* التنقيزة ومنع التحرك الجانبي نهائياً */
        html, body { 
            width: 100%; 
            margin: 0; padding: 0;
            overflow-x: hidden; 
            background-color: #000; 
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; border: none !important; outline: none !important; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 6px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { 
            width: 100%; 
            min-height: 100vh; 
            scroll-snap-align: start; 
            position: relative; 
            background: #000;
            overflow: hidden;
            padding-bottom: 120px;
        }

        /* الفيديو الأصلي عريض 100% */
        .v-header { width: 100%; position: relative; overflow: hidden; }
        .bg-v { width: 100%; height: auto; display: block; }
        
        .bottle-center { text-align: center; padding: 60px 0; }
        .img-bottle { width: 42%; max-width: 190px; cursor: zoom-in; margin: 0 auto; display: block; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; margin-top: 15px; letter-spacing: 6px; text-transform: uppercase; line-height: 1.2; }
        .perfume-type { font-family: 'Montserrat', sans-serif; font-size: 0.75rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; font-weight: 400; margin-top: 5px; opacity: 0.9; }

        /* صفوف المعلومات مع الضباب الملون */
        .row { display: flex; align-items: center; width: 100%; padding: 60px 5%; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; z-index: 2; }
        .img-box img { width: 90%; max-width: 480px; border-radius: 2px; cursor: zoom-in; }
        
        .txt-box { width: 50%; padding: 0 5%; text-align: left; position: relative; color: #fff; z-index: 2; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 150%; height: 150%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.25; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.7rem; color: #fff; margin-bottom: 20px; text-transform: uppercase; display: inline-block; }
        p { font-family: 'Montserrat', sans-serif; font-size: 0.95rem; line-height: 1.7; color: #eee; margin-bottom: 12px; }
        b { color: var(--color); font-weight: 600; }

        .tech-notes { font-size: 0.75rem; color: #888; margin-top: 25px; padding-top: 20px; border-top: 0.5px solid rgba(255,255,255,0.15) !important; line-height: 1.6; }

        /* منطقة الشراء - بدون خطوط عريضة */
        .purchase-area { max-width: 1000px; margin: 80px auto 0; display: flex; gap: 50px; padding: 20px; align-items: flex-start; }
        .details-side { width: 45%; }
        .form-side { width: 55%; }
        
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 30px; border-bottom: 0.5px solid rgba(255,255,255,0.1) !important; padding-bottom: 15px; }
        .mini-thumb { width: 65px; height: 65px; object-fit: cover; border: 0.5px solid rgba(255,255,255,0.1) !important; }
        
        .size-container { display: flex; gap: 15px; margin-top: 25px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 18px; border: 0.5px solid rgba(255,255,255,0.2) !important; border-radius: 1px; transition: 0.4s; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.03); color: var(--color); }

        .form-side input { width: 100%; padding: 20px; margin-bottom: 15px; background: transparent; color: #fff; border-bottom: 0.5px solid rgba(255,255,255,0.15) !important; font-family: 'Montserrat', sans-serif; font-size: 0.9rem; }
        .buy-btn { width: 100%; padding: 25px; background: #fff; color: #000; font-weight: 800; font-size: 1.1rem; cursor: pointer; letter-spacing: 3px; text-transform: uppercase; transition: 0.4s; }
        .buy-btn:hover { background: var(--color); color: #fff; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.98); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 50px 7%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; width: 100%; padding: 20px; }
            .details-side, .form-side { width: 100%; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay" onclick="this.style.display='none'"><img src="" id="zoomedImg" style="max-width:92%"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">SAUVAGE</h1>
            <div class="perfume-type">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>A high-fashion composition infused with wild freshness. Raw elegance at its peak.</p>
                <h3>The Bottle</h3>
                <p>Luxurious dark lines reflecting the power of the desert at twilight. A legendary design.</p>
            </div>
        </div>
        
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Top:</b> Reggio di Calabria Bergamot</p>
                <p><b>Heart:</b> Sichuan Pepper & Lavender</p>
                <p><b>Base:</b> Rare Ambroxan & Vanilla Absolute</p>
                <div class="tech-notes">
                    <p>* Top Notes: First impression, lasts 15 min.</p>
                    <p>* Heart Notes: The soul of perfume, lasts 1 hour.</p>
                    <p>* Base Notes: The deep trail, lasts up to 8 hours.</p>
                </div>
            </div>
        </div>

        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE ELIXIR</h2><p style="font-size:10px; color:#555;">VELOORIA EXCLUSIVE</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's1')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's1')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s1" value="10ml"><input type="text" placeholder="YOUR FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><input type="text" placeholder="CITY"><button class="buy-btn">GET IT NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-type">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>A magnetic energy. Bold, unpredictable, and surprisingly original.</p>
                <h3>The Concept</h3>
                <p>The power of togetherness. A sensual fragrance that lingers in the memory.</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Top:</b> Cardamom & Pink Pepper</p>
                <p><b>Heart:</b> Lavender & Sage</p>
                <p><b>Base:</b> Smoky Vanilla & Chestnut</p>
                <div class="tech-notes"><p>* Long-lasting masculine trail for more than 8 hours.</p></div>
            </div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SWY ABSOLUTELY</h2><p style="font-size:10px; color:#555;">INTENSE COLLECTION</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's2')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's2')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s2" value="10ml"><input type="text" placeholder="YOUR FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><input type="text" placeholder="CITY"><button class="buy-btn">GET IT NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-type">EAU DE PARFUM / FEMME</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>The scent of freedom. A floral masterpiece mixing orange blossom and lavender.</p>
                <h3>The Style</h3>
                <p>Designed for the bold and modern woman who lives by her own rules.</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Top:</b> Mandarin & French Lavender</p>
                <p><b>Heart:</b> Moroccan Orange Blossom</p>
                <p><b>Base:</b> Madagascar Vanilla & Musk</p>
                <div class="tech-notes"><p>* A sophisticated trail that lasts up to 7 hours.</p></div>
            </div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#555;">FEMALE ELEGANCE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's3')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's3')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s3" value="10ml"><input type="text" placeholder="YOUR FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><input type="text" placeholder="CITY"><button class="buy-btn">GET IT NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-type">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>Mysterious and sensual. A duality of jasmine and rich, dark cocoa.</p>
                <h3>The Power</h3>
                <p>Empowerment in a bottle. For the woman who knows when to be good and when to be bad.</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Top:</b> Fresh Almond & Coffee</p>
                <p><b>Heart:</b> Sambac Jasmine & Tuberose</p>
                <p><b>Base:</b> Roasted Tonka Bean & Cocoa</p>
                <div class="tech-notes"><p>* Heavy-hitting longevity of 8+ hours on skin.</p></div>
            </div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#555;">SEDUCTIVE COLLECTION</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's4')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's4')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s4" value="10ml"><input type="text" placeholder="YOUR FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><input type="text" placeholder="CITY"><button class="buy-btn">GET IT NOW | 319 DH</button></form></div>
        </div>
    </div>

    <script>
        function zoom(src) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = src;
            overlay.style.display = 'flex';
        }
        function selectSize(element, size, inputId) {
            element.parentElement.querySelectorAll('.size-item').forEach(i => i.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
