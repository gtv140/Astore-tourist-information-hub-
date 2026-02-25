<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Modern Luxury Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f1f5f9; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #020617; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; -webkit-font-smoothing: antialiased; }

        /* Modern Progress Bar */
        .p-bar { position: fixed; top: 0; z-index: 9999; height: 4px; background: linear-gradient(90deg, var(--accent), #fcd34d); width: 0%; transition: 0.2s; }

        /* Sticky Glass Header */
        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.8); backdrop-filter: blur(12px); padding: 12px 20px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }
        .dark header { background: rgba(30,41,59,0.8); border-bottom-color: rgba(255,255,255,0.05); }

        /* Modern Hero Section */
        .hero { position: relative; height: 60vh; width: 92%; margin: 15px auto; border-radius: 35px; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.2); }
        .hero-img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }
        .hero-overlay { position: absolute; bottom: 0; left: 0; padding: 30px; background: linear-gradient(transparent, rgba(0,0,0,0.9)); width: 100%; color: white; }
        .hero-overlay h1 { font-size: 2.2rem; font-weight: 800; line-height: 1.1; margin-bottom: 8px; }
        .hero-overlay p { font-size: 0.9rem; opacity: 0.9; font-weight: 300; }

        /* Floating Minimal Controls */
        .controls { position: fixed; bottom: 30px; right: 20px; z-index: 9500; display: flex; flex-direction: column; gap: 12px; }
        .fab { width: 55px; height: 55px; border-radius: 20px; background: var(--primary); color: white; border: none; box-shadow: 0 10px 25px rgba(0,0,0,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.2rem; cursor: pointer; }
        .fab.dark-toggle { background: #334155; }

        /* Clean Card Layout */
        .container { padding: 0 20px 100px; }
        .card { background: var(--card); border-radius: 28px; padding: 25px; margin-bottom: 20px; box-shadow: 0 4px 20px rgba(0,0,0,0.03); border: 1px solid rgba(0,0,0,0.02); }
        .card h3 { font-size: 1.2rem; margin-bottom: 15px; display: flex; align-items: center; gap: 10px; color: var(--primary); }

        /* Detail List */
        .spot-card { background: var(--bg); padding: 15px; border-radius: 20px; margin-bottom: 12px; }
        .spot-card b { display: block; color: var(--text); font-size: 0.95rem; }
        .spot-card span { font-size: 0.8rem; color: #64748b; }

        /* Modern SOS & WA */
        .action-grid { display: grid; grid-template-columns: 1fr; gap: 15px; margin-top: 10px; }
        .btn { padding: 18px; border-radius: 20px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 10px; font-size: 1rem; transition: 0.3s; }
        .sos { background: #fee2e2; color: #ef4444; }
        .wa { background: #25d366; color: white; box-shadow: 0 10px 25px rgba(37,211,102,0.3); }

        .ticker { background: #ef4444; color: white; padding: 8px; font-size: 0.75rem; text-align: center; font-weight: 600; }

        footer { text-align: center; padding: 20px; opacity: 0.5; font-size: 0.7rem; }
    </style>
</head>
<body id="master-body">

<div class="p-bar" id="pb"></div>

<div class="ticker">
    <marquee>📍 2026 Season Open! | Minimarg: Road Clear | Rama: Accessible | WhatsApp for Jeep: +92 317 1588489</marquee>
</div>

<header>
    <div style="font-weight: 900; letter-spacing: -1px; font-size: 1.1rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.75rem; font-weight: 700;">10:27 AM</div>
</header>

<section class="hero">
    <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800" class="hero-img" alt="Astore">
    <div class="hero-overlay">
        <span style="background:var(--accent); color:black; padding:4px 10px; border-radius:10px; font-size:0.6rem; font-weight:900; text-transform:uppercase;">Luxury Portal</span>
        <h1 id="h1">The Swiss of Pakistan</h1>
        <p id="hp">Explore the untouched majesty of Astore Valley.</p>
    </div>
</section>

<div class="container">
    
    <div class="action-grid">
        <a href="tel:+923171588489" class="btn sos">
            <i class="fas fa-phone-alt"></i> 24/7 EMERGENCY SOS
        </a>
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
        <div class="spot-card">
            <b id="s3">Deosai Plains</b>
            <span id="d3">Entry to the world's second-highest plateau.</span>
        </div>
    </div>

    <div class="card">
        <h3 id="ih"><i class="fas fa-info-circle"></i> Quick Details</h3>
        <p id="ip" style="font-size: 0.85rem; color: #64748b;">Astore is the gateway to some of the most beautiful spots in Gilgit-Baltistan. Carry your original CNIC for all check-posts. 4x4 Jeeps are highly recommended for internal travel.</p>
    </div>

    <a href="https://wa.me/923171588489" class="btn wa">
        <i class="fab fa-whatsapp fa-lg"></i> <span id="wb">BOOK 4x4 JEEP NOW</span>
    </a>

</div>

<div class="controls">
    <button class="fab dark-toggle" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <button class="fab" onclick="toggleLang()"><b id="li">UR</b></button>
</div>

<footer>
    © 2026 ASTORE TOURIST INFORMATION HUB<br>MODERNIZED BY GEMINI
</footer>

<script>
    window.onscroll = () => {
        let s = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;
        document.getElementById('pb').style.width = s + '%';
    };

    setInterval(() => { document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'}); }, 1000);

    let isU = false;
    function toggleLang() {
        isU = !isU;
        const c = {
            ur: { h1: "پاکستان کا سوئٹزرلینڈ", hp: "استور کی خوبصورتی کا تجربہ کریں", th: "مشہور مقامات", s1: "منی مرگ اور رینبو لیک", d1: "برزل پاس کے پیچھے چھپا ایک جادوئی منظر", s2: "راما میڈوز اور جھیل", d2: "نانگا پربت کے دامن میں ہریالی کا قالین", s3: "دیوسائی کے میدان", d3: "دنیا کی دوسری بلند ترین سطحِ مرتفع کا راستہ", ih: "ضروری معلومات", ip: "استور گلگت بلتستان کا ایک اہم تاریخی ضلع ہے۔ چیک پوسٹس کے لیے اصل شناختی کارڈ ساتھ رکھنا لازمی ہے۔", wb: "جیپ بک کرنے کے لیے رابطہ کریں", li: "EN" },
            en: { h1: "The Swiss of Pakistan", hp: "Explore the untouched majesty of Astore Valley.", th: "Top Destinations", s1: "Minimarg & Rainbow Lake", d1: "A fairytale land behind the Burzil Pass.", s2: "Rama Meadows & Lake", d2: "Lush greenery at the foot of Nanga Parbat.", s3: "Deosai Plains", d3: "Entry to the world's second-highest plateau.", ih: "Quick Details", ip: "Astore is the gateway to some of the most beautiful spots. Carry your original CNIC for all check-posts.", wb: "BOOK 4x4 JEEP NOW", li: "UR" }
        };
        const a = isU ? c.ur : c.en;
        document.getElementById('h1').innerText = a.h1;
        document.getElementById('hp').innerText = a.hp;
        document.getElementById('th').innerHTML = `<i class="fas fa-map-marked-alt"></i> ${a.th}`;
        document.getElementById('s1').innerText = a.s1; document.getElementById('d1').innerText = a.d1;
        document.getElementById('s2').innerText = a.s2; document.getElementById('d2').innerText = a.d2;
        document.getElementById('s3').innerText = a.s3; document.getElementById('d3').innerText = a.d3;
        document.getElementById('ih').innerHTML = `<i class="fas fa-info-circle"></i> ${a.ih}`;
        document.getElementById('ip').innerText = a.ip;
        document.getElementById('wb').innerText = a.wb;
        document.getElementById('li').innerText = a.li;
        document.body.style.direction = isU ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
