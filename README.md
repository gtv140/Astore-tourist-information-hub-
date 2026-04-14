<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub | Complete Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #10b981; --accent: #fbbf24; --bg: #020617; --card: rgba(255, 255, 255, 0.05); --glass: blur(15px); --text: #f8fafc; }
        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        #loader { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: 0.5s; }
        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.85); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .lang-btn { background: var(--card); border: 1px solid var(--primary); color: var(--primary); padding: 5px 12px; border-radius: 10px; font-size: 0.7rem; font-weight: 800; cursor: pointer; }

        .hero { height: 28vh; margin: 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 18s infinite cubic-bezier(0.4, 0, 0.2, 1); }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        .section-title { padding: 15px 20px 5px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 8px; }
        .section-title i { color: var(--primary); }

        /* Detail Cards */
        .info-card { margin: 10px 20px; background: var(--card); border-radius: 20px; padding: 15px; border: 1px solid rgba(255,255,255,0.05); }
        .info-card h4 { color: var(--accent); margin-bottom: 8px; font-size: 0.9rem; display: flex; align-items: center; gap: 8px; }
        .info-card p { font-size: 0.8rem; opacity: 0.8; line-height: 1.5; }
        .tag-row { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 10px; }
        .tag { background: rgba(16, 185, 129, 0.1); color: var(--primary); padding: 4px 10px; border-radius: 8px; font-size: 0.7rem; font-weight: 600; }

        /* Grid */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; padding: 15px 20px; }
        .grid-item { background: var(--card); padding: 15px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.05); text-align: center; }
        .grid-item i { font-size: 1.5rem; color: var(--primary); margin-bottom: 8px; display: block; }
        .grid-item span { font-size: 0.75rem; font-weight: 600; }

        /* Booking */
        .book-box { margin: 20px; background: linear-gradient(135deg, #064e3b, #020617); padding: 25px; border-radius: 30px; border: 1px solid var(--primary); text-align: center; }
        .btn-wa { background: var(--primary); color: white; border: none; padding: 18px; border-radius: 18px; width: 100%; font-weight: 800; display: flex; align-items: center; justify-content: center; gap: 10px; cursor: pointer; }

        .bottom-nav { position: fixed; bottom: 15px; left: 15px; right: 15px; background: rgba(255,255,255,0.08); backdrop-filter: blur(20px); display: flex; justify-content: space-around; padding: 15px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-link { color: rgba(255,255,255,0.4); font-size: 1.3rem; }
        .nav-link.active { color: var(--primary); }
    </style>
</head>
<body>

<div id="loader">
    <div style="width:40px; height:40px; border:3px solid var(--card); border-top-color:var(--primary); border-radius:50%; animation:spin 1s linear infinite"></div>
    <p style="margin-top:15px; font-weight:700; letter-spacing:2px; font-size:0.7rem;">ASTORE COMPLETE HUB</p>
</div>

<header>
    <div id="brand" style="font-weight: 800;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <button class="lang-btn" onclick="toggleLang()">URDU</button>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
    </div>
</section>

<div class="section-title"><i class="fa-solid fa-shield-check"></i> <span id="t-essential">Travel Essentials</span></div>
<div class="info-card">
    <h4 id="t-net-h"><i class="fa-solid fa-tower-cell"></i> Network & Connectivity</h4>
    <p id="t-net-p">Astore city mein SCOM aur Telenor chalta hai. Minimarg aur Deosai mein sirf SCOM signals aate hain. 4G services limited hain.</p>
    <div class="tag-row"><div class="tag">SCOM Highly Recommended</div></div>
</div>

<div class="info-card">
    <h4 id="t-cash-h"><i class="fa-solid fa-money-bill-transfer"></i> Money & ATM</h4>
    <p id="t-cash-p">Sirf Astore City mein NBP ya HBL ka ATM milega. Upper areas (Rama/Minimarg) ke liye cash sath rakhein kyunke online payment mushkil hai.</p>
</div>

<div class="section-title"><i class="fa-solid fa-location-dot"></i> <span id="t-spot">Spot Details</span></div>
<div class="info-card">
    <h4>Rama Meadows & Lake</h4>
    <p id="t-rama-p">Astore city se 30 min ki drive hai. Yahan Jeep road hai. Lake tak janay ke liye 1 hour ka trek ya ghore (horse) ka safar zaroori hai.</p>
    <div class="tag-row"><div class="tag">Family Friendly</div><div class="tag">Easy Access</div></div>
</div>

<div class="info-card">
    <h4>Minimarg & Rainbow Lake</h4>
    <p id="t-mini-p">Iske liye Burzil Pass cross karna hota hai. Entry ke liye CNIC zaroori hai (Army check post). Raasta thoda kathin hai par manzar jannat jesa hai.</p>
    <div class="tag-row"><div class="tag">Needs Permission</div><div class="tag">Best in July-Aug</div></div>
</div>

<div class="grid">
    <div class="grid-item"><i class="fa-solid fa-car-side"></i><span>4x4 Jeep</span></div>
    <div class="grid-item"><i class="fa-solid fa-hotel"></i><span>Best Hotels</span></div>
    <div class="grid-item"><i class="fa-solid fa-user-shield"></i><span>Local Guide</span></div>
    <div class="grid-item"><i class="fa-solid fa-utensils"></i><span>Local Food</span></div>
</div>

<div class="book-box">
    <h3 id="t-book-h">Need Personalized Plan?</h3>
    <p id="t-book-p" style="font-size:0.8rem; opacity:0.7; margin-bottom:15px;">Hum aapko rasta, mausam aur kharche ki mukammal details denge.</p>
    <button class="btn-wa" onclick="contactWa()"><i class="fa-brands fa-whatsapp"></i> <span id="t-btn">Talk to Expert</span></button>
</div>

<div style="height: 100px;"></div>

<nav class="bottom-nav">
    <a href="#" class="nav-link active"><i class="fa-solid fa-house"></i></a>
    <a href="#" class="nav-link"><i class="fa-solid fa-map-location-dot"></i></a>
    <a href="tel:923171588489" class="nav-link"><i class="fa-solid fa-phone"></i></a>
    <a href="#" class="nav-link"><i class="fa-solid fa-circle-info"></i></a>
</nav>

<script>
    function endLoader() {
        const l = document.getElementById('loader');
        if(l) { l.style.opacity = '0'; setTimeout(() => l.style.display='none', 500); }
    }
    setTimeout(endLoader, 2500);
    window.addEventListener('load', endLoader);

    function contactWa() {
        window.open("https://wa.me/923171588489?text=*Hello Astore Hub!*%0AI need full travel details and a plan for Astore Valley.");
    }

    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        const btn = document.querySelector('.lang-btn');
        const tEssential = document.getElementById('t-essential');
        const tNetH = document.getElementById('t-net-h');
        const tNetP = document.getElementById('t-net-p');
        const tCashH = document.getElementById('t-cash-h');
        const tCashP = document.getElementById('t-cash-p');
        const tSpot = document.getElementById('t-spot');
        const tRamaP = document.getElementById('t-rama-p');
        const tMiniP = document.getElementById('t-mini-p');
        const tBookH = document.getElementById('t-book-h');
        const tBtn = document.getElementById('t-btn');

        if(isUrdu) {
            btn.innerText = "ENGLISH";
            tEssential.innerText = "سفر کی ضروریات";
            tNetH.innerText = "نیٹ ورک اور سگنلز";
            tNetP.innerText = "استور سٹی میں تمام نیٹ ورک چلتے ہیں، لیکن بالائی علاقوں میں صرف SCOM چلے گا۔";
            tCashH.innerText = "پیسے اور اے ٹی ایم";
            tCashP.innerText = "صرف استور سٹی میں اے ٹی ایم کی سہولت ہے، آگے کے لیے کیش ساتھ رکھیں۔";
            tSpot.innerText = "مقامات کی تفصیل";
            tRamaP.innerText = "راما لیک کے لیے 1 گھنٹہ ہائیکنگ یا گھوڑا لینا پڑتا ہے۔ جیپ روڈ موجود ہے۔";
            tMiniP.innerText = "منی مرگ کے لیے شناختی کارڈ ساتھ رکھنا لازمی ہے (آرمی چیک پوسٹ کی وجہ سے)۔";
            tBookH.innerText = "مکمل ٹرپ پلان چاہیے؟";
            tBtn.innerText = "رابطہ کریں";
        } else {
            btn.innerText = "URDU";
            tEssential.innerText = "Travel Essentials";
            tNetH.innerText = "Network & Connectivity";
            tNetP.innerText = "Astore city has mixed networks, but Minimarg/Deosai only support SCOM.";
            tCashH.innerText = "Money & ATM";
            tCashP.innerText = "ATM is only available in Astore City. Carry cash for remote spots.";
            tSpot.innerText = "Spot Details";
            tRamaP.innerText = "Rama Lake requires a 1-hour hike or a horse ride. Jeep road is accessible.";
            tMiniP.innerText = "CNIC is mandatory for Minimarg entry due to Army checkposts.";
            tBookH.innerText = "Need Personalized Plan?";
            tBtn.innerText = "Talk to Expert";
        }
    }
</script>

</body>
</html>
