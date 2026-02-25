<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Gilgit-Baltistan Digital Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #7000ff;
            --bg: #050505;
            --card-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Plus Jakarta Sans', sans-serif; background: var(--bg); color: #fff; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- MODERN FEATURES --- */
        
        /* 1. Animated Background Glow */
        .glow-bg {
            position: fixed; width: 300px; height: 300px; background: var(--primary);
            filter: blur(150px); opacity: 0.1; z-index: -1; border-radius: 50%;
            animation: move 20s infinite alternate;
        }
        @keyframes move { from { top: 0; left: 0; } to { bottom: 0; right: 0; } }

        /* 2. Luxury Hero Section */
        .hero {
            height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.7), var(--bg)), 
                        url('https://picsum.photos/1920/1080?mountain') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne', sans-serif; font-size: clamp(40px, 10vw, 100px); letter-spacing: -2px; line-height: 0.9; }
        .hero h1 span { color: var(--primary); text-shadow: 0 0 20px rgba(0,242,255,0.4); }
        .hero-badge { background: var(--glass-border); padding: 8px 20px; border-radius: 50px; font-size: 10px; letter-spacing: 4px; margin-bottom: 20px; }

        /* 3. Modern Destination Cards */
        .container { max-width: 1200px; margin: 0 auto; padding: 60px 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        
        .card {
            background: var(--card-bg); border: 1px solid var(--glass-border); border-radius: 30px;
            overflow: hidden; backdrop-filter: blur(10px); transition: 0.4s;
        }
        .card:hover { transform: translateY(-10px); border-color: var(--primary); box-shadow: 0 10px 40px rgba(0,242,255,0.1); }
        
        /* Modern Photos Loader */
        .card-img { width: 100%; height: 250px; background: #111; position: relative; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }

        .card-body { padding: 30px; }
        .card-body h3 { font-family: 'Syne', sans-serif; margin-bottom: 10px; color: var(--primary); }
        .card-body p { font-size: 14px; opacity: 0.7; line-height: 1.6; }

        /* 4. GB Quick Guide Section */
        .guide-box {
            background: linear-gradient(135deg, rgba(112,0,255,0.1), rgba(0,242,255,0.1));
            border-radius: 40px; padding: 50px; border: 1px solid var(--glass-border); margin: 50px 0;
        }

        /* 5. Mobile-Ready Booking Form */
        .form-section { background: var(--card-bg); border-radius: 40px; padding: 40px; border: 1px solid var(--glass-border); }
        .input-group { margin-bottom: 20px; }
        input, select, textarea {
            width: 100%; padding: 18px; background: rgba(0,0,0,0.4); border: 1px solid var(--glass-border);
            border-radius: 15px; color: #fff; font-size: 15px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); box-shadow: 0 0 15px rgba(0,242,255,0.2); }
        .btn-premium {
            width: 100%; padding: 20px; border-radius: 15px; border: none;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: #fff; font-weight: 800; text-transform: uppercase; letter-spacing: 2px;
            cursor: pointer; transition: 0.4s;
        }
        .btn-premium:hover { letter-spacing: 4px; box-shadow: 0 10px 30px rgba(0,242,255,0.4); }

        /* 6. Desktop & Mobile Easy Dock */
        .dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 450px; background: rgba(10,10,10,0.8);
            backdrop-filter: blur(20px); border-radius: 100px; padding: 15px 30px;
            border: 1px solid var(--glass-border); display: flex; justify-content: space-between; z-index: 9999;
        }
        .dock a { color: #fff; opacity: 0.5; font-size: 20px; transition: 0.3s; }
        .dock a:hover { color: var(--primary); opacity: 1; transform: translateY(-5px); }

        /* Map */
        .map-ui { border-radius: 30px; overflow: hidden; border: 1px solid var(--glass-border); margin-top: 50px; }
        .map-ui iframe { width: 100%; height: 350px; filter: invert(90%) hue-rotate(180deg); }

        @media (max-width: 768px) {
            .hero h1 { font-size: 50px; }
            .guide-box { padding: 30px; }
        }
    </style>
</head>
<body>

    <div class="glow-bg"></div>

    <section class="hero">
        <div class="hero-badge">OFFICIAL TOURISM HUB • 2026</div>
        <h1>ASTORE<br><span>VALLEY</span></h1>
        <p style="margin-top: 20px;">The Gateway to Gilgit-Baltistan</p>
    </section>

    <div class="container">
        
        <h2 style="font-family:'Syne'; font-size:32px; margin-bottom:40px; text-align:center;">Ultimate <span>Guide</span></h2>
        
        <div class="grid">
            <div class="card">
                <div class="card-img">
                    <img src="https://picsum.photos/seed/astore/800/600" alt="Astore">
                </div>
                <div class="card-body">
                    <h3>Astore Valley</h3>
                    <p>Known for Nanga Parbat views, Rama Meadows, and historical routes. It's the quietest paradise in GB.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-img">
                    <img src="https://picsum.photos/seed/hunza/800/600" alt="Hunza">
                </div>
                <div class="card-body">
                    <h3>Hunza Valley</h3>
                    <p>The land of longevity. Famous for Attabad Lake, Passu Cones, and the hospitality of its people.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-img">
                    <img src="https://picsum.photos/seed/skardu/800/600" alt="Skardu">
                </div>
                <div class="card-body">
                    <h3>Skardu City</h3>
                    <p>The hub of Baltistan. Gateway to K2 and home to the mesmerizing Cold Desert and Shangrila Lake.</p>
                </div>
            </div>
        </div>

        <div class="guide-box">
            <h2 style="font-family:'Syne'; margin-bottom:20px;">Why Visit <span>Gilgit Baltistan?</span></h2>
            <p style="opacity:0.8; font-size:15px; margin-bottom:30px;">
                GB is home to 5 of the 14 highest peaks in the world. From the world's second-highest plateau (Deosai) 
                to ancient Silk Road forts, this region offers everything. 
                <br><br>
                <b>Travel Tips:</b> Always carry an SCOM sim, keep local currency (Cash), and book a 4x4 Jeep for Astore/Deosai.
            </p>
            <div style="display:flex; gap:20px; flex-wrap:wrap;">
                <div style="background:rgba(255,255,255,0.05); padding:15px; border-radius:15px; flex:1; min-width:150px;">
                    <i class="fa-solid fa-cloud-sun" style="color:var(--primary);"></i>
                    <h4 style="margin-top:10px;">Weather</h4>
                    <p style="font-size:12px; opacity:0.6;">Best: May - Oct</p>
                </div>
                <div style="background:rgba(255,255,255,0.05); padding:15px; border-radius:15px; flex:1; min-width:150px;">
                    <i class="fa-solid fa-car" style="color:var(--primary);"></i>
                    <h4 style="margin-top:10px;">Roads</h4>
                    <p style="font-size:12px; opacity:0.6;">KKH is Excellent</p>
                </div>
            </div>
        </div>

        <div class="form-section" id="book">
            <h2 style="font-family:'Syne'; text-align:center; margin-bottom:30px;">Plan Your <span>Adventure</span></h2>
            <form id="waForm">
                <div class="input-group">
                    <input type="text" id="name" placeholder="Your Full Name" required>
                </div>
                <div class="input-group">
                    <input type="tel" id="phone" placeholder="WhatsApp Number (+92...)" required>
                </div>
                <div class="input-group">
                    <select id="dest">
                        <option>Astore & Deosai Safari</option>
                        <option>Full GB Luxury Package</option>
                        <option>Hunza Valley Trip</option>
                        <option>Skardu Adventure</option>
                    </select>
                </div>
                <div class="input-group">
                    <textarea id="msg" rows="4" placeholder="Any special notes or travel dates?"></textarea>
                </div>
                <button type="submit" class="btn-premium">Connect to Hub via WhatsApp</button>
            </form>
        </div>

        <div class="map-ui">
            <iframe src="http://googleusercontent.com/maps.google.com/7"></iframe>
        </div>

    </div>

    <footer style="text-align:center; padding:60px 20px; opacity:0.3; font-size:11px; letter-spacing:2px;">
        © 2026 ASTORE TOURIST HUB | EXPERIENCING THE NORTH
    </footer>

    <nav class="dock">
        <a href="#" title="Home"><i class="fa-solid fa-house-chimney"></i></a>
        <a href="#book" title="Guide"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#book" title="Book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank" title="WhatsApp"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank" title="Facebook"><i class="fa-brands fa-facebook-f"></i></a>
    </nav>

    <script>
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const d = document.getElementById('dest').value;
            const m = document.getElementById('msg').value;

            const text = `*GB HUB - NEW TOUR INQUIRY*\n---\n*Name:* ${n}\n*WhatsApp:* ${p}\n*Destination:* ${d}\n*Message:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>

</body>
</html>
