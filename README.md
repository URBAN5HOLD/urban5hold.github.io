<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر فيلوريا - عرض خاص</title> <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --main-pink: #fce4ec;
            --dark-pink: #f06292;
            --gold: #d4af37;
            --black: #212121;
        }

        /* هادي باش نحيدو أي فراغ الفوق ونخبيو العنوان */
        * { box-sizing: border-box; }
        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #fff;
            color: var(--black);
            text-align: center;
        }

        /* شريط التوصيل - الوسط */
        .promo-bar { 
            background: var(--black); 
            color: #fff; 
            padding: 12px; 
            font-weight: bold; 
            font-size: 15px; 
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
        }

        .timer-container {
            background: #fff3f3;
            padding: 15px;
            margin: 0; /* حيدنا المارجين باش تلصق مع الشريط الأسود */
            border-bottom: 1px solid #ffcdd2;
        }
        #timer { font-size: 24px; font-weight: bold; color: #d32f2f; }

        .hero-img { width: 90%; max-width: 450px; border-radius: 15px; margin: 20px auto; display: block; }

        .price-tag { font-size: 28px; margin: 20px 0; }
        .discount-badge { background: #ff5252; color: #fff; padding: 5px 15px; border-radius: 5px; font-size: 18px; }

        /* تنسيق زر الواتساب باش يجي في الوسط 100% */
        .sticky-footer {
            position: fixed;
            bottom: 0;
            left: 0; /* ضروري */
            right: 0; /* ضروري */
            width: 100%;
            background: #fff;
            padding: 15px 0;
            box-shadow: 0 -5px 15px rgba(0,0,0,0.1);
            z-index: 10000;
            display: flex;
            justify-content: center; /* هادي كتجيب المحتوى للوسط */
            align-items: center;
        }

        .cta-btn {
            background: #25D366; 
            color: white;
            padding: 15px 0; /* حيدنا Padding الجناب */
            width: 80%; /* عطيناه عرض محدد */
            max-width: 350px; /* باش ما يجيش عريض بزاف فـ الـ PC */
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.3rem;
            display: block; /* باش يحترم العرض */
            margin: 0 auto; /* هادي هي اللي كتجيبو للوسط */
            animation: pulse 2s infinite;
        }

        .info-card { padding: 20px; margin-bottom: 20px; }
        .info-card img { width: 90%; max-width: 400px; border-radius: 10px; }

        @keyframes pulse { 0% {transform: scale(1);} 50% {transform: scale(1.05);} 100% {transform: scale(1);} }
        .spacer { height: 100px; }

        /* تعاليق البنات */
        .review-card {
            background: #fff;
            padding: 15px;
            border-radius: 12px;
            margin: 10px auto;
            width: 90%;
            max-width: 500px;
            text-align: right;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            gap: 10px;
        }
        .profile-img { width: 45px; height: 45px; border-radius: 50%; background: #eee; }
    </style>
</head>
<body>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0; font-weight: bold;">سالي الخصم ديال 50% فـ:</p>
        <div id="timer">05:00:00</div>
    </div>

    <section>
        <h1 style="color: var(--dark-pink); font-size: 1.5rem; padding: 20px 10px;">احصلي على شعر حريري في أقل من 5 دقائق ✨</h1>
        <img src="https://via.placeholder.com/500x500" class="hero-img" alt="Product Image">
        
        <div class="price-tag">
            <span style="text-decoration: line-through; color: #999; font-size: 18px;">499 درهم</span><br>
            <strong>249 درهم فقط</strong> <span class="discount-badge">تخفيض 50%</span>
        </div>
    </section>

    <div class="info-card">
        <img src="https://via.placeholder.com/400x400" alt="شرح 1">
        <h3>سهل الاستعمال 💆‍♀️</h3>
        <p>بلا ما تحتاجي تمشي للصالون، هاد المشط كيسخن فـ 30 ثانية وكيسرح الشعر بكل سهولة.</p>
    </div>

    <div class="spacer"></div>

    <div class="sticky-footer">
        <a href="https://wa.me/2126691444558" class="cta-btn">اطلبي الآن عبر الواتساب</a>
    </div>

    <script>
        function startTimer(duration, display) {
            var timer = duration, hours, minutes, seconds;
            setInterval(function () {
                hours = parseInt(timer / 3600, 10);
                minutes = parseInt((timer % 3600) / 60, 10);
                seconds = parseInt(timer % 60, 10);
                hours = hours < 10 ? "0" + hours : hours;
                minutes = minutes < 10 ? "0" + minutes : minutes;
                seconds = seconds < 10 ? "0" + seconds : seconds;
                display.textContent = hours + ":" + minutes + ":" + seconds;
                if (--timer < 0) { timer = duration; }
            }, 1000);
        }
        window.onload = function () {
            var fiveHours = 60 * 60 * 5, display = document.querySelector('#timer');
            startTimer(fiveHours, display);
        };
    </script>

</body>
</html>
