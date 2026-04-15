<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* 1. ضبط التنقيزة ومنع الهروب الجانبي */
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
            display: flex;
            flex-direction: column;
            padding-bottom: 60px;
        }

        /* 2. هندسة الفيديو: عرض 100% وطول سينمائي */
        .v-header { width: 100%; height: 55vh; position: relative; overflow: hidden; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; padding: 40px 0; }
        .img-bottle { width: 42%; max-width: 180px; cursor: zoom-in; margin: 0 auto; display: block; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff; margin-top: 10px; letter-spacing: 5px; text-transform: uppercase; }
        .perfume-type { font-family: 'Montserrat', sans-serif; font-size: 0.7rem; color: var(--color); letter-spacing: 3px; font-weight: 400; margin-top: 5px; text-transform: uppercase; }

        /* 3. المعلومات كاملة مع الضباب الملون */
        .row { display: flex; align-items: center; width: 100%; padding: 40px 5%; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; z-index: 2; }
        .img-box img { width: 95%; max-width: 450px; border-radius: 2px; cursor: zoom-in; }
        
        .txt-box { width: 50%; padding: 0 4%; text-align: left; position: relative; color: #fff; z-index: 2; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 140%; height: 140%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.28; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.5rem; color: #fff; margin-bottom: 12px; text-transform: uppercase; border-bottom: 0.5px solid var(--color) !important; display: inline-block; }
        p { font-family: 'Montserrat', sans-serif; font-size: 0.9rem; line-height: 1.6; color: #eee; margin-bottom: 8px; }
        b { color: var(--color); font-weight: 600; }

        .tech-notes { font-size: 0.75rem; color: #999; margin-top: 15px; padding-top: 15px; border-top: 0.5px solid rgba(255,255,255,0.1) !important; }

        /* 4. منطقة الشراء - تصميم رقيق بدون خطوط عريضة */
        .purchase-area { max-width: 1000px; margin: 50px auto 0; display: flex; gap: 40px; padding: 20px; align-items: flex-start; justify-content: center; width: 100%; }
        .details-side { width: 45%; }
        .form-side { width: 50%; }
        
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; border-bottom: 0.5px solid rgba(255,255,255,0.1) !important; padding-bottom: 15px; }
        .mini-thumb { width: 65px; height: 65px; object-fit: cover; }
        
        .size-container { display: flex; gap: 12px; margin-top: 15px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 15px; border: 0.5px solid rgba(255,255,255,0.2) !important; border-radius: 2px; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.03); color: var(--color); }

        .form-side input { width: 100%; padding: 18px; margin-bottom: 12px; background: transparent; color: #fff; border-bottom: 0.5px solid rgba(255,255,255,0.15) !important; font-size: 0.9rem; }
        .buy-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 2px; text-transform: uppercase; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.98); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 30px 6%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; width: 90%; margin: 40px auto; }
            .details-side, .form-side { width: 100%; }
            .v-header { height: 45vh; } /* فيديو أقصر شوية في التلفون باش تبان الهضرة */
        }

        /* ألوان الهوية البصرية لكل عطر */
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
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A high-fashion composition infused with wild freshness. Raw elegance.</p><h3>The Bottle</h3><p>Dark lines reflecting the power of the desert at twilight.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Bergamot</p><p><b>Heart:</b> Sichuan Pepper</p><p><b>Base:</b> Ambroxan</p><div class="tech-notes"><p>* Top Notes: First 15 min.</p><p>* Heart Notes: Up to 1 hour.</p><p>* Base Notes: Longest lasting trail.</p></div></div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE ELIXIR</h2><p style="font-size:10px; color:#555;">PREMIUM QUALITY</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's1')"><div class="size-box"><span>5ML</span></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's1')"><div class="size-box"><span>10ML</span></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s1" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
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
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Magnetic energy. Bold, unpredictable, and original.</p><h3>The Concept</h3><p>The power of togetherness. A sensual fragrance.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Cardamom</p><p><b>Heart:</b> Lavender</p><p><b>Base:</b> Vanilla & Chestnut</p><div class="tech-notes"><p>* Masculine trail lasting 8+ hours.</p></div></div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SWY ABSOLUTELY</h2><p style="font-size:10px; color:#555;">INTENSE MALE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's2')"><div class="size-box"><span>5ML</span></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's2')"><div class="size-box"><span>10ML</span></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s2" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
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
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The scent of freedom. Mixing orange blossom and lavender.</p><h3>The Style</h3><p>For the bold woman who lives by her own rules.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Mandarin</p><p><b>Heart:</b> Orange Blossom</p><p><b>Base:</b> Vanilla & Musk</p><div class="tech-notes"><p>* Sophisticated trail up to 7 hours.</p></div></div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#555;">CHIC FEMALE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's3')"><div class="size-box"><span>5ML</span></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's3')"><div class="size-box"><span>10ML</span></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s3" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
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
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Mysterious and sensual. Jasmine and rich cocoa.</p><h3>The Power</h3><p>Empowerment in a bottle. Good and bad.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this.src)"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Almond & Coffee</p><p><b>Heart:</b> Jasmine Sambac</p><p><b>Base:</b> Tonka Bean & Cocoa</p><div class="tech-notes"><p>* Long-lasting trail of 8+ hours.</p></div></div>
        </div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#555;">SEDUCTIVE FEMALE</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's4')"><div class="size-box"><span>5ML</span></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's4')"><div class="size-box"><span>10ML</span></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="s4" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
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
