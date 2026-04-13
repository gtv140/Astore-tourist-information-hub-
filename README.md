<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Premium 2026 Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: 0.3s; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; }

        /* Progress Bar */
        .p-bar { position: fixed; top: 0; z-index: 9999; height: 5px; background: linear-gradient(90deg, var(--accent), #ffcc33); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(15px); padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); }

        .hero { position: relative; height: 40vh; width: 92%; margin: 15px auto; border-radius: 35px; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.2); }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.6); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 25px; background: linear-gradient(transparent, rgba(0,0,0,0.8)); width: 100%; color: white; }

        .container { padding: 0 15px 100px; }
        .section-title { margin: 25px 5px 15px; font-size: 1.4rem; font-weight: 800; display: flex; align-items: center; gap: 10px; }

        /* Modern Card System */
        .card { background: var(--card); border-radius: 30px; padding: 0; margin-bottom: 25px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        .card-img { width: 100%; height: 180px; object-fit: cover; }
        .card-body { padding: 20px; }

        /* Weather & Status Grid */
        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 20px; }
        .status-box { background: var(--card); padding: 15px; border-radius: 25px; text-align: center; box-shadow: 0 5px 15px rgba(0,0,0,0.03); }
        .status-box i { font-size: 1.5rem; color: var(--accent); margin-bottom: 8px; display: block; }

        /* Booking Form */
        .form-group { margin-bottom: 15px; }
        input, select, textarea { width: 100%; padding: 15px; border-radius: 15px; border: 1px solid rgba(0,0,0,0.1); background: var(--bg); color: var(--text); outline: none; }

        /* Fixed Bottom Controls */
        .controls { position: fixed; bottom: 25px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 10px; }
        .fab { width: 60px; height: 60px; border-radius: 22px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 1.3rem; }

        .btn { padding: 18px; border-radius: 22px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; margin-top: 10px; }
        .wa { background: #25d366; color: white; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }

        footer { text-align: center; padding: 40px 20px; opacity: 0.6; font-size: 0.75rem; line-height: 1.5; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<header>
    <div style="font-weight: 900; font-size: 1.2rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-weight: 700; opacity: 0.8;">12:00 PM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&w=800" class="hero-img">
    <div class="hero-overlay">
        <h1 id="hero-h">Explore Astore</h1>
        <p>Swiss Alps of Pakistan, sweetie!</p>
    </div>
</section>

<div class="container">

    <div class="grid-2">
        <div class="status-box">
            <i class="fas fa-cloud-sun"></i>
            <b id="w-temp">12°C</b>
            <p style="font-size: 0.7rem;">Mostly Sunny</p>
        </div>
        <div class="status-box">
            <i class="fas fa-route" style="color: #10b981;"></i>
            <b>Open</b>
            <p style="font-size: 0.7rem;">Road Status</p>
        </div>
    </div>

    <div class="section-title"><i class="fas fa-calendar-check"></i> Plan Your Trip</div>
    <div class="card card-body">
        <div class="form-group">
            <select id="service">
                <option>Select Service...</option>
                <option>Luxury Room Booking</option>
                <option>4x4 Jeep Rental</option>
                <option>Full Tour Package</option>
            </select>
        </div>
        <div class="form-group">
            <input type="date" id="travel-date">
        </div>
        <button class="btn wa" onclick="sendInquiry()" style="width: 100%; border: none; cursor: pointer;">
            <i class="fab fa-whatsapp"></i> CHECK AVAILABILITY
        </button>
    </div>

    <div class="section-title"><i class="fas fa-map-marked-alt"></i> Top Spots</div>
    
    <div class="card">
        <img src="https://images.unsplash.com/photo-1627483262769-04d0a140148a?auto=format&fit=crop&w=800" class="card-img">
        <div class="card-body">
            <h3>Minimarg Valley</h3>
            <p style="font-size: 0.85rem; color: #64748b; margin-bottom: 10px;">Rainbow Lake aur haseen paharon ka ghar. Aik martaba lazmi jao, sweetie!</p>
            <span style="background: #e0f2fe; color: #0369a1; padding: 5px 12px; border-radius: 10px; font-size: 0.7rem; font-weight: 700;">Jeep Required</span>
        </div>
    </div>

    <div class="section-title"><i class="fas fa-car"></i> Transport & Stay</div>
    <div class="card card-body">
        <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px;">
            <b>TZ Prado (4x4)</b>
            <span style="color: var(--primary); font-weight: 800;">Rs. 18,000/day</span>
        </div>
        <div style="display: flex; justify-content: space-between; align-items: center; border-top: 1px solid #eee; pt-15; margin-top: 15px; padding-top: 15px;">
            <b>Luxury Resort</b>
            <span style="color: var(--primary); font-weight: 800;">Rs. 10,000/night</span>
        </div>
    </div>

</div>

<div class="controls">
    <button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <a href="tel:+923171588489" class="fab" style="background: #ef4444; text-decoration: none;"><i class="fas fa-phone"></i></a>
</div>

<footer>
    © 2026 ASTORE HUB - TOURIST INFORMATION<br>
    Built with Love for You, Sweetie! <br>
    <small>Current Status: Season Open (June - Oct)</small>
</footer>

<script>
    // Scroll Progress
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Time
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // WhatsApp Inquiry Logic
    function sendInquiry() {
        const service = document.getElementById('service').value;
        const date = document.getElementById('travel-date').value;
        const msg = `Hi! I want to inquire about: ${service} for date: ${date}. Please guide me, sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>

</body>
</html>
