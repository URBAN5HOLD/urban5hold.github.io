<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Brand Officiel</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', sans-serif;
  background: linear-gradient(180deg, rgba(43,30,20,0.95), rgba(245,240,230,0.95));
  color: #fff;
  direction: rtl;
}

.container {
  max-width: 480px;
  margin: 0 auto;
  padding: 40px 20px;
}

.brand {
  font-family: 'Playfair Display', serif;
  font-size: 36px;
  text-align: center;
  margin-bottom: 10px;
}

.subtitle {
  text-align: center;
  font-size: 15px;
  color: #ddd;
  margin-bottom: 30px;
}

.product-main, .product-row {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.product-card {
  background: rgba(255,255,255,0.08);
  border-radius: 20px;
  padding: 22px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.25);
  backdrop-filter: blur(8px);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  animation: fadeUp 1s ease forwards;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 25px 60px rgba(0,0,0,0.35);
}

.product-image {
  width: 100%;
  border-radius: 16px;
  margin-bottom: 18px;
}

.title {
  font-family: 'Playfair Display', serif;
  font-size: 22px;
  margin-bottom: 8px;
  color: #fff;
}

.desc {
  font-size: 14.5px;
  line-height: 1.7;
  color: #eee;
  margin-bottom: 12px;
}

.features {
  list-style: none;
  margin-bottom: 15px;
  padding-left: 0;
}

.features li {
  margin-bottom: 6px;
  font-size: 14px;
  color: #ddd;
}

.price {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 15px;
  color: #fff;
}

.btn {
  display: block;
  width: 100%;
  text-align: center;
  padding: 15px;
  background: linear-gradient(135deg, #3a2a1f, #6f4e37);
  color: #fff;
  text-decoration: none;
  font-size: 16px;
  border-radius: 12px;
  font-weight: bold;
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.25);
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* animation delay */
.product-card:nth-child(1) { animation-delay: 0.2s; }
.product-card:nth-child(2) { animation-delay: 0.4s; }
.product-card:nth-child(3) { animation-delay: 0.6s; }

</style>
</head>
<body>

<div class="container">
  <div class="brand">Urban Hold</div>
  <div class="subtitle">ثبات راقي. حضور قوي.</div>

  <!-- البطاقة الرئيسية -->
  <div class="product-main">
    <div class="product-card">
      <img src="gel.jpg" alt="جيل تثبيت الشعر" class="product-image">
      <div class="title">جيل تثبيت الشعر</div>
      <div class="desc">
        تركيبة قوية تمنحك ثباتا قصويا ولمسة نهائية لامعة طبيعية. للشعر القاسي والقصير، يوفر تحكم كامل دون أن يترك الشعر صلبا.
      </div>
      <ul class="features">
        <li>✔ ثبات طويل يدوم طوال اليوم</li>
        <li>✔ ملمس طبيعي بدون قساوة</li>
        <li>✔ مناسب للاستعمال اليومي</li>
      </ul>
      <div class="price">35 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب الجيل" target="_blank">اطلب الآن عبر واتساب</a>
    </div>
  </div>

  <!-- الصف للبطاقتين التاليتين -->
  <div class="product-row">
    <div class="product-card">
      <img src="spray.jpg" alt="سبراي تثبيت الشعر" class="product-image">
      <div class="title">سبراي تثبيت الشعر</div>
      <div class="desc">
        سبراي خفيف يعطيك ثبات متوسط ولمسة ناعمة للشعر مع حماية من الرطوبة.
      </div>
      <ul class="features">
        <li>✔ ثبات متوسط وطبيعي</li>
        <li>✔ حماية من الرطوبة</li>
        <li>✔ مثالي للشعر القصير والطويل</li>
      </ul>
      <div class="price">40 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب السبراي" target="_blank">اطلب الآن عبر واتساب</a>
    </div>

    <div class="product-card">
      <img src="wax.jpg" alt="واكس الشعر" class="product-image">
      <div class="title">واكس الشعر</div>
      <div class="desc">
        واكس غني لتشكيل الشعر بأشكال متعددة مع لمسة نهائية لامعة طبيعية.
      </div>
      <ul class="features">
        <li>✔ تشكيل سهل ومرن</li>
        <li>✔ لمسة لامعة طبيعية</li>
        <li>✔ مثالي للشعر القصير والطويل</li>
      </ul>
      <div class="price">45 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب الواكس" target="_blank">اطلب الآن عبر واتساب</a>
    </div>
  </div>

</div>

</body>
</html>
