<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Mobile Optimized</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; font-size: 14px; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.9); backdrop-filter: blur(10px); padding: 10px 15px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.9); }

        /* Fixed Animated Slider with Correct Hill Images */
        .hero { position: relative; height: 35vh; width: 100%; overflow: hidden; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 12s infinite ease-in-out; position: absolute; }
        .slide { width: 100%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .slide-content { position: absolute; bottom: 0; left: 0; padding: 15px; color: white; background: linear-gradient(transparent, rgba(0,0,0,0.8)); width: 100%; }

        @keyframes slide { 
            0%, 20% { transform: translateX(0%); } 
            25%, 45% { transform: translateX(-25%); } 
            50%, 70% { transform: translateX(-50%); } 
            75%, 95% { transform: translateX(-75%); } 
            100% { transform: translateX(0%); } 
        }

        .container { padding: 12px; margin-top: -10px; position: relative; z-index: 100; }

        .section-title { margin: 20px 0 10px; font-size: 1.1rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 8px; }
        .card { background: var(--card); border-radius: 20px; padding: 15px; margin-bottom: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); }

        .status-scroll { display: flex; gap: 8px; overflow-x: auto; padding-bottom: 10px; scrollbar-width: none; }
        .status-scroll::-webkit-scrollbar { display: none; }
        .chip { background: var(--card); padding: 8px 12px; border-radius: 15px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); white-space: nowrap; font-size: 0.75rem; font-weight: 600; display: flex; align-items: center; gap: 5px; }

        .info-table { width: 100%; border-collapse: collapse; font-size: 0.8rem; }
        .info-table td { padding: 10px 5px; border-bottom: 1px solid rgba(0,0,0,0.05); }

        .booking-ui { background: var(--primary); color: white; border-radius: 20px; padding: 20px; }
        input, select { width: 100%; padding: 12px; border-radius: 12px; border: none; margin: 8px 0 12px; font-size: 0.85rem; }

        .btn { padding: 14px; border-radius: 15px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 8px; border: none; width: 100%; font-size: 0.9rem; }
        .wa-btn { background: #25d366; color: white; }
        .sos-btn { background: #fee2e2; color: #ef4444; margin-top: 10px; font-size: 0.8rem; }

        .fab { position: fixed; bottom: 20px; right: 15px; width: 50px; height: 50px; border-radius: 15px; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; box-shadow: 0 5px 15px rgba(0,0,0,0.2); z-index: 9999; border: none; }

        footer { text-align: center; padding: 30px; opacity: 0.6; font-size: 0.7rem; }
    </style>
</head>
<body>

<header>
    <div style="font-weight: 900; font-size: 1rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.7rem; font-weight: 700;">--:--</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800" alt="Mountain">
            <div class="slide-content"><h2>Rama Meadows</h2><p>Greenery & Peace</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800" alt="Lake">
            <div class="slide-content"><h2>Rainbow Lake</h2><p>Nature's Magic</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800" alt="Hills">
            <div class="slide-content"><h2>Minimarg</h2><p>Hidden Paradise</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=800" alt="Forest">
            <div class="slide-content"><h2>Astore Valley</h2><p>The Alps of Pakistan</p></div>
        </div>
    </div>
</section>

<div class="container">

    <div class="status-scroll">
        <div class="chip"><i class="fas fa-signal" style="color:#2563eb"></i> SCOM SIM Only</div>
        <div class="chip"><i class="fas fa-sun" style="color:#f59e0b"></i> 14°C Sunny</div>
        <div class="chip"><i class="fas fa-road" style="color:#10b981"></i> Road Open</div>
    </div>

    <div class="section-title"><i class="fas fa-car"></i> Jeep Rates</div>
    <div class="card">
        <table class="info-table">
            <tr><td><b>Minimarg (Return)</b></td><td style="text-align:right">Rs. 18,000</td></tr>
            <tr><td><b>Rama Lake (Return)</b></td><td style="text-align:right">Rs. 7,000</td></tr>
        </table>
    </div>

    <div class="section-title"><i class="fas fa-calendar-check"></i> Quick Booking</div>
    <div class="booking-ui">
        <label style="font-size: 0.7rem;">Destination</label>
        <select id="srv">
            <option>Minimarg & Rainbow Lake</option>
            <option>Rama Meadows Night</option>
        </select>
        <label style="font-size: 0.7rem;">Date</label>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp"></i> REQUEST QUOTE
        </button>
        <a href="tel:+923171588489" class="btn sos-btn">24/7 HELPLINE</a>
    </div>

</div>

<button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>

<footer>
    © 2026 ASTORE HUB | Verified Mobile-First<br>
    Sweetie, ab check karo! 😘
</footer>

<script>
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! Rates for ${s} on ${d || 'soon'}. Please guide me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
