<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Gilgit-Baltistan Guide 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;700&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --accent: #00f2ff;
            --deep-blue: #020617;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Plus Jakarta Sans', sans-serif; background: var(--deep-blue); color: #fff; overflow-x: hidden; scroll-behavior: smooth; }

        /* Hero Section with High-End Visuals */
        .hero {
            height: 100vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.5), var(--deep-blue)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=2070&auto=format&fit=crop');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;
        }

        .hero h1 { font-family: 'Syne', sans-serif; font-size: clamp(40px, 10vw, 100px); line-height: 0.9; margin-bottom: 20px; }
        .hero span { color: var(--accent); }

        /* Navigation Dock */
        .dock {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(15, 23, 42, 0.8);
            backdrop-filter: blur(20px); padding: 15px; border-radius: 50px;
            display: flex; justify-content: space-around; border: 1px solid var(--border); z-index: 1000;
        }
        .dock a { color: #fff; text-decoration: none; font-size: 20px; transition: 0.3s; opacity: 0.6; }
        .dock a:hover { color: var(--accent); opacity: 1; transform: translateY(-5px); }

        /* Sections Styling */
        .section { padding: 80px 20px; max-width: 1200px; margin: 0 auto; }
        .section-title { font-family: 'Syne', sans-serif; font-size: 32px; margin-bottom: 40px; text-align: center; }

        /* Destination Grid */
        .gb-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .dest-card {
            height: 400px; border-radius: 30px; overflow: hidden; position: relative;
            border: 1px solid var(--border); transition: 0.5s;
        }
        .dest-card:hover { transform: scale(0.98); border-color: var(--accent); }
        .dest-card img { width: 100%; height: 100%; object-fit: cover; }
        .dest-overlay {
            position: absolute; bottom: 0; width: 100%; padding: 30px;
            background: linear-gradient(transparent, rgba(0,0,0,0.9));
        }

        /* Booking Hub */
        .booking-hub {
            background: var(--glass); border-radius: 40px; padding: 40px;
            border: 1px solid var(--border); display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px;
        }
        input, select, textarea {
            width: 100%; padding: 15px; border-radius: 15px; border: 1px solid var(--border);
            background: rgba(255,255,255,0.05); color: #fff; margin-bottom: 15px; outline: none;
        }
        .btn-main {
            width: 100%; padding: 18px; border-radius: 15px; border: none;
            background: var(--accent); color: #000; font-weight: 800; text-transform: uppercase;
            cursor: pointer; transition: 0.3s;
        }
        .btn-main:hover { box-shadow: 0 0 30px rgba(0, 242, 255, 0.5); }

        /* Modern Quote */
        .quote { text-align: center; padding: 60px 20px; font-size: 22px; font-style: italic; color: #cbd5e1; }

        @media (max-width: 768px) { .hero h1 { font-size: 50px; } }
    </style>
</head>
<body>

    <header class="hero">
        <div style="background: rgba(0,242,255,0.1); padding: 5px 15px; border-radius: 20px; font-size: 10px; color: var(--accent); margin-bottom: 10px; letter-spacing: 2px;">DISCOVER THE NORTH</div>
        <h1>ASTORE<br><span>HUB</span></h1>
        <p style="opacity: 0.6; font-size: 12px; letter-spacing: 5px;">GILGIT-BALTISTAN TOURISM</p>
    </header>

    <div class="quote">
        "Mountains are the beginning and the end of all natural scenery."
    </div>

    <section class="section" id="explore">
        <h2 class="section-title">Explore Gilgit-Baltistan</h2>
        <div class="gb-grid">
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=600" alt="Rama Astore">
                <div class="dest-overlay">
                    <span style="color:var(--accent); font-size:10px;">MAIN HUB</span>
                    <h3>Astore Valley</h3>
                    <p style="font-size:12px; opacity:0.7;">Home to Rama Meadows & Deosai Gate.</p>
                </div>
            </div>
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=600" alt="Hunza">
                <div class="dest-overlay">
                    <h3>Hunza Valley</h3>
                    <p style="font-size:12px; opacity:0.7;">Land of fruit, forts and long life.</p>
                </div>
            </div>
            <div class="dest-card">
                <img src="https://images.unsplash.com/photo-1622324341735-906567087679?q=80&w=600" alt="Skardu">
                <div class="dest-overlay">
                    <h3>Skardu</h3>
                    <p style="font-size:12px; opacity:0.7;">Gateway to K2 and Cold Deserts.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="booking">
        <h2 class="section-title">Plan Your Adventure</h2>
        <div class="booking-hub">
            <div class="form-side">
                <h3 style="margin-bottom:20px;">Book a Service</h3>
                <form id="tourForm">
                    <input type="text" id="name" placeholder="Your Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                    <select id="service">
                        <option>Full GB Tour (7 Days)</option>
                        <option>Astore & Deosai Jeep Safari</option>
                        <option>Hunza Luxury Trip</option>
                        <option>Custom Adventure</option>
                    </select>
                    <textarea rows="4" id="msg" placeholder="Tell us your plan..."></textarea>
                    <button type="submit" class="btn-main">Send WhatsApp Inquiry</button>
                </form>
            </div>
            <div class="info-side" style="display:flex; flex-direction:column; justify-content:center;">
                <div style="background:rgba(255,255,255,0.05); padding:25px; border-radius:20px;">
                    <h4>Quick Guide:</h4>
                    <ul style="font-size:13px; color:#aaa; margin-top:15px; list-style:none;">
                        <li style="margin-bottom:10px;"><i class="fa-solid fa-check" style="color:var(--accent);"></i> Best Time: May to October</li>
                        <li style="margin-bottom:10px;"><i class="fa-solid fa-check" style="color:var(--accent);"></i> Transport: 4x4 recommended for Astore</li>
                        <li style="margin-bottom:10px;"><i class="fa-solid fa-check" style="color:var(--accent);"></i> Stay: Luxury rooms available in Rama</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="contact">
        <div class="gb-grid" style="grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));">
            <div class="glass-panel" style="text-align:center;">
                <i class="fa-brands fa-whatsapp" style="font-size:40px; color:#25d366;"></i>
                <h3 style="margin-top:10px;">0317-1588489</h3>
            </div>
            <div class="glass-panel" style="text-align:center;">
                <i class="fa-brands fa-facebook" style="font-size:40px; color:#1877f2;"></i>
                <h3 style="margin-top:10px;">Astore Hub FB</h3>
            </div>
        </div>
        <div style="margin-top:40px;">
            <iframe src="http://googleusercontent.com/maps.google.com/7" width="100%" height="300" style="border:0; border-radius:30px; filter:grayscale(1) invert(1);"></iframe>
        </div>
    </section>

    <footer style="text-align:center; padding:40px; font-size:10px; opacity:0.4;">
        © 2026 ASTORE TOURIST INFORMATION HUB | BUILT FOR THE NORTH
    </footer>

    <nav class="dock">
        <a href="#"><i class="fa-solid fa-house"></i></a>
        <a href="#explore"><i class="fa-solid fa-mountain"></i></a>
        <a href="#booking"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const s = document.getElementById('service').value;
            const m = document.getElementById('msg').value;
            const text = `*GB ADVENTURE INQUIRY*\n---\n*Explorer:* ${n}\n*WhatsApp:* ${p}\n*Selected Service:* ${s}\n*Details:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
