<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Urban Hold - المنتجات</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family:'Inter',sans-serif;
  background: linear-gradient(180deg, #2b1e14 0%, #4a3525 50%, #f5f0e6 100%);
  min-height: 100vh;
  color: #111;
  padding: 40px 20px;
}

h1 { text-align:center; font-family:'Playfair Display', serif; font-size:36px; color:#fff; margin-bottom:10px;}
.subtitle { text-align:center; color:#e8dccb; font-size:16px; margin-bottom:40px;}

.product-row {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}

.product-card {
  flex: 1 1 250px;
  max-width: 300px;
  background: rgba(255,255,255,0.15);
  backdrop-filter: blur(12px);
  border-radius: 20px;
  padding: 20px;
  text-align: center;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 8px 20px rgba(0,0,0,0.25);
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 28px rgba(0,0,0,0.35);
}

.product-image {
  width:100%;
  border-radius: 16px;
  margin-bottom:15px;
}

.title { font-family:'Playfair Display', serif; font-size:22px; margin-bottom:10px; color:#fff;}
.desc { font-size:14px; line-height:1.6; color:#eee; margin-bottom:12px;}
.features { list-style:none; padding:0; margin-bottom:15px;}
.features li { margin-bottom:6px; color:#fff; font-size:14px;}

.price { font-weight:600; font-size:18px; color:#fff; margin-bottom:15px;}
</style>
</head>
<body>

<h1>Urban Hold</h1>
<div class="subtitle">ثبات راقي. حضور قوي.</div>

<div class="product-row">

  <div class="product-card" onclick="window.location.href='product1.html'">
    <img src="gel.jpg" alt="جيل تثبيت الشعر" class="product-image">
    <div class="title">جيل تثبيت الشعر</div>
    <div class="desc">تركيبة مدروسة تمنحك ثبات قوي ولمسة طبيعية بدون قساوة.</div>
    <ul class="features">
      <li>✔ ثبات طويل طوال اليوم</li>
      <li>✔ ملمس طبيعي</li>
      <li>✔ مناسب للاستعمال اليومي</li>
    </ul>
    <div class="price">35 درهم</div>
  </div>

  <div class="product-card" onclick="window.location.href='product2.html'">
    <img src="spray.jpg" alt="سبراي تثبيت الشعر" class="product-image">
    <div class="title">سبراي تثبيت الشعر</div>
    <div class="desc">سبراي خفيف يعطيك ثبات متوسط ولمسة ناعمة مع حماية من الرطوبة.</div>
    <ul class="features">
      <li>✔ ثبات متوسط وطبيعي</li>
      <li>✔ حماية من الرطوبة</li>
      <li>✔ مثالي للشعر القصير والطويل</li>
    </ul>
    <div class="price">40 درهم</div>
  </div>

  <div class="product-card" onclick="window.location.href='product3.html'">
    <img src="wax.jpg" alt="واكس الشعر" class="product-image">
    <div class="title">واكس الشعر</div>
    <div class="desc">واكس غني لتشكيل الشعر بأشكال متعددة ولمسة نهائية لامعة طبيعية.</div>
    <ul class="features">
      <li>✔ تشكيل سهل ومرن</li>
      <li>✔ لمسة لامعة طبيعية</li>
      <li>✔ مثالي للشعر القصير والطويل</li>
    </ul>
    <div class="price">45 درهم</div>
  </div>

</div>

</body>
</html>

<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جيل تثبيت الشعر - Urban Hold</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">
<style>
body { font-family:'Inter',sans-serif; background:#f3f0e6; color:#111; padding:30px;}
.container { max-width:600px; margin:auto; background:rgba(255,255,255,0.95); padding:25px; border-radius:20px; box-shadow:0 10px 25px rgba(0,0,0,0.2);}
h1 { font-family:'Playfair Display', serif; font-size:28px; margin-bottom:15px;}
.product-image { width:100%; border-radius:16px; margin-bottom:20px;}
.desc { line-height:1.7; margin-bottom:15px;}
.features { list-style:none; padding:0; margin-bottom:20px;}
.features li { margin-bottom:8px; font-size:15px;}
.price { font-size:20px; font-weight:600; margin-bottom:20px;}
.btn { display:block; text-align:center; padding:15px; background:#25D366; color:#fff; text-decoration:none; border-radius:12px; font-weight:bold; transition:0.3s ease;}
.btn:hover { background:#1ebe5d;}
</style>
</head>
<body>

<div class="container">
  <h1>جيل تثبيت الشعر</h1>
  <img src="gel.jpg" alt="جيل تثبيت الشعر" class="product-image">
  <div class="desc">
    هذا الجيل غني بالمواد الطبيعية التي تمنح الشعر ثباتًا ممتازًا ولمسة ناعمة بدون أي قساوة. مناسب للاستعمال اليومي ويعطي لمعة خفيفة.
  </div>
  <ul class="features">
    <li>✔ ثبات طويل طوال اليوم</li>
    <li>✔ ملمس طبيعي بدون قساوة</li>
    <li>✔ مناسب لجميع أنواع الشعر</li>
  </ul>
  <div class="price">35 درهم</div>
  <a class="btn" href="https://wa.me/212600000000?text=سلام، بغيت نطلب جيل تثبيت الشعر" target="_blank">اطلب الآن عبر واتساب</a>
</div>

</body>
</html>
