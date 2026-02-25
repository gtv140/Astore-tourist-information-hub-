<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Gilgit-Baltistan Ultimate Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00f2ff;
            --accent: #ff007a;
            --bg: #030712;
            --card-bg: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.08);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; }
        body { background: var(--bg); color: #fff; line-height: 1.6; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- Header & Nav --- */
        nav.top-nav {
            position: absolute; top: 0; width: 100%; padding: 30px;
            display: flex; justify-content: space-between; align-items: center; z-index: 100;
        }
        .logo { font-family: 'Syne'; font-weight: 800; font-size: 24px; letter-spacing: -1px; }
        .logo span { color: var(--primary); }

        /* --- Luxury Hero --- */
        .hero {
            height: 100vh; position: relative; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1920&auto=format&fit=crop');
            background-size: cover; background-position: center; text-align: center;
        }
        .hero-content h1 { font-family: 'Syne'; font-size: clamp(50px, 12vw, 120px); line-height: 0.85; margin-bottom: 20px; }
        .hero-content p { font-size: 14px; letter-spacing: 6px; text-transform: uppercase; opacity: 0.7; }

        /* --- Container --- */
        .container { max-width: 1300px; margin: 0 auto; padding: 80px 20px; }
        .section-header { text-align: center; margin-bottom: 60px; }
        .section-header h2 { font-family: 'Syne'; font-size: 40px; margin-bottom: 10px; }
        .section-header p { color: #888; }

        /* --- Modern Grid (USA Style) --- */
        .grid-layout { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px; }
        .info-card {
            background: var(--card-bg); border: 1px solid var(--border); border-radius: 32px;
            overflow: hidden; transition: 0.5s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .info-card:hover { transform: translateY(-15px); border-color: var(--primary); }
        .info-card img { width: 100%; height: 280px; object-fit: cover; }
        .info-card-body { padding: 30px; }
        .info-card-body .tag { font-size: 10px; font-weight: 800; color: var(--primary); text-transform: uppercase; letter-spacing: 2px; }
        .info-card-body h3 { margin: 10px 0; font-size: 24px; font-family: 'Syne'; }
        .info-card-body p { font-size: 14px; color: #9ca3af; }

        /* --- Detailed Guide Section --- */
        .gb-guide-section { background: rgba(255,255,255,0.02); border-radius: 40px; padding: 60px; border: 1px solid var(--border); margin: 60px 0; }
        .guide-topic { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; align-items: center; margin-bottom: 50px; }
        .guide-topic:nth-child(even) { direction: rtl; }
        .guide-topic:nth-child(even) .text-side { direction: ltr; }
        .guide-img { border-radius: 24px; overflow: hidden; height: 350px; }
        .guide-img img { width: 100%; height: 100%; object-fit: cover; }

        /* --- Booking / WhatsApp Form --- */
        .booking-ui { background: linear-gradient(135deg, #0f172a 0%, #020617 100%); border-radius: 40px; padding: 60px; border: 1px solid var(--border); }
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        input, select, textarea {
            width: 100%; padding: 20px; border-radius: 16px; border: 1px solid var(--border);
            background: rgba(255,255,255,0.03); color: #fff; margin-bottom: 20px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); }
        .btn-main {
            width: 100%; padding: 22px; border-radius: 16px; border: none;
            background: var(--primary); color: #000; font-weight: 800; text-transform: uppercase;
            cursor: pointer; transition: 0.3s; letter-spacing: 1px;
        }
        .btn-main:hover { box-shadow: 0 0 30px rgba(0,242,255,0.4); transform: scale(1.02); }

        /* --- Mobile Navigation Bar --- */
        .mobile-dock {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(20px); border-radius: 100px; padding: 15px 30px;
            display: flex; justify-content: space-between; border: 1px solid var(--border); z-index: 1000;
        }
        .mobile-dock a { color: #fff; opacity: 0.5; font-size: 20px; transition: 0.3s; }
        .mobile-dock a.active, .mobile-dock a:hover { opacity: 1; color: var(--primary); }

        /* Map styling */
        .map-frame { border-radius: 30px; overflow: hidden; height: 400px; margin-top: 50px; border: 1px solid var(--border); }
        .map-frame iframe { width: 100%; height: 100%; filter: grayscale(1) invert(1) brightness(0.8); }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 60px; }
            .guide-topic { grid-template-columns: 1fr; }
            .form-row { grid-template-columns: 1fr; }
            .gb-guide-section { padding: 30px; }
        }
    </style>
</head>
<body>

    <nav class="top-nav">
        <div class="logo">ASTORE<span>HUB</span></div>
        <div class="nav-links" style="display:flex; gap:30px; font-size: 12px; font-weight: 700; text-transform: uppercase; letter-spacing: 2px;">
            <a href="#explore" style="color:#fff; text-decoration:none;">Explore</a>
            <a href="#guide" style="color:#fff; text-decoration:none;">Guide</a>
            <a href="#book" style="color:#fff; text-decoration:none;">Booking</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Welcome to the Heaven</p>
            <h1>GILGIT<br><span>BALTISTAN</span></h1>
            <div style="margin-top: 20px; font-size: 11px; opacity: 0.6; letter-spacing: 4px;">OFFICIAL VISITOR INFORMATION 2026</div>
        </div>
    </section>

    <div class="container" id="explore">
        <div class="section-header">
            <h2>Explore The North</h2>
            <p>Select your next destination from our premium curated list.</p>
        </div>

        <div class="grid-layout">
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800" alt="Astore">
                <div class="info-card-body">
                    <span class="tag">Main Gateway</span>
                    <h3>Astore Valley</h3>
                    <p>Home to Rama Meadows and the gateway to Nanga Parbat. Perfect for camping and hiking.</p>
                </div>
            </div>
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800" alt="Hunza">
                <div class="info-card-body">
                    <span class="tag">Cultural Hub</span>
                    <h3>Hunza Valley</h3>
                    <p>Known for its historical forts, hospitality, and the stunning Attabad Lake. A must-visit for everyone.</p>
                </div>
            </div>
            <div class="info-card">
                <img src="https://images.unsplash.com/photo-1622324341735-906567087679?q=80&w=800" alt="Skardu">
                <div class="info-card-body">
                    <span class="tag">Mountain Hub</span>
                    <h3>Skardu & Baltistan</h3>
                    <p>The base for K2 climbers. Visit Shangrila, Lower Kachura, and the mesmerizing Cold Deserts.</p>
                </div>
            </div>
        </div>

        <div class="gb-guide-section" id="guide">
            <h2 style="font-family:'Syne'; text-align:center; margin-bottom:50px; font-size:36px;">Full <span>Travel Guide</span></h2>
            
            <div class="guide-topic">
                <div class="guide-img">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800" alt="Deosai">
                </div>
                <div class="text-side">
                    <h3 style="color:var(--primary); margin-bottom:15px;">1. Deosai National Park</h3>
                    <p>Duniya ka doosra sab se uncha plateau (Roof of the World). Yahan Himalayan Brown Bears aur Sheosar Lake milti hai. Astore ya Skardu dono se access mumkin hai.</p>
                </div>
            </div>

            <div class="guide-topic">
                <div class="guide-img">
                    <img src="https://images.unsplash.com/photo-1590424753858-3bc67b8d0023?q=80&w=800" alt="Transport">
                </div>
                <div class="text-side">
                    <h3 style="color:var(--primary); margin-bottom:15px;">2. Transport & Routes</h3>
                    <p>Gilgit-Baltistan ke liye Karakoram Highway (KKH) behtareen hai. Lekin Astore aur Deosai ke liye hamesha **4x4 Jeeps** use karein. Rawalpindi se bus aur plane (PIA) dono options hain.</p>
                </div>
            </div>
        </div>

        <div class="booking-ui" id="book">
            <h2 style="font-family:'Syne'; text-align:center; margin-bottom:40px;">Plan Your <span>Adventure</span></h2>
            <form id="tourForm">
                <div class="form-row">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>Astore & Deosai Safari (7 Days)</option>
                    <option>Hunza & Nagar Expedition (5 Days)</option>
                    <option>Skardu Luxury Package (6 Days)</option>
                    <option>Fairy Meadows Trekking (4 Days)</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Mention group size and preferred dates..."></textarea>
                <button type="submit" class="btn-main">Connect with Information Hub</button>
            </form>
        </div>

        <div class="map-frame">
            <iframe src="http://googleusercontent.com/maps.google.com/8"></iframe>
        </div>
    </div>

    <nav class="mobile-dock">
        <a href="#"><i class="fa-solid fa-house"></i></a>
        <a href="#explore"><i class="fa-solid fa-compass"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank"><i class="fa-brands fa-facebook"></i></a>
    </nav>

    <footer style="text-align:center; padding: 60px; opacity:0.3; font-size:10px; letter-spacing:3px;">
        © 2026 ASTORE TOURIST HUB | GILGIT-BALTISTAN TOURISM
    </footer>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `*GB ADVENTURE INQUIRY*\n---\n*Explorer:* ${n}\n*WhatsApp:* ${p}\n*Plan:* ${t}\n*Details:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
