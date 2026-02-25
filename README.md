<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Premium Tour Guide</title>
    <meta name="description" content="Astore Tourist Information Hub - Book Jeeps & Hotels for Rama, Minimarg, and Deosai.">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #064e3b;
            --accent: #f59e0b;
            --glass: rgba(255, 255, 255, 0.1);
            --bg: #0f172a;
            --card-bg: #ffffff;
        }

        * { box-sizing: border-box; font-family: 'Inter', -apple-system, sans-serif; }
        body { margin: 0; background: #f8fafc; color: #1e293b; overflow-x: hidden; }

        /* Modern Glassy Header */
        nav {
            position: fixed; top: 0; width: 100%; z-index: 1000;
            background: rgba(6, 78, 59, 0.8); backdrop-filter: blur(15px);
            padding: 15px 5%; display: flex; justify-content: space-between; align-items: center;
        }
        nav .logo { color: white; font-weight: 800; font-size: 1.5rem; letter-spacing: -1px; }

        /* Hero Section with Parallax */
        .hero {
            height: 90vh; background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.6)), 
            url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&q=80&w=1500');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center;
        }

        .hero h1 { font-size: clamp(3rem, 10vw, 6rem); margin: 0; font-weight: 900; line-height: 1; text-shadow: 0 10px 20px rgba(0,0,0,0.3); }

        /* Quick Action Bar (Mobile Easy) */
        .action-bar {
            display: grid; grid-template-columns: repeat(4, 1fr);
            position: fixed; bottom: 0; width: 100%; background: white;
            box-shadow: 0 -5px 20px rgba(0,0,0,0.1); z-index: 2000; padding: 10px 0;
        }
        .action-item { text-align: center; text-decoration: none; color: #64748b; font-size: 0.7rem; font-weight: bold; }
        .action-item i { display: block; font-size: 1.2rem; color: var(--primary); margin-bottom: 2px; }

        /* Modern Grid & Cards */
        .container { max-width: 1200px; margin: auto; padding: 80px 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        
        .premium-card {
            background: white; border-radius: 24px; overflow: hidden;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .premium-card:hover { transform: translateY(-15px) scale(1.02); box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25); }
        .premium-card img { width: 100%; height: 250px; object-fit: cover; }
        .card-info { padding: 25px; }

        /* Interactive Booking Form */
        .glass-box {
            background: var(--primary); color: white; border-radius: 32px;
            padding: 50px; position: relative; overflow: hidden;
        }
        .booking-input {
            width: 100%; padding: 15px; border-radius: 12px; border: none;
            margin-bottom: 15px; background: rgba(255,255,255,0.9); font-size: 1rem;
        }

        /* Weather & Alerts */
        .badge { background: var(--accent); color: white; padding: 5px 15px; border-radius: 50px; font-weight: bold; font-size: 0.8rem; }

        /* Desktop vs Mobile adjustments */
        @media (max-width: 768px) {
            .hero h1 { font-size: 3.5rem; }
            .container { padding: 40px 15px; }
            nav { padding: 10px 5%; }
            .desktop-only { display: none; }
        }
        @media (min-width: 769px) {
            .action-bar { display: none; } /* Hide mobile menu on PC */
        }
    </style>
</head>
<body>

<nav>
    <div class="logo">ASTORE HUB.</div>
    <div class="desktop-only">
        <a href="#destinations" style="color:white; margin-left:20px; text-decoration:none;">Explore</a>
        <a href="#booking" style="color:white; margin-left:20px; text-decoration:none;">Book Now</a>
    </div>
</nav>

<section class="hero">
    <span class="badge pulse">2026 Season Open</span>
    <h1>BEYOND THE <br> CLOUDS</h1>
    <p style="font-size: 1.2rem; letter-spacing: 2px;">AUTHENTIC ASTORE EXPERIENCE</p>
    <a href="#booking" style="background:white; color:var(--primary); padding:18px 45px; border-radius:50px; font-weight:900; text-decoration:none; margin-top:20px; box-shadow:0 10px 20px rgba(0,0,0,0.2);">START JOURNEY</a>
</section>

<div class="container" id="destinations">
    <h2 style="font-size: 3rem; margin-bottom: 50px;">World Class <br> <span style="color:var(--primary)">Destinations</span></h2>
    <div class="grid">
        <div class="premium-card">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
            <div class="card-info">
                <span style="color:var(--accent); font-weight:800;">TOP PICK</span>
                <h3>Rama Meadows</h3>
                <p>Feel the silence of the pines and the majesty of Nanga Parbat.</p>
                <a href="https://wa.me/923171588489" style="text-decoration:none; color:var(--primary); font-weight:bold;">View Details →</a>
            </div>
        </div>
        <div class="premium-card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Rainbow">
            <div class="card-info">
                <span style="color:var(--accent); font-weight:800;">OFF-BEAT</span>
                <h3>Minimarg Valley</h3>
                <p>The rainbow lake is waiting for you at the edge of the world.</p>
                <a href="https://wa.me/923171588489" style="text-decoration:none; color:var(--primary); font-weight:bold;">View Details →</a>
            </div>
        </div>
        <div class="premium-card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b" alt="Deosai">
            <div class="card-info">
                <span style="color:var(--accent); font-weight:800;">ADVENTURE</span>
                <h3>Deosai Plains</h3>
                <p>Roam freely with the brown bears in the highest plateau.</p>
                <a href="https://wa.me/923171588489" style="text-decoration:none; color:var(--primary); font-weight:bold;">View Details →</a>
            </div>
        </div>
    </div>
</div>

<div class="container" id="booking">
    <div class="glass-box">
        <h2 style="font-size: 2.5rem; margin-top:0;">Plan Your Escape</h2>
        <p>Hamari team 24/7 mojud hai aapki trip plan karne ke liye.</p>
        <div style="max-width: 400px;">
            <input type="text" id="custName" class="booking-input" placeholder="Your Full Name">
            <select id="custDest" class="booking-input">
                <option>Rama Lake</option>
                <option>Minimarg/Rainbow Lake</option>
                <option>Deosai Plains</option>
            </select>
            <button onclick="bookWA()" style="width:100%; padding:18px; border-radius:12px; border:none; background:var(--accent); color:white; font-weight:bold; cursor:pointer;">
                <i class="fab fa-whatsapp"></i> CONNECT TO AGENT
            </button>
        </div>
    </div>
</div>

<div class="action-bar">
    <a href="tel:+923171588489" class="action-item"><i class="fas fa-phone"></i>Call</a>
    <a href="https://wa.me/923171588489" class="action-item"><i class="fab fa-whatsapp"></i>WhatsApp</a>
    <a href="#destinations" class="action-item"><i class="fas fa-map-marked-alt"></i>Places</a>
    <a href="https://www.google.com/maps/search/Astore+Valley" class="action-item"><i class="fas fa-location-arrow"></i>Map</a>
</div>

<footer style="padding: 100px 20px 150px; text-align: center; background: #1e293b; color: white;">
    <h2>ASTORE HUB.</h2>
    <p>Contact: +92 317 1588489 | Gilgit Baltistan, Pakistan</p>
    <div style="margin-top: 20px; opacity: 0.5; font-size: 0.8rem;">
        © 2026 Astore Hub - Powered by Gemini AI
    </div>
</footer>

<script>
    function bookWA() {
        const name = document.getElementById('custName').value;
        const dest = document.getElementById('custDest').value;
        const msg = `Hi! I am ${name}. I want to plan a trip to ${dest}. Please guide me!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, '_blank');
    }
</script>

</body>
</html>
