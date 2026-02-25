<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Elite Tourist Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #0b3d2e; --accent: #f59e0b; --bg: #f3f4f6; --white: #ffffff; }
        * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
        body { font-family: 'Inter', -apple-system, sans-serif; background: var(--bg); color: #1f2937; line-height: 1.6; }

        /* Road Alerts Ticker */
        .alert-ticker { background: #fee2e2; color: #b91c1c; padding: 8px; font-size: 0.75rem; font-weight: bold; overflow: hidden; position: sticky; top: 0; z-index: 1001; }
        .ticker-content { display: inline-block; white-space: nowrap; animation: ticker 20s linear infinite; }
        @keyframes ticker { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        /* Navigation */
        nav { background: var(--white); padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 31px; z-index: 1000; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1); }
        .logo { font-weight: 900; color: var(--primary); letter-spacing: -1px; font-size: 1.4rem; text-decoration: none; }

        /* Hero */
        .hero { height: 45vh; background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }
        .hero h1 { font-size: 2.5rem; line-height: 1.1; }

        .container { width: 100%; max-width: 500px; margin: 0 auto; padding: 25px 15px; }

        /* Distance Card */
        .stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 25px; }
        .stat-card { background: var(--white); padding: 15px; border-radius: 15px; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.05); }
        .stat-card b { display: block; font-size: 1.1rem; color: var(--primary); }
        .stat-card span { font-size: 0.7rem; color: #6b7280; text-transform: uppercase; }

        /* Itinerary Timeline */
        .timeline { background: var(--white); padding: 25px; border-radius: 20px; margin-bottom: 30px; }
        .timeline-item { border-left: 2px solid var(--accent); padding-left: 20px; position: relative; margin-bottom: 20px; }
        .timeline-item::before { content: ''; position: absolute; left: -6px; top: 0; width: 10px; height: 10px; background: var(--accent); border-radius: 50%; }
        .timeline-item h4 { font-size: 0.9rem; color: var(--primary); }
        .timeline-item p { font-size: 0.8rem; color: #4b5563; }

        /* Gear Checklist */
        .checklist { background: #064e3b; color: white; padding: 25px; border-radius: 20px; margin-bottom: 30px; }
        .check-item { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; font-size: 0.85rem; }
        .check-item i { color: var(--accent); }

        /* Map Placeholder */
        .map-box { background: #e5e7eb; border-radius: 20px; height: 200px; margin-bottom: 30px; display: flex; align-items: center; justify-content: center; text-align: center; color: #6b7280; font-size: 0.8rem; border: 2px dashed #d1d5db; }

        /* Professional Form */
        .booking-card { background: var(--white); padding: 30px 20px; border-radius: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); }
        .input-group { margin-bottom: 15px; }
        .input-group label { display: block; font-size: 0.8rem; font-weight: bold; margin-bottom: 5px; color: #374151; }
        input, select { width: 100%; padding: 12px; border: 1px solid #d1d5db; border-radius: 10px; font-size: 1rem; background: #f9fafb; }
        .book-btn { width: 100%; padding: 16px; background: #059669; color: white; border: none; border-radius: 12px; font-weight: 800; font-size: 1.1rem; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; }

        /* Footer */
        .wa-float { position: fixed; bottom: 20px; right: 20px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 8px 16px rgba(37,211,102,0.3); z-index: 2000; }
        footer { text-align: center; padding: 40px 20px; background: var(--white); border-top: 1px solid #e5e7eb; font-size: 0.8rem; }
    </style>
</head>
<body>

<div class="alert-ticker">
    <div class="ticker-content">
        ⚠️ ROAD UPDATE: Astore-Gilgit road is Open for all traffic. Burzil Pass is currently restricted to 4x4 vehicles only. Please carry original CNICs for NOC.
    </div>
</div>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <div style="font-size: 0.8rem; color: #059669; font-weight: bold;"><i class="fas fa-circle"></i> Online</div>
</nav>

<div class="hero">
    <h1>Explore the Heart of Gilgit</h1>
    <p>Premium Jeep Services & Guided Tours</p>
</div>

<div class="container">
    
    <div class="stats-grid">
        <div class="stat-card"><span>From Gilgit</span><b>110 KM</b></div>
        <div class="stat-card"><span>Altitude</span><b>2,600m</b></div>
    </div>

    <div style="margin-bottom: 30px;">
        <h2 style="color: var(--primary); margin-bottom: 10px;">Why Visit Astore?</h2>
        <p style="font-size: 0.9rem; color: #4b5563;">Astore Valley Pakistan ka wo chupa hua khazana hai jo "Land of Giants" (Deosai) ka rasta faraham karta hai. Yahan ki **Rainbow Lake** dunya ki haseen tareen lakes mein shumar hoti hai. Hamari service aapko in mushkil raston par intehayi sukoon aur hifazat ke sath le jati hai.</p>
    </div>

    <div class="timeline">
        <h3 style="margin-bottom: 20px; color: var(--primary);"><i class="fas fa-route"></i> 3-Day Perfect Plan</h3>
        <div class="timeline-item">
            <h4>Day 1: Arrival & Rama</h4>
            <p>Astore arrival, visit to Rama Meadows and night stay under the stars.</p>
        </div>
        <div class="timeline-item">
            <h4>Day 2: Minimarg Odyssey</h4>
            <p>Early drive to Minimarg, visiting Rainbow Lake and Domail Valley.</p>
        </div>
        <div class="timeline-item">
            <h4>Day 3: Deosai Crossing</h4>
            <p>Crossing Chillum Gate to Sheosar Lake and exit via Skardu or return.</p>
        </div>
    </div>

    <div class="checklist">
        <h3 style="margin-bottom: 15px;"><i class="fas fa-suitcase"></i> Travel Essentials</h3>
        <div class="check-item"><i class="fas fa-check"></i> Warm Jackets (Hatta ke June mein bhi)</div>
        <div class="check-item"><i class="fas fa-check"></i> Original CNIC (For NOC/Checkposts)</div>
        <div class="check-item"><i class="fas fa-check"></i> Sunblock & Sunglasses</div>
        <div class="check-item"><i class="fas fa-check"></i> Power Bank (Electricity issues in remote areas)</div>
    </div>

    <div class="map-box">
        <div>
            <i class="fas fa-map-marked-alt fa-3x" style="margin-bottom:10px; color: var(--accent);"></i>
            <p>Main Bazar Astore, Gilgit-Baltistan<br><a href="https://maps.google.com" style="color: var(--primary); font-weight:bold;">Open in Google Maps</a></p>
        </div>
    </div>

    <div class="booking-card" id="book">
        <h2 style="text-align:center; color: var(--primary); margin-bottom:20px;">Reserve Your Seat</h2>
        <div class="input-group">
            <label>Full Name</label>
            <input type="text" id="userName" placeholder="e.g. Ali Khan">
        </div>
        <div class="input-group">
            <label>Trip Type</label>
            <select id="tripType">
                <option>Minimarg Special (Full Day)</option>
                <option>Rama Meadows (Short Trip)</option>
                <option>Deosai Plains Crossing</option>
                <option>Custom Full Package</option>
            </select>
        </div>
        <button class="book-btn" onclick="startBooking()">
            <i class="fab fa-whatsapp"></i> Confirm Booking
        </button>
        <p style="font-size: 0.7rem; text-align:center; margin-top:10px; color: #6b7280;">* No advance payment required for basic booking.</p>
    </div>

</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <div style="margin-bottom: 20px;">
        <i class="fab fa-facebook fa-2x" style="margin: 0 10px; color: #1877f2;"></i>
        <i class="fab fa-instagram fa-2x" style="margin: 0 10px; color: #e4405f;"></i>
    </div>
    <p><b>ASTORE TOURIST INFORMATION HUB</b></p>
    <p>Official Partners: Local Jeep Union Astore</p>
    <p>Direct Call: +92 317 1588489</p>
</footer>

<script>
    function startBooking() {
        const name = document.getElementById('userName').value;
        const trip = document.getElementById('tripType').value;
        if(!name) { alert('Please enter your name, sweetie!'); return; }
        const url = `https://wa.me/923171588489?text=Assalam-o-Alaikum! My name is ${name}. I want to inquire about the ${trip}. Please guide me about the rates and availability.`;
        window.open(url, '_blank');
    }
</script>

</body>
</html>
