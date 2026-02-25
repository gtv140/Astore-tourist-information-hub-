<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Complete Gilgit-Baltistan Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --neon: #00f2ff;
            --deep: #020617;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; }
        body { background: var(--deep); color: #fff; line-height: 1.6; overflow-x: hidden; scroll-behavior: smooth; }

        /* Modern Hero with Parallax */
        .hero {
            height: 100vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.6), var(--deep)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&fit=crop&w=1920&q=80');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 20px;
        }

        .hero h1 { font-family: 'Syne', sans-serif; font-size: clamp(40px, 8vw, 90px); line-height: 0.9; margin-bottom: 20px; }
        .hero span { color: var(--neon); text-shadow: 0 0 20px rgba(0, 242, 255, 0.5); }
        .hero p { font-size: 14px; letter-spacing: 5px; text-transform: uppercase; opacity: 0.8; }

        /* Info Section Styling */
        .container { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }
        .section-title { font-family: 'Syne', sans-serif; font-size: clamp(24px, 5vw, 40px); margin-bottom: 40px; text-align: center; }
        .section-title span { color: var(--neon); }

        /* Destinations Grid */
        .guide-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; margin-bottom: 60px; }
        .guide-card {
            background: var(--glass); border: 1px solid var(--border); border-radius: 30px; overflow: hidden;
            transition: 0.4s; position: relative;
        }
        .guide-card:hover { transform: translateY(-10px); border-color: var(--neon); }
        .guide-card img { width: 100%; height: 250px; object-fit: cover; }
        .card-content { padding: 25px; }
        .card-content h3 { margin-bottom: 10px; color: var(--neon); }
        .card-content p { font-size: 14px; color: #ccc; margin-bottom: 15px; }
        .tag { background: rgba(0, 242, 255, 0.1); color: var(--neon); padding: 4px 12px; border-radius: 50px; font-size: 10px; font-weight: 700; text-transform: uppercase; }

        /* Special Tips Area */
        .tips-box { background: linear-gradient(135deg, rgba(0, 242, 255, 0.1) 0%, transparent 100%); border-radius: 30px; padding: 40px; border: 1px solid var(--border); margin: 40px 0; }
        .tips-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 20px; }
        .tip-item { background: rgba(255,255,255,0.02); padding: 20px; border-radius: 20px; text-align: center; }
        .tip-item i { font-size: 30px; color: var(--neon); margin-bottom: 15px; }

        /* WhatsApp Floating Form */
        .form-container { background: var(--glass); border-radius: 40px; border: 1px solid var(--border); padding: 40px; margin-top: 40px; }
        input, select, textarea { width: 100%; padding: 18px; border-radius: 20px; border: 1px solid var(--border); background: rgba(0,0,0,0.3); color: #fff; margin-bottom: 15px; outline: none; transition: 0.3s; }
        input:focus { border-color: var(--neon); }
        .btn-send { width: 100%; padding: 20px; border-radius: 20px; border: none; background: var(--neon); color: #000; font-weight: 800; text-transform: uppercase; letter-spacing: 2px; cursor: pointer; transition: 0.3s; }
        .btn-send:hover { box-shadow: 0 0 30px rgba(0, 242, 255, 0.4); transform: scale(1.02); }

        /* Dock Navigation */
        .dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 450px; background: rgba(2, 6, 23, 0.8); backdrop-filter: blur(20px);
            padding: 15px 30px; border-radius: 100px; border: 1px solid var(--border);
            display: flex; justify-content: space-between; z-index: 1000;
        }
        .dock a { color: #fff; opacity: 0.6; text-decoration: none; font-size: 20px; transition: 0.3s; }
        .dock a:hover { color: var(--neon); opacity: 1; transform: translateY(-5px); }

        /* Map UI */
        .map-box { border-radius: 40px; overflow: hidden; border: 1px solid var(--border); margin-top: 40px; }
        .map-box iframe { width: 100%; height: 400px; filter: invert(90%) hue-rotate(180deg); }

        @media (max-width: 768px) { .hero h1 { font-size: 45px; } .dock { padding: 15px 20px; } }
    </style>
</head>
<body>

    <header class="hero">
        <p>Your Adventure Starts Here</p>
        <h1>ASTORE<span>HUB</span></h1>
        <div style="border: 1px solid var(--neon); padding: 5px 20px; border-radius: 50px; font-size: 11px; color: var(--neon); margin-top: 20px;">
            GILGIT-BALTISTAN GUIDE 2026
        </div>
    </header>

    <div class="container">
        <h2 class="section-title">Explore <span>The Wonders</span></h2>
        
        <div class="guide-grid">
            <div class="guide-card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=800&q=80" alt="Astore">
                <div class="card-content">
                    <span class="tag">The Main Hub</span>
                    <h3>Astore Valley</h3>
                    <p>Astore is the gateway to Nanga Parbat. Must visit: Rama Meadows, Rama Lake, and the hidden Minimarg (via permission).</p>
                    <a href="#book" style="color:var(--neon); text-decoration:none; font-size:12px; font-weight:800;">RESERVE JEEP →</a>
                </div>
            </div>

            <div class="guide-card">
                <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&fit=crop&w=800&q=80" alt="Deosai">
                <div class="card-content">
                    <span class="tag">The High Plateau</span>
                    <h3>Deosai Plains</h3>
                    <p>The "Roof of the World". Located between Skardu and Astore. Famous for Himalayan Brown Bears and Sheosar Lake.</p>
                </div>
            </div>

            <div class="guide-card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?auto=format&fit=crop&w=800&q=80" alt="Hunza">
                <div class="card-content">
                    <span class="tag">Culture & Peaks</span>
                    <h3>Hunza Valley</h3>
                    <p>Famous for Attabad Lake, Altit/Baltit Forts, and Rakaposhi View. The most tourist-friendly spot in GB.</p>
                </div>
            </div>

            <div class="guide-card">
                <img src="https://images.unsplash.com/photo-1622324341735-906567087679?auto=format&fit=crop&w=800&q=80" alt="Skardu">
                <div class="card-content">
                    <span class="tag">Cold Desert</span>
                    <h3>Skardu City</h3>
                    <p>Gateway to K2. Visit Lower Kachura (Shangrila), Upper Kachura, and the Katpana Cold Desert.</p>
                </div>
            </div>
        </div>

        <div class="tips-box">
            <h2 style="font-family:'Syne';">Pro Travel <span>Tips</span></h2>
            <div class="tips-grid">
                <div class="tip-item">
                    <i class="fa-solid fa-sim-card"></i>
                    <h4>Network</h4>
                    <p style="font-size:12px; opacity:0.7;">Buy an **SCOM SIM**. Others (Telenor/Zong) mostly don't work in Astore/Deosai.</p>
                </div>
                <div class="tip-item">
                    <i class="fa-solid fa-car"></i>
                    <h4>Transport</h4>
                    <p style="font-size:12px; opacity:0.7;">For Astore and Deosai, only use **4x4 Jeeps**. Sedans are not recommended.</p>
                </div>
                <div class="tip-item">
                    <i class="fa-solid fa-wallet"></i>
                    <h4>Cash</h4>
                    <p style="font-size:12px; opacity:0.7;">Keep enough **Cash**. ATMs are very rare outside Gilgit, Skardu, and Hunza.</p>
                </div>
            </div>
        </div>

        <div class="form-container" id="book">
            <h2 class="section-title">Plan Your <span>Tour</span></h2>
            <form id="waForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap:20px;">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>Astore & Deosai Safari (Best)</option>
                    <option>Hunza & Nagar Cultural Tour</option>
                    <option>Skardu & Khaplu Adventure</option>
                    <option>Fairy Meadows Expedition</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Mention group size, dates, or custom requirements..."></textarea>
                <button type="submit" class="btn-send">Send Inquiry to Hub</button>
            </form>
        </div>

        <div class="map-box">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d105263.951004313!2d74.76757041477123!3d35.33333333!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e60f084f7b6051%3A0x6b04f7b7f7f3484c!2sAstore!5e0!3m2!1sen!2spk!4v1700000000000"></iframe>
        </div>
    </div>

    <div style="text-align:center; padding: 60px 20px;">
        <div style="display:flex; justify-content:center; gap:40px; margin-bottom:20px;">
            <a href="https://wa.me/923171588489" style="color:#25d366; font-size:40px;"><i class="fa-brands fa-whatsapp"></i></a>
            <a href="https://www.facebook.com/share/1BoG9YCsZN/" style="color:#1877f2; font-size:40px;"><i class="fa-brands fa-facebook"></i></a>
        </div>
        <p style="font-size:10px; opacity:0.3; text-transform:uppercase; letter-spacing:2px;">© 2026 Astore Tourist Hub | Powered by Passion</p>
    </div>

    <nav class="dock">
        <a href="#" title="Home"><i class="fa-solid fa-house-chimney"></i></a>
        <a href="#book" title="Book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank" title="Contact"><i class="fa-solid fa-comments"></i></a>
        <a href="#book" title="Guide"><i class="fa-solid fa-map-location-dot"></i></a>
    </nav>

    <script>
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `*NEW TOUR INQUIRY FROM HUB*\n---\n*Explorer:* ${n}\n*WhatsApp:* ${p}\n*Tour:* ${t}\n*Request:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };

        // Smooth Appearance on Scroll
        window.addEventListener('scroll', () => {
            const cards = document.querySelectorAll('.guide-card');
            cards.forEach(card => {
                const top = card.getBoundingClientRect().top;
                if(top < window.innerHeight - 100) card.style.opacity = "1";
            });
        });
    </script>
</body>
</html>
