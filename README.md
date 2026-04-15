<html lang="fr">
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
        
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; background: #000; padding-bottom: 50px; }
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

        .f-wrap { padding: 60px 0; text-align: center; }
        .f-glass { max-width: 420px; margin: 0 auto; padding: 30px; background: rgba(255,255,255,0.05); border-radius: 8px; border: 1px solid rgba(255,255,255,0.1) !important; }
        .in-f { width: 100%; padding: 18px; margin-bottom: 12px; background: rgba(255,255,255,0.1); color: #fff; border-radius: 4px; text-align: center; font-size: 1rem; }
        .btn-f { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; cursor: pointer; border-radius: 4px; transition: 0.3s; font-size: 1.1rem; }
        .btn-f:hover { background: var(--color); color: #fff; box-shadow: 0 5px 25px var(--glow); }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; cursor: zoom-out; }
        .zoom-overlay img { max-width: 90%; max-height: 90%; object-fit: contain; }

        @media (max-width: 900px) { 
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; } 
            .img-box, .txt-box { width: 100%; text-align: center; } 
            .img-box img { width: 100%; margin-bottom: 20px; }
            .brand-logo { font-size: 1.8rem; }
            .product-section { height: auto; scroll-snap-align: start; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay"><img src="" id="zoomedImg"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">SAUVAGE</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p>Une composition haute couture infusée d'une fraîcheur sauvage. Le sillage est d'une puissance rare, une élégance brute qui révèle un homme authentique et vrai.</p>
                <p><b>Pour :</b> Lui<br><b>Style :</b> Brut et Noble<br><b>Occasion :</b> Le jour et la nuit<br><b>Famille olfactive :</b> AROMATIQUE Fougère<br><b>La fragrance :</b> Fraîche et Puissante</p>
                <h3>Le flacon</h3>
                <p>Un objet de design luxueux aux lignes sombres et épurées, reflétant la puissance du désert à l'heure magique du crépuscule.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Notes Olfactives</h3>
                <p><b>Ingrédients Principaux :</b> Bergamote, Poivre, Ambroxan</p>
                <p><b>Famille Olfactive :</b> AROMATIQUE Fougère</p>
                <p><b>Notes de Tête :</b> Bergamote de Calabre</p>
                <p><b>Notes de Cœur :</b> Poivre du Sichuan & Lavande</p>
                <p><b>Notes de Fond :</b> Ambroxan & Musc</p>
                <div class="tech-notes">
                    <p>* Notes de tête : Première impression d’un parfum, dure entre 5 et 15 minutes.</p>
                    <p>* Notes de cœur : Commencent à ressortir lorsque les notes de tête s’estompent (20-60 min).</p>
                    <p>* Notes de fond : La senteur qui reste le plus longtemps sur la peau (jusqu’à 6 heures).</p>
                </div>
            </div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro" class="in-f" required><input type="text" placeholder="Adresse" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button></form></div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p>Un parfum qui vit dans le présent, porté par l'énergie de la modernité. Imprévisible, il surprend par son originalité, comme l'accord épicé des notes de tête.</p>
                <p><b>Pour :</b> Lui<br><b>Style :</b> Magnétique et Sensuel<br><b>Occasion :</b> Le jour et la nuit<br><b>Famille olfactive :</b> FOUGÈRE Oriental<br><b>La fragrance :</b> Addictive et Intense</p>
                <h3>Le flacon</h3>
                <p>Les lignes nettes et les courbes rappellent des épaules masculines. Le bouchon métallique rond ajoute une touche d'élégance moderne.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Notes Olfactives</h3>
                <p><b>Ingrédients Principaux :</b> Cardamome, Sauge, Vanille</p>
                <p><b>Famille Olfactive :</b> FOUGÈRE Oriental</p>
                <p><b>Notes de Tête :</b> Cardamome & Poivre Rose</p>
                <p><b>Notes de Cœur :</b> Sauge & Feuille de Violette</p>
                <p><b>Notes de Fond :</b> Vanille & Châtaigne</p>
                <div class="tech-notes">
                    <p>* Notes de tête : Première impression (5-15 min).</p>
                    <p>* Notes de cœur : Ressortent après (20-60 min).</p>
                    <p>* Notes de fond : Reste le plus longtemps (jusqu’à 6 heures).</p>
                </div>
            </div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro" class="in-f" required><input type="text" placeholder="Adresse" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button></form></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">LIBRE (EDP)</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p>Le parfum de la liberté. Une tension entre la sensualité brûlante de la fleur d'oranger du Maroc et la fraîcheur audacieuse de la lavande de France.</p>
                <p><b>Pour :</b> Elle<br><b>Style :</b> Audacieuse et Libre<br><b>Occasion :</b> Le jour et la nuit<br><b>Famille olfactive :</b> FLORAL Lavande<br><b>La fragrance :</b> Éclatante et Chic</p>
                <h3>Le flacon</h3>
                <p>Un flacon couture avec le logo Cassandre surdimensionné, incrusté dans le verre comme un bijou précieux.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Notes Olfactives</h3>
                <p><b>Ingrédients Principaux :</b> Lavande, Fleur d'Oranger, Vanille</p>
                <p><b>Famille Olfactive :</b> FLORAL Solaire</p>
                <p><b>Notes de Tête :</b> Mandarine & Lavande</p>
                <p><b>Notes de Cœur :</b> Fleur d'Oranger & Jasmin d’Arabie</p>
                <p><b>Notes de Fond :</b> Vanille de Madagascar & Musc</p>
                <div class="tech-notes">
                    <p>* Notes de tête : Première impression (5-15 min).</p>
                    <p>* Notes de cœur : Ressortent بعد (20-60 min).</p>
                    <p>* Notes de fond : Reste le plus longtemps (jusqu’à 6 heures).</p>
                </div>
            </div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro" class="in-f" required><input type="text" placeholder="Adresse" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button></form></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">GOOD GIRL</h1></div>
        
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p>La douceur et le pouvoir de séduction du jasmin renforcent encore l’éclat de Good Girl. Le côté mystérieux est révélé grâce au cacao riche en arômes et à l’enivrante fève tonka, tandis que les notes d’amande et de café déposent une touche finale d’éclat mêlé d’audace.</p>
                <p><b>Pour :</b> Elle<br><b>Elle est :</b> Séductrice et Puissante<br><b>Occasion :</b> Le jour et la nuit<br><b>Famille olfactive :</b> AMBRÉE Ambrée Florale<br><b>La fragrance :</b> Puissante et Provocante</p>
                <h3>Le flacon</h3>
                <p>Associant l’esthétique de la haute couture à l’expertise technique, l’emblématique talon aiguille Good Girl est à l’image des femmes puissantes qui inspirent sa silhouette.</p>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Notes Olfactives</h3>
                <p><b>Ingrédients Principaux :</b> Jasmin, Tubéreuse, Fève Tonka</p>
                <p><b>Famille Olfactive :</b> AMBRÉE Ambrée Florale</p>
                <p><b>Notes de Tête :</b> Amande</p>
                <p><b>Notes de Cœur :</b> Jasmin d’Arabie & Tubéreuse</p>
                <p><b>Notes de Fond :</b> Fève Tonka & Cacao</p>
                <div class="tech-notes">
                    <p>* Notes de tête : Première impression d’un parfum, dure entre 5 et 15 minutes.</p>
                    <p>* Notes de cœur : Commencent à ressortir lorsque les notes de tête s’estompent (20-60 min).</p>
                    <p>* Notes de fond : La senteur qui reste le plus longtemps sur la peau (jusqu’à 6 heures).</p>
                </div>
            </div>
        </div>
        <div class="f-wrap"><form class="f-glass"><input type="text" placeholder="Nom Complet" class="in-f" required><input type="tel" placeholder="Numéro" class="in-f" required><input type="text" placeholder="Adresse" class="in-f" required><button type="submit" class="btn-f">COMMANDER | 319 DH</button></form></div>
    </div>

    <script>
        function zoom(img) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = img.src;
            overlay.style.display = 'flex';
        }
        document.getElementById('zoomOverlay').onclick = function() {
            this.style.display = 'none';
        }
    </script>
</body>
</html>
