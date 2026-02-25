<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Feel the Mountains</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --primary: #00f2ff;
            --secondary: #0066ff;
            --bg-dark: #020617;
            --card-glass: rgba(255, 255, 255, 0.03);
            --accent-gradient: linear-gradient(135deg, #00f2ff 0%, #0066ff 100%);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Plus Jakarta Sans', sans-serif; background: var(--bg-dark); color: #fff; overflow-x: hidden; }

        /* Smooth Background Glows */
        .glow {
            position: fixed; width: 400px; height: 400px; background: radial-gradient(circle, rgba(0, 242, 255, 0.1) 0%, transparent 70%);
            z-index: -1; pointer-events: none;
        }

        /* Hero Section with Parallax Feel */
        .hero {
            height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center;
            background: linear-gradient(to bottom, rgba(2, 6, 23, 0.3), var(--bg-dark)),
                        url('https://images.unsplash.com/photo-1622324341735-906567087679?q=80&w=2070&auto=format&fit=crop');
            background-size: cover; background-position: center; background-attachment: fixed; text-align: center; padding: 20px;
        }

        .hero h1 {
            font-family: 'Syne', sans-serif; font-size: clamp(40px, 10vw, 90px); font-weight: 800;
            line-height: 0.9; text-transform: uppercase; margin-bottom: 20px;
            background: var(--accent-gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent;
        }

        .hero-badge {
            background: rgba(255, 255, 255, 0.1); padding: 8px 20px; border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.2); font-size: 12px; letter-spacing: 3px; margin-bottom: 20px;
        }

        /* Floating Info Hub Cards */
        .content-wrapper { max-width: 1200px; margin: -80px auto 100px; padding: 20px; }

        .grid-layout { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px; }

        .glass-panel {
            background: var(--card-glass); backdrop-filter: blur(20px); border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 40px; padding: 40px; transition: 0.5s; position: relative;
        }
        .glass-panel:hover { border-color: var(--primary); transform: translateY(-10px); background: rgba(255, 255, 255, 0.05); }

        /* Stylish Forms */
        h2 { font-family: 'Syne', sans-serif; font-size: 24px; margin-bottom: 25px; display: flex; align-items: center; gap: 15px; }
        .input-box { position: relative; margin-bottom: 25px; }
        .input-box input, .input-box select {
            width: 100%; background: transparent; border: none; border-bottom: 2px solid rgba(255,255,255,0.1);
            padding: 10px 0; color: #fff; font-size: 16px; outline: none; transition: 0.3s;
        }
        .input-box input:focus { border-color: var(--primary); }
        .input-box label { font-size: 11px; text-transform: uppercase; color: var(--primary); display: block; margin-bottom: 5px; }

        /* Luxury Button */
        .action-btn {
            width: 100%; padding: 18px; border-radius: 20px; border: none;
            background: var(--accent-gradient); color: #000; font-weight: 800;
            text-transform: uppercase; letter-spacing: 2px; cursor: pointer; transition: 0.3s;
        }
        .action-btn:hover { box-shadow: 0 0 40px rgba(0, 242, 255, 0.4); transform: scale(1.02); }

        /* Floating Dock Navigation */
        .dock {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            background: rgba(15, 23, 42, 0.8); backdrop-filter: blur(15px);
            padding: 15px 40px; border-radius: 100px; border: 1px solid rgba(255,255,255,0.1);
            display: flex; gap: 40px; z-index: 1000;
        }
        .dock i { font-size: 22px; color: #64748b; cursor: pointer; transition: 0.3s; }
        .dock i:hover { color: var(--primary); transform: translateY(-5px); }

        /* History Activity Bar */
        .activity-bar { margin-top: 30px; font-size: 12px; color: #64748b; text-align: center; }

        /* Map Styling */
        .map-box iframe { width: 100%; height: 250px; border-radius: 30px; filter: grayscale(1) invert(1) brightness(0.7); border: 1px solid rgba(255,255,255,0.1); }
    </style>
</head>
<body>

    <div class="glow" style="top: 10%; right: 10%;"></div>
    <div class="glow" style="bottom: 20%; left: 5%;"></div>

    <section class="hero">
        <div class="hero-badge">ASTORE • GILGIT BALTISTAN</div>
        <h1>ASTORE<br>VALLEY</h1>
        <p style="letter-spacing: 8px; font-size: 12px; margin-top: 10px; opacity: 0.6;">INFORMATION HUB & SERVICES</p>
    </section>

    <div class="content-wrapper">
        <div class="grid-layout">
            
            <div class="glass-panel" id="stay">
                <h2><i class="fa-solid fa-moon"></i> Stay Hub</h2>
                <form id="stayForm">
                    <div class="input-box">
                        <label>Explorer Name</label>
                        <input type="text" id="sname" placeholder="Who is travelling?" required>
                    </div>
                    <div class="input-box">
                        <label>WhatsApp Contact</label>
                        <input type="tel" id="sphone" placeholder="+92 ..." required>
                    </div>
                    <div class="input-box">
                        <label>Accommodation</label>
                        <select id="stype">
                            <option>Mountain View Suite</option>
                            <option>Luxury Pine Cabin</option>
                            <option>Basecamp Standard</option>
                        </select>
                    </div>
                    <button type="submit" class="action-btn">Request Reservation</button>
                </form>
            </div>

            <div class="glass-panel" id="ride">
                <h2><i class="fa-solid fa-compass"></i> Ride Hub</h2>
                <form id="rideForm">
                    <div class="input-box">
                        <label>Pickup Location</label>
                        <input type="text" id="loc" placeholder="Astore Bazar / Gilgit" required>
                    </div>
                    <div class="input-box">
                        <label>Select Fleet</label>
                        <select id="vtype">
                            <option>Prado V6 (Deosai Special)</option>
                            <option>Jeep 4x4 (Local Routes)</option>
                            <option>Hiace (Group Travel)</option>
                        </select>
                    </div>
                    <button type="submit" class="action-btn" style="background: #fff; color: #000;">Book Adventure</button>
                </form>
            </div>

        </div>

        <div class="glass-panel" style="margin-top: 30px; text-align: center;">
            <h2 style="justify-content: center;">FIND US IN THE PEAKS</h2>
            <div class="map-box">
                <iframe src="http://googleusercontent.com/maps.google.com/5"></iframe>
            </div>
            <div style="margin-top: 30px; display: flex; justify-content: center; gap: 50px;">
                <a href="https://wa.me/923171588489" target="_blank" style="color: #25d366; font-size: 30px;"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank" style="color: #1877f2; font-size: 30px;"><i class="fa-brands fa-facebook"></i></a>
                <a href="mailto:mohammadasimkhan2746@gmail.com" style="color: #ff4b4b; font-size: 30px;"><i class="fa-solid fa-envelope"></i></a>
            </div>
        </div>

        <div class="activity-bar" id="historyText">Waiting for your first adventure booking...</div>
    </div>

    <nav class="dock">
        <i class="fa-solid fa-bed" onclick="window.scrollTo(0, 800)"></i>
        <i class="fa-solid fa-car" onclick="window.scrollTo(0, 800)"></i>
        <i class="fa-solid fa-map-location-dot" onclick="window.scrollTo(0, 1500)"></i>
        <i class="fa-solid fa-info-circle" onclick="alert('Astore Hub v3.0 - Ready for 2026')"></i>
    </nav>

    <script>
        const WHATSAPP_API = "923171588489";

        function sendBooking(e, category) {
            e.preventDefault();
            const formData = new FormData(e.target);
            let message = `*ASTORE HUB - NEW INQUIRY*\n*Category:* ${category}\n---\n`;
            
            for (let [key, value] of formData.entries()) {
                message += `*${key.toUpperCase()}:* ${value}\n`;
            }

            window.open(`https://wa.me/${WHATSAPP_API}?text=${encodeURIComponent(message)}`, '_blank');
            
            // Update Activity Bar
            document.getElementById('historyText').innerText = `Last Inquiry: ${category} sent at ${new Date().toLocaleTimeString()}`;
            e.target.reset();
        }

        document.getElementById('stayForm').onsubmit = (e) => sendBooking(e, 'Accommodation');
        document.getElementById('rideForm').onsubmit = (e) => sendBooking(e, 'Transport Fleet');

        // Simple Parallax Effect
        window.addEventListener('scroll', () => {
            let offset = window.pageYOffset;
            document.querySelector('.hero h1').style.transform = `translateY(${offset * 0.4}px)`;
        });
    </script>
</body>
</html>
