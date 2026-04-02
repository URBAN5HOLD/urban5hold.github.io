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

        .promo-bar { background: var(--black); color: #fff; padding: 12px; font-weight: bold; width: 100%; }
        .timer-container { background: #fff3f3; padding: 15px; border-bottom: 2px solid #ffcdd2; }
        #timer { font-size: 28px; font-weight: bold; color: #d32f2f; }

        .hero { padding: 20px; }
        h1 { color: var(--dark-pink); font-size: 1.7rem; }
        .hero-img { width: 95%; max-width: 500px; border-radius: 15px; margin-bottom: 20px; }

        /* الأثمنة */
        .price-box { margin: 15px 0; }
        .new-price { font-size: 30px; color: #e91e63; font-weight: bold; }
        .badge { background: #ff5252; color: #fff; padding: 5px 10px; border-radius: 4px; font-size: 14px; }

        /* قسم 3 صور مع مساحة كبيرة للشرح */
        .info-card { padding: 40px 15px; border-bottom: 1px solid #eee; }
        .info-card img { width: 95%; max-width: 480px; border-radius: 10px; margin-bottom: 20px; }
        .info-card p { font-size: 1.2rem; color: #444; padding: 10px 20px; min-height: 80px; }

        /* قسم التعاليق */
        .reviews-container { background: var(--main-pink); padding: 40px 15px; }
        .review-card {
            background: #fff; padding: 15px; border-radius: 12px; margin: 10px auto;
            width: 100%; max-width: 500px; text-align: right; display: flex; gap: 12px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        /* إخفاء التعاليق الزائدة */
        .extra-reviews { display: none; }
        
        .profile-img { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; background: #ddd; }
        .stars { color: #ffc107; font-size: 12px; }
        .review-name { font-weight: bold; font-size: 15px; }

        /* زر قراءة المزيد */
        .show-more-btn {
            background: #fff; border: 1px solid var(--dark-pink); color: var(--dark-pink);
            padding: 10px 25px; border-radius: 25px; cursor: pointer; margin: 20px 0; font-weight: bold;
        }

        /* الصورة الرابعة في الأخير */
        .final-proof { padding: 40px 15px; background: #fff; }

        .sticky-footer { position: fixed; bottom: 0; width: 100%; background: #fff; padding: 15px; z-index: 9999; display: flex; justify-content: center; }
        .cta-btn { background: var(--green-wa); color: #fff; width: 90%; max-width: 400px; padding: 16px; border-radius: 50px; text-decoration: none; font-weight: bold; font-size: 1.3rem; animation: pulse 2.5s infinite; }

        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.05); } 100% { transform: scale(1); } }
        .spacer { height: 100px; }
    </style>
</head>
<body>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0;">ينتهي الخصم خلال:</p>
        <div id="timer">05:00:00</div>
    </div>

    <section class="hero">
        <h1>احصلي على شعر حريري في دقائق ✨</h1>
        <img src="https://via.placeholder.com/600x600" class="hero-img">
        <div class="price-box">
            <span class="new-price">249 درهم</span> <span class="badge">تخفيض 50%-</span>
        </div>
    </section>

    <div class="info-card">
        <img src="https://via.placeholder.com/500x500" alt="صورة 1">
        <p>هنا اكتبي شرح مفصل للميزة الأولى.. (مثلا: كيفاش المشط كيحمي الزغبة من التقصف بفضل تقنية السيراميك)</p>
    </div>

    <div class="info-card">
        <img src="https://via.placeholder.com/500x500" alt="صورة 2">
        <p>هنا اكتبي شرح مفصل للميزة الثانية.. (مثلا: السرعة في التسخين والنتيجة اللي كتدوم لعدة أيام)</p>
    </div>

    <div class="info-card">
        <img src="https://via.placeholder.com/500x500" alt="صورة 3">
        <p>هنا اكتبي شرح مفصل للميزة الثالثة.. (مثلا: سهولة الحمل والاستخدام في السفر والمناسبات الزربانة)</p>
    </div>

    <section class="reviews-container">
        <h2>شنو قالو البنات على المنتج ديالنا؟ ⭐</h2>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">سناء - الدار البيضاء</span>
                <p style="font-size:14px; margin:5px 0;">بصراحة واعر بزااااف، هناني من السيشوار. كيسرح دغيا ❤️</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/718978/pexels-photo-718978.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">ليلى</span>
                <p style="font-size:14px; margin:5px 0;">وصلني اليوم، السلعة جودة عالية برافو 👍</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">مريم</span>
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
        <h2>صور حقيقية لطلبيات زبوناتنا 📸</h2>
        <img src="https://via.placeholder.com/500x500" class="hero-img">
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

        // Timer Script
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
