<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Tourist Hub | Official</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #10b981;
            --accent: #fbbf24;
            --danger: #ef4444;
            --bg: #020617;
            --card: rgba(255, 255, 255, 0.06);
            --glass: blur(15px);
            --text: #f8fafc;
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        /* --- Global Components --- */
        #loader { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: 0.8s; }
        .spinner { width: 40px; height: 40px; border: 3px solid var(--card); border-top-color: var(--primary); border-radius: 50%; animation: spin 1s linear infinite; }
        @keyframes spin { to { transform: rotate(360deg); } }

        header { position: sticky; top: 0; z-index: 100; padding: 18px 20px; background: rgba(2, 6, 23, 0.85); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); }

        /* --- Status Strips --- */
        .status-scroll { display: flex; gap: 10px; padding: 15px; overflow-x: auto; scrollbar-width: none; }
        .info-pill { background: var(--card); padding: 10px 18px; border-radius: 50px; border: 1px solid rgba(255,255,255,0.1); white-space: nowrap; font-size: 0.8rem; display: flex; align-items: center; gap: 8px; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }
        .dot { height: 8px; width: 8px; border-radius: 50%; background: #22c55e; box-shadow: 0 0 10px #22c55e; }

        /* --- Hero Slider --- */
        .hero { height: 32vh; margin: 0 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 18s infinite cubic-bezier(0.4, 0, 0.2, 1); }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        /* --- Sections --- */
        .section-title { padding: 25px 20px 10px; font-weight: 800; font-size: 1.1rem; color: var(--text); display: flex; align-items: center; gap: 8px; }
        .section-title i { color: var(--primary); }

        /* --- Destinations --- */
        .scrolling-wrapper { display: flex; overflow-x: auto; gap: 15px; padding: 0 20px 15px; scrollbar-width: none; }
        .dest-card { min-width: 240px; background: var(--card); border-radius: 25px; overflow: hidden; border: 1px solid rgba(255,255,255,0.05); }
        .dest-card img { width: 100%; height: 140px; object-fit: cover; }
        .dest-info { padding: 15px; }
        .dest-info h4 { font-size: 0.95rem; margin-bottom: 5px; color: var(--accent); }
        .dest-info p { font-size: 0.75rem; opacity: 0.7; line-height: 1.4; }

        /* --- Grid Services --- */
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; padding: 0 20px; }
        .box { background: var(--card); padding: 18px 10px; border-radius: 20px; text-align: center; border: 1px solid rgba(255,255,255,0.05); transition: 0.3s; }
        .box i { font-size: 1.5rem; color: var(--primary); margin-bottom: 8px; display: block; }
        .box:active { background: var(--primary); transform: scale(0.95); }
        .box.active { border-color: var(--primary); background: rgba(16, 185, 129, 0.1); }

        /* --- Data Lists --- */
        .data-list { margin: 15px 20px; background: var(--card); border-radius: 22px; padding: 18px; border: 1px solid rgba(255,255,255,0.05); }
        .data-item { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.05); font-size: 0.85rem; }
        .data-item:last-child { border: none; }
        .data-val { font-weight: 700; color: var(--primary); }

        /* --- Booking Card --- */
        .booking-card { margin: 25px 20px; background: linear-gradient(145deg, rgba(255,255,255,0.05), rgba(255,255,255,0.01)); padding: 25px; border-radius: 30px; border: 1px solid var(--primary); text-align: center; }
        .btn-wa { background: var(--primary); color: white; border: none; padding: 16px; border-radius: 18px; width: 100%; font-weight: 800; display: flex; align-items: center; justify-content: center; gap: 10px; margin-top: 15px; box-shadow: 0 10px 20px rgba(16, 185, 129, 0.2); }

        /* --- FAB & Nav --- */
        .emergency-fab { position: fixed; bottom: 100px; right: 20px; background: var(--danger); width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 1.5rem; box-shadow: 0 10px 25px rgba(239, 68, 68, 0.4); z-index: 99; animation: pulse 2s infinite; color: white; text-decoration: none; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }

        .nav-bar { position: fixed; bottom: 20px; left: 20px; right: 20px; background: rgba(255,255,255,0.07); backdrop-filter: blur(25px); padding: 15px; border-radius: 25px; display: flex; justify-content: space-around; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-link { color: rgba(255,255,255,0.4); font-size: 1.4rem; transition: 0.3s; }
        .nav-link.active { color: var(--primary); }
    </style>
</head>
<body>

<div id="loader">
    <div class="spinner"></div>
    <p style="margin-top: 15px; font-weight: 600; letter-spacing: 2px; font-size: 0.8rem;">ASTORE MASTER HUB</p>
</div>

<header>
    <div style="font-weight: 800; font-size: 1.1rem; letter-spacing: -0.5px;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="clock" style="font-size: 0.85rem; font-weight: 600; opacity: 0.7;"></div>
</header>

<div class="status-scroll">
    <div class="info-pill"><span class="dot"></span> Minimarg: Open</div>
    <div class="info-pill"><i class="fa-solid fa-cloud-sun" style="color:var(--accent)"></i> 14°C Astore</div>
    <div class="info-pill"><i class="fa-solid fa-signal" style="color:var(--primary)"></i> SCOM 4G Active</div>
    <div class="info-pill"><i class="fa-solid fa-snowflake" style="color:white"></i> Deosai: Snowing</div>
</div>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=800"></div>
    </div>
</section>

<div class="section-title"><i class="fa-solid fa-star"></i> Must Visit Spots</div>
<div class="scrolling-wrapper">
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=500">
        <div class="dest-info">
            <h4>Rama Meadows</h4>
            <p>Peaceful pine forests and a stunning alpine lake view.</p>
        </div>
    </div>
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=500">
        <div class="dest-info">
            <h4>Minimarg</h4>
            <p>The hidden jewel. Visit Rainbow Lake and lush green plains.</p>
        </div>
    </div>
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=500">
        <div class="dest-info">
            <h4>Deosai Plains</h4>
            <p>Plateau of Giants. Best visited between July and September.</p>
        </div>
    </div>
</div>

<div class="section-title"><i class="fa-solid fa-concierge-bell"></i> Services</div>
<div class="grid">
    <div class="box" onclick="select(this, 'Jeep')"><i class="fa-solid fa-truck-monster"></i>Jeep</div>
    <div class="box" onclick="select(this, 'Hotel')"><i class="fa-solid fa-bed"></i>Hotel</div>
    <div class="box" onclick="select(this, 'Guide')"><i class="fa-solid fa-person-hiking"></i>Guide</div>
</div>

<div class="section-title"><i class="fa-solid fa-info-circle"></i> Quick Info</div>
<div class="data-list">
    <div class="data-item"><span>Gilgit to Astore</span> <span class="data-val">4 Hours</span></div>
    <div class="data-item"><span>Best SIM Network</span> <span class="data-val">SCOM</span></div>
    <div class="data-item"><span>Local Food</span> <span class="data-val">Chapshuro</span></div>
    <div class="data-item"><span>ATM Facility</span> <span class="data-val">Astore City</span></div>
</div>

<div class="booking-card">
    <h3 style="margin-bottom:8px">Plan Your Trip</h3>
    <p style="font-size: 0.8rem; opacity: 0.7;">Select date and chat with our local expert.</p>
    <input type="date" id="bookDate" style="width:100%; padding:15px; border-radius:15px; border:none; background:rgba(255,255,255,0.1); color:white; margin:15px 0; outline:none;">
    <button class="btn-wa" onclick="goWhatsApp()"><i class="fa-brands fa-whatsapp"></i> Start Booking</button>
</div>

<a href="tel:1122" class="emergency-fab"><i class="fa-solid fa-phone-alt"></i></a>

<div style="height: 100px;"></div>

<nav class="nav-bar">
    <a href="#" class="nav-link active"><i class="fa-solid fa-house"></i></a>
    <a href="#" class="nav-link"><i class="fa-solid fa-map-marked"></i></a>
    <a href="#" class="nav-link" onclick="alert('Offline PDF Guide coming soon!')"><i class="fa-solid fa-download"></i></a>
    <a href="tel:923171588489" class="nav-link"><i class="fa-solid fa-headset"></i></a>
</nav>

<audio id="clickSfx" src="https://www.soundjay.com/buttons/sounds/button-16.mp3"></audio>

<script>
    // System Handlers
    window.addEventListener('load', () => {
        setTimeout(() => {
            const ldr = document.getElementById('loader');
            ldr.style.opacity = '0';
            setTimeout(() => ldr.remove(), 700);
        }, 1200);
        document.getElementById('bookDate').valueAsDate = new Date();
    });

    setInterval(() => {
        document.getElementById('clock').innerText = new Date().toLocaleTimeString([], {hour:'2-digit', minute:'2-digit'});
    }, 1000);

    // Interaction Logic
    let service = "";
    function select(el, name) {
        document.querySelectorAll('.box').forEach(b => b.classList.remove('active'));
        el.classList.add('active');
        service = name;
        document.getElementById('clickSfx').play();
        if(navigator.vibrate) navigator.vibrate(40);
    }

    function goWhatsApp() {
        const d = document.getElementById('bookDate').value;
        if(!service) { alert("Please select a service (Jeep/Hotel/Guide) first, sweetie!"); return; }
        const msg = `*Astore Tourist Hub Inquiry*%0A---%0A*Service:* ${service}%0A*Travel Date:* ${d}%0A*Source:* Official Website`;
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }
</script>

</body>
</html>
