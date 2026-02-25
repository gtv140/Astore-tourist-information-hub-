<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Official GB Travel Guide</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --bg: #020617;
            --card-bg: rgba(255, 255, 255, 0.05);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; scroll-behavior: smooth; }

        /* Navigation */
        nav {
            position: fixed; top: 0; width: 100%; padding: 15px 5%;
            background: rgba(2, 6, 23, 0.9); backdrop-filter: blur(15px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 20px; font-weight: 800; color: #fff; }
        .logo span { color: var(--primary); }

        /* Hero Section */
        .hero {
            height: 70vh; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1600&auto=format') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(35px, 10vw, 80px); line-height: 1; margin-bottom: 10px; }
        .hero p { font-size: 12px; letter-spacing: 4px; color: var(--primary); text-transform: uppercase; }

        /* Main Content Container */
        .container { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }
        .section-title { font-family: 'Syne'; font-size: 28px; margin-bottom: 30px; border-left: 4px solid var(--primary); padding-left: 15px; }

        /* Grid for Destinations */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        
        .card {
            background: var(--card-bg); border-radius: 20px; overflow: hidden;
            border: 1px solid var(--border); transition: 0.3s;
        }
        .card:hover { border-color: var(--primary); transform: translateY(-5px); }
        .card-img { height: 230px; width: 100%; overflow: hidden; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }
        
        .card-info { padding: 20px; }
        .card-info h3 { font-family: 'Syne'; font-size: 20px; margin-bottom: 8px; color: var(--primary); }
        .card-info p { font-size: 14px; opacity: 0.8; line-height: 1.5; }

        /* Travel Essentials (Mobile Friendly) */
        .essentials {
            background: rgba(0, 242, 255, 0.05); border-radius: 25px; padding: 25px;
            margin: 40px 0; border: 1px dashed var(--border);
        }
        .ess-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; margin-top: 15px; }
        .ess-item { background: rgba(0,0,0,0.2); padding: 12px; border-radius: 12px; font-size: 12px; display: flex; align-items: center; gap: 8px; }
        .ess-item i { color: var(--primary); }

        /* Booking Form */
        .booking-box { background: var(--card-bg); border-radius: 25px; padding: 30px; border: 1px solid var(--border); }
        input, select, textarea {
            width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px;
            border: 1px solid var(--border); background: #000; color: #fff; font-size: 16px; outline: none;
        }
        input:focus { border-color: var(--primary); }
        .btn-submit {
            width: 100%; padding: 18px; background: var(--primary); color: #000;
            border: none; border-radius: 12px; font-weight: 800; text-transform: uppercase; cursor: pointer;
        }

        /* Floating WhatsApp */
        .wa-float {
            position: fixed; bottom: 90px; right: 20px; background: #25d366;
            width: 55px; height: 55px; border-radius: 50%; display: flex;
            align-items: center; justify-content: center; font-size: 25px; color: #fff;
            z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.4);
        }

        /* Bottom Nav Dock */
        .dock {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 15px;
            border-top: 1px solid var(--border); z-index: 1000;
        }
        .dock a { color: #fff; opacity: 0.5; font-size: 20px; }
        .dock a.active { color: var(--primary); opacity: 1; }

        @media (max-width: 600px) {
            .hero h1 { font-size: 40px; }
            .section-title { font-size: 22px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div style="font-size: 10px; opacity: 0.5; font-weight: 700;">GB GUIDE 2026</div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Welcome to Gilgit Baltistan</p>
            <h1>PEAKS &<br><span>PARADISE</span></h1>
        </div>
    </section>

    <div class="container">
        
        <h2 class="section-title">Destinations</h2>
        <div class="grid">
            <div class="card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800" alt="Astore Valley">
                </div>
                <div class="card-info">
                    <h3>Astore Valley</h3>
                    <p>Gateway to Nanga Parbat and home to the beautiful Rama Meadows.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800" alt="Hunza Valley">
                </div>
                <div class="card-info">
                    <h3>Hunza Valley</h3>
                    <p>Historical forts, Attabad lake, and the kindest people of the north.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1622324341735-906567087679?q=80&w=800" alt="Skardu City">
                </div>
                <div class="card-info">
                    <h3>Skardu & Deosai</h3>
                    <p>Explore the cold deserts and the world's second highest plateau.</p>
                </div>
            </div>
        </div>

        <div class="essentials">
            <h3 style="font-family: 'Syne'; font-size: 18px;">Travel Essentials</h3>
            <div class="ess-grid">
                <div class="ess-item"><i class="fa-solid fa-check-circle"></i> SCOM Sim Card</div>
                <div class="ess-item"><i class="fa-solid fa-check-circle"></i> Warm Clothes</div>
                <div class="ess-item"><i class="fa-solid fa-check-circle"></i> Original CNIC</div>
                <div class="ess-item"><i class="fa-solid fa-check-circle"></i> Cash (No ATMs)</div>
            </div>
        </div>

        <h2 class="section-title" id="book">Plan Your Trip</h2>
        <div class="booking-box">
            <form id="waForm">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Trip</option>
                    <option>Hunza & Nagar Trip</option>
                    <option>Skardu Adventure</option>
                </select>
                <textarea id="msg" rows="3" placeholder="Travel dates or Group size..."></textarea>
                <button type="submit" class="btn-submit">Send Inquiry to WhatsApp</button>
            </form>
        </div>

        <div style="height: 300px; border-radius: 20px; overflow: hidden; margin-top: 40px; border: 1px solid var(--border);">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1641.488316239103!2d74.843!3d35.367!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e663a890d79663%3A0x77c442436f564177!2sAstore!5e0!3m2!1sen!2s!4v1710000000000" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg);"></iframe>
        </div>

    </div>

    <div style="height: 100px;"></div>

    <a href="https://wa.me/923171588489" class="wa-float" target="_blank">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <nav class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <script>
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const text = `*NEW INQUIRY*\nName: ${n}\nWhatsApp: ${p}\nTour: ${t}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
