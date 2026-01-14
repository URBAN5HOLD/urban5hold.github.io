<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Urban Hold</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Inter:wght@300;400&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(180deg, #2b1e14 0%, #4a3525 50%, #f5f0e6 100%);
      direction: rtl;
      color: #111;
      min-height: 100vh;
    }

    .container { max-width: 960px; margin: 40px auto; padding: 0 20px; }

    .brand { 
      font-family: 'Playfair Display', serif; 
      font-size: 36px; 
      text-align: center; 
      color: #fff; 
      margin-bottom: 10px; 
    }
    .subtitle { 
      text-align: center; 
      color: #e8dccb; 
      font-size: 16px; 
      margin-bottom: 40px; 
    }

    .product-row {
      display: flex; 
      flex-wrap: wrap; 
      gap: 25px; 
      justify-content: center;
    }

    .product-card {
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 20px;
      width: 300px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
      color: #fff;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 25px 50px rgba(0,0,0,0.4);
    }

    .product-image {
      width: 100%;
      border-radius: 15px;
      margin-bottom: 15px;
    }

    .title { font-family: 'Playfair Display', serif; font-size: 22px; margin-bottom: 10px; }
    .desc { font-size: 14px; line-height: 1.6; margin-bottom: 12px; }
    .features { list-style: none; margin-bottom: 12px; font-size: 14px; }
    .features li { margin-bottom: 6px; }
    .price { font-size: 18px; font-weight: 600; margin-bottom: 15px; }
    .btn {
      display: block;
      text-align: center;
      padding: 12px;
      background: linear-gradient(135deg, #3a2a1f, #6f4e37);
      color: #fff;
      text-decoration: none;
      border-radius: 12px;
      font-size: 16px;
    }
    .note { text-align: center; font-size: 13px; color: #eee; margin-top: 30px; }
  </style>
</head>
<body>
  <div class="container">
    <div class="brand">Urban Hold</div>
    <div class="subtitle">ثبات راقي. حضور قوي.</div>

    <div class="product-row">
      <!-- المنتج الأول -->
      <div class="product-card" onclick="window.location.href='https://wa.me/212600000000?text=سلام، بغيت نطلب جيل تثبيت الشعر'">
        <img src="gel.jpg" alt="جيل تثبيت الشعر" class="product-image" />
        <div class="title">جيل تثبيت الشعر</div>
        <div class="desc">تركيبة مدروسة بعناية لتمنحك ثباتًا قويًا ولمسة طبيعية.</div>
        <ul class="features">
          <li>✔ ثبات طويل يدوم طوال اليوم</li>
          <li>✔ ملمس طبيعي بدون قساوة</li>
          <li>✔ مناسب للاستعمال اليومي</li>
        </ul>
        <div class="price">35 درهم</div>
        <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب جيل تثبيت الشعر" target="_blank">اطلب الآن</a>
      </div>

      <!-- المنتج الثاني -->
      <div class="product-card" onclick="window.location.href='https://wa.me/212691444558?text=سلام، بغيت نطلب سبراي تثبيت الشعر'">
        <img src="spray.jpg" alt="سبراي تثبيت الشعر" class="product-image" />
        <div class="title">سبراي تثبيت الشعر</div>
        <div class="desc">سبراي خفيف يعطيك ثبات متوسط ولمسة ناعمة للشعر مع حماية من الرطوبة.</div>
        <ul class="features">
          <li>✔ ثبات متوسط وطبيعي</li>
          <li>✔ حماية من الرطوبة</li>
          <li>✔ مثالي للشعر القصير والطويل</li>
        </ul>
        <div class="price">40 درهم</div>
        <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب سبراي تثبيت الشعر" target="_blank">اطلب الآن</a>
      </div>

      <!-- المنتج الثالث -->
      <div class="product-card" onclick="window.location.href='https://wa.me/212691444558?text=سلام، بغيت نطلب واكس الشعر'">
        <img src="wax.jpg" alt="واكس الشعر" class="product-image" />
        <div class="title">واكس الشعر</div>
        <div class="desc">واكس غني لتشكيل الشعر بأشكال متعددة مع لمسة نهائية لامعة طبيعية.</div>
        <ul class="features">
          <li>✔ تشكيل سهل ومرن</li>
          <li>✔ لمسة لامعة طبيعية</li>
          <li>✔ مثالي للشعر القصير والطويل</li>
        </ul>
        <div class="price">45 درهم</div>
        <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب واكس الشعر" target="_blank">اطلب الآن</a>
      </div>
    </div>

    <div class="note">توصيل لجميع المدن المغربية</div>
  </div>
</body>
</html>
