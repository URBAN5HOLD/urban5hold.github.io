.logo-container {
  text-align: center;     /* Logo فالوسط */
  margin: 10px auto;      /* مسافة بسيطة من الأعلى والأسفل */
  padding: 10px 0;        /* مسافة إضافية صغيرة للراحة */
}

.logo {
  max-width: 150px;       /* حجم مناسب للصفحة */
  height: auto;            /* يحافظ على النسبة */
  display: inline-block;   /* باش يبقى متناسق وسط الصفحة */
}


<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جيل طبيعي لتثبيت الشعر</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(180deg, #0f0f0f, #1a1a1a);
  color: #f5f5f5;
  direction: rtl;
}

/* ===== Hero Section ===== */
.hero {
  text-align: center;
  padding: 80px 20px;
}

.hero h1 {
  font-size: 40px;
  margin-bottom: 20px;
  letter-spacing: 1px;
}

.hero p {
  font-size: 18px;
  max-width: 700px;
  margin: auto;
  color: #cfcfcf;
}

/* ===== Product Section ===== */
.product {
  max-width: 900px;
  margin: 60px auto;
  background: #111;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
}

.product img {
  width: 100%;       /* تعمر الكادر ديال الصفحة */
  max-width: 488;  /* أقصى عرض باش ما توليش كبيرة بزاف */
  height: auto;      /* يحافظ على النسبة ويخليها متناسبة */
  object-fit: contain; /* الصورة كلها تبان بلا تقطيع */
  border-radius: 12px; /* اختيار شخصي: يقدر يعطي شكل راقي */
  margin: 20px 0;    /* مسافة من النص فوق وتحت */
  display: block;
  margin-left: auto;
  margin-right: auto; /* باش الصورة تبان فالوسط */
}



.product-content {
  padding: 40px;
}

.product-content h2 {
  font-size: 28px;
  margin-bottom: 15px;
}

.product-content .subtitle {
  color: #8fd19e;
  margin-bottom: 25px;
  font-size: 16px;
}

/* ===== Description ===== */
.product-content p {
  font-size: 17px;
  line-height: 1.9;
  color: #ddd;
}

/* ===== Benefits ===== */
.benefits {
  margin-top: 30px;
}

.benefits div {
  margin-bottom: 12px;
  font-size: 16px;
}

/* ===== Button ===== */
.btn {
  display: inline-block;
  margin-top: 40px;
  padding: 15px 35px;
  background: #25D366;
  color: #000;
  font-size: 18px;
  font-weight: bold;
  border-radius: 30px;
  text-decoration: none;
}

.btn:hover {
  opacity: 0.85;
}

/* ===== Footer ===== */
.footer {
  text-align: center;
  padding: 30px;
  color: #777;
  font-size: 14px;
}
</style>
</head>

<body>

<!-- ===== HERO ===== -->
<section class="hero">
  <h1>ماشي غير جيل… هاد أسلوب عناية</h1>
  <p>
  أغلب منتجات تثبيت الشعر كتخدم اليوم وتضر غداً.
  احنا صنعنا جيل واعي، كيحترم شعرك قبل ما يفرض عليه الشكل.
  </p>
</section>

<!-- ===== PRODUCT ===== -->
<section class="product">

 <img src="gel.jpg" alt="جيل تثبيت الشعر">


  <div class="product-content">
    <h2>جيل تثبيت الشعر الطبيعي</h2>
    <div class="subtitle">تثبيت ذكي بلا مواد كيميائية قاصحة</div>

    <p>
    معظم الجيلات فالسوق معمّرة بالكحول والمواد الكيميائية
    اللي كتعطيك شكل مؤقت ولكن مع الوقت كتجفف الشعر وكتضعف الجذور.<br><br>

    هاد الجيل تصاوب بعقلية مختلفة:
    تثبيت يدوم، بدون ما يعاقب شعرك.
    </p>

    <div class="benefits">
      <div>✔ تثبيت قوي ومرن بدون تصلب</div>
      <div>✔ بلا كحول وبلا مواد مؤذية</div>
      <div>✔ لمعان طبيعي ماشي دهني</div>
      <div>✔ صالح للاستعمال اليومي</div>
    </div>

    <a class="btn" href="https://wa.me/212691444558" target="_blank">
      اطلبه الآن عبر واتساب
    </a>

  </div>
</section>

<div class="footer">
  منتوج موجّه للناس اللي وعات أن العناية ماشي رفاهية.
</div>

</body>
</html>


