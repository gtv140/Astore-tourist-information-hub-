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
            --accent: #ff007a;
            --bg: #010409;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- Custom Scrollbar --- */
        ::-webkit-scrollbar { width: 5px; }
        ::-webkit-scrollbar-track { background: var(--bg); }
        ::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 10px; }

        /* --- Navigation --- */
        nav {
            position: fixed; top: 0; width: 100%; padding: 20px 6%;
            background: rgba(1, 4, 9, 0.8); backdrop-filter: blur(20px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 22px; font-weight: 800; letter-spacing: -1px; }
        .logo span { color: var(--primary); text-shadow: 0 0 15px rgba(0,242,255,0.5); }

        /* --- Hero Section --- */
        .hero {
            height: 90vh; position: relative; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.4), var(--bg)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1600&auto=format') no-repeat center center/cover;
            text-align: center; overflow: hidden;
        }
        .hero-content h1 { font-family: 'Syne'; font-size: clamp(45px, 12vw, 120px); line-height: 0.85; margin-bottom: 20px; text-transform: uppercase; }
        .hero-content p { font-size: 11px; letter-spacing: 6px; color: var(--primary); text-transform: uppercase; font-weight: 800; }

        /* --- Main Layout --- */
        .container { max-width: 1200px; margin: 0 auto; padding: 60px 20px; }
        .section-header { margin-bottom: 50px; text-align: center; }
        .section-header h2 { font-family: 'Syne'; font-size: 40px; margin-bottom: 10px; }
        .section-header p { opacity: 0.6; font-size: 14px; }

        /* --- Premium Cards --- */
        .tour-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .tour-card {
            background: var(--glass); border-radius: 30px; overflow: hidden;
            border: 1px solid var(--border); transition: all 0.5s cubic-bezier(0.23, 1, 0.32, 1);
            position: relative;
        }
        .tour-card:hover { border-color: var(--primary); transform: translateY(-10px) scale(1.02); background: rgba(255,255,255,0.06); }
        .img-wrapper { height: 280px; width: 100%; position: relative; }
        .img-wrapper img { width: 100%; height: 100%; object-fit: cover; }
        .badge { position: absolute; top: 20px; right: 20px; background: var(--primary); color: #000; padding: 5px 15px; border-radius: 50px; font-size: 10px; font-weight: 800; }
        
        .content { padding: 30px; }
        .content h3 { font-family: 'Syne'; font-size: 24px; margin-bottom: 12px; }
        .content p { font-size: 14px; opacity: 0.7; line-height: 1.6; }

        /* --- Route Info Section --- */
        .route-section { background: rgba(255,255,255,0.02); border-radius: 40px; padding: 40px; border: 1px solid var(--border); margin: 60px 0; }
        .step { display: flex; gap: 20px; margin-bottom: 30px; }
        .step-num { min-width: 40px; height: 40px; background: var(--primary); color: #000; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 800; }

        /* --- Premium Form --- */
        .booking-ui { background: linear-gradient(145deg, #0d1117, #010409); border-radius: 40px; padding: 40px; border: 1px solid var(--primary); box-shadow: 0 20px 50px rgba(0,242,255,0.1); }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 20px; border-radius: 15px;
            border: 1px solid var(--border); background: rgba(255,255,255,0.03); color: #fff; font-size: 16px; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); box-shadow: 0 0 15px rgba(0,242,255,0.2); }
        .btn-glow {
            width: 100%; padding: 20px; background: var(--primary); color: #000;
            border: none; border-radius: 15px; font-weight: 800; text-transform: uppercase; cursor: pointer; transition: 0.4s;
        }
        .btn-glow:hover { letter-spacing: 2px; box-shadow: 0 0 30px var(--primary); }

        /* --- Floating Actions --- */
        .wa-btn { position: fixed; bottom: 100px; right: 25px; background: #25d366; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; color: #fff; z-index: 999; box-shadow: 0 10px 20px rgba(0,0,0,0.3); }

        /* --- Mobile Navigation Dock --- */
        .mobile-nav {
            position: fixed; bottom: 0; width: 100%; background: rgba(1,4,9,0.9);
            backdrop-filter: blur(20px); display: flex; justify-content: space-around;
            padding: 15px 0 25px; border-top: 1px solid var(--border); z-index: 1000;
        }
        .mobile-nav a { color: #fff; opacity: 0.4; font-size: 22px; transition: 0.3s; }
        .mobile-nav a.active { color: var(--primary); opacity: 1; transform: translateY(-5px); }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 55px; }
            .section-header h2 { font-size: 30px; }
            .booking-ui { padding: 25px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div style="font-size: 10px; font-weight: 800; color: var(--primary); background: rgba(0,242,255,0.1); padding: 4px 10px; border-radius: 5px;">LIVE 2026</div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Your Portal to the North</p>
            <h1>BEYOND THE<br><span>MOUNTAINS</span></h1>
            <div style="margin-top:30px; display:flex; gap:15px; justify-content:center;">
                <div style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:50px; font-size:12px; border:1px solid var(--border);">Astore: 14°C</div>
                <div style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:50px; font-size:12px; border:1px solid var(--border);">Skardu: 11°C</div>
            </div>
        </div>
    </section>

    <div class="container">
        
        <div class="section-header">
            <h2>Luxury <span>Destinations</span></h2>
            <p>Curated experiences for the modern traveler.</p>
        </div>

        <div class="tour-grid">
            <div class="tour-card">
                <div class="img-wrapper">
                    <span class="badge">Most Popular</span>
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800" alt="Astore">
                </div>
                <div class="content">
                    <h3>Rama Meadows</h3>
                    <p>The emerald heart of Astore. Surrounded by cedar forests and the shadow of Nanga Parbat.</p>
                </div>
            </div>

            <div class="tour-card">
                <div class="img-wrapper">
                    <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800" alt="Hunza">
                </div>
                <div class="content">
                    <h3>Hunza Valley</h3>
                    <p>Historical forts, crystal lakes, and the world-famous Karimabad market experience.</p>
                </div>
            </div>

            <div class="tour-card">
                <div class="img-wrapper">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800" alt="Deosai">
                </div>
                <div class="content">
                    <h3>Deosai Plains</h3>
                    <p>A high-altitude wilderness home to brown bears and the majestic Sheosar Lake.</p>
                </div>
            </div>
        </div>

        <div class="route-section">
            <h2 style="font-family:'Syne'; margin-bottom:30px; text-align:center;">The <span>Journey</span> Map</h2>
            <div class="step">
                <div class="step-num">1</div>
                <div>
                    <h4>Islamabad to Chilas</h4>
                    <p style="font-size:13px; opacity:0.6;">Start your journey via the Hazara Motorway and Naran-Babusar Top (Seasonal) or KKH.</p>
                </div>
            </div>
            <div class="step">
                <div class="step-num">2</div>
                <div>
                    <h4>Chilas to Astore</h4>
                    <p style="font-size:13px; opacity:0.6;">A 3-hour adventurous drive from the Raikot Bridge leads you into the heart of Astore.</p>
                </div>
            </div>
        </div>

        

        <div class="section-header" id="book">
            <h2>Plan Your <span>Adventure</span></h2>
            <p>Fill out the form and our hub will contact you on WhatsApp.</p>
        </div>

        <div class="booking-ui">
            <form id="masterForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:20px;">
                    <input type="text" id="name" placeholder="Your Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tourType">
                    <option>Astore & Deosai Explorer (7 Days)</option>
                    <option>The Grand GB Tour (12 Days)</option>
                    <option>Hunza Luxury Retreat (5 Days)</option>
                    <option>Custom Adventure Trip</option>
                </select>
                <textarea id="notes" rows="4" placeholder="Mention group size, dates, or special requests..."></textarea>
                <button type="submit" class="btn-glow">Book My Journey</button>
            </form>
        </div>

        <div style="height: 400px; border-radius: 40px; overflow: hidden; margin-top: 60px; border: 1px solid var(--border);">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1645.748721644782!2d74.8485292!3d34.9921612!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5db0c66000001%3A0x6d9539b36d07d9f9!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v1700000000000!5m2!1sen!2spk" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg) brightness(0.8);"></iframe>
        </div>

    </div>

    <a href="https://wa.me/923171588489" class="wa-btn" target="_blank">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <nav class="mobile-nav">
        <a href="#" class="active"><i class="fa-solid fa-house-user"></i></a>
        <a href="#book"><i class="fa-solid fa-map-location-dot"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-solid fa-headset"></i></a>
    </nav>

    <footer style="text-align: center; padding: 100px 20px 140px; opacity: 0.3; font-size: 10px; letter-spacing: 3px;">
        © 2026 ASTORE TOURIST HUB | EXPERIENCING THE NORTH
    </footer>

    <script>
        document.getElementById('masterForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tourType').value;
            const m = document.getElementById('notes').value;

            const text = `*NEW TOUR INQUIRY - ASTORE HUB*\n---\n*Explorer:* ${n}\n*WhatsApp:* ${p}\n*Selected Tour:* ${t}\n*Inquiry:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
