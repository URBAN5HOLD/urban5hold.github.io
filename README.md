<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VELORIA BEAUTY - العرض المتكامل</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --main-pink: #fff5f6;
            --dark-pink: #f06292;
            --black: #1a1a1a;
            --green-wa: #25D366;
        }

        * { box-sizing: border-box; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; background-color: #fff; text-align: center; line-height: 1.6; color: #333; }

        .brand-header {
            padding: 20px 0;
            background-color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            border-bottom: 1px solid #f8f8f8;
        }
        .brand-logo { width: 75px; height: auto; margin-bottom: 8px; border-radius: 50%; }
        .brand-name { font-size: 22px; font-weight: bold; color: var(--dark-pink); letter-spacing: 2px; }

        .promo-bar { background: var(--black); color: #fff; padding: 12px; font-weight: bold; width: 100%; font-size: 14px; }
        
        .timer-container { background: #fff3f3; padding: 15px; border-bottom: 2px solid #ffcdd2; }
        #timer { font-size: 28px; font-weight: bold; color: #d32f2f; }

        .hero { padding: 20px; }
        h1 { color: var(--dark-pink); font-size: 1.6rem; margin-bottom: 15px; padding: 0 10px; }
        .hero-img { width: 95%; max-width: 480px; border-radius: 15px; margin: 0 auto 20px; display: block; box-shadow: 0 4px 15px rgba(0,0,0,0.08); }

        .price-box { margin: 15px 0; }
        .new-price { font-size: 32px; color: #e91e63; font-weight: bold; }
        .badge { background: #ff5252; color: #fff; padding: 6px 15px; border-radius: 5px; font-size: 14px; display: inline-block; margin-top: 5px; font-weight: bold; }

        .info-card { padding: 40px 15px; border-bottom: 1px solid #f0f0f0; }
        .info-card h3 { color: var(--dark-pink); margin-bottom: 15px; font-size: 1.3rem; }
        .info-card p { font-size: 1.1rem; color: #555; max-width: 550px; margin: 0 auto; padding: 0 15px; }

        .reviews-container { background: var(--main-pink); padding: 40px 15px; }
        .review-card {
            background: #fff; padding: 15px; border-radius: 15px; margin: 12px auto;
            width: 100%; max-width: 500px; text-align: right; display: flex; gap: 12px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.04);
        }
        .extra-reviews { display: none; }
        .profile-img { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; background: #eee; }
        .stars { color: #ffc107; font-size: 12px; margin-bottom: 4px; }
        .review-name { font-weight: bold; font-size: 15px; color: #222; }

        .show-more-btn {
            background: #fff; border: 1.5px solid var(--dark-pink); color: var(--dark-pink);
            padding: 12px 30px; border-radius: 30px; cursor: pointer; margin: 25px 0; font-weight: bold;
        }

        .final-proof { padding: 50px 15px; background: #fff; }

        .sticky-footer { 
            position: fixed; bottom: 0; left: 0; width: 100%; background: #fff; 
            padding: 15px 0; z-index: 10000; box-shadow: 0 -5px 20px rgba(0,0,0,0.1);
            display: flex; justify-content: center;
        }
        .cta-btn { 
            background: var(--green-wa); color: #fff; width: 88%; max-width: 380px; 
            padding: 18px; border-radius: 50px; text-decoration: none; font-weight: bold; 
            font-size: 1.4rem; display: block; margin: 0 auto; animation: pulse 2.5s infinite; 
        }

        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.04); } 100% { transform: scale(1); } }
        .spacer { height: 120px; }
    </style>
</head>
<body>

    <header class="brand-header">
        <img src="logo.png" alt="Veloria Logo" class="brand-logo">
        <span class="brand-name">VELORIA BEAUTY</span>
    </header>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0; font-weight: bold;">مدة الخصم 50% تنتهي في:</p>
        <div id="timer">12:00:00</div>
    </div>

    <section class="hero">
        <h1>عرض الأناقة: حقيبة الماكياج الذكية + علبة المجوهرات ✨</h1>
        <img src="1.jpg" class="hero-img" alt="حقيبة الماكياج">
        <div class="price-box">
            <span style="text-decoration: line-through; color: #999; font-size: 20px;">538 درهم</span><br>
            <span class="new-price">269 درهم فقط</span><br>
            <span class="badge">خصم حصري -50% على الحقيبة والعلبة معاً</span>
        </div>
    </section>

    <div class="info-card">
        <h3>مرآة ذكية بـ 3 مستويات إضاءة 💡</h3>
        <img src="2.jpg" class="hero-img" alt="مرآة ليد">
        <p>تمتعي بإضاءة احترافية أينما كنتِ! حقيبة فيلوريا مزودة بمرآة LED تعمل باللمس، بـ 3 ألوان (أبيض، دافئ، وطبيعي). المرآة قابلة لإعادة الشحن (USB) ويمكن فصلها عن الحقيبة تماماً لاستعمالها بشكل مستقل.</p>
    </div>

    <div class="info-card">
        <h3>تنظيم مثالي لمجوهراتك 💍</h3>
        <img src="3.jpg" class="hero-img" alt="علبة المجوهرات">
        <p>علبة مجوهرات أنيقة مقسمة بذكاء لتنظيم الخواتم، السلاسل، والحلقات. حجم مثالي يوضع داخل الحقيبة أو يستعمل بشكل منفصل في السفر.</p>
    </div>

    <section class="reviews-container">
        <h2>شنو قالو البنات على المجموعة ديالنا؟ ⭐</h2>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">نهيلة - الرباط</span>
                <p style="font-size:14px; margin:5px 0; color: #444;">أحسن حاجة فهاد الحقيبة هي ديك المرايا! الإضاءة ديالها واعرة بزااف، والدرجات بـ3 كايخليوك تقادي الماكياج بدقة ❤️</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/718978/pexels-photo-718978.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">إلهام - الدار البيضاء</span>
                <p style="font-size:14px; margin:5px 0; color: #444;">عجبني بزااف أن المرايا كتحيد وكتشارجا بـ USB. الحقيبة والعلبة ديال الجواهر جاو طوب وكيبانو كلاس 👍</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">سلمى - فاس</span>
                <p style="font-size:14px; margin:5px 0; color: #444;">المرايا ليد اللي فيها بـ Touch كتحمق، والضوء الساطع كيبين كاع التفاصيل. الحقيبة واسعة كتهز كولشي ✨</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://images.pexels.com/photos/1587009/pexels-photo-1587009.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;">
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">إيمان - طنجة</span>
                <p style="font-size:14px; margin:5px 0; color: #444;">السلعة واصلة كيفما فالصور. الحقيبة جاتني كبر شوية من داكشي لي تخيلت وهذا رباح، والجودة خلاتني مماندماناش 👌</p>
            </div>
        </div>

        <div class="extra-reviews" id="extraReviews">
            <div class="review-card">
                <img src="https://images.pexels.com/photos/1239291/pexels-photo-1239291.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div style="flex:1;">
                    <div class="stars">⭐⭐⭐⭐⭐</div><span class="review-name">مريم - طنجة</span>
                    <p style="font-size:14px; margin:5px 0; color: #444;">صدماتني الجودة ديال المرايا والإضاءة ديالها. أحسن كادو تقدري تعطيه لشي عروسة أو لراسك!</p>
                </div>
            </div>
        </div>

        <button class="show-more-btn" id="showMore" onclick="toggleReviews()">قراءة المزيد من الآراء</button>
    </section>

    <section class="final-proof">
        <h2>توصيل سريع ومضمون في أقل من 24 ساعة 🚀</h2>
        <img src="4.jpg" class="hero-img" alt="توصيل سريع">
        <p>فيلوريا تضمن لك وصول طلبيتك في وقت قياسي وبجودة عالية في جميع أنحاء المغرب.</p>
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
        window.onload = function () { startTimer(60*60*12, document.querySelector('#timer')); };
    </script>
</body>
</html>
