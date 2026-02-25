<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Valley | Tourist Information Hub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #004d40; --secondary: #c5e1a5; --dark: #1b1b1b; --text: #ffffff; }
        body { font-family: 'Poppins', sans-serif; margin: 0; background-color: #f4f7f6; color: #333; scroll-behavior: smooth; }
        
        /* Navigation */
        nav { background: rgba(0, 77, 64, 0.95); padding: 15px 5%; position: fixed; width: 90%; top: 0; z-index: 1000; display: flex; justify-content: space-between; align-items: center; backdrop-filter: blur(5px); }
        nav a { color: white; text-decoration: none; margin-left: 20px; font-weight: 500; font-size: 14px; text-transform: uppercase; }

        /* Hero Section */
        .hero { height: 100vh; background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&q=80&w=1500'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; }
        .hero h1 { font-size: 4rem; margin-bottom: 10px; text-shadow: 2px 2px 10px rgba(0,0,0,0.5); }
        .hero p { font-size: 1.2rem; margin-bottom: 30px; max-width: 600px; }

        /* Section Styling */
        .section { padding: 80px 10% 40px; }
        .section-title { text-align: center; margin-bottom: 50px; font-size: 2.5rem; color: var(--primary); position: relative; }
        .section-title::after { content: ''; width: 80px; height: 4px; background: var(--secondary); position: absolute; bottom: -10px; left: 50%; transform: translateX(-50%); }

        /* Destinations Grid */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .card { background: white; border-radius: 15px; overflow: hidden; box-shadow: 0 10px 20px rgba(0,0,0,0.05); transition: 0.4s; position: relative; }
        .card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); }
        .card img { width: 100%; height: 200px; object-fit: cover; }
        .card-body { padding: 20px; }
        .card-body h3 { margin: 0 0 10px; color: var(--primary); }

        /* Pricing Table */
        .table-box { background: white; border-radius: 15px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.05); margin-top: 30px; }
        table { width: 100%; border-collapse: collapse; }
        th { background: var(--primary); color: white; padding: 15px; text-align: left; }
        td { padding: 15px; border-bottom: 1px solid #eee; }

        /* Contact Section */
        .contact-card { background: var(--primary); color: white; padding: 60px; border-radius: 20px; text-align: center; }
        .btn { display: inline-block; padding: 15px 35px; border-radius: 50px; font-weight: bold; text-decoration: none; transition: 0.3s; margin: 10px; }
        .btn-call { background: white; color: var(--primary); }
        .btn-whatsapp { background: #25d366; color: white; }

        /* Floating Buttons */
        .floating-wa { position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 5px 15px rgba(0,0,0,0.3); z-index: 1000; }

        footer { text-align: center; padding: 40px; color: #888; border-top: 1px solid #ddd; }
        
        @media (max-width: 768px) { .hero h1 { font-size: 2.5rem; } nav { flex-direction: column; } }
    </style>
</head>
<body>

<nav>
    <div style="font-size: 20px; font-weight: 800; color: #c5e1a5;">ASTORE HUB</div>
    <div class="links">
        <a href="#destinations">Destinations</a>
        <a href="#prices">Services</a>
        <a href="#contact">Contact</a>
    </div>
</nav>

<section class="hero" id="home">
    <h1>Explore Astore Valley</h1>
    <p>Discover Rama Lake, Minimarg, and the mighty Deosai Plains with your local travel partner.</p>
    <a href="tel:+923171588489" class="btn btn-call"><i class="fas fa-phone"></i> Call +92 317 1588489</a>
</section>

<section class="section" id="destinations">
    <h2 class="section-title">Places You Must Visit</h2>
    <div class="grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b?q=80&w=1000" alt="Rama Lake">
            <div class="card-body"><h3>Rama Meadows & Lake</h3><p>Pine trees aur barfani paharon ke darmiyan aik khoobsurat muqam.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833?q=80&w=1000" alt="Deosai">
            <div class="card-body"><h3>Deosai Plains</h3><p>Dunya ka 2nd highest plateau. Chillum gate se rasta jata hai.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?q=80&w=1000" alt="Rainbow Lake">
            <div class="card-body"><h3>Minimarg & Rainbow Lake</h3><p>Pakistan ki sab se mehfooz aur khoobsurat sarhadi wadi.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1000" alt="Rupal">
            <div class="card-body"><h3>Rupal Face (Nanga Parbat)</h3><p>Adventurers ke liye Nanga Parbat ka sab se kareebi view point.</p></div>
        </div>
    </div>
</section>

<section class="section" id="prices">
    <h2 class="section-title">Estimated Trip Costs</h2>
    <div class="table-box">
        <table>
            <tr><th>Service</th><th>Rate (PKR)</th><th>Details</th></tr>
            <tr><td>4x4 Jeep (Full Day)</td><td>12,000 - 15,000</td><td>Deosai / Minimarg Trip</td></tr>
            <tr><td>Local Tour Guide</td><td>2,500 / Day</td><td>For trekking & history</td></tr>
            <tr><td>Standard Room</td><td>5,000 / Night</td><td>Astore City / Gorikot</td></tr>
            <tr><td>Camping Kit</td><td>2,000 / Person</td><td>Includes Tent & Mat</td></tr>
        </table>
    </div>
</section>

<section class="section" id="contact">
    <div class="contact-card">
        <h2>Plan Your Adventure Today</h2>
        <p>Aapko Jeep chahiye, Hotel ya NOC ke bare mein maloomat? Hum 24 ghante hazir hain.</p>
        <a href="tel:+923171588489" class="btn btn-call"><i class="fas fa-phone"></i> Call Now</a>
        <a href="https://wa.me/923171588489" class="btn btn-whatsapp"><i class="fab fa-whatsapp"></i> WhatsApp Us</a>
        <p style="margin-top: 20px; opacity: 0.8;">📍 Main Bazar, Astore, Gilgit-Baltistan</p>
    </div>
</section>

<a href="https://wa.me/923171588489" class="floating-wa" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<footer>
    <p>&copy; 2026 Astore Tourist Hub | Design by Gemini AI</p>
</footer>

</body>
</html>
