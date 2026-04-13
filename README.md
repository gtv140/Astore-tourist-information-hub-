<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Final Master Guide 2026</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; --danger: #ef4444; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: 0.3s ease; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; line-height: 1.6; }

        .p-bar { position: fixed; top: 0; z-index: 10000; height: 5px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(20px); padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); }

        .hero { position: relative; height: 48vh; width: 100%; overflow: hidden; }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.65); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 30px; background: linear-gradient(transparent, rgba(0,0,0,1)); width: 100%; color: white; }

        .container { padding: 0 16px 120px; margin-top: -30px; position: relative; z-index: 100; }

        .section-title { margin: 30px 0 15px; font-size: 1.3rem; font-weight: 800; border-left: 5px solid var(--primary); padding-left: 12px; color: var(--primary); }
        .card { background: var(--card); border-radius: 30px; padding: 20px; margin-bottom: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); overflow: hidden; }
        .card-img { width: 100%; height: 180px; object-fit: cover; border-radius: 20px; margin-bottom: 15px; }

        .status-scroll { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 15px; scrollbar-width: none; }
        .status-scroll::-webkit-scrollbar { display: none; }
        .chip { background: var(--card); padding: 12px 20px; border-radius: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); display: flex; align-items: center; gap: 8px; white-space: nowrap; font-size: 0.85rem; font-weight: 600; }

        .info-table { width: 100%; border-collapse: collapse; font-size: 0.85rem; }
        .info-table td { padding: 12px 5px; border-bottom: 1px solid rgba(0,0,0,0.05); }

        .checklist-item { display: flex; align-items: center; gap: 10px; margin-bottom: 12px; font-size: 0.9rem; font-weight: 500; }
        .checklist-item input { width: 18px; height: 18px; accent-color: var(--primary); }

        .booking-ui { background: var(--primary); color: white; border-radius: 30px; padding: 25px; margin-top: 10px; }
        .booking-ui label { font-size: 0.75rem; font-weight: 700; opacity: 0.9; }
        .booking-ui input, .booking-ui select { width: 100%; padding: 15px; border-radius: 15px; border: none; margin-top: 8px; margin-bottom: 15px; font-weight: 600; font-size: 0.9rem; }

        .btn { padding: 18px; border-radius: 22px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; border: none; cursor: pointer; }
        .wa-btn { background: #25d366; color: white; box-shadow: 0 10px 25px rgba(37,211,102,0.4); width: 100%; }
        .sos-btn { background: #fee2e2; color: #ef4444; width: 100%; margin-top: 10px; }

        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 60px; height: 60px; border-radius: 22px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 30px rgba(0,0,0,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.4rem; }

        footer { text-align: center; padding: 50px 20px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body id="master-body">

<div class="p-bar" id="pb"></div>

<header>
    <div style="font-weight: 900; font-size: 1.2rem; letter-spacing: -1px;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.8rem; font-weight: 700;">12:00 PM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&w=1000" class="hero-img">
    <div class="hero-overlay">
        <span style="background:var(--accent); color:black; padding:5px 12px; border-radius:12px; font-size:0.65rem; font-weight:900; text-transform:uppercase;">Elite Guide 2026</span>
        <h1>Swiss of Pakistan</h1>
        <p>Unlimited malomat aur luxury safar, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="status-scroll">
        <div class="chip"><i class="fas fa-sun" style="color:#f59e0b"></i> 14°C Sunny</div>
        <div class="chip"><i class="fas fa-check-circle" style="color:#10b981"></i> Road Open</div>
        <div class="chip"><i class="fas fa-signal" style="color:#3b82f6"></i> SCOM High</div>
    </div>

    <div class="section-title">📍 Top Spots</div>
    
    <div class="card">
        <img src="https://images.unsplash.com/photo-1627483262769-04d0a140148a?auto=format&fit=crop&w=800" class="card-img" alt="Minimarg">
        <h3 style="font-size: 1.1rem;">Minimarg & Rainbow Lake</h3>
        <p style="font-size: 0.8rem; color: #64748b; margin-top: 5px;">Fairytale land behind Burzil Pass. 4x4 Jeep is required here.</p>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=800" class="card-img" alt="Rama Meadows">
        <h3 style="font-size: 1.1rem;">Rama Meadows & Lake</h3>
        <p style="font-size: 0.8rem; color: #64748b; margin-top: 5px;">Nanga Parbat view point aur luxury resorts ki jagah.</p>
    </div>

    <div class="section-title">⏱️ Distance & Time</div>
    <div class="card">
        <table class="info-table">
            <tr><td>Astore to Rama</td><td>11 KM</td><td>40 Mins</td></tr>
            <tr><td>Astore to Minimarg</td><td>65 KM</td><td>4.5 Hours</td></tr>
            <tr><td>Astore to Deosai</td><td>42 KM</td><td>2.5 Hours</td></tr>
        </table>
    </div>

    <div class="section-title">✅ Zaroori Checklist</div>
    <div class="card">
        <div class="checklist-item"><input type="checkbox"> <span>Original CNIC</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>SCOM Sim Card</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Warm Clothes</span></div>
        <div class="checklist-item"><input type="checkbox"> <span>Extra Cash (No ATM)</span></div>
    </div>

    <div class="section-title">🚀 Instant Booking</div>
    <div class="booking-ui">
        <label>Service Type</label>
        <select id="srv">
            <option>Minimarg Day Trip (Jeep)</option>
            <option>Rama Night Stay (Room)</option>
            <option>Full Tour (Car + Stay)</option>
        </select>
        <label>Travel Date</label>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp fa-lg"></i> BOOK NOW ON WHATSAPP
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
    <b>ASTORE TOURIST HUB 2026</b><br>
    Built with Love by Gemini for You, Sweetie! 😘
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

    // Smart Booking logic
    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi Astore Hub! I'm interested in: ${s} on Date: ${d}. Please guide me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
