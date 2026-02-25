<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Cinematic Travel</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Montserrat:wght@300;600&display=swap" rel="stylesheet">
    <style>
        * { box-sizing: border-box; }
        body { margin: 0; font-family: 'Montserrat', sans-serif; background: #050a08; color: #fff; overflow-x: hidden; }

        /* Cinematic Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1500');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;
        }

        .hero h1 { 
            font-family: 'Cinzel', serif; font-size: clamp(3rem, 10vw, 7rem); 
            letter-spacing: 15px; margin: 0; color: #d4af37;
            animation: fadeInDown 2s ease;
        }

        .hero p { 
            font-size: 1.2rem; letter-spacing: 5px; text-transform: uppercase; 
            margin-top: 20px; animation: fadeInUp 2s ease;
        }

        /* Glassy Navigation */
        nav {
            position: fixed; top: 0; width: 100%; padding: 25px 5%;
            display: flex; justify-content: space-between; align-items: center;
            background: rgba(0,0,0,0.2); backdrop-filter: blur(10px); z-index: 1000;
        }
        nav .logo { font-family: 'Cinzel'; font-size: 1.8rem; color: #d4af37; text-decoration: none; }

        /* Destinations Sections */
        .section { padding: 100px 10%; position: relative; }
        .parallax-bg {
            height: 400px; background-size: cover; background-position: center; background-attachment: fixed;
            border-radius: 30px; margin: 50px 0; position: relative;
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
        }

        .content-overlay {
            position: absolute; bottom: 30px; left: 30px; right: 30px;
            background: rgba(255, 255, 255, 0.1); backdrop-filter: blur(15px);
            padding: 30px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.2);
        }

        /* Stats & Feeling */
        .experience-bar {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px; text-align: center; background: #0a1410; padding: 60px 0;
        }
        .stat-card h2 { color: #d4af37; font-size: 3rem; margin-bottom: 5px; }

        /* Contact Section with "Feel" */
        .contact-premium {
            background: linear-gradient(45deg, #0b3d2e, #1b1b1b);
            padding: 80px 5%; border-radius: 50px; text-align: center;
            margin: 50px 10%; border: 1px solid #d4af37;
        }

        .btn-luxury {
            padding: 20px 50px; background: #d4af37; color: #000;
            text-decoration: none; font-weight: bold; border-radius: 50px;
            display: inline-block; margin: 20px; font-size: 1.1rem;
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.4);
        }

        /* Animations */
        @keyframes fadeInDown { from { opacity: 0; transform: translateY(-50px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }

        .wa-float {
            position: fixed; bottom: 30px; right: 30px; background: #25d366;
            color: white; width: 65px; height: 65px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 30px; box-shadow: 0 15px 35px rgba(37, 211, 102, 0.4);
            z-index: 9999; text-decoration: none;
        }

        footer { text-align: center; padding: 50px; opacity: 0.6; font-size: 0.8rem; }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <div class="links desktop-only">
        <a href="tel:+923171588489" style="color:#d4af37; text-decoration:none; font-weight:bold;">📞 0317 1588489</a>
    </div>
</nav>

<section class="hero">
    <p>Authentic Northern Experience</p>
    <h1>ASTORE</h1>
    <a href="#explore" class="btn-luxury">EXPLORE THE WILD</a>
</section>

<div class="experience-bar">
    <div class="stat-card"><h2>12+</h2><p>Destinations</p></div>
    <div class="stat-card"><h2>4x4</h2><p>Expert Drivers</p></div>
    <div class="stat-card"><h2>NOC</h2><p>Assistance</p></div>
</div>

<div class="container" id="explore" style="max-width: 1200px; margin: auto;">
    
    <div class="parallax-bg" style="background-image: url('https://images.unsplash.com/photo-1627896157734-4d7d4388f28b');">
        <div class="content-overlay">
            <h2 style="margin:0; font-family:'Cinzel';">Rama Meadows</h2>
            <p>Where the silence of the forest meets the majesty of Nanga Parbat.</p>
        </div>
    </div>

    <div class="parallax-bg" style="background-image: url('https://images.unsplash.com/photo-1533130061792-64b345e4e833');">
        <div class="content-overlay">
            <h2 style="margin:0; font-family:'Cinzel';">Minimarg</h2>
            <p>Access the hidden rainbow of the borderlands with our expert guides.</p>
        </div>
    </div>

    <div class="parallax-bg" style="background-image: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b');">
        <div class="content-overlay">
            <h2 style="margin:0; font-family:'Cinzel';">Deosai Plains</h2>
            <p>Roam the land of giants at 13,000 feet above sea level.</p>
        </div>
    </div>
</div>

<section class="contact-premium">
    <h2 style="font-family: 'Cinzel'; font-size: 2.5rem; color: #d4af37;">Begin Your Odyssey</h2>
    <p>Aapki safety aur sukoon hamari pehli tarjeeh hai. Custom tour plans ke liye rabta karein.</p>
    <a href="tel:+923171588489" class="btn-luxury">Call Now</a>
    <a href="https://wa.me/923171588489" class="btn-luxury" style="background:transparent; border: 2px solid #25d366; color:#25d366;">WhatsApp Booking</a>
</section>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<footer>
    <p>&copy; 2026 ASTORE TOURIST HUB. CRAFTED FOR ADVENTURERS.</p>
</footer>

</body>
</html>
