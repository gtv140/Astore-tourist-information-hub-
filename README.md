<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Modern Luxury Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; transition: background 0.3s, color 0.3s; }
        html { scroll-behavior: smooth; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; -webkit-font-smoothing: antialiased; }

        .p-bar { position: fixed; top: 0; z-index: 9999; height: 4px; background: linear-gradient(90deg, var(--accent), #fcd34d); width: 0%; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(12px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); border-bottom-color: rgba(255,255,255,0.05); }

        .hero { position: relative; height: 50vh; width: 92%; margin: 15px auto; border-radius: 35px; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.2); }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 30px; background: linear-gradient(transparent, rgba(0,0,0,0.9)); width: 100%; color: white; }
        .hero-overlay h1 { font-size: 2rem; font-weight: 800; line-height: 1.1; margin-bottom: 8px; }

        .container { padding: 0 20px 100px; }
        .card { background: var(--card); border-radius: 28px; padding: 25px; margin-bottom: 20px; box-shadow: 0 4px 20px rgba(0,0,0,0.03); border: 1px solid rgba(0,0,0,0.02); }
        .card h3 { font-size: 1.1rem; margin-bottom: 15px; display: flex; align-items: center; gap: 10px; color: var(--primary); }

        .spot-card { background: var(--bg); padding: 15px; border-radius: 20px; margin-bottom: 12px; }
        .spot-card b { display: block; color: var(--text); font-size: 0.95rem; }
        .spot-card span { font-size: 0.8rem; color: #64748b; }

        .update-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 15px; }
        .update-item { background: var(--bg); padding: 15px; border-radius: 20px; text-align: center; }
        .update-item i { font-size: 1.5rem; margin-bottom: 8px; display: block; color: var(--accent); }

        .btn { padding: 18px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; transition: 0.3s; margin-bottom: 10px; }
        .sos { background: #fee2e2; color: #ef4444; }
        .wa { background: #25d366; color: white; box-shadow: 0 10px 25px rgba(37,211,102,0.3); }

        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 55px; height: 55px; border-radius: 20px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); cursor: pointer; display: flex; align-items: center; justify-content: center; }

        .ticker { background: #ef4444; color: white; padding: 8px; font-size: 0.75rem; text-align: center; font-weight: 600; }
        footer { text-align: center; padding: 20px; opacity: 0.5; font-size: 0.7rem; }
        
        /* RTL support for icons */
        body[style*="rtl"] .card h3 i { margin-left: 10px; margin-right: 0; }
    </style>
</head>
<body id="master-body">

<div class="p-bar" id="pb"></div>

<div class="ticker">
    <marquee id="marquee">📍 2026 Season Open! | Minimarg: Road Clear | Rama: Accessible | WhatsApp: +92 317 1588489</marquee>
</div>

<header>
    <div style="font-weight: 900; letter-spacing: -1px; font-size: 1.1rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.75rem; font-weight: 700;">12:00 PM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800" class="hero-img" alt="Astore">
    <div class="hero-overlay">
        <span id="badge" style="background:var(--accent); color:black; padding:4px 10px; border-radius:10px; font-size:0.6rem; font-weight:900; text-transform:uppercase;">Luxury Portal</span>
        <h1 id="h1">The Swiss of Pakistan</h1>
        <p id="hp">Explore the untouched majesty of Astore Valley.</p>
    </div>
</section>

<div class="container">
    
    <a href="tel:+923171588489" class="btn sos">
        <i class="fas fa-phone-alt"></i> <span id="sos-text">24/7 EMERGENCY SOS</span>
    </a>

    <div class="card">
        <h3 id="uh"><i class="fas fa-bolt"></i> Live Status</h3>
        <div class="update-grid">
            <div class="update-item">
                <i class="fas fa-cloud-sun"></i>
                <b id="temp">14°C</b>
                <span id="tl">Astore Valley</span>
            </div>
            <div class="update-item">
                <i class="fas fa-road" style="color: #10b981;"></i>
                <b id="rs">Open</b>
                <span id="rl">Burzil Pass</span>
            </div>
        </div>
    </div>

    <div class="card">
        <h3 id="th"><i class="fas fa-map-marked-alt"></i> Top Destinations</h3>
        <div class="spot-card">
            <b id="s1">Minimarg & Rainbow Lake</b>
            <span id="d1">A fairytale land behind the Burzil Pass.</span>
        </div>
        <div class="spot-card">
            <b id="s2">Rama Meadows & Lake</b>
            <span id="d2">Lush greenery at the foot of Nanga Parbat.</span>
        </div>
    </div>

    <div class="card">
        <h3 id="ih"><i class="fas fa-info-circle"></i> Quick Details</h3>
        <p id="ip" style="font-size: 0.85rem; color: #64748b;">Astore is the gateway to Gilgit-Baltistan. Carry your original CNIC. Use <b>SCOM</b> for best signals, sweetie!</p>
    </div>

    <a href="https://wa.me/923171588489" class="btn wa">
        <i class="fab fa-whatsapp fa-lg"></i> <span id="wb">BOOK 4x4 JEEP NOW</span>
    </a>

</div>

<div class="controls">
    <button class="fab" id="mode-toggle" onclick="toggleDark()"><i class="fas fa-moon"></i></button>
    <button class="fab" onclick="toggleLang()"><b id="li">UR</b></button>
</div>

<footer>
    © 2026 ASTORE TOURIST INFORMATION HUB<br>MODERNIZED BY GEMINI
</footer>

<script>
    // Progress Bar
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    // Real-time Clock
    setInterval(() => { 
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'}); 
    }, 1000);

    // Dark Mode Toggle
    function toggleDark() {
        document.body.classList.toggle('dark');
        const icon = document.querySelector('#mode-toggle i');
        icon.classList.toggle('fa-moon');
        icon.classList.toggle('fa-sun');
    }

    // Language Toggle Logic
    let isU = false;
    function toggleLang() {
        isU = !isU;
        const c = {
            ur: { 
                h1: "پاکستان کا سوئٹزرلینڈ", hp: "استور کی خوبصورتی کا تجربہ کریں، سویٹی!", 
                th: "مشہور مقامات", s1: "منی مرگ اور رینبو جھیل", d1: "برزل پاس کے پار ایک جادوئی وادی", 
                s2: "راما میڈوز اور جھیل", d2: "نانگا پربت کے سائے میں ہریالی", 
                ih: "ضروری معلومات", ip: "استور میں چیک پوسٹس کے لیے اصل شناختی کارڈ لازمی ہے۔ بہترین نیٹ ورک کے لیے SCOM استعمال کریں، سویٹی!",
                uh: "تازہ ترین صورتحال", temp: "14°C", tl: "وادی استور", rs: "کھلا ہے", rl: "برزل پاس",
                sos: "24/7 ہنگامی مدد", wb: "جیپ بک کرنے کے لیے رابطہ کریں", li: "EN",
                m: "📍 2026 سیزن کھلا ہے! | منی مرگ: راستہ صاف ہے | راما: رسائی ممکن ہے | واٹس ایپ: 923171588489+"
            },
            en: { 
                h1: "The Swiss of Pakistan", hp: "Explore the untouched majesty of Astore Valley.", 
                th: "Top Destinations", s1: "Minimarg & Rainbow Lake", d1: "A fairytale land behind the Burzil Pass.", 
                s2: "Rama Meadows & Lake", d2: "Lush greenery at the foot of Nanga Parbat.", 
                ih: "Quick Details", ip: "Astore is the gateway to Gilgit-Baltistan. Carry your original CNIC. Use SCOM for best signals, sweetie!",
                uh: "Live Status", temp: "14°C", tl: "Astore Valley", rs: "Open", rl: "Burzil Pass",
                sos: "24/7 EMERGENCY SOS", wb: "BOOK 4x4 JEEP NOW", li: "UR",
                m: "📍 2026 Season Open! | Minimarg: Road Clear | Rama: Accessible | WhatsApp: +92 317 1588489"
            }
        };
        const a = isU ? c.ur : c.en;
        document.getElementById('h1').innerText = a.h1;
        document.getElementById('hp').innerText = a.hp;
        document.getElementById('th').innerHTML = `<i class="fas fa-map-marked-alt"></i> ${a.th}`;
        document.getElementById('s1').innerText = a.s1; document.getElementById('d1').innerText = a.d1;
        document.getElementById('s2').innerText = a.s2; document.getElementById('d2').innerText = a.d2;
        document.getElementById('ih').innerHTML = `<i class="fas fa-info-circle"></i> ${a.ih}`;
        document.getElementById('ip').innerHTML = a.ip;
        document.getElementById('uh').innerHTML = `<i class="fas fa-bolt"></i> ${a.uh}`;
        document.getElementById('temp').innerText = a.temp; document.getElementById('tl').innerText = a.tl;
        document.getElementById('rs').innerText = a.rs; document.getElementById('rl').innerText = a.rl;
        document.getElementById('sos-text').innerText = a.sos;
        document.getElementById('wb').innerText = a.wb;
        document.getElementById('li').innerText = a.li;
        document.getElementById('marquee').innerText = a.m;
        document.body.style.direction = isU ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
