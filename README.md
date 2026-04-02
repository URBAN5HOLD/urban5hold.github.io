<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر فيلوريا - عرض خاص</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --main-pink: #fff5f6;
            --dark-pink: #f06292;
            --black: #1a1a1a;
            --green-wa: #25D366;
        }

        * { box-sizing: border-box; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; background-color: #fff; text-align: center; line-height: 1.6; }

        .promo-bar { background: var(--black); color: #fff; padding: 12px; font-weight: bold; width: 100%; font-size: 14px; }
        .timer-container { background: #fff3f3; padding: 15px; border-bottom: 2px solid #ffcdd2; }
        #timer { font-size: 28px; font-weight: bold; color: #d32f2f; }

        .hero { padding: 20px; }
        h1 { color: var(--dark-pink); font-size: 1.6rem; margin-bottom: 15px; }
        .hero-img { width: 100%; max-width: 480px; border-radius: 15px; margin: 0 auto 20px; display: block; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }

        .price-box { margin: 15px 0; }
        .new-price { font-size: 30px; color: #e91e63; font-weight: bold; }
        .badge { background: #ff5252; color: #fff; padding: 5px 12px; border-radius: 4px; font-size: 14px; }

        /* الأقسام بـ 3 صور والشرح */
        .info-card { padding: 40px 15px; border-bottom: 1px solid #eee; }
        .info-card h3 { color: var(--dark-pink); margin-bottom: 15px; }
        .info-card p { font-size: 1.1rem; color: #444; max-width: 550px; margin: 0 auto; text-align: center; padding: 0 10px; }

        /* التعاليق */
        .reviews-container { background: var(--main-pink); padding: 40px 15px; }
        .review-card {
            background: #fff; padding: 15px; border-radius: 12px; margin: 10px auto;
            width: 100%; max-width: 500px; text-align: right; display: flex; gap: 12px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .extra-reviews { display: none; }
        .profile-img { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; }
        .stars { color: #ffc107; font-size: 12px; }
        .review-name { font-weight: bold; font-size: 15px; }

        .show-more-btn {
            background: #fff; border: 1px solid var(--dark-pink); color: var(--dark-pink);
            padding: 10px 25px; border-radius: 25px; cursor: pointer; margin: 20px 0; font-weight: bold;
        }

        /* الصورة الرابعة النهائية */
        .final-proof { padding: 40px 15px; background: #fff; }

        .sticky-footer { 
            position: fixed; bottom: 0; left: 0; width: 100%; background: #fff; 
            padding: 15px 0; z-index: 9999; box-shadow: 0 -5px 15px rgba(0,0,0,0.1);
            display: flex; justify-content: center;
        }
        .cta-btn { 
            background: var(--green-wa); color: #fff; width: 85%; max-width: 380px; 
            padding: 16px; border-radius: 50px; text-decoration: none; font-weight: bold; 
            font-size: 1.3rem; display: block; margin: 0 auto; animation: pulse 2.5s infinite; 
        }

        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.03); } 100% { transform: scale(1); } }
        .spacer { height: 110px; }
    </style>
</head>
<body>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0; font-weight: bold;">ينتهي الخصم (50%-) خلال:</p>
        <div id="timer">05:00:00</div>
    </div>

    <section class="hero">
        <h1>احصلي على شعر حريري في دقائق ✨</h1>
        <img src="1.jpg" class="hero-img" alt="الصورة الرئيسية للمنتج">
        <div class="price-box">
            <span class="new-price">249 درهم</span> <span class="badge">تخفيض 50%-</span>
        </div>
    </section>

    <div class="info-card">
        <h3>سهل الاستعمال واحترافي 💆‍♀️</h3>
        <img src="2.jpg" class="hero-img" alt="شرح الميزة الأولى">
        <p>هنا تكتبي الشرح اللي كيجي تحت التصويرة التانية (مثلا: كيفاش كيسخن دغيا وكيوفر عليك وقت الصالون).</p>
    </div>

    <div class="info-card">
        <h3>حماية فائقة لشعرك 🔥</h3>
        <img src="3.jpg" class="hero-img" alt="شرح الميزة الثانية">
        <p>هنا تكتبي الشرح اللي كيجي تحت التصويرة التالتة (مثلا: تقنية السيراميك اللي كتحافظ على صحة ولمعان الشعر).</p>
    </div>

    <section class="reviews-container">
        <h2>آراء الزبونات في المنتج ⭐</h2>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">سناء - الدار البيضاء</span>
                <p style="font-size:14px; margin:5px 0;">بصراحة واعر بزااااف، هناني من السيشوار وتمارة ديالو ❤️</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/718978/pexels-photo-718978.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">ليلى - طنجة</span>
                <p style="font-size:14px; margin:5px 0;">وصلني اليوم، السلعة جودة عالية برافو 👍</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">مريم - مراكش</span>
                <p style="font-size:14px; margin:5px 0;">زوين بزاف، النتيجة عجباتني من أول استعمال.</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1587009/pexels-photo-1587009.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">خديجة</span>
                <p style="font-size:14px; margin:5px 0;">خديت جوج ليا ولختي، عجبنا بزااف مكيحرقش الشعر 🎀</p>
            </div>
        </div>

        <div class="extra-reviews" id="extraReviews">
            <div class="review-card">
                <img src="https://images.pexels.com/photos/1239291/pexels-photo-1239291.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div><div class="stars">⭐⭐⭐⭐⭐</div><span class="review-name">إيمان</span><p>طوب طوب كنصحكم بيه البنات 👌</p></div>
            </div>
        </div>

        <button class="show-more-btn" id="showMore" onclick="toggleReviews()">قراءة المزيد من الآراء</button>
    </section>

    <section class="final-proof">
        <h2>طلبيات زبوناتنا الوفيات 📸</h2>
        <img src="4.jpg" class="hero-img" alt="صورة حقيقية للمنتج">
        <p>فيلوريا تضمن لك الجودة والمصداقية في كل طلبية.</p>
    </section>

    <div class="spacer"></div>

    <div class="sticky-footer">
        <a href="https://wa.me/212691444558" class="cta-btn">اطلبي الآن عبر الواتساب</a>
    </div>

    <script>
        function toggleReviews() {
            var extra = document.getElementById("extraReviews");
            var btn = document.getElementById("showMore");
            if (extra.style.display === "block") {
                extra.style.display = "none";
                btn.innerHTML = "قراءة المزيد من الآراء";
            } else {
                extra.style.display = "block";
                btn.innerHTML = "إغلاق";
            }
        }

        function startTimer(duration, display) {
            var timer = duration, hours, minutes, seconds;
            setInterval(function () {
                hours = parseInt(timer / 3600, 10);
                minutes = parseInt((timer % 3600) / 60, 10);
                seconds = parseInt(timer % 60, 10);
                display.textContent = (hours<10?"0"+hours:hours)+":"+(minutes<10?"0"+minutes:minutes)+":"+(seconds<10?"0"+seconds:seconds);
                if (--timer < 0) timer = duration;
            }, 1000);
        }
        window.onload = function () { startTimer(60*60*5, document.querySelector('#timer')); };
    </script>
</body>
</html>
