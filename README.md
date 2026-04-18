<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Official Luxury Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* [نفس الـ CSS السابق بدون أي تغيير] */
        * { margin: 0; padding: 0; box-sizing: border-box; outline: none !important; border: none !important; text-decoration: none !important; background: none !important; -webkit-tap-highlight-color: transparent; }
        html, body { width: 100%; background-color: #000 !important; scroll-snap-type: y mandatory; scroll-behavior: smooth; font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden; }
        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 10px; color: #fff !important; pointer-events: none; }
        .scroll-trigger { position: fixed; top: 75%; right: 25px; transform: translateY(-50%); width: 40px; height: 40px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; }
        .arrow-icon { width: 20px; height: 20px; border-right: 3px solid var(--current-arrow-color, #fff) !important; border-bottom: 3px solid var(--current-arrow-color, #fff) !important; transform: rotate(45deg); animation: bounce 2s infinite; transition: 0.5s ease; }
        .arrow-up { transform: rotate(-135deg) !important; }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }
        @keyframes bounce-up { 0%, 100% { transform: translateY(5px) rotate(-135deg); } 50% { transform: translateY(-5px) rotate(-135deg); } }
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        .glow-center { position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); width: 600px; height: 600px; background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 75%) !important; opacity: 0.3; z-index: 0; pointer-events: none; }
        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }
        .bottle-center { text-align: center; padding: 40px 0; position: relative; z-index: 2; }
        .img-bottle { width: 32%; max-width: 130px; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff !important; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }
        .text-glow-free { position: relative; z-index: 2; padding: 25px; background: radial-gradient(ellipse at center, var(--glow-color) 0%, rgba(0,0,0,0) 85%) !important; }
        .row { display: flex; align-items: center; width: 100%; padding: 50px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 4px; display: block; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        .txt-box { width: 55%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.5rem; margin-bottom: 20px; color: var(--color) !important; letter-spacing: 2px; }
        .txt-box p { font-size: 0.95rem; line-height: 1.9; color: #f0f0f0 !important; font-weight: 300; margin-bottom: 12px; }
        .highlight { color: var(--color) !important; font-weight: 600; font-size: 0.85rem; margin-right: 5px; }
        .purchase-area { max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 40px; border-top: 1px solid rgba(255,255,255,0.1) !important; border-bottom: 1px solid rgba(255,255,255,0.1) !important; width: 90%; position: relative; z-index: 2; }
        .mini-thumb { width: 100px; height: 100px; object-fit: cover; }
        .size-container { display: flex; gap: 15px; margin-top: 15px; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2) !important; text-align: center; cursor: pointer; color: #fff; }
        .size-box span { display: block; font-size: 9px; color: #888; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05) !important; }
        input { width: 100%; padding: 18px 0; margin-bottom: 15px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.3) !important; font-family: 'Montserrat'; }
        .order-btn { width: 100%; padding: 22px; background-color: #fff !important; color: #000 !important; font-weight: 800; cursor: pointer; letter-spacing: 4px; }
        @media (max-width: 900px) { .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; } .img-box, .txt-box { width: 100%; } .purchase-area { flex-direction: column-reverse; padding: 25px; } }
        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.35); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.35); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.35); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.35); }
        /* هاد الكود كيخفي الرابط تماماً وما كيخليش بلاصتو خاوية */
a[href*="veloriabeauty.github.io"] {
    display: none !important;
    visibility: hidden !important;
}
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="sauvage-bottle.png" id="perfume-img" alt="Sauvage">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-detail-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>THE LEGENDARY DEPTH</h3>
                <p>Sauvage Elixir is an extraordinary concentration, a masterpiece of wild freshness. It intoxicates the senses with a custom-made heart of spices and a rich, woody trail that lingers long after you leave the room.</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-detail-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>OFFICIAL COMPOSITION</h3>
                <p><span class="highlight">Notes:</span> A powerful blend of Nutmeg, Cinnamon, and Cardamom, balanced perfectly by the freshness of Grapefruit and the warmth of Licorice.</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">SAUVAGE ELIXIR</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/sauvage-thumb.png" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec1', 'SAUVAGE ELIXIR')">ORDER NOW | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-detail-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>MAGNETIC SENSUALITY</h3>
                <p>Stronger With You lives in the present, molded by the energy of modernity. Unpredictable, it surprises with its originality, like the spicy accord in the top notes—a mix of cardamom, pink peppercorn, and violet leaves.</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-detail-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>OLFACTORY ARCHITECTURE</h3>
                <p><span class="highlight">Heart:</span> The aromatic heart consists of Sage and Lavender, bringing a confident elegance with the easy insouciance of youth, followed by a base of smoky Vanilla Jungle Essence.</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">STRONGER WITH YOU</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/stronger-thumb.png" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec2')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec2')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec2', 'STRONGER WITH YOU')">ORDER NOW | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE INTENSE</h1>
            <div class="perfume-sub">EAU DE PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-detail-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>BORN TO BE WILD</h3>
                <p>The iconic structure of Libre, intensified. A burning floral duality, where the tension between French lavender and Moroccan orange blossom becomes even more excessive, enveloped in a creamy orchid accord.</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-detail-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>THE RAW ELEMENTS</h3>
                <p><span class="highlight">Base:</span> Madagascar Vanilla and Tonka Bean provide a dark, smoky depth that contrasts beautifully with the bright citrus top notes, creating a trail that is both fierce and feminine.</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">LIBRE INTENSE</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/libre-thumb.png" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec3')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec3')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec3', 'LIBRE INTENSE')">ORDER NOW | 319 DH</button></form></div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>IT'S SO GOOD TO BE BAD</h3>
                <p>Inspired by the duality of the modern woman: audacious and sexy, elegant and enigmatic. Good Girl represents the complex vibrant world of femininity through a bold mix of dark and light elements.</p>
            </div></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box"><div class="text-glow-free">
                <h3>OLFACTORY NOTES</h3>
                <p><span class="highlight">Heart:</span> The sweet qualities of Jasmine and Tuberose give the fragrance its brightness, while Roasted Tonka Bean and Cocoa provide the mysterious dark side that lasts all night.</p>
            </div></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:15px">
                    <div><h4 style="font-family:'Cinzel'">GOOD GIRL</h4><p style="color:#666; font-size:10px">10ML / 319 DH</p></div>
                    <img src="assets/gg-thumb.png" class="mini-thumb">
                </div>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec4')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec4')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec4', 'GOOD GIRL')">ORDER NOW | 319 DH</button></form></div>
        </div>
    </section>

    <script>
        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerText = `ORDER NOW | ${price} DH`;
        }

        function sendOrder(sectionId, productName) {
            const section = document.getElementById(sectionId);
            const name = section.querySelector('input[name="name"]').value;
            const phone = section.querySelector('input[name="phone"]').value;
            const city = section.querySelector('input[name="city"]').value;
            const size = section.querySelector('.active-size').innerText.split('\n')[0];
            const price = section.querySelector('.order-btn').innerText.split('|')[1].trim();

            if(!name || !phone || !city) {
                alert("عافاك عمر المعلومات كاملة");
                return;
            }

            const botToken = "8751066528:AAFJOYkbqi3bSxncJh4tKSQeH_0wCT660ps";
            const chatId = "7635707772"; 
            
            const message = `🚀 *طلب جديد: Velooria Beauty*\n\n` +
                            `📦 *المنتوج:* ${productName}\n` +
                            `📏 *القياس:* ${size}\n` +
                            `💰 *الثمن:* ${price}\n` +
                            `--------------------------\n` +
                            `👤 *الاسم:* ${name}\n` +
                            `📞 *الهاتف:* ${phone}\n` +
                            `📍 *المدينة:* ${city}\n\n` +
                            `✅ يونس، كليان جديد كيتسناك!`;

            fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ chat_id: chatId, text: message, parse_mode: 'Markdown' })
            })
            .then(res => {
                alert("شكراً! تم إرسال طلبك بنجاح.");
                section.querySelector('form').reset();
            })
            .catch(err => alert("وقع مشكل فالاتصال، حاول مرة أخرى."));
        }

        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        const colors = ['#4A90E2', '#CD7F32', '#D4AF37', '#1a4d99'];
        let currentIdx = 0;
        const scrollBtn = document.getElementById('scrollBtn');
        const arrow = scrollBtn.querySelector('.arrow-icon');

        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -window.innerHeight/2 && rect.top <= window.innerHeight/2) {
                    currentIdx = index;
                    document.documentElement.style.setProperty('--current-arrow-color', colors[index]);
                    if(currentIdx === sections.length - 1) {
                        arrow.classList.add('arrow-up');
                        arrow.style.animation = "bounce-up 2s infinite";
                    } else {
                        arrow.classList.remove('arrow-up');
                        arrow.style.animation = "bounce 2s infinite";
                    }
                }
            });
        });

        scrollBtn.onclick = () => {
            if(currentIdx === sections.length - 1) {
                window.scrollTo({ top: 0, behavior: 'smooth' });
            } else {
                document.getElementById(sections[currentIdx + 1]).scrollIntoView({ behavior: 'smooth' });
            }
        };
  
    </script>
<style>
  #interactive-cat {
    position: fixed;
    width: 110px; /* حجم القط */
    z-index: 9999;
    cursor: pointer;
    /* السر فـ هاد السطر هو اللي كيعطي القفزة الانسيابية */
    transition: all 1.2s cubic-bezier(0.68, -0.55, 0.27, 1.55);
    bottom: 50px;
    right: 50px;
    pointer-events: auto;
  }
  
  /* تأثير "الخدش" ملي يوقف فوق العطر */
  @keyframes scratch {
    0% { transform: rotate(0); }
    25% { transform: rotate(-10deg) scale(1.05); }
    75% { transform: rotate(10deg) scale(1.05); }
    100% { transform: rotate(0); }
  }
  .attacking { animation: scratch 0.3s infinite; }
</style>

<img src="assets/cat.gif" id="interactive-cat" alt="Veloria Cat">

<style>
  #interactive-cat {
    position: fixed;
    width: 100px;
    z-index: 9999;
    cursor: pointer;
    /* حيدنا الـ transition العادي باش نتحكمو بالفيزياء يدويًا */
    pointer-events: auto;
    transform-origin: bottom center;
  }
</style>

<img src="assets/cat.gif" id="interactive-cat" alt="Veloria Cat">

<script>
  const cat = document.getElementById('interactive-cat');
  const perfume = document.getElementById('perfume-img');

  let posX = window.innerWidth - 150;
  let posY = window.innerHeight - 150;
  let vx = 0; // السرعة الأفقية
  let vy = 0; // السرعة العمودية
  let gravity = 0.8; // قوة الجاذبية
  let friction = 0.9; // الاحتكاك (باش يوقف مابقاش يزلق)
  let targetX = posX;
  let targetY = posY;

  function updatePhysics() {
    // تطبيق الجاذبية
    vy += gravity;
    
    // تحريك القط بناءً على السرعة
    posX += vx;
    posY += vy;

    // حواف الشاشة (الأرضية)
    if (posY > window.innerHeight - 110) {
      posY = window.innerHeight - 110;
      vy *= -0.3; // ارتداد خفيف ملي كيقيس الأرض
      vx *= friction;
    }

    // حواف الشاشة (الجوانب)
    if (posX > window.innerWidth - 100) posX = window.innerWidth - 100;
    if (posX < 0) posX = 0;

    // تطبيق المواقع على العنصر
    cat.style.left = posX + 'px';
    cat.style.top = posY + 'px';

    // دوران خفيف حسب السرعة (باش يبان واقعي)
    cat.style.transform = `rotate(${vx * 2}deg)`;

    requestAnimationFrame(updatePhysics);
  }

  // دالة القفز نحو الهدف (العطر أو مكان عشوائي)
  function jumpTo(targetX, targetY) {
    const dx = targetX - posX;
    const dy = targetY - posY;
    
    // حساب القوة المحتاجة للقفزة
    vx = dx * 0.05;
    vy = -Math.sqrt(Math.abs(dy) * 2) - 5; // قفزة للأعلى
  }

  // ذكاء القط: يقرر فين ينقز
  setInterval(() => {
    const rand = Math.random();
    if (rand < 0.5 && perfume) {
      const rect = perfume.getBoundingClientRect();
      jumpTo(rect.left, rect.top - 50);
    } else {
      jumpTo(Math.random() * window.innerWidth, window.innerHeight - 150);
    }
  }, 5000);

  // الهروب عند لمس الماوس
  cat.addEventListener('mouseenter', () => {
    vx = (Math.random() - 0.5) * 40; // هربة سريعة للجنب
    vy = -20; // قفزة عالية ديال الخلعة
  });

  // البدء
  updatePhysics();
</script>
  const cat = document.getElementById('interactive-cat');
  const perfume = document.getElementById('perfume-img');
  const allTexts = document.querySelectorAll('p, h1, h2'); // كاع الكلمات اللي فالسيت

  function catAction() {
    // اختار حركة عشوائية: يا إما يمشي للعطر، يا إما لشي كلمة، يا إما بلاصة عشوائية
    const rand = Math.random();

    if (rand < 0.4 && perfume) {
        // هجوم على العطر
        const rect = perfume.getBoundingClientRect();
        cat.style.left = (rect.left + Math.random() * 50) + 'px';
        cat.style.top = (rect.top - 40) + 'px';
        cat.classList.add('attacking');
        setTimeout(() => cat.classList.remove('attacking'), 2000);

    } else if (rand < 0.7 && allTexts.length > 0) {
        // ينقز فوق شي كلمة عشوائية فالسيت
        const randomText = allTexts[Math.floor(Math.random() * allTexts.length)];
        const rect = randomText.getBoundingClientRect();
        cat.style.left = rect.left + 'px';
        cat.style.top = (rect.top - 50) + 'px';

    } else {
        // حركة عشوائية حرة
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        cat.style.left = x + 'px';
        cat.style.top = y + 'px';
    }
  }

  // تنفيذ الحركة كل 4 ثواني (باش يبان نشيط)
  setInterval(catAction, 4000);

  // الهروب السريع ملي يقرب ليه الفار (الماوس)
  cat.addEventListener('mouseover', () => {
    cat.style.transition = "all 0.4s ease-out"; // هروب سريع
    cat.style.left = Math.random() * (window.innerWidth - 100) + 'px';
    cat.style.top = Math.random() * (window.innerHeight - 100) + 'px';
    
    // يرجع للحركة المنظمة بعد الهروب
    setTimeout(() => { cat.style.transition = "all 1.2s cubic-bezier(0.68, -0.55, 0.27, 1.55)"; }, 500);
  });
</script>
  const cat = document.getElementById('interactive-cat');
  // هنا خاصك تآكد بلي صورة العطر عندها id="perfume-img"
  const perfume = document.getElementById('perfume-img') || document.querySelector('img');

  // حركة عشوائية
  function moveCat() {
    if (cat.classList.contains('scared')) return;
    const x = Math.random() * (window.innerWidth - 150);
    const y = Math.random() * (window.innerHeight - 150);
    cat.style.left = x + 'px';
    cat.style.top = y + 'px';
  }

  // القط كيهجم على العطر كل 12 ثانية
  setInterval(() => {
    if (perfume && !cat.classList.contains('scared')) {
      const rect = perfume.getBoundingClientRect();
      cat.style.left = (rect.left + 20) + 'px';
      cat.style.top = (rect.top + 20) + 'px';
    }
  }, 12000);

  // القط كيهرب ملي تكليكي عليه
  cat.addEventListener('click', () => {
    cat.classList.add('scared');
    if (perfume) {
      const rect = perfume.getBoundingClientRect();
      cat.style.left = rect.left + 'px';
      cat.style.top = rect.top + 'px';
    }
    setTimeout(() => {
      cat.classList.remove('scared');
      moveCat();
    }, 3000);
  });

  setInterval(moveCat, 6000);
</script>
</body>
</html>
