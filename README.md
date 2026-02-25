<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | The Ultimate Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f9fafb; --white: #ffffff; }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); color: #333; line-height: 1.6; }

        /* Modern Nav */
        nav { 
            background: var(--white); padding: 15px 5%; display: flex; 
            justify-content: space-between; align-items: center;
            position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .logo { font-weight: 800; color: var(--primary); text-decoration: none; font-size: 1.3rem; }

        /* Hero Section */
        .hero { 
            height: 50vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800');
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; 
            text-align: center; color: white; padding: 20px;
        }
        .hero h1 { font-size: 2.2rem; margin-bottom: 10px; }

        /* Weather Badge */
        .weather-badge {
            background: rgba(255,255,255,0.2); backdrop-filter: blur(10px);
            padding: 8px 15px; border-radius: 50px; font-size: 0.8rem; margin-bottom: 15px;
            display: flex; align-items: center; gap: 8px; border: 1px solid rgba(255,255,255,0.3);
        }

        .container { width: 100%; max-width: 500px; margin: 0 auto; padding: 30px 15px; }

        /* Detailed Info Section */
        .info-box { background: var(--white); padding: 25px; border-radius: 20px; margin-bottom: 30px; border-left: 5px solid var(--primary); }
        .info-box h2 { color: var(--primary); font-size: 1.5rem; margin-bottom: 10px; }
        .info-box p { font-size: 0.9rem; color: #555; text-align: justify; }

        /* Tour Categories */
        .cat-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 10px; margin-bottom: 30px; }
        .cat-item { background: var(--white); padding: 15px 5px; border-radius: 12px; text-align: center; font-size: 0.7rem; font-weight: bold; box-shadow: 0 2px 5px rgba(0,0,0,0.05); }
        .cat-item i { display: block; font-size: 1.2rem; color: var(--accent); margin-bottom: 5px; }

        /* Destination Cards */
        .card { 
            background: var(--white); border-radius: 20px; overflow: hidden; 
            margin-bottom: 25px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        .card img { width: 100%; height: 200px; object-fit: cover; }
        .card-body { padding: 20px; }
        .stars { color: var(--accent); font-size: 0.8rem; margin-bottom: 5px; }

        /* FAQ Section */
        .faq-item { background: #eee; padding: 12px; border-radius: 10px; margin-bottom: 10px; font-size: 0.85rem; }
        .faq-item b { display: block; color: var(--primary); }

        /* Booking Form */
        .booking-box { 
            background: var(--primary); color: white; border-radius: 25px; 
            padding: 30px 20px; text-align: center;
        }
        .input-field { 
            width: 100%; padding: 15px; border-radius: 12px; border: none; 
            margin-bottom: 10px; font-size: 1rem;
        }
        .btn-submit { 
            width: 100%; padding: 18px; background: #25d366; color: white; 
            border: none; border-radius: 12px; font-weight: bold; cursor: pointer;
        }

        .wa-float { 
            position: fixed; bottom: 20px; right: 20px; background: #25d366; 
            color: white; width: 60px; height: 60px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center; font-size: 30px; z-index: 2000;
        }
        footer { text-align: center; padding: 30px; font-size: 0.8rem; color: #888; }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <a href="tel:+923171588489" style="color: var(--primary);"><i class="fas fa-phone-alt"></i></a>
</nav>

<div class="hero">
    <div class="weather-badge"><i class="fas fa-cloud-sun"></i> Astore: 12°C | Sunny</div>
    <h1>Welcome to Astore</h1>
    <p>The Gateway to Deosai & Nanga Parbat</p>
</div>

<div class="container">
    
    <div class="info-box">
        <h2>About Astore Valley</h2>
        <p>Astore Gilgit-Baltistan ka wo haseen zila hai jo Nanga Parbat ke kadmon mein waqiye hai. Ye wadi apni "Rainbow Lake" aur "Deosai Plains" ki wajah se puri dunya mein mashhoor hai. Pur-sukoon mahool aur thandi hawayein ise garmiyon ka behtreen tour banati hain.</p>
    </div>

    <div class="cat-grid">
        <div class="cat-item"><i class="fas fa-heart"></i>Honeymoon</div>
        <div class="cat-item"><i class="fas fa-khanda"></i>Adventure</div>
        <div class="cat-item"><i class="fas fa-users"></i>Family</div>
    </div>

    <h2 style="margin-bottom:20px; color: var(--primary);">Popular Spots</h2>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
        <div class="card-body">
            <div class="stars">★★★★★ (4.9/5)</div>
            <h3>Rama Meadows & Lake</h3>
            <p>Astore city se 30 mins ki drive par ye jagah camping ke liye best hai.</p>
            <p style="color:var(--accent); font-weight:bold; margin-top:10px;">Price: Rs. 8,500 (Jeep)</p>
        </div>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
        <div class="card-body">
            <div class="stars">★★★★★ (5.0/5)</div>
            <h3>Minimarg Valley</h3>
            <p>Rainbow Lake aur Burzil Pass yahan ke main attractions hain.</p>
            <p style="color:var(--accent); font-weight:bold; margin-top:10px;">Price: Rs. 14,000 (Jeep)</p>
        </div>
    </div>

    <div style="margin: 30px 0;">
        <h3 style="margin-bottom:15px; color:var(--primary);">Common Questions</h3>
        <div class="faq-item">
            <b>Best time to visit?</b>
            May se September tak raste khule aur mausam suhana hota hai.
        </div>
        <div class="faq-item">
            <b>Is NOC required for Minimarg?</b>
            Ji han, Minimarg ke liye army NOC zaroori hai jo hum arrange karte hain.
        </div>
    </div>

    <div class="booking-box" id="book">
        <h2>Book Your Jeep</h2>
        <input type="text" id="name" class="input-field" placeholder="Full Name">
        <select id="tour" class="input-field">
            <option>Rama Meadows Tour</option>
            <option>Minimarg & Rainbow Lake</option>
            <option>Full Deosai Crossing</option>
        </select>
        <button class="btn-submit" onclick="booking()">WhatsApp Booking</button>
    </div>

</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <p>Astore Tourist Information Hub</p>
    <p>Managed by: +92 317 1588489</p>
</footer>

<script>
    function booking() {
        const n = document.getElementById('name').value;
        const t = document.getElementById('tour').value;
        if(!n) { alert('Name please!'); return; }
        window.open(`https://wa.me/923171588489?text=Hi, I am ${n}. I want to book ${t}.`, '_blank');
    }
</script>

</body>
</html>
