<html lang="en">
<head>
  <!-- Google tag (gtag.js) -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=G-4BSNJLYWR0"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-4BSNJLYWR0');
  </script>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Velooria Beauty | Official Luxury Collection</title>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">

  <style>
    /* ── Reset ─────────────────────────────────────────────────── */
    * { margin:0; padding:0; box-sizing:border-box; outline:none !important; border:none !important; text-decoration:none !important; background:none !important; -webkit-tap-highlight-color:transparent; }
    html, body { width:100%; background-color:#000 !important; scroll-snap-type:y mandatory; scroll-behavior:smooth; font-family:'Montserrat',sans-serif; color:#fff; overflow-x:hidden; }

    /* ── Fixed UI chrome ───────────────────────────────────────── */
    .logo-fixed { position:fixed; top:25px; left:50%; transform:translateX(-50%); z-index:1000; font-family:'Cinzel',serif; font-size:1.2rem; letter-spacing:10px; color:#fff !important; pointer-events:none; }
    .scroll-trigger { position:fixed; top:75%; right:25px; transform:translateY(-50%); width:40px; height:40px; z-index:2000; cursor:pointer; display:flex; align-items:center; justify-content:center; }
    .arrow-icon { width:20px; height:20px; border-right:3px solid var(--current-arrow-color,#fff) !important; border-bottom:3px solid var(--current-arrow-color,#fff) !important; transform:rotate(45deg); animation:bounce 2s infinite; transition:0.5s ease; }
    .arrow-up { transform:rotate(-135deg) !important; }
    @keyframes bounce     { 0%,100%{transform:translateY(-5px) rotate(45deg);}  50%{transform:translateY(5px) rotate(45deg);} }
    @keyframes bounce-up  { 0%,100%{transform:translateY(5px) rotate(-135deg);} 50%{transform:translateY(-5px) rotate(-135deg);} }

    /* ── Sections ──────────────────────────────────────────────── */
    .product-section { width:100%; min-height:100vh; scroll-snap-align:start; position:relative; padding-bottom:80px; background-color:#000 !important; }
    .glow-center { position:absolute; top:40%; left:50%; transform:translate(-50%,-50%); width:600px; height:600px; background:radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 75%) !important; opacity:0.3; z-index:0; pointer-events:none; }
    .v-header { width:100%; position:relative; z-index:1; line-height:0; }
    .bg-v { width:100%; height:auto; display:block; }
    .bottle-center { text-align:center; padding:40px 0; position:relative; z-index:2; margin-top:-50px; }
    .img-bottle { width:65%; max-width:400px; margin:0 auto; display:block; filter:drop-shadow(0 0 35px rgba(0,0,0,0.9)); transition:transform 0.3s ease; }
    .brand-logo { font-family:'Cinzel',serif; font-size:2rem; color:#fff !important; letter-spacing:6px; margin:10px 0; }
    .perfume-sub { font-size:0.7rem; color:var(--color) !important; letter-spacing:4px; text-transform:uppercase; font-weight:600; }
    .text-glow-free { position:relative; z-index:2; padding:25px; background:radial-gradient(ellipse at center, var(--glow-color) 0%, rgba(0,0,0,0) 85%) !important; }
    .row { display:flex; align-items:center; width:100%; padding:50px 10%; gap:60px; position:relative; z-index:2; }
    .row.rev { flex-direction:row-reverse; }
    .img-box { width:45%; }
    .img-box img { width:100%; border-radius:4px; display:block; box-shadow:0 10px 30px rgba(0,0,0,0.5); }
    .txt-box { width:55%; text-align:left; }
    .txt-box h3 { font-family:'Cinzel',serif; font-size:1.5rem; margin-bottom:20px; color:var(--color) !important; letter-spacing:2px; }
    .txt-box p { font-size:0.95rem; line-height:1.9; color:#f0f0f0 !important; font-weight:300; margin-bottom:12px; }
    .highlight { color:var(--color) !important; font-weight:600; font-size:0.85rem; margin-right:5px; }
    .purchase-area { max-width:1000px; margin:40px auto; display:flex; gap:40px; padding:40px; border-top:1px solid rgba(255,255,255,0.1) !important; border-bottom:1px solid rgba(255,255,255,0.1) !important; width:90%; position:relative; z-index:2; }
    .mini-thumb { width:100px; height:100px; object-fit:cover; }
    .size-container { display:flex; gap:15px; margin-top:15px; }
    .size-box { flex:1; padding:15px; border:1px solid rgba(255,255,255,0.2) !important; text-align:center; cursor:pointer; color:#fff; }
    .size-box span { display:block; font-size:9px; color:#888; }
    .active-size { border-color:var(--color) !important; background:rgba(255,255,255,0.05) !important; }
    input { width:100%; padding:18px 0; margin-bottom:15px; color:#fff !important; border-bottom:1px solid rgba(255,255,255,0.3) !important; font-family:'Montserrat'; }
    .order-btn { width:100%; padding:22px; background-color:#fff !important; color:#000 !important; font-weight:800; cursor:pointer; letter-spacing:4px; }
    @media(max-width:900px){ .row,.row.rev{flex-direction:column;text-align:center;padding:40px 5%;} .img-box,.txt-box{width:100%;} .purchase-area{flex-direction:column-reverse;padding:25px;} }

    /* ── Theme colours ─────────────────────────────────────────── */
    .sauv-t  { --color:#4A90E2; --glow-color:rgba(74,144,226,0.35); }
    .stron-t { --color:#CD7F32; --glow-color:rgba(205,127,50,0.35); }
    .libre-t { --color:#D4AF37; --glow-color:rgba(212,175,55,0.35); }
    .gg-t    { --color:#1a4d99; --glow-color:rgba(26,77,153,0.35); }
    a[href*="veloriabeauty.github.io"]{ display:none !important; visibility:hidden !important; }

    /* ══════════════════════════════════════════════════════════════
       🐱  CAT WIDGET  —  position:fixed, bottom-RIGHT corner
       z-index 9990 = above all videos and page content.
       Typebot bubble uses placement:"left" so there is ZERO overlap.
    ══════════════════════════════════════════════════════════════ */
    #cat-widget {
      position: fixed;
      bottom: 22px;
      right: 22px;
      z-index: 9990;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0;
      cursor: pointer;
      /* Fade in smoothly 1.5s after load */
      opacity: 0;
      transition: opacity 1.2s ease;
    }
    #cat-widget.cat-visible { opacity: 1; }

    /* ── Speech bubble above cat ───────────────────────────────── */
    /*    Arabic text, Montserrat font, white pill with gold outline  */
    #cat-bubble {
      position: relative;
      font-family: 'Montserrat', sans-serif;
      font-size: 10.5px;
      font-weight: 600;
      letter-spacing: 0.3px;
      color: #1a1a1a !important;
      background: rgba(255,255,255,0.95) !important;
      padding: 9px 13px;
      border-radius: 14px 14px 14px 5px;
      max-width: 158px;
      text-align: center;
      line-height: 1.55;
      direction: rtl;
      /* Gold accent border, soft shadow */
      box-shadow:
        0 4px 20px rgba(0,0,0,0.5),
        0 0 0 1.2px rgba(212,175,55,0.45) !important;
      /* Entrance bounce */
      animation:
        bubbleIn   0.55s cubic-bezier(0.34,1.56,0.64,1) 2.2s both,
        bubblePulse 3.8s ease-in-out 3.5s infinite;
    }
    /* Bubble tail pointing down-left toward the cat head */
    #cat-bubble::after {
      content: '';
      position: absolute;
      bottom: -7px;
      left: 18px;
      width: 0; height: 0;
      border-left:  7px solid transparent !important;
      border-right: 0   solid transparent !important;
      border-top:   8px solid rgba(255,255,255,0.95) !important;
    }
    @keyframes bubbleIn {
      from { opacity:0; transform:scale(0.65) translateY(8px); }
      to   { opacity:1; transform:scale(1)    translateY(0);   }
    }
    @keyframes bubblePulse {
      0%,100% { transform:scale(1); }
      50%      { transform:scale(1.025); }
    }

    /* ── Cat SVG ───────────────────────────────────────────────── */
    #velooria-cat-svg {
      width: 80px;
      height: 80px;
      margin-top: 5px;
      animation: catFloat 4s ease-in-out infinite;
      filter: drop-shadow(0 0 14px rgba(255,255,255,0.13));
      transition: transform 0.25s ease, filter 0.25s ease;
    }
    #cat-widget:hover #velooria-cat-svg {
      transform: scale(1.13) translateY(-3px);
      filter: drop-shadow(0 0 28px rgba(255,255,255,0.32));
      animation-play-state: paused;
    }
    #cat-widget:active #velooria-cat-svg { transform: scale(0.94); }

    @keyframes catFloat {
      0%,100% { transform:translateY(0px);  }
      50%      { transform:translateY(-7px); }
    }

    /* Tail, ear, eyes sub-animations */
    #cat-tail  { transform-origin:85% 70%; animation:tailWag 1.25s ease-in-out infinite; }
    @keyframes tailWag {
      0%  { transform:rotate(0deg);  }
      30% { transform:rotate(22deg); }
      70% { transform:rotate(-13deg);}
      100%{ transform:rotate(0deg);  }
    }
    #cat-ear-l { transform-origin:30% 20%; animation:earTwitch 6s ease-in-out infinite; }
    @keyframes earTwitch {
      0%,80%,100%{ transform:rotate(0deg);  }
      86%         { transform:rotate(-9deg); }
      92%         { transform:rotate(5deg);  }
    }
    #cat-eye-l, #cat-eye-r { animation:catBlink 5.5s ease-in-out infinite; transform-origin:center; }
    @keyframes catBlink {
      0%,85%,90%,100%{ transform:scaleY(1);    }
      87%             { transform:scaleY(0.07); }
    }

    /* Subtle WhatsApp hint on hover */
    #cat-widget::before {
      content: '▸ واتساب';
      font-family: 'Montserrat', sans-serif;
      font-size: 9px;
      letter-spacing: 1px;
      color: rgba(255,255,255,0) !important;
      position: absolute;
      bottom: -18px;
      right: 4px;
      transition: color 0.35s ease;
      pointer-events: none;
      white-space: nowrap;
    }
    #cat-widget:hover::before { color: rgba(255,255,255,0.40) !important; }
  </style>
</head>
<body>

  <div class="logo-fixed">VELOORIA</div>
  <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

  <!-- ══════════════════════════════════════════════════════════════
       🐱  CAT WIDGET  —  fixed bottom-right
       Click → meow sound → WhatsApp redirect
       Speech bubble in Arabic, Montserrat font
  ══════════════════════════════════════════════════════════════ -->
  <div id="cat-widget" role="button" aria-label="تواصل معانا على واتساب" tabindex="0">

    <!-- Arabic speech bubble (Montserrat, RTL) -->
    <div id="cat-bubble">إلى بغيتي تواصل معانا ورك عليا</div>

    <!-- Inline SVG cat — renders sharp on all devices, no external file needed -->
    <svg id="velooria-cat-svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">

      <!-- Tail (right side — mirrored from left version) -->
      <g id="cat-tail">
        <path d="M72 78 Q90 90 86 73 Q82 60 72 72"
              fill="rgba(255,255,255,0.85)"/>
      </g>

      <!-- Body -->
      <ellipse cx="50" cy="72" rx="26" ry="22" fill="rgba(255,255,255,0.91)"/>

      <!-- Head -->
      <ellipse cx="50" cy="44" rx="22" ry="20" fill="rgba(255,255,255,0.95)"/>

      <!-- Left ear (with twitch animation) -->
      <g id="cat-ear-l">
        <polygon points="30,30 36,14 44,28"  fill="rgba(255,255,255,0.95)"/>
        <polygon points="33,28 37,18 42,27"  fill="rgba(255,185,185,0.40)"/>
      </g>

      <!-- Right ear -->
      <polygon points="70,30 64,14 56,28"  fill="rgba(255,255,255,0.95)"/>
      <polygon points="67,28 63,18 58,27"  fill="rgba(255,185,185,0.40)"/>

      <!-- Left eye (with blink animation) -->
      <g id="cat-eye-l">
        <ellipse cx="42" cy="43" rx="4" ry="4.6" fill="rgba(15,15,15,0.90)"/>
        <ellipse cx="43.6" cy="41.4" rx="1.3" ry="1.3" fill="rgba(255,255,255,0.96)"/>
      </g>

      <!-- Right eye -->
      <g id="cat-eye-r">
        <ellipse cx="58" cy="43" rx="4" ry="4.6" fill="rgba(15,15,15,0.90)"/>
        <ellipse cx="59.6" cy="41.4" rx="1.3" ry="1.3" fill="rgba(255,255,255,0.96)"/>
      </g>

      <!-- Nose -->
      <polygon points="50,50 47.5,53 52.5,53" fill="rgba(255,150,150,0.78)"/>

      <!-- Mouth -->
      <path d="M47.5 53 Q50 57.5 52.5 53"
            stroke="rgba(100,50,50,0.55)" stroke-width="0.8" fill="none"/>

      <!-- Whiskers left -->
      <line x1="48" y1="51" x2="27" y2="48" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>
      <line x1="48" y1="53" x2="27" y2="53" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>
      <line x1="48" y1="55" x2="27" y2="58" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>

      <!-- Whiskers right -->
      <line x1="52" y1="51" x2="73" y2="48" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>
      <line x1="52" y1="53" x2="73" y2="53" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>
      <line x1="52" y1="55" x2="73" y2="58" stroke="rgba(210,210,210,0.55)" stroke-width="0.75"/>

      <!-- Paws -->
      <ellipse cx="35" cy="90" rx="7.5" ry="5" fill="rgba(255,255,255,0.88)"/>
      <ellipse cx="65" cy="90" rx="7.5" ry="5" fill="rgba(255,255,255,0.88)"/>

      <!-- Gold collar — Velooria brand accent -->
      <path d="M30 60 Q50 66 70 60"
            stroke="rgba(212,175,55,0.80)" stroke-width="3.8" fill="none" stroke-linecap="round"/>
      <!-- Collar gem -->
      <circle cx="50" cy="63" r="3.2" fill="rgba(212,175,55,0.93)"/>
      <circle cx="50" cy="63" r="1.6" fill="rgba(255,243,192,0.99)"/>
    </svg>

  </div><!-- /#cat-widget -->


  <!-- ══════════════════════════════════════════════════════════════
       PRODUCT SECTIONS — 100% unchanged from original
  ══════════════════════════════════════════════════════════════ -->

  <section class="product-section sauv-t" id="sec1">
    <div class="glow-center"></div>
    <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
    <div class="bottle-center">
      <img src="assets/sauvage-bottle.png" class="img-bottle">
      <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
      <div class="perfume-sub">EXTRAIT DE PARFUM</div>
    </div>
    <div class="row">
      <div class="img-box"><img src="assets/sauvage-detail-left.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>THE LEGENDARY DEPTH</h3>
        <p>Sauvage Elixir is an extraordinary concentration, a masterpiece of wild freshness. It intoxicates the senses with a custom-made heart of spices and a rich, woody trail that lingers long after you leave the room.</p>
      </div></div>
    </div>
    <div class="row rev">
      <div class="img-box"><img src="assets/sauvage-detail-right.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>OFFICIAL COMPOSITION</h3>
        <p><span class="highlight">Notes:</span> A powerful blend of Nutmeg, Cinnamon, and Cardamom, balanced perfectly by the freshness of Grapefruit and the warmth of Licorice.</p>
      </div></div>
    </div>
    <div class="purchase-area">
      <div style="flex:1">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:15px">
          <div><h4 style="font-family:'Cinzel'">SAUVAGE ELIXIR</h4><p style="color:#666;font-size:10px">10ML / 319 DH</p></div>
          <img src="assets/sauvage-thumb.png" class="mini-thumb">
        </div>
        <div class="size-container">
          <div class="size-box" onclick="selectSize(this,199,'sec1')">5ML<span>± 80 SPRAYS</span></div>
          <div class="size-box active-size" onclick="selectSize(this,319,'sec1')">10ML<span>± 160 SPRAYS</span></div>
        </div>
      </div>
      <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec1','SAUVAGE ELIXIR')">ORDER NOW | 319 DH</button></form></div>
    </div>
  </section>

  <section class="product-section stron-t" id="sec2">
    <div class="glow-center"></div>
    <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
    <div class="bottle-center">
      <img src="assets/stronger-bottle.png" class="img-bottle">
      <h1 class="brand-logo">STRONGER WITH YOU</h1>
      <div class="perfume-sub">EAU DE PARFUM</div>
    </div>
    <div class="row">
      <div class="img-box"><img src="assets/stronger-detail-left.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>MAGNETIC SENSUALITY</h3>
        <p>Stronger With You lives in the present, molded by the energy of modernity. Unpredictable, it surprises with its originality, like the spicy accord in the top notes—a mix of cardamom, pink peppercorn, and violet leaves.</p>
      </div></div>
    </div>
    <div class="row rev">
      <div class="img-box"><img src="assets/stronger-detail-right.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>OLFACTORY ARCHITECTURE</h3>
        <p><span class="highlight">Heart:</span> The aromatic heart consists of Sage and Lavender, bringing a confident elegance with the easy insouciance of youth, followed by a base of smoky Vanilla Jungle Essence.</p>
      </div></div>
    </div>
    <div class="purchase-area">
      <div style="flex:1">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:15px">
          <div><h4 style="font-family:'Cinzel'">STRONGER WITH YOU</h4><p style="color:#666;font-size:10px">10ML / 319 DH</p></div>
          <img src="assets/stronger-thumb.png" class="mini-thumb">
        </div>
        <div class="size-container">
          <div class="size-box" onclick="selectSize(this,199,'sec2')">5ML<span>± 80 SPRAYS</span></div>
          <div class="size-box active-size" onclick="selectSize(this,319,'sec2')">10ML<span>± 160 SPRAYS</span></div>
        </div>
      </div>
      <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec2','STRONGER WITH YOU')">ORDER NOW | 319 DH</button></form></div>
    </div>
  </section>

  <section class="product-section libre-t" id="sec3">
    <div class="glow-center"></div>
    <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
    <div class="bottle-center">
      <img src="assets/libre-bottle.png" class="img-bottle">
      <h1 class="brand-logo">LIBRE INTENSE</h1>
      <div class="perfume-sub">EAU DE PARFUM INTENSE</div>
    </div>
    <div class="row">
      <div class="img-box"><img src="assets/libre-detail-left.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>BORN TO BE WILD</h3>
        <p>The iconic structure of Libre, intensified. A burning floral duality, where the tension between French lavender and Moroccan orange blossom becomes even more excessive, enveloped in a creamy orchid accord.</p>
      </div></div>
    </div>
    <div class="row rev">
      <div class="img-box"><img src="assets/libre-detail-right.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>THE RAW ELEMENTS</h3>
        <p><span class="highlight">Base:</span> Madagascar Vanilla and Tonka Bean provide a dark, smoky depth that contrasts beautifully with the bright citrus top notes, creating a trail that is both fierce and feminine.</p>
      </div></div>
    </div>
    <div class="purchase-area">
      <div style="flex:1">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:15px">
          <div><h4 style="font-family:'Cinzel'">LIBRE INTENSE</h4><p style="color:#666;font-size:10px">10ML / 319 DH</p></div>
          <img src="assets/libre-thumb.png" class="mini-thumb">
        </div>
        <div class="size-container">
          <div class="size-box" onclick="selectSize(this,199,'sec3')">5ML<span>± 80 SPRAYS</span></div>
          <div class="size-box active-size" onclick="selectSize(this,319,'sec3')">10ML<span>± 160 SPRAYS</span></div>
        </div>
      </div>
      <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec3','LIBRE INTENSE')">ORDER NOW | 319 DH</button></form></div>
    </div>
  </section>

  <section class="product-section gg-t" id="sec4">
    <div class="glow-center"></div>
    <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
    <div class="bottle-center">
      <img src="assets/goodgirl-bottle.png" class="img-bottle">
      <h1 class="brand-logo">GOOD GIRL</h1>
      <div class="perfume-sub">EAU DE PARFUM</div>
    </div>
    <div class="row">
      <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>IT'S SO GOOD TO BE BAD</h3>
        <p>Inspired by the duality of the modern woman: audacious and sexy, elegant and enigmatic. Good Girl represents the complex vibrant world of femininity through a bold mix of dark and light elements.</p>
      </div></div>
    </div>
    <div class="row rev">
      <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
      <div class="txt-box"><div class="text-glow-free">
        <h3>OLFACTORY NOTES</h3>
        <p><span class="highlight">Heart:</span> The sweet qualities of Jasmine and Tuberose give the fragrance its brightness, while Roasted Tonka Bean and Cocoa provide the mysterious dark side that lasts all night.</p>
      </div></div>
    </div>
    <div class="purchase-area">
      <div style="flex:1">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:15px">
          <div><h4 style="font-family:'Cinzel'">GOOD GIRL</h4><p style="color:#666;font-size:10px">10ML / 319 DH</p></div>
          <img src="assets/gg-thumb.png" class="mini-thumb">
        </div>
        <div class="size-container">
          <div class="size-box" onclick="selectSize(this,199,'sec4')">5ML<span>± 80 SPRAYS</span></div>
          <div class="size-box active-size" onclick="selectSize(this,319,'sec4')">10ML<span>± 160 SPRAYS</span></div>
        </div>
      </div>
      <div style="flex:1.2"><form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec4','GOOD GIRL')">ORDER NOW | 319 DH</button></form></div>
    </div>
  </section>


  <!-- ══════════════════════════════════════════════════════════════
       ORDER + SCROLL LOGIC — 100% unchanged
  ══════════════════════════════════════════════════════════════ -->
  <script>
    function selectSize(element, price, sectionId) {
      const section = document.getElementById(sectionId);
      section.querySelectorAll('.size-box').forEach(b => b.classList.remove('active-size'));
      element.classList.add('active-size');
      section.querySelector('.order-btn').innerText = `ORDER NOW | ${price} DH`;
    }

    function sendOrder(sectionId, productName) {
      const section = document.getElementById(sectionId);
      const name  = section.querySelector('input[name="name"]').value;
      const phone = section.querySelector('input[name="phone"]').value;
      const city  = section.querySelector('input[name="city"]').value;
      const size  = section.querySelector('.active-size').innerText.split('\n')[0];
      const price = section.querySelector('.order-btn').innerText.split('|')[1].trim();
      if(!name||!phone||!city){ alert("عافاك عمر المعلومات كاملة"); return; }
      const botToken = "8751066528:AAFJOYkbqi3bSxncJh4tKSQeH_0wCT660ps";
      const chatId   = "7635707772";
      const message  = `🚀 *طلب جديد: Velooria Beauty*\n\n📦 *المنتوج:* ${productName}\n📏 *القياس:* ${size}\n💰 *الثمن:* ${price}\n--------------------------\n👤 *الاسم:* ${name}\n📞 *الهاتف:* ${phone}\n📍 *المدينة:* ${city}\n\n✅ يونس، كليان جديد كيتسناك!`;
      fetch(`https://api.telegram.org/bot${botToken}/sendMessage`,{
        method:'POST', headers:{'Content-Type':'application/json'},
        body: JSON.stringify({chat_id:chatId,text:message,parse_mode:'Markdown'})
      })
      .then(()=>{ alert("شكراً! تم إرسال طلبك بنجاح."); section.querySelector('form').reset(); })
      .catch(()=> alert("وقع مشكل فالاتصال، حاول مرة أخرى."));
    }

    const sections = ['sec1','sec2','sec3','sec4'];
    const colors   = ['#4A90E2','#CD7F32','#D4AF37','#1a4d99'];
    let currentIdx = 0;
    const scrollBtn = document.getElementById('scrollBtn');
    const arrow     = scrollBtn.querySelector('.arrow-icon');

    window.addEventListener('scroll', () => {
      sections.forEach((id,index) => {
        const rect = document.getElementById(id).getBoundingClientRect();
        if(rect.top >= -window.innerHeight/2 && rect.top <= window.innerHeight/2){
          currentIdx = index;
          document.documentElement.style.setProperty('--current-arrow-color', colors[index]);
          if(currentIdx === sections.length-1){
            arrow.classList.add('arrow-up');
            arrow.style.animation = "bounce-up 2s infinite";
          } else {
            arrow.classList.remove('arrow-up');
            arrow.style.animation = "bounce 2s infinite";
          }
        }
      });
    });

    scrollBtn.onclick = () => {
      if(currentIdx === sections.length-1) window.scrollTo({top:0,behavior:'smooth'});
      else document.getElementById(sections[currentIdx+1]).scrollIntoView({behavior:'smooth'});
    };
  </script>


  <!-- ══════════════════════════════════════════════════════════════
       🔊  VELOORIA AUDIO ENGINE  —  Web Audio API (zero external files)
       ──────────────────────────────────────────────────────────────

       BRAND SOUND  (fires on first user interaction: click or scroll)
       ┌─ Phase 1 : HD Perfume Spray  (0 → 0.32s)
       │   Two-layer pink-noise synthesis:
       │   • Layer A — tight band 8.8kHz → 1.4kHz: the compressed gas hiss
       │   • Layer B — wide  band 3.2kHz → 600Hz:  the wet mist body
       │   Both with snap attack (6–10ms) + exponential decay.
       │   Feeds through a DynamicsCompressor for broadcast clarity.
       │
       └─ Phase 2 : Luxury Chime  (starts 0.20s, sustains ~2s)
           Tuned to E-major (evokes prestige, clarity — Chanel/Dior aesthetic):
           • E4  (330 Hz) triangle  — warm sub-undertone / depth
           • E5  (659 Hz) sine      — root / clean iconic note
           • B5  (988 Hz) sine      — perfect fifth / floating harmony
           • E7 (2637 Hz) sine      — crystal shimmer / luxury sparkle
           • E5+2¢ twin             — subtle stereo width on speakers
           Each tone: gentle attack + piano-style exponential decay.
           Micro-LFO shimmer on every oscillator (≤0.25% freq deviation).

       MEOW SOUND  (only on cat click — never on brand-sound trigger)
       • FM sine carrier following real-cat F0 contour:
         640 Hz → 920 Hz → 570 Hz over 260 ms
       • Low-frequency modulator (180→260 Hz) adds vocal "mrrr" texture
       • Peaking filter at 1100 Hz = vowel formant = "sounds like a real cat"
       • Cute and clean — not cartoon, not harsh
  ══════════════════════════════════════════════════════════════ -->
  <script>
    /* ── Shared AudioContext — created lazily inside a gesture ── */
    let _ctx        = null;
    let brandPlayed = false;

    function getCtx() {
      if (!_ctx) _ctx = new (window.AudioContext || window.webkitAudioContext)();
      return _ctx;
    }

    /* ══════════════════════════════════════════════════════════
       BRAND SOUND
    ══════════════════════════════════════════════════════════ */
    function playBrandSound() {
      if (brandPlayed) return;
      brandPlayed = true;

      const ctx = getCtx();
      const now = ctx.currentTime;

      /* Compressor — keeps the whole sound even and hi-fi */
      const comp = ctx.createDynamicsCompressor();
      comp.threshold.value = -20;
      comp.knee.value      =  8;
      comp.ratio.value     =  4;
      comp.attack.value    =  0.003;
      comp.release.value   =  0.22;
      comp.connect(ctx.destination);

      const master = ctx.createGain();
      master.gain.value = 0.62;
      master.connect(comp);

      /* ── Helper: pink-ish noise buffer ─────────────────────
         Average 3 random values per sample → gentle high-freq roll-off
         (sounds denser and more "real" than pure white noise)
      ─────────────────────────────────────────────────────── */
      function makePinkNoise(secs) {
        const len = Math.ceil(ctx.sampleRate * secs);
        const buf = ctx.createBuffer(1, len, ctx.sampleRate);
        const d   = buf.getChannelData(0);
        for (let i = 0; i < len; i++)
          d[i] = (Math.random() + Math.random() + Math.random()) / 3 * 2 - 1;
        const src = ctx.createBufferSource();
        src.buffer = buf;
        return src;
      }

      /* Layer A — compressed gas hiss */
      const nA  = makePinkNoise(0.36);
      const fA  = ctx.createBiquadFilter();
      fA.type   = 'bandpass';
      fA.frequency.setValueAtTime(8800, now);
      fA.frequency.exponentialRampToValueAtTime(1400, now + 0.30);
      fA.Q.value = 1.5;
      const gA  = ctx.createGain();
      gA.gain.setValueAtTime(0,    now);
      gA.gain.linearRampToValueAtTime(1.0,  now + 0.006); // snap
      gA.gain.exponentialRampToValueAtTime(0.001, now + 0.30);
      nA.connect(fA); fA.connect(gA); gA.connect(master);
      nA.start(now); nA.stop(now + 0.36);

      /* Layer B — wet mist body */
      const nB  = makePinkNoise(0.40);
      const fB  = ctx.createBiquadFilter();
      fB.type   = 'bandpass';
      fB.frequency.setValueAtTime(3200, now);
      fB.frequency.exponentialRampToValueAtTime(550, now + 0.33);
      fB.Q.value = 0.60;
      const gB  = ctx.createGain();
      gB.gain.setValueAtTime(0,    now);
      gB.gain.linearRampToValueAtTime(0.48, now + 0.010);
      gB.gain.exponentialRampToValueAtTime(0.001, now + 0.33);
      nB.connect(fB); fB.connect(gB); gB.connect(master);
      nB.start(now); nB.stop(now + 0.40);

      /* ── Helper: one chime tone ─────────────────────────────
         freq      — pitch in Hz
         startT    — when to begin
         peak      — max gain (0–1)
         attack    — rise time in seconds
         hold      — flat sustain in seconds
         decay     — fall time in seconds
         oscType   — 'sine' | 'triangle'
      ─────────────────────────────────────────────────────── */
      function chimeTone(freq, startT, peak, attack, hold, decay, oscType) {
        const osc  = ctx.createOscillator();
        const gain = ctx.createGain();
        osc.type            = oscType || 'sine';
        osc.frequency.value = freq;

        /* Micro-LFO: adds organic "aliveness" without audible vibrato */
        const lfo     = ctx.createOscillator();
        const lfoGain = ctx.createGain();
        lfo.type            = 'sine';
        lfo.frequency.value = 5.0 + Math.random() * 2.0; // 5–7 Hz, random per tone
        lfoGain.gain.value  = freq * 0.0020;              // ≤0.20% frequency deviation
        lfo.connect(lfoGain); lfoGain.connect(osc.frequency);
        lfo.start(startT); lfo.stop(startT + attack + hold + decay + 0.1);

        /* Piano-style ADSR */
        gain.gain.setValueAtTime(0, startT);
        gain.gain.linearRampToValueAtTime(peak,  startT + attack);
        gain.gain.setValueAtTime(peak,            startT + attack + hold);
        gain.gain.exponentialRampToValueAtTime(0.001, startT + attack + hold + decay);

        osc.connect(gain); gain.connect(master);
        osc.start(startT); osc.stop(startT + attack + hold + decay + 0.1);
      }

      const cs = now + 0.20; // chime starts just before spray tail ends

      /* Warm depth undertone */
      chimeTone(329.63, cs,         0.16, 0.020, 0.01, 1.70, 'triangle'); // E4

      /* Iconic root */
      chimeTone(659.25, cs,         0.52, 0.012, 0.02, 1.50, 'sine');     // E5

      /* Floating fifth */
      chimeTone(987.77, cs + 0.055, 0.36, 0.014, 0.02, 1.30, 'sine');     // B5

      /* Crystal shimmer */
      chimeTone(2637.0, cs + 0.105, 0.10, 0.008, 0.01, 0.80, 'sine');     // E7

      /* Detuned twin for stereo width (+2 cents ≈ ×1.00116) */
      chimeTone(659.25 * 1.00116, cs + 0.004, 0.25, 0.012, 0.02, 1.40, 'sine');
    }

    /* ══════════════════════════════════════════════════════════
       MEOW SOUND  —  FM synthesis, cat vocal contour
    ══════════════════════════════════════════════════════════ */
    function playMeow() {
      const ctx = getCtx();
      const now = ctx.currentTime;

      const master = ctx.createGain();
      master.gain.value = 0.52;
      master.connect(ctx.destination);

      /* Carrier — follows real-cat fundamental frequency path */
      const carrier = ctx.createOscillator();
      carrier.type  = 'sine';
      carrier.frequency.setValueAtTime(640,  now);
      carrier.frequency.linearRampToValueAtTime(920,  now + 0.10); // rise
      carrier.frequency.exponentialRampToValueAtTime(570, now + 0.26); // fall

      /* Modulator — low-frequency FM adds "mrrr" texture */
      const mod     = ctx.createOscillator();
      const modGain = ctx.createGain();
      mod.type  = 'sine';
      mod.frequency.setValueAtTime(175, now);
      mod.frequency.linearRampToValueAtTime(255, now + 0.11);
      modGain.gain.setValueAtTime(52,  now);
      modGain.gain.linearRampToValueAtTime(78,  now + 0.10);
      modGain.gain.exponentialRampToValueAtTime(8, now + 0.26);
      mod.connect(modGain); modGain.connect(carrier.frequency);

      /* Amplitude envelope */
      const env = ctx.createGain();
      env.gain.setValueAtTime(0,   now);
      env.gain.linearRampToValueAtTime(1.0, now + 0.022);   // quick onset
      env.gain.setValueAtTime(1.0,          now + 0.082);
      env.gain.exponentialRampToValueAtTime(0.001, now + 0.27); // smooth tail

      /* Formant filter — vowel resonance keeps it sounding like a cat */
      const formant       = ctx.createBiquadFilter();
      formant.type        = 'peaking';
      formant.frequency.value = 1100;
      formant.gain.value  =  6;
      formant.Q.value     =  1.8;

      carrier.connect(formant);
      formant.connect(env);
      env.connect(master);

      mod.start(now);     mod.stop(now + 0.30);
      carrier.start(now); carrier.stop(now + 0.30);
    }

    /* ══════════════════════════════════════════════════════════
       EVENT BINDINGS
    ══════════════════════════════════════════════════════════ */

    /* Brand sound — fires on FIRST click or FIRST scroll anywhere */
    function onFirstInteraction() {
      playBrandSound();
      document.removeEventListener('click',  onFirstInteraction);
      document.removeEventListener('scroll', onFirstScrollInteraction);
    }
    function onFirstScrollInteraction() {
      playBrandSound();
      document.removeEventListener('click',  onFirstInteraction);
      document.removeEventListener('scroll', onFirstScrollInteraction);
    }
    document.addEventListener('click',  onFirstInteraction);
    document.addEventListener('scroll', onFirstScrollInteraction, { passive: true });

    /* Cat widget — meow then WhatsApp */
    const catWidget = document.getElementById('cat-widget');

    catWidget.addEventListener('click', function(e) {
      e.stopPropagation(); // prevent triggering brand sound again

      /* Edge case: cat is the very first interaction — play brand sound too */
      if (!brandPlayed) playBrandSound();

      /* Meow */
      playMeow();

      /* Redirect to WhatsApp after meow completes (~300ms) */
      setTimeout(() => window.open('https://wa.me/212691444558', '_blank'), 320);
    });

    /* Keyboard accessibility */
    catWidget.addEventListener('keydown', e => {
      if (e.key === 'Enter' || e.key === ' ') catWidget.click();
    });

    /* Cat fades in 1.5s after page load */
    setTimeout(() => catWidget.classList.add('cat-visible'), 1500);
  </script>


  <!-- ══════════════════════════════════════════════════════════════
       🤖  TYPEBOT  —  100% unchanged  (placement:"left" = no overlap with cat)
  ══════════════════════════════════════════════════════════════ -->
  <script type="module">
    import Typebot from 'https://cdn.jsdelivr.net/npm/@typebot.io/js@0/dist/web.js';
    Typebot.initBubble({
      typebot: "my-typebot-v5y1jji",
      previewMessage: { message: "مرحباً بيك! محتاجة مساعدة في اختيار عطر؟" },
      theme: {
        placement: "left",
        button: {
          backgroundColor: "#1D1D1D",
          customIconSrc: "https://s3.typebotstorage.com/public/workspaces/cmo1ozjlf000006jon0c0dnhf/typebots/cmo25o37s000007mi2v5y1jji/bubble-icon?v=1776539635531",
          size: "large",
        },
        chatWindow: { backgroundColor: "#171923" },
      },
    });
  </script>

</body>
</html>

