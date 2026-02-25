<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | The Ultimate North Portal</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #ff007a;
            --bg: #02040a;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- Animated Background --- */
        .bg-glow {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #111827 0%, #02040a 100%);
            z-index: -1;
        }

        /* --- Navbar --- */
        nav {
            position: fixed; top: 0; width: 100%; padding: 15px 6%;
            background: rgba(2, 4, 10, 0.8); backdrop-filter: blur(20px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 20px; font-weight: 800; color: var(--primary); text-transform: uppercase; }
        .logo span { color: #fff; }

        /* --- Hero --- */
        .hero {
            height: 80vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            text-align: center; padding: 20px;
            background: linear-gradient(rgba(2,4,10,0.7), var(--bg)), url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1200&auto=format');
            background-size: cover; background-position: center;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(45px, 15vw, 90px); line-height: 0.85; margin-bottom: 20px; }
        .hero span { color: var(--primary); }

        /* --- Live Weather --- */
        .weather-card {
            background: var(--glass); border: 1px solid var(--primary);
            padding: 10px 20px; border-radius: 100px; display: flex; align-items: center; gap: 10px;
            font-size: 13px; font-weight: 800; box-shadow: 0 0 20px rgba(0,242,255,0.2);
        }

        .container { max-width: 1100px; margin: 0 auto; padding: 60px 20px; }
        .section-title { font-family: 'Syne'; font-size: 32px; margin-bottom: 40px; }
        .section-title span { color: var(--secondary); }

        /* --- Modern Grid --- */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .card {
            background: var(--glass); border-radius: 35px; overflow: hidden; border: 1px solid var(--border);
            transition: 0.5s cubic-bezier(0.2, 0.8, 0.2, 1);
        }
        .card:hover { transform: translateY(-10px); border-color: var(--primary); }
        .card img { width: 100%; height: 260px; object-fit: cover; }
        .card-body { padding: 30px; }
        .card-body h3 { font-family: 'Syne'; color: var(--primary); margin-bottom: 10px; }
        .card-body p { font-size: 14px; opacity: 0.7; line-height: 1.6; }

        /* --- Social Links --- */
        .social-strip { display: flex; justify-content: center; gap: 20px; margin-top: 20px; }
        .social-icon { 
            width: 50px; height: 50px; border-radius: 50%; background: var(--glass);
            display: flex; align-items: center; justify-content: center; color: #fff;
            text-decoration: none; border: 1px solid var(--border); font-size: 20px; transition: 0.3s;
        }
        .social-icon:hover { border-color: var(--secondary); color: var(--secondary); transform: scale(1.1); }

        /* --- Booking UI --- */
        .booking-ui {
            background: linear-gradient(145deg, #0a0f1d, #02040a);
            padding: 40px; border-radius: 40px; border: 1px solid var(--primary);
            box-shadow: 0 20px 50px rgba(0, 242, 255, 0.1);
        }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 20px; border-radius: 18px;
            border: 1px solid var(--border); background: #000; color: #fff; font-size: 16px; outline: none;
        }
        .btn-premium {
            width: 100%; padding: 22px; background: var(--primary); color: #000;
            border: none; border-radius: 18px; font-weight: 800; font-size: 16px;
            text-transform: uppercase; cursor: pointer; transition: 0.4s;
        }
        .btn-premium:hover { letter-spacing: 2px; box-shadow: 0 0 30px var(--primary); }

        /* --- App Dock --- */
        .dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 420px; background: rgba(0,0,0,0.85);
            backdrop-filter: blur(25px); border-radius: 100px; padding: 15px 30px;
            display: flex; justify-content: space-between; align-items: center;
            border: 1px solid var(--border); z-index: 2000;
        }
        .dock a { color: #fff; opacity: 0.4; font-size: 24px; transition: 0.3s; text-decoration: none; }
        .dock a.active { color: var(--primary); opacity: 1; transform: scale(1.2); }

        @media (max-width: 600px) {
            .hero h1 { font-size: 55px; }
            .booking-ui { padding: 25px; }
        }
    </style>
</head>
<body>

    <div class="bg-glow"></div>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <a href="tel:+923171588489" style="color:var(--primary); font-size: 20px;"><i class="fa-solid fa-phone-volume"></i></a>
    </nav>

    <section class="hero">
        <p style="letter-spacing: 6px; font-size: 10px; font-weight: 800; margin-bottom: 10px;">PREMIUM TRAVEL PORTAL</p>
        <h1>EXPLORE THE<br><span>MOUNTAINS</span></h1>
        
        <div class="weather-card">
            <i class="fa-solid fa-cloud-sun"></i>
            <span>ASTORE LIVE: 14°C</span>
        </div>
    </section>

    <div class="container">
        
        <h2 class="section-title">Exclusive <span>Destinations</span></h2>
        <div class="grid">
            <div class="card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800&auto=format" alt="Rama">
                <div class="card-body">
                    <h3>Rama Meadows</h3>
                    <p>A panoramic valley at the foot of Nanga Parbat. Experience the serene Rama Lake and pine-scented air.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800&auto=format" alt="Deosai">
                <div class="card-body">
                    <h3>Deosai Plains</h3>
                    <p>The "Summer Palace" of the North. A high-altitude wilderness filled with wildflowers and crystal springs.</p>
                </div>
            </div>
        </div>

        <div style="text-align: center; margin: 60px 0;">
            <p style="color: var(--secondary); font-weight: 800; margin-bottom: 20px;">FOLLOW OUR JOURNEY</p>
            <div class="social-strip">
                <a href="#" class="social-icon"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#" class="social-icon"><i class="fa-brands fa-instagram"></i></a>
                <a href="#" class="social-icon"><i class="fa-brands fa-tiktok"></i></a>
            </div>
        </div>

        <h2 class="section-title" id="book">Plan Your <span>Adventure</span></h2>
        <div class="booking-ui">
            <form id="finalHubForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="whatsapp" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Expedition</option>
                    <option>Hunza Valley Luxury Retreat</option>
                    <option>Grand GB Safari (12 Days)</option>
                    <option>Custom Family Package</option>
                </select>
                <textarea id="notes" rows="4" placeholder="Tell us your travel dates and group size..."></textarea>
                <button type="submit" class="btn-premium">Inquire via WhatsApp</button>
            </form>
        </div>

        
        <div style="height: 350px; border-radius: 40px; overflow: hidden; margin: 50px 0 100px; border: 1px solid var(--border);">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1645.748721644782!2d74.8485292!3d34.9921612!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5db0c66000001%3A0x6d9539b36d07d9f9!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v1700000000000!5m2!1sen!2spk0" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg) brightness(0.8);"></iframe>
        </div>

    </div>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house-chimney"></i></a>
        <a href="#book"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <footer style="text-align: center; padding-bottom: 140px; opacity: 0.2; font-size: 10px; letter-spacing: 5px;">
        © 2026 ASTORE TOURIST HUB | EXPERIENCING THE NORTH
    </footer>

    <script>
        document.getElementById('finalHubForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const w = document.getElementById('whatsapp').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('notes').value;

            const text = `🚀 *OFFICIAL HUB INQUIRY*\n---\n👤 *Explorer:* ${n}\n📱 *WhatsApp:* ${w}\n🏔️ *Tour:* ${t}\n📝 *Notes:* ${m}\n---\n*Sent from AstoreHub.io*`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
