<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Premium Travels</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --gold: #f59e0b; --bg: #fdfdfd; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', Roboto, sans-serif; background: var(--bg); color: #333; overflow-x: hidden; }

        /* Modern Full-Width Header */
        nav { 
            background: white; padding: 15px 5%; display: flex; justify-content: space-between; 
            align-items: center; position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 15px rgba(0,0,0,0.1);
        }
        .logo { font-weight: 800; color: var(--primary); text-decoration: none; font-size: 1.2rem; }

        /* Cinematic Mobile Hero */
        .hero { 
            height: 70vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1000');
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px;
        }
        .hero h1 { font-size: 2.5rem; margin-bottom: 10px; text-transform: uppercase; letter-spacing: 2px; }
        .hero-btn { background: var(--gold); color: white; padding: 15px 35px; border-radius: 50px; text-decoration: none; font-weight: bold; margin-top: 20px; box-shadow: 0 5px 15px rgba(245, 158, 11, 0.4); }

        /* Services Quick Look */
        .services-bar { display: flex; overflow-x: auto; gap: 20px; padding: 25px; background: white; white-space: nowrap; -webkit-overflow-scrolling: touch; }
        .service-item { display: inline-block; text-align: center; min-width: 100px; }
        .service-item i { font-size: 1.5rem; color: var(--primary); background: #f0fdf4; padding: 15px; border-radius: 50%; margin-bottom: 8px; }
        .service-item p { font-size: 0.8rem; font-weight: bold; }

        /* Premium Card Layout */
        .container { padding: 30px 20px; }
        .section-title { font-size: 1.8rem; color: var(--primary); text-align: center; margin-bottom: 30px; position: relative; }
        
        .dest-card { 
            background: white; border-radius: 25px; overflow: hidden; margin-bottom: 30px; 
            box-shadow: 0 10px 30px rgba(0,0,0,0.08); border: 1px solid #f0f0f0;
        }
        .dest-card img { width: 100%; height: 250px; object-fit: cover; }
        .dest-info { padding: 25px; }
        .dest-info h3 { font-size: 1.5rem; margin-bottom: 10px; color: var(--primary); }
        .dest-meta { display: flex; gap: 15px; margin-top: 15px; font-size: 0.8rem; color: #666; font-weight: bold; }

        /* Luxury Booking Section */
        .booking-box { background: var(--primary); border-radius: 30px; padding: 40px 25px; color: white; text-align: center; }
        .booking-box h2 { font-size: 1.8rem; margin-bottom: 15px; }
        .input-style { width: 100%; padding: 15px; border-radius: 12px; border: none; margin-bottom: 15px; font-size: 1rem; }
        .book-btn { width: 100%; padding: 18px; background: #25d366; color: white; border: none; border-radius: 12px; font-weight: bold; font-size: 1.1rem; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; }

        /* Floating WhatsApp Icon */
        .wa-float { position: fixed; bottom: 25px; right: 25px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 5px 20px rgba(0,0,0,0.3); z-index: 2000; text-decoration: none; }

        footer { text-align: center; padding: 40px 20px; background: #f1f5f9; color: #64748b; font-size: 0.9rem; margin-top: 40px; }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo"><i class="fas fa-compass"></i> ASTORE HUB</a>
    <a href="tel:+923171588489" style="color:var(--primary); text-decoration:none;"><i class="fas fa-phone-alt"></i></a>
</nav>

<section class="hero">
    <h1>Experience Astore</h1>
    <p>Premium 4x4 Jeep & Tour Services</p>
    <a href="#book" class="hero-btn">PLAN YOUR TRIP</a>
</section>

<div class="services-bar">
    <div class="service-item"><i class="fas fa-car-side"></i><p>Jeep Rental</p></div>
    <div class="service-item"><i class="fas fa-hotel"></i><p>Hotels</p></div>
    <div class="service-item"><i class="fas fa-hiking"></i><p>Local Guides</p></div>
    <div class="service-item"><i class="fas fa-shield-alt"></i><p>NOC Assist</p></div>
</div>

<div class="container">
    <h2 class="section-title">Major Attractions</h2>
    
    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
        <div class="dest-info">
            <h3>Rama Meadows</h3>
            <p>Explore the lush green valley and the crystal clear Rama Lake.</p>
            <div class="dest-meta">
                <span><i class="fas fa-clock"></i> Full Day</span>
                <span><i class="fas fa-tag" style="color:var(--gold)"></i> Rs. 8,000</span>
            </div>
        </div>
    </div>

    <div class="dest-card">
        <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
        <div class="dest-info">
            <h3>Minimarg Valley</h3>
            <p>Visit the iconic Rainbow Lake near the border mountains.</p>
            <div class="dest-meta">
                <span><i class="fas fa-clock"></i> Full Day</span>
                <span><i class="fas fa-tag" style="color:var(--gold)"></i> Rs. 14,000</span>
            </div>
        </div>
    </div>

    <div class="booking-box" id="book">
        <h2>Quick Booking</h2>
        <p style="margin-bottom: 25px; opacity: 0.8;">Enter details for instant quote</p>
        <input type="text" id="custName" class="input-style" placeholder="Your Full Name">
        <select id="custLoc" class="input-style">
            <option>Minimarg & Rainbow Lake</option>
            <option>Rama Meadows</option>
            <option>Deosai Plains</option>
        </select>
        <button class="book-btn" onclick="sendToWA()"><i class="fab fa-whatsapp"></i> Book on WhatsApp</button>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <p>📍 Main Bazar Astore, Gilgit-Baltistan</p>
    <p>Contact: +92 317 1588489</p>
    <p style="margin-top:15px; opacity:0.5;">© 2026 Astore Tourist Information Hub</p>
</footer>

<script>
    function sendToWA() {
        const name = document.getElementById('custName').value;
        const loc = document.getElementById('custLoc').value;
        const text = `Hi, I am ${name}. I want to book a trip to ${loc}. Please share details.`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
    }
</script>

</body>
</html>
