<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Luxury Northern Travels</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #7000ff;
            --bg: #030712;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.08);
        }

        /* Base Setup */
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; scroll-behavior: smooth; }

        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 10px; }

        /* Header */
        nav.main-nav {
            position: fixed; top: 0; width: 100%; padding: 18px 6%;
            background: rgba(3, 7, 18, 0.8); backdrop-filter: blur(20px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 22px; font-weight: 800; letter-spacing: -1px; }
        .logo span { color: var(--primary); text-shadow: 0 0 15px rgba(0,242,255,0.4); }

        /* Hero Section - Super Modern */
        .hero {
            height: 85vh; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.5), var(--bg)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1600&auto=format') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(42px, 12vw, 100px); line-height: 0.85; margin-bottom: 15px; text-transform: uppercase; }
        .hero p { font-size: 10px; letter-spacing: 6px; text-transform: uppercase; color: var(--primary); font-weight: 800; opacity: 0.8; }

        /* Weather Widget */
        .weather-bar {
            display: flex; gap: 10px; justify-content: center; margin-top: 25px;
        }
        .weather-pill {
            background: var(--glass); border: 1px solid var(--border);
            padding: 8px 15px; border-radius: 100px; font-size: 12px;
            display: flex; align-items: center; gap: 8px;
        }

        /* Container */
        .container { max-width: 1200px; margin: 0 auto; padding: 50px 20px; }
        .section-header { margin-bottom: 40px; }
        .section-header h2 { font-family: 'Syne'; font-size: 36px; line-height: 1; }
        .section-header p { color: #9ca3af; font-size: 14px; margin-top: 10px; }

        /* Destination Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .modern-card {
            background: var(--glass); border-radius: 32px; overflow: hidden;
            border: 1px solid var(--border); transition: 0.5s cubic-bezier(0.2, 0.8, 0.2, 1);
            position: relative;
        }
        .modern-card:hover { transform: translateY(-10px); border-color: var(--primary); background: rgba(255,255,255,0.06); }
        .card-img { height: 280px; position: relative; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }
        .card-body { padding: 30px; }
        .card-body h3 { font-family: 'Syne'; font-size: 24px; margin-bottom: 12px; color: var(--primary); }
        .card-body p { font-size: 14px; color: #9ca3af; line-height: 1.6; }

        /* Booking Section */
        .booking-card {
            background: linear-gradient(145deg, #0f172a, #020617);
            padding: 40px; border-radius: 35px; border: 1px solid var(--primary);
            box-shadow: 0 20px 50px rgba(0, 242, 255, 0.1);
        }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 20px; border-radius: 16px;
            border: 1px solid var(--border); background: rgba(0,0,0,0.3); color: #fff;
            font-size: 16px; outline: none; transition: 0.3s;
        }
        input:focus { border-color: var(--primary); box-shadow: 0 0 15px rgba(0, 242, 255, 0.2); }
        .btn-submit {
            width: 100%; padding: 22px; background: var(--primary); color: #000;
            border: none; border-radius: 16px; font-weight: 800; font-size: 16px;
            text-transform: uppercase; cursor: pointer; transition: 0.4s;
        }
        .btn-submit:hover { letter-spacing: 2px; box-shadow: 0 10px 30px var(--primary); }

        /* App Dock */
        .app-dock {
            position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%);
            width: 90%; max-width: 400px; background: rgba(10, 10, 10, 0.8);
            backdrop-filter: blur(25px); border-radius: 100px; padding: 12px 30px;
            display: flex; justify-content: space-between; align-items: center;
            border: 1px solid var(--border); z-index: 1000; box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }
        .app-dock a { color: #fff; opacity: 0.4; font-size: 22px; transition: 0.3s; }
        .app-dock a.active { color: var(--primary); opacity: 1; transform: scale(1.2); }

        @media (max-width: 600px) {
            .hero h1 { font-size: 55px; }
            .booking-card { padding: 25px; }
        }
    </style>
</head>
<body>

    <nav class="main-nav">
        <div class="logo">ASTORE<span>HUB</span></div>
        <div style="font-size: 10px; font-weight: 800; opacity: 0.6;">v2.0 MASTER</div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <p>Your Adventure Starts Here</p>
            <h1>PEAKS &<br><span>VISIONS</span></h1>
            
            <div class="weather-bar">
                <div class="weather-pill"><i class="fa-solid fa-cloud-sun"></i> Astore: 12°C</div>
                <div class="weather-pill"><i class="fa-solid fa-temperature-low"></i> Hunza: 15°C</div>
            </div>
        </div>
    </section>

    <div class="container">
        
        <div class="section-header">
            <h2>Elite <span>Destinations</span></h2>
            <p>Handpicked spots for the ultimate Gilgit-Baltistan experience.</p>
        </div>

        <div class="grid">
            <div class="modern-card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800">
                </div>
                <div class="card-body">
                    <h3>Rama Meadows</h3>
                    <p>Known as the "Crown of Astore", this lush valley offers the best views of Nanga Parbat.</p>
                </div>
            </div>

            <div class="modern-card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800">
                </div>
                <div class="card-body">
                    <h3>Deosai Plains</h3>
                    <p>The highest plateau in Pakistan. A mystical landscape of flowers and clear blue lakes.</p>
                </div>
            </div>
        </div>

        

        <div class="section-header" id="book" style="margin-top: 80px;">
            <h2>Reserve <span>Your Seat</span></h2>
            <p>Direct connection to the hub's expert planners via WhatsApp.</p>
        </div>

        <div class="booking-card">
            <form id="ultraForm">
                <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px;">
                    <input type="text" id="name" placeholder="Your Full Name" required>
                    <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                </div>
                <select id="tour">
                    <option>The Astore Explorer (7 Days)</option>
                    <option>Hunza & Nagar Luxury (6 Days)</option>
                    <option>The Grand GB Safari (10 Days)</option>
                </select>
                <textarea id="msg" rows="4" placeholder="Mention your group size and arrival dates..."></textarea>
                <button type="submit" class="btn-submit">Initialize Booking</button>
            </form>
        </div>

        <div style="height: 350px; border-radius: 35px; overflow: hidden; margin-top: 50px; border: 1px solid var(--border);">
            <iframe src="http://googleusercontent.com/maps.google.com/8" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg) brightness(0.8);"></iframe>
        </div>

    </div>

    <nav class="app-dock">
        <a href="#" class="active"><i class="fa-solid fa-house-chimney-window"></i></a>
        <a href="#book"><i class="fa-solid fa-compass"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <footer style="text-align: center; padding: 100px 20px 160px; opacity: 0.3; font-size: 10px; letter-spacing: 4px;">
        © 2026 ASTORE TOURIST HUB | DIGITAL GATEWAY
    </footer>

    <script>
        document.getElementById('ultraForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const p = document.getElementById('phone').value;
            const t = document.getElementById('tour').value;
            const m = document.getElementById('msg').value;

            const text = `🚀 *NEW EXPEDITION INQUIRY*\n---\n*Explorer:* ${n}\n*Contact:* ${p}\n*Trip:* ${t}\n*Notes:* ${m}`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
