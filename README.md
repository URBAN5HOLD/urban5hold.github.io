<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* الحل الجذري لتحرك الصفحة يميناً ويساراً */
        html, body { 
            max-width: 100%; 
            overflow-x: hidden; 
            background-color: #000; 
            margin: 0; padding: 0;
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { width: 100vw; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; overflow: hidden; padding-bottom: 60px; }

        /* تعديل الفيديو ليملاً الشاشة من القنت للقنت */
        .v-header { 
            width: 100%; 
            height: 100vh; /* الفيديو كياخد الشاشة كاملة في الطول فاش كتحل الصفحة */
            overflow: hidden; 
            position: relative; 
        }
        .bg-v { 
            width: 100%; 
            height: 100%; 
            object-fit: cover; /* هادي هي السر باش الفيديو يعمر المستطيل كامل بلا فراغات */
            display: block; 
        }
        
        .bottle-center { text-align: center; padding: 40px 0; }
        .img-bottle { width: 40%; max-width: 180px; height: auto; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; margin-top: 10px; letter-spacing: 5px; }

        .row { display: flex; align-items: center; width: 100%; padding: 40px 5%; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 95%; max-width: 450px; border-radius: 2px; }
        .txt-box { width: 50%; padding: 0 5%; text-align: left; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 120%; height: 120%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.25; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.6rem; color: var(--color); margin-bottom: 12px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; }
        p { font-size: 0.85rem; line-height: 1.6; color: #eee; margin-bottom: 10px; }

        /* منطقة الشراء المعدلة لتناسب شاشة التلفون */
        .purchase-area { 
            max-width: 100%; 
            margin: 40px auto; 
            display: flex; 
            flex-wrap: wrap; /* باش تهبط العناصر فاش تصغار الشاشة */
            gap: 30px; 
            padding: 0 20px; 
        }
        .details-side { flex: 1; min-width: 300px; }
        .form-side { flex: 1.2; min-width: 300px; }

        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .mini-thumb { width: 60px; height: 60px; border-radius: 2px; object-fit: cover; }
        
        .size-container { display: flex; gap: 15px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 15px; border: 1px solid rgba(255,255,255,0.1) !important; border-radius: 2px; transition: 0.3s; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); }

        .form-side input { width: 100%; padding: 15px; margin-bottom: 10px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.1) !important; }
        .buy-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; font-size: 1rem; cursor: pointer; margin-top: 10px; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 768px) {
            .row, .row.rev { flex-direction: column; text-align: center; }
            .img-box, .txt-box { width: 100%; padding: 20px; }
            .v-header { height: 60vh; } /* فالتلفون نقصو شوية الطول باش يبان النص تحت الفيديو */
            .purchase-area { flex-direction: column; }
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
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><h3>The Fragrance</h3><p>Raw elegance that reveals an authentic man.</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE</h2><p>PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb" onclick="zoom(this.src)"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 's1')"><div class="size-box"><span>5ML</span><p style="font-size:10px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 's1')"><div class="size-box"><span>10ML</span><p style="font-size:10px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side">
                <form><input type="hidden" id="s1" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form>
            </div>
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
