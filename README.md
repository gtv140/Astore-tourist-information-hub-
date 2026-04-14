<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub | The Ultimate Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #10b981;
            --accent: #fbbf24;
            --bg: #020617;
            --card: rgba(255, 255, 255, 0.05);
            --glass: blur(15px);
            --text: #f8fafc;
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        /* --- UI Elements --- */
        #loader { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: 0.8s; }
        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.85); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); }
        
        .lang-btn { background: var(--card); border: 1px solid var(--primary); color: var(--primary); padding: 5px 12px; border-radius: 10px; font-size: 0.7rem; font-weight: 800; cursor: pointer; }

        .status-scroll { display: flex; gap: 10px; padding: 15px; overflow-x: auto; scrollbar-width: none; }
        .pill { background: var(--card); padding: 10px 18px; border-radius: 50px; border: 1px solid rgba(255,255,255,0.1); white-space: nowrap; font-size: 0.75rem; display: flex; align-items: center; gap: 8px; }

        /* --- Hero --- */
        .hero { height: 30vh; margin: 0 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 18s infinite cubic-bezier(0.4, 0, 0.2, 1); }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        /* --- Destinations --- */
        .scrolling-wrapper { display: flex; overflow-x: auto; gap: 15px; padding: 0 20px 15px; scrollbar-width: none; }
        .dest-card { min-width: 260px; background: var(--card); border-radius: 25px; overflow: hidden; border: 1px solid rgba(255,255,255,0.05); }
        .dest-card img { width: 100%; height: 140px; object-fit: cover; }
        .dest-info { padding: 15px; }
        .dest-info h4 { color: var(--accent); font-size: 1rem; margin-bottom: 4px; }
        .dest-info p { font-size: 0.75rem; opacity: 0.7; line-height: 1.4; }

        /* --- Distance & Info --- */
        .info-section { margin: 20px; background: var(--card); border-radius: 25px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); }
        .info-row { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.05); font-size: 0.85rem; }
        .info-row:last-child { border: none; }
        .val { font-weight: 800; color: var(--primary); }

        /* --- Packing Smart List --- */
        .pack-list { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; margin: 10px 0; }
        .pack-item { background: rgba(16, 185, 129, 0.1); padding: 10px; border-radius: 12px; font-size: 0.7rem; display: flex; align-items: center; gap: 6px; }

        /* --- Booking --- */
        .book-card { margin: 25px 20px; background: linear-gradient(135deg, #064e3b, #020617); padding: 25px; border-radius: 30px; border: 1px solid var(--primary); text-align: center; position: relative; overflow: hidden; }
        .book-card::before { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: radial-gradient(circle, rgba(16,185,129,0.1) 0%, transparent 70%); pointer-events: none; }
        .btn-wa { background: var(--primary); color: white; border: none; padding: 18px; border-radius: 18px; width: 100%; font-weight: 800; font-size: 1rem; display: flex; align-items: center; justify-content: center; gap: 10px; box-shadow: 0 10px 25px rgba(16, 185, 129, 0.3); cursor: pointer; }

        /* --- Nav --- */
        .bottom-nav { position: fixed; bottom: 15px; left: 15px; right: 15px; background: rgba(255,255,255,0.08); backdrop-filter: blur(20px); display: flex; justify-content: space-around; padding: 15px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-link { color: rgba(255,255,255,0.4); font-size: 1.3rem; text-decoration: none; }
        .nav-link.active { color: var(--primary); }

        .section-title { padding: 10px 20px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 8px; margin-top: 10px; }
        .section-title i { color: var(--primary); }

        /* Emergency */
        .sos { position: fixed; bottom: 90px; right: 20px; background: #ef4444; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; box-shadow: 0 5px 20px rgba(239, 68, 68, 0.4); z-index: 999; text-decoration: none; font-size: 1.2rem; }
    </style>
</head>
<body>

<div id="loader">
    <div style="width:40px; height:40px; border:3px solid var(--card); border-top-color:var(--primary); border-radius:50%; animation:spin 1s linear infinite"></div>
    <p style="margin-top:15px; font-weight:700; letter-spacing:2px; font-size:0.7rem;">LOADING ASTORE HUB PRO</p>
</div>

<header>
    <div id="brand" style="font-weight: 800; font-size: 1.1rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <button class="lang-btn" onclick="toggleLang()">URDU</button>
</header>

<div class="status-scroll">
    <div class="pill"><span style="color:#22c55e">●</span> Road: Minimarg Open</div>
    <div class="pill"><i class="fa-solid fa-cloud-bolt" style="color:var(--accent)"></i> 12°C Astore</div>
    <div class="pill"><i class="fa-solid fa-tower-cell" style="color:var(--primary)"></i> 4G Network OK</div>
</div>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
    </div>
</section>

<div class="section-title"><i class="fa-solid fa-compass"></i> <span id="t-dest">Popular Destinations</span></div>
<div class="scrolling-wrapper">
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=500">
        <div class="dest-info">
            <h4 class="d-name">Rama Valley</h4>
            <p class="d-desc">Famous for its pine forests and the breathtaking Rama Lake.</p>
        </div>
    </div>
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=500">
        <div class="dest-info">
            <h4 class="d-name">Minimarg</h4>
            <p class="d-desc">The hidden paradise. Rainbow Lake is a must-visit spot here.</p>
        </div>
    </div>
</div>

<div class="section-title"><i class="fa-solid fa-suitcase-rolling"></i> <span id="t-pack">Smart Travel Guide</span></div>
<div class="info-section">
    <p style="font-size: 0.75rem; opacity: 0.7; margin-bottom: 10px;">Recommended for today:</p>
    <div class="pack-list">
        <div class="pack-item"><i class="fa-solid fa-shirt"></i> Warm Jacket</div>
        <div class="pack-item"><i class="fa-solid fa-mobile-screen"></i> SCOM SIM</div>
        <div class="pack-item"><i class="fa-solid fa-wallet"></i> Physical Cash</div>
        <div class="pack-item"><i class="fa-solid fa-shoe-prints"></i> Trekking Shoes</div>
    </div>
    <div style="margin-top:15px;">
        <div class="info-row"><span>City to Rama</span> <span class="val">11 KM</span></div>
        <div class="info-row"><span>City to Minimarg</span> <span class="val">65 KM</span></div>
        <div class="info-row"><span>City to Deosai</span> <span class="val">42 KM</span></div>
    </div>
</div>

<div class="book-card">
    <h3 id="t-book-h" style="margin-bottom:8px">Ready for Adventure?</h3>
    <p id="t-book-p" style="font-size: 0.8rem; opacity: 0.7; margin-bottom: 20px;">Book your professional Jeep, Hotel or Guide with us.</p>
    <button class="btn-wa" onclick="contactWa()"><i class="fa-brands fa-whatsapp"></i> <span id="t-btn">Contact Local Expert</span></button>
</div>

<a href="tel:1122" class="sos"><i class="fa-solid fa-truck-medical"></i></a>
<div style="height: 100px;"></div>

<nav class="bottom-nav">
    <a href="#" class="nav-link active"><i class="fa-solid fa-house-user"></i></a>
    <a href="#" class="nav-link"><i class="fa-solid fa-map-pin"></i></a>
    <a href="tel:923171588489" class="nav-link"><i class="fa-solid fa-phone"></i></a>
    <a href="#" class="nav-link" onclick="alert('Tourist Policy Updated for 2026')"><i class="fa-solid fa-shield-halved"></i></a>
</nav>

<script>
    // System UI
    window.onload = () => {
        setTimeout(() => {
            const l = document.getElementById('loader');
            l.style.opacity = '0';
            setTimeout(() => l.remove(), 700);
        }, 1200);
    };

    function contactWa() {
        window.open("https://wa.me/923171588489?text=*Hello Astore Hub!*%0AI'm planning a trip and need professional help.");
    }

    // Language Toggle Feature
    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        const btn = document.querySelector('.lang-btn');
        const tDest = document.getElementById('t-dest');
        const tPack = document.getElementById('t-pack');
        const tBookH = document.getElementById('t-book-h');
        const tBtn = document.getElementById('t-btn');

        if(isUrdu) {
            btn.innerText = "ENGLISH";
            tDest.innerText = "مشہور سیاحتی مقامات";
            tPack.innerText = "سفری گائیڈ اور ضروری سامان";
            tBookH.innerText = "سفر کے لیے تیار ہیں؟";
            tBtn.innerText = "ماہر سے رابطہ کریں";
            document.getElementById('brand').innerHTML = 'استور <span style="color:var(--primary)">ہب</span>';
        } else {
            btn.innerText = "URDU";
            tDest.innerText = "Popular Destinations";
            tPack.innerText = "Smart Travel Guide";
            tBookH.innerText = "Ready for Adventure?";
            tBtn.innerText = "Contact Local Expert";
            document.getElementById('brand').innerHTML = 'ASTORE <span style="color:var(--primary)">HUB</span>';
        }
        if(navigator.vibrate) navigator.vibrate(50);
    }

    @keyframes spin { to { transform: rotate(360deg); } }
</script>

</body>
</html>
