<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>H Y</title>

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

/* ===== HEADER ===== */
header{
  height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  background:url("hero.jpg") center/cover no-repeat;
}

.brand-logo{
  font-family:'Playfair Display',serif;
  font-size:44px;
  font-weight:600;
  letter-spacing:0.12em;
  color:#000;
}

/* ===== SECTION ===== */
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

.products-bottom{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
}

/* ===== CARD ===== */
.card{
  border-radius:18px;
  overflow:hidden;
  background:#f5f5f5;
  box-shadow:0 30px 60px rgba(0,0,0,0.12);
  transition:transform .5s ease, box-shadow .5s ease;
}

.card:hover{
  transform:translateY(-10px);
  box-shadow:0 45px 90px rgba(0,0,0,0.18);
}

.card img{
  width:100%;
  height:380px;
  object-fit:cover;
  display:block;
}

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

/* ===== WhatsApp BAR ===== */
.whatsapp-bar{
  background:#25D366;
  text-align:center;
  padding:16px;
  font-weight:500;
  letter-spacing:0.04em;
  color:#fff;
  transition:background .3s ease;
}

.card:hover .whatsapp-bar{
  background:#1ebe5d;
}

/* ===== LINK RESET ===== */
a{
  text-decoration:none;
  color:inherit;
  display:block;
}

/* ===== RESPONSIVE ===== */
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
      <img src="gel.jpg" alt="">
      <div class="card-content">
        <h3>Gel de fixation forte</h3>
        <p>
        منتوج تثبيت قوي كيعطيك شعر قاصح ولامع بحال الفازك بالماء،
        كيثبت التسريحة طول النهار بلا أثر دهني،
        ومناسب للاستعمال اليومي بطريقة سهلة ونظيفة.
        </p>
      </div>
      <div class="whatsapp-bar">اطلب الآن عبر واتساب</div>
    </a>

    <!-- TWO PRODUCTS -->
    <div class="products-bottom">

      <a href="https://wa.me/212691444558" class="card">
        <img src="spray.jpg" alt="">
        <div class="card-content">
          <h3>Fixation moyenne</h3>
          <p>
          ثبات متوسط كيعطي ستايل طبيعي،
          ما كيقصّحش الشعر بزاف وكيخليه منظم وأنيق.
          </p>
        </div>
        <div class="whatsapp-bar">اطلب الآن عبر واتساب</div>
      </a>

      <a href="https://wa.me/212691444558" class="card">
        <img src="wax.jpg" alt="">
        <div class="card-content">
          <h3>Fixation légère</h3>
          <p>
          تركيبة خفيفة بزاف،
          كتحافظ على مظهر طبيعي مع ثبات متوسط
          مناسب للاستعمال اليومي.
          </p>
        </div>
        <div class="whatsapp-bar">اطلب الآن عبر واتساب</div>
      </a>

    </div>
  </div>
</section>

</body>
</html>
