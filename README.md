<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Hub | All-in-One Guide</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">

    <style>
        :root { 
            --primary: #065f46; 
            --accent: #fbbf24; 
            --bg: #f1f5f9; 
            --card: #ffffff; 
            --text: #0f172a; 
            --glass: rgba(255, 255, 255, 0.8);
        }
        .dark { 
            --bg: #020617; 
            --card: #1e293b; 
            --text: #f8fafc; 
            --primary: #34d399;
            --glass: rgba(30, 41, 59, 0.8);
        }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Plus Jakarta Sans', sans-serif; transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1); }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; line-height: 1.6; }

        /* 1. TOP HEADER & ROAD ALERT */
        .alert-top { background: var(--accent); color: #000; padding: 8px; text-align: center; font-size: 0.7rem; font-weight: 800; text-transform: uppercase; letter-spacing: 1px; }
        
        header { position: sticky; top: 0; z-index: 2000; background: var(--glass); backdrop-filter: blur(15px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }

        /* 2. ANIMATED IMAGE SLIDER */
        .hero { position: relative; height: 35vh; width: 100%; overflow: hidden; border-radius: 0 0 30px 30px; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 16s infinite; }
        .slide { width: 100%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(0,0,0,0.8), transparent); display: flex; flex-direction: column; justify-content: flex-end; padding: 25px; color: white; }

        @keyframes slide { 
            0%, 20% { transform: translateX(0%); } 
            25%, 45% { transform: translateX(-25%); } 
            50%, 70% { transform: translateX(-50%); } 
            75%, 95% { transform: translateX(-75%); } 
            100% { transform: translateX(0%); } 
        }

        .container { padding: 20px; max-width: 600px; margin: auto; }

        /* 3. DYNAMIC WEATHER & STATUS CHIPS */
        .status-bar { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 15px; scrollbar-width: none; }
        .status-bar::-webkit-scrollbar { display: none; }
        .chip { background: var(--card); padding: 10px 18px; border-radius: 18px; box-shadow: 0 4px 12px rgba(0,0,0,0.05); white-space: nowrap; font-size: 0.75rem; font-weight: 700; display: flex; align-items: center; gap: 8px; }

        /* 4. UNLIMITED SERVICES GRID */
        .section-title { margin: 25px 0 15px; font-size: 1.1rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 10px; }
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
        .feature-box { background: var(--card); border-radius: 20px; padding: 15px 5px; text-align: center; box-shadow: 0 4px 15px rgba(0,0,0,0.03); border: 1px solid rgba(0,0,0,0.02); cursor: pointer; text-decoration: none; color: inherit; }
        .feature-box:active { transform: scale(0.92); }
        .feature-box i { font-size: 1.4rem; color: var(--primary); margin-bottom: 8px; display: block; }
        .feature-box span { font-size: 0.65rem; font-weight: 800; text-transform: uppercase; }

        /* 5. INTERACTIVE CHECKLIST */
        .card { background: var(--card); border-radius: 25px; padding: 20px; margin-bottom: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        .check-item { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; font-weight: 600; font-size: 0.85rem; }
        .check-item input { width: 20px; height: 20px; accent-color: var(--primary); }

        /* 6. PREMIUM BOOKING PANEL */
        .booking-panel { background: var(--primary); color: white; border-radius: 30px; padding: 25px; box-shadow: 0 15px 35px rgba(6,95,70,0.3); }
        .booking-panel label { font-size: 0.6rem; font-weight: 800; opacity: 0.8; letter-spacing: 1px; }
        .booking-panel select, .booking-panel input { width: 100%; background: rgba(255,255,255,0.15); border: 1px solid rgba(255,255,255,0.2); border-radius: 12px; padding: 12px; color: white; margin: 5px 0 15px; font-weight: 600; outline: none; }
        .booking-panel select option { color: black; }

        .btn-wa { background: #25d366; color: white; border: none; padding: 16px; border-radius: 15px; width: 100%; font-weight: 800; display: flex; align-items: center; justify-content: center; gap: 10px; box-shadow: 0 10px 20px rgba(37,211,102,0.3); cursor: pointer; }
        .btn-sos { background: rgba(255,255,255,0.1); color: white; margin-top: 10px; border: 1px dashed rgba(255,255,255,0.3); text-decoration: none; padding: 12px; display: block; text-align: center; border-radius: 12px; font-size: 0.75rem; font-weight: 700; }

        /* FLOATING UTILS */
        .fab { position: fixed; bottom: 25px; right: 20px; width: 55px; height: 55px; border-radius: 20px; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; box-shadow: 0 10px 30px rgba(0,0,0,0.2); z-index: 3000; border: none; }

        footer { text-align: center; padding: 50px 20px; opacity: 0.4; font-size: 0.7rem; letter-spacing: 0.5px; }
    </style>
</head>
<body>

<div class="alert-top">
    <marquee scrollamount="5"><i class="fas fa-exclamation-triangle"></i> ALERT: Road to Minimarg is now OPEN for 4x4 vehicles. SCOM Network is working fine. Stay Safe!</marquee>
</div>

<header>
    <div style="font-weight: 900; font-size: 1.2rem; letter-spacing: -1px;">ASTORE<span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-weight: 800; font-size: 0.8rem; color: var(--primary);">00:00</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=1000">
            <div class="overlay"><h2>Rama Meadows</h2><p>Experience the green magic of Astore.</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1000">
            <div class="overlay"><h2>Rainbow Lake</h2><p>Crystal clear reflections of heaven.</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=1000">
            <div class="overlay"><h2>Minimarg Valley</h2><p>The most beautiful border village.</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=1000">
            <div class="overlay"><h2>Deosai Safari</h2><p>Land of the Giants and Brown Bears.</p></div>
        </div>
    </div>
</section>

<div class="container">

    <div class="status-bar">
        <div class="chip"><i class="fas fa-signal" style="color: #2563eb;"></i> SCOM Online</div>
        <div class="chip"><i class="fas fa-thermometer-half" style="color: #f59e0b;"></i> 12°C Cold</div>
        <div class="chip"><i class="fas fa-gas-pump" style="color: #ef4444;"></i> Fuel Available</div>
        <div class="chip"><i class="fas fa-mountain" style="color: #10b981;"></i> Road Clear</div>
    </div>

    <div class="section-title"><i class="fas fa-th-large"></i> Hub Services</div>
    <div class="grid">
        <a href="#book" class="feature-box"><i class="fas fa-car-side"></i><span>Jeep Rental</span></a>
        <a href="https://wa.me/923171588489" class="feature-box"><i class="fas fa-hotel"></i><span>Hotel Stay</span></a>
        <a href="https://wa.me/923171588489" class="feature-box"><i class="fas fa-hiking"></i><span>Tour Guide</span></a>
        <a href="https://wa.me/923171588489" class="feature-box"><i class="fas fa-utensils"></i><span>Local Food</span></a>
        <a href="https://wa.me/923171588489" class="feature-box"><i class="fas fa-campground"></i><span>Camping</span></a>
        <a href="https://wa.me/923171588489" class="feature-box"><i class="fas fa-camera"></i><span>Photo Tour</span></a>
    </div>

    <div class="section-title"><i class="fas fa-tasks"></i> Travel Essentials</div>
    <div class="card">
        <div class="check-item"><input type="checkbox"> <span>SCOM SIM Card (Internet)</span></div>
        <div class="check-item"><input type="checkbox"> <span>Heavy Woolen Jacket</span></div>
        <div class="check-item"><input type="checkbox"> <span>Original CNIC/Passport</span></div>
        <div class="check-item"><input type="checkbox"> <span>Cash (ATMs are rare)</span></div>
        <div class="check-item"><input type="checkbox"> <span>Power Bank</span></div>
    </div>

    <div class="section-title" id="book"><i class="fas fa-calendar-alt"></i> Instant Booking</div>
    <div class="booking-panel">
        <div class="form-group">
            <label>SELECT DESTINATION</label>
            <select id="srv">
                <option>Minimarg & Rainbow Lake</option>
                <option>Rama Meadows & Lake</option>
                <option>Deosai Plains Safari</option>
                <option>Tarishing (Nanga Parbat)</option>
                <option>Astore City Full Tour</option>
            </select>
        </div>
        <div class="form-group">
            <label>TRAVEL DATE</label>
            <input type="date" id="dt">
        </div>
        <button class="btn-wa" onclick="sendBooking()">
            <i class="fab fa-whatsapp fa-lg"></i> CONFIRM ON WHATSAPP
        </button>
        <a href="tel:+923171588489" class="btn-sos"><i class="fas fa-phone-alt"></i> 24/7 EMERGENCY HELPLINE</a>
    </div>

</div>

<button class="fab" onclick="document.body.classList.toggle('dark')">
    <i class="fas fa-moon"></i>
</button>

<footer>
    <b>ASTORE TOURIST INFORMATION HUB 2026</b><br>
    Everything Unlimited, Everything Clickable.<br>
    Designed with Love for You, Sweetie! 😘
</footer>

<script>
    // Update Clock
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // Booking Logic
    function sendBooking() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const phone = "923171588489";
        const msg = `Hi Astore Hub! I want to book [${s}] for [${d || 'upcoming dates'}]. Please share rates and availability, sweetie!`;
        window.open(`https://wa.me/${phone}?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
