<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | The Ultimate North Experience</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --bg: #020617;
            --card-bg: rgba(255, 255, 255, 0.04);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; line-height: 1.6; overflow-x: hidden; scroll-behavior: smooth; }

        /* Navigation */
        nav.navbar {
            position: fixed; top: 0; width: 100%; padding: 15px 5%;
            background: rgba(2, 6, 23, 0.9); backdrop-filter: blur(15px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 22px; font-weight: 800; }
        .logo span { color: var(--primary); }

        /* Hero Section */
        .hero {
            height: 80vh; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1600&auto=format') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(40px, 12vw, 90px); line-height: 0.9; margin-bottom: 15px; }
        .hero p { font-size: 11px; letter-spacing: 5px; text-transform: uppercase; color: var(--primary); font-weight: 700; }

        .container { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }
        .section-header { margin-bottom: 40px; }
        .section-header h2 { font-family: 'Syne'; font-size: 32px; border-left: 5px solid var(--primary); padding-left: 15px; }

        /* Destinations Grid */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; }
        .tour-card {
            background: var(--card-bg); border-radius: 24px; overflow: hidden;
            border: 1px solid var(--border); transition: 0.4s;
        }
        .tour-card:hover { border-color: var(--primary); transform: translateY(-5px); }
        .img-container { height: 250px; overflow: hidden; }
        .img-container img { width: 100%; height: 100%; object-fit: cover; }
        .card-content { padding: 25px; }
        .card-content h3 { font-family: 'Syne'; color: var(--primary); margin-bottom: 10px; }

        /* About & Trust Section */
        .about-section { background: rgba(255,255,255,0.02); border-radius: 30px; padding: 35px; border: 1px solid var(--border); margin: 50px 0; }
        .features-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 20px; margin-top: 30px; }
        .feature { text-align: center; }
        .feature i { font-size: 30px; color: var(--primary); margin-bottom: 10px; }
        .feature p { font-size: 13px; font-weight: 600; }

        /* Reviews Section */
        .review-card { background: var(--card-bg); padding: 25px; border-radius: 20px; border-top: 3px solid var(--primary); font-style: italic; }
        .reviewer { margin-top: 15px; font-weight: 800; font-style: normal; font-size: 14px; color: var(--primary); }

        /* Booking Form */
        .booking-form { background: var(--card-bg); padding: 35px; border-radius: 30px; border: 1px solid var(--primary); }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 20px; border-radius: 12px;
            border: 1px solid var(--border); background: #000; color: #fff; outline: none; font-size: 16px;
        }
        .btn-pro {
            width: 100%; padding: 20px; background: var(--primary); color: #000;
            border: none; border-radius: 12px; font-weight: 800; cursor: pointer; text-transform: uppercase;
        }

        /* Bottom Nav */
        .bottom-nav {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 15px 0 30px;
            border-top: 1px solid var(--border); z-index: 1000;
        }
        .bottom-nav a { color: #fff; opacity: 0.5; font-size: 22px; transition: 0.3s; }
        .bottom-nav a.active { color: var(--primary); opacity: 1; }

        @media (max-width: 768px) {
            .hero h1 { font-size: 50px; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">ASTORE<span>HUB</span></div>
        <a href="tel:+923171588489" style="color:var(--primary); font-size:22px;"><i class="fa-solid fa-phone-volume"></i></a>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Official Digital Guide</p>
            <h1>ASTORE<br><span>VALLEY</span></h1>
            <div style="margin-top:20px;">
                <span style="font-size:12px; border:1px solid var(--primary); padding:5px 15px; border-radius:50px; color:var(--primary);">Season Open: May - Oct</span>
            </div>
        </div>
    </section>

    <div class="container">
        
        <div class="about-section">
            <h2 style="font-family:'Syne'; margin-bottom:15px;">Experience the North</h2>
            <p style="opacity:0.7; font-size:14px;">Astore Hub is Gilgit-Baltistan's leading travel information portal. We connect explorers to the untouched beauty of the mountains with local expertise and secure services.</p>
            <div class="features-row">
                <div class="feature"><i class="fa-solid fa-jeep"></i><p>4x4 Jeeps</p></div>
                <div class="feature"><i class="fa-solid fa-map-location-dot"></i><p>Local Experts</p></div>
                <div class="feature"><i class="fa-solid fa-hotel"></i><p>Hotel Deals</p></div>
            </div>
        </div>

        <div class="section-header"><h2>Top Destinations</h2></div>
        <div class="grid">
            <div class="tour-card">
                <div class="img-container"><img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800"></div>
                <div class="card-content"><h3>Rama Meadows</h3><p>A lush green oasis surrounded by snow-capped peaks. The heart of Astore.</p></div>
            </div>
            <div class="tour-card">
                <div class="img-container"><img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800"></div>
                <div class="card-content"><h3>Deosai Plains</h3><p>The "Land of Giants" - a high altitude plateau with breathtaking views of Sheosar Lake.</p></div>
            </div>
        </div>

        

        <div class="section-header" style="margin-top:60px;"><h2>Traveler Reviews</h2></div>
        <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));">
            <div class="review-card">"The best tour guide for Astore. Everything was managed perfectly!"<div class="reviewer">- Ahmed Raza, Lahore</div></div>
            <div class="review-card">"Truly professional hub. They know every hidden spot in GB."<div class="reviewer">- Sara Khan, Islamabad</div></div>
        </div>

        <div class="section-header" id="book" style="margin-top:60px;"><h2>Plan Your Tour</h2></div>
        <div class="booking-form">
            <form id="finalForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Expedition</option>
                    <option>Grand Hunza Valley Tour</option>
                    <option>Skardu Adventure Trip</option>
                </select>
                <textarea id="notes" rows="4" placeholder="Mention group size and travel dates..."></textarea>
                <button type="submit" class="btn-pro">Send Booking Inquiry</button>
            </form>
        </div>

        

        <div style="height: 350px; border-radius: 30px; overflow: hidden; margin-top: 40px; border: 1px solid var(--border);">
            <iframe src="http://googleusercontent.com/maps.google.com/7" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg) brightness(0.8);"></iframe>
        </div>

    </div>

    <footer style="text-align:center; padding: 100px 20px 150px; opacity:0.3; font-size:10px; letter-spacing:3px;">
        © 2026 ASTORE TOURIST HUB | EXPERIENCING THE NORTH
    </footer>

    <div class="bottom-nav">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-mountain"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <script>
        document.getElementById('finalForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('notes').value;
            const text = `*HUB BOOKING INQUIRY*\n---\n*Explorer:* ${n}\n*WhatsApp:* ${p}\n*Trip:* ${t}\n*Details:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
