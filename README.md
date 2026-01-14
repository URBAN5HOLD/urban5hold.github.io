<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Urban Hold</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Inter',sans-serif;
  background:#ffffff;
  color:#111;
}

/* ===== HERO ===== */
.hero{
  position:relative;
  height:100vh;
  background:url('hero.jpg') center/cover no-repeat;
  display:flex;
  align-items:center;
  justify-content:center;
}

.hero::after{
  content:"";
  position:absolute;
  inset:0;
  background:rgba(255,255,255,0.35);
}

.logo{
  position:relative;
  z-index:2;
  width:220px;
  animation:logoFloat 1.2s ease;
}

@keyframes logoFloat{
  from{opacity:0; transform:translateY(30px);}
  to{opacity:1; transform:translateY(0);}
}

/* ===== SECTION ===== */
.section{
  max-width:1100px;
  margin:auto;
  padding:80px 20px;
}

/* ===== PRODUCT CARD ===== */
.product{
  background:#fff;
  border-radius:18px;
  overflow:hidden;
  cursor:pointer;
  transition:all .4s ease;
  box-shadow:0 15px 40px rgba(0,0,0,.08);
}

.product:hover{
  transform:translateY(-6px);
  box-shadow:0 25px 60px rgba(0,0,0,.15);
}

.product img{
  width:100%;
  display:block;
}

.product-content{
  padding:22px;
}

.product h2{
  font-family:'Playfair Display',serif;
  font-size:22px;
  margin-bottom:10px;
}

.product p{
  font-size:14px;
  line-height:1.8;
  color:#444;
}

/* ===== GRID ===== */
.main-product{
  max-width:520px;
  margin:0 auto 70px;
}

.sub-products{
  display:flex;
  gap:40px;
  justify-content:center;
  flex-wrap:wrap;
}

.sub-products .product{
  max-width:420px;
}

/* ===== LINK RESET ===== */
a{
  text-decoration:none;
  color:inherit;
}
</style>
</head>

<body>

<!-- HERO -->
<div class="hero">
  <img src="LOGO.png" alt="Urban Hold" class="logo">
</div>

<!-- PRODUCTS -->
<div class="section">

  <!-- المنتج الأساسي -->
  <a href="https://wa.me/212691444558?text=سلام، بغيت نطلب جيل تثبيت الشعر">
    <div class="product main-product">
      <img src="gel.jpg" alt="جيل تثبيت الشعر">
      <div class="product-content">
        <h2>جيل تثبيت الشعر</h2>
        <p>
          جيل احترافي بتركيبة مركّزة، يمنحك ثبات قوي ولمعة أنيقة تدوم طوال اليوم.
          يحافظ على شكل التسريحة بدون تكتل أو جفاف، ويُستعمل بسهولة للحصول
          على ستايل عصري ونظيف.
        </p>
      </div>
    </div>
  </a>

  <!-- المنتجات الثانوية -->
  <div class="sub-products">

    <a href="https://wa.me/212691444558?text=سلام، بغيت نطلب سبراي تثبيت الشعر">
      <div class="product">
        <img src="spray.jpg" alt="سبراي تثبيت الشعر">
        <div class="product-content">
          <h2>سبراي تثبيت الشعر</h2>
          <p>
            سبراي خفيف يمنحك ثبات متوازن ولمسة طبيعية،
            مناسب للاستعمال اليومي ويترك الشعر مرن وسهل التعديل.
          </p>
        </div>
      </div>
    </a>

    <a href="https://wa.me/212691444558?text=سلام، بغيت نطلب واكس الشعر">
      <div class="product">
        <img src="wax.jpg" alt="واكس الشعر">
        <div class="product-content">
          <h2>واكس الشعر</h2>
          <p>
            واكس خفيف القوام يمنحك مظهر عصري بدون قساوة،
            مثالي للستايلات اليومية ولمسة أنيقة غير مبالغ فيها.
          </p>
        </div>
      </div>
    </a>

  </div>
</div>

</body>
</html>
