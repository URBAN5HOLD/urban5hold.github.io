<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Urban Hold</title>

  <!-- خطوط راقية -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Inter', sans-serif;
      direction: rtl;
      color: #111;

      background: linear-gradient(180deg, rgba(58,42,31,0.85), rgba(245,240,230,0.95)), 
                  url('background.jpg') center/cover no-repeat;
      min-height: 100vh;
    }

    .overlay {
      min-height: 100vh;
      padding-bottom: 60px;
    }

    .container {
      max-width: 450px;
      margin: 0 auto;
      padding: 40px 20px;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .brand {
      font-family: 'Playfair Display', serif;
      font-size: 34px;
      color: #fff;
      text-align: center;
      margin-bottom: 10px;
    }

    .subtitle {
      text-align: center;
      color: #e8dccb;
      font-size: 14px;
      margin-bottom: 30px;
    }

    .product-card {
      background: rgba(255,255,255,0.92);
      border-radius: 22px;
      padding: 22px;
      box-shadow: 0 25px 60px rgba(0,0,0,0.25);
      margin-bottom: 20px;
      animation: fadeUp 1.2s ease forwards;
    }

    .product-image {
      width: 100%;
      border-radius: 16px;
      margin-bottom: 15px;
    }

    .title {
      font-family: 'Playfair Display', serif;
      font-size: 22px;
      margin-bottom: 8px;
    }

    .desc {
      font-size: 14.5px;
      line-height: 1.7;
      color: #444;
      margin-bottom: 15px;
    }

    .features {
      list-style: none;
      margin-bottom: 15px;
    }

    .features li {
      margin-bottom: 5px;
      font-size: 14px;
    }

    .price {
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 15px;
    }

    .btn {
      display: block;
      width: 100%;
      text-align: center;
      padding: 16px;
      background: linear-gradient(135deg, #3a2a1f, #6f4e37);
      color: #fff;
      text-decoration: none;
      font-size: 17px;
      border-radius: 14px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    }

    .note {
      text-align: center;
      font-size: 13px;
      color: #eee;
      margin-top: 25px;
    }

    /* ترتيب المنتجات الثانية والثالثة */
    .product-row {
      display: flex;
      gap: 20px;
      margin-top: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .product-row .product-card:nth-child(1) { animation-delay: 0.3s; }
    .product-row .product-card:nth-child(2) { animation-delay: 0.6s; }

  </style>
</head>
<body>
  <div class="overlay">
    <div class="container">

      <div class="brand">Urban Hold</div>
      <div class="subtitle">ثبات راقي. حضور قوي.</div>

      <!-- المنتج الأول -->
      <div class="product-card">
        <img src="gel.jpg" alt="جيل تثبيت الشعر" class="product-image" />
        <div class="title">جيل تثبيت الشعر</div>
        <div class="desc">
          تركيبة مدروسة بعناية لتمنحك ثباتًا قويًا ولمسة طبيعية، بدون قساوة أو آثار دهنية.
        </div>
        <ul class="features">
          <li>✔ ثبات طويل يدوم طوال اليوم</li>
          <li>✔ ملمس طبيعي بدون قساوة</li>
          <li>✔ مناسب للاستعمال اليومي</li>
        </ul>
        <div class="price">35 درهم</div>
        <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب جيل تثبيت الشعر" target="_blank">
          اطلب الآن عبر واتساب
        </a>
      </div>

      <!-- المنتجات الثانية والثالثة -->
      <div class="product-row">
        <!-- المنتج الثاني -->
        <div class="product-card">
          <img src="spray.jpg" alt="سبراي تثبيت الشعر" class="product-image" />
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
          <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب سبراي تثبيت الشعر" target="_blank">
            اطلب الآن عبر واتساب
          </a>
        </div>

        <!-- المنتج الثالث -->
        <div class="product-card">
          <img src="wax.jpg" alt="واكس الشعر" class="product-image" />
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
          <a class="btn" href="https://wa.me/212691444558?text=سلام، بغيت نطلب واكس الشعر" target="_blank">
            اطلب الآن عبر واتساب
          </a>
        </div>
      </div>

      <div class="note">توصيل لجميع المدن المغربية</div>

    </div>
  </div>
</body>
</html>
