<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | The Master Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@300;400;600;800&family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        /* الهيدر */
        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.5rem; letter-spacing: 12px; color: #fff; text-shadow: 0 0 15px rgba(0,0,0,1); }

        /* الأقسام الرئيسية */
        .product-master-wrapper { border-bottom: 2px solid rgba(255,255,255,0.05); margin-bottom: 50px; }

        .hero-section { height: 100vh; width: 100%; position: relative; display: flex; flex-direction: column; align-items: center; justify-content: center; }
        .bg-video { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; object-fit: cover; filter: brightness(0.4); }
        .hero-content { position: relative; z-index: 10; text-align: center; }
        .product-img-main { width: 75vw; max-width: 380px; filter: drop-shadow(0px 20px 60px rgba(0,0,0,1)); }

        /* تفاصيل المنتج */
        .details-section { min-height: 70vh; width: 100%; display: flex; align-items: center; padding: 60px 8%; gap: 50px; background: #050505; }
        .details-section.reverse { flex-direction: row-reverse; background: #000; }

        .text-side { flex: 1.2; text-align: center; }
        .image-side { flex: 0.8; display: flex; justify-content: center; }
        .side-img { width: 100%; max-width: 350px; border-radius: 2px; filter: brightness(0.8); transition: 0.5s; }
        .side-img:hover { filter: brightness(1); transform: scale(1.02); }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.2rem; margin-bottom: 20px; color: #D4AF37; letter-spacing: 2px; }
        .desc-text { font-size: 1rem; line-height: 1.8; color: #bbb; max-width: 550px; margin: 0 auto; }
        
        .notes-grid { margin-top: 25px; display: grid; gap: 15px; }
        .note-item b { color: #fff; display: block; font-size: 0.85rem; text-transform: uppercase; letter-spacing: 1px; }
        .note-item p { font-size: 0.95rem; color: #D4AF37; }

        /* فورم الحجز */
        .form-container { padding: 80px 5%; text-align: center; background: #000; }
        .glass-form { background: rgba(255, 255, 255, 0.04); backdrop-filter: blur(25px); -webkit-backdrop-filter: blur(25px); padding: 40px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.1); max-width: 450px; margin: 0 auto; }
        
        .input-field { width: 100%; background: rgba(255,255,255,0.06); border: none; padding: 16px; margin-bottom: 15px; border-radius: 15px; color: #fff; text-align: center; outline: none; transition: 0.3s; }
        .input-field:focus { background: rgba(255,255,255,0.1); }

        .order-btn { background: #fff; color: #000; width: 100%; padding: 20px; border-radius: 15px; font-weight: 800; cursor: pointer; border: none; text-transform: uppercase; letter-spacing: 3px; transition: 0.4s; }
        .order-btn:hover { background: #D4AF37; color: #fff; transform: translateY(-3px); }

        .batch-info { font-size: 0.75rem; color: #777; margin-top: 15px; letter-spacing: 1px; }

        @media (max-width: 900px) { .details-section, .details-section.reverse { flex-direction: column; padding: 50px 5%; } .product-img-main { width: 85vw; } }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-master-wrapper">
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
                <p class="desc-text">Sauvage Elixir is an extraordinarily concentrated fragrance steeped in the iconic freshness of Sauvage with an intoxicating heart of Spices, a "tailor-made" Lavender essence and a blend of rich Woods.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Him</div>
                    <div class="note-item"><b>He Is:</b> Raw & Noble</div>
                    <div class="note-item"><b>Olfactive Family:</b> Woody Aromatic</div>
                </div>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side"><img src="assets/sauvage-detail-2.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Notes</h3>
                <div class="notes-grid">
                    <div class="note-item"><b>Top Notes</b><p>Cinnamon, Nutmeg, Cardamom & Grapefruit</p></div>
                    <div class="note-item"><b>Heart Notes</b><p>Lavender Essence</p></div>
                    <div class="note-item"><b>Base Notes</b><p>Licorice, Sandalwood, Amber & Patchouli</p></div>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 319 DH</button>
                <p class="batch-info">تم حجز 14 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/armani.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/armani-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 2.5rem;">STRONGER WITH YOU</h2>
            </div>
        </section>

        <section class="details-section">
            <div class="image-side"><img src="assets/armani-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">This fragrance for men is a warm, sensual eau de parfum, featuring notes of spicy cardamom and smoky vanilla. It tells a story of excitement and mysterious attraction.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Him</div>
                    <div class="note-item"><b>He Is:</b> Sensual & Confident</div>
                    <div class="note-item"><b>Olfactive Family:</b> Fougere Amber</div>
                </div>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side"><img src="assets/armani-detail-2.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Notes</h3>
                <div class="notes-grid">
                    <div class="note-item"><b>Top Notes</b><p>Cardamom, Pink Pepper, Violet Leaf</p></div>
                    <div class="note-item"><b>Heart Notes</b><p>Sage, Melon, Pineapple</p></div>
                    <div class="note-item"><b>Base Notes</b><p>Vanilla, Chestnut, Cedarwood</p></div>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 289 DH</button>
                <p class="batch-info">تم حجز 14 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/libre.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/libre-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Bodoni Moda', serif; font-style: italic; font-size: 3.5rem;">Libre</h2>
            </div>
        </section>

        <section class="details-section">
            <div class="image-side"><img src="assets/libre-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">Libre is a grand floral eau de parfum, with an unequivocal YSL twist. The burning sensuality of the orange blossom from Morocco, twisted with the aromatic boldness of lavender from France.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Her</div>
                    <div class="note-item"><b>She Is:</b> Free & Fierce</div>
                    <div class="note-item"><b>Olfactive Family:</b> Floral Lavender</div>
                </div>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side"><img src="assets/libre-detail-2.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Notes</h3>
                <div class="notes-grid">
                    <div class="note-item"><b>Top Notes</b><p>Lavender, Mandarin Orange, Black Currant</p></div>
                    <div class="note-item"><b>Heart Notes</b><p>Orange Blossom, Jasmine</p></div>
                    <div class="note-item"><b>Base Notes</b><p>Madagascar Vanilla, Musk, Ambergris</p></div>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="batch-info">تم حجز 14 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </section>
    </div>

    <div class="product-master-wrapper">
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/goodgirl.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/goodgirl-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Playfair Display', serif; font-size: 3rem;">Good Girl Glam</h2>
            </div>
        </section>

        <section class="details-section">
            <div class="image-side"><img src="assets/gg-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">Very Good Girl Glam Parfum showcases intense cherry top notes echoed in its shimmering stiletto bottle. Upcycled rose water amplifies the feminine heart of the fragrance.</p>
                <div class="notes-grid">
                    <div class="note-item"><b>For:</b> Her</div>
                    <div class="note-item"><b>She Is:</b> Captivating & Bold</div>
                    <div class="note-item"><b>Olfactive Family:</b> Floral Woody Amber</div>
                </div>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side"><img src="assets/gg-detail-2.jpg" class="side-img"></div>
            <div class="text-side">
                <h3>The Notes</h3>
                <div class="notes-grid">
                    <div class="note-item"><b>Top Notes</b><p>Black Cherry & Bitter Almond</p></div>
                    <div class="note-item"><b>Heart Notes</b><p>Rose & Ambrette Seeds</p></div>
                    <div class="note-item"><b>Base Notes</b><p>Vanilla Bourbon & Tonka Bean</p></div>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="batch-info">تم حجز 14 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </section>
    </div>

</body>
</html>
