<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@300;400;600;800&family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">
    
    <style>
        /* كود إزالة أي فراغات أو هوامش من GitHub */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { 
            margin: 0 !important; 
            padding: 0 !important; 
            width: 100%; 
            background-color: #000; 
            color: #fff; 
            font-family: 'Montserrat', sans-serif; 
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.5rem; letter-spacing: 12px; color: #fff; }

        .product-master-wrapper { margin-bottom: 20px; border-bottom: 1px solid rgba(255,255,255,0.05); }

        /* Hero Section */
        .hero-section { height: 100vh; width: 100%; position: relative; display: flex; flex-direction: column; align-items: center; justify-content: center; margin: 0 !important; }
        .bg-video { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; object-fit: cover; filter: brightness(0.4); }
        .hero-content { position: relative; z-index: 10; text-align: center; }
        .product-img-main { width: 80vw; max-width: 380px; filter: drop-shadow(0px 20px 60px rgba(0,0,0,1)); }

        /* Details Sections */
        .details-section { min-height: 50vh; width: 100%; display: flex; align-items: center; padding: 30px 8%; gap: 20px; background: #050505; }
        .details-section.reverse { flex-direction: row-reverse; background: #000; }

        .text-side { flex: 1.2; text-align: center; }
        .image-side { flex: 0.8; display: flex; justify-content: center; }
        .side-img { width: 100%; max-width: 320px; border-radius: 5px; filter: brightness(0.7); }

        /* Typography */
        h2 { margin-bottom: 0; }
        h3 { font-family: 'Playfair Display', serif; font-size: 1.8rem; margin-bottom: 8px; border: none; } /* حيدت الخط */
        .desc-text { font-size: 0.95rem; line-height: 1.5; color: #bbb; max-width: 550px; margin: 0 auto; }
        
        .notes-grid { margin-top: 10px; display: grid; gap: 8px; }
        .note-item b { color: #fff; display: block; font-size: 0.75rem; text-transform: uppercase; letter-spacing: 1px; }

        /* Form Styling */
        .form-container { padding: 40px 5%; text-align: center; background: #000; }
        .glass-form { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px); padding: 30px 20px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.05); max-width: 420px; margin: 0 auto; }
        
        .input-field { width: 100%; background: rgba(255,255,255,0.05); border: none; padding: 14px; margin-bottom: 10px; border-radius: 10px; color: #fff; text-align: center; outline: none; border: 1px solid rgba(255,255,255,0.1); }
        
        .order-btn { width: 100%; padding: 16px; border-radius: 10px; font-weight: 800; cursor: pointer; border: none; text-transform: uppercase; letter-spacing: 2px; color: #fff; transition: 0.4s; }
        
        .priority-msg { font-size: 0.8rem; margin-top: 12px; letter-spacing: 0.5px; font-weight: 500; font-style: italic; }

        /* تيمات الألوان المخصصة */
        .sauvage-theme h3, .sauvage-theme .note-item p { color: #4A90E2; }
        .sauvage-theme .order-btn { background: #1A365D; }
        .sauvage-theme .priority-msg { color: #4A90E2; }

        .armani-theme h3, .armani-theme .note-item p { color: #CD7F32; }
        .armani-theme .order-btn { background: #8B4513; }
        .armani-theme .priority-msg { color: #CD7F32; }

        .libre-theme h3, .libre-theme .note-item p { color: #D4AF37; }
        .libre-theme .order-btn { background: #B8860B; }
        .libre-theme .priority-msg { color: #D4AF37; }

        .goodgirl-theme h3, .goodgirl-theme .note-item p { color: #E31E24; }
        .goodgirl-theme .order-btn { background: #8B0000; }
        .goodgirl-theme .priority-msg { color: #E31E24; }

        @media (max-width: 900px) { .details-section, .details-section.reverse { flex-direction: column; padding: 30px 5%; } .product-img-main { width: 90vw; } }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-master-wrapper sauvage-theme">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/sauvage.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/sauvage-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Cinzel', serif; font-size: 3.5rem; letter-spacing: 8px;">SAUVAGE</h2>
            </div>
        </section>
        <section class="details-section">
            <div class="image-side"><img src="assets/sauvage-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">Extraordinarily concentrated, steeped in iconic freshness with an intoxicating heart of spices.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Him | <b>Family:</b> Woody Aromatic</div>
                </div>
            </div>
        </section>
        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 319 DH</button>
                <p class="priority-msg">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper armani-theme">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/armani.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/armani-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 2rem;">STRONGER WITH YOU</h2>
            </div>
        </section>
        <section class="details-section">
            <div class="image-side"><img src="assets/armani-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">A warm, sensual story of excitement featuring notes of spicy cardamom and smoky vanilla.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Him | <b>Family:</b> Fougere Amber</div>
                </div>
            </div>
        </section>
        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 289 DH</button>
                <p class="priority-msg">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper libre-theme">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/libre.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/libre-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Bodoni Moda', serif; font-style: italic; font-size: 3.2rem;">Libre</h2>
            </div>
        </section>
        <section class="details-section">
            <div class="image-side"><img src="assets/libre-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">Grand floral eau de parfum. The burning sensuality of Moroccan orange blossom with French lavender.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Her | <b>Family:</b> Floral Lavender</div>
                </div>
            </div>
        </section>
        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="priority-msg">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper goodgirl-theme">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/goodgirl.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/goodgirl-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Playfair Display', serif; font-size: 2.8rem;">Good Girl Glam</h2>
            </div>
        </section>
        <section class="details-section">
            <div class="image-side"><img src="assets/gg-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">Intense cherry top notes echoed in a shimmering stiletto bottle. Feminine, captivating, and bold.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Her | <b>Family:</b> Floral Woody Amber</div>
                </div>
            </div>
        </section>
        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="priority-msg">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </section>
    </div>

</body>
</html>
