<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VELORIA BEAUTY - العرض المتكامل</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { --main-pink: #fff5f6; --dark-pink: #f06292; --black: #1a1a1a; --green-wa: #25D366; }
        h1 { display: none !important; }
        * { box-sizing: border-box; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; background-color: #fff; text-align: center; line-height: 1.6; color: #333; }

        .brand-header { padding: 20px 0; background-color: #fff; display: flex; flex-direction: column; align-items: center; border-bottom: 1px solid #f8f8f8; }
        .brand-logo { width: 75px; height: auto; margin-bottom: 8px; border-radius: 50%; }
        .brand-name { font-size: 22px; font-weight: bold; color: var(--dark-pink); letter-spacing: 2px; }

        .promo-bar { background: var(--black); color: #fff; padding: 12px; font-weight: bold; width: 100%; font-size: 14px; }
        .timer-container { background: #fff3f3; padding: 15px; border-bottom: 2px solid #ffcdd2; }
        #timer { font-size: 28px; font-weight: bold; color: #d32f2f; }
        .exclusive-text { color: #d32f2f; font-weight: bold; margin-top: 5px; font-size: 14px; }

        .hero { padding: 20px; }
        .hero-img { width: 95%; max-width: 480px; border-radius: 15px; margin: 0 auto 20px; display: block; box-shadow: 0 4px 15px rgba(0,0,0,0.08); cursor: pointer; }

        .price-box { margin: 15px 0; }
        .new-price { font-size: 32px; color: #e91e63; font-weight: bold; }
        .badge { background: #ff5252; color: #fff; padding: 6px 15px; border-radius: 5px; font-size: 14px; display: inline-block; margin-top: 5px; font-weight: bold; }

        .lighting-grid { display: flex; gap: 10px; justify-content: center; padding: 0 10px; margin-top: 25px; }
        .light-item { flex: 1; min-width: 80px; max-width: 150px; cursor: pointer; }
        .light-item img { width: 100%; border-radius: 12px; border: 2px solid #fff; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .light-label { font-size: 11px; font-weight: bold; margin-top: 5px; color: var(--dark-pink); }

        .mirror-details { padding: 25px 15px; background: #fffafb; margin: 20px 20px; border-radius: 15px; border: 1px dashed var(--dark-pink); }
        .mirror-details h4 { color: var(--dark-pink); margin-top: 0; }
        .mirror-details ul { text-align: right; display: inline-block; padding: 0; margin: 0; list-style: none; }
        .mirror-details li { margin-bottom: 8px; font-size: 14px; }
        .mirror-details li::before { content: "✓ "; color: var(--dark-pink); font-weight: bold; }

        .modal { display: none; position: fixed; z-index: 20000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.95); justify-content: center; align-items: center; cursor: pointer; }
        .modal-content { max-width: 95%; max-height: 85%; border-radius: 10px; cursor: default; }

        .info-card { padding: 40px 15px; border-bottom: 1px solid #f0f0f0; }
        .info-card h3 { color: var(--dark-pink); margin-bottom: 15px; }

        .faq-section { padding: 40px 15px; background: #fff; text-align: right; }
        .faq-title { color: var(--dark-pink); margin-bottom: 25px; text-align: center; }
        .faq-item { border-bottom: 1px solid #eee; padding: 15px 0; }
        .faq-question { font-weight: bold; color: #333; cursor: pointer; display: flex; justify-content: space-between; align-items: center; }
        .faq-question::after { content: '+'; font-size: 20px; color: var(--dark-pink); }
        .faq-answer { display: none; padding-top: 10px; color: #666; font-size: 14px; }
        .extra-content { display: none; }

        .reviews-container { background: var(--main-pink); padding: 40px 15px; }
        .review-card { background: #fff; padding: 15px; border-radius: 15px; margin: 12px auto; width: 100%; max-width: 500px; text-align: right; display: flex; gap: 12px; box-shadow: 0 3px 10px rgba(0,0,0,0.04); }
        .profile-img { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; }
        .stars { color: #ffc107; font-size: 12px; }

        .btn-outline { background: #fff; border: 1.5px solid var(--dark-pink); color: var(--dark-pink); padding: 10px 25px; border-radius: 30px; cursor: pointer; margin: 20px 0; font-weight: bold; }
        .sticky-footer { position: fixed; bottom: 0; left: 0; width: 100%; background: #fff; padding: 15px 0; z-index: 10000; box-shadow: 0 -5px 20px rgba(0,0,0,0.1); display: flex; justify-content: center; }
        .cta-btn { background: var(--green-wa); color: #fff; width: 88%; max-width: 380px; padding: 18px; border-radius: 50px; text-decoration: none; font-weight: bold; font-size: 1.4rem; animation: pulse 2.5s infinite; text-align: center; }
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
        <p style="margin:0; font-weight: bold;">مدة الخصم تنتهي في:</p>
        <div id="timer">--:--:--</div>
        <div class="exclusive-text">خصم حصري على المجموعة كاملة</div>
    </div>

    <section class="hero">
        <img src="1.jpg" class="hero-img" alt="حقيبة الماكياج" onclick="openModal(this.src)">
        <div class="price-box">
            <span style="text-decoration: line-through; color: #999; font-size: 20px;">419 درهم</span><br>
            <span class="new-price">279 درهم فقط</span><br>
            <span class="badge">أطلبي الآن واستفيدي من عرض 50%-</span>
        </div>
    </section>

    <div class="info-card">
        <h3>مرآة ذكية احترافية 💡</h3>
        <div class="lighting-grid">
            <div class="light-item" onclick="openModal('light1.jpg')"><img src="light1.jpg"><div class="light-label">أبيض طبيعي</div></div>
            <div class="light-item" onclick="openModal('light2.jpg')"><img src="light2.jpg"><div class="light-label">أصفر دافئ</div></div>
            <div class="light-item" onclick="openModal('light3.jpg')"><img src="light3.jpg"><div class="light-label">أبيض ناصع</div></div>
        </div>

        <div class="mirror-details">
            <h4>تفاصيل ومميزات المرآة:</h4>
            <ul>
                <li><strong>إضاءة LED ذكية:</strong> 3 مستويات من الإضاءة كتحكمي فيها باللمس.</li>
                <li><strong>قابلة للفصل والشحن:</strong> تقدري تحيديها وتخدمي بها بوحدها، وكتشارجا بـ USB.</li>
                <li><strong>بطارية ليتيو قوية:</strong> كتدوم مدة طويلة بلا ما تحتاجي تشارجيها كل نهار.</li>
                <li><strong>وضوح عالي:</strong> زجاج نقي كيبين تفاصيل الماكياج بكل دقة.</li>
            </ul>
        </div>
    </div>

    <div id="myModal" class="modal" onclick="closeModal()">
        <img class="modal-content" id="img01" onclick="event.stopPropagation()">
    </div>

    <div class="info-card">
        <h3>نظمي مجوهراتك بكل أناقة 💍</h3>
        <img src="3.jpg" class="hero-img" alt="علبة المجوهرات" onclick="openModal(this.src)">
        <p>العلبة مصممة باش تحافظي على الخواتم والسلاسل ديالك من الضياع، ومصنوعة من مواد كتحميها من الخدوش.</p>
    </div>

    <section class="faq-section">
        <h2 class="faq-title">أسئلة كيسولوها البنات 🤔</h2>
        <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش بصح التوصيل فابور؟</div><div class="faq-answer">نعم أختي، التوصيل مجاني لجميع المدن المغربية والدفع حتى كتوصلك الأمانة.</div></div>
        <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">شحال كيبقى شحن المرآة؟</div><div class="faq-answer">البطارية قوية بزاف، تقدري تخدمي بها حتى لـ 10 أيام من الاستعمال العادي بشحنة وحدة.</div></div>
        <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">إلى وصلاتني ولقيت فيها شي مشكل؟</div><div class="faq-answer">عندنا ضمان الجودة! إلى كان أي عيب، كنبدلوها ليك فوراً أو كنرجعو ليك فلوسك.</div></div>
        <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش الحقيبة والعلبة كيجيو مجموعين؟</div><div class="faq-answer">نعم، العرض كيشمل الحقيبة الذكية + علبة المجوهرات + كابل الشحن بـ 279 درهم فقط.</div></div>
        <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش الحقيبة جلد؟</div><div class="faq-answer">نعم، المادة الخارجية من الجلد الاصطناعي الفاخر، ساهل في التنظيف وكيحمي المحتويات من الصدمات.</div></div>

        <div class="extra-content" id="extraFaq">
            <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">شحال كياخد التوصيل من وقت؟</div><div class="faq-answer">بين 24 و 48 ساعة كحد أقصى كيكون الطلب عندك.</div></div>
            <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش نقدر نغسل الحقيبة؟</div><div class="faq-answer">يفضل تمسحيها غير بقطعة قماش مبللة باش تحافظي على الجلد والدوائر الكهربائية ديال المرايا.</div></div>
            <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش المرايا فيها ألوان بزاف؟</div><div class="faq-answer">فيها 3 ديال الدرجات (أبيض طبيعي، أصفر دافئ، وأبيض ناصع) باش تختاري الإضاءة اللي كترتاحي فيها.</div></div>
            <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">واش العلبة د المجوهرات كتهز بزاف؟</div><div class="faq-answer">نعم، فيها بلايص مخصصين للخواتم والسلاسل والحلقات ومقسمة بذكاء.</div></div>
            <div class="faq-item"><div class="faq-question" onclick="toggleFaq(this)">كيفاش نطلب العرض؟</div><div class="faq-answer">كليكي على زر الواتساب التحت، صيفطي المعلومات ديالك وحنا نتواصلو معك نأكدو الطلبية.</div></div>
        </div>
        <button class="btn-outline" id="btnFaq" onclick="toggleMore('extraFaq', 'btnFaq', 'أسئلة')">إظهار المزيد من الأسئلة</button>
    </section>

    <section class="reviews-container">
        <h2>آراء البنات اللي جربوا المجموعة ⭐</h2>
        <div class="review-card">
            <img src="https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">نهيلة - الرباط</span><p style="font-size:14px; margin:5px 0;">المرايا واعرة والضوء فيها مجهد كيعاون فالمكياج. العلبة د المجوهرات نفعاتني بزاف في التنظيم!</p></div>
        </div>
        <div class="review-card">
            <img src="https://images.pexels.com/photos/718978/pexels-photo-718978.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">إلهام - كازا</span><p style="font-size:14px; margin:5px 0;">جودة طوب! الحقيبة كتهز بزاف والعلبة د الخواتم كيجيو فيها مستفين. شكراً فيلوريا.</p></div>
        </div>
        <div class="review-card">
            <img src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">سلمى - فاس</span><p style="font-size:14px; margin:5px 0;">أحسن باك خديت هاد العام، المرايا كتحيد وهادشي نفعني بزاف فالسفر. العلبة الصغيرة كلاس بزااف.</p></div>
        </div>

        <div class="extra-content" id="extraReviews">
            <div class="review-card">
                <img src="https://images.pexels.com/photos/1587009/pexels-photo-1587009.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">إيمان - طنجة</span><p style="font-size:14px; margin:5px 0;">السلعة واصلة كيفما فالصور تماماً. المرايا كتشارجا دغيا وكتصبر، والحقيبة الجلد ديالها رطب وزوين.</p></div>
            </div>
            <div class="review-card">
                <img src="https://images.pexels.com/photos/415829/pexels-photo-415829.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">مريم - مراكش</span><p style="font-size:14px; margin:5px 0;">بصراحة صدماتني الجودة! الحقيبة متينة وكتحمي الماكياج والمرايا فيها إضاءة بروفيسيونال.</p></div>
            </div>
            <div class="review-card">
                <img src="https://images.pexels.com/photos/1845208/pexels-photo-1845208.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">حنان - أكادير</span><p style="font-size:14px; margin:5px 0;">تعامل راقي وتوصيل سريع. الحقيبة والعلبة جاو مجموعين ومقادين، عجبوني بزاف كهدية.</p></div>
            </div>
            <div class="review-card">
                <img src="https://images.pexels.com/photos/774909/pexels-photo-774909.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
                <div style="flex:1;"><div class="stars">⭐⭐⭐⭐⭐</div><span style="font-weight:bold">كوثر - القنيطرة</span><p style="font-size:14px; margin:5px 0;">المرآة ذكية بزاف، نفعاتني حيت كنقدر نحيدها ونخدم بها برا الحقيبة. شكراً ليكم.</p></div>
            </div>
        </div>
        <button class="btn-outline" id="btnReviews" onclick="toggleMore('extraReviews', 'btnReviews', 'الآراء')">إظهار المزيد من الآراء</button>
    </section>

    <section class="final-proof">
        <h2>توصيل سريع ومضمون في أقل من 24 ساعة 🚀</h2>
        <img src="4.jpg" class="hero-img" alt="توصيل سريع" onclick="openModal(this.src)">
        <p>فيلوريا تضمن لك جودة عالية وتوصيل سريع لجميع مدن المغرب مع إمكانية فحص المنتوج قبل الدفع.</p>
    </section>

    <div class="spacer"></div>
    <div class="sticky-footer"><a href="https://wa.me/212691444558" class="cta-btn">اطلبي الآن عبر الواتساب</a></div>

    <script>
        function openModal(src) { document.getElementById("myModal").style.display = "flex"; document.getElementById("img01").src = src; }
        function closeModal() { document.getElementById("myModal").style.display = "none"; }
        function toggleFaq(element) { const answer = element.nextElementSibling; answer.style.display = (answer.style.display === "block") ? "none" : "block"; }
        
        function toggleMore(id, btnId, text) {
            var content = document.getElementById(id);
            var btn = document.getElementById(btnId);
            if (content.style.display === "block") {
                content.style.display = "none";
                btn.innerHTML = "إظهار المزيد من " + text;
            } else {
                content.style.display = "block";
                btn.innerHTML = "إغلاق";
            }
        }

        function startPersistentTimer() {
            var duration = 12 * 60 * 60;
            var now = Math.floor(Date.now() / 1000);
            var endTime = localStorage.getItem('v_timer_end');
            if (!endTime || now > endTime) { endTime = now + duration; localStorage.setItem('v_timer_end', endTime); }
            var display = document.querySelector('#timer');
            setInterval(function() {
                var currentNow = Math.floor(Date.now() / 1000);
                var distance = endTime - currentNow;
                if (distance < 0) { endTime = currentNow + duration; localStorage.setItem('v_timer_end', endTime); distance = duration; }
                var h = Math.floor(distance / 3600);
                var m = Math.floor((distance % 3600) / 60);
                var s = Math.floor(distance % 60);
                display.textContent = (h < 10 ? "0" + h : h) + ":" + (m < 10 ? "0" + m : m) + ":" + (s < 10 ? "0" + s : s);
            }, 1000);
        }
        window.onload = startPersistentTimer;
    </script>
</body>
</html>
