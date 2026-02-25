<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Valley | Premium Tours</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f4f7f6; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: var(--bg); color: #333; line-height: 1.6; }

        /* Navigation - Proper Spacing */
        nav { 
            background: white; padding: 15px 5%; display: flex; 
            justify-content: space-between; align-items: center;
            position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .logo { font-weight: 800; color: var(--primary); text-decoration: none; font-size: 1.3rem; }

        /* Full-Width Mobile Hero */
        .hero { 
            height: 50vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800');
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; 
            text-align: center; color: white; padding: 20px;
        }
        .hero h1 { font-size: 2.2rem; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        .hero p { font-size: 1rem; opacity: 0.9; }

        /* Main Container - Fixed Width for Mobile */
        .container { width: 100%; max-width: 500px; margin: 0 auto; padding: 30px 15px; }
        
        .section-title { font-size: 1.8rem; color: var(--primary); text-align: center; margin-bottom: 30px; font-weight: 700; }

        /* Responsive Cards */
        .card { 
            background: white; border-radius: 20px; overflow: hidden; 
            margin-bottom: 25px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border: 1px solid #eee; display: flex; flex-direction: column;
        }
        .card img { width: 100%; height: 220px; object-fit: cover; display: block; background: #ddd; }
        .card-content { padding: 20px; }
        .card-content h3 { font-size: 1.4rem; color: var(--primary); margin-bottom: 10px; }
        .card-content p { font-size: 0.95rem; color: #666; margin-bottom: 15px; }
        .card-footer { display: flex; justify-content: space-between; align-items: center; border-top: 1px solid #f0f0f0; padding-top: 15px; }
        .price { font-weight: 800; color: var(--accent); font-size: 1.1rem; }

        /* Professional Form */
        .booking-box { 
            background: var(--primary); color: white; border-radius: 25px; 
            padding: 30px 20px; text-align: center; margin-top: 20px;
        }
        .booking-box h2 { font-size: 1.6rem; margin-bottom: 20px; }
        .input-field { 
            width: 100%; padding: 15px; border-radius: 12px; border: none; 
            margin-bottom: 15px; font-size: 1rem; outline: none;
        }
        .btn-submit { 
            width: 100%; padding: 18px; background: #25d366; color: white; 
            border: none; border-radius: 12px; font-weight: bold; font-size: 1.1rem;
            cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px;
        }

        /* Floating WhatsApp Button */
        .wa-float { 
            position: fixed; bottom: 25px; right: 25px; background: #25d366; 
            color: white; width: 60px; height: 60px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 30px; box-shadow: 0 5px 20px rgba(0,0,0,0.2); z-index: 2000; text-decoration: none;
        }

        footer { text-align: center; padding: 40px 20px; font-size: 0.85rem; color: #888; background: white; border-top: 1px solid #eee; }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo"><i class="fas fa-mountain"></i> ASTORE HUB</a>
    <a href="tel:+923171588489" style="color: var(--primary);"><i class="fas fa-phone-alt"></i></a>
</nav>

<div class="hero">
    <h1>Astore Valley</h1>
    <p>Premium 4x4 Jeep & Tour Services</p>
</div>

<div class="container">
    <h2 class="section-title">Explore Paradise</h2>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama Meadows">
        <div class="card-content">
            <h3>Rama Meadows</h3>
            <p>Experience the absolute peace under the shadows of Nanga Parbat.</p>
            <div class="card-footer">
                <span style="font-size: 0.8rem;"><i class="fas fa-clock"></i> Full Day Trip</span>
                <span class="price">Rs. 8,500</span>
            </div>
        </div>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
        <div class="card-content">
            <h3>Minimarg Valley</h3>
            <p>A hidden jewel featuring the famous Rainbow Lake near the border.</p>
            <div class="card-footer">
                <span style="font-size: 0.8rem;"><i class="fas fa-clock"></i> Full Day Trip</span>
                <span class="price">Rs. 14,000</span>
            </div>
        </div>
    </div>

    <div class="booking-box" id="book">
        <h2>Quick Reservation</h2>
        <input type="text" id="custName" class="input-field" placeholder="Full Name">
        <select id="custLoc" class="input-field">
            <option>Rama Meadows</option>
            <option>Minimarg & Rainbow Lake</option>
            <option>Deosai Plains</option>
        </select>
        <button class="btn-submit" onclick="sendWA()">
            <i class="fab fa-whatsapp"></i> Book via WhatsApp
        </button>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <p>Main Bazar Astore, Gilgit-Baltistan</p>
    <p>+92 317 1588489</p>
    <p style="margin-top: 10px; opacity: 0.6;">© 2026 Astore Tourist Hub</p>
</footer>

<script>
    function sendWA() {
        const name = document.getElementById('custName').value;
        const loc = document.getElementById('custLoc').value;
        if(!name) { alert('Please enter your name'); return; }
        const msg = `Hi! I am ${name}. I want to book a trip to ${loc}. Please share details.`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, '_blank');
    }
</script>

</body>
</html>
