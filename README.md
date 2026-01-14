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

body {
  font-family: 'Inter', sans-serif;
  background: linear-gradient(180deg, #2b1e14 0%, #4a3525 50%, #f5f0e6 100%);
  color: #111;
  min-height: 100vh;
}

.container {
  max-width: 430px;
  margin: 0 auto;
  padding: 40px 22px;
}

.brand {
  font-family: 'Playfair Display', serif;
  font-size: 34px;
  text-align: center;
  color: #fff;
  margin-bottom: 15px;
}

.subtitle {
  text-align: center;
  color: #e8dccb;
  margin-bottom: 30px;
}

/* بطاقة المنتج الرئيسية */
.product-main .product-card {
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(10px);
  border-radius: 22px;
  padding: 22px;
  box-shadow: 0 25px 60px rgba(0,0,0,0.3);
  margin-bottom: 30px;
  animation: fadeUp 1s ease forwards;
}

.product-row {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}

.product-row .product-card {
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(10px);
  border-radius: 22px;
  padding: 18px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.25);
  flex: 1 1 200px;
  max-width: 250px;
  animation: fadeUp 1s ease forwards;
}

/* تأخير تدريجي لكل بطاقة */
.product-row .product-card:nth-child(1) { animation-delay: 0.3s; }
.product-row .product-card:nth-child(2) { animation-delay: 0.6s; }

.product-image {
  width: 100%;
  border-radius: 16px;
  margin-bottom: 12px;
}

.title {
  font-family: 'Playfair Display', serif;
  font-size: 20px;
  margin-bottom: 8px;
  color: #fff;
}

.desc {
  font-size: 14px;
  line-height: 1.6;
  color: #ddd;
  margin-bottom: 10px;
}

.features {
  list-style: none;
  margin-bottom: 12px;
}

.features li {
  font-size: 13px;
  margin-bottom: 6px;
  color: #ccc;
}

.price {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 12px;
  color: #fff;
}

.btn {
  display: block;
  width: 100%;
  text-align: center;
  padding: 12px;
  background: linear-gradient(135deg, #3a2a1f, #6f4e37);
  color: #fff;
  text-decoration: none;
  font-size: 16px;
  border-radius: 12px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.25);
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
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
        تركيبة قوية تمنحك ثباتا قصويا ولمسة نهائية لامعة طبيعية...
      </div>
      <ul class="features">
        <li>✔ ثبات طويل يدوم طوال اليوم</li>
        <li>✔ ملمس طبيعي بدون قساوة</li>
      </ul>
      <div class="price">35 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=طلب الجيل" target="_blank">اطلب الآن</a>
    </div>
  </div>

  <!-- الصف للبطاقتين الصغيرتين -->
  <div class="product-row">
    <div class="product-card">
      <img src="spray.jpg" alt="سبراي تثبيت الشعر" class="product-image">
      <div class="title">سبراي تثبيت الشعر</div>
      <div class="desc">سبراي خفيف يعطيك ثبات متوسط ولمسة ناعمة للشعر...</div>
      <ul class="features">
        <li>✔ ثبات متوسط وطبيعي</li>
        <li>✔ حماية من الرطوبة</li>
      </ul>
      <div class="price">40 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=طلب السبراي" target="_blank">اطلب الآن</a>
    </div>

    <div class="product-card">
      <img src="wax.jpg" alt="واكس الشعر" class="product-image">
      <div class="title">واكس الشعر</div>
      <div class="desc">واكس غني لتشكيل الشعر بأشكال متعددة...</div>
      <ul class="features">
        <li>✔ تشكيل سهل ومرن</li>
        <li>✔ لمسة لامعة طبيعية</li>
      </ul>
      <div class="price">45 درهم</div>
      <a class="btn" href="https://wa.me/212691444558?text=طلب الواكس" target="_blank">اطلب الآن</a>
    </div>
  </div>
</div>
</body>
</html>
