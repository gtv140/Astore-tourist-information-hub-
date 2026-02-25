<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore & GB Tourist Hub | 2026 Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;700&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --accent: #00f2ff;
            --deep-blue: #020617;
            --glass: rgba(255, 255, 255, 0.05);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Plus Jakarta Sans', sans-serif; background: var(--deep-blue); color: #fff; overflow-x: hidden; scroll-behavior: smooth; }

        /* Hero Section with Fixed Background */
        .hero {
            height: 100vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.6), var(--deep-blue)), 
                        url('https://source.unsplash.com/featured/?mountains,nature,pakistan');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;
        }

        .hero h1 { font-family: 'Syne', sans-serif; font-size: clamp(45px, 10vw, 100px); line-height: 0.9; margin-bottom: 20px; }
        .hero span { color: var(--accent); text-shadow: 0 0 20px rgba(0, 242, 255, 0.5); }

        /* Floating Nav Dock */
        .dock {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 420px; background: rgba(15, 23, 42, 0.8);
            backdrop-filter: blur(25px); padding: 15px; border-radius: 100px;
            display: flex; justify-content: space-around; border: 1px solid var(--border); z-index: 1000;
        }
        .dock a { color: #fff; text-decoration: none; font-size: 22px; transition: 0.3s; opacity: 0.6; }
        .dock a:hover { color: var(--accent); opacity: 1; transform: translateY(-5px); }

        /* Sections */
        .section { padding: 60px 20px; max-width: 1200px; margin: 0 auto; }
        .section-title { font-family: 'Syne', sans-serif; font-size: 36px; margin-bottom: 40px; text-align: center; }

        /* Destination Cards */
        .gb-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; }
        .dest-card {
            height: 450px; border-radius: 35px; overflow: hidden; position: relative;
            border: 1px solid var(--border); transition: 0.5s cubic-bezier(0.2, 1, 0.2, 1);
        }
        .dest-card:hover { transform: translateY(-10px); border-color: var(--accent); }
        .dest-card img { width: 100%; height: 100%; object-fit: cover; }
        
        .dest-overlay {
            position: absolute; bottom: 0; width: 100%; padding: 40px 30px;
            background: linear-gradient(transparent, rgba(2, 6, 23, 0.95));
        }

        /* Information Glass Hub */
        .glass-panel {
            background: var(--glass); backdrop-filter: blur(20px); border-radius: 40px; padding: 40px;
            border: 1px solid var(--border); margin-top: 30px;
        }

        /* Modern Form */
        input, select, textarea {
            width: 100%; padding: 18px; border-radius: 20px; border: 1px solid var(--border);
            background: rgba(255,255,255,0.03); color: #fff; margin-bottom: 20px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--accent); background: rgba(255,255,255,0.08); }

        .btn-premium {
            width: 100%; padding: 20px; border-radius: 20px; border: none;
            background: linear-gradient(90deg, #00f2ff, #0066ff); color: #000;
            font-weight: 800; text-transform: uppercase; letter-spacing: 2px;
            cursor: pointer; transition: 0.4s;
        }
        .btn-premium:hover { box-shadow: 0 10px 40px rgba(0, 242, 255, 0.4); transform: scale(1.02); }

        /* Mobile Map */
        .map-box iframe { width: 100%; height: 300px; border-radius: 35px; filter: invert(90%) hue-rotate(180deg); }

        @media (max-width: 768px) { .hero h1 { font-size: 55px; } }
    </style>
</head>
<body>

    <header class="hero">
        <div style="border: 1px solid var(--accent); padding: 5px 20px; border-radius: 50px; font-size: 11px; color: var(--accent); margin-bottom: 15px; letter-spacing: 3px;">GATEWAY TO HEAVEN</div>
        <h1>ASTORE<br><span>HUB</span></h1>
        <p style="opacity: 0.6; font-size: 13px; letter-spacing: 6px; font-weight: 300;">GILGIT BALTISTAN ULTIMATE GUIDE</p>
    </header>

    <section class="section" id="explore">
        <h2 class="section-title">Explore The North</h2>
        <div class="gb-grid">
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=800" alt="Astore Valley">
                <div class="dest-overlay">
                    <small style="color:var(--accent)">CENTER HUB</small>
                    <h3>Astore Valley</h3>
                    <p style="font-size:13px; opacity:0.7; margin-top:5px;">Explore Rama Meadows, Lake & The Mighty Deosai Plains.</p>
                </div>
            </div>
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1622324341735-906567087679?auto=format&fit=crop&w=800" alt="Skardu">
                <div class="dest-overlay">
                    <small>BALTISTAN</small>
                    <h3>Skardu City</h3>
                    <p style="font-size:13px; opacity:0.7; margin-top:5px;">Land of Shangrila Lake, Cold Desert and K2 Basecamp.</p>
                </div>
            </div>
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?auto=format&fit=crop&w=800" alt="Hunza">
                <div class="dest-overlay">
                    <small>GILGIT</small>
                    <h3>Hunza Valley</h3>
                    <p style="font-size:13px; opacity:0.7; margin-top:5px;">Famous for Altit/Baltit Forts and the Attabad Lake.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="booking">
        <div class="glass-panel">
            <h2 style="text-align:left; margin-bottom:25px;"><i class="fa-solid fa-paper-plane"></i> Plan Your Journey</h2>
            <form id="gbForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap:20px;">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tourType">
                    <option>Astore & Deosai Safari (Best Seller)</option>
                    <option>Skardu Luxury Tour</option>
                    <option>Hunza Cultural Trip</option>
                    <option>Fairy Meadows Trekking</option>
                </select>
                <textarea rows="4" id="notes" placeholder="Any specific requirements or group size?"></textarea>
                <button type="submit" class="btn-premium">Connect with Hub Expert</button>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="map-box">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d418247.9404245645!2d74.6545199187332!3d35.15509981878954!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e679a9538a7c6f%3A0xc3f847625f18706d!2sAstore%20Valley!5e0!3m2!1sen!2s!4v1700000000000!5m2!1sen!2s"></iframe>
        </div>
        <div style="margin-top:40px; display:flex; justify-content:center; gap:30px;">
            <a href="https://wa.me/923171588489" style="color:#25d366; font-size:35px;"><i class="fa-brands fa-whatsapp"></i></a>
            <a href="https://www.facebook.com/share/1BoG9YCsZN/" style="color:#1877f2; font-size:35px;"><i class="fa-brands fa-facebook"></i></a>
        </div>
        <p style="text-align:center; margin-top:40px; font-size:10px; opacity:0.4;">© 2026 ASTORE TOURIST HUB | EXPERIENCING GILGIT BALTISTAN</p>
    </section>

    <nav class="dock">
        <a href="#"><i class="fa-solid fa-house-chimney"></i></a>
        <a href="#explore"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#booking"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <script>
        document.getElementById('gbForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tourType').value;
            const msg = document.getElementById('notes').value;
            const wa_msg = `*GB HUB EXPLORER INQUIRY*\n---\n*Name:* ${n}\n*Phone:* ${p}\n*Tour:* ${t}\n*Notes:* ${msg}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(wa_msg)}`, '_blank');
        };
    </script>
</body>
</html>
