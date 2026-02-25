<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Luxury Experience</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --bg: #010409;
            --card-bg: #0d1117;
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; }

        /* Modern Nav */
        nav {
            position: sticky; top: 0; width: 100%; padding: 20px;
            background: rgba(1, 4, 9, 0.95); backdrop-filter: blur(10px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 22px; font-weight: 800; letter-spacing: -1px; }
        .logo span { color: var(--primary); }

        /* Hero */
        .hero {
            padding: 60px 20px; text-align: center;
            background: linear-gradient(rgba(0,0,0,0.7), var(--bg)), url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1200&auto=format');
            background-size: cover; background-position: center;
        }
        .hero h1 { font-family: 'Syne'; font-size: 48px; text-transform: uppercase; line-height: 1; margin-bottom: 10px; }

        .weather-chip {
            display: inline-flex; align-items: center; gap: 8px;
            background: rgba(0, 242, 255, 0.15); border: 1px solid var(--primary);
            padding: 8px 16px; border-radius: 50px; font-size: 13px; font-weight: 700;
        }

        .container { padding: 20px; max-width: 1000px; margin: 0 auto; }

        /* Destination Cards - Fixed Images */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-top: 20px; }
        .card { background: var(--card-bg); border-radius: 20px; overflow: hidden; border: 1px solid var(--border); }
        .card .img-box { width: 100%; height: 200px; background: #161b22; position: relative; }
        .card img { width: 100%; height: 100%; object-fit: cover; }
        .card-info { padding: 20px; }
        .card-info h3 { font-family: 'Syne'; color: var(--primary); margin-bottom: 8px; }
        .card-info p { font-size: 14px; opacity: 0.7; line-height: 1.5; }

        /* Booking Section */
        .form-card { background: var(--card-bg); padding: 30px; border-radius: 25px; border: 1px solid var(--primary); margin: 40px 0 100px; }
        input, select, textarea {
            width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px;
            border: 1px solid var(--border); background: #010409; color: #fff; font-size: 16px;
        }
        .btn-glow {
            width: 100%; padding: 18px; background: var(--primary); color: #000;
            border: none; border-radius: 12px; font-weight: 800; cursor: pointer; text-transform: uppercase;
        }

        /* Fixed Bottom Bar */
        .dock {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 15px 0 30px;
            border-top: 1px solid var(--border); z-index: 2000;
        }
        .dock a { color: #fff; opacity: 0.5; font-size: 24px; transition: 0.3s; }
        .dock a.active { color: var(--primary); opacity: 1; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div id="time" style="font-size: 12px; font-weight: bold; color: var(--primary);">00:00</div>
    </nav>

    <section class="hero">
        <p style="letter-spacing: 5px; font-size: 10px; margin-bottom: 10px;">PREMIUM TRAVEL HUB</p>
        <h1>EXPLORE THE<br><span>NORTH</span></h1>
        <div class="weather-chip">
            <i class="fa-solid fa-cloud-sun-rain"></i>
            <span>ASTORE: 14°C | LIVE</span>
        </div>
    </section>

    <div class="container">
        <h2 style="font-family:'Syne'; font-size: 28px; margin: 20px 0;">Top Spots</h2>
        
        <div class="grid">
            <div class="card">
                <div class="img-box">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=600" alt="Rama">
                </div>
                <div class="card-info">
                    <h3>Rama Meadows</h3>
                    <p>Experience the lush green meadows and the majestic Rama Lake at the foot of Nanga Parbat.</p>
                </div>
            </div>

            <div class="card">
                <div class="img-box">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&fit=crop&w=600" alt="Deosai">
                </div>
                <div class="card-info">
                    <h3>Deosai Plains</h3>
                    <p>Visit the Land of Giants. A high-altitude plateau with breathtaking wildflowers and clear blue skies.</p>
                </div>
            </div>
        </div>

        <h2 id="book" style="font-family:'Syne'; font-size: 28px; margin: 40px 0 20px;">Book Your Tour</h2>
        <div class="form-card">
            <form id="waForm">
                <input type="text" id="user" placeholder="Your Name" required>
                <input type="tel" id="whatsapp" placeholder="WhatsApp Number" required>
                <select id="trip">
                    <option>Astore & Deosai Special</option>
                    <option>Hunza Valley Retreat</option>
                    <option>Skardu Adventure</option>
                </select>
                <textarea id="note" placeholder="Any special requests?"></textarea>
                <button type="submit" class="btn-glow">Request Booking</button>
            </form>
        </div>
    </div>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house-user"></i></a>
        <a href="#book"><i class="fa-solid fa-map-marked-alt"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <script>
        // Real-time Clock
        function getTime() {
            const now = new Date();
            document.getElementById('time').innerText = now.getHours() + ":" + now.getMinutes().toString().padStart(2, '0');
        }
        setInterval(getTime, 1000);
        getTime();

        // Form Submission
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const u = document.getElementById('user').value;
            const t = document.getElementById('trip').value;
            const text = `🚀 *ASTORE HUB BOOKING*\n---\n*Name:* ${u}\n*Tour:* ${t}\n---\nSent from Website.`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
