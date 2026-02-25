<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Official Tourist Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --main: #0b3d2e; --gold: #c5a059; --bg: #fdfdfd; }
        
        * { box-sizing: border-box; transition: all 0.3s ease; }
        body { font-family: 'Garamond', serif; margin: 0; background: var(--bg); color: #333; }

        /* Navigation */
        nav { 
            background: white; padding: 20px 8%; display: flex; 
            justify-content: space-between; align-items: center;
            box-shadow: 0 2px 15px rgba(0,0,0,0.05); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-size: 1.8rem; font-weight: bold; color: var(--main); letter-spacing: 2px; }
        nav a { text-decoration: none; color: #555; margin-left: 30px; font-weight: 600; font-size: 15px; }
        nav a:hover { color: var(--gold); }

        /* Hero Section */
        .hero {
            height: 75vh; 
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1500');
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center;
        }
        .hero h1 { font-size: 4rem; margin: 0; letter-spacing: 5px; text-transform: uppercase; }
        .hero p { font-size: 1.2rem; margin-top: 10px; opacity: 0.9; }

        /* Sections */
        .container { max-width: 1200px; margin: auto; padding: 80px 20px; }
        .heading { text-align: center; margin-bottom: 60px; }
        .heading h2 { font-size: 2.5rem; color: var(--main); margin-bottom: 10px; }
        .heading .line { width: 80px; height: 3px; background: var(--gold); margin: auto; }

        /* Professional Destinations Grid */
        .dest-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 40px; }
        .dest-card { background: white; border: 1px solid #eee; border-radius: 0px; overflow: hidden; }
        .dest-card:hover { box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
        .dest-card img { width: 100%; height: 300px; object-fit: cover; filter: grayscale(20%); }
        .dest-card:hover img { filter: grayscale(0%); }
        .dest-info { padding: 30px; }
        .dest-info h3 { margin-top: 0; color: var(--main); font-size: 1.6rem; }

        /* Information & Rates Table */
        .info-section { background: #f9f9f9; padding: 80px 0; }
        .table-container { background: white; padding: 40px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; }
        th, td { padding: 20px; text-align: left; border-bottom: 1px solid #eee; }
        th { color: var(--main); font-size: 1.1rem; }

        /* Contact Section */
        .contact-area { background: var(--main); color: white; padding: 80px 20px; text-align: center; }
        .contact-area h2 { font-size: 2.5rem; margin-bottom: 20px; }
        .btn-gold { 
            background: var(--gold); color: white; padding: 15px 40px; 
            text-decoration: none; display: inline-block; font-weight: bold; margin: 10px; 
            border-radius: 2px; text-transform: uppercase; letter-spacing: 1px;
        }
        
        /* Floating WhatsApp Button (Pure Website Style) */
        .wa-btn {
            position: fixed; bottom: 30px; right: 30px; background: #25d366; 
            color: white; width: 60px; height: 60px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 30px; text-decoration: none; box-shadow: 0 5px 15px rgba(0,0,0,0.2); z-index: 1000;
        }

        footer { padding: 40px; text-align: center; background: white; border-top: 1px solid #eee; color: #777; font-size: 14px; }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            nav { padding: 20px 5%; flex-direction: column; }
            nav .links { margin-top: 15px; }
            nav a { margin: 0 10px; font-size: 13px; }
        }
    </style>
</head>
<body>

<nav>
    <div class="logo">ASTORE HUB</div>
    <div class="links">
        <a href="#destinations">DESTINATIONS</a>
        <a href="#rates">RATES</a>
        <a href="#contact">CONTACT</a>
    </div>
</nav>

<div class="hero">
    <h1>Discover Astore</h1>
    <p>Premium Jeep Services & Guided Tours Across the Valley</p>
</div>

<div class="container" id="destinations">
    <div class="heading">
        <h2>Our Main Attractions</h2>
        <div class="line"></div>
    </div>
    <div class="dest-grid">
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
            <div class="dest-info">
                <h3>Rama Meadows</h3>
                <p>Nanga Parbat ke haseen nazaaron ke saath camping ke liye behtareen jagah.</p>
            </div>
        </div>
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
            <div class="dest-info">
                <h3>Minimarg Valley</h3>
                <p>Rainbow Lake aur sarhad ki khoobsurti ka aik munfarid nazaara.</p>
            </div>
        </div>
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b" alt="Deosai">
            <div class="dest-info">
                <h3>Deosai Plains</h3>
                <p>The Land of Giants. Chillum gate se Deosai ki jannat ka safar shuru karein.</p>
            </div>
        </div>
    </div>
</div>

<div class="info-section" id="rates">
    <div class="container">
        <div class="heading">
            <h2>Service Rates 2026</h2>
            <div class="line"></div>
        </div>
        <div class="table-container">
            <table>
                <tr>
                    <th>Service Description</th>
                    <th>Average Rate</th>
                    <th>Booking Info</th>
                </tr>
                <tr>
                    <td>4x4 Jeep (Minimarg Trip)</td>
                    <td>PKR 12,000 - 15,000</td>
                    <td>Inclusive of Driver</td>
                </tr>
                <tr>
                    <td>Deosai Plains Tour</td>
                    <td>PKR 10,000 - 13,000</td>
                    <td>Full Day Return</td>
                </tr>
                <tr>
                    <td>Standard Guest House Room</td>
                    <td>PKR 5,000 / Night</td>
                    <td>Astore/Gorikot Area</td>
                </tr>
            </table>
        </div>
    </div>
</div>

<div class="contact-area" id="contact">
    <h2>Ready to Plan Your Journey?</h2>
    <p>Contact +92 317 1588489 for customized tour packages and real-time road updates.</p>
    <a href="tel:+923171588489" class="btn-gold">Call Now</a>
    <a href="https://wa.me/923171588489" class="btn-gold" style="background:#25d366;">WhatsApp Booking</a>
</div>

<a href="https://wa.me/923171588489" class="wa-btn" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<footer>
    <p>&copy; 2026 Astore Tourist Information Hub. All Rights Reserved.</p>
    <p>📍 Main Bazaar Astore, Gilgit Baltistan</p>
</footer>

</body>
</html>
