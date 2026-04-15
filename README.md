<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | The Master Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@300;600;800&family=Playfair+Display:ital,wght@1,600&display=swap" rel="stylesheet">
    
    <style>
        /* الأساسيات */
        * { margin: 0; padding: 0; box-sizing: border-box; outline: none; border: none; text-decoration: none; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }

        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.3rem; letter-spacing: 10px; color: #fff; opacity: 0.8; }

        .product-section { width: 100%; position: relative; overflow: hidden; padding-bottom: 50px; }

        /* الفيديو الفوقاني لاصق */
        .v-header { height: 100vh; width: 100%; position: relative; margin-top: 0; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.45); display: block; }

        /* الشعارات على ستيل الماركات العالمية */
        .bottle-center { text-align: center; padding: 120px 0; background: #000; }
        .img-bottle { width: 85vw; max-width: 420px; filter: drop-shadow(0 0 60px var(--glow)); margin-bottom: 30px; }
        
        .brand-logo { font-size: 3.5rem; letter-spacing: 5px; color: #fff; }
        .sauvage-logo { font-family: 'Cinzel', serif; letter-spacing: 15px; }
        .armani-logo { font-family: 'Montserrat', sans-serif; font-weight: 800; }
        .libre-logo { font-family: 'Bodoni Moda', serif; font-style: italic; letter-spacing: 2px; }
        .gg-logo { font-family: 'Playfair Display', serif; font-style: italic; }

        /* التصميم العريض جداً */
        .row { display: flex; align-items: center; width: 100%; min-height: 650px; padding: 40px 0; }
        .row.rev { flex-direction: row-reverse; }

        .img-box { width: 50%; display: flex; }
        .row .img-box { justify-content: flex-start; }
        .row.rev .img-box { justify-content: flex-end; }
        .img-box img { width: 100%; max-width: 750px; filter: brightness(0.75); object-fit: cover; }

        .txt-box { width: 50%; padding: 0 7%; position: relative; z-index: 5; text-align: center; }
        
        /* الانعكاس الضبابي المجهد */
        .glow-effect { 
            position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); 
            width: 140%; height: 140%; 
            background: radial-gradient(circle, var(--glow) 0%, transparent 70%); 
            opacity: 0.45; filter: blur(110px); z-index: -1; 
        }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.8rem; color: var(--color); margin-bottom: 25px; font-style: italic; }
        .desc-full { font-size: 1.1rem; line-height: 2; color: #ddd; text-align: center; }

        .specs-list { margin-top: 30px; list-style: none; display: inline-block; text-align: left; }
        .specs-list li { margin-bottom: 12px; font-size: 1rem; }
        .specs-list b { color: var(--color); }

        /* فورم الحجز الهربان (Glass Design) */
        .f-wrap { padding: 120px 0; text-align: center; }
        .f-glass { 
            max-width: 480px; margin: 0 auto; padding: 50px; 
            background: rgba(255, 255, 255, 0.03); 
            backdrop-filter: blur(15px); -webkit-backdrop-filter: blur(15px);
            border-radius: 30px;
        }
        .in-f { 
            width: 100%; padding: 22px; margin-bottom: 18px; 
            background: rgba(255, 255, 255, 0.05); 
            color: #fff; border-radius: 15px; text-align: center; font-size: 1rem;
            transition: 0.3s;
        }
        .in-f:focus { background: rgba(255, 255, 255, 0.1); }
        .btn-f { 
            width: 100%; padding: 22px; background: #fff; color: #000; 
            font-weight: 800; cursor: pointer; border-radius: 15px; 
            text-transform: uppercase; letter-spacing: 3px; transition: 0.5s;
        }
        .btn-f:hover { transform: scale(1.05); box-shadow: 0 0 30px var(--glow); }
        .pri-txt { color: var(--color); margin-top: 25px; font-weight: 600; font-size: 0.9rem; letter-spacing: 1px; }

        /* الألوان الدقيقة لكل عطر */
        .sauv-t { --glow: rgba(0, 71, 171, 0.8); --color: #4A90E2; } /* أزرق ديور */
        .arman-t { --glow: rgba(205, 127, 50, 0.7); --color: #CD7F32; } /* برونزي أرماني */
        .libre-t { --glow: rgba(212, 175, 55, 0.7); --color: #D4AF37; } /* ذهبي إيف سان لوران */
        .gg-t { --glow: rgba(227, 30, 36, 0.7); --color: #E31E24; } /* أحمر كارولينا هيريرا */

        @media (max-width: 1000px) { 
            .row, .row.rev { flex-direction: column; } 
            .img-box, .txt-box { width: 100%; padding: 40px 5%; }
            .img-box { justify-content: center !important; }
            .brand-logo { font-size: 2.5rem; }
        }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle"><h1 class="brand-logo sauvage-logo">SAUVAGE</h1></div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p class="desc-full">An extraordinarily concentrated fragrance steeped in the iconic freshness of Sauvage with an intoxicating heart of spices.</p></div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Full Name" class="in-f"><input type="tel" placeholder="Phone Number" class="in-f"><button type="submit" class="btn-f">ORDER NOW | 319 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section arman-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/armani.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/armani-bottle.png" class="img-bottle"><h1 class="brand-logo armani-logo">ARMANI</h1></div>
        <div class="row">
            <div class="img-box"><img src="assets/armani-left.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Essence</h3><p class="desc-full">A warm, sensual story of excitement and attraction. It features a unique blend of spicy cardamom and smoky vanilla.</p></div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Full Name" class="in-f"><input type="tel" placeholder="Phone Number" class="in-f"><button type="submit" class="btn-f">ORDER NOW | 289 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle"><h1 class="brand-logo libre-logo">LIBRE</h1></div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box"><div class="glow-effect"></div><h3>The Freedom</h3><p class="desc-full">The burning sensuality of Moroccan orange blossom is twisted with the aromatic boldness of French lavender.</p></div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Full Name" class="in-f"><input type="tel" placeholder="Phone Number" class="in-f"><button type="submit" class="btn-f">ORDER NOW | 299 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle"><h1 class="brand-logo gg-logo">Good Girl</h1></div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p class="desc-full">The sweet, alluring qualities of jasmine bring Good Girl a bright femininity. Cocoa and tonka express its mysterious side.</p>
                <ul class="specs-list">
                    <li><b>For:</b> Her | <b>She Is:</b> Seductive & Strong</li>
                    <li><b>Occasion:</b> Day & Night</li>
                    <li><b>Olfactive Family:</b> Ambery Floral</li>
                </ul>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Bottle</h3>
                <p class="desc-full">Combining haute couture aesthetics, the iconic Good Girl stiletto reflects powerful women.</p>
                <div class="tech-notes">
                    <p>*Top notes: First impression, 5-15 mins.</p>
                    <p>*Heart notes: Character, 20-60 mins.</p>
                    <p>*Base notes: Underlying aroma, 6 hours.</p>
                </div>
            </div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Full Name" class="in-f"><input type="tel" placeholder="Phone Number" class="in-f"><input type="text" placeholder="City & Address" class="in-f"><button type="submit" class="btn-f">ORDER NOW | 299 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

</body>
</html>
