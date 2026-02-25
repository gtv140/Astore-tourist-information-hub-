<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Valley | Premium Travel Agency</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700;800&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #0a4d3c; --accent: #f59e0b; --text-dark: #1e293b; --light: #f8fafc; }
        * { box-sizing: border-box; transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1); }
        body { font-family: 'Montserrat', sans-serif; margin: 0; background: var(--light); color: var(--text-dark); scroll-behavior: smooth; }

        /* Professional Header */
        nav { 
            background: white; padding: 15px 8%; display: flex; justify-content: space-between; 
            align-items: center; position: sticky; top: 0; z-index: 1000; box-shadow: 0 4px 20px rgba(0,0,0,0.08); 
        }
        .logo { font-size: 1.6rem; font-weight: 800; color: var(--primary); text-decoration: none; display: flex; align-items: center; gap: 10px; }
        .nav-links { display: flex; gap: 30px; }
        .nav-links a { text-decoration: none; color: var(--text-dark); font-weight: 600; font-size: 0.9rem; }
        .nav-links a:hover { color: var(--accent); }
        .btn-nav { background: var(--primary); color: white !important; padding: 10px 25px; border-radius: 50px; }

        /* Modern Hero Section */
        .hero { 
            height: 90vh; background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1500');
            background-size: cover; background-position: center; display: flex; flex-direction: column; 
            justify-content: center; align-items: center; color: white; text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Playfair Display', serif; font-size: clamp(2.5rem, 8vw, 5.5rem); margin: 0; }
        .hero p { font-size: 1.2rem; max-width: 600px; margin: 20px 0; font-weight: 300; }

        /* Feature Cards (Icons) */
        .container { max-width: 1200px; margin: auto; padding: 80px 20px; }
        .section-header { text-align: center; margin-bottom: 60px; }
        .section-header h2 { font-size: 2.5rem; color: var(--primary); margin: 0; }
        
        /* Dynamic Tab Destination Section */
        .dest-tabs { display: flex; justify-content: center; gap: 15px; margin-bottom: 40px; flex-wrap: wrap; }
        .tab-btn { padding: 12px 30px; border: 2px solid var(--primary); border-radius: 50px; cursor: pointer; font-weight: bold; background: transparent; color: var(--primary); }
        .tab-btn.active { background: var(--primary); color: white; }

        .dest-display { display: grid; grid-template-columns: 1fr 1fr; gap: 50px; align-items: center; background: white; padding: 40px; border-radius: 30px; box-shadow: 0 20px 40px rgba(0,0,0,0.05); }
        .dest-image { width: 100%; height: 400px; border-radius: 20px; object-fit: cover; }

        /* Professional Booking Form */
        .booking-engine { background: var(--primary); color: white; border-radius: 40px; padding: 60px; display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: center; }
        .form-card { background: white; padding: 40px; border-radius: 25px; color: var(--text-dark); }
        .input-group { margin-bottom: 20px; }
        .input-group label { display: block; margin-bottom: 8px; font-weight: 700; font-size: 0.9rem; }
        .input-group input, .input-group select { width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 10px; font-size: 1rem; }

        /* Pricing Tool Section */
        .price-calculator { background: #e2e8f0; padding: 40px; border-radius: 20px; margin-top: 30px; text-align: center; }
        .price-value { font-size: 2.5rem; color: var(--primary); font-weight: 800; }

        /* Floating WhatsApp */
        .wa-float { position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white; width: 65px; height: 65px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 10px 30px rgba(37,211,102,0.4); z-index: 1000; text-decoration: none; }

        @media (max-width: 992px) {
            .dest-display, .booking-engine { grid-template-columns: 1fr; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo"><i class="fas fa-mountain"></i> ASTORE TRAVELS</a>
    <div class="nav-links">
        <a href="#destinations">Destinations</a>
        <a href="#services">Services</a>
        <a href="#booking" class="btn-nav">Book Trip</a>
    </div>
</nav>

<section class="hero">
    <h1>Experience Astore Valley</h1>
    <p>Discover the hidden gems of the Himalayas with Astore's most trusted travel partner since 2015.</p>
    <a href="#booking" style="padding: 18px 45px; background: var(--accent); color: white; border-radius: 50px; text-decoration: none; font-weight: 800; font-size: 1.1rem; box-shadow: 0 10px 25px rgba(245, 158, 11, 0.4);">START YOUR ADVENTURE</a>
</section>

<div class="container" id="destinations">
    <div class="section-header">
        <h2>Top Rated Destinations</h2>
        <p>Explore our most popular tour locations</p>
    </div>

    <div class="dest-tabs">
        <button class="tab-btn active" onclick="updateDest('Rama Meadows', 'Rama is known for its lush green meadows and the majestic Rama Lake at the base of Nanga Parbat.', 'https://images.unsplash.com/photo-1627896157734-4d7d4388f28b', this)">Rama Meadows</button>
        <button class="tab-btn" onclick="updateDest('Minimarg', 'A hidden paradise near the border. Famous for its Rainbow Lake and pristine nature.', 'https://images.unsplash.com/photo-1533130061792-64b345e4e833', this)">Minimarg</button>
        <button class="tab-btn" onclick="updateDest('Deosai Plains', 'The land of giants. Explore the second highest plateau in the world via Astore.', 'https://images.unsplash.com/photo-1464822759023-fed622ff2c3b', this)">Deosai Plains</button>
    </div>

    <div class="dest-display" id="destDisplay">
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" class="dest-image" id="destImg">
        <div class="dest-text">
            <h3 id="destTitle" style="font-size: 2.5rem; color: var(--primary); margin: 0;">Rama Meadows</h3>
            <p id="destDesc" style="font-size: 1.1rem; line-height: 1.8; margin: 20px 0;">Rama is known for its lush green meadows and the majestic Rama Lake at the base of Nanga Parbat. Perfect for camping and nature lovers.</p>
            <div style="display: flex; gap: 20px; font-weight: 700; color: var(--accent);">
                <span><i class="fas fa-clock"></i> Full Day</span>
                <span><i class="fas fa-jeep"></i> 4x4 Required</span>
            </div>
        </div>
    </div>
</div>

<div class="container" id="booking">
    <div class="booking-engine">
        <div>
            <h2 style="font-size: 3rem; font-family: 'Playfair Display';">Ready to Plan <br>Your Escape?</h2>
            <p style="font-size: 1.1rem; opacity: 0.9; margin: 30px 0;">Hamein apni details batayein aur hamara expert team foran aapse rabta karegi pricing aur itinerary ke liye.</p>
            <ul style="list-style: none; padding: 0; font-weight: 600;">
                <li><i class="fas fa-check-circle" style="color: var(--accent);"></i> Authorized Local Drivers</li>
                <li><i class="fas fa-check-circle" style="color: var(--accent);"></i> NOC Assistance for Border Areas</li>
                <li><i class="fas fa-check-circle" style="color: var(--accent);"></i> 24/7 Emergency Support</li>
            </ul>
        </div>
        <div class="form-card">
            <div class="input-group">
                <label>Your Name</label>
                <input type="text" id="name" placeholder="Enter Full Name">
            </div>
            <div class="input-group">
                <label>Select Destination</label>
                <select id="location" onchange="calculatePrice()">
                    <option value="12000">Minimarg & Rainbow Lake (Rs. 12,000)</option>
                    <option value="8000">Rama Meadows (Rs. 8,000)</option>
                    <option value="15000">Deosai Plains (Rs. 15,000)</option>
                </select>
            </div>
            <div class="price-calculator">
                <span style="display: block; font-size: 0.9rem; font-weight: 700;">ESTIMATED JEEP RATE</span>
                <span class="price-value" id="totalPrice">Rs. 12,000</span>
            </div>
            <button onclick="sendBooking()" style="width:100%; padding:15px; background: #25d366; color:white; border:none; border-radius:12px; font-weight:800; margin-top:20px; cursor:pointer;">BOOK VIA WHATSAPP</button>
        </div>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer style="background: #1e293b; color: white; padding: 60px 20px; text-align: center;">
    <h2 style="font-family: 'Playfair Display'; font-size: 2rem;">ASTORE TRAVELS</h2>
    <p>Main Market Astore, Gilgit-Baltistan | +92 317 1588489</p>
    <div style="margin-top: 30px; opacity: 0.5; font-size: 0.8rem;">&copy; 2026 Astore Tourist Information Hub. All Rights Reserved.</div>
</footer>

<script>
    function updateDest(title, desc, img, btn) {
        document.getElementById('destTitle').innerText = title;
        document.getElementById('destDesc').innerText = desc;
        document.getElementById('destImg').src = img;
        
        // Update button styles
        let btns = document.querySelectorAll('.tab-btn');
        btns.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
    }

    function calculatePrice() {
        let price = document.getElementById('location').value;
        document.getElementById('totalPrice').innerText = 'Rs. ' + parseInt(price).toLocaleString();
    }

    function sendBooking() {
        let name = document.getElementById('name').value;
        let loc = document.getElementById('location').options[document.getElementById('location').selectedIndex].text;
        let msg = `Hi! I'm ${name}. I'm interested in booking a trip for ${loc}. Please confirm availability.`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, '_blank');
    }
</script>

</body>
</html>
