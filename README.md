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
  /* إزالة أي خط تحت النص نهائياً */
.card,
.card *{
  text-decoration: none !important;
  border: none !important;
}

/* العناوين */
.card h3{
  font-family:'Playfair Display', serif;
  font-style: arabe;
  font-size:22px;
  font-weight:500;
  letter-spacing:0.03em;
  color:#111;
  margin-bottom:14px;
}

/* الوصف */
.card p{
  font-family:'Inter', sans-serif;
  font-style: italic;
  font-size:15px;
  line-height:1.8;
  color:#333;
  text-decoration:none !important;
}

}


body{
  font-family:'Inter',sans-serif;
  background:#fff;
  color:#111;
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
  object-fit:contain;
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
   .card img{
  width: 100%;
  height: 300px;      /* هنا كتحدد الطول اللي بغيت */
  object-fit: cover; /* كيقص الزائد بلا ما يشوّه الصورة */
  display: block;
}

  }
}
</style>
</head>

<body>

<section>
  <div class="products">

    <!-- MAIN PRODUCT -->
    <a href="https://wa.me/212691444558" class="card">
      <img src="gel.jpg" alt="">
      <div class="card-content">
        <h3>Gel de fixation forte</h3>
        <p>
       A strong-hold styling product that gives your hair a firm, shiny look similar to a water-based pomade.
Keeps your hairstyle in place all day without leaving any greasy residue
and is suitable for daily use with a clean and easy application


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
