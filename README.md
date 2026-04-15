<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | تجربة الحجز الملكي</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; }

        /* اللوغو الفيكسد */
        .logo-fixed {
            position: fixed; top: 25px; left: 50%; transform: translateX(-50%);
            z-index: 1000; font-family: 'Playfair Display';
            font-size: 1.4rem; letter-spacing: 10px; color: #fff;
            text-shadow: 0 0 10px rgba(0,0,0,0.5);
        }

        .section {
            height: 100vh; width: 100%; display: flex; flex-direction: column;
            align-items: center; justify-content: center;
            position: relative; scroll-snap-align: start; overflow: hidden;
        }

        /* الميديا (الفيديو) */
        .bg-wrapper { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; }
        .bg-wrapper video { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.45); }

        .content { position: relative; z-index: 10; text-align: center; width: 90%; max-width: 480px; }

        /* تصويرة القرعة */
        .product-img {
            width: 160px; height: auto; margin-bottom: 5px;
            filter: drop-shadow(0px 10px 20px rgba(0,0,0,0.9));
            animation: fadeInDown 1.5s ease forwards;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* الفورم الزجاجية السينمائية */
        .glass-form {
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px);
            padding: 35px 25px; border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 2px;
            
            /* التأخير السينمائي 4 ثواني */
            opacity: 0; transform: translateY(40px);
            animation: fadeInUp cinematic 1.8s cubic-bezier(0.4, 0, 0.2, 1) forwards;
            animation-delay: 4s;
        }

        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }

        h2 { 
            font-family: 'Playfair Display', serif; font-size: 2.8rem; 
            color: #fff; margin-bottom: 15px; text-transform: uppercase; 
            letter-spacing: 3px; 
        }

        input {
            width: 100%; background: transparent; border: none; 
            border-bottom: 1px solid rgba(255,255,255,0.2);
            color: #fff; padding: 15px 5px; margin-bottom: 15px; 
            outline: none; transition: 0.3s; font-family: 'Montserrat';
        }
        input:focus { border-bottom-color: #D4AF37; }
        
        /* اختفاء Placeholder عند الكتابة */
        input::placeholder { color: rgba(255,255,255,0.5); font-style: italic; transition: 0.2s; }
        input:focus::placeholder { opacity: 0; }

        .order-btn {
            background: #fff; color: #000; border: none; padding: 18px; width: 100%;
            font-weight: 600; text-transform: uppercase; letter-spacing: 2px;
            cursor: pointer; transition: 0.4s; margin-top: 10px;
        }
        .order-btn:hover { background: #D4AF37; color: #fff; letter-spacing: 4px; }

        /* سيكولوجية الحجز المسبق */
        .priority-tag { font-size: 0.75rem; color: #D4AF37; margin-top: 15px; letter-spacing: 1px; font-weight: 600; }
        .batch-alert { font-size: 0.7rem; color: rgba(255,255,255,0.7); margin-top: 5px; font-style: italic; }

        @media (max-width: 768px) {
            h2 { font-size: 2rem; }
            .product-img { width: 130px; }
        }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/sauvage.mp4" type="video/mp4"></video>
        </div>
        
        <div class="content">
            <img src="assets/sauvage-bottle.png" alt="Sauvage" class="product-img">
            
            <form class="glass-form">
                <h2>Sauvage Elixir</h2>
                <input type="text" placeholder="تفضل بوضع اسمك يا سيدي..." required>
                <input type="tel" placeholder="رقم هاتفك الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                
                <button type="submit" class="order-btn">احجز الآن | 319 DH</button>
                
                <p class="priority-tag">📅 الدفعة الأولى: قيد التحضير اليدوي الآن</p>
                <p class="batch-alert">تم حجز 17 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/libre.mp4" type="video/mp4"></video>
        </div>
        
        <div class="content">
            <img src="assets/libre-bottle.png" alt="Libre" class="product-img">
            
            <form class="glass-form">
                <h2>YSL Libre</h2>
                <input type="text" placeholder="اسمكِ سيدتي الجميلة..." required>
                <input type="tel" placeholder="رقم هاتفكِ الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                
                <p class="priority-tag">👑 أسبقية التوصيل حسب ترتيب الحجز المسبق</p>
                <p class="batch-alert">المقاعد المتبقية في دفعة هذا الأسبوع: 4 فقط</p>
            </form>
        </div>
    </section>

    </body>
</html>
