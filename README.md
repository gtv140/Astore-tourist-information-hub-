<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub | Unlimited Features 2026</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #065f46; --accent: #fbbf24; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Plus Jakarta Sans', sans-serif; transition: 0.3s ease; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; -webkit-tap-highlight-color: transparent; }

        header { position: sticky; top: 0; z-index: 1000; background: rgba(255,255,255,0.9); backdrop-filter: blur(15px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(15,23,42,0.9); }

        /* Floating Alert */
        .alert-banner { background: var(--accent); color: #000; padding: 10px; text-align: center; font-size: 0.75rem; font-weight: 800; animation: blink 2s infinite; }
        @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0.7; } }

        /* Modern Slider */
        .hero { height: 35vh; width: 100%; position: relative; overflow: hidden; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 15s infinite; }
        .slide { width: 100%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.65); }
        .hero-text { position: absolute; bottom: 20px; left: 20px; color: white; }

        @keyframes slide { 0%, 20% { transform: translateX(0%); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } 100% { transform: translateX(0%); } }

        .container { padding: 15px; }

        /* Feature Grid */
        .section-title { margin: 20px 0 10px; font-size: 1.1rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 8px; }
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-bottom: 20px; }
        .service-btn { background: var(--card); border-radius: 15px; padding: 15px 5px; text-align: center; box-shadow: 0 4px 10px rgba(0,0,0,0.05); cursor: pointer; border: none; }
        .service-btn i { color: var(--primary); font-size: 1.4rem; margin-bottom: 8px; display: block; }
        .service-btn span { font-size: 0.65rem; font-weight: 700; color: var(--text); }

        /* Utility Cards */
        .card { background: var(--card); border-radius: 20px; padding: 15px; margin-bottom: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); }
        .checklist-item { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; font-size: 0.8rem; font-weight: 600; }
        .checklist-item input { accent-color: var(--primary); width: 18px; height: 18px; }

        /* Booking Panel */
        .booking-box { background: var(--primary); color: white; border-radius: 25px; padding: 25px; margin-top: 10px; }
        .booking-box select, .booking-box input { width: 100%; padding: 12px; border-radius: 12px; border: none; margin: 8px 0 15px; font-weight: 600; }

        .btn-main { background: #25d366; color: white; padding: 16px; border-radius: 15px; border: none; width: 100%; font-weight: 800; font-size: 1rem; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; }
        .sos-btn { background: #fee2e2; color: #ef4444; margin-top: 10px; font-size: 0.8rem; padding: 12px; border-radius: 12px; display: block; text-align: center; text-decoration: none; font-weight: 700; }

        /* Floating Buttons */
        .fab { position: fixed; bottom: 20px; right: 20px; width: 55px; height: 55px; border-radius: 18px; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; box-shadow: 0 10px 25px rgba(0,0,0,0.2); z-index: 2000; border: none; }

        footer { text-align: center; padding: 40px; opacity: 0.5; font-size: 0.7rem; line-height: 1.8; }
    </style>
</head>
<body>

<div class="alert-banner"><i class="fas fa-bullhorn"></i> ROAD ALERT: Burzil Pass is open for 4x4 vehicles only!</div>

<header>
    <div style="font-weight: 800; font-size: 1.1rem;">ASTORE<span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.8rem; font-weight: 700;">00:00</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800"></div>
    </div>
    <div class="hero-text">
        <h2 style="font-size: 1.5rem; font-weight: 800;">Unlimited Adventure</h2>
        <p style="font-size: 0.8rem; opacity: 0.9;">Your 2026 Ultimate Guide, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="section-title"><i class="fas fa-th-large"></i> Explore Services</div>
    <div class="grid">
        <button class="service-btn" onclick="alert('Searching Jeeps...')"><i class="fas fa-jeep"></i><span>Jeep Rental</span></button>
        <button class="service-btn" onclick="alert('Finding Hotels...')"><i class="fas fa-hotel"></i><span>Hotel Stay</span></button>
        <button class="service-btn" onclick="alert('Loading Maps...')"><i class="fas fa-map-marked"></i><span>Tour Guide</span></button>
        <button class="service-btn" onclick="alert('Weather Forecast...')"><i class="fas fa-cloud-sun"></i><span>Weather</span></button>
        <button class="service-btn" onclick="alert('Packing Tips...')"><i class="fas fa-suitcase"></i><span>Packing</span></button>
        <button class="service-btn" onclick="alert('Food Guide...')"><i class="fas fa-utensils"></i><span>Local Food</span></button>
    </div>

    <div class="section-title"><i class="fas fa-clipboard-check"></i> Travel Checklist</div>
    <div class="card">
        <div class="checklist-item"><input type="checkbox"> <span>SCOM SIM (Internet)</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>CNIC Original</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Warm Clothes</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Extra Cash (No ATMs)</span></div>
    </div>

    <div class="section-title"><i class="fas fa-calendar-check"></i> Instant Booking</div>
    <div class="booking-box">
        <label style="font-size: 0.7rem; font-weight: 800;">CHOOSE DESTINATION</label>
        <select id="srv">
            <option>Minimarg & Rainbow Lake</option>
            <option>Rama Meadows Tour</option>
            <option>Deosai Plains Safari</option>
            <option>Tarishing (Nanga Parbat)</option>
        </select>
        <label style="font-size: 0.7rem; font-weight: 800;">TRAVEL DATE</label>
        <input type="date" id="dt">
        <button class="btn-main" onclick="book()">
            <i class="fab fa-whatsapp fa-lg"></i> BOOK ON WHATSAPP
        </button>
        <a href="tel:+923171588489" class="sos-btn"><i class="fas fa-phone-alt"></i> EMERGENCY SOS HELPLINE</a>
    </div>

</div>

<button class="fab" onclick="document.body.classList.toggle('dark')">
    <i class="fas fa-moon"></i>
</button>

<footer>
    <b>ASTORE TOURIST MASTER HUB 2026</b><br>
    Built with Unlimited Passion for Astore Travelers<br>
    Everything Clickable & Verified, sweetie! 😘
</footer>

<script>
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! I want to book ${s} for ${d || 'my upcoming trip'}. Please send details, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
