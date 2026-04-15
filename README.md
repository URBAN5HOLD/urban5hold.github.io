<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.5rem; letter-spacing: 12px; color: #fff; }

        .product-section { position: relative; width: 100%; border-bottom: 1px solid rgba(255,255,255,0.05); margin-bottom: 50px; }

        /* 1. Video */
        .v-header { height: 100vh; width: 100%; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.5); }

        /* 2. Central Bottle & Title */
        .bottle-center { text-align: center; padding: 80px 0; background: #000; }
        .img-bottle { width: 80vw; max-width: 400px; filter: drop-shadow(0 0 40px var(--glow)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.8rem; margin-top: 20px; letter-spacing: 6px; }

        /* 3. Details (Free Layout) */
        .row { display: flex; align-items: center; padding: 60px 10%; gap: 60px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { flex: 1; display: flex; justify-content: center; }
        .img-box img { width: 100%; max-width: 420px; filter: brightness(0.8); }
        
        .txt-box { flex: 1.2; position: relative; }
        /* الانعكاس الملون الضبابي */
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 130%; height: 130%; background: radial-gradient(circle, var(--glow) 0%, transparent 75%); opacity: 0.12; filter: blur(70px); z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.2rem; color: var(--color); margin-bottom: 15px; }
        .p-text { font-size: 1rem; line-height: 1.8; color: #ccc; text-align: justify; }
        .notes { margin-top: 20px; list-style: none; }
        .notes li { margin-bottom: 8px; font-size: 0.9rem; }
        .notes b { color: var(--color); letter-spacing: 1px; }

        /* 4. Order Form */
        .f-wrap { padding: 80px 0; text-align: center; }
        .f-glass { max-width: 450px; margin: 0 auto; padding: 30px; }
        .in-f { width: 100%; padding: 18px; margin-bottom: 12px; background: rgba(255,255,255,0.06); border: 1px solid rgba(255,255,255,0.1); color: #fff; border-radius: 8px; text-align: center; }
        .btn-f { width: 100%; padding: 20px; background: #f2f2f2; color: #000; border: none; font-weight: 800; cursor: pointer; border-radius: 8px; text-transform: uppercase; }
        .btn-f:hover { background: #fff; transform: scale(1.02); }
        .pri-txt { color: var(--color); margin-top: 15px; font-style: italic; font-size: 0.85rem; }

        /* الألوان لكل عطر */
        .sauv-t { --glow: #0047ab; --color: #4A90E2; }
        .arman-t { --glow: #cd7f32; --color: #CD7F32; }
        .libre-t { --glow: #d4af37; --color: #D4AF37; }
        .gg-t { --glow: #ff0000; --color: #E31E24; }

        @media (max-width: 900px) { .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; } }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle"><h1 class="brand-logo">SAUVAGE</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-1.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p class="p-text">Sauvage Elixir is an extraordinarily concentrated fragrance steeped in the iconic freshness of Sauvage with an intoxicating heart of Spices.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-2.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Composition</h3><p class="p-text">A blend of rich Woods and Lavender essence, pushing the boundaries of extreme concentration.</p></div>
        </div>

        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="الاسم الكامل" class="in-f"><input type="tel" placeholder="رقم الهاتف" class="in-f"><input type="text" placeholder="العنوان" class="in-f"><button type="submit" class="btn-f">احجز الآن | 319 DH</button><p class="pri-txt">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section arman-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/armani.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/armani-bottle.png" class="img-bottle"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/armani-1.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p class="p-text">A warm, sensual story of excitement featuring notes of spicy cardamom and smoky vanilla.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/armani-2.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Notes</h3><p class="p-text">Top: Cardamom, Heart: Sage, Base: Vanilla & Chestnut.</p></div>
        </div>

        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="الاسم الكامل" class="in-f"><input type="tel" placeholder="رقم الهاتف" class="in-f"><input type="text" placeholder="العنوان" class="in-f"><button type="submit" class="btn-f">احجز الآن | 289 DH</button><p class="pri-txt">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle"><h1 class="brand-logo">LIBRE</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/libre-1.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p class="p-text">The burning sensuality of Moroccan orange blossom twisted with French lavender.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-2.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Bottle</h3><p class="p-text">A couture statement with the iconic oversized YSL logo wrapped around the glass.</p></div>
        </div>

        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="الاسم الكامل" class="in-f"><input type="tel" placeholder="رقم الهاتف" class="in-f"><input type="text" placeholder="العنوان" class="in-f"><button type="submit" class="btn-f">احجز الآن | 299 DH</button><p class="pri-txt">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle"><h1 class="brand-logo">GOOD GIRL GLAM</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/gg-1.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p class="p-text">Intense cherry top notes echoed in its shimmering stiletto bottle. A spectacular expression of femininity.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-2.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>Composition</h3><p class="p-text">Top: Black Cherry, Heart: Rose, Base: Vanilla Bourbon.</p></div>
        </div>

        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="الاسم الكامل" class="in-f"><input type="tel" placeholder="رقم الهاتف" class="in-f"><input type="text" placeholder="العنوان" class="in-f"><button type="submit" class="btn-f">احجز الآن | 299 DH</button><p class="pri-txt">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

</body>
</html>
