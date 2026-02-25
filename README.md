<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore & GB Ultimate Hub | 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@400;700&family=Outfit:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00d2ff;
            --accent: #3a7bd5;
            --bg: #010409;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Outfit', sans-serif; background: var(--bg); color: #fff; scroll-behavior: smooth; overflow-x: hidden; }

        /* Hero Section */
        .hero {
            height: 100vh; width: 100%; position: relative;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.5), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1920&auto=format&fit=crop');
            background-size: cover; background-position: center; text-align: center;
        }

        .hero h1 {
            font-family: 'Unbounded', sans-serif; font-size: clamp(35px, 8vw, 80px);
            text-transform: uppercase; line-height: 1; margin-bottom: 15px;
            background: linear-gradient(to right, #fff, var(--primary));
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
        }

        /* Weather Widget */
        .weather-row { display: flex; gap: 15px; margin-top: 20px; }
        .weather-chip { background: var(--glass); padding: 10px 20px; border-radius: 50px; border: 1px solid var(--border); font-size: 12px; backdrop-filter: blur(10px); }

        /* Destination Section */
        .section-header { padding: 60px 20px 20px; text-align: center; }
        .section-header h2 { font-family: 'Unbounded'; font-size: 22px; color: var(--primary); }

        .dest-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; padding: 20px; max-width: 1200px; margin: 0 auto; }
        
        .dest-card {
            height: 450px; border-radius: 40px; overflow: hidden; position: relative;
            border: 1px solid var(--border); transition: 0.5s;
        }
        .dest-card:hover { transform: translateY(-10px); border-color: var(--primary); }
        .dest-card img { width: 100%; height: 100%; object-fit: cover; transition: 0.5s; }
        .dest-card:hover img { transform: scale(1.1); }
        
        .dest-overlay {
            position: absolute; bottom: 0; left: 0; right: 0; padding: 40px 30px;
            background: linear-gradient(transparent, rgba(1, 4, 9, 0.95));
        }

        /* Information Hub Glass */
        .info-hub { background: var(--glass); margin: 20px; padding: 30px; border-radius: 30px; border: 1px solid var(--border); max-width: 1100px; margin: 40px auto; }
        
        /* Modern Form */
        .booking-form { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 30px; }
        input, select, textarea {
            width: 100%; background: rgba(255,255,255,0.05); border: 1px solid var(--border);
            padding: 18px; border-radius: 20px; color: #fff; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); }

        .btn-glow {
            width: 100%; padding: 20px; border-radius: 20px; border: none;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: #000; font-weight: 700; text-transform: uppercase; cursor: pointer; transition: 0.4s;
        }
        .btn-glow:hover { box-shadow: 0 0 30px rgba(0, 210, 255, 0.4); transform: scale(1.02); }

        /* Floating Navigation Dock */
        .dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 85%; max-width: 450px; background: rgba(1, 4, 9, 0.85);
            backdrop-filter: blur(20px); padding: 15px 30px; border-radius: 100px;
            border: 1px solid var(--border); display: flex; justify-content: space-between; z-index: 1000;
        }
        .dock a { color: #fff; opacity: 0.5; font-size: 20px; transition: 0.3s; }
        .dock a:hover { color: var(--primary); opacity: 1; transform: translateY(-5px); }

        /* Map styling */
        .map-box { padding: 20px; }
        .map-box iframe { width: 100%; height: 350px; border-radius: 40px; filter: grayscale(1) invert(1) brightness(0.8); border: 1px solid var(--border); }

        @media (max-width: 600px) { .hero h1 { font-size: 40px; } .weather-row { flex-direction: column; } }
    </style>
</head>
<body>

    <section class="hero">
        <div style="background: rgba(0,210,255,0.15); padding: 5px 20px; border-radius: 50px; font-size: 11px; color: var(--primary); margin-bottom: 10px; letter-spacing: 3px;">EXPLORE GILGIT BALTISTAN</div>
        <h1>ASTORE HUB</h1>
        <p style="letter-spacing: 5px; opacity: 0.7; font-size: 12px;">YOUR JOURNEY TO THE HEAVENS BEGINS HERE</p>
        
        <div class="weather-row">
            <div class="weather-chip"><i class="fa-solid fa-temperature-low"></i> Astore: 8°C (Snowy)</div>
            <div class="weather-chip"><i class="fa-solid fa-sun"></i> Hunza: 14°C (Clear)</div>
        </div>
    </section>

    <div class="section-header">
        <h2>THE NORTHERN WONDERS</h2>
        <p style="font-size: 13px; color: #666; margin-top: 10px;">Select your next adventure across Gilgit-Baltistan</p>
    </div>

    <div class="dest-grid">
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800&auto=format&fit=crop" alt="Rama Astore">
            <div class="dest-overlay">
                <span style="color: var(--primary); font-size: 11px; font-weight: 700;">ASTORE VALLEY</span>
                <h3>Rama Meadows</h3>
                <p style="font-size: 13px; opacity: 0.7; margin-top: 5px;">A emerald green paradise surrounded by pine forests and the Rama Lake.</p>
            </div>
        </div>

        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800&auto=format&fit=crop" alt="Deosai">
            <div class="dest-overlay">
                <span style="color: var(--primary); font-size: 11px; font-weight: 700;">SKARDU</span>
                <h3>Deosai Plains</h3>
                <p style="font-size: 13px; opacity: 0.7; margin-top: 5px;">Known as the 'Roof of the World', a massive plateau with rare wildlife.</p>
            </div>
        </div>

        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800&auto=format&fit=crop" alt="Hunza">
            <div class="dest-overlay">
                <span style="color: var(--primary); font-size: 11px; font-weight: 700;">HUNZA VALLEY</span>
                <h3>Altit & Baltit</h3>
                <p style="font-size: 13px; opacity: 0.7; margin-top: 5px;">Centuries of history, ancient forts, and the famous Attabad Lake.</p>
            </div>
        </div>
    </div>

    <section class="info-hub" id="info">
        <h2 style="font-family: 'Unbounded'; font-size: 18px; margin-bottom: 15px;">Travel Tips for GB</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px;">
            <div style="padding: 15px; border-left: 2px solid var(--primary);">
                <h4 style="font-size: 14px;">Best Season</h4>
                <p style="font-size: 12px; color: #888;">May to October for road trips. Nov to Feb for snow lovers.</p>
            </div>
            <div style="padding: 15px; border-left: 2px solid var(--primary);">
                <h4 style="font-size: 14px;">Transport</h4>
                <p style="font-size: 12px; color: #888;">4x4 Jeeps are mandatory for Astore & Deosai routes.</p>
            </div>
            <div style="padding: 15px; border-left: 2px solid var(--primary);">
                <h4 style="font-size: 14px;">Connectivity</h4>
                <p style="font-size: 12px; color: #888;">SCOM is the only reliable network in remote areas.</p>
            </div>
        </div>
    </section>

    <section class="info-hub" id="book">
        <h2 style="font-family: 'Unbounded'; font-size: 18px;">Plan Your Trip</h2>
        <p style="font-size: 12px; color: #666;">Contact our expert guides for a custom tour plan.</p>
        <form id="tourForm" class="booking-form">
            <input type="text" id="name" placeholder="Full Name" required>
            <input type="tel" id="phone" placeholder="WhatsApp Number" required>
            <select id="tour">
                <option>Astore & Deosai Safari</option>
                <option>Full GB Luxury Package</option>
                <option>Hunza & Nagar Expedition</option>
                <option>Skardu & Khaplu Tour</option>
            </select>
            <textarea id="msg" placeholder="Tell us about your group size and dates..."></textarea>
            <button type="submit" class="btn-glow">Connect with Expert</button>
        </form>
    </section>

    <div class="map-box">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d105263.95759714811!2d74.786961!3d34.96695!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e1293a38096f97%3A0xc6c4f9011e4c7003!2sAstore!5e0!3m2!1sen!2spk!4v1700000000000"></iframe>
    </div>

    <div style="text-align: center; padding: 40px;">
        <div style="display: flex; justify-content: center; gap: 30px; margin-bottom: 20px;">
            <a href="https://wa.me/923171588489" style="color:#25d366; font-size: 30px;"><i class="fa-brands fa-whatsapp"></i></a>
            <a href="https://www.facebook.com/share/1BoG9YCsZN/" style="color:#1877f2; font-size: 30px;"><i class="fa-brands fa-facebook"></i></a>
        </div>
        <p style="font-size: 10px; opacity: 0.4;">© 2026 ASTORE HUB | BUILT FOR THE ADVENTURERS</p>
    </div>

    <nav class="dock">
        <a href="#" title="Home"><i class="fa-solid fa-house-user"></i></a>
        <a href="#info" title="Guide"><i class="fa-solid fa-map-marked-alt"></i></a>
        <a href="#book" title="Book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank" title="Chat"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const waMsg = `*GB HUB - TRIP INQUIRY*\n---\n*Name:* ${n}\n*WhatsApp:* ${p}\n*Tour:* ${t}\n*Note:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(waMsg)}`, '_blank');
        };
    </script>
</body>
</html>
