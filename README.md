<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Beauty | Luxury Decants</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; color: #fff; }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; padding-bottom: 100px; }
        .v-header { width: 100%; height: 50vw; max-height: 70vh; overflow: hidden; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }

        /* --- Purchase Area (Minimalist & Free) --- */
        .purchase-area { 
            max-width: 1000px; margin: 50px auto; 
            display: flex; gap: 50px; padding: 20px;
            align-items: flex-start;
        }

        /* Left Side: Product Details & Sizes */
        .details-side { width: 45%; }
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .product-meta h2 { font-family: 'Cinzel', serif; font-size: 1.1rem; color: #fff; letter-spacing: 2px; }
        .mini-thumb { width: 60px; height: 60px; border-radius: 4px; cursor: pointer; transition: 0.3s; object-fit: cover; border: 1px solid rgba(255,255,255,0.2) !important; }
        .mini-thumb:hover { transform: scale(1.1); border-color: var(--color) !important; }

        .size-container { display: flex; gap: 20px; margin-top: 20px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { 
            padding: 15px; border: 1px solid rgba(255,255,255,0.15) !important; 
            border-radius: 2px; transition: 0.4s ease; background: transparent;
        }
        .size-item span { display: block; font-weight: 600; font-size: 1rem; margin-bottom: 5px; }
        .size-item .sprays { font-size: 0.7rem; color: #888; letter-spacing: 1px; }
        
        /* Active State logic based on perfume color */
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); box-shadow: 0 0 15px var(--glow); }

        /* Right Side: Form */
        .form-side { width: 55%; }
        .form-side input { 
            width: 100%; padding: 18px; margin-bottom: 15px; 
            background: transparent; color: #fff; 
            border-bottom: 1px solid rgba(255,255,255,0.2) !important; 
            font-size: 0.95rem; font-family: 'Montserrat', sans-serif;
        }
        .form-side input:focus { border-bottom-color: var(--color) !important; }
        .buy-btn { 
            width: 100%; padding: 22px; background: #fff; color: #000; 
            font-weight: 800; cursor: pointer; border-radius: 2px; 
            font-size: 1.1rem; letter-spacing: 2px; margin-top: 10px;
            transition: 0.4s;
        }
        .buy-btn:hover { background: var(--color); color: #fff; box-shadow: 0 5px 20px var(--glow); }

        /* Zoom Overlay */
        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; cursor: zoom-out; }
        .zoom-overlay img { max-width: 80%; max-height: 80%; }

        @media (max-width: 850px) {
            .purchase-area { flex-direction: column-reverse; gap: 40px; }
            .details-side, .form-side { width: 100%; }
        }

        /* Themes */
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
        
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta">
                    <div>
                        <h2>SAUVAGE ELIXIR</h2>
                        <p style="font-size: 0.7rem; color: #666;">PREMIUM QUALITY DECANT</p>
                    </div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb" onclick="fullZoom(this.src)">
                </div>

                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'sauvage-input')">
                        <div class="size-box">
                            <span>5ML</span>
                            <p class="sprays">~ 75 SPRAYS</p>
                        </div>
                    </div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'sauvage-input')">
                        <div class="size-box">
                            <span>10ML</span>
                            <p class="sprays">~ 150 SPRAYS</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="form-side">
                <form>
                    <input type="hidden" id="sauvage-input" value="10ml">
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
        
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta">
                    <div>
                        <h2>STRONGER WITH YOU</h2>
                        <p style="font-size: 0.7rem; color: #666;">INTENSE MALE FRAGRANCE</p>
                    </div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb" onclick="fullZoom(this.src)">
                </div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'stronger-input')">
                        <div class="size-box">
                            <span>5ML</span>
                            <p class="sprays">~ 75 SPRAYS</p>
                        </div>
                    </div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'stronger-input')">
                        <div class="size-box">
                            <span>10ML</span>
                            <p class="sprays">~ 150 SPRAYS</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="form-side">
                <form>
                    <input type="hidden" id="stronger-input" value="10ml">
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
        function fullZoom(src) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = src;
            overlay.style.display = 'flex';
        }

        function selectSize(element, size, inputId) {
            const container = element.parentElement;
            container.querySelectorAll('.size-item').forEach(item => item.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
