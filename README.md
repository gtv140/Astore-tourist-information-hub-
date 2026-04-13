<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Elite Travel 2026</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: 0.3s ease; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; }

        .p-bar { position: fixed; top: 0; z-index: 10000; height: 5px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.85); backdrop-filter: blur(15px); padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.85); }

        .hero { position: relative; height: 45vh; width: 94%; margin: 15px auto; border-radius: 40px; overflow: hidden; box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25); }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.65); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 30px; background: linear-gradient(transparent, rgba(0,0,0,0.8)); width: 100%; color: white; }
        .hero-overlay h1 { font-size: 2.2rem; font-weight: 800; letter-spacing: -1px; }

        .container { padding: 0 15px 120px; }
        .section-title { margin: 30px 5px 15px; font-size: 1.3rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 10px; }

        .card { background: var(--card); border-radius: 35px; overflow: hidden; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); border: 1px solid rgba(0,0,0,0.02); }
        .card-img { width: 100%; height: 220px; object-fit: cover; }
        .card-body { padding: 25px; }

        .status-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: -30px; position: relative; z-index: 100; padding: 0 10px; }
        .status-box { background: var(--card); padding: 18px; border-radius: 25px; text-align: center; box-shadow: 0 15px 30px rgba(0,0,0,0.1); }
        .status-box i { font-size: 1.6rem; color: var(--accent); margin-bottom: 5px; display: block; }

        /* Modern Form */
        .booking-form { padding: 20px; }
        .input-group { margin-bottom: 15px; }
        label { display: block; margin-bottom: 8px; font-size: 0.8rem; font-weight: 600; opacity: 0.7; }
        input, select { width: 100%; padding: 16px; border-radius: 20px; border: 1px solid rgba(0,0,0,0.08); background: var(--bg); color: var(--text); font-size: 0.9rem; }

        /* Buttons & Controls */
        .btn { padding: 18px; border-radius: 22px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; border: none; cursor: pointer; width: 100%; }
        .wa-btn { background: #25d366; color: white; font-size: 1rem; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #fee2e2; color: #ef4444; margin-bottom: 20px; }

        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 60px; height: 60px; border-radius: 22px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 30px rgba(0,0,0,0.2); cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 1.4rem; }

        .price-chip { background: var(--primary); color: white; padding: 6px 15px; border-radius: 50px; font-size: 0.8rem; font-weight: 700; }
        
        marquee { background: #ef4444; color: white; padding: 10px; font-size: 0.85rem; font-weight: 600; }
        footer { text-align: center; padding: 50px 20px; opacity: 0.5; font-size: 0.75rem; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<marquee>🚨 Live Updates: Minimarg Pass is Open | Rama Lake Snow Melting | Book SCOM SIMs in Advance | WhatsApp: +92 317 1588489</marquee>

<header>
    <div style="font-weight: 800; font-size: 1.3rem; letter-spacing: -1px;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.85rem; font-weight: 700;">12:00 PM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&w=1200" class="hero-img">
    <div class="hero-overlay">
        <span style="background:var(--accent); color:black; padding:5px 12px; border-radius:12px; font-size:0.65rem; font-weight:900; text-transform:uppercase;">Luxury Portal 2026</span>
        <h1>Explore Heaven</h1>
        <p>Your luxury gateway to Astore Valley, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="status-grid">
        <div class="status-box">
            <i class="fas fa-cloud-sun"></i>
            <b style="font-size: 1.2rem;">14°C</b>
            <p style="font-size: 0.65rem; opacity: 0.7;">Mostly Clear</p>
        </div>
        <div class="status-box">
            <i class="fas fa-check-circle" style="color: #10b981;"></i>
            <b style="font-size: 1.2rem;">All Clear</b>
            <p style="font-size: 0.65rem; opacity: 0.7;">Road Status</p>
        </div>
    </div>

    <div class="section-title"><i class="fas fa-bolt"></i> Quick Booking</div>
    <div class="card booking-form">
        <div class="input-group">
            <label>What do you need?</label>
            <select id="service-type">
                <option value="Luxury Jeep">4x4 Jeep Rental (Tz/Prado)</option>
                <option value="Hotel Room">Luxury Room Booking</option>
                <option value="Full Package">Complete Tour Package</option>
            </select>
        </div>
        <div class="input-group">
            <label>Travel Date</label>
            <input type="date" id="travel-date">
        </div>
        <button onclick="bookNow()" class="btn wa-btn">
            <i class="fab fa-whatsapp"></i> BOOK NOW WITH WHATSAPP
        </button>
    </div>

    <div class="section-title"><i class="fas fa-map-marked-alt"></i> Top Destinations</div>
    
    <div class="card">
        <img src="https://images.unsplash.com/photo-1627483262769-04d0a140148a?auto=format&fit=crop&w=800" class="card-img">
        <div class="card-body">
            <div style="display:flex; justify-content:space-between; align-items:center;">
                <h3>Minimarg Valley</h3>
                <span class="price-chip">Rs. 18k / Jeep</span>
            </div>
            <p style="font-size: 0.85rem; color: #64748b; margin-top: 10px;">Rainbow lake aur haseen maidan. Burzil pass se guzarna aik adventure hai, sweetie!</p>
        </div>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=800" class="card-img">
        <div class="card-body">
            <div style="display:flex; justify-content:space-between; align-items:center;">
                <h3>Rama Meadows</h3>
                <span class="price-chip">Rs. 10k / Night</span>
            </div>
            <p style="font-size: 0.85rem; color: #64748b; margin-top: 10px;">Nanga Parbat ka view aur thandi hawayein. Camping ke liye best jagah hai.</p>
        </div>
    </div>

    <div class="section-title"><i class="fas fa-shield-alt"></i> Safe Travels</div>
    <a href="tel:+923171588489" class="btn sos-btn">
        <i class="fas fa-phone-alt"></i> 24/7 TOURIST HELPLINE
    </a>

</div>

<div class="controls">
    <button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
</div>

<footer>
    © 2026 ASTORE TOURIST INFORMATION HUB<br>
    Built with Love for a great experience, sweetie! 😘<br>
    <small>Verified by Gemini 2.0</small>
</footer>

<script>
    // Progress Bar script
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Real-time Clock
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // Smart Booking logic
    function bookNow() {
        const service = document.getElementById('service-type').value;
        const date = document.getElementById('travel-date').value;
        const message = `Hi! I want to book a ${service} for ${date ? date : 'upcoming dates'}. Please share details, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(message)}`);
    }
</script>

</body>
</html>
