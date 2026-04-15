<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        html, body { 
            width: 100%; margin: 0; padding: 0;
            overflow-x: hidden; 
            background-color: #000; 
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; border: none !important; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 6px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { 
            width: 100%; min-height: 100vh; 
            scroll-snap-align: start; 
            scroll-snap-stop: always;
            position: relative; background: #000;
            display: flex; flex-direction: column;
            padding-bottom: 80px;
        }

        .v-header { width: 100%; overflow: hidden; background: #000; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }
        
        .bottle-center { text-align: center; padding: 50px 0; }
        .img-bottle { width: 45%; max-width: 180px; cursor: zoom-in; margin: 0 auto; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; margin-top: 10px; letter-spacing: 6px; }
        .perfume-sub { font-family: 'Montserrat', sans-serif; font-size: 0.75rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; margin-top: 5px; }

        .row { display: flex; align-items: center; width: 100%; padding: 60px 5%; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; z-index: 2; }
        .img-box img { width: 95%; max-width: 480px; border-radius: 2px; cursor: zoom-in; }
        
        .txt-box { width: 50%; padding: 0 5%; text-align: left; position: relative; color: #fff; z-index: 2; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 150%; height: 150%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.3; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.7rem; color: #fff; margin-bottom: 15px; text-transform: uppercase; border-bottom: 0.5px solid var(--color) !important; display: inline-block; padding-bottom: 5px; }
        p { font-family: 'Montserrat', sans-serif; font-size: 0.95rem; line-height: 1.7; color: #eee; margin-bottom: 12px; }
        b { color: var(--color); }

        /* منطقة الشراء المعدلة */
        .purchase-area { max-width: 1000px; margin: 60px auto 0; display: flex; gap: 50px; padding: 20px; align-items: flex-start; }
        .details-side { width: 45%; }
        .form-side { width: 55%; }
        
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; border-bottom: 0.5px solid rgba(255,255,255,0.1) !important; padding-bottom: 15px; }
        
        /* الصورة الصغيرة زدت فيها 5% وحيدت الـ Cursor */
        .mini-thumb { width: 72px; height: 72px; object-fit: cover; border: 0.5px solid rgba(255,255,255,0.15) !important; pointer-events: none; }
        
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-box { flex: 1; padding: 18px; border: 0.5px solid rgba(255,255,255,0.2) !important; text-align: center; cursor: pointer; color: #fff; }
        .active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); }

        .form-side input { width: 100%; padding: 20px; margin-bottom: 15px; background: transparent; color: #fff; border-bottom: 0.5px solid rgba(255,255,255,0.15) !important; font-size: 0.9rem; }
        .buy-btn { width: 100%; padding: 25px; background: #fff; color: #000; font-weight: 800; font-size: 1.1rem; cursor: pointer; letter-spacing: 3px; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.98); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 8%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; width: 100%; }
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
            <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A high-fashion composition infused with wild freshness.</p><h3>The Bottle</h3><p>Luxurious dark lines reflecting the desert power.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Bergamot | <b>Heart:</b> Lavender | <b>Base:</b> Ambroxan</p></div></div>

        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE ELIXIR</h2><p style="font-size:10px; color:#555;">PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div>
                <div class="size-container"><div class="size-box">5ML</div><div class="size-box" style="border-color: #4A90E2 !important; color: #4A90E2;">10ML</div></div>
            </div>
            <div class="form-side"><form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        <div class="row"><div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Magnetic energy. Bold and original.</p><h3>The Concept</h3><p>Sensual fragrance that lingers.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Cardamom | <b>Heart:</b> Sage | <b>Base:</b> Chestnut</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SWY ABSOLUTELY</h2><p style="font-size:10px; color:#555;">INTENSE MALE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div>
                <div class="size-container"><div class="size-box">5ML</div><div class="size-box" style="border-color: #CD7F32 !important; color: #CD7F32;">10ML</div></div>
            </div>
            <div class="form-side"><form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-sub">EAU DE PARFUM / FEMME</div>
        </div>
        <div class="row"><div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The scent of freedom. Orange blossom and lavender.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Mandarin | <b>Base:</b> Vanilla</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#555;">FEMALE ELEGANCE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div>
                <div class="size-container"><div class="size-box">5ML</div><div class="size-box" style="border-color: #D4AF37 !important; color: #D4AF37;">10ML</div></div>
            </div>
            <div class="form-side"><form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this.src)">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row"><div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Mysterious jasmine and rich dark cocoa.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Almond | <b>Base:</b> Cocoa</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#555;">SEDUCTIVE FEMALE</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div>
                <div class="size-container"><div class="size-box">5ML</div><div class="size-box" style="border-color: #1a4d99 !important; color: #1a4d99;">10ML</div></div>
            </div>
            <div class="form-side"><form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <script>
        function zoom(src) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = src;
            overlay.style.display = 'flex';
        }
    </script>
</body>
</html>
