<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | The Ultimate GB Experience</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --accent: #7000ff;
            --bg: #020617;
            --card-bg: rgba(255, 255, 255, 0.04);
            --border: rgba(255, 255, 255, 0.1);
        }

        /* Base Styles */
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; line-height: 1.6; overflow-x: hidden; }
        a { text-decoration: none; color: inherit; }

        /* Smooth Image Handling */
        img { display: block; width: 100%; height: 100%; object-fit: cover; transition: opacity 0.5s; background: #111; }

        /* Navigation */
        nav.navbar {
            position: fixed; top: 0; width: 100%; padding: 15px 5%;
            background: rgba(2, 6, 23, 0.85); backdrop-filter: blur(15px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 20px; letter-spacing: -1px; }
        .logo span { color: var(--primary); }

        /* Hero Section */
        .hero {
            height: 85vh; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.5), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1600&auto=format') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(40px, 12vw, 100px); line-height: 0.9; margin-bottom: 15px; }
        .hero p { font-size: 12px; letter-spacing: 5px; text-transform: uppercase; color: var(--primary); opacity: 0.8; }

        /* Container */
        .container { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }
        .section-header { margin-bottom: 40px; text-align: left; }
        .section-header h2 { font-family: 'Syne'; font-size: 32px; border-left: 4px solid var(--primary); padding-left: 15px; }

        /* Grid System */
        .main-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        
        /* Modern Cards */
        .tour-card {
            background: var(--card-bg); border-radius: 24px; overflow: hidden;
            border: 1px solid var(--border); transition: 0.4s; position: relative;
        }
        .tour-card:hover { transform: translateY(-10px); border-color: var(--primary); }
        .image-container { height: 250px; position: relative; }
        
        .card-info { padding: 20px; }
        .card-info h3 { font-size: 20px; margin-bottom: 10px; font-family: 'Syne'; }
        .card-info p { font-size: 14px; color: #9ca3af; }

        /* Info Features */
        .essentials {
            background: linear-gradient(135deg, rgba(112,0,255,0.05), rgba(0,242,255,0.05));
            border-radius: 30px; padding: 30px; border: 1px solid var(--border); margin: 40px 0;
        }
        .essentials-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 15px; margin-top: 20px; }
        .ess-item { background: rgba(0,0,0,0.3); padding: 15px; border-radius: 15px; text-align: center; font-size: 12px; }
        .ess-item i { font-size: 24px; color: var(--primary); margin-bottom: 10px; display: block; }

        /* Booking Form */
        .form-box { background: var(--card-bg); border-radius: 30px; padding: 30px; border: 1px solid var(--border); }
        input, select, textarea {
            width: 100%; padding: 16px; margin-bottom: 15px; border-radius: 12px;
            border: 1px solid var(--border); background: #000; color: #fff; outline: none;
        }
        .btn-send {
            width: 100%; padding: 18px; background: var(--primary); color: #000;
            border: none; border-radius: 12px; font-weight: 800; cursor: pointer; text-transform: uppercase;
        }

        /* Mobile Bottom Nav */
        .bottom-nav {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(20px); border-radius: 100px; padding: 12px 25px;
            display: flex; justify-content: space-between; border: 1px solid var(--border); z-index: 1000;
        }
        .bottom-nav a { color: #fff; opacity: 0.5; font-size: 20px; transition: 0.3s; }
        .bottom-nav a.active { color: var(--primary); opacity: 1; }

        /* Maps Inversion */
        .map-box { border-radius: 24px; overflow: hidden; height: 350px; margin-top: 40px; border: 1px solid var(--border); }
        .map-box iframe { filter: invert(90%) hue-rotate(180deg); }

        @media (max-width: 768px) {
            .hero { height: 70vh; }
            .section-header h2 { font-size: 26px; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">ASTORE<span>HUB</span></div>
        <div style="font-size: 10px; opacity: 0.6; font-weight: 700;">G-B OFFICIAL 2026</div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Welcome to the Heaven</p>
            <h1>PEAKS &<br><span>BEYOND</span></h1>
            <div style="display:flex; gap:10px; justify-content:center; margin-top:20px;">
                <span style="font-size: 11px; background: rgba(0,242,255,0.1); padding: 5px 15px; border-radius: 20px; color: var(--primary);">Astore: 12°C</span>
                <span style="font-size: 11px; background: rgba(255,255,255,0.05); padding: 5px 15px; border-radius: 20px;">Hunza: 16°C</span>
            </div>
        </div>
    </section>

    <div class="container">
        
        <div class="section-header">
            <h2>Explore Destinations</h2>
        </div>

        <div class="main-grid">
            <div class="tour-card">
                <div class="image-container">
                    <img src="https://picsum.photos/seed/astore6/800/600" onerror="this.src='https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800'" alt="Astore">
                </div>
                <div class="card-info">
                    <h3>Rama Meadows</h3>
                    <p>The lush green heart of Astore valley. Perfect for nature lovers.</p>
                </div>
            </div>

            <div class="tour-card">
                <div class="image-container">
                    <img src="https://picsum.photos/seed/hunza9/800/600" onerror="this.src='https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800'" alt="Hunza">
                </div>
                <div class="card-info">
                    <h3>Hunza Valley</h3>
                    <p>The cultural hub with ancient forts and the stunning Attabad Lake.</p>
                </div>
            </div>

            <div class="tour-card">
                <div class="image-container">
                    <img src="https://picsum.photos/seed/deosai2/800/600" onerror="this.src='https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800'" alt="Deosai">
                </div>
                <div class="card-info">
                    <h3>Deosai Plains</h3>
                    <p>Second highest plateau in the world, home to the brown bear.</p>
                </div>
            </div>
        </div>

        <div class="essentials">
            <h3 style="font-family: 'Syne';">Travel Essentials</h3>
            <p style="font-size: 13px; opacity: 0.7;">Make sure you have these before traveling.</p>
            <div class="essentials-grid">
                <div class="ess-item"><i class="fa-solid fa-sim-card"></i> SCOM Sim</div>
                <div class="ess-item"><i class="fa-solid fa-shirt"></i> Warm Cloths</div>
                <div class="ess-item"><i class="fa-solid fa-id-card"></i> Original CNIC</div>
                <div class="ess-item"><i class="fa-solid fa-money-bill-wave"></i> Cash Only</div>
            </div>
        </div>

        <div class="section-header" id="book">
            <h2>Plan Your Trip</h2>
        </div>

        <div class="form-box">
            <form id="tourForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px;">
                    <input type="text" id="name" placeholder="Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>Astore & Deosai Trip</option>
                    <option>Hunza & Nagar Trip</option>
                    <option>Skardu Adventure</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Message (Group size, Dates)"></textarea>
                <button type="submit" class="btn-send">Send Inquiry to Hub</button>
            </form>
        </div>

        <div class="map-box">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d104524.34145616654!2d74.78168249726563!3d35.33481230000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5df988950d73d%3A0xc07f60756a147814!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v171588489!5m2!1sen!2spk" width="100%" height="100%" frameborder="0"></iframe>
        </div>

    </div>

    <footer style="text-align:center; padding: 60px 20px; opacity: 0.3; font-size: 10px; letter-spacing: 2px;">
        © 2026 ASTORE TOURIST HUB | GILGIT-BALTISTAN
    </footer>

    <nav class="bottom-nav">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-compass"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank"><i class="fa-brands fa-facebook"></i></a>
    </nav>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `*HUB TOUR INQUIRY*\n---\n*Name:* ${n}\n*WhatsApp:* ${p}\n*Trip:* ${t}\n*Note:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
