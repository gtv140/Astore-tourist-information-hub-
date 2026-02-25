<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Official</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Plus+Jakarta+Sans:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --accent: #ff007a;
            --bg: #050505;
            --glass: rgba(255, 255, 255, 0.05);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Plus Jakarta Sans', sans-serif; }
        body { background: var(--bg); color: #fff; overflow-x: hidden; scroll-behavior: smooth; }

        /* --- Stylish Header --- */
        header {
            padding: 20px 5%; display: flex; justify-content: space-between; align-items: center;
            background: rgba(0,0,0,0.8); backdrop-filter: blur(10px); position: sticky; top: 0; z-index: 1000;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }
        .logo { font-family: 'Syne'; font-size: 22px; font-weight: 800; color: var(--primary); }
        .logo span { color: #fff; }

        /* --- Hero Section --- */
        .hero {
            height: 70vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            text-align: center; padding: 20px;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1200&auto=format');
            background-size: cover; background-position: center;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(40px, 12vw, 80px); line-height: 0.9; margin-bottom: 15px; text-transform: uppercase; }
        .hero p { color: var(--primary); letter-spacing: 5px; font-size: 10px; font-weight: bold; }

        /* --- Section Styling --- */
        .container { padding: 40px 20px; max-width: 1100px; margin: 0 auto; }
        .section-title { font-family: 'Syne'; font-size: 32px; margin-bottom: 30px; border-left: 5px solid var(--accent); padding-left: 15px; }

        /* --- Colorful Modern Cards --- */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        .modern-card {
            background: var(--glass); border-radius: 30px; overflow: hidden; border: 1px solid rgba(255,255,255,0.1);
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .modern-card:hover { transform: scale(1.02); border-color: var(--primary); box-shadow: 0 10px 30px rgba(0, 242, 255, 0.2); }
        .card-img { height: 250px; background: #111; position: relative; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }
        .card-content { padding: 25px; }
        .card-content h3 { font-family: 'Syne'; font-size: 24px; color: var(--primary); margin-bottom: 10px; }
        .card-content p { font-size: 14px; opacity: 0.7; line-height: 1.6; }

        /* --- Extra Details List --- */
        .details-list { background: rgba(255,0,122,0.05); padding: 30px; border-radius: 30px; margin: 40px 0; border: 1px dashed var(--accent); }
        .details-list h4 { color: var(--accent); margin-bottom: 15px; font-family: 'Syne'; }
        .details-list li { list-style: none; margin-bottom: 10px; font-size: 14px; display: flex; align-items: center; gap: 10px; }
        .details-list li i { color: var(--primary); }

        /* --- Booking Form --- */
        .booking-box { background: #0f0f0f; padding: 35px; border-radius: 40px; border: 1px solid var(--primary); margin-bottom: 100px; }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 15px; border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.1); background: #000; color: #fff; font-size: 16px; outline: none;
        }
        input:focus { border-color: var(--primary); }
        .btn-main {
            width: 100%; padding: 20px; background: linear-gradient(to right, var(--primary), #0072ff);
            color: #000; border: none; border-radius: 15px; font-weight: 800; font-size: 16px;
            cursor: pointer; text-transform: uppercase; transition: 0.3s;
        }
        .btn-main:hover { letter-spacing: 2px; box-shadow: 0 5px 20px var(--primary); }

        /* --- Modern App-Style Dock --- */
        .dock {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(10, 10, 10, 0.8);
            backdrop-filter: blur(20px); border-radius: 100px; padding: 15px 30px;
            display: flex; justify-content: space-between; align-items: center;
            border: 1px solid rgba(255,255,255,0.1); z-index: 2000; box-shadow: 0 10px 40px rgba(0,0,0,0.5);
        }
        .dock a { color: #fff; opacity: 0.4; font-size: 22px; transition: 0.3s; text-decoration: none; }
        .dock a.active { color: var(--primary); opacity: 1; transform: scale(1.2); }

        footer { text-align: center; padding-bottom: 140px; opacity: 0.3; font-size: 12px; }
    </style>
</head>
<body>

    <header>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div id="clock" style="font-weight: bold; color: var(--primary); font-size: 14px;">00:00</div>
    </header>

    <section class="hero">
        <p>DISCOVER THE UNSEEN</p>
        <h1>BEYOND THE<br><span>HORIZON</span></h1>
        <div style="margin-top: 20px; background: rgba(0,242,255,0.1); padding: 8px 20px; border-radius: 50px; font-size: 12px; border: 1px solid var(--primary);">
            <i class="fa-solid fa-cloud-sun"></i> Astore Temp: 14°C
        </div>
    </section>

    <div class="container">
        
        <h2 class="section-title">Premium Trips</h2>
        <div class="grid">
            <div class="modern-card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&w=800" alt="Rama">
                </div>
                <div class="card-content">
                    <h3>Rama Meadows</h3>
                    <p>Known as the "Fairyland", Rama offers lush forests and the crystal clear Rama Lake. Perfect for camping and soul searching.</p>
                </div>
            </div>
            <div class="modern-card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&w=800" alt="Deosai">
                </div>
                <div class="card-content">
                    <h3>Deosai Plains</h3>
                    <p>The Land of Giants. A massive high-altitude plateau with vibrant flowers and the rare Himalayan Brown Bears.</p>
                </div>
            </div>
        </div>

        <div class="details-list">
            <h4><i class="fa-solid fa-circle-info"></i> Travel Essentials</h4>
            <li><i class="fa-solid fa-check"></i> Best Time: May to October</li>
            <li><i class="fa-solid fa-check"></i> Vehicle: 4x4 Jeep is mandatory for Deosai</li>
            <li><i class="fa-solid fa-check"></i> Clothing: Heavy woolens even in summer</li>
            <li><i class="fa-solid fa-check"></i> Support: 24/7 Local Guides Available</li>
        </div>

        <h2 class="section-title" id="book">Get a Free Quote</h2>
        <div class="booking-box">
            <form id="waForm">
                <input type="text" id="name" placeholder="Enter Your Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Explorer</option>
                    <option>Hunza Valley Retreat</option>
                    <option>Skardu Adventure Trip</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Mention dates and total members..."></textarea>
                <button type="submit" class="btn-main">Send WhatsApp Inquiry</button>
            </form>
        </div>

        <footer>© 2026 ASTORE HUB | PREVIEW EDITION</footer>
    </div>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house-chimney"></i></a>
        <a href="#book"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <script>
        // Clock Update
        function updateClock() {
            const now = new Date();
            document.getElementById('clock').innerText = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
        }
        setInterval(updateClock, 1000);
        updateClock();

        // Form Handler
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;
            const msg = `🚀 *NEW INQUIRY*\n---\n*Explorer:* ${n}\n*Tour:* ${t}\n*Details:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, '_blank');
        };
    </script>
</body>
</html>
