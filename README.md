<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Complete Tourist Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f39c12; --light: #f8f9fa; --dark: #1a1a1a; }
        * { box-sizing: border-box; transition: 0.3s; }
        body { font-family: 'Segoe UI', Tahoma, sans-serif; margin: 0; background: var(--light); color: var(--dark); line-height: 1.6; }

        /* Announcement */
        .alert { background: #d32f2f; color: white; padding: 10px; text-align: center; font-size: 14px; position: sticky; top: 0; z-index: 2000; }

        /* Hero Section */
        header { 
            height: 80vh; 
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&q=80&w=1500'); 
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; padding: 20px;
        }
        header h1 { font-size: clamp(2.5rem, 8vw, 4.5rem); margin: 0; text-transform: uppercase; letter-spacing: 2px; }

        /* Main Container */
        .container { max-width: 1100px; margin: auto; padding: 40px 20px; }
        .section-title { text-align: center; font-size: 2.2rem; color: var(--primary); margin-bottom: 40px; position: relative; }
        .section-title::after { content: ''; width: 60px; height: 4px; background: var(--accent); position: absolute; bottom: -10px; left: 50%; transform: translateX(-50%); }

        /* Destinations Grid */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        .card { background: white; border-radius: 20px; overflow: hidden; box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
        .card:hover { transform: translateY(-10px); }
        .card img { width: 100%; height: 230px; object-fit: cover; }
        .card-content { padding: 20px; }

        /* Booking Form */
        .booking-section { background: var(--primary); color: white; padding: 60px 20px; border-radius: 30px; margin: 40px 0; }
        .booking-form { max-width: 500px; margin: auto; background: white; padding: 30px; border-radius: 20px; color: var(--dark); }
        .form-group { margin-bottom: 15px; }
        .form-group label { display: block; font-weight: bold; margin-bottom: 5px; }
        .form-group input, .form-group select { width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 8px; }
        
        .btn-submit { background: #25d366; color: white; width: 100%; padding: 15px; border: none; border-radius: 8px; font-size: 1.1rem; font-weight: bold; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; }

        /* Table Style */
        .price-table { width: 100%; border-collapse: collapse; background: white; border-radius: 15px; overflow: hidden; margin: 20px 0; box-shadow: 0 5px 15px rgba(0,0,0,0.05); }
        .price-table th, .price-table td { padding: 15px; text-align: left; border-bottom: 1px solid #eee; }
        .price-table th { background: var(--primary); color: white; }

        /* Floating WhatsApp */
        .wa-float { position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white; width: 65px; height: 65px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 35px; box-shadow: 0 10px 20px rgba(0,0,0,0.3); z-index: 3000; animation: pulse 2s infinite; text-decoration: none; }
        @keyframes pulse { 0% { box-shadow: 0 0 0 0px rgba(37,211,102,0.7); } 100% { box-shadow: 0 0 0 20px rgba(37,211,102,0); } }

        footer { text-align: center; padding: 40px; color: #777; font-size: 14px; background: #eee; }
    </style>
</head>
<body>

<div class="alert">
    <marquee>⚠️ <strong>Tourist Update:</strong> Roads to Minimarg & Deosai are now open. 4x4 Jeeps and CNIC mandatory.</marquee>
</div>

<header>
    <h1>Astore Hub</h1>
    <p>Your Local Partner for Gilgit-Baltistan Adventures</p>
    <a href="tel:+923171588489" style="background:var(--accent); color:white; padding:15px 30px; border-radius:50px; text-decoration:none; font-weight:bold; margin-top:20px;">📞 Call 0317 1588489</a>
</header>

<div class="container">
    <h2 class="section-title">Major Attractions</h2>
    <div class="grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
            <div class="card-content"><h3>Rama Meadows</h3><p>The greenest part of Astore. Perfect for family camping and relaxation.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Rainbow">
            <div class="card-content"><h3>Rainbow Lake</h3><p>A hidden gem in Minimarg valley. Crystal clear water with changing colors.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b" alt="Deosai">
            <div class="card-content"><h3>Deosai Plains</h3><p>The Roof of the World. Accessible via Chillum, Astore.</p></div>
        </div>
    </div>

    <h2 class="section-title">Service Rates</h2>
    <table class="price-table">
        <tr><th>Service</th><th>Estimated Rate</th><th>Note</th></tr>
        <tr><td>4x4 Jeep (Minimarg/Deosai)</td><td>Rs. 12,000 - 15,000</td><td>Full day trip</td></tr>
        <tr><td>Standard Hotel Room</td><td>Rs. 4,000 - 6,000</td><td>Rama/Astore City</td></tr>
        <tr><td>Tourist Guide</td><td>Rs. 2,500</td><td>Daily rate</td></tr>
    </table>
</div>

<div class="container" id="booking">
    <div class="booking-section">
        <h2 style="text-align: center; color: white;">Plan Your Trip</h2>
        <p style="text-align: center;">Fill this form to get an instant quote on WhatsApp.</p>
        <div class="booking-form">
            <div class="form-group"><label>Name</label><input type="text" id="name" placeholder="Your Name"></div>
            <div class="form-group"><label>Destination</label>
                <select id="dest">
                    <option>Minimarg & Rainbow Lake</option>
                    <option>Rama Meadows</option>
                    <option>Deosai Plains</option>
                    <option>Rupal Face</option>
                </select>
            </div>
            <div class="form-group"><label>Travel Date</label><input type="date" id="date"></div>
            <button onclick="sendWA()" class="btn-submit"><i class="fab fa-whatsapp"></i> Get Quote via WhatsApp</button>
        </div>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <p>📍 Main Bazar Astore, Gilgit-Baltistan</p>
    <p>&copy; 2026 Astore Tourist Hub | All Rights Reserved</p>
</footer>

<script>
    function sendWA() {
        const name = document.getElementById('name').value;
        const dest = document.getElementById('dest').value;
        const date = document.getElementById('date').value;
        const phone = "923171588489";
        const text = `Hi, I am ${name}. I want to visit ${dest} on ${date}. Please provide trip details and rates.`;
        window.open(`https://wa.me/${phone}?text=${encodeURIComponent(text)}`, '_blank');
    }
</script>

</body>
</html>
