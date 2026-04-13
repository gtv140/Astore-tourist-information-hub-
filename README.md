<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Mobile-First Premium Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        /* Modern Mobile-First CSS Variables */
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; --danger: #ef4444; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); line-height: 1.5; font-size: 16px; overflow-x: hidden; }

        /* Smooth Progress Bar */
        .p-bar { position: fixed; top: 0; z-index: 10000; height: 4px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.85); backdrop-filter: blur(20px); padding: 12px 15px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.85); }

        /* Modern Animated Slider for Mobile */
        .hero { position: relative; height: 40vh; width: 100%; overflow: hidden; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 15s infinite ease-in-out; }
        .slide { width: 100%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.65); }
        .slide-content { position: absolute; bottom: 0; left: 0; padding: 20px; color: white; background: linear-gradient(transparent, rgba(0,0,0,1)); width: 100%; }

        @keyframes slide { 0% { left: 0%; } 20% { left: 0%; } 25% { left: -100%; } 45% { left: -100%; } 50% { left: -200%; } 70% { left: -200%; } 75% { left: -300%; } 95% { left: -300%; } 100% { left: 0%; } }

        .container { padding: 15px 15px 100px; margin-top: -15px; position: relative; z-index: 100; }

        /* Responsive Grid System */
        .section-title { margin: 25px 0 12px; font-size: 1.2rem; font-weight: 800; border-left: 5px solid var(--primary); padding-left: 10px; color: var(--primary); display: flex; align-items: center; gap: 8px; }
        .card { background: var(--card); border-radius: 25px; padding: 18px; margin-bottom: 20px; box-shadow: 0 8px 25px rgba(0,0,0,0.05); transition: 0.3s; width: 100%; }

        /* Scrolling Info Chips (Mobile UX) */
        .status-scroll { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 12px; scrollbar-width: none; }
        .status-scroll::-webkit-scrollbar { display: none; }
        .chip { background: var(--card); padding: 10px 18px; border-radius: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); display: flex; align-items: center; gap: 6px; white-space: nowrap; font-size: 0.8rem; font-weight: 600; }

        /* Optimized Responsive Table */
        .table-container { width: 100%; overflow-x: auto; -webkit-overflow-scrolling: touch; }
        .info-table { width: 100%; border-collapse: collapse; min-width: 300px; font-size: 0.8rem; }
        .info-table td { padding: 12px 5px; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark .info-table td { border-bottom-color: rgba(255,255,255,0.05); }

        /* Checkbox UI for Mobile */
        .checklist-item { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; font-size: 0.9rem; font-weight: 500; }
        .checklist-item input { width: 22px; height: 22px; accent-color: var(--primary); flex-shrink: 0; }

        /* Food & Travel Chips */
        .chip-group { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 8px; }
        .food-chip { background: #fff7ed; color: #a16207; padding: 8px 15px; border-radius: 50px; font-size: 0.75rem; font-weight: 600; border: 1px solid #fdba74; }

        /* Touch-Friendly Booking UI */
        .booking-ui { background: var(--primary); color: white; border-radius: 25px; padding: 22px; }
        input, select { width: 100%; padding: 15px; border-radius: 15px; border: none; margin: 8px 0 15px; font-weight: 600; font-size: 0.9rem; }

        /* Buttons and Helpline */
        .btn { padding: 16px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 8px; border: none; cursor: pointer; font-size: 0.95rem; }
        .wa-btn { background: #25d366; color: white; box-shadow: 0 8px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #fee2e2; color: #ef4444; width: 100%; margin-top: 10px; }

        /* Fixed Mobile Controls */
        .controls { position: fixed; bottom: 20px; right: 15px; z-index: 9500; display: flex; flex-direction: column; gap: 10px; }
        .fab { width: 55px; height: 55px; border-radius: 18px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.2rem; }

        footer { text-align: center; padding: 40px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<header>
    <div style="font-weight: 900; font-size: 1.1rem; letter-spacing: -1px;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.75rem; font-weight: 700;">--:--</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&w=1200" alt="Hills">
            <div class="slide-content"><h1>Hills of Heaven</h1><p>Unlimited views, sweetie!</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1627483262769-04d0a140148a?auto=format&fit=crop&w=1200" alt="Lakes">
            <div class="slide-content"><h1>Rainbow Lake</h1><p>Crystal Clear Waters</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1591117207239-788cd203bca7?auto=format&fit=crop&w=1200" alt="Roads">
            <div class="slide-content"><h1>The Long Road</h1><p>Minimarg Adventure</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=1200" alt="Stay">
            <div class="slide-content"><h1>Luxury Stay</h1><p>Rama Meadows Night</p></div>
        </div>
    </div>
</section>

<div class="container">

    <div class="status-scroll">
        <div class="chip"><i class="fas fa-signal" style="color:#2563eb"></i> SCOM SIM (Mandatory)</div>
        <div class="chip"><i class="fas fa-cloud-sun" style="color:#f59e0b"></i> 14°C Sunny</div>
        <div class="chip"><i class="fas fa-check-circle" style="color:#10b981"></i> Road Open</div>
    </div>

    <div class="section-title"><i class="fas fa-car-side"></i> Jeep Rates (Return)</div>
    <div class="card table-container">
        <table class="info-table">
            <tr><td><b>Minimarg (Return)</b></td><td style="text-align:right">Rs. 18,000</td></tr>
            <tr><td><b>Rama Lake (Return)</b></td><td style="text-align:right">Rs. 7,000</td></tr>
            <tr><td><b>Deosai Safari</b></td><td style="text-align:right">Rs. 15,000</td></tr>
            <tr><td><b>Tarishing Basecamp</b></td><td style="text-align:right">Rs. 8,500</td></tr>
        </table>
    </div>

    <div class="section-title"><i class="fas fa-suitcase"></i> Packing List</div>
    <div class="card">
        <div class="checklist-item"><input type="checkbox"> <span>❄️ Warm Jacket & Gloves</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>🧴 Sunblock (Must)</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>🔋 Power Bank (信号弱)</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>💵 Extra Cash (No ATM)</span></div>
    </div>

    <div class="section-title"><i class="fas fa-utensils"></i> Must Try Local Food</div>
    <div class="card">
        <p style="font-size: 0.8rem; margin-bottom: 8px;">Astore ka fresh desi food lazmi try karein.</p>
        <div class="chip-group">
            <span class="food-chip">🐟 Fresh Trout Fish</span>
            <span class="food-chip">🧈 local Desi Ghee</span>
            <span class="food-chip">🍵 Namkeen Chai</span>
        </div>
    </div>

    <div class="section-title"><i class="fas fa-calendar-alt"></i> Quick Booking</div>
    <div class="booking-ui">
        <label style="font-size:0.7rem; font-weight:700; opacity:0.9;">Destination</label>
        <select id="srv">
            <option>Minimarg & Rainbow Lake</option>
            <option>Rama Meadows Night Stay</option>
            <option>Deosai Safari</option>
            <option>Nanga Parbat Basecamp</option>
        </select>
        <label style="font-size:0.7rem; font-weight:700; opacity:0.9;">Travel Date</label>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp"></i> REQUEST INSTANT QUOTE
        </button>
        <a href="tel:+923171588489" class="btn sos-btn">
            <i class="fas fa-phone-alt"></i> 24/7 HELPLINE
        </a>
    </div>

</div>

<div class="controls">
    <button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
</div>

<footer>
    <b>ASTORE TOURIST INFORMATION HUB 2026</b><br>
    Built with love for Mobile Users, Sweetie! 😘<br>
    <small>Verified by Gemini 2.0 Mobile First</small>
</footer>

<script>
    // Smooth Scroll Progress
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Live Time Update
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // Dynamic WhatsApp Messenger
    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! I need current rates for ${s} on Date: ${d}. Guide me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
