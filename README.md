<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Modern Luxury Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: 0.3s; }
        body { background: var(--bg); color: var(--text); -webkit-font-smoothing: antialiased; }

        /* Modern Progress Bar */
        .p-bar { position: fixed; top: 0; z-index: 9999; height: 4px; background: linear-gradient(90deg, var(--accent), #fcd34d); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(12px); padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); }

        /* Hero Image Section */
        .hero { position: relative; height: 45vh; width: 92%; margin: 15px auto; border-radius: 35px; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.2); }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 25px; background: linear-gradient(transparent, rgba(0,0,0,0.9)); width: 100%; color: white; }

        .container { padding: 0 15px 100px; }
        
        /* Modern Cards */
        .card { background: var(--card); border-radius: 30px; padding: 0; margin-bottom: 25px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 1px solid rgba(0,0,0,0.02); }
        .card-content { padding: 20px; }
        .card-img { width: 100%; height: 200px; object-fit: cover; }
        .card h3 { font-size: 1.2rem; margin-bottom: 10px; color: var(--primary); display: flex; align-items: center; gap: 8px; }

        /* Update Grid */
        .update-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 10px; }
        .update-item { background: var(--bg); padding: 15px; border-radius: 20px; text-align: center; }

        /* Buttons */
        .btn { padding: 18px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; margin-bottom: 10px; }
        .sos { background: #fee2e2; color: #ef4444; }
        .wa { background: #25d366; color: white; box-shadow: 0 10px 25px rgba(37,211,102,0.3); }

        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 55px; height: 55px; border-radius: 20px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 1.2rem; }

        .badge { background: var(--accent); color: black; padding: 4px 12px; border-radius: 12px; font-size: 0.7rem; font-weight: 900; text-transform: uppercase; }
        
        .price-tag { color: var(--primary); font-weight: 800; font-size: 1.1rem; display: block; margin-top: 10px; }
        
        marquee { background: #ef4444; color: white; padding: 8px; font-size: 0.8rem; font-weight: 600; }
        footer { text-align: center; padding: 30px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body>

<div class="p-bar" id="pb"></div>

<marquee>📍 2026 Season Updates: Minimarg Road Clear | Rama Meadows Greenery Peak | Limited Jeeps Available!</marquee>

<header>
    <div style="font-weight: 900; font-size: 1.2rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.8rem; font-weight: 700;">--:--</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&w=800" class="hero-img">
    <div class="hero-overlay">
        <span class="badge">Astore Luxury 2026</span>
        <h1>Pakistan ka Switzerland</h1>
        <p>Astore ki haseen wadiyon mein aapka swagat hai, sweetie!</p>
    </div>
</section>

<div class="container">
    
    <a href="tel:+923171588489" class="btn sos">
        <i class="fas fa-phone-alt"></i> 24/7 EMERGENCY SOS
    </a>

    <h2 style="margin: 20px 5px;">📍 Top Locations</h2>
    
    <div class="card">
        <img src="https://images.unsplash.com/photo-1627483262769-04d0a140148a?auto=format&fit=crop&w=800" class="card-img">
        <div class="card-content">
            <h3>Minimarg & Rainbow Lake</h3>
            <p style="font-size: 0.85rem; color: #64748b;">Burzil Pass ke paar aik chupi hui jannat. Yahan ka sukoon aur thandi hawayein aapka dil jeet lein gi.</p>
        </div>
    </div>

    <h2 style="margin: 20px 5px;">🚗 4x4 Jeep Rentals</h2>
    <div class="card">
        <div class="card-content">
            <h3>Tz Prado & Willys Jeep</h3>
            <p style="font-size: 0.85rem; color: #64748b;">Deosai aur Minimarg ke liye mazboot 4x4 jeeps aur expert drivers available hain.</p>
            <div class="update-grid">
                <div class="update-item"><b>15,000/-</b><span>Per Day</span></div>
                <div class="update-item"><b>Fuel</b><span>Extra</span></div>
            </div>
        </div>
    </div>

    <h2 style="margin: 20px 5px;">🏨 Luxury Rooms</h2>
    <div class="card">
        <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=800" class="card-img">
        <div class="card-content">
            <h3>Rama Meadows Resort</h3>
            <p style="font-size: 0.85rem; color: #64748b;">Nanga Parbat ke view ke sath luxury rooms. Solar heating aur 24/7 garam paani available hai.</p>
            <span class="price-tag">Rs. 8,000 - 12,000 / Night</span>
        </div>
    </div>

    <div class="card" style="background: var(--primary); color: white;">
        <div class="card-content">
            <h3 style="color: white;"><i class="fas fa-info-circle"></i> Zaroori Baat</h3>
            <p style="font-size: 0.85rem; opacity: 0.9;">
                1. Original CNIC sath rakhein.<br>
                2. Sirf <b>SCOM</b> ki sim chalti hai yahan.<br>
                3. Thore garam kapray lazmi rakhein, sweetie!
            </p>
        </div>
    </div>

    <a href="https://wa.me/923171588489" class="btn wa">
        <i class="fab fa-whatsapp fa-lg"></i> BOOK EVERYTHING NOW
    </a>

</div>

<div class="controls">
    <button class="fab" id="mode-btn" onclick="toggleMode()"><i class="fas fa-moon"></i></button>
</div>

<footer>
    © 2026 ASTORE TOURIST HUB<br>MODERNIZED BY GEMINI
</footer>

<script>
    // Progress Bar
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Time function
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    // Dark mode toggle
    function toggleMode() {
        document.body.classList.toggle('dark');
        const icon = document.querySelector('#mode-btn i');
        icon.classList.toggle('fa-moon');
        icon.classList.toggle('fa-sun');
    }
</script>

</body>
</html>
