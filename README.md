<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | GB Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;700&family=Syne:wght@800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root { --primary: #00f2ff; --bg: #05070a; --glass: rgba(255,255,255,0.05); }
        
        /* Mobile Optimization */
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; }

        /* Smooth Images Loader */
        img { max-width: 100%; height: auto; display: block; background: #111; }

        /* Modern Header */
        nav { position: fixed; top: 0; width: 100%; padding: 15px; background: rgba(5,7,10,0.8); backdrop-filter: blur(10px); z-index: 1000; display: flex; justify-content: space-between; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .logo { font-family: 'Syne'; font-size: 18px; color: var(--primary); }

        /* Hero Section - Mobile Optimized */
        .hero { height: 60vh; background: linear-gradient(to bottom, rgba(0,0,0,0.2), var(--bg)), url('https://picsum.photos/id/1015/800/1200') no-repeat center center/cover; display: flex; align-items: center; justify-content: center; text-align: center; padding: 20px; }
        .hero h1 { font-family: 'Syne'; font-size: 40px; line-height: 1; margin-top: 50px; }

        /* Destination Grid - Mobile Stack */
        .container { padding: 20px; max-width: 1200px; margin: 0 auto; }
        .section-title { font-family: 'Syne'; font-size: 24px; margin: 30px 0 20px; color: var(--primary); }
        
        .grid { display: grid; grid-template-columns: 1fr; gap: 20px; }
        @media(min-width: 768px) { .grid { grid-template-columns: repeat(3, 1fr); } }

        .card { background: var(--glass); border-radius: 20px; overflow: hidden; border: 1px solid rgba(255,255,255,0.1); }
        .card-img { width: 100%; height: 220px; object-fit: cover; }
        .card-content { padding: 20px; }
        .card-content h3 { margin-bottom: 8px; font-size: 18px; }
        .card-content p { font-size: 14px; opacity: 0.7; }

        /* Booking Form - Super Simple for Mobile */
        .form-box { background: var(--glass); padding: 25px; border-radius: 25px; margin-top: 40px; border: 1px solid var(--primary); }
        input, select, textarea { width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px; border: 1px solid rgba(255,255,255,0.2); background: #000; color: #fff; font-size: 16px; }
        .btn { width: 100%; padding: 18px; background: var(--primary); color: #000; border: none; border-radius: 12px; font-weight: 800; text-transform: uppercase; cursor: pointer; }

        /* Floating WhatsApp for Mobile */
        .wa-float { position: fixed; bottom: 90px; right: 20px; background: #25d366; width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 28px; color: #fff; z-index: 1000; box-shadow: 0 5px 15px rgba(0,0,0,0.3); }

        /* Mobile Dock Nav */
        .dock { position: fixed; bottom: 0; width: 100%; background: #000; display: flex; justify-content: space-around; padding: 15px; border-top: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .dock a { color: #fff; opacity: 0.5; font-size: 22px; }
        .dock a.active { color: var(--primary); opacity: 1; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE HUB</div>
        <div style="font-size: 10px; opacity: 0.5;">GB GUIDE 2026</div>
    </nav>

    <div class="hero">
        <h1>EXPLORE<br><span style="color:var(--primary)">ASTORE</span></h1>
    </div>

    <div class="container">
        <h2 class="section-title">Destinations</h2>
        <div class="grid">
            <div class="card">
                <img src="https://picsum.photos/seed/astore/600/400" class="card-img" alt="Astore">
                <div class="card-content">
                    <h3>Rama Meadows</h3>
                    <p>Green paradise near Nanga Parbat. Best for camping.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://picsum.photos/seed/hunza/600/400" class="card-img" alt="Hunza">
                <div class="card-content">
                    <h3>Hunza Valley</h3>
                    <p>Stunning Attabad Lake and ancient forts.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://picsum.photos/seed/skardu/600/400" class="card-img" alt="Skardu">
                <div class="card-content">
                    <h3>Skardu City</h3>
                    <p>Gateway to K2 and Cold Deserts.</p>
                </div>
            </div>
        </div>

        <div class="form-box" id="book">
            <h2 style="margin-bottom: 20px; text-align: center;">Plan Your Tour</h2>
            <form id="waForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai</option>
                    <option>Hunza Valley</option>
                    <option>Skardu Adventure</option>
                </select>
                <button type="submit" class="btn">Send Inquiry</button>
            </form>
        </div>
    </div>

    <a href="https://wa.me/923171588489" class="wa-float"><i class="fa-brands fa-whatsapp"></i></a>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-solid fa-comment"></i></a>
    </div>

    <script>
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            window.open(`https://wa.me/923171588489?text=Hi, I am ${n}. I want to book ${t} tour.`, '_blank');
        };
    </script>
</body>
</html>
