<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; padding-bottom: 100px; }
        .v-header { width: 100%; height: 56.25vw; max-height: 80vh; overflow: hidden; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; padding: 60px 0; }
        .img-bottle { width: 40%; max-width: 200px; height: auto; transition: 0.4s; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.5rem; margin-top: 15px; letter-spacing: 6px; }

        .row { display: flex; align-items: center; width: 100%; padding: 50px 5%; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        
        .img-box { width: 50%; display: flex; justify-content: center; z-index: 2; }
        .img-box img { width: 90%; max-width: 500px; border-radius: 2px; cursor: zoom-in; }

        .txt-box { width: 50%; padding: 0 5%; text-align: left; position: relative; z-index: 2; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 140%; height: 140%; background: radial-gradient(circle, var(--glow) 0%, transparent 75%); opacity: 0.35; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.8rem; color: var(--color); margin-bottom: 15px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; padding-bottom: 5px; }
        p, li { font-size: 0.9rem; line-height: 1.6; color: #eee; margin-bottom: 10px; }
        b { color: var(--color); }

        .tech-notes { font-size: 0.75rem; color: #bbb; margin-top: 20px; line-height: 1.5; font-style: italic; border-top: 1px solid rgba(255,255,255,0.2) !important; padding-top: 15px; }

        /* --- New Purchase Area (Minimalist & English) --- */
        .purchase-area { max-width: 1000px; margin: 80px auto 0; display: flex; gap: 50px; padding: 20px; align-items: flex-start; }
        
        .details-side { width: 45%; }
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .product-meta h2 { font-family: 'Cinzel', serif; font-size: 1rem; color: #fff; letter-spacing: 2px; }
        .mini-thumb { width: 55px; height: 55px; border-radius: 2px; cursor: pointer; transition: 0.3s; object-fit: cover; border: 1px solid rgba(255,255,255,0.2) !important; }
        
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 12px; border: 1px solid rgba(255,255,255,0.15) !important; border-radius: 2px; transition: 0.4s ease; background: transparent; }
        .size-item span { display: block; font-weight: 600; font-size: 1rem; }
        .size-item .sprays { font-size: 0.65rem; color: #888; letter-spacing: 1px; margin-top: 4px; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); box-shadow: 0 0 15px var(--glow); }

        .form-side { width: 55%; }
        .form-side input { width: 100%; padding: 15px; margin-bottom: 12px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.15) !important; font-size: 0.9rem; font-family: 'Montserrat', sans-serif; }
        .form-side input:focus { border-bottom-color: var(--color) !important; }
        .buy-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; cursor: pointer; border-radius: 2px; font-size: 1rem; letter-spacing: 2px; transition: 0.4s; margin-top: 10px; }
        .buy-btn:hover { background: var(--color); color: #fff; box-shadow: 0 5px 20px var(--glow); }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; cursor: zoom-out; }
        .zoom-overlay img { max-width: 80%; max-height: 80%; }

        @media (max-width: 900px) { 
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; } 
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; gap: 40px; margin-top: 40px; }
            .details-side, .form-side { width: 100%; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay" onclick="this.style.display='none'"><img src="" id="zoomedImg"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">SAUVAGE</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>A high-fashion composition infused with wild freshness. The trail is of rare power, a raw elegance that reveals an authentic and true man.</p>
                <p><b>For:</b> Him | <b>Style:</b> Raw & Noble | <b>Occasion:</b> Day & Night | <b>Family:</b> AROMATIC Fougère</p>
                <h3>The Bottle</h3>
                <p>A luxurious design object with clean, dark lines, reflecting the power of the desert at the magical hour of twilight.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Main Ingredients:</b> Bergamot, Pepper, Ambroxan</p>
                <p><b>Top Notes:</b> Calabria Bergamot</p>
                <p><b>Heart Notes:</b> Sichuan Pepper & Lavender</p>
                <p><b>Base Notes:</b> Ambroxan & Musk</p>
                <div class="tech-notes">
                    <p>* Top notes: First impression, lasts 5-15 minutes.</p>
                    <p>* Heart notes: Emerges after top notes fade (20-60 min).</p>
                    <p>* Base notes: The longest lasting scent (up to 6 hours).</p>
                </div>
            </div>
        </div>

        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta">
                    <div><h2>SAUVAGE ELIXIR</h2><p style="font-size:0.6rem; color:#666;">PREMIUM TRAVEL DECANT</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb" onclick="zoom(this.src)">
                </div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'sauv-in')"><div class="size-box"><span>5ML</span><p class="sprays">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'sauv-in')"><div class="size-box"><span>10ML</span><p class="sprays">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side">
                <form>
                    <input type="hidden" id="sauv-in" value="10ml">
                    <input type="text" placeholder="FULL NAME" required>
                    <input type="tel" placeholder="PHONE NUMBER" required>
                    <input type="text" placeholder="CITY" required>
                    <input type="text" placeholder="SHIPPING ADDRESS" required>
                    <button type="submit" class="buy-btn">ORDER NOW | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p>A fragrance that lives in the present, carried by the energy of modernity. Unpredictable, it surprises with its originality, like the spicy accord of the top notes.</p>
                <p><b>For:</b> Him | <b>Style:</b> Magnetic & Sensual | <b>Occasion:</b> Day & Night | <b>Family:</b> ORIENTAL Fougère</p>
                <h3>The Bottle</h3>
                <p>The clean lines and curves recall masculine shoulders. The round metallic cap adds a touch of modern elegance.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Olfactory Notes</h3>
                <p><b>Main Ingredients:</b> Cardamom, Sage, Vanilla</p>
                <p><b>Top Notes:</b> Cardamom & Pink Pepper</p>
                <p><b>Heart Notes:</b> Sage & Violet Leaf</p>
                <p><b>Base Notes:</b> Vanilla & Chestnut</p>
                <div class="tech-notes">
                    <p>* Top notes: First impression (5-15 min).</p>
                    <p>* Heart notes: Emerges after (20-60 min).</p>
                    <p>* Base notes: Longest lasting (up to 6 hours).</p>
                </div>
            </div>
        </div>

        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta">
                    <div><h2>STRONGER WITH YOU</h2><p style="font-size:0.6rem; color:#666;">INTENSE MALE FRAGRANCE</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb" onclick="zoom(this.src)">
                </div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'stron-in')"><div class="size-box"><span>5ML</span><p class="sprays">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'stron-in')"><div class="size-box"><span>10ML</span><p class="sprays">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side">
                <form>
                    <input type="hidden" id="stron-in" value="10ml">
                    <input type="text" placeholder="FULL NAME" required>
                    <input type="tel" placeholder="PHONE NUMBER" required>
                    <input type="text" placeholder="CITY" required>
                    <input type="text" placeholder="SHIPPING ADDRESS" required>
                    <button type="submit" class="buy-btn">ORDER NOW | 319 DH</button>
                </form>
            </div>
        </div>
    </div>

    <script>
        function zoom(img) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = img.src || img;
            overlay.style.display = 'flex';
        }
        function selectSize(element, size, inputId) {
            element.parentElement.querySelectorAll('.size-item').forEach(i => i.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
