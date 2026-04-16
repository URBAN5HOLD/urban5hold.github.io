<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Official Luxury Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { 
            margin: 0; padding: 0; box-sizing: border-box; 
            text-decoration: none !important;
            -webkit-tap-highlight-color: transparent;
        }

        html, body { 
            width: 100%; background-color: #000 !important; 
            scroll-snap-type: y mandatory; scroll-behavior: smooth; 
            font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden;
        }

        .logo-fixed { 
            position: fixed; top: 0; left: 0; width: 100%; 
            background-color: #000 !important; padding: 25px 0; 
            z-index: 10000; font-family: 'Cinzel', serif; 
            font-size: 1.2rem; letter-spacing: 10px; color: #fff !important; 
            text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.5);
        }

        .scroll-trigger { 
            position: fixed; bottom: 45%; right: 15px; 
            width: 50px; height: 50px; z-index: 10001; 
            cursor: pointer; display: flex; align-items: center; justify-content: center;
            background: rgba(255,255,255,0.1); border-radius: 50%;
        }
        
        .arrow-icon { 
            width: 15px; height: 15px; 
            border-right: 3px solid var(--current-arrow-color, #fff); 
            border-bottom: 3px solid var(--current-arrow-color, #fff); 
            transform: rotate(45deg); transition: all 0.5s ease;
            animation: bounce 2s infinite;
        }
        .arrow-up { transform: rotate(-135deg) !important; }

        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }
        @keyframes bounce-up { 0%, 100% { transform: translateY(5px) rotate(-135deg); } 50% { transform: translateY(-5px) rotate(-135deg); } }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 40px 0; position: relative; z-index: 2; }
        .img-bottle { width: 100%; max-width: 160px; height: 250px; object-fit: contain; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }

        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff !important; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        .purchase-area { max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 40px; border-top: 1px solid rgba(255,255,255,0.1); width: 90%; position: relative; z-index: 2; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2); text-align: center; cursor: pointer; color: #fff; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05) !important; }

        .purchase-area input { 
            width: 100%; padding: 15px; margin-bottom: 10px; 
            background: rgba(255,255,255,0.05) !important; 
            border: 1px solid rgba(255,255,255,0.1) !important; 
            color: #fff !important; font-family: 'Montserrat';
        }
        .order-btn { width: 100%; padding: 20px; background: #fff !important; color: #000 !important; font-weight: 800; cursor: pointer; border: none; }

        /* Themes */
        .sauv-t { --color: #4A90E2; }
        .stron-t { --color: #CD7F32; }
        .libre-t { --color: #D4AF37; }
        .gg-t { --color: #1a4d99; }

        /* Chatbot Style */
        #chat-trigger { position: fixed; bottom: 20px; left: 20px; width: 60px; height: 60px; background: #fff; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; z-index: 10005; box-shadow: 0 4px 15px rgba(0,0,0,0.3); }
        #chat-window { display: none; position: fixed; bottom: 90px; left: 20px; width: 320px; height: 450px; background: #000; border: 1px solid #333; border-radius: 15px; flex-direction: column; z-index: 10005; overflow: hidden; }
        #chat-msgs { flex: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; gap: 10px; }
        .msg-ai { background: #222; padding: 10px; border-radius: 10px; align-self: flex-start; font-size: 0.85rem; max-width: 85%; }
        .msg-user { background: #fff; color: #000; padding: 10px; border-radius: 10px; align-self: flex-end; font-size: 0.85rem; max-width: 85%; }
        .chat-input-area { padding: 10px; border-top: 1px solid #333; display: flex; background: #111; gap: 5px; }
        .chat-input-area input { flex: 1; background: transparent; border: 1px solid #333 !important; color: #fff; padding: 8px; border-radius: 5px; outline: none; }
        .chat-input-area button { background: #fff; color: #000; border: none; padding: 8px 15px; border-radius: 5px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; gap:10px;">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML</div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML</div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec1', 'SAUVAGE ELIXIR')">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <div id="chat-trigger"><img src="https://cdn-icons-png.flaticon.com/512/134/134914.png" width="30" style="filter: invert(1);"></div>
    <div id="chat-window">
        <div style="background: #fff; color: #000; padding: 15px; font-weight: bold; display: flex; justify-content: space-between;">
            <span>VELOORIA AI</span>
            <span id="close-chat" style="cursor: pointer;">✕</span>
        </div>
        <div id="chat-msgs">
            <div class="msg-ai">أهلاً بك فـ Velooria! ✨ كيف نقدر نعاونك؟</div>
        </div>
        <div class="chat-input-area">
            <input id="chat-input" type="text" placeholder="كتب ميساج...">
            <button id="send-btn">صيفط</button>
        </div>
    </div>

    <script>
        // Settings
        const API_KEY = "AIzaSyDNR5p5cQYntUfOBM4ox9E_th2ZNWJ0awl";
        const BOT_TOKEN = "8751066528:AAG3zm-hNENKPnAqEAHb1zBsFVSB6mVatT8";
        const CHAT_ID = "7635707772";

        // 1. Scrolling Logic
        const sections = ['sec1']; // ضيف sec2, sec3... هنا
        let currentIdx = 0;

        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -window.innerHeight/2 && rect.top <= window.innerHeight/2) {
                    currentIdx = index;
                }
            });
        });

        document.getElementById('scrollBtn').onclick = () => {
            if(currentIdx === sections.length - 1) window.scrollTo({top: 0, behavior: 'smooth'});
            else window.scrollTo({top: document.getElementById(sections[currentIdx+1]).offsetTop - 70, behavior: 'smooth'});
        };

        function selectSize(el, price, secId) {
            const sec = document.getElementById(secId);
            sec.querySelectorAll('.size-box').forEach(b => b.classList.remove('active-size'));
            el.classList.add('active-size');
            sec.querySelector('.order-btn').innerText = `ORDER NOW | ${price} DH`;
        }

        // 2. Chatbot Logic
        const trigger = document.getElementById('chat-trigger');
        const windowChat = document.getElementById('chat-window');
        const input = document.getElementById('chat-input');
        const send = document.getElementById('send-btn');
        const msgs = document.getElementById('chat-msgs');

        trigger.onclick = () => windowChat.style.display = windowChat.style.display === 'none' ? 'flex' : 'none';
        document.getElementById('close-chat').onclick = () => windowChat.style.display = 'none';

        async function getAI(text) {
            try {
                const r = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${API_KEY}`, {
                    method: 'POST',
                    headers: {'Content-Type': 'application/json'},
                    body: JSON.stringify({ contents: [{ parts: [{ text: "أنت بائع عطور في متجر Velooria. جاوب بالدارجة المغربية فقط باختصار.\nUser: " + text }] }] })
                });
                const d = await r.json();
                return d.candidates[0].content.parts[0].text;
            } catch(e) { return "وقع مشكل فالاتصال، عاود صيفط."; }
        }

        send.onclick = async () => {
            const val = input.value.trim();
            if(!val) return;

            msgs.innerHTML += `<div class="msg-user">${val}</div>`;
            input.value = "";
            
            const aiMsg = await getAI(val);
            msgs.innerHTML += `<div class="msg-ai">${aiMsg}</div>`;
            msgs.scrollTop = msgs.scrollHeight;

            if (/(06|07|05)\d{8}/.test(val)) {
                fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
                    method: 'POST',
                    headers: {'Content-Type': 'application/json'},
                    body: JSON.stringify({ chat_id: CHAT_ID, text: `💬 ميساج جديد فيه رقم: ${val}` })
                });
            }
        };
    </script>
</body>
</html>
