<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Brand Officiel</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Inter',sans-serif;
  background:linear-gradient(
    180deg,
    #2b1e14 0%,
    #4a3525 45%,
    #f5f0e6 100%
  );
  color:#1e1a17;
}

/* HERO */
.hero{
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
}

.hero h1{
  font-family:'Playfair Display',serif;
  font-size:64px;
  color:#f5f0e6;
  margin-bottom:20px;
}

.hero p{
  color:#e6ddcf;
  opacity:0.85;
  font-size:18px;
}

/* SECTION */
.section{
  padding:120px 8%;
}

.section h2{
  text-align:center;
  font-family:'Playfair Display',serif;
  font-size:42px;
  margin-bottom:80px;
}

/* PRODUCTS LAYOUT */
.products{
  display:flex;
  flex-direction:column;
  gap:50px;
}

/* CARD GENERAL */
.card{
  position:relative;
  background:rgba(255,255,255,0.78);
  backdrop-filter:blur(8px);
  border-radius:26px;
  overflow:hidden;
  box-shadow:0 30px 70px rgba(0,0,0,0.25);
  transition:transform 0.4s ease, box-shadow 0.4s ease;
  cursor:pointer;
}

.card:hover{
  transform:translateY(-6px);
  box-shadow:0 45px 90px rgba(0,0,0,0.35);
}

/* CARD LINK */
.card a{
  position:absolute;
  inset:0;
  z-index:5;
}

/* IMAGE */
.card img{
  width:100%;
  height:100%;
  object-fit:cover;
  position:absolute;
  inset:0;
  z-index:1;
}

/* OVERLAY */
.card::after{
  content:'';
  position:absolute;
  inset:0;
  background:linear-gradient(
    180deg,
    rgba(0,0,0,0.15),
    rgba(0,0,0,0.55)
  );
  z-index:2;
}

/* CONTENT */
.card-content{
  position:relative;
  z-index:3;
  padding:40px;
  color:#fff;
}

.card-content h3{
  font-family:'Playfair Display',serif;
  font-size:32px;
  margin-bottom:10px;
}

.card-content p{
  font-size:15px;
  opacity:0.85;
}

/* MAIN CARD */
.card-main{
  height:420px;
}

/* SMALL CARDS */
.card-row{
  display:flex;
  gap:40px;
  flex-wrap:wrap;
}

.card-small{
  flex:1;
  min-width:260px;
  height:300px;
}

/* FOOTER */
footer{
  text-align:center;
  padding:70px 0;
  font-size:12px;
  opacity:0.6;
}
</style>
</head>

<body>

<section class="hero">
  <div>
    <h1>YOUR BRAND</h1>
    <p>Élégance. Identité. Présence.</p>
  </div>
</section>

<section class="section">
  <h2>Collection</h2>

  <div class="products">

    <!-- PRODUIT PRINCIPAL -->
    <div class="card card-main">
      <img src="gel.jpg" alt="Produit principal">
      <a href="https://wa.me/212691444558" target="_blank"></a>
      <div class="card-content">
        <h3>Produit Signature</h3>
        <p>La pièce maîtresse de la collection.</p>
      </div>
    </div>

    <!-- DEUX PRODUITS -->
    <div class="card-row">

      <div class="card card-small">
        <img src="spray.jpg" alt="Produit 2">
        <a href="https://wa.me/212691444558" target="_blank"></a>
        <div class="card-content">
          <h3>Produit II</h3>
          <p>Équilibre et distinction.</p>
        </div>
      </div>

      <div class="card card-small">
        <img src="produit3.jpg" alt="Produit 3">
        <a href="https://wa.me/212691444558" target="_blank"></a>
        <div class="card-content">
          <h3>Produit III</h3>
          <p>Minimalisme affirmé.</p>
        </div>
      </div>

    </div>

  </div>
</section>

<footer>
© 2026 — Brand Officiel
</footer>

</body>
</html>
