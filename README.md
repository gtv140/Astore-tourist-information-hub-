<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Tourist Hub | Premium Travel</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root {
            --neon: #00eaff;
            --dark-bg: #050505;
            --glass: rgba(255, 255, 255, 0.05);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        body { font-family: 'Poppins', sans-serif; color: #fff; background: var(--dark-bg); overflow-x: hidden; }

        /* Background Animation */
        body::before {
            content: ""; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #111 0%, #000 100%);
            z-index: -1;
        }

        .container { max-width: 900px; margin: 40px auto; padding: 25px; background: var(--glass); border-radius: 30px; backdrop-filter: blur(15px); border: 1px solid rgba(0, 234, 255, 0.2); box-shadow: 0 0 40px rgba(0, 0, 0, 0.5); padding-bottom: 100px; }

        /* Modern Logo */
        .logo { text-align: center; font-family: 'Orbitron', sans-serif; font-size: clamp(24px, 5vw, 40px); background: linear-gradient(90deg, #00eaff, #00fff0); -webkit-background-clip: text; -webkit-text-fill-color: transparent; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 5px; }
        .hero-text { text-align: center; font-size: 14px; color: #888; margin-bottom: 30px; letter-spacing: 1px; }

        /* Advanced Slider */
        .slider { position: relative; border-radius: 20px; overflow: hidden; border: 1px solid var(--neon); box-shadow: 0 0 20px rgba(0, 234, 255, 0.3); }
        .slides { display: flex; transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1); }
        .slides img { width: 100%; flex-shrink: 0; filter: brightness(0.8); transition: 0.5s; }
        .slider-overlay { position: absolute; bottom: 20px; left: 20px; right: 20px; background: rgba(0,0,0,0.6); padding: 15px; border-radius: 10px; border-left: 4px solid var(--neon); backdrop-filter: blur(5px); }

        /* Form Styling */
        section { margin-top: 50px; }
        h2 { font-family: 'Orbitron', sans-serif; color: var(--neon); font-size: 20px; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; }
        h2::after { content: ""; height: 2px; flex: 1; background: linear-gradient(90deg, var(--neon), transparent); }

        form { display: grid; gap: 15px; }
        input, select, button { padding: 14px; border-radius: 12px; border: 1px solid rgba(0, 234, 255, 0.3); background: rgba(255,255,255,0.05); color: #fff; font-size: 14px; transition: 0.3s; }
        input:focus { border-color: var(--neon); box-shadow: 0 0 10px rgba(0, 234, 255, 0.2); outline: none; background: rgba(255,255,255,0.1); }
        
        button { background: var(--neon); color: #000; font-weight: 700; cursor: pointer; border: none; text-transform: uppercase; }
        button:hover { background: #fff; transform: translateY(-3px); box-shadow: 0 5px 15px var(--neon); }

        /* History Cards */
        #historyList { display: grid; gap: 10px; }
        .history-card { background: rgba(255,255,255,0.03); border-radius: 12px; padding: 15px; border-left: 5px solid var(--neon); animation: slideIn 0.5s ease-out; }
        @keyframes slideIn { from { opacity: 0; transform: translateX(-20px); } to { opacity: 1; transform: translateX(0); } }

        /* Bottom Menu Improvement */
        .icon-menu { position: fixed; bottom: 15px; left: 50%; transform: translateX(-50%); width: 90%; max-width: 500px; display: flex; justify-content: space-around; background: rgba(0,0,0,0.8); backdrop-filter: blur(10px); padding: 12px; border-radius: 20px; border: 1px solid var(--neon); z-index: 1000; }
        .icon-item { color: #fff; text-decoration: none; text-align: center; font-size: 10px; opacity: 0.7; transition: 0.3s; cursor: pointer; }
        .icon-item i { font-size: 20px; display: block; margin-bottom: 4px; color: var(--neon); }
        .icon-item:hover { opacity: 1; transform: translateY(-5px); }

        /* WhatsApp Float */
        .whatsapp-btn { position: fixed; bottom: 90px; right: 20px; background: #25d366; color: #fff; width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 28px; text-decoration: none; box-shadow: 0 0 20px #25d366; z-index: 999; }

        /* Ad Slider */
        .ads-container { display: flex; overflow-x: auto; gap: 15px; padding-bottom: 10px; scrollbar-width: none; }
        .ads-container img { height: 160px; border-radius: 15px; border: 1px solid var(--neon); }
    </style>
</head>
<body>

<div class="container">
    <h1 class="logo">ASTORE HUB</h1>
    <p class="hero-text">Exploring the Unexplored Peaks of Gilgit-Baltistan</p>

    <div class="slider">
        <div class="slides" id="mainSlides">
            <img src="https://picsum.photos/id/1015/800/400" alt="Mountain">
            <img src="https://picsum.photos/id/1025/800/400" alt="Lake">
            <img src="https://picsum.photos/id/1035/800/400" alt="Valley">
        </div>
        <div class="slider-overlay">
            <h3 id="sliderTitle">Astore Valley</h3>
            <p style="font-size: 12px;">Plan your next adventure with us.</p>
        </div>
    </div>

    <section id="room">
        <h2><i class="fa-solid fa-bed"></i> Room Booking</h2>
        <form id="roomForm">
            <input type="text" id="rname" placeholder="Full Name" required>
            <input type="tel" id="rphone" placeholder="WhatsApp Number" required>
            <div style="display: flex; gap: 10px;">
                <input type="date" id="rcheckin" required style="flex:1">
                <input type="date" id="rcheckout" required style="flex:1">
            </div>
            <select id="rtype" required>
                <option value="Standard">Standard Room - Rs. 3500/night</option>
                <option value="Luxury">Luxury Room - Rs. 7000/night</option>
                <option value="Family">Family Suite - Rs. 10000/night</option>
            </select>
            <button type="submit"><i class="fa-brands fa-whatsapp"></i> Reserve Now</button>
        </form>
    </section>

    <section id="car">
        <h2><i class="fa-solid fa-car"></i> Car Rental</h2>
        <form id="carForm">
            <input type="text" id="cname" placeholder="Full Name" required>
            <input type="tel" id="cphone" placeholder="WhatsApp Number" required>
            <input type="date" id="cdate" required>
            <select id="ctype" required>
                <option value="Jeep 4x4">Prado/Jeep (For Deosai) - Rs. 12000/day</option>
                <option value="Corolla">Corolla (Local City) - Rs. 5000/day</option>
                <option value="Hiace">Hiace (For Group) - Rs. 15000/day</option>
            </select>
            <button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Ride</button>
        </form>
    </section>

    <section id="packages">
        <h2><i class="fa-solid fa-map"></i> Top Packages</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;">
            <div style="background:var(--glass); padding:20px; border-radius:15px; border-top:3px solid var(--neon);">
                <h4>Rama Meadows</h4>
                <p style="font-size:12px; color:#aaa; margin-top:5px;">3 Days | Tour Guide | Meals</p>
                <p style="color:var(--neon); margin-top:10px; font-weight:700;">Rs. 15,000</p>
            </div>
            <div style="background:var(--glass); padding:20px; border-radius:15px; border-top:3px solid var(--neon);">
                <h4>Deosai Plains</h4>
                <p style="font-size:12px; color:#aaa; margin-top:5px;">Full Day Jeep Safari</p>
                <p style="color:var(--neon); margin-top:10px; font-weight:700;">Rs. 25,000</p>
            </div>
        </div>
    </section>

    <section id="map">
        <h2><i class="fa-solid fa-location-dot"></i> Our Location</h2>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d105263.15345759163!2d74.805562!3d35.341112!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e5d0f86235b2ef%3A0x7d00f94f92318023!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v1700000000000" 
        width="100%" height="250" style="border:0; border-radius:20px; filter: grayscale(1) invert(1);" allowfullscreen="" loading="lazy"></iframe>
    </section>

    <section id="history">
        <h2><i class="fa-solid fa-clock-rotate-left"></i> Your Bookings</h2>
        <div id="historyList">
            <p style="font-size:12px; color:#666;">No recent bookings found.</p>
        </div>
        <button onclick="clearHistory()" style="margin-top:10px; background:transparent; color:#ff4444; border:1px solid #ff4444; font-size:10px; padding:5px 10px;">Clear History</button>
    </section>

    <div style="text-align:center; padding:20px; font-size:12px; color:#555;">
        Designed for Astore Hub &copy; 2026
    </div>
</div>

<div class="icon-menu">
    <div class="icon-item" onclick="scrollToSection('room')"><i class="fa-solid fa-bed"></i>Rooms</div>
    <div class="icon-item" onclick="scrollToSection('car')"><i class="fa-solid fa-car"></i>Cars</div>
    <div class="icon-item" onclick="scrollToSection('packages')"><i class="fa-solid fa-mountain"></i>Tours</div>
    <div class="icon-item" onclick="scrollToSection('map')"><i class="fa-solid fa-map-pin"></i>Map</div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>

<script>
    // Slider Logic
    let currentSlide = 0;
    const slideTrack = document.getElementById('mainSlides');
    const totalSlides = slideTrack.children.length;

    function moveSlider() {
        currentSlide = (currentSlide + 1) % totalSlides;
        slideTrack.style.transform = `translateX(-${currentSlide * 100}%)`;
    }
    setInterval(moveSlider, 4000);

    // Form Handling
    const WHATSAPP_NUM = "923171588489";

    document.getElementById("roomForm").onsubmit = function(e) {
        e.preventDefault();
        const data = {
            type: "🏨 ROOM",
            name: document.getElementById("rname").value,
            phone: document.getElementById("rphone").value,
            checkin: document.getElementById("rcheckin").value,
            checkout: document.getElementById("rcheckout").value,
            option: document.getElementById("rtype").value
        };
        sendToWhatsApp(data);
    };

    document.getElementById("carForm").onsubmit = function(e) {
        e.preventDefault();
        const data = {
            type: "🚗 CAR",
            name: document.getElementById("cname").value,
            phone: document.getElementById("cphone").value,
            date: document.getElementById("cdate").value,
            option: document.getElementById("ctype").value
        };
        sendToWhatsApp(data);
    };

    function sendToWhatsApp(data) {
        let message = `*NEW BOOKING ALERT*\n------------------\n`;
        for (const [key, value] of Object.entries(data)) {
            message += `*${key.toUpperCase()}:* ${value}\n`;
        }
        
        window.open(`https://wa.me/${WHATSAPP_NUM}?text=${encodeURIComponent(message)}`, '_blank');
        
        saveHistory(data);
    }

    // LocalStorage History
    function saveHistory(item) {
        let history = JSON.parse(localStorage.getItem("astore_bookings")) || [];
        item.timestamp = new Date().toLocaleString();
        history.unshift(item);
        localStorage.setItem("astore_bookings", JSON.stringify(history.slice(0, 5))); // Keep last 5
        renderHistory();
    }

    function renderHistory() {
        const list = document.getElementById("historyList");
        const history = JSON.parse(localStorage.getItem("astore_bookings")) || [];
        
        if(history.length === 0) {
            list.innerHTML = `<p style="font-size:12px; color:#666;">No recent bookings.</p>`;
            return;
        }

        list.innerHTML = history.map(h => `
            <div class="history-card">
                <div style="display:flex; justify-content:space-between; font-size:10px; color:var(--neon); margin-bottom:5px;">
                    <span>${h.type}</span> <span>${h.timestamp}</span>
                </div>
                <div style="font-size:13px;">${h.option} for ${h.name}</div>
            </div>
        `).join('');
    }

    function clearHistory() {
        localStorage.removeItem("astore_bookings");
        renderHistory();
    }

    function scrollToSection(id) {
        document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    }

    // Initial Load
    renderHistory();
</script>

</body>
</html>
