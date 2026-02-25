<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Luxury Digital Guide</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #ff00c8;
            --accent: #7000ff;
            --bg: #030712;
            --glass: rgba(255, 255, 255, 0.05);
            --border: rgba(255, 255, 255, 0.12);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        
        body { 
            background: var(--bg); 
            color: #fff; 
            font-family: 'Plus Jakarta Sans', sans-serif; 
            overflow-x: hidden;
            background: linear-gradient(45deg, #030712, #0f172a, #030712);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* --- Header --- */
        nav {
            position: sticky; top: 0; width: 100%; padding: 20px 6%;
            background: rgba(3, 7, 18, 0.85); backdrop-filter: blur(20px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 24px; font-weight: 800; letter-spacing: -1px; }
        .logo span { background: linear-gradient(to right, var(--primary), var(--secondary)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }

        /* --- Hero --- */
        .hero {
            padding: 80px 20px; text-align: center;
            position: relative; overflow: hidden;
        }
        .hero h1 { 
            font-family: 'Syne'; font-size: clamp(45px, 15vw, 90px); 
            line-height: 0.8; margin-bottom: 20px; text-transform: uppercase;
            filter: drop-shadow(0 0 20px rgba(0,242,255,0.3));
        }
        .weather-pills { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; }
        .pill { 
            background: var(--glass); border: 1px solid var(--primary);
            padding: 8px 18px; border-radius: 50px; font-size: 12px; font-weight: 800;
            box-shadow: 0 0 15px rgba(0,242,255,0.1);
        }

        /* --- Main Content --- */
        .container { max-width: 1100px; margin: 0 auto; padding: 40px 20px; }
        .section-tag { color: var(--secondary); font-weight: 800; font-size: 12px; letter-spacing: 4px; text-transform: uppercase; margin-bottom: 10px; display: block; }
        
        /* --- Modern Glass Cards --- */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .glass-card {
            background: var(--glass); border-radius: 35px; border: 1px solid var(--border);
            overflow: hidden; transition: 0.5s; backdrop-filter: blur(10px);
        }
        .glass-card:hover { border-color: var(--primary); transform: translateY(-10px) scale(1.02); box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
        .img-wrap { height: 260px; width: 100%; position: relative; }
        .img-wrap img { width: 100%; height: 100%; object-fit: cover; }
        .card-body { padding: 30px; }
        .card-body h3 { font-family: 'Syne'; font-size: 26px; margin-bottom: 15px; color: var(--primary); }
        .card-body p { font-size: 14px; color: #94a3b8; line-height: 1.7; margin-bottom: 15px; }
        .meta { display: flex; gap: 15px; font-size: 11px; font-weight: 700; color: var(--secondary); }

        /* --- Extra Details Section --- */
        .info-strip { 
            background: linear-gradient(to right, var(--accent), var(--secondary));
            padding: 40px; border-radius: 30px; margin: 60px 0; text-align: center;
        }
        .info-strip h2 { font-family: 'Syne'; font-size: 32px; margin-bottom: 10px; }

        /* --- Booking UI --- */
        .booking-ui {
            background: rgba(255,255,255,0.02); padding: 40px; border-radius: 40px;
            border: 2px solid var(--border); box-shadow: 0 30px 60px rgba(0,0,0,0.5);
        }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 20px; border-radius: 18px;
            border: 1px solid var(--border); background: #000; color: #fff; font-size: 16px; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); background: #080c14; }
        .btn-rainbow {
            width: 100%; padding: 22px; border-radius: 18px; border: none;
            background: linear-gradient(to right, var(--primary), var(--accent));
            color: #000; font-weight: 800; font-size: 16px; cursor: pointer; text-transform: uppercase;
            transition: 0.4s;
        }
        .btn-rainbow:hover { transform: scale(1.02); box-shadow: 0 10px 30px var(--primary); letter-spacing: 1px; }

        /* --- Fixed Dock --- */
        .nav-dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(0,0,0,0.8);
            backdrop-filter: blur(25px); border-radius: 100px; padding: 15px 30px;
            display: flex; justify-content: space-between; align-items: center;
            border: 1px solid var(--border); z-index: 2000; box-shadow: 0 20px 50px rgba(0,0,0,0.8);
        }
        .nav-dock a { color: #fff; opacity: 0.4; font-size: 24px; transition: 0.3s; }
        .nav-dock a.active { color: var(--primary); opacity: 1; transform: scale(1.2); }

        footer { text-align: center; padding: 100px 20px 150px; opacity: 0.2; font-size: 10px; letter-spacing: 5px; }

        @media (max-width: 600px) {
            .hero h1 { font-size: 55px; }
            .booking-ui { padding: 25px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div id="live-time" style="font-size: 12px; font-weight: 800; color: var(--primary);">00:00:00</div>
    </nav>

    <section class="hero">
        <span class="section-tag">Explore Gilgit Baltistan</span>
        <h1>PEAKS OF<br><span>HEAVEN</span></h1>
        <div class="weather-pills">
            <div class="pill"><i class="fa-solid fa-sun"></i> Astore: 14°C</div>
            <div class="pill"><i class="fa-solid fa-wind"></i> Wind: 5km/h</div>
            <div class="pill"><i class="fa-solid fa-mountain"></i> Elev: 2600m</div>
        </div>
    </section>

    <div class="container">
        
        <span class="section-tag">Featured Trips</span>
        <h2 style="font-family:'Syne'; font-size: 36px; margin-bottom: 30px;">Choose Your Journey</h2>

        <div class="grid">
            <div class="glass-card">
                <div class="img-wrap">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=800" alt="Rama">
                </div>
                <div class="card-body">
                    <div class="meta"><span>7 DAYS</span><span>⭐ 4.9</span></div>
                    <h3>Rama Meadows</h3>
                    <p>The "Crown Jewel" of Astore. Experience cedar forests, the alpine Rama Lake, and a direct face-to-face view of Nanga Parbat's eastern face.</p>
                </div>
            </div>

            <div class="glass-card">
                <div class="img-wrap">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&fit=crop&w=800" alt="Deosai">
                </div>
                <div class="card-body">
                    <div class="meta"><span>5 DAYS</span><span>⭐ 5.0</span></div>
                    <h3>Deosai Plains</h3>
                    <p>The "Land of Giants". A massive high-altitude plateau where the sky meets the earth. Home to Himalayan Brown Bears and Sheosar Lake.</p>
                </div>
            </div>
        </div>

        

        <div class="info-strip">
            <h2>Why Travel With Us?</h2>
            <p>We are locals. We know the shortcuts, the hidden springs, and the best trout spots.</p>
        </div>

        <span class="section-tag" id="book">Plan Your Escape</span>
        <h2 style="font-family:'Syne'; font-size: 36px; margin-bottom: 30px;">Get a Free Quote</h2>
        
        <div class="booking-ui">
            <form id="masterForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px;">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>Astore & Deosai Explorer (Best Value)</option>
                    <option>The Hunza Valley Luxury Retreat</option>
                    <option>Grand Northern Expedition (12 Days)</option>
                    <option>Custom Photography Tour</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Group size? Preferred dates? Any health conditions?"></textarea>
                <button type="submit" class="btn-rainbow">Launch My Adventure</button>
            </form>
        </div>

        <div style="height: 350px; border-radius: 40px; overflow: hidden; margin-top: 60px; border: 1px solid var(--border); filter: grayscale(1) invert(1) contrast(1.2);">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3266.386928014565!2d74.8492!3d35.3672!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e68b37568f114d%3A0xc66513364f7b44d3!2sAstore!5e0!3m2!1sen!2spk!4v1700000000000!5m2!1sen!2spk" width="100%" height="100%" frameborder="0"></iframe>
        </div>

    </div>

    <nav class="nav-dock">
        <a href="#" class="active"><i class="fa-solid fa-house-chimney-window"></i></a>
        <a href="#book"><i class="fa-solid fa-compass"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-day"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <footer>
        © 2026 ASTORE TOURIST HUB | BEYOND THE PEAKS
    </footer>

    <script>
        // Real-time Clock Update
        function updateClock() {
            const now = new Date();
            document.getElementById('live-time').innerText = now.toLocaleTimeString();
        }
        setInterval(updateClock, 1000);
        updateClock();

        // Professional WhatsApp Form
        document.getElementById('masterForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `🔥 *NEW EXPEDITION INQUIRY*\n---\n👤 *Explorer:* ${n}\n📱 *WhatsApp:* ${p}\n🏔️ *Selected Tour:* ${t}\n📝 *Notes:* ${m}\n---\n*Sent from Astore Hub v2.0*`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
