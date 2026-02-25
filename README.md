<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GB Ultimate Hub | Explore the North</title>
    <link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@400;700&family=Outfit:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00d2ff;
            --accent: #3a7bd5;
            --dark: #020817;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Outfit', sans-serif; background: var(--dark); color: #fff; scroll-behavior: smooth; }

        /* Smooth Hero Section */
        .hero {
            height: 100vh; width: 100%; position: relative;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.4), var(--dark)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=2070&auto=format&fit=crop');
            background-size: cover; background-position: center; text-align: center; padding: 20px;
        }

        .hero h1 {
            font-family: 'Unbounded', sans-serif; font-size: clamp(35px, 8vw, 80px);
            text-transform: uppercase; line-height: 1; margin-bottom: 15px;
            background: linear-gradient(to right, #fff, var(--primary));
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
        }

        .hero p { font-size: 14px; letter-spacing: 5px; color: var(--primary); font-weight: 300; }

        /* GB Destinations Explorer */
        .section-title { padding: 40px 20px 20px; text-align: center; font-family: 'Unbounded'; font-size: 20px; }
        
        .dest-slider {
            display: flex; overflow-x: auto; gap: 20px; padding: 20px;
            scrollbar-width: none; -ms-overflow-style: none;
        }
        .dest-slider::-webkit-scrollbar { display: none; }

        .dest-card {
            min-width: 280px; height: 380px; background: var(--glass);
            border-radius: 30px; border: 1px solid var(--border); overflow: hidden;
            position: relative; transition: 0.5s; flex-shrink: 0;
        }
        .dest-card:hover { border-color: var(--primary); transform: translateY(-10px); }
        .dest-card img { width: 100%; height: 100%; object-fit: cover; opacity: 0.6; }
        .dest-info { position: absolute; bottom: 20px; left: 20px; right: 20px; }
        .dest-info h3 { font-family: 'Unbounded'; font-size: 16px; margin-bottom: 5px; }

        /* Quote Section */
        .quote-box {
            background: var(--glass); margin: 40px 20px; padding: 40px; border-radius: 30px;
            text-align: center; border-left: 5px solid var(--primary);
        }
        .quote-box blockquote { font-style: italic; font-size: 18px; color: #ddd; }
        .quote-box cite { display: block; margin-top: 15px; font-size: 12px; color: var(--primary); letter-spacing: 2px; }

        /* Integrated Form Hub */
        .form-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; padding: 20px; }
        
        .glass-form {
            background: var(--glass); backdrop-filter: blur(15px); padding: 30px;
            border-radius: 30px; border: 1px solid var(--border);
        }

        input, select, textarea {
            width: 100%; background: rgba(255,255,255,0.05); border: 1px solid var(--border);
            padding: 15px; border-radius: 15px; color: #fff; margin-bottom: 15px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); background: rgba(255,255,255,0.1); }

        .book-btn {
            width: 100%; padding: 18px; border-radius: 15px; border: none;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: #000; font-weight: 700; text-transform: uppercase; cursor: pointer; transition: 0.4s;
        }
        .book-btn:hover { box-shadow: 0 0 30px rgba(0, 210, 255, 0.4); transform: translateY(-3px); }

        /* Information Grid */
        .info-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; padding: 20px; }
        .info-item { background: var(--glass); padding: 20px; border-radius: 20px; text-align: center; border: 1px solid var(--border); }
        .info-item i { font-size: 30px; color: var(--primary); margin-bottom: 10px; }

        /* Mobile Responsive Bottom Dock */
        .dock {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 450px; background: rgba(2, 8, 23, 0.9);
            backdrop-filter: blur(20px); padding: 15px 30px; border-radius: 100px;
            border: 1px solid var(--border); display: flex; justify-content: space-between; z-index: 1000;
        }
        .dock a { color: #fff; opacity: 0.6; text-decoration: none; font-size: 20px; transition: 0.3s; }
        .dock a:hover { color: var(--primary); opacity: 1; transform: translateY(-5px); }

        /* Activity Log */
        .activity { padding: 20px; text-align: center; font-size: 11px; color: #666; }
    </style>
</head>
<body>

    <header class="hero">
        <p>WELCOME TO THE HIGHLANDS</p>
        <h1>GILGIT<br>BALTISTAN</h1>
        <div style="margin-top: 20px; padding: 10px 25px; border: 1px solid #fff; border-radius: 50px; font-size: 10px;">
            ASTORE INFORMATION HUB • 2026
        </div>
    </header>

    <div class="info-grid">
        <div class="info-item"><i class="fa-solid fa-cloud-sun"></i><h4>Weather</h4><p style="font-size:12px;">Plan around seasons</p></div>
        <div class="info-item"><i class="fa-solid fa-route"></i><h4>Roads</h4><p style="font-size:12px;">KKH & Local Routes</p></div>
        <div class="info-item"><i class="fa-solid fa-person-hiking"></i><h4>Trek</h4><p style="font-size:12px;">Deosai to Fairy Meadows</p></div>
    </div>

    <h2 class="section-title">TOP DESTINATIONS</h2>
    <div class="dest-slider">
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?w=400" alt="Rama">
            <div class="dest-info"><h3>Rama Meadows</h3><p style="font-size:11px;">Green Paradise in Astore</p></div>
        </div>
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?w=400" alt="Deosai">
            <div class="dest-info"><h3>Deosai Plains</h3><p style="font-size:11px;">Roof of the World</p></div>
        </div>
        <div class="dest-card">
            <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?w=400" alt="Hunza">
            <div class="dest-info"><h3>Hunza Valley</h3><p style="font-size:11px;">Ancient Forts & Culture</p></div>
        </div>
    </div>

    <div class="quote-box">
        <i class="fa-solid fa-quote-left" style="color:var(--primary); font-size:30px; margin-bottom:15px;"></i>
        <blockquote>"Gilgit Baltistan is not just a place, it's a feeling of being closer to the heavens."</blockquote>
        <cite>— LOCAL EXPLORERS GUILD</cite>
    </div>

    <h2 class="section-title">SERVICE BOOKINGS</h2>
    <div class="form-container">
        <div class="glass-form" id="booking">
            <h3 style="margin-bottom:20px; font-family:'Unbounded'; font-size:14px;">BOOK ROOM/TRIP</h3>
            <form id="tourForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="type">
                    <option>Standard Astore Package</option>
                    <option>Luxury GB Full Tour</option>
                    <option>Deosai Jeep Safari</option>
                </select>
                <textarea rows="3" id="msg" placeholder="Any Special Requests?"></textarea>
                <button type="submit" class="book-btn">SEND TO WHATSAPP</button>
            </form>
        </div>

        <div class="glass-form">
            <h3 style="margin-bottom:20px; font-family:'Unbounded'; font-size:14px;">LIVE GUIDANCE</h3>
            <div style="text-align:center;">
                <p style="font-size:12px; color:#aaa; margin-bottom:20px;">Need instant info about roads, weather, or hotels?</p>
                <a href="https://wa.me/923171588489" target="_blank" class="book-btn" style="text-decoration:none; display:block; background:#25d366; color:#fff;">
                    <i class="fa-brands fa-whatsapp"></i> CHAT WITH HUB
                </a>
            </div>
        </div>
    </div>

    <div style="padding:20px;">
        <iframe src="http://googleusercontent.com/maps.google.com/6" width="100%" height="300" style="border:0; border-radius:30px; filter:grayscale(1) invert(1);"></iframe>
    </div>

    <div class="activity" id="status">Active & Connected to GB Satellite Hub</div>

    <nav class="dock">
        <a href="#" onclick="window.scrollTo(0,0)"><i class="fa-solid fa-house"></i></a>
        <a href="#booking"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank"><i class="fa-brands fa-facebook"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-solid fa-headset"></i></a>
    </nav>

    <script>
        const WHATSAPP_HUB = "923171588489";

        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('type').value;
            const m = document.getElementById('msg').value;

            const text = `*NEW EXPLORER INQUIRY*\n---\n*Name:* ${n}\n*Phone:* ${p}\n*Package:* ${t}\n*Request:* ${m}`;
            window.open(`https://wa.me/${WHATSAPP_HUB}?text=${encodeURIComponent(text)}`, '_blank');
            
            document.getElementById('status').innerText = "Last message sent to Hub successfully!";
            this.reset();
        };

        // Scroll animations (simple fade)
        window.addEventListener('scroll', () => {
            const forms = document.querySelectorAll('.glass-form');
            forms.forEach(f => {
                const top = f.getBoundingClientRect().top;
                if(top < window.innerHeight - 100) f.style.opacity = "1";
            });
        });
    </script>
</body>
</html>
