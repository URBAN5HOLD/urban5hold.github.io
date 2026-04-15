<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | The Art of Fragrance</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --gold: #D4AF37; --bg: #000; }
        
        html, body { 
            width: 100%; margin: 0; padding: 0;
            overflow-x: hidden; background-color: var(--bg);
            scroll-snap-type: y mandatory; scroll-behavior: smooth;
            font-family: 'Montserrat', sans-serif;
        }

        * { box-sizing: border-box; -webkit-font-smoothing: antialiased; }

        .logo-fixed { 
            position: fixed; top: 20px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.3rem; 
            letter-spacing: 10px; color: #fff; text-shadow: 0 0 20px rgba(0,0,0,1);
        }

        .product-section { 
            width: 100%; min-height: 100vh; scroll-snap-align: start; 
            scroll-snap-stop: always; position: relative; display: flex; 
            flex-direction: column; overflow: hidden;
        }

        .v-header { width: 100%; line-height: 0; background: #000; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 60px 0 20px; }
        .img-bottle { width: 40%; max-width: 160px; margin: 0 auto; transition: 0.5s; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.5rem; color: #fff; letter-spacing: 8px; margin-top: 15px; }
        .perfume-sub { font-size: 0.8rem; color: var(--color); letter-spacing: 5px; text-transform: uppercase; font-weight: 200; }

        .row { display: flex; align-items: center; width: 100%; padding: 40px 8%; gap: 40px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; position: relative; }
        .img-box img { width: 100%; border-radius: 2px; filter: grayscale(20%); transition: 0.5s; }
        .img-box img:hover { filter: grayscale(0%); }
        
        .txt-box { width: 50%; color: #fff; position: relative; }
        .glow { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 160%; height: 160%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.2; z-index: -1; }

        h3 { font-family: 'Cinzel', serif; font-size: 1.6rem; margin-bottom: 20px; color: var(--color); border-bottom: 1px solid rgba(255,255,255,0.1); padding-bottom: 10px; }
        p { font-size: 0.95rem; line-height: 1.8; color: #ccc; font-weight: 300; margin-bottom: 15px; }
        b { color: #fff; font-weight: 600; }

        .perf-data { background: rgba(255,255,255,0.03); padding: 15px; border-left: 2px solid var(--color); font-size: 0.85rem; margin-top: 20px; }

        /* سهم السكرول العصري */
        .scroll-down {
            position: absolute; bottom: 30px; left: 50%; transform: translateX(-50%);
            cursor: pointer; z-index: 10; display: flex; flex-direction: column; align-items: center;
        }
        .scroll-down span {
            width: 1px; height: 60px; background: linear-gradient(to bottom, transparent, var(--color));
            animation: grow 2s infinite;
        }
        @keyframes grow { 
            0% { height: 0; opacity: 0; } 
            50% { height: 60px; opacity: 1; } 
            100% { height: 0; opacity: 0; } 
        }

        .purchase-area { max-width: 1100px; margin: 60px auto; display: flex; gap: 60px; padding: 40px; background: rgba(255,255,255,0.02); border: 1px solid rgba(255,255,255,0.05); }
        .mini-thumb { width: 85px; height: 85px; object-fit: cover; border: 1px solid var(--color); pointer-events: none; }
        .size-box { flex: 1; padding: 20px; border: 1px solid rgba(255,255,255,0.2); text-align: center; color: #fff; cursor: pointer; }
        .active-size { border-color: var(--color); background: rgba(212, 175, 55, 0.1); color: var(--color); }

        .order-btn { width: 100%; padding: 25px; background: #fff; color: #000; font-family: 'Cinzel', serif; font-weight: 700; font-size: 1.2rem; cursor: pointer; transition: 0.4s; letter-spacing: 4px; }
        .order-btn:hover { background: var(--color); color: #fff; }

        input { width: 100%; padding: 20px; margin-bottom: 20px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.2); font-family: 'Montserrat', sans-serif; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 10%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; padding: 20px; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <section class="product-section sauv-t" id="sauvage">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE</h1>
            <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>The Masterpiece</h3>
                <p>An extraordinary concentration of <b>Sauvage</b>. This Elixir reinterprets the iconic freshness with an extreme, intoxicating trail.</p>
                <p>A nocturnal soul that captures the raw power of the desert under a moonlit sky.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>Olfactory DNA</h3>
                <p><b>Top:</b> Cinnamon, Nutmeg, Cardamom & Grapefruit</p>
                <p><b>Heart:</b> A unique "Lavender AOP" essence from Nyons</p>
                <p><b>Base:</b> Licorice, Sandalwood, Amber & Patchouli</p>
                <div class="perf-data">Longevity: 12-14 Hours | Sillage: Enormous / Room-filling</div>
            </div>
        </div>

        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:30px">
                    <div><h2 style="font-family:'Cinzel';">ELIXIR 10ML</h2><p style="color:#666; font-size:12px">VELOORIA EXCLUSIVE DECANT</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><button class="order-btn">ORDER | 319 DH</button></form>
            </div>
        </div>
        <div class="scroll-down" onclick="document.getElementById('stronger').scrollIntoView();"><span></span></div>
    </section>

    <section class="product-section stron-t" id="stronger">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>The Obsession</h3>
                <p><b>Stronger With You Absolutely</b> is the most intense fragrance in the collection. A magnetic power that reflects absolute love.</p>
                <p>A refined masculine signature with a new, addictive rum accord.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>Olfactory DNA</h3>
                <p><b>Top:</b> Rum Accord, Bergamot & Elemi</p>
                <p><b>Heart:</b> Lavender & Davana</p>
                <p><b>Base:</b> Chestnut, Madagascar Vanilla, Cedar & Patchouli</p>
                <div class="perf-data">Longevity: 10-12 Hours | Sillage: Heavy / Intoxicating</div>
            </div>
        </div>

        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:30px">
                    <div><h2 style="font-family:'Cinzel';">INTENSE 10ML</h2><p style="color:#666; font-size:12px">ARMANI COLLECTION</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><button class="order-btn">ORDER | 319 DH</button></form>
            </div>
        </div>
        <div class="scroll-down" onclick="document.getElementById('libre').scrollIntoView();"><span></span></div>
    </section>

    <section class="product-section libre-t" id="libre">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>The Liberty</h3>
                <p>The fragrance of a woman who lives by her own rules. A floral fire that blends the coolness of French Lavender with Moroccan Orange Blossom.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>Olfactory DNA</h3>
                <p><b>Top:</b> Lavender, Mandarin Orange & Petitgrain</p>
                <p><b>Heart:</b> Orange Blossom, Jasmine & Lavender</p>
                <p><b>Base:</b> Madagascar Vanilla, Musk, Ambergris & Cedar</p>
                <div class="perf-data">Longevity: 8-9 Hours | Sillage: Elegant / Sophisticated</div>
            </div>
        </div>

        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:30px">
                    <div><h2 style="font-family:'Cinzel';">LIBRE 10ML</h2><p style="color:#666; font-size:12px">FEMALE ELITE</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><button class="order-btn">ORDER | 319 DH</button></form>
            </div>
        </div>
        <div class="scroll-down" onclick="document.getElementById('goodgirl').scrollIntoView();"><span></span></div>
    </section>

    <section class="product-section gg-t" id="goodgirl">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>The Duality</h3>
                <p>It's so good to be bad. <b>Good Girl</b> reflects the multi-dimensional character of the modern woman. Bold, sexy, and enigmatic.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>Olfactory DNA</h3>
                <p><b>Top:</b> Almond, Coffee, Bergamot & Lemon</p>
                <p><b>Heart:</b> Tuberose, Jasmine Sambac, Orris & Orange Blossom</p>
                <p><b>Base:</b> Tonka Bean, Cacao, Vanilla, Praline & Sandalwood</p>
                <div class="perf-data">Longevity: 10+ Hours | Sillage: Alluring / Seductive</div>
            </div>
        </div>

        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:30px">
                    <div><h2 style="font-family:'Cinzel';">GOOD GIRL 10ML</h2><p style="color:#666; font-size:12px">CH COLLECTION</p></div>
                    <img src="assets/gg-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE NUMBER"><button class="order-btn">ORDER | 319 DH</button></form>
            </div>
        </div>
    </section>

</body>
</html>
