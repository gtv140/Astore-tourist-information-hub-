<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Platinum | The Ultimate Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275); font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text); line-height: 1.6; overflow-x: hidden; }

        /* Animations */
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        .animate-card { animation: fadeInUp 0.8s ease forwards; opacity: 0; }

        .progress-bar { position: fixed; top: 0; z-index: 6000; height: 4px; background: var(--accent); width: 0%; }

        .ticker-bar { background: #b91c1c; color: white; padding: 10px; font-size: 0.8rem; overflow: hidden; position: sticky; top: 0; z-index: 5000; font-weight: bold; border-bottom: 2px solid var(--accent); }
        .ticker-text { display: inline-block; white-space: nowrap; animation: move 25s linear infinite; }
        @keyframes move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        nav { background: var(--card); padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 38px; z-index: 4500; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 900; color: var(--primary); font-size: 1.2rem; text-decoration: none; }

        .float-controls { position: fixed; top: 120px; right: 15px; z-index: 5500; display: flex; flex-direction: column; gap: 10px; }
        .circle-btn { width: 45px; height: 45px; border-radius: 50%; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; border: none; cursor: pointer; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }

        .hero { height: 45vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }

        .container { max-width: 500px; margin: 0 auto; padding: 25px 15px; }
        .card { background: var(--card); padding: 22px; border-radius: 24px; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); }
        
        /* Map & Gallery */
        .map-frame { width: 100%; height: 200px; border-radius: 15px; border: none; margin-top: 15px; }
        .gallery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 15px; }
        .gallery-img { width: 100%; height: 100px; object-fit: cover; border-radius: 12px; }

        /* FAQ */
        .faq-item { border-bottom: 1px solid #f1f5f9; padding: 10px 0; cursor: pointer; }
        .faq-ans { display: none; font-size: 0.85rem; color: #64748b; padding-top: 5px; }

        .btn-wa { background: #25d366; color: white; padding: 18px; border-radius: 16px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: 800; font-size: 1.1rem; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #ef4444; color: white; padding: 14px; border-radius: 14px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: bold; margin-bottom: 20px; font-size: 0.9rem; }

        input, select { width: 100%; padding: 14px; border-radius: 14px; border: 1px solid #e2e8f0; margin-bottom: 15px; background: #f8fafc; color: #1e293b; outline: none; }

        footer { text-align: center; padding: 40px 20px 100px; opacity: 0.6; font-size: 0.75rem; border-top: 1px solid #eee; }
    </style>
</head>
<body id="master-body">

<div class="progress-bar" id="pBar"></div>

<div class="ticker-bar">
    <div class="ticker-text" id="ticker-data">
        🚀 2026 SEASON: Road to Minimarg & Rama is CLEAR. | 4x4 Jeep Discounts Active. | Use SOS for Emergency. | Contact: +92 317 1588489
    </div>
</div>

<nav>
    <a href="#" class="logo">ASTORE HUB PRO</a>
    <div id="clock" style="font-size: 0.75rem; font-weight: bold; color: var(--primary);">00:00:00</div>
</nav>

<div class="float-controls">
    <button class="circle-btn" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <button class="circle-btn" onclick="toggleLang()"><b id="l-ind">UR</b></button>
</div>

<header class="hero">
    <h1 id="hero-h1">Visit Astore Valley</h1>
    <p id="hero-p">Experience the Majesty of Nanga Parbat</p>
</header>

<div class="container">
    
    <a href="tel:+923171588489" class="sos-btn animate-card" style="animation-delay: 0.1s;">
        <i class="fas fa-phone-alt"></i> EMERGENCY SOS SUPPORT
    </a>

    <div class="card animate-card" style="animation-delay: 0.2s;">
        <h3 id="hist-h3"><i class="fas fa-history"></i> History of Astore</h3>
        <p id="hist-p" style="font-size: 0.85rem; margin-top:10px; text-align: justify;">Astore is a historic gateway linking Gilgit to Kashmir. Known for its brave people and stunning landscapes like Rama Meadows and Rainbow Lake, it is the oldest district of the region.</p>
    </div>

    <div class="card animate-card" style="animation-delay: 0.3s;">
        <h3 id="calc-h3">Trip Calculator</h3>
        <select onchange="calcTrip(this.value)">
            <option value="">Choose City...</option>
            <option value="490">Islamabad</option>
            <option value="850">Lahore</option>
            <option value="110">Gilgit</option>
        </select>
        <div id="trip-res" style="font-weight:bold; color:var(--primary); font-size:0.85rem; text-align: center;"></div>
    </div>

    <div class="card animate-card" style="animation-delay: 0.4s;">
        <h3 id="map-h3">Our Location</h3>
        <iframe class="map-frame" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d104543.123456789!2d74.8!3d35.3!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e6e!2sAstore!5e0!3m2!1sen!2spk!4v1" allowfullscreen="" loading="lazy"></iframe>
    </div>

    <div class="card animate-card" style="animation-delay: 0.5s;">
        <h3 id="faq-h3">Common Questions</h3>
        <div class="faq-item" onclick="toggleFaq(1)">
            <b>Do I need an NOC?</b>
            <div class="faq-ans" id="f1">For Minimarg, yes. We help you process it at the Chilum checkpost with your original CNIC.</div>
        </div>
        <div class="faq-item" onclick="toggleFaq(2)">
            <b>Best time for Rama?</b>
            <div class="faq-ans" id="f2">June to August is perfect for greenery and flowers.</div>
        </div>
    </div>

    <a href="https://wa.me/923171588489" class="btn-wa animate-card" style="animation-delay: 0.6s;">
        <i class="fab fa-whatsapp"></i> <span id="wa-btn">BOOK JEEP ON WHATSAPP</span>
    </a>

</div>

<footer>
    <p>© 2026 Official Astore Tourist Portal</p>
    <p>Developing Astore, One Click at a Time</p>
</footer>

<script>
    window.onscroll = () => {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
        let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        document.getElementById("pBar").style.width = (winScroll / height) * 100 + "%";
    };
    setInterval(() => { document.getElementById('clock').innerText = new Date().toLocaleTimeString(); }, 1000);

    function calcTrip(km) {
        if(!km) return;
        const drive = Math.round(km / 45);
        document.getElementById('trip-res').innerHTML = `📍 Distance: ${km} KM | 🚗 Drive: ${drive} Hours approx.`;
    }

    function toggleFaq(id) {
        const el = document.getElementById('f'+id);
        el.style.display = (el.style.display === 'block') ? 'none' : 'block';
    }

    let isUr = false;
    function toggleLang() {
        isUr = !isUr;
        const content = {
            ur: { h1: "وادئ استور کی سیر", p: "نانگا پربت کی خوبصورتی کا تجربہ کریں", hist: "استور کی تاریخ", wa: "واٹس ایپ پر رابطہ کریں", ind: "EN", tick: "تازہ ترین: استور اور راما کے راستے کھلے ہیں۔ | جیپ بکنگ پر رعایت دستیاب ہے۔" },
            en: { h1: "Visit Astore Valley", p: "Experience the Majesty of Nanga Parbat", hist: "History of Astore", wa: "BOOK JEEP ON WHATSAPP", ind: "UR", tick: "🚀 2026 SEASON: Road to Minimarg & Rama is CLEAR. | 4x4 Jeep Discounts Active." }
        };
        const active = isUr ? content.ur : content.en;
        document.getElementById('hero-h1').innerText = active.h1;
        document.getElementById('hero-p').innerText = active.p;
        document.getElementById('hist-h3').innerText = active.hist;
        document.getElementById('wa-btn').innerText = active.wa;
        document.getElementById('l-ind').innerText = active.ind;
        document.getElementById('ticker-data').innerText = active.tick;
        document.body.style.direction = isUr ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
