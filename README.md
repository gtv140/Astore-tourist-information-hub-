<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Premium Hub | Explore Gilgit-Baltistan</title>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Outfit:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --neon: #00eaff;
            --neon-secondary: #7000ff;
            --bg: #030712;
            --card-bg: rgba(17, 24, 39, 0.7);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        body { font-family: 'Outfit', sans-serif; background: var(--bg); color: #f3f4f6; overflow-x: hidden; line-height: 1.6; }

        /* Animated Background Particles Effect */
        body::after {
            content: ""; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #111827 0%, #030712 100%);
            z-index: -2;
        }

        .container { max-width: 800px; margin: 20px auto; padding: 15px; padding-bottom: 120px; }

        /* Ultra Modern Header */
        header { text-align: center; padding: 40px 0; animation: fadeInDown 1s ease; }
        .logo { font-family: 'Syncopate', sans-serif; font-size: 32px; font-weight: 700; color: #fff; text-transform: uppercase; letter-spacing: 5px; text-shadow: 0 0 20px var(--neon); }
        .logo span { color: var(--neon); }
        .status-badge { display: inline-block; padding: 5px 15px; background: rgba(0, 234, 255, 0.1); border: 1px solid var(--neon); border-radius: 50px; font-size: 10px; text-transform: uppercase; letter-spacing: 2px; color: var(--neon); margin-top: 10px; }

        /* Glassmorphism Cards */
        .glass-card { background: var(--card-bg); backdrop-filter: blur(12px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 24px; padding: 25px; margin-bottom: 30px; box-shadow: 0 20px 50px rgba(0,0,0,0.5); transition: 0.4s; }
        .glass-card:hover { border-color: var(--neon); transform: translateY(-5px); }

        /* Hero Slider */
        .slider-box { position: relative; border-radius: 24px; overflow: hidden; height: 250px; margin-bottom: 30px; border: 1px solid rgba(255,255,255,0.1); }
        .slides { display: flex; height: 100%; transition: 0.8s cubic-bezier(0.4, 0, 0.2, 1); }
        .slides img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .slider-content { position: absolute; bottom: 20px; left: 20px; text-shadow: 0 2px 10px #000; }

        /* Form Inputs Modern */
        h2 { font-size: 18px; text-transform: uppercase; letter-spacing: 2px; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; color: var(--neon); }
        .input-group { margin-bottom: 15px; }
        input, select { width: 100%; padding: 14px 18px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 14px; color: #fff; outline: none; transition: 0.3s; }
        input:focus { border-color: var(--neon); background: rgba(255,255,255,0.1); box-shadow: 0 0 15px rgba(0,234,255,0.2); }

        /* Futuristic Button */
        .btn-glow { width: 100%; padding: 16px; background: linear-gradient(45deg, var(--neon), #00a2ff); border: none; border-radius: 14px; color: #000; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; cursor: pointer; transition: 0.4s; display: flex; align-items: center; justify-content: center; gap: 10px; }
        .btn-glow:hover { box-shadow: 0 0 30px rgba(0, 234, 255, 0.6); transform: scale(1.02); }

        /* Floating Nav Bar */
        .nav-hub { position: fixed; bottom: 25px; left: 50%; transform: translateX(-50%); width: 90%; max-width: 400px; background: rgba(15, 23, 42, 0.8); backdrop-filter: blur(20px); padding: 15px 25px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.1); display: flex; justify-content: space-between; align-items: center; z-index: 1000; box-shadow: 0 10px 40px rgba(0,0,0,0.8); }
        .nav-link { color: #94a3b8; text-decoration: none; font-size: 20px; transition: 0.3s; cursor: pointer; }
        .nav-link:hover, .nav-link.active { color: var(--neon); transform: translateY(-5px); }

        /* Notification Toast */
        .toast { position: fixed; top: 20px; right: 20px; background: var(--neon); color: #000; padding: 12px 25px; border-radius: 12px; font-weight: 600; display: none; animation: slideInRight 0.5s; z-index: 2000; }

        @keyframes fadeInDown { from { opacity: 0; transform: translateY(-30px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes slideInRight { from { transform: translateX(100%); } to { transform: translateX(0); } }

        /* Map Dark Mode */
        .map-container iframe { width: 100%; height: 200px; border-radius: 20px; filter: invert(90%) hue-rotate(180deg) opacity(0.8); }
    </style>
</head>
<body>

<div id="toast" class="toast">Booking Saved Locally!</div>

<div class="container">
    <header>
        <h1 class="logo">ASTORE<span>HUB</span></h1>
        <div class="status-badge">● Open For Bookings 2026</div>
    </header>

    <div class="slider-box">
        <div class="slides" id="slideRow">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=800&q=80" alt="Astore">
            <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&fit=crop&w=800&q=80" alt="Rama">
        </div>
        <div class="slider-content">
            <h3 id="slideTitle">Rama Meadows</h3>
            <p style="font-size: 12px; color: var(--neon);">Nature's Best Kept Secret</p>
        </div>
    </div>

    <section id="rooms" class="glass-card">
        <h2><i class="fa-solid fa-hotel"></i> Stay with Us</h2>
        <form id="roomForm">
            <div class="input-group"><input type="text" id="rname" placeholder="Guest Name" required></div>
            <div class="input-group"><input type="tel" id="rphone" placeholder="WhatsApp Number" required></div>
            <div style="display:flex; gap:10px; margin-bottom:15px;">
                <input type="date" id="rcheckin" required>
                <input type="date" id="rcheckout" required>
            </div>
            <select id="rtype" style="margin-bottom:15px;">
                <option value="Standard (PKR 3,500)">Standard - Economy</option>
                <option value="Luxury (PKR 7,500)">Luxury - View Facing</option>
                <option value="Family Suite (PKR 12,000)">Family Grand Suite</option>
            </select>
            <button type="submit" class="btn-glow"><i class="fa-brands fa-whatsapp"></i> Book Room</button>
        </form>
    </section>

    <section id="cars" class="glass-card">
        <h2><i class="fa-solid fa-jeep"></i> Adventure Rides</h2>
        <form id="carForm">
            <div class="input-group"><input type="text" id="cname" placeholder="Full Name" required></div>
            <select id="ctype" style="margin-bottom:15px;">
                <option value="Jeep 4x4 (Deosai Special)">Toyota TZ/Prado (4x4)</option>
                <option value="Local Corolla">Sedan (Corolla/Civic)</option>
                <option value="Grand Cabin">Hiace (12 Seater)</option>
            </select>
            <button type="submit" class="btn-glow" style="background: linear-gradient(45deg, #7000ff, #00eaff); color: #fff;">
                <i class="fa-solid fa-car-side"></i> Request Quote
            </button>
        </form>
    </section>

    <section id="map" class="glass-card">
        <h2><i class="fa-solid fa-location-arrow"></i> Headquarters</h2>
        <div class="map-container">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d104524.34145616654!2d74.78168249726563!3d35.33481230000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5df988950d73d%3A0xc07f60756a147814!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v171588489!5m2!1sen!2spk"></iframe>
        </div>
        <div style="margin-top:20px; display:flex; justify-content:space-around;">
            <a href="https://wa.me/923171588489" class="nav-link" style="font-size:30px; color:#25d366;"><i class="fa-brands fa-whatsapp"></i></a>
            <a href="https://www.facebook.com/share/1BoG9YCsZN/" class="nav-link" style="font-size:30px; color:#1877f2;"><i class="fa-brands fa-facebook"></i></a>
            <a href="mailto:mohammadasimkhan2746@gmail.com" class="nav-link" style="font-size:30px; color:#ea4335;"><i class="fa-solid fa-envelope"></i></a>
        </div>
    </section>

    <section id="history" class="glass-card" style="border-left: 4px solid var(--neon);">
        <h2><i class="fa-solid fa-receipt"></i> Recent Activity</h2>
        <div id="activityLog" style="font-size: 13px; color: #94a3b8;">No recent bookings.</div>
    </section>
</div>

<nav class="nav-hub">
    <a onclick="scrollToSection('rooms')" class="nav-link"><i class="fa-solid fa-bed"></i></a>
    <a onclick="scrollToSection('cars')" class="nav-link"><i class="fa-solid fa-car"></i></a>
    <div style="height:40px; width:1px; background:rgba(255,255,255,0.1);"></div>
    <a onclick="scrollToSection('map')" class="nav-link"><i class="fa-solid fa-compass"></i></a>
    <a onclick="scrollToSection('history')" class="nav-link"><i class="fa-solid fa-history"></i></a>
</nav>

<script>
    // Intelligent Slider
    const slideRow = document.getElementById('slideRow');
    const titles = ["Rama Meadows", "Deosai Plains", "Astore Valley"];
    let step = 0;

    setInterval(() => {
        step = (step + 1) % 2;
        slideRow.style.transform = `translateX(-${step * 100}%)`;
        document.getElementById('slideTitle').innerText = titles[step];
    }, 5000);

    // Dynamic WhatsApp Logic
    const PHONE = "923171588489";

    function handleBooking(e, type) {
        e.preventDefault();
        const toast = document.getElementById('toast');
        let msg = `*NEW BOOKING: ${type}*\n---\n`;
        
        const formData = new FormData(e.target);
        let logData = { type: type, time: new Date().toLocaleTimeString() };

        for (let [key, value] of formData.entries()) {
            msg += `*${key.replace('r','').replace('c','').toUpperCase()}:* ${value}\n`;
        }

        // WhatsApp Redirect
        window.open(`https://wa.me/${PHONE}?text=${encodeURIComponent(msg)}`, '_blank');

        // Save to History
        saveToHistory(type);
        
        // Show Success Toast
        toast.style.display = "block";
        setTimeout(() => toast.style.display = "none", 3000);
        e.target.reset();
    }

    document.getElementById('roomForm').onsubmit = (e) => handleBooking(e, 'HOTEL STAY');
    document.getElementById('carForm').onsubmit = (e) => handleBooking(e, 'CAR RENTAL');

    function saveToHistory(type) {
        let logs = JSON.parse(localStorage.getItem('astore_logs')) || [];
        logs.unshift(`${type} requested at ${new Date().toLocaleString()}`);
        localStorage.setItem('astore_logs', JSON.stringify(logs.slice(0,3)));
        updateLogUI();
    }

    function updateLogUI() {
        const logBox = document.getElementById('activityLog');
        let logs = JSON.parse(localStorage.getItem('astore_logs')) || [];
        if(logs.length > 0) {
            logBox.innerHTML = logs.map(l => `<div style="margin-bottom:8px; padding-bottom:5px; border-bottom:1px solid rgba(255,255,255,0.05);">📅 ${l}</div>`).join('');
        }
    }

    function scrollToSection(id) {
        document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    }

    window.onload = updateLogUI;
</script>

</body>
</html>
