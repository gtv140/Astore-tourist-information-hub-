<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Signature | Peak Luxury</title>
    <link href="https://fonts.googleapis.com/css2?family=Bormioli:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --accent: #d4af37; /* Gold Accent for Luxury */
            --bg: #0a0a0a;
            --surface: #161616;
            --text-main: #ffffff;
            --text-dim: #a0a0a0;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text-main); overflow-x: hidden; scroll-behavior: smooth; }

        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 5px; }
        ::-webkit-scrollbar-track { background: var(--bg); }
        ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 10px; }

        /* Hero Video/Image Background */
        .hero {
            height: 100vh; width: 100%; position: relative;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            background: linear-gradient(to bottom, rgba(0,0,0,0.5), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=2070&auto=format&fit=crop');
            background-size: cover; background-position: center; text-align: center;
        }

        .hero h1 {
            font-size: clamp(40px, 8vw, 80px); letter-spacing: -2px; font-weight: 800;
            background: linear-gradient(to right, #fff, var(--text-dim));
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            animation: heroFade 1.5s ease;
        }

        /* Floating Cards Design */
        .section-container { max-width: 1100px; margin: -100px auto 50px; padding: 20px; position: relative; z-index: 10; }

        .booking-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; }

        .card {
            background: var(--surface); border: 1px solid rgba(255,255,255,0.05);
            border-radius: 30px; padding: 40px; transition: 0.5s cubic-bezier(0.2, 1, 0.2, 1);
            position: relative; overflow: hidden;
        }
        .card:hover { transform: translateY(-15px); border-color: var(--accent); }
        .card i { font-size: 40px; color: var(--accent); margin-bottom: 20px; opacity: 0.8; }

        /* Premium Inputs */
        .field { margin-bottom: 20px; }
        .field label { display: block; font-size: 11px; text-transform: uppercase; letter-spacing: 2px; color: var(--text-dim); margin-bottom: 8px; }
        .field input, .field select {
            width: 100%; background: rgba(255,255,255,0.03); border: none; border-bottom: 1px solid #333;
            padding: 12px 0; color: #fff; outline: none; transition: 0.3s; font-size: 16px;
        }
        .field input:focus { border-color: var(--accent); }

        /* Action Button */
        .cta-btn {
            width: 100%; padding: 20px; background: var(--accent); color: #000;
            border: none; border-radius: 50px; font-weight: 700; text-transform: uppercase;
            letter-spacing: 2px; cursor: pointer; transition: 0.4s; margin-top: 10px;
        }
        .cta-btn:hover { letter-spacing: 4px; box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3); }

        /* Dynamic History Section */
        .history-box { margin-top: 40px; background: #111; border-radius: 20px; padding: 20px; }
        .log-entry { padding: 15px; border-bottom: 1px solid #222; display: flex; justify-content: space-between; align-items: center; }

        /* Bottom Minimal Nav */
        .dock {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            background: rgba(255,255,255,0.05); backdrop-filter: blur(20px);
            padding: 10px 30px; border-radius: 100px; border: 1px solid rgba(255,255,255,0.1);
            display: flex; gap: 30px; z-index: 1000;
        }
        .dock-item { color: var(--text-dim); text-decoration: none; font-size: 20px; transition: 0.3s; }
        .dock-item:hover { color: var(--accent); transform: scale(1.2); }

        @keyframes heroFade { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }

        /* Responsive Mobile Fixes */
        @media (max-width: 600px) { .hero h1 { font-size: 45px; } .dock { gap: 20px; padding: 10px 20px; } }
    </style>
</head>
<body>

    <div class="hero">
        <div class="status-badge" style="border: 1px solid var(--accent); padding: 5px 15px; border-radius: 20px; font-size: 10px; color: var(--accent); margin-bottom: 20px;">EST. 2026 | ASTORE VALLEY</div>
        <h1>ASTORE SIGNATURE</h1>
        <p style="color: var(--text-dim); font-weight: 300; letter-spacing: 5px;">THE PEAK OF LUXURY</p>
        <div style="margin-top: 40px; animation: bounce 2s infinite;">
            <i class="fa-solid fa-chevron-down" style="color: var(--accent);"></i>
        </div>
    </div>

    <div class="section-container">
        <div class="booking-grid">
            <div class="card" id="room-card">
                <i class="fa-solid fa-hotel"></i>
                <h3 style="margin-bottom: 20px;">RESERVE A SUITE</h3>
                <form id="roomForm">
                    <div class="field"><label>Name</label><input type="text" id="rname" placeholder="John Doe" required></div>
                    <div class="field"><label>WhatsApp</label><input type="tel" id="rphone" placeholder="+92 ..." required></div>
                    <div style="display: flex; gap: 15px;">
                        <div class="field" style="flex:1;"><label>Check In</label><input type="date" id="rcheckin"></div>
                        <div class="field" style="flex:1;"><label>Check Out</label><input type="date" id="rcheckout"></div>
                    </div>
                    <div class="field">
                        <label>Category</label>
                        <select id="rtype">
                            <option>Presidential Suite</option>
                            <option>Royal Alpine Room</option>
                            <option>Executive Cabin</option>
                        </select>
                    </div>
                    <button type="submit" class="cta-btn">Check Availability</button>
                </form>
            </div>

            <div class="card" id="car-card">
                <i class="fa-solid fa-car-rear"></i>
                <h3 style="margin-bottom: 20px;">ELITE TRANSPORT</h3>
                <form id="carForm">
                    <div class="field"><label>Pickup Date</label><input type="date" id="cdate"></div>
                    <div class="field">
                        <label>Vehicle Fleet</label>
                        <select id="ctype">
                            <option>Land Cruiser V8 (Elite 4x4)</option>
                            <option>Prado TX (Adventure)</option>
                            <option>Luxury Grand Cabin</option>
                        </select>
                    </div>
                    <button type="submit" class="cta-btn" style="background: transparent; border: 1px solid var(--accent); color: var(--accent);">Request Fleet</button>
                </form>
            </div>
        </div>

        <div class="card" style="margin-top: 30px; text-align: center;">
            <h2 style="letter-spacing: 5px; margin-bottom: 20px;">OUR PRESENCE</h2>
            <iframe src="http://googleusercontent.com/maps.google.com/4" width="100%" height="300" style="border-radius: 20px; filter: grayscale(1) invert(1) brightness(0.8);" allowfullscreen="" loading="lazy"></iframe>
            <div style="margin-top: 30px; display: flex; justify-content: center; gap: 40px;">
                <a href="https://wa.me/923171588489" target="_blank" class="dock-item" style="color:#25d366;"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank" class="dock-item" style="color:#1877f2;"><i class="fa-brands fa-facebook"></i></a>
                <a href="mailto:mohammadasimkhan2746@gmail.com" class="dock-item" style="color:#ff4b4b;"><i class="fa-solid fa-envelope"></i></a>
            </div>
        </div>

        <div class="history-box" id="historyBox">
            <h4 style="font-size: 12px; color: var(--accent); letter-spacing: 2px; margin-bottom: 10px;">RECENT REQUESTS</h4>
            <div id="logContent" style="font-size: 13px; color: var(--text-dim);">No requests yet.</div>
        </div>
    </div>

    <div class="dock">
        <a onclick="window.scrollTo(0, 800)" class="dock-item"><i class="fa-solid fa-bed"></i></a>
        <a onclick="window.scrollTo(0, 800)" class="dock-item"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="https://wa.me/923171588489" class="dock-item"><i class="fa-solid fa-headset"></i></a>
    </div>

    <script>
        const WHATSAPP = "923171588489";

        function processBooking(e, category) {
            e.preventDefault();
            const formData = new FormData(e.target);
            let message = `*ASTORE SIGNATURE RESERVATION*\n*CATEGORY:* ${category}\n---\n`;
            
            for (let [key, value] of formData.entries()) {
                message += `*${key.toUpperCase()}:* ${value}\n`;
            }

            window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent(message)}`, '_blank');
            saveLog(category);
            e.target.reset();
        }

        document.getElementById('roomForm').onsubmit = (e) => processBooking(e, 'SUITE RESERVATION');
        document.getElementById('carForm').onsubmit = (e) => processBooking(e, 'FLEET REQUEST');

        function saveLog(cat) {
            let logs = JSON.parse(localStorage.getItem('sig_logs')) || [];
            logs.unshift({cat: cat, time: new Date().toLocaleTimeString()});
            localStorage.setItem('sig_logs', JSON.stringify(logs.slice(0,3)));
            renderLogs();
        }

        function renderLogs() {
            const box = document.getElementById('logContent');
            let logs = JSON.parse(localStorage.getItem('sig_logs')) || [];
            if(logs.length > 0) {
                box.innerHTML = logs.map(l => `<div class="log-entry"><span>${l.cat}</span><span style="font-size:10px;">${l.time}</span></div>`).join('');
            }
        }

        window.onload = renderLogs;
    </script>
</body>
</html>
