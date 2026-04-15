<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* Scroll Snap Setup */
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        body, html { width: 100%; background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.4rem; letter-spacing: 10px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.5); }
        
        /* القسم كياخد شاشة كاملة */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; border-bottom: 1px solid rgba(255,255,255,0.05) !important; padding-bottom: 50px; }

        .v-header { width: 100%; height: 56.25vw; max-height: 80vh; overflow: hidden; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; padding: 60px 0; background: #000; }
        .img-bottle { width: 45%; max-width: 250px; height: auto; filter: drop-shadow(0 0 30px var(--glow)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.8rem; margin-top: 15px; letter-spacing: 6px; }

        .row { display: flex; align-items: center; width: 100%; min-height: 500px; padding: 40px 0; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 90%; max-width: 600px; height: auto; border-radius: 2px; }

        .txt-box { width: 50%; padding: 0 5%; text-align: center; position: relative; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; height: 100%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.15; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.2rem; color: var(--color); margin-bottom: 20px; text-transform: uppercase; }
        .desc-full { font-size: 0.95rem; line-height: 1.8; color: #ccc; }
        
        .specs-list { margin-top: 20px; list-style: none; display: inline-block; text-align: left; }
        .specs-list li { margin-bottom: 8px; font-size: 0.9rem; color: #eee; }
        .specs-list b { color: var(--color); }
        
        .tech-notes { font-size: 0.8rem; color: #777; margin-top: 25px; line-height: 1.6; font-style: italic; border-top: 1px solid rgba(255,255,255,0.1) !important; padding-top: 15px; max-width: 450px; margin: auto; }

        .f-wrap { padding: 80px 0; text-align: center; background: #000; }
        .f-glass { max-width: 450px; margin: 0 auto; padding: 30px; background: rgba(255,255,255,0.03); border-radius: 8px; }
        .in-f { width: 100%; padding: 18px; margin-bottom: 10px; background: rgba(255,255,255,0.07); color: #fff; border-radius: 4px; text-align: center; font-family: 'Montserrat'; }
        
        .btn-f { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; cursor: pointer; letter-spacing: 2px; border-radius: 4px; transition: 0.3s; }
        .btn-f:hover { background: var(--color); color: #fff; box-shadow: 0 5px 20px var(--glow); }
        
        .pri-txt { color: var(--color); margin-top: 15px; font-weight: 600; font-size: 0.85rem; }

        /* Themes */
        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }

        @media (max-width: 900px) { 
            .row, .row.rev { flex-direction: column; } 
            .img-box, .txt-box { width: 100%; padding: 20px 5%; } 
            .product-section { height: auto; scroll-snap-align: none; }
            html { scroll-snap-type: none; }
        }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="sauvage-bottle.png" class="img-bottle"><h1 class="brand-logo">SAUVAGE</h1></div>
        <div class="row"><div class="img-box"><img src="sauvage-left.jpg"></div><div class="txt-box"><div class="glow-effect"></div><h3>La fragrance</h3><p class="desc-full">Sauvage Elixir est un parfum extraordinairement concentré, infusé de la fraîcheur emblématique de Sauvage. Une composition haute couture.</p></div></div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro de Téléphone" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="stronger-bottle.png" class="img-bottle"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        <div class="row"><div class="img-box"><img src="stronger-left.jpg"></div><div class="txt-box"><div class="glow-effect"></div><h3>La fragrance</h3><p class="desc-full">Un parfum qui vit dans le présent, façonné par l'énergie de la modernité.</p></div></div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro de Téléphone" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="libre-bottle.png" class="img-bottle"><h1 class="brand-logo">LIBRE (EAU DE PARFUM)</h1></div>
        <div class="row"><div class="img-box"><img src="libre-left.jpg"></div><div class="txt-box"><div class="glow-effect"></div><h3>La fragrance</h3><p class="desc-full">Libre : la nouvelle Eau de Parfum, le parfum de la liberté.</p></div></div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro de Téléphone" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="goodgirl-bottle.png" class="img-bottle"><h1 class="brand-logo">GOOD GIRL</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="gg-detail-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p class="desc-full">La douceur et le pouvoir de séduction du jasmin renforcent encore l’éclat de Good Girl. Le côté mystérieux de Good Girl est révélé grâce au cacao riche en arômes et à l’enivrante fève tonka, tandis que les notes d’amande et de café déposent une touche finale d’éclat mêlé d’audace.</p>
                <ul class="specs-list">
                    <li><b>Pour :</b> Elle</li>
                    <li><b>Elle est :</b> Séductrice et Puissante</li>
                    <li><b>Occasion :</b> Le jour et la nuit</li>
                    <li><b>Famille olfactive :</b> AMBRÉE Ambrée Florale</li>
                    <li><b>La fragrance :</b> Puissante et Provocante</li>
                </ul>
                <div style="margin-top:20px;">
                    <h4 style="font-family:'Playfair Display'; color:var(--color);">Le flacon</h4>
                    <p class="desc-full">Associant l’esthétique de la haute couture à l’expertise technique, l’emblématique talon aiguille Good Girl est à l’image des femmes puissantes.</p>
                </div>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="gg-detail-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Ingrédients Principaux</h3>
                <div class="desc-full" style="text-align:left; display:inline-block;">
                    <p><b>Famille Olfactive :</b> AMBRÉE Ambrée Florale</p>
                    <p><b>Notes de Tête :</b> Amande</p>
                    <p><b>Notes de Cœur :</b> Jasmin d’Arabie & Tubéreuse</p>
                    <p><b>Notes de Fond :</b> Fève Tonka & Cacao</p>
                </div>
                <div class="tech-notes">
                    <p>* Notes de tête : Première impression d’un parfum (5-15 min).</p>
                    <p>* Notes de cœur : Dure 20 à 60 minutes environ.</p>
                    <p>* Notes de fond : Reste le plus longtemps sur la peau (jusqu’à 6 heures).</p>
                </div>
            </div>
        </div>

        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro de Téléphone" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button><p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p></form></div>
    </div>

</body>
</html>
