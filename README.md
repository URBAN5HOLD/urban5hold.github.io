<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Outazarine</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Inter',sans-serif;
  background:#fff;
  color:#111;
}

/* ===== HEADER / LOGO ===== */
header{
  height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  background:url("hero.jpg") center/cover no-repeat;
}

.brand-logo{
  font-family:'Playfair Display',serif;
  font-size:42px;
  font-weight:600;
  letter-spacing:0.08em;
  color:#000;
  background:rgba(255,255,255,0.85);
  padding:18px 40px;
}

/* ===== PRODUCTS SECTION ===== */
section{
  max-width:1200px;
  margin:120px auto;
  padding:0 20px;
}

.products{
  display:grid;
  grid-template-columns:1fr;
  gap:60px;
}

/* layout */
.products-bottom{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
}

/* ===== CARD ===== */
.card{
  position:relative;
  border-radius:18px;
  overflow:hidden;
  cursor:pointer;
  background:#f6f6f6;
  box-shadow:0 30px 60px rgba(0,0,0,0.12);
  transition:transform .5s ease, box-shadow .5s ease;
}

.card:hover{
  transform:translateY(-10px);
  box-shadow:0 45px 90px rgba(0,0,0,0.18);
}

/* image */
.card img{
  width:100%;
  height:380px;
  object-fit:cover;
  display:block;
}

/* content */
.card-content{
  padding:26px;
}

.card h3{
  font-family:'Playfair Display',serif;
  font-size:22px;
  margin-bottom:12px;
}

.card p{
  font-size:15px;
  line-height:1.7;
  color:#333;
}

/* ===== WhatsApp badge ===== */
.whatsapp-badge{
  position:absolute;
  bottom:20px;
  right:20px;
  width:52px;
  height:52px;
  background:#25D366;
  border-radius:12px;
  display:flex;
  align-items:center;
  justify-content:center;
  box-shadow:0 10px 25px rgba(0,0,0,0.25);
}

.whatsapp-badge svg{
  width:26px;
  height:26px;
  fill:#fff;
}

/* ===== remove any underline ===== */
a,
a:hover,
a:focus,
a:visited{
  text-decoration:none !important;
  border:none !important;
  color:inherit;
}

.card *{
  text-decoration:none !important;
}

/* ===== responsive ===== */
@media(max-width:900px){
  .products-bottom{
    grid-template-columns:1fr;
  }

  .card img{
    height:300px;
  }
}
</style>
</head>

<body>

<header>
  <div class="brand-logo">OUTAZARINE</div>
</header>

<section>
  <div class="products">

    <!-- MAIN PRODUCT -->
    <a href="https://wa.me/212691444558" class="card">
      <img src="product1.jpg" alt="">
      <div class="card-content">
        <h3>Gel de fixation forte</h3>
        <p>
        منتوج التثبيت القوي لي كيعطيك شعر قاصح ولامع بحال الفازك بالماء.
        كيثبت التسريحة طوال النهار بلا ما يخلي أثر دهني، ومناسب للاستعمال اليومي
        بطريقة سهلة ونظيفة.
        </p>
      </div>
      <div class="whatsapp-badge">
        <svg viewBox="0 0 24 24">
          <path d="M12 2a10 10 0 0 0-8.66 15l-1.3 4.74 4.86-1.28A10 10 0 1 0 12 2z"/>
        </svg>
      </div>
    </a>

    <!-- TWO PRODUCTS -->
    <div class="products-bottom">

      <a href="https://wa.me/212691444558" class="card">
        <img src="product2.jpg" alt="">
        <div class="card-content">
          <h3>Fixation moyenne</h3>
          <p>
          نسخة أخف شوية من المنتوج الأول، كيعطي ثبات مزيان
          ولكن كيخلي الشعر طبيعي وما قاصحش بزاف،
          مناسب للناس لي باغيين ستايل أنيق ومريح.
          </p>
        </div>
        <div class="whatsapp-badge">
          <svg viewBox="0 0 24 24">
            <path d="M12 2a10 10 0 0 0-8.66 15l-1.3 4.74 4.86-1.28A10 10 0 1 0 12 2z"/>
          </svg>
        </div>
      </a>

      <a href="https://wa.me/212691444558" class="card">
        <img src="product3.jpg" alt="">
        <div class="card-content">
          <h3>Fixation légère</h3>
          <p>
          منتوج خفيف بزاف، كيعطي مظهر طبيعي
          وثبات متوسط، مناسب للاستعمال اليومي
          وللناس لي ما باغيينش شعرهم يتقاصح بزاف
          ولكن يبقى منظم وأنيق.
          </p>
        </div>
        <div class="whatsapp-badge">
          <svg viewBox="0 0 24 24">
            <path d="M12 2a10 10 0 0 0-8.66 15l-1.3 4.74 4.86-1.28A10 10 0 1 0 12 2z"/>
          </svg>
        </div>
      </a>

    </div>
  </div>
</section>

</body>
</html>
