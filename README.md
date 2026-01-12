<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>منتجاتنا</title>
  <style>
    /* ----- تصميم عام للصفحة ----- */
    body {
      font-family: Arial, sans-serif;
      background: #f7f7f7;
      margin: 0;
      padding: 0;
      direction: rtl; /* النص بالعربية */
    }

    /* ----- رأس الصفحة ----- */
    header {
      background: #25D366; /* لون واتساب أخضر */
      color: #fff;
      text-align: center;
      padding: 25px 15px;
      font-size: 28px;
      font-weight: bold;
    }

    /* ----- حاوية المنتجات ----- */
    .products-container {
      max-width: 1000px;
      margin: 30px auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); /* شبكة متجاوبة */
      gap: 20px;
      padding: 0 15px;
    }

    /* ----- بطاقة كل منتوج ----- */
    .product-card {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.2s;
    }

    /* تأثير عند المرور على البطاقة */
    .product-card:hover {
      transform: translateY(-5px);
    }

    /* صورة المنتوج */
    .product-card img {
      width: 100%;
      height: 250px;
      object-fit: cover;
    }

    /* معلومات المنتوج */
    .product-info {
      padding: 20px;
      text-align: center;
    }

    .product-info h2 {
      margin: 0 0 10px;
      color: #222;
      font-size: 22px;
    }

    .product-info p {
      color: #555;
      font-size: 16px;
      line-height: 1.5;
    }

    /* زر التواصل واتساب */
    .btn {
      display: inline-block;
      margin-top: 15px;
      padding: 12px 25px;
      background: #25D366;
      color: #fff;
      font-size: 18px;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      transition: background 0.2s;
    }

    .btn:hover {
      background: #1ebe5d;
    }

    /* تذييل الصفحة */
    footer {
      text-align: center;
      margin: 40px 0 20px;
      color: #777;
      font-size: 14px;
    }
  </style>
</head>
<body>

<header>منتجاتنا</header>

<div class="products-container">

  <!-- ----- منتوج 1 ----- -->
  <div class="product-card">
    <img src="images/gel1.jpg" alt="جيل تثبيت الشعر">
    <div class="product-info">
      <h2>جيل تثبيت الشعر</h2>
      <p>
        جيل قوي لتثبيت الشعر، يعطي شكل أنيق وثبات طويل بدون ما يخلي الشعر قاصح.
        مناسب للاستعمال اليومي ويعطي لمعة خفيفة.
      </p>
      <a class="btn" href="https://wa.me/212600000000" target="_blank">تواصل عبر واتساب</a>
    </div>
  </div>

  <!-- ----- منتوج 2 ----- -->
  <div class="product-card">
    <img src="images/gel2.jpg" alt="شامبو مغذي">
    <div class="product-info">
      <h2>شامبو مغذي للشعر</h2>
      <p>
        شامبو طبيعي يغذي فروة الرأس ويعطي لمعان وقوة للشعر. خفيف وكيصلح لجميع أنواع الشعر.
      </p>
      <a class="btn" href="https://wa.me/212600000000" target="_blank">تواصل عبر واتساب</a>
    </div>
  </div>

  <!-- ----- منتوج 3 ----- -->
  <div class="product-card">
    <img src="images/gel3.jpg" alt="بلسم مرطب">
    <div class="product-info">
      <h2>بلسم مرطب</h2>
      <p>
        بلسم مرطب للشعر الجاف والتالف. كيرطب الشعر بعمق ويخليه ناعم وسهل التسريح.
      </p>
      <a class="btn" href="https://wa.me/212600000000" target="_blank">تواصل عبر واتساب</a>
    </div>
  </div>

  <!-- ----- تقدر تزيد أي منتوج جديد بنفس الطريقة ----- -->

</div>

<footer>
  للطلب أو الاستفسار، كليكي على الزر وغادي تهضر معنا مباشرة فواتساب.
</footer>

</body>
</html>

