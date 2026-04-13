<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Ultimate 2026 Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; --danger: #ef4444; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: 0.3s; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; line-height: 1.6; }

        .p-bar { position: fixed; top: 0; z-index: 10000; height: 5px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(20px); padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); }

        .hero { position: relative; height: 45vh; width: 100%; overflow: hidden; }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.6); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 30px; background: linear-gradient(transparent, rgba(0,0,0,1)); width: 100%; color: white; }

        .container { padding: 0 16px 120px; margin-top: -30px; position: relative; z-index: 100; }

        /* Modern Grid & Cards */
        .section-title { margin: 30px 0 15px; font-size: 1.3rem; font-weight: 800; border-left: 5px solid var(--primary); padding-left: 12px; color: var(--primary); }
        .card { background: var(--card); border-radius: 30px; padding: 20px; margin-bottom: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        
        /* Distance & Rate Table */
        .info-table { width: 100%; border-collapse: collapse; font-size: 0.85rem; }
        .info-table td { padding: 12px 5px; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark .info-table td { border-bottom-color: rgba(255,255,255,0.05); }

        /* Checklist UI */
        .checklist-item { display: flex; align-items: center; gap: 10px; margin-bottom: 12px; font-size: 0.9rem; font-weight: 500; }
        .checklist-item input { width: 20px; height: 20px; accent-color: var(--primary); }

        /* Status Pills */
        .badge { padding: 5px 12px; border-radius: 50px; font-size: 0.7rem; font-weight: 800; text-transform: uppercase; }
        .badge-safe { background: #dcfce7; color: #15803d; }
        .badge-warn { background: #fef9c3; color: #a16207; }

        /* Booking UI */
        .booking-ui { background: var(--primary); color: white; border-radius: 30px; padding: 25px; }
        .booking-ui input, .booking-ui select { width: 100%; padding: 15px; border-radius: 15px; border: none; margin-top: 10px; margin-bottom: 15px; font-weight: 600; }

        .btn { padding: 18px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; border: none; cursor: pointer; }
        .wa-btn { background: #25d366; color: white; box-shadow: 0 10px 25px rgba(37,211,102,0.4); }
        .map-btn { background: var(--bg); color: var(--text); font-size: 0.8rem; margin-top: 10px; border: 1px solid rgba(0,0,0,0.1); }

        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 60px; height: 60px; border-radius: 22px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 30px rgba(0,0,0,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.4rem; }

        footer { text-align: center; padding: 50px 20px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<header>
    <div style="font-weight: 900; font-size: 1.2rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.8rem; font-weight: 700;">12:00 PM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1000" class="hero-img">
    <div class="hero-overlay">
        <h1>Ultimate Guide 2026</h1>
        <p>Astore ki har malomat ab aapki muthi mein, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="section-title">📍 Travel Distance Card</div>
    <div class="card">
        <table class="info-table">
            <tr><td><b>Astore to Rama</b></td><td>11 KM</td><td>45 Mins</td></tr>
            <tr><td><b>Astore to Minimarg</b></td><td>65 KM</td><td>4-5 Hours</td></tr>
            <tr><td><b>Astore to Deosai</b></td><td>42 KM</td><td>2.5 Hours</td></tr>
        </table>
        <a href="https://www.google.com/maps/dir/Astore" class="btn map-btn"><i class="fas fa-map-marker-alt"></i> OPEN LIVE NAVIGATOR</a>
    </div>

    <div class="section-title">⚠️ Live Safety Status</div>
    <div class="card" style="border-left: 6px solid var(--accent);">
        <div style="display:flex; justify-content:space-between; align-items:center;">
            <span class="badge badge-safe">Season Open</span>
            <span style="font-size:0.7rem; font-weight:700;">Update: Today 2:00 PM</span>
        </div>
        <p style="font-size: 0.85rem; margin-top:10px; color:#64748b;">Astore-Minimarg road is clear. Burzil Pass is accessible for 4x4 Jeeps. Carry extra fuel, sweetie!</p>
    </div>

    <div class="section-title">✅ Traveler's Checklist</div>
    <div class="card">
        <div class="checklist-item"><input type="checkbox"> <span>Original CNIC (Must)</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>SCOM Sim Card</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Warm Jackets & Gloves</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Power Bank (Signals are weak)</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Cash (ATM is limited)</span></div>
    </div>

    <div class="section-title">💰 Budget Estimator</div>
    <div class="card">
        <table class="info-table">
            <tr><td>4x4 Willys Jeep</td><td>Rs. 12,000</td><td>Per Day</td></tr>
            <tr><td>Prado / TZ</td><td>Rs. 18,000</td><td>Per Day</td></tr>
            <tr><td>Standard Room</td><td>Rs. 6,500</td><td>Per Night</td></tr>
            <tr><td>Luxury Suite</td><td>Rs. 12,000</td><td>Per Night</td></tr>
        </table>
    </div>

    <div class="section-title">🚀 Instant Booking</div>
    <div class="booking-ui">
        <label style="font-size:0.75rem; font-weight:700;">Choose Your Adventure</label>
        <select id="srv">
            <option>Minimarg Day Trip</option>
            <option>Rama Meadows Night Stay</option>
            <option>Deosai Safari</option>
            <option>Complete 5-Day Tour</option>
        </select>
        <label style="font-size:0.75rem; font-weight:700;">Departure Date</label>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp fa-lg"></i> SEND BOOKING REQUEST
        </button>
    </div>

</div>

<div class="controls">
    <button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <a href="tel:+923171588489" class="fab" style="background:var(--danger);"><i class="fas fa-phone-alt"></i></a>
</div>

<footer>
    <b>ASTORE TOURIST INFORMATION HUB 2026</b><br>
    Verified Information & Professional Services<br>
    Built with Love for you, sweetie! 😘
</footer>

<script>
    // Smooth Scroll Progress
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Live Time
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // WhatsApp Intelligent Message
    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! I'm interested in: ${s} on Date: ${d}. Please confirm availability for me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
