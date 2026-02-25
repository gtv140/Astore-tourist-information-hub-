<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Complete Gilgit-Baltistan Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00f2ff;
            --accent: #7000ff;
            --bg: #020617;
            --card-bg: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.08);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; }
        body { background: var(--bg); color: #fff; line-height: 1.6; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- Header & Hero --- */
        nav.top-nav {
            position: fixed; top: 0; width: 100%; padding: 20px 5%;
            display: flex; justify-content: space-between; align-items: center; 
            z-index: 1000; background: rgba(2, 6, 23, 0.8); backdrop-filter: blur(10px);
        }
        .logo { font-family: 'Syne'; font-weight: 800; font-size: 22px; }
        .logo span { color: var(--primary); }

        .hero {
            height: 100vh; position: relative; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1920&auto=format');
            background-size: cover; background-position: center; text-align: center;
        }
        .hero-content h1 { font-family: 'Syne'; font-size: clamp(45px, 10vw, 110px); line-height: 0.9; margin-bottom: 20px; }
        .hero-content span { color: var(--primary); }
        
        /* --- Weather Bar --- */
        .weather-bar { display: flex; gap: 20px; justify-content: center; margin-top: 30px; flex-wrap: wrap; }
        .weather-item { background: rgba(255,255,255,0.05); padding: 8px 15px; border-radius: 50px; font-size: 11px; border: 1px solid var(--border); }

        /* --- Global Sections --- */
        .container { max-width: 1250px; margin: 0 auto; padding: 80px 20px; }
        .section-title { font-family: 'Syne'; font-size: 38px; margin-bottom: 50px; text-align: center; }
        .section-title span { color: var(--primary); }

        /* --- Cards UI --- */
        .grid-layout { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px; }
        .info-card {
            background: var(--card-bg); border: 1px solid var(--border); border-radius: 30px;
            overflow: hidden; transition: 0.4s; position: relative;
        }
        .info-card:hover { transform: translateY(-10px); border-color: var(--primary); }
        .info-card img { width: 100%; height: 280px; object-fit: cover; }
        .card-body { padding: 30px; }
        .card-body h3 { font-family: 'Syne'; margin-bottom: 10px; color: var(--primary); }
        
        /* --- Packing Checklist --- */
        .essentials-box { background: rgba(0, 242, 255, 0.03); border-radius: 35px; padding: 40px; border: 1px solid var(--border); margin: 60px 0; }
        .check-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; margin-top: 25px; }
        .check-item { background: rgba(255,255,255,0.03); padding: 15px; border-radius: 15px; display: flex; align-items: center; gap: 10px; font-size: 13px; }
        .check-item i { color: var(--primary); }

        /* --- Form --- */
        .booking-section { background: linear-gradient(135deg, #0f172a 0%, #020617 100%); border-radius: 40px; padding: 50px; border: 1px solid var(--border); }
        .input-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        input, select, textarea {
            width: 100%; padding: 18px; border-radius: 15px; border: 1px solid var(--border);
            background: rgba(255,255,255,0.02); color: #fff; margin-bottom: 20px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); }
        .btn-submit {
            width: 100%; padding: 20px; border-radius: 15px; border: none;
            background: var(--primary); color: #000; font-weight: 800; text-transform: uppercase;
            cursor: pointer; transition: 0.3s;
        }
        .btn-submit:hover { box-shadow: 0 0 30px rgba(0,242,255,0.5); transform: scale(1.01); }

        /* --- Bottom Dock --- */
        .bottom-dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 420px; background: rgba(10, 10, 10, 0.85); backdrop-filter: blur(20px);
            padding: 15px 30px; border-radius: 100px; border: 1px solid var(--border);
            display: flex; justify-content: space-between; z-index: 2000;
        }
        .bottom-dock a { color: #fff; opacity: 0.5; font-size: 20px; transition: 0.3s; }
        .bottom-dock a:hover { color: var(--primary); opacity: 1; }

        @media (max-width: 768px) {
            .input-row { grid-template-columns: 1fr; }
            .hero-content h1 { font-size: 55px; }
            .section-title { font-size: 30px; }
        }
    </style>
</head>
<body>

    <nav class="top-nav">
        <div class="logo">ASTORE<span>HUB</span></div>
        <div style="font-size: 10px; letter-spacing: 2px; opacity: 0.7;">EXPLORE GB 2026</div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Experience the Heaven on Earth</p>
            <h1>PEAKS &<br><span>PARADISE</span></h1>
            <div class="weather-bar">
                <div class="weather-item"><i class="fa-solid fa-temperature-half"></i> Astore: 12°C</div>
                <div class="weather-item"><i class="fa-solid fa-cloud-sun"></i> Hunza: 16°C</div>
                <div class="weather-item"><i class="fa-solid fa-snowflake"></i> Deosai: 4°C</div>
            </div>
        </div>
    </section>

    <div class="container">
        
        <h2 class="section-title">Major <span>Destinations</span></h2>
        <div class="grid-layout">
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800" alt="Astore">
                <div class="card-body">
                    <h3>Astore Valley</h3>
                    <p>Known for Nanga Parbat base camps, Rama Meadows, and the historical Burzil Pass routes.</p>
                </div>
            </div>
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800" alt="Hunza">
                <div class="card-body">
                    <h3>Hunza Valley</h3>
                    <p>The crown jewel of KKH. Famous for Attabad Lake, Passu Cones, and Rakaposhi views.</p>
                </div>
            </div>
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1622324341735-906567087679?q=80&w=800" alt="Skardu">
                <div class="card-body">
                    <h3>Skardu City</h3>
                    <p>Gateway to K2. Explore Shangrila Lake, Upper Kachura, and the Katpana Cold Desert.</p>
                </div>
            </div>
        </div>

        <h2 class="section-title" style="margin-top: 80px;">Hidden <span>Gems</span></h2>
        <div class="grid-layout">
            <div class="info-card" style="height: auto;">
                <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800" alt="Minimarg">
                <div class="card-body">
                    <h4 style="color:var(--primary)">Minimarg & Domel</h4>
                    <p style="font-size: 13px;">The most untouched village in Astore. Access is restricted (Army permission required).</p>
                </div>
            </div>
            <div class="info-card" style="height: auto;">
                <img src="https://images.unsplash.com/photo-1590424753858-3bc67b8d0023?q=80&w=800" alt="Khaplu">
                <div class="card-body">
                    <h4 style="color:var(--primary)">Khaplu Valley</h4>
                    <p style="font-size: 13px;">Historical architecture and the beautiful Chaqchan Mosque await you here.</p>
                </div>
            </div>
        </div>

        <div class="essentials-box">
            <h2 style="font-family:'Syne'; text-align:center;">Travel <span>Essentials</span></h2>
            <p style="text-align:center; font-size:13px; opacity:0.6;">Don't leave home without these!</p>
            <div class="check-grid">
                <div class="check-item"><i class="fa-solid fa-circle-check"></i> SCOM Sim Card</div>
                <div class="check-item"><i class="fa-solid fa-circle-check"></i> Warm Jackets</div>
                <div class="check-item"><i class="fa-solid fa-circle-check"></i> Original CNIC</div>
                <div class="check-item"><i class="fa-solid fa-circle-check"></i> Power Bank</div>
                <div class="check-item"><i class="fa-solid fa-circle-check"></i> Cash (Lots of it)</div>
            </div>
        </div>

        <div class="booking-section" id="book">
            <h2 style="font-family:'Syne'; text-align:center; margin-bottom:30px;">Plan Your <span>Tour</span></h2>
            <form id="tourForm">
                <div class="input-row">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>Astore & Deosai Safari (Best for Nature)</option>
                    <option>Full GB Grand Tour (10 Days)</option>
                    <option>Hunza Luxury Package</option>
                    <option>Skardu Adventure Trip</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Any special requirements? (e.g. Group size, dates)"></textarea>
                <button type="submit" class="btn-submit">Submit Inquiry to Hub</button>
            </form>
        </div>

        <div style="border-radius: 30px; overflow: hidden; height: 400px; margin-top: 60px; border: 1px solid var(--border);">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d104524.34145616654!2d74.78168249726563!3d35.33481230000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5df988950d73d%3A0xc07f60756a147814!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v171588489!5m2!1sen!2spk0" width="100%" height="100%" frameborder="0" style="filter: grayscale(1) invert(1) brightness(0.8);"></iframe>
        </div>

    </div>

    <nav class="bottom-dock">
        <a href="#" title="Home"><i class="fa-solid fa-house"></i></a>
        <a href="#book" title="Explore"><i class="fa-solid fa-mountain"></i></a>
        <a href="#book" title="Book"><i class="fa-solid fa-calendar-days"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank"><i class="fa-brands fa-facebook"></i></a>
    </nav>

    <footer style="text-align: center; padding: 60px; opacity: 0.3; font-size: 10px; letter-spacing: 2px;">
        © 2026 ASTORE TOURIST HUB | EXPERIENCING GILGIT BALTISTAN
    </footer>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `*GB HUB - TOUR INQUIRY*\n---\n*Name:* ${n}\n*WhatsApp:* ${p}\n*Trip:* ${t}\n*Notes:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
