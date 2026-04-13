<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Mobile Premium Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; transition: 0.3s; }

        /* Smooth Progress Bar */
        .p-bar { position: fixed; top: 0; z-index: 10000; height: 4px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(20px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); }

        /* Hero Carousel Style */
        .hero { position: relative; height: 42vh; width: 100%; overflow: hidden; }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 25px; background: linear-gradient(transparent, rgba(0,0,0,0.9)); width: 100%; color: white; }
        .hero-overlay h1 { font-size: 1.8rem; font-weight: 800; line-height: 1.2; }

        .container { padding: 0 16px 120px; margin-top: -20px; position: relative; z-index: 100; }

        /* Quick Status Chips */
        .status-scroll { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 15px; scrollbar-width: none; }
        .status-scroll::-webkit-scrollbar { display: none; }
        .chip { background: var(--card); padding: 12px 20px; border-radius: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); display: flex; align-items: center; gap: 8px; white-space: nowrap; font-size: 0.85rem; font-weight: 600; }

        /* Mobile Optimized Cards */
        .section-title { margin: 25px 0 15px; font-size: 1.2rem; font-weight: 800; display: flex; align-items: center; gap: 10px; }
        .card { background: var(--card); border-radius: 28px; overflow: hidden; margin-bottom: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); }
        .card-img { width: 100%; height: 180px; object-fit: cover; }
        .card-body { padding: 20px; }

        /* Form Styling */
        .booking-ui { padding: 20px; background: var(--card); border-radius: 28px; }
        input, select { width: 100%; padding: 14px; border-radius: 16px; border: 1.5px solid #e2e8f0; margin-bottom: 12px; background: var(--bg); color: var(--text); font-size: 0.9rem; }

        /* Buttons */
        .btn { padding: 16px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; border: none; font-size: 0.95rem; }
        .wa-btn { background: #25d366; color: white; width: 100%; box-shadow: 0 8px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #fee2e2; color: #ef4444; width: 100%; margin-top: 10px; }

        /* Floating Menu */
        .controls { position: fixed; bottom: 25px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 56px; height: 56px; border-radius: 18px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.2rem; }

        .price-badge { background: var(--accent); color: black; padding: 4px 10px; border-radius: 10px; font-size: 0.75rem; font-weight: 800; }
        
        marquee { background: #ef4444; color: white; padding: 6px; font-size: 0.75rem; font-weight: 600; }
        footer { text-align: center; padding: 40px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<marquee>📍 2026 Season: Minimarg Road Open | Rama Lake Snow Melting | Book 4x4 Jeeps in Advance!</marquee>

<header>
    <div style="font-weight: 900; font-size: 1.1rem; letter-spacing: -0.5px;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.75rem; font-weight: 700;">10:00 AM</div>
</header>

<section class="hero">
    <img src="[attachment_2](attachment)" class="hero-img" alt="Astore Valley">
    <div class="hero-overlay">
        <h1>Swiss of Pakistan</h1>
        <p style="font-size: 0.85rem; opacity: 0.9;">Astore ki wadiyon mein aapka swagat hai, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="status-scroll">
        <div class="chip"><i class="fas fa-sun" style="color:#f59e0b"></i> 14°C Astore</div>
        <div class="chip"><i class="fas fa-road" style="color:#10b981"></i> Road Clear</div>
        <div class="chip"><i class="fas fa-wifi" style="color:#3b82f6"></i> SCOM Only</div>
    </div>

    <div class="section-title">📍 Top Spots</div>
    
    <div class="card">
        <img src="[attachment_1](attachment)" class="card-img" alt="Minimarg">
        <div class="card-body">
            <div style="display:flex; justify-content:space-between; align-items:start;">
                <h3 style="font-size: 1rem;">Minimarg & Rainbow Lake</h3>
                <span class="price-badge">Jeep Trip</span>
            </div>
            <p style="font-size: 0.8rem; color: #64748b; margin-top: 5px;">Burzil Pass ke paar aik jannat. Yahan ka rasta adventurous hai, sweetie!</p>
        </div>
    </div>

    <div class="card">
        <img src="[attachment_0](attachment)" class="card-img" alt="Rama Meadows">
        <div class="card-body">
            <div style="display:flex; justify-content:space-between; align-items:start;">
                <h3 style="font-size: 1rem;">Rama Meadows</h3>
                <span class="price-badge">Luxury Stay</span>
            </div>
            <p style="font-size: 0.8rem; color: #64748b; margin-top: 5px;">Nanga Parbat ke view aur haryali ke liye best jagah.</p>
        </div>
    </div>

    <div class="section-title">🚗 Transport & Booking</div>
    <div class="booking-ui">
        <select id="srv">
            <option>Select Service...</option>
            <option>TZ Prado (4x4)</option>
            <option>Willys Jeep</option>
            <option>Luxury Hotel Room</option>
        </select>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp"></i> BOOK NOW ON WHATSAPP
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
    © 2026 ASTORE HUB<br>MODERNIZED FOR YOU, SWEETIE! 😘
</footer>

<script>
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi! I want to book ${s} for ${d}. Please guide me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
