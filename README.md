<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Ultra Modern Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #10b981; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #34d399; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Plus Jakarta Sans', sans-serif; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; font-size: 14px; -webkit-font-smoothing: antialiased; }

        header { position: sticky; top: 0; z-index: 1000; background: rgba(255,255,255,0.8); backdrop-filter: blur(15px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(15,23,42,0.8); }

        /* Animated Banner */
        .hero { position: relative; height: 32vh; width: 100%; overflow: hidden; border-radius: 0 0 30px 30px; }
        .slider { display: flex; width: 300%; height: 100%; animation: slide 12s infinite; }
        .slide { width: 100.33%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        .overlay { position: absolute; inset: 0; background: linear-gradient(0deg, rgba(0,0,0,0.7) 0%, transparent 60%); display: flex; flex-direction: column; justify-content: flex-end; padding: 20px; color: white; }

        @keyframes slide { 0%, 30% { transform: translateX(0%); } 33%, 63% { transform: translateX(-33.33%); } 66%, 96% { transform: translateX(-66.66%); } 100% { transform: translateX(0%); } }

        .container { padding: 20px; }

        /* Service Grid - UNLIMITED SERVICES */
        .section-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px; }
        .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-bottom: 25px; }
        .service-card { background: var(--card); padding: 15px; border-radius: 20px; text-align: center; box-shadow: 0 4px 12px rgba(0,0,0,0.03); border: 1px solid rgba(0,0,0,0.02); cursor: pointer; }
        .service-card:active { transform: scale(0.95); }
        .service-card i { font-size: 1.5rem; color: var(--primary); margin-bottom: 10px; display: block; }
        .service-card span { font-size: 0.75rem; font-weight: 700; display: block; }

        /* Modern Booking Form */
        .booking-panel { background: var(--primary); color: white; border-radius: 25px; padding: 25px; box-shadow: 0 20px 40px rgba(6,78,59,0.2); }
        .form-group { margin-bottom: 15px; }
        .form-group label { font-size: 0.65rem; font-weight: 800; text-transform: uppercase; opacity: 0.8; letter-spacing: 1px; }
        .booking-panel select, .booking-panel input { width: 100%; background: rgba(255,255,255,0.15); border: 1px solid rgba(255,255,255,0.2); border-radius: 12px; padding: 12px; color: white; margin-top: 5px; outline: none; }
        .booking-panel select option { color: #000; }

        .cta-btn { background: #25d366; color: white; border: none; padding: 15px; border-radius: 15px; width: 100%; font-weight: 800; display: flex; align-items: center; justify-content: center; gap: 10px; box-shadow: 0 10px 20px rgba(37,211,102,0.3); margin-top: 10px; }

        /* Floating Actions */
        .fab-container { position: fixed; bottom: 20px; right: 20px; display: flex; flex-direction: column; gap: 10px; z-index: 2000; }
        .fab { width: 50px; height: 50px; border-radius: 15px; display: flex; align-items: center; justify-content: center; box-shadow: 0 10px 20px rgba(0,0,0,0.1); border: none; }
        .fab-wa { background: #25d366; color: white; }
        .fab-theme { background: var(--card); color: var(--text); }

        footer { text-align: center; padding: 40px; opacity: 0.4; font-size: 0.7rem; }
    </style>
</head>
<body>

<header>
    <div style="font-weight: 800; font-size: 1.1rem; color: var(--primary);">ASTORE<span style="opacity: 0.5;">HUB</span></div>
    <div id="time" style="font-weight: 700; font-size: 0.8rem;">00:00</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800">
            <div class="overlay"><h3>Rama Meadows</h3><p>Nature in its purest form</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800">
            <div class="overlay"><h3>Rainbow Lake</h3><p>Magic of Astore Valley</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800">
            <div class="overlay"><h3>Minimarg</h3><p>The Hidden Paradise</p></div>
        </div>
    </div>
</section>

<div class="container">
    
    <div class="section-header">
        <h2 style="font-weight: 800;">Unlimited Services</h2>
        <span style="color: var(--primary); font-size: 0.7rem; font-weight: 700;">24/7 LIVE</span>
    </div>

    <div class="grid">
        <div class="service-card" onclick="setDest('Minimarg Jeep')"><i class="fas fa-car-side"></i><span>Jeep Rental</span></div>
        <div class="service-card" onclick="setDest('Hotel Booking')"><i class="fas fa-hotel"></i><span>Hotel Stay</span></div>
        <div class="service-card" onclick="setDest('Full Tour')"><i class="fas fa-map-marked-alt"></i><span>Tour Packages</span></div>
        <div class="service-card" onclick="setDest('Guide Service')"><i class="fas fa-user-tie"></i><span>Local Guide</span></div>
    </div>

    <div class="booking-panel">
        <h3 style="margin-bottom: 15px;">Quick Reservation</h3>
        <div class="form-group">
            <label>Choose Service</label>
            <select id="srv">
                <option>Minimarg & Rainbow Lake</option>
                <option>Rama Meadows Tour</option>
                <option>Deosai Safari</option>
                <option>Tarishing (Nanga Parbat)</option>
            </select>
        </div>
        <div class="form-group">
            <label>Travel Date</label>
            <input type="date" id="dt">
        </div>
        <button class="cta-btn" onclick="book()">
            <i class="fab fa-whatsapp"></i> BOOK NOW
        </button>
    </div>

</div>

<div class="fab-container">
    <button class="fab fab-theme" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <a href="https://wa.me/923171588489" class="fab fab-wa"><i class="fab fa-whatsapp fa-lg"></i></a>
</div>

<footer>
    © 2026 ASTORE HUB PREMIUM<br>
    Everything clickable & Unlimited, sweetie! 😘
</footer>

<script>
    // Live Clock
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // Clickable Grid Logic
    function setDest(val) {
        document.getElementById('srv').scrollIntoView({behavior: 'smooth'});
        alert("Service Selected: " + val + ". Now select date and click Book!");
    }

    // WhatsApp Booking
    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! I want to book ${s} for ${d || 'soon'}. Guide me sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
