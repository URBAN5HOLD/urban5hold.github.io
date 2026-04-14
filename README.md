
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Fragrance | High-End Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #D4AF37; --white: #ffffff; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        /* سيستيم الهبوط الحر - كل عطر كياخد الشاشة كاملة */
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; }

        .section {
            height: 100vh;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            scroll-snap-align: start; /* كايجر الكليان للقسم نيشان */
            overflow: hidden;
        }

        /* الخلفية الميديا (فيديو أو صورة لكل قسم) */
        .bg-container {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: 1;
        }
        .bg-container video, .bg-container img {
            width: 100%; height: 100%; object-fit: cover;
            filter: brightness(0.5); /* باش تبان الكتيبة واضحة */
        }

        .content {
            position: relative;
            z-index: 10;
            text-align: center;
            max-width: 800px;
            padding: 20px;
        }

        h2 { font-family: 'Playfair Display', serif; font-size: 4rem; color: var(--gold); margin-bottom: 20px; text-transform: uppercase; letter-spacing: 5px; }
        .tagline { font-size: 1.2rem; font-weight: 200; margin-bottom: 40px; letter-spacing: 2px; }

        /* فورم الحجز الراقية */
        .glass-form {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 40px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 5px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        .full-width { grid-column: span 2; }
        
        input {
            background: transparent; border: none; border-bottom: 1px solid rgba(255,255,255,0.3);
            color: #fff; padding: 15px; outline: none; transition: 0.3s; font-family: 'Montserrat';
        }
        input:focus { border-bottom-color: var(--gold); }
        
        .order-btn {
            grid-column: span 2;
            background: var(--gold); color: #000; border: none;
            padding: 20px; font-weight: 600; cursor: pointer;
            text-transform: uppercase; letter-spacing: 2px; transition: 0.4s;
        }
        .order-btn:hover { background: #fff; letter-spacing: 4px; }

        /* لوغو فيكسد */
        .main-logo { position: fixed; top: 30px; left: 50%; transform: translateX(-50%); z-index: 100; font-family: 'Playfair Display'; font-size: 1.5rem; letter-spacing: 10px; color: var(--gold); }

        @media (max-width: 768px) {
            h2 { font-size: 2.5rem; }
            .glass-form { grid-template-columns: 1fr; }
            .full-width { grid-column: span 1; }
            .order-btn { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <div class="main-logo">VELOORIA</div>

    <section class="section" id="sauvage">
        <div class="bg-container">
            <video autoplay muted loop playsinline><source src="sauvage_video.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <h2>Sauvage Elixir</h2>
            <p class="tagline">التركيز الأقصى.. هيبة لا تنتهي</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="العنوان والمدينة" class="full-width" required>
                <button type="submit" class="order-btn">احجز الآن - 319 DH</button>
            </form>
        </div>
    </section>

    <section class="section" id="swy">
        <div class="bg-container">
            <video autoplay muted loop playsinline><source src="armani_video.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <h2>Intensely You</h2>
            <p class="tagline">دفء العاطفة وجاذبية العنبر</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="العنوان والمدينة" class="full-width" required>
                <button type="submit" class="order-btn">احجز الآن - 289 DH</button>
            </form>
        </div>
    </section>

    <section class="section" id="libre">
        <div class="bg-container">
            <video autoplay muted loop playsinline><source src="libre_video.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <h2>YSL Libre</h2>
            <p class="tagline">عطر الحرية والأنوثة الطاغية</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="العنوان والمدينة" class="full-width" required>
                <button type="submit" class="order-btn">احجز الآن - 299 DH</button>
            </form>
        </div>
    </section>

    <section class="section" id="goodgirl">
        <div class="bg-container">
            <video autoplay muted loop playsinline><source src="goodgirl_video.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <h2>Good Girl Glam</h2>
            <p class="tagline">جرأة الكرز وقوة الورد</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="العنوان والمدينة" class="full-width" required>
                <button type="submit" class="order-btn">احجز الآن - 299 DH</button>
            </form>
        </div>
    </section>

</body>
</html>
