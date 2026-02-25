<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Luxury North</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #ff007a;
            --bg: #000000;
            --card: #0d1117;
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; line-height: 1.6; }

        /* --- Navbar --- */
        nav {
            padding: 20px 6%; display: flex; justify-content: space-between; align-items: center;
            background: #000; border-bottom: 1px solid var(--border); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 24px; font-weight: 800; text-transform: uppercase; letter-spacing: -1px; }
        .logo span { color: var(--primary); }
        .time-box { font-size: 12px; font-weight: 800; opacity: 0.6; }

        /* --- Section Titles --- */
        .container { padding: 30px 20px; max-width: 1000px; margin: 0 auto; }
        h2.title { font-family: 'Syne'; font-size: 32px; margin-bottom: 25px; border-bottom: 2px solid var(--primary); display: inline-block; padding-bottom: 5px; }

        /* --- Destination Cards (As per Screenshot 2) --- */
        .grid { display: flex; overflow-x: auto; gap: 20px; padding-bottom: 20px; scroll-snap-type: x mandatory; }
        .grid::-webkit-scrollbar { display: none; }
        
        .card {
            min-width: 85%; background: var(--card); border-radius: 25px; overflow: hidden;
            border: 1px solid var(--border); scroll-snap-align: center;
        }
        .card-img { width: 100%; height: 230px; background: #161b22; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }
        
        .card-content { padding: 25px; }
        .card-content h3 { font-family: 'Syne'; color: var(--primary); font-size: 24px; margin-bottom: 10px; }
        .card-content p { font-size: 14px; opacity: 0.8; }

        /* --- Booking UI (Solid & Colorful) --- */
        .booking-section { background: var(--card); padding: 30px; border-radius: 30px; border: 1px solid var(--primary); margin-top: 20px; }
        input, select, textarea {
            width: 100%; padding: 18px; margin-bottom: 15px; border-radius: 15px;
            border: 1px solid var(--border); background: #000; color: #fff; font-size: 16px; outline: none;
        }
        .btn-send {
            width: 100%; padding: 20px; background: var(--primary); color: #000;
            border: none; border-radius: 15px; font-weight: 800; text-transform: uppercase; cursor: pointer;
        }

        /* --- Fixed Bottom Nav --- */
        .bottom-nav {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 15px 0 30px;
            border-top: 1px solid var(--border); z-index: 2000;
        }
        .bottom-nav a { color: #fff; opacity: 0.4; font-size: 24px; transition: 0.3s; }
        .bottom-nav a.active { color: var(--primary); opacity: 1; }

        /* --- Weather Pill --- */
        .weather-pill {
            background: rgba(0,242,255,0.1); border: 1px solid var(--primary);
            padding: 10px 20px; border-radius: 50px; display: inline-flex; align-items: center;
            gap: 10px; font-size: 14px; font-weight: 800; margin-bottom: 30px;
        }

        footer { text-align: center; padding: 50px 0 120px; opacity: 0.3; font-size: 10px; letter-spacing: 3px; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <div class="time-box" id="clock">09:04 AM</div>
    </nav>

    <div class="container">
        
        <div class="weather-pill">
            <i class="fa-solid fa-cloud-sun"></i>
            <span>ASTORE LIVE: 14°C</span>
        </div>

        <h2 class="title">Top Spots</h2>
        
        <div class="grid">
            <div class="card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?w=800" alt="Rama">
                </div>
                <div class="card-content">
                    <h3>Rama Meadows</h3>
                    <p>The green jewel of Astore. Surrounded by mountains and pine forests. Experience the pure alpine air.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-img">
                    <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?w=800" alt="Deosai">
                </div>
                <div class="card-content">
                    <h3>Deosai Plains</h3>
                    <p>The Land of Giants. A mystical high-altitude plateau with vibrant flowers and Sheosar Lake.</p>
                </div>
            </div>
        </div>

        <h2 class="title" id="book" style="margin-top: 40px;">Book Tour</h2>
        
        <div class="booking-section">
            <form id="waForm">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Explorer</option>
                    <option>Hunza Valley Retreat</option>
                    <option>Skardu Special Trip</option>
                </select>
                <textarea id="msg" placeholder="Travel dates and details..." rows="4"></textarea>
                <button type="submit" class="btn-send">Send WhatsApp Inquiry</button>
            </form>
        </div>

        <footer>© 2026 ASTORE HUB | ALL RIGHTS RESERVED</footer>
    </div>

    <div class="bottom-nav">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-image"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <script>
        // Clock
        function updateClock() {
            const now = new Date();
            document.getElementById('clock').innerText = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
        }
        setInterval(updateClock, 1000);
        updateClock();

        // Form
        document.getElementById('waForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            const text = `🚀 *ASTORE HUB INQUIRY*\n---\n*Explorer:* ${n}\n*Trip:* ${t}\n---\nSent from Website.`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
