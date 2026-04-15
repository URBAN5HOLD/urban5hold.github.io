<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* منع التحرك الجانبي نهائياً */
        html, body { 
            width: 100%; 
            max-width: 100vw; 
            overflow-x: hidden; 
            background-color: #000; 
            margin: 0; padding: 0;
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 6px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { width: 100vw; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; overflow: hidden; padding-bottom: 50px; }

        /* تعديل الفيديو ليصبح مستطيل من القنت للقنت */
        .v-header { 
            width: 100%; 
            height: 55vh; /* الطول 55% من الشاشة ليعطي شكل مستطيل */
            overflow: hidden; 
            position: relative; 
        }
        .bg-v { 
            width: 100%; 
            height: 100%; 
            object-fit: cover; /* لملء المستطيل بالكامل */
            display: block; 
        }
        
        .bottle-center { text-align: center; padding: 40px 0; }
        .img-bottle { width: 40%; max-width: 170px; height: auto; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; margin-top: 10px; letter-spacing: 5px; text-transform: uppercase; }

        .row { display: flex; align-items: center; width: 100%; padding: 30px 5%; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 90%; max-width: 400px; border-radius: 2px; }
        .txt-box { width: 50%; padding: 0 5%; text-align: left; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; height: 100%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.2; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.5rem; color: var(--color); margin-bottom: 12px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; }
        p { font-size: 0.85rem; line-height: 1.6; color: #eee; margin-bottom: 10px; }

        /* منطقة الشراء المودرن */
        .purchase-area { max-width: 1000px; margin: 50px auto; display: flex; gap: 40px; padding: 0 20px; align-items: flex-start; }
        .details-side { width: 45%; }
        .form-side { width: 55%; }

        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .mini-thumb { width: 55px; height: 55px; border-radius: 2px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1) !important; }
        
        .size-container { display: flex; gap: 15px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 12px; border: 1px solid rgba(255,255,255,0.1) !important; border-radius: 2px; transition: 0.3s; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); }

        .form-side input { width: 100%; padding: 15px; margin-bottom: 10px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.1) !important; font-family: 'Montserrat', sans-serif; }
        .buy-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; font-size: 1rem; cursor: pointer; margin-top: 10px; transition: 0.3s; }
        .buy-btn:hover { background: var(--color); color: #fff; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; }
            .img-box, .txt-box { width: 100%; padding: 20px; }
            .purchase-area { flex-direction: column-reverse; gap: 30px; }
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
    <div class="zoom-overlay" id="zoomOverlay" onclick="this.style.display='none'"><img src="" id="zoomedImg" style="max-width:90%"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">SAUVAGE</h1></div>
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Raw elegance that reveals an authentic man. Fresh and powerful trail.</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE ELIXIR</h2><p style="font-size:10px">PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb" onclick="zoom(this.src)"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i1')"><div class="size-box"><span>5ML</span><p style="font-size:10px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i1')"><div class="size-box"><span>10ML</span><p style="font-size:10px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i1" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        <div class="row"><div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Magnetic and sensual energy. A surprise of originality.</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>STRONGER WITH YOU</h2><p style="font-size:10px">INTENSE FRAGRANCE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb" onclick="zoom(this.src)"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i2')"><div class="size-box"><span>5ML</span><p style="font-size:10px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i2')"><div class="size-box"><span>10ML</span><p style="font-size:10px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i2" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">LIBRE (EDP)</h1></div>
        <div class="row"><div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The perfume of freedom. Sensual orange blossom and bold lavender.</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px">FEMALE ELEGANCE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb" onclick="zoom(this.src)"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i3')"><div class="size-box"><span>5ML</span><p style="font-size:10px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i3')"><div class="size-box"><span>10ML</span><p style="font-size:10px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i3" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">GOOD GIRL</h1></div>
        <div class="row"><div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The sweetness of jasmine mixed with rich cocoa and tonka bean.</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px">POWDERED SEDUCTION</p></div><img src="assets/gg-hand.jpg" class="mini-thumb" onclick="zoom(this.src)"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i4')"><div class="size-box"><span>5ML</span><p style="font-size:10px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i4')"><div class="size-box"><span>10ML</span><p style="font-size:10px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i4" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <script>
        function zoom(img) {
            document.getElementById('zoomOverlay').style.display = 'flex';
            document.getElementById('zoomedImg').src = img.src || img;
        }
        function selectSize(element, size, inputId) {
            element.parentElement.querySelectorAll('.size-item').forEach(i => i.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
