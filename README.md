<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub | Ultimate Tourist Guide & Booking</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { 
            --primary: #10b981; 
            --accent: #fbbf24; 
            --bg: #020617; 
            --card: rgba(255, 255, 255, 0.05); 
            --glass: blur(20px); 
            --text: #f8fafc; 
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        /* --- Loader --- */
        #loader { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: 0.6s; }
        @keyframes spin { to { transform: rotate(360deg); } }

        /* --- Header --- */
        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.85); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .lang-btn { background: var(--card); border: 1px solid var(--primary); color: var(--primary); padding: 6px 15px; border-radius: 12px; font-size: 0.75rem; font-weight: 800; cursor: pointer; }

        /* --- Hero Slider --- */
        .hero { height: 25vh; margin: 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 20s infinite ease-in-out; }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        /* --- Action Cards (Help & Book) --- */
        .action-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; padding: 10px 20px; }
        .action-card { background: var(--card); border-radius: 22px; padding: 20px 10px; text-align: center; border: 1px solid rgba(255,255,255,0.05); cursor: pointer; transition: 0.3s; }
        .action-card.book { background: linear-gradient(135deg, #064e3b, #020617); border-color: var(--primary); }
        .action-card i { font-size: 1.8rem; margin-bottom: 8px; display: block; }
        .action-card.help i { color: var(--accent); }
        .action-card.book i { color: var(--primary); }
        .action-card h3 { font-size: 0.9rem; margin-bottom: 4px; }
        .action-card p { font-size: 0.65rem; opacity: 0.6; }

        /* --- Places Section --- */
        .section-title { padding: 15px 20px 5px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 8px; }
        .section-title i { color: var(--primary); }

        .places-list { padding: 10px 20px; }
        .place-card { background: var(--card); border-radius: 18px; margin-bottom: 12px; padding: 15px; border: 1px solid rgba(255,255,255,0.03); cursor: pointer; transition: 0.3s; }
        .place-card h4 { color: var(--accent); display: flex; justify-content: space-between; align-items: center; font-size: 0.95rem; }
        .place-card .dist { font-size: 0.7rem; background: rgba(16, 185, 129, 0.1); color: var(--primary); padding: 3px 8px; border-radius: 6px; }
        .place-desc { max-height: 0; overflow: hidden; transition: 0.4s ease; font-size: 0.8rem; opacity: 0.7; line-height: 1.5; padding-top: 0; }
        .place-card.active { border-color: var(--primary); background: rgba(255,255,255,0.08); }
        .place-card.active .place-desc { max-height: 200px; padding-top: 12px; margin-top: 10px; border-top: 1px solid rgba(255,255,255,0.05); }

        /* --- Service Modal --- */
        .modal-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.85); backdrop-filter: blur(5px); z-index: 1500; display: none; }
        .modal-overlay.active { display: block; }
        .booking-modal { position: fixed; bottom: -100%; left: 0; right: 0; background: #0f172a; border-radius: 30px 30px 0 0; padding: 35px 20px; z-index: 2000; transition: 0.5s cubic-bezier(0.4, 0, 0.2, 1); border-top: 2px solid var(--primary); }
        .booking-modal.active { bottom: 0; }
        .svc-item { background: var(--card); border: 1px solid rgba(255,255,255,0.05); padding: 18px; border-radius: 18px; margin-bottom: 12px; display: flex; align-items: center; gap: 15px; color: white; text-decoration: none; transition: 0.2s; }
        .svc-item:active { transform: scale(0.96); background: rgba(16, 185, 129, 0.1); }
        .svc-item i { color: var(--primary); font-size: 1.3rem; width: 25px; }

        /* --- Footer Nav --- */
        .bottom-nav { position: fixed; bottom: 15px; left: 15px; right: 15px; background: rgba(255,255,255,0.08); backdrop-filter: blur(25px); display: flex; justify-content: space-around; padding: 16px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-link { color: rgba(255,255,255,0.4); font-size: 1.4rem; text-decoration: none; }
        .nav-link.active { color: var(--primary); }

        .sos-btn { position: fixed; bottom: 95px; right: 20px; background: #ef4444; width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; box-shadow: 0 10px 20px rgba(239, 68, 68, 0.4); z-index: 900; text-decoration: none; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
    </style>
</head>
<body>

<div id="loader">
    <div style="width:45px; height:45px; border:4px solid var(--card); border-top-color:var(--primary); border-radius:50%; animation:spin 1s linear infinite"></div>
    <p style="margin-top:20px; font-weight:800; letter-spacing:3px; font-size:0.7rem;">ASTORE MASTER HUB</p>
</div>

<header>
    <div id="brand" style="font-weight: 800; font-size: 1.2rem;">ASTORE <span style="color:var(--primary)">HUB PRO</span></div>
    <button class="lang-btn" onclick="toggleLang()">URDU</button>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
    </div>
</section>

<div class="action-grid">
    <div class="action-card help" onclick="directContact('Help Desk / Information')">
        <i class="fa-solid fa-circle-question"></i>
        <h3 id="t-h1">Help Desk</h3>
        <p id="t-p1">Inquiry & Info</p>
    </div>
    <div class="action-card book" onclick="toggleModal(true)">
        <i class="fa-solid fa-bolt"></i>
        <h3 id="t-h2">Quick Book</h3>
        <p id="t-p2">Cars & Hotels</p>
    </div>
</div>

<div class="section-title"><i class="fa-solid fa-map-location-dot"></i> <span id="t-explore">Explore Astore Valley</span></div>

<div class="places-list">
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Rama Meadows <span class="dist">11 KM</span></h4>
        <div class="place-desc" id="d1">Rama Meadows Astore ki sab se haseen jagah hai. Yahan ghane jungle aur rasta asaan hai. Rama Lake tak janay ke liye 1 ghanta trek ya ghora (horse) mil jata hai.</div>
    </div>
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Minimarg & Rainbow Lake <span class="dist">65 KM</span></h4>
        <div class="place-desc" id="d2">Jannat-e-Benazir! Yahan Rainbow Lake mashhoor hai. Burzil Pass cross karna hota hai. Army post par CNIC dikhana lazmi hai. June se August behtreen waqt hai.</div>
    </div>
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Deosai Plains <span class="dist">45 KM</span></h4>
        <div class="place-desc" id="d3">Dunya ka doosra buland tareen maidan. Chilam Chowki se rasta shuru hota hai. Yahan wild life aur khubsurat phool dekhne ko milte hain.</div>
    </div>
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Gorikot Hub <span class="dist">12 KM</span></h4>
        <div class="place-desc" id="d4">Ye Astore ka main junction hai. Yahan se rasta ramma aur minimarg ke liye divide hota hai. Hotels aur market ke liye ye best base camp hai.</div>
    </div>
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Rupal Face <span class="dist">55 KM</span></h4>
        <div class="place-desc" id="d5">Nanga Parbat ka sab se bara face. Trekkers ke liye ye aik challenge aur adventure hai. Tarishing village se ye safar shuru hota hai.</div>
    </div>
    <div class="place-card" onclick="this.classList.toggle('active')">
        <h4>Gudai Valley <span class="dist">30 KM</span></h4>
        <div class="place-desc" id="d6">Minimarg ke raste mein ane wali khubsurat waadi. Yahan ka thanda pani aur local ghar tourists ke liye pur-kashish hain.</div>
    </div>
</div>

<div class="modal-overlay" id="overlay" onclick="toggleModal(false)"></div>
<div class="booking-modal" id="bookModal">
    <h2 style="margin-bottom:20px; text-align:center; font-weight:800;">Select Booking Service ⚡</h2>
    <a href="#" class="svc-item" onclick="directContact('Hotel Booking Request')">
        <i class="fa-solid fa-hotel"></i> <span>Book Best Hotel</span>
    </a>
    <a href="#" class="svc-item" onclick="directContact('4x4 Jeep Rental Request')">
        <i class="fa-solid fa-truck-monster"></i> <span>Rent 4x4 Jeep</span>
    </a>
    <a href="#" class="svc-item" onclick="directContact('Full Tour Package Inquiry')">
        <i class="fa-solid fa-suitcase-rolling"></i> <span>Full Tour Package</span>
    </a>
    <button onclick="toggleModal(false)" style="width:100%; padding:18px; border-radius:18px; border:none; background:rgba(255,255,255,0.05); color:white; font-weight:800; margin-top:10px;">Cancel</button>
</div>

<a href="tel:1122" class="sos-btn"><i class="fa-solid fa-truck-medical"></i></a>

<div style="height: 110px;"></div>

<nav class="bottom-nav">
    <a href="#" class="nav-link active"><i class="fa-solid fa-house"></i></a>
    <a href="tel:923171588489" class="nav-link"><i class="fa-solid fa-headset"></i></a>
    <a href="#" class="nav-link" onclick="alert('Network Alert: SCOM is active in Minimarg. Carry Cash!')"><i class="fa-solid fa-tower-cell"></i></a>
</nav>

<script>
    // --- Loader Logic ---
    window.addEventListener('load', () => {
        setTimeout(() => {
            const l = document.getElementById('loader');
            l.style.opacity = '0';
            setTimeout(() => l.style.display = 'none', 600);
        }, 1500);
    });

    // --- Interaction Logic ---
    function toggleModal(show) {
        const m = document.getElementById('bookModal');
        const o = document.getElementById('overlay');
        if(show) {
            m.classList.add('active');
            o.classList.add('active');
        } else {
            m.classList.remove('active');
            o.classList.remove('active');
        }
    }

    function directContact(svc) {
        const msg = encodeURIComponent(`*Astore Hub Official Inquiry*\n---\n*Service Requested:* ${svc}\n*Status:* Ready to Plan`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }

    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        const btn = document.querySelector('.lang-btn');
        const h1 = document.getElementById('t-h1');
        const p1 = document.getElementById('t-p1');
        const h2 = document.getElementById('t-h2');
        const p2 = document.getElementById('t-p2');
        const exp = document.getElementById('t-explore');

        if(isUrdu) {
            btn.innerText = "ENGLISH";
            h1.innerText = "مددگار مرکز";
            p1.innerText = "معلومات اور سوالات";
            h2.innerText = "فوری بکنگ";
            p2.innerText = "گاڑی اور ہوٹل";
            exp.innerText = "استور کی سیر کریں";
            document.getElementById('brand').innerHTML = 'استور <span style="color:var(--primary)">ہب پرو</span>';
            document.getElementById('d1').innerText = "راما میڈوز استور کی سب سے حسین جگہ ہے۔ یہاں گھنے جنگل اور راستہ آسان ہے۔ جھیل تک جانے کے لیے ٹریکنگ کرنی پڑتی ہے۔";
            document.getElementById('d2').innerText = "منی مرگ اور رینبو لیک کے لیے شناختی کارڈ ساتھ رکھنا لازمی ہے۔ یہ علاقہ اپنی ہریالی کے لیے مشہور ہے۔";
            document.getElementById('d3').innerText = "دیوسائی دنیا کا بلند ترین میدان ہے۔ یہاں کے مناظر اور خاموشی سیاحوں کو بہت پسند آتی ہے۔";
        } else {
            btn.innerText = "URDU";
            h1.innerText = "Help Desk";
            p1.innerText = "Inquiry & Info";
            h2.innerText = "Quick Book";
            p2.innerText = "Cars & Hotels";
            exp.innerText = "Explore Astore Valley";
            document.getElementById('brand').innerHTML = 'ASTORE <span style="color:var(--primary)">HUB PRO</span>';
            document.getElementById('d1').innerText = "Rama Meadows is a beautiful pine-forested valley. Easy access and great for family camping.";
            document.getElementById('d2').innerText = "Minimarg is home to Rainbow Lake. CNIC is mandatory for entry via Burzil Pass.";
            document.getElementById('d3').innerText = "Deosai is the second highest plateau in the world. Famous for wildlife and flora.";
        }
    }
</script>

</body>
</html>
