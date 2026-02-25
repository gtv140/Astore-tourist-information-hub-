<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Real-Time Guide</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root {
            --primary: #00f2ff;
            --bg: #010409;
            --card-bg: rgba(255, 255, 255, 0.05);
            --border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; scroll-behavior: smooth; }

        /* Navigation */
        nav.navbar {
            position: fixed; top: 0; width: 100%; padding: 15px 6%;
            background: rgba(1, 4, 9, 0.9); backdrop-filter: blur(15px);
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--border); z-index: 1000;
        }
        .logo { font-family: 'Syne'; font-size: 20px; font-weight: 800; text-transform: uppercase; }
        .logo span { color: var(--primary); }

        /* Hero with Real Image */
        .hero {
            height: 75vh; display: flex; align-items: center; justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), var(--bg)), 
                        url('https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=1200&auto=format') no-repeat center center/cover;
            text-align: center; padding: 20px;
        }
        .hero h1 { font-family: 'Syne'; font-size: clamp(40px, 12vw, 80px); line-height: 0.9; margin-bottom: 15px; }

        /* Live Weather Widget */
        .weather-box {
            background: rgba(0, 242, 255, 0.1); border: 1px solid var(--primary);
            padding: 10px 20px; border-radius: 50px; display: inline-flex; align-items: center; gap: 10px;
            font-size: 14px; font-weight: 700; margin-top: 10px;
        }

        .container { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }
        
        /* Grid System */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .card {
            background: var(--card-bg); border-radius: 24px; overflow: hidden;
            border: 1px solid var(--border); transition: 0.3s;
        }
        .card:hover { border-color: var(--primary); transform: translateY(-5px); }
        .card img { width: 100%; height: 220px; object-fit: cover; }
        .card-body { padding: 20px; }
        .card-body h3 { font-family: 'Syne'; margin-bottom: 10px; color: var(--primary); }

        /* Booking Form */
        .booking-ui { background: var(--card-bg); padding: 30px; border-radius: 30px; border: 1px solid var(--border); margin-top: 40px; }
        input, select, textarea {
            width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px;
            border: 1px solid var(--border); background: #000; color: #fff; outline: none;
        }
        .btn-send {
            width: 100%; padding: 18px; background: var(--primary); color: #000;
            border: none; border-radius: 12px; font-weight: 800; cursor: pointer; text-transform: uppercase;
        }

        /* Bottom App Bar */
        .app-bar {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 15px 0 30px;
            border-top: 1px solid var(--border); z-index: 1000;
        }
        .app-bar a { color: #fff; opacity: 0.5; font-size: 20px; text-decoration: none; }
        .app-bar a.active { color: var(--primary); opacity: 1; }

        @media (max-width: 768px) {
            .hero h1 { font-size: 50px; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">ASTORE<span>HUB</span></div>
        <div id="live-clock" style="font-size: 10px; opacity: 0.6;">00:00:00</div>
    </nav>

    <section class="hero">
        <div>
            <p style="letter-spacing: 5px; font-size: 10px; font-weight: 800; color: var(--primary);">WELCOME TO HEAVEN</p>
            <h1>ASTORE<br>VALLEY</h1>
            
            <div class="weather-box">
                <i class="fa-solid fa-temperature-half"></i>
                <span>Astore: 12°C | Sunny</span>
            </div>
        </div>
    </section>

    <div class="container">
        
        <h2 style="font-family:'Syne'; margin-bottom:25px;">Top Spots</h2>
        <div class="grid">
            <div class="card">
                <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?q=80&w=800&auto=format" alt="Rama">
                <div class="card-body">
                    <h3>Rama Meadows</h3>
                    <p>The green jewel of Astore. Surrounded by mountains and pine forests.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?q=80&w=800&auto=format" alt="Hunza">
                <div class="card-body">
                    <h3>Hunza Valley</h3>
                    <p>Ancient forts, blue lakes, and the world-famous hospitality.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?q=80&w=800&auto=format" alt="Deosai">
                <div class="card-body">
                    <h3>Deosai Plains</h3>
                    <p>The second-highest plateau in the world. Home of the Brown Bear.</p>
                </div>
            </div>
        </div>

        

        <h2 id="book" style="font-family:'Syne'; margin: 50px 0 20px;">Book Tour</h2>
        <div class="booking-ui">
            <form id="hubForm">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Safari</option>
                    <option>Hunza Luxury Trip</option>
                    <option>Skardu Adventure</option>
                </select>
                <textarea id="msg" placeholder="Travel dates & details..."></textarea>
                <button type="submit" class="btn-send">Send Inquiry to Hub</button>
            </form>
        </div>

        <div style="height: 300px; border-radius: 24px; overflow: hidden; margin: 40px 0 100px; border: 1px solid var(--border);">
            <iframe src="http://googleusercontent.com/maps.google.com/9" width="100%" height="100%" frameborder="0" style="filter: invert(90%) hue-rotate(180deg);"></iframe>
        </div>
    </div>

    <div class="app-bar">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-mountain-sun"></i></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </div>

    <script>
        // Live Clock Function
        function updateTime() {
            const now = new Date();
            document.getElementById('live-clock').innerText = now.toLocaleTimeString();
        }
        setInterval(updateTime, 1000);

        // Form Function
        document.getElementById('hubForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            const text = `*HUB INQUIRY*\nName: ${n}\nTour: ${t}\nSent from Astore Hub.`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
