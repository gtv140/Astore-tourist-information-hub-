<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub Pro | Pure Experience</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #10b981; --accent: #fbbf24; --bg: #020617; --card: rgba(255, 255, 255, 0.05); --glass: blur(15px); --text: #f8fafc; }
        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        #loader { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: 0.6s; }
        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.85); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .lang-btn { background: var(--card); border: 1px solid var(--primary); color: var(--primary); padding: 6px 15px; border-radius: 12px; font-size: 0.75rem; font-weight: 800; cursor: pointer; }

        .hero { height: 25vh; margin: 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 20s infinite ease-in-out; }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        .section-title { padding: 15px 20px 5px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 8px; color: var(--primary); }
        
        /* Interactive Grid */
        .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; padding: 10px 20px; }
        .grid-item { background: var(--card); padding: 20px; border-radius: 20px; text-align: center; border: 1px solid rgba(255,255,255,0.05); cursor: pointer; }
        .grid-item i { font-size: 1.8rem; color: var(--primary); margin-bottom: 10px; display: block; }
        .grid-item span { font-size: 0.8rem; font-weight: 700; }
        .grid-item.active { background: rgba(16, 185, 129, 0.15); border-color: var(--primary); transform: scale(0.95); }

        /* Places Accordion */
        .details-list { margin: 10px 20px; }
        .detail-item { background: var(--card); border-radius: 15px; margin-bottom: 10px; overflow: hidden; border: 1px solid rgba(255,255,255,0.05); }
        .detail-header { padding: 15px; display: flex; justify-content: space-between; align-items: center; cursor: pointer; font-size: 0.85rem; font-weight: 600; color: var(--accent); }
        .detail-content { padding: 0 15px; max-height: 0; overflow: hidden; transition: 0.3s ease; font-size: 0.8rem; opacity: 0.7; line-height: 1.5; }
        .detail-item.open .detail-content { padding: 0 15px 15px; max-height: 200px; }
        .detail-item.open i.fa-chevron-down { transform: rotate(180deg); color: var(--primary); }

        /* Booking CTA */
        .booking-cta { margin: 25px 20px; background: linear-gradient(135deg, #064e3b, #020617); padding: 30px 20px; border-radius: 35px; border: 1px solid var(--primary); text-align: center; }
        .btn-main { background: var(--primary); color: white; border: none; padding: 18px; border-radius: 20px; width: 100%; font-weight: 800; font-size: 1rem; display: flex; align-items: center; justify-content: center; gap: 12px; margin-top: 20px; cursor: pointer; }

        /* Special Clickable Branding */
        .p-brand-link { color: inherit; text-decoration: none; display: inline-flex; align-items: center; gap: 5px; }
        .p-brand-link i { font-size: 0.7rem; color: var(--primary); opacity: 0.7; transition: 0.3s; }
        .p-brand-link:hover i { opacity: 1; transform: scale(1.1); }

        /* SOS/Floating */
        .sos-btn { position: fixed; bottom: 100px; right: 20px; background: #ef4444; width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; z-index: 999; text-decoration: none; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
        .bottom-nav { position: fixed; bottom: 20px; left: 20px; right: 20px; background: rgba(255,255,255,0.08); backdrop-filter: blur(25px); display: flex; justify-content: space-around; padding: 18px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-link { color: rgba(255,255,255,0.4); font-size: 1.4rem; }
        .nav-link.active { color: var(--primary); }
    </style>
</head>
<body>

<div id="loader">
    <div style="width:45px; height:45px; border:4px solid var(--card); border-top-color:var(--primary); border-radius:50%; animation:spin 1s linear infinite"></div>
    <p style="margin-top:20px; font-weight:800; letter-spacing:3px; font-size:0.7rem; color:var(--primary);">ASTORE HUB LOADING...</p>
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

<div class="section-title"><i class="fa-solid fa-hand-pointer"></i> <span id="t-serv">Select Service</span></div>
<div class="grid">
    <div class="grid-item" onclick="selectService(this, 'Jeep 4x4')"><i class="fa-solid fa-truck-monster"></i><span>Jeep 4x4</span></div>
    <div class="grid-item" onclick="selectService(this, 'Hotel/Camp')"><i class="fa-solid fa-tents"></i><span>Hotels</span></div>
    <div class="grid-item" onclick="selectService(this, 'Local Guide')"><i class="fa-solid fa-user-check"></i><span>Guides</span></div>
    <div class="grid-item" onclick="selectService(this, 'Tour Plan')"><i class="fa-solid fa-map-location-dot"></i><span>Tour Plan</span></div>
</div>

<div class="section-title"><i class="fa-solid fa-circle-info"></i> <span id="t-info">Essential Info</span></div>
<div class="details-list">
    <div class="detail-item">
        <div class="detail-header" onclick="toggleDetail(this)">
            <span>Network & Signals</span> <i class="fa-solid fa-chevron-down"></i>
        </div>
        <div class="detail-content">
            Astore city mein complete Jazz/Telenor chalta hai, par Minimarg aur Deosai ke liye apko SCOM sim zaroori hai.
        </div>
    </div>
    <div class="detail-item">
        <div class="detail-header" onclick="toggleDetail(this)">
            <span>Transport Advice</span> <i class="fa-solid fa-chevron-down"></i>
        </div>
        <div class="detail-content">
            Astore City ke baad ke raste bohot rough hain, isliye hamesha expert drivers ke sath 4x4 Jeep use karein.
        </div>
    </div>
</div>

<div class="booking-cta">
    <h2 style="margin-bottom:10px">Ready for Astore?</h2>
    <p style="font-size:0.85rem; opacity:0.7;">Select a service above and click below to book with a local expert.</p>
    <button class="btn-main" onclick="bookNow()"><i class="fa-brands fa-whatsapp"></i> <span>Start Booking</span></button>
</div>

<div class="section">
    <div class="card" style="font-size: 0.8rem; text-align: center; border: 1px solid var(--primary);">
        <b style="color:var(--primary);">Astore Hub Pro Supervised by:</b><br>
        
        <a href="https://web-hub-code.github.io/Web-hub/" target="_blank" class="p-brand-link">
            Muhammad Nazim <i class="fa-solid fa-external-link-alt"></i>
        </a>
        <br>
        
        <b style="color:var(--primary); margin-top:5px; display:inline-block;">Powered By:</b><br>
        
        <a href="https://web-hub-code.github.io/PRIMESOLUTIONS/" target="_blank" class="p-brand-link">
            Prime Solutions <i class="fa-solid fa-external-link-alt"></i>
        </a>
    </div>
</div>

<footer class="footer" style="background: #000; padding: 40px 20px; text-align: center; border-top: 1px solid var(--primary);">
    <div style="font-weight: 800; color: var(--primary);">Official Astore Hub</div>
    <p style="font-size: 0.7rem; opacity: 0.5;">A property of Prime Solutions</p>
</footer>

<a href="tel:1122" class="sos-btn"><i class="fa-solid fa-phone-flip"></i></a>

<div style="height: 120px;"></div>

<nav class="bottom-nav">
    <a href="#" class="nav-link active"><i class="fa-solid fa-house-chimney"></i></a>
    <a href="https://wa.me/923171588489" class="nav-link"><i class="fa-solid fa-headset"></i></a>
</nav>

<script>
    // System Loader Fix
    window.addEventListener('load', () => {
        setTimeout(() => {
            const l = document.getElementById('loader');
            l.style.opacity = '0';
            setTimeout(() => l.style.display='none', 600);
        }, 1500);
    });

    // Interaction Logic
    let selectedSvc = "";
    function selectService(el, name) {
        document.querySelectorAll('.grid-item').forEach(i => i.classList.remove('active'));
        el.classList.add('active');
        selectedSvc = name;
        if(navigator.vibrate) navigator.vibrate(40);
    }

    function toggleDetail(el) {
        const item = el.parentElement;
        item.classList.toggle('open');
    }

    function bookNow() {
        if(!selectedSvc) {
            alert("Please select a service (Jeep/Hotel/Guide) first, sweetie! 😘");
            return;
        }
        window.open(`https://wa.me/923171588489?text=*Hello Astore Hub Official*%0AI'm inquiring about: ${selectedSvc}`);
    }

    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        const btn = document.querySelector('.lang-btn');
        const sTitle = document.getElementById('t-serv');
        const iTitle = document.getElementById('t-info');
        btn.innerText = isUrdu ? "ENGLISH" : "URDU";
        sTitle.innerText = isUrdu ? "سروس منتخب کریں" : "Select Service";
        iTitle.innerText = isUrdu ? "ضروری معلومات" : "Essential Info";
    }
</script>

</body>
</html>
