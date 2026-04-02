<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lisseur Professionnel - صالون في دارك</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&family=Playfair+Display:ital,wght@1,600&display=swap" rel="stylesheet">
    <style>
        :root {
            --accent-color: #d4a373; /* لون ذهبي ناعم */
            --pink-bg: #fff5f6; /* خلفية وردية خفيفة */
            --dark-text: #333;
            --cta-color: #e63946; /* لون زر الطلب واضح */
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #fff;
            color: var(--dark-text);
        }

        .header-promo {
            background: #000;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            font-size: 0.9rem;
            font-weight: bold;
        }

        .container {
            width: 90%;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 30px 0;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: #8c5e58;
        }

        .main-img {
            width: 100%;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        /* Price & Badge */
        .price-section {
            margin: 20px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
        }

        .new-price {
            font-size: 2rem;
            font-weight: 700;
            color: var(--cta-color);
        }

        .old-price {
            text-decoration: line-through;
            color: #999;
        }

        /* Features List */
        .features {
            background: var(--pink-bg);
            padding: 25px;
            border-radius: 15px;
            margin: 30px 0;
        }

        .feature-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .feature-item:before {
            content: '✦';
            margin-left: 10px;
            color: var(--accent-color);
            font-weight: bold;
        }

        /* Reviews Section (Social Proof) */
        .reviews {
            margin-top: 40px;
        }

        .review-card {
            border-bottom: 1px solid #eee;
            padding: 15px 0;
        }

        .stars { color: #f1c40f; margin-bottom: 5px; }

        /* Floating CTA Button */
        .cta-container {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(255,255,255,0.9);
            padding: 15px;
            box-shadow: 0 -5px 15px rgba(0,0,0,0.1);
            z-index: 100;
            text-align: center;
        }

        .btn-order {
            background: var(--cta-color);
            color: #fff;
            text-decoration: none;
            display: block;
            padding: 15px;
            border-radius: 8px;
            font-size: 1.3rem;
            font-weight: bold;
            animation: shake 3s infinite;
        }

        @keyframes shake {
            0% { transform: translateX(0); }
            5% { transform: translateX(-5px); }
            10% { transform: translateX(5px); }
            15% { transform: translateX(0); }
        }

        /* Spacer for fixed button */
        .spacer { height: 100px; }
    </style>
</head>
<body>

    <div class="header-promo">
        شحن مجاني لجميع المدن المغربية 📦 الدفع عند الاستلام
    </div>

    <div class="container">
        <section class="hero">
            <h1>احصلي على شعر ناعم وجذاب في دقائق ✨</h1>
            <p>المكواة الاحترافية المفضلة لدى صالونات التجميل الآن بين يديك</p>
            <img src="https://via.placeholder.com/600x600" class="main-img" alt="Product Image">
        </section>

        <div class="price-section">
            <span class="new-price">349 درهم</span>
            <span class="old-price">599 درهم</span>
        </div>

        <section class="features">
            <div class="feature-item">تقنية الأيونات لحماية الشعر من التلف</div>
            <div class="feature-item">تسخين سريع في أقل من 30 ثانية</div>
            <div class="feature-item">تصميم مريح وسهل الاستخدام (2 في 1)</div>
            <div class="feature-item">مناسب لجميع أنواع الشعر (الخشن والناعم)</div>
        </section>

        <section class="reviews">
            <h3>آراء زبوناتنا الوفيات ⭐</h3>
            <div class="review-card">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <p>"بصراحة واعر بزااف، كيرطب الشعر من أول دوزة ومكايحرقش. شكراً!"</p>
                <strong>- هدى، الدار البيضاء</strong>
            </div>
            <div class="review-card">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <p>"وصلني فـ 24 ساعة، التغليف أنيق والمنتج جودته عالية."</p>
                <strong>- ليلى، طنجة</strong>
            </div>
        </section>

        <div class="spacer"></div>
    </div>

    <div class="cta-container">
        <div class="container">
            <a href="https://wa.me/2126XXXXXXXX" class="btn-order">اطلبي الآن عبر الواتساب</a>
            <p style="font-size: 0.8rem; margin: 5px 0 0;">(العرض سينتهي قريباً!)</p>
        </div>
    </div>

</body>
</html>
