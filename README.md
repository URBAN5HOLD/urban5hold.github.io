<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Premium Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --bg: #000; }
        html, body { 
            width: 100%; margin: 0; padding: 0;
            overflow-x: hidden; background-color: var(--bg);
            scroll-snap-type: y mandatory; scroll-behavior: smooth;
        }
        * { box-sizing: border-box; outline: none; -webkit-tap-highlight-color: transparent; }

        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 8px; color: #fff; }

        /* سهم السكرول - طالع بـ 10% */
        .scroll-trigger {
            position: fixed; bottom: 15%; right: 25px; 
            width: 50px; height: 50px; z-index: 2000;
            cursor: pointer; display: flex; align-items: center; justify-content: center;
        }
        .arrow-icon {
            width: 20px; height: 20px;
            border-right: 2.5px solid var(--current-color);
            border-bottom: 2.5px solid var(--current-color);
            transform: rotate(45deg);
            animation: bounce 2s infinite;
        }
        @keyframes bounce { 0%, 100% { transform: rotate(45deg) translate(0,0); } 50% { transform: rotate(45deg) translate(5px,5px); } }

        .product-section { 
            width: 100%; min-height: 100vh; scroll-snap-align: start; 
            scroll-snap-stop: always; position: relative; padding-bottom: 80px;
        }

        /* تضييق فيديو Sauvage */
        .v-header-sauvage { width: 85%; margin: 0 auto; line-height: 0; }
        .v-header { width: 100%; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 30px 0; }
        .img-bottle { width: 40%; max-width: 160px; margin: 0 auto; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; }

        .row { display: flex; align-items: center; width: 100%; padding: 25px 8%; gap: 25px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; }
        .img-box img { width: 100%; border-radius: 2px; }
        
        .txt-box { width: 50%; color: #fff; }
        h3 { font-family: 'Cinzel', serif; font-size: 1.3rem; margin-bottom: 10px; color: var(--color); }
        p { font-size: 0.85rem; line-height: 1.6; color: #ccc; font-weight: 300; }

        .purchase-area { max-width: 1000px; margin: 40px auto; display: flex; gap: 30px; padding: 30px; border-top: 1px solid rgba(255,255,255,0.05); width: 90%; }
        .mini-thumb { width: 80px; height: 80px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1); }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.1); text-align: center; color: #fff; }
        .active-size { border-color: var(--color); color: var(--color); background: rgba(255,255,255,0.02); }

        input { width: 100%; padding: 15px 5px; margin-bottom: 15px; background: transparent; color: #fff; border: none; border-bottom: 1px solid rgba(255,255,255,0.15); font-family: 'Montserrat'; }
        .order-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-family: 'Montserrat'; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 2px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 20px 8%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; }
            .v-header-sauvage { width: 100%; }
        }

        .sauv-t { --color: #4A90E2; --current-color: #4A90E2; }
        .stron-t { --color: #CD7F32; --current-color: #CD7F32; }
        .libre-t { --color: #D4AF37; --current-color: #D4AF37; }
        .gg-t { --color: #1a4d99; --current-color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="v-header-sauvage"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE</h1>
            <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box"><h3>The Top Notes</h3><p>A spicy blast of Grapefruit, Cinnamon, Nutmeg, and Cardamom for an immediate magnetic impact.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box"><h3>The Base</h3><p>Rich Licorice, Sandalwood, and Amber create a powerful, long-lasting trail that stays for 12+ hours.</p></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">DECANT 10ML</h4><p style="color:#555; font-size:10px">HIGH CONCENTRATION</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box"><h3>The Accord</h3><p>A new Rum accord combined with Bergamot, creating a masculine intensity that is both bold and sweet.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box"><h3>The Signature</h3><p>The iconic Smoky Chestnut and Madagascar Vanilla notes deliver an addictive, magnetic attraction.</p></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">INTENSE 10ML</h4><p style="color:#555; font-size:10px">MAGNETIC SCENT</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box"><h3>The Duality</h3><p>French Lavender meets Moroccan Orange Blossom for a unique floral tension that defines freedom.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box"><h3>The Base</h3><p>Grown in Madagascar, the Vanilla extract provides a creamy, couture finish that lasts all day.</p></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">LIBRE 10ML</h4><p style="color:#555; font-size:10px">COUTURE FLOWERS</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box"><h3>Bright & Bold</h3><p>The sweet, alluring qualities of Jasmine and Almond give Good Girl its bright and feminine side.</p></div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box"><h3>Dark & Moody</h3><p>Richly fragrant Cocoa and Tonka Bean express the mysterious and seductive side of the fragrance.</p></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">GOOD GIRL 10ML</h4><p style="color:#555; font-size:10px">POWERFUL SEDUCTION</p></div>
                    <img src="assets/gg-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <script>
        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        let currentIdx = 0;
        const btn = document.getElementById('scrollBtn');
        btn.onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView();
        };
        window.onscroll = () => {
            const scrollPos = window.scrollY + window.innerHeight / 2;
            sections.forEach((id, index) => {
                const el = document.getElementById(id);
                if (scrollPos >= el.offsetTop && scrollPos < el.offsetTop + el.offsetHeight) {
                    const color = getComputedStyle(el).getPropertyValue('--color');
                    document.documentElement.style.setProperty('--current-color', color);
                    currentIdx = index;
                }
            });
        };
    </script>
</body>
</html>
