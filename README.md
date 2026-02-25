<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Platinum | Complete Encyclopedia & Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; transition: 0.4s ease; font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text); line-height: 1.6; overflow-x: hidden; }

        /* Tech Features */
        .progress-bar { position: fixed; top: 0; z-index: 6000; height: 5px; background: var(--accent); width: 0%; }
        .ticker-bar { background: #b91c1c; color: white; padding: 10px; font-size: 0.8rem; overflow: hidden; position: sticky; top: 0; z-index: 5000; font-weight: bold; border-bottom: 2px solid var(--accent); }
        .ticker-text { display: inline-block; white-space: nowrap; animation: move 25s linear infinite; }
        @keyframes move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        nav { background: var(--card); padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 38px; z-index: 4500; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 900; color: var(--primary); font-size: 1.2rem; text-decoration: none; }

        .float-controls { position: fixed; top: 120px; right: 15px; z-index: 5500; display: flex; flex-direction: column; gap: 10px; }
        .circle-btn { width: 45px; height: 45px; border-radius: 50%; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; border: none; cursor: pointer; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }

        .hero { height: 40vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }

        .container { max-width: 500px; margin: 0 auto; padding: 25px 15px; }
        .card { background: var(--card); padding: 22px; border-radius: 24px; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); border: 1px solid rgba(0,0,0,0.05); }
        
        /* Content Styling */
        h3 { color: var(--primary); margin-bottom: 15px; display: flex; align-items: center; gap: 10px; }
        .detail-box { border-left: 3px solid var(--accent); padding-left: 15px; margin-bottom: 20px; }
        .detail-box h4 { font-size: 1rem; margin-bottom: 5px; color: var(--text); }
        .detail-box p { font-size: 0.85rem; color: #64748b; }

        .check-list { list-style: none; font-size: 0.85rem; }
        .check-list li { margin-bottom: 8px; display: flex; align-items: center; gap: 10px; }
        .check-list i { color: #10b981; }

        .btn-wa { background: #25d366; color: white; padding: 18px; border-radius: 16px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: 800; font-size: 1.1rem; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #ef4444; color: white; padding: 14px; border-radius: 14px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: bold; margin-bottom: 20px; font-size: 0.9rem; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.02); } 100% { transform: scale(1); } }

        footer { text-align: center; padding: 40px 20px 100px; opacity: 0.6; font-size: 0.75rem; border-top: 1px solid #eee; }
    </style>
</head>
<body id="master-body">

<div class="progress-bar" id="pBar"></div>

<div class="ticker-bar">
    <div class="ticker-text" id="ticker-data">
        📢 UPDATED: All features added! | Minimarg Road: OPEN | Rama Lake: ACCESSIBLE | Deosai entry from Astore: OPEN | Special 4x4 Jeep deals for Feb-March 2026!
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
    <h1 id="hero-h1">Astore Encyclopedia</h1>
    <p id="hero-p">Every Detail You Need in One Place</p>
</header>

<div class="container">
    
    <a href="tel:+923171588489" class="sos-btn">
        <i class="fas fa-phone-alt"></i> EMERGENCY SOS SUPPORT
    </a>

    <div class="card">
        <h3 id="h-dest"><i class="fas fa-mountain"></i> Major Destinations</h3>
        
        <div class="detail-box">
            <h4 id="d1-t">Minimarg & Burzil Pass</h4>
            <p id="d1-d">Height: 13,800 ft. A high-security zone near the LOC. Famous for 'Rainbow Lake' and 'Domel'. Requires an NOC (Original CNIC) at Chilum check post.</p>
        </div>

        <div class="detail-box">
            <h4 id="d2-t">Rama Meadows & Lake</h4>
            <p id="d2-d">The 'Switzerland of Astore'. Surrounded by thick pine forests. Best for camping. The lake offers the clearest reflection of Nanga Parbat's Rupal Face.</p>
        </div>

        <div class="detail-box">
            <h4 id="d3-t">Tarashing Village</h4>
            <p id="d3-d">The gateway to the mighty Nanga Parbat. Here you can find the Rupal Glacier. It is the base camp for many international mountaineers.</p>
        </div>
    </div>

    <div class="card">
        <h3 id="h-check"><i class="fas fa-clipboard-check"></i> Essential Checklist</h3>
        <ul class="check-list" id="check-items">
            <li><i class="fas fa-check-circle"></i> Original CNIC (Mandatory for Checkposts)</li>
            <li><i class="fas fa-check-circle"></i> Warm Clothes (Even in Summer)</li>
            <li><i class="fas fa-check-circle"></i> Power Bank (Electricity can be limited)</li>
            <li><i class="fas fa-check-circle"></i> Basic First-Aid & Altitude Meds</li>
            <li><i class="fas fa-check-circle"></i> Cash (ATM's are rare in remote areas)</li>
        </ul>
    </div>

    <div class="card">
        <h3 id="h-reach"><i class="fas fa-car"></i> Getting There</h3>
        <p style="font-size: 0.85rem; margin-bottom:10px;">Distances from Major Hubs:</p>
        <div style="font-size: 0.8rem; background: #f1f5f9; padding: 10px; border-radius: 10px; color: #1e293b;">
            <b>Gilgit to Astore:</b> 110 KM (approx 3-4 hours)<br>
            <b>Islamabad to Astore:</b> 490 KM (approx 12-14 hours)<br>
            <b>Chilas to Astore:</b> 100 KM (via Karakoram Highway)
        </div>
    </div>

    <div class="card">
        <h3 id="h-map"><i class="fas fa-map-marked-alt"></i> Interactive Map</h3>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d105285.34110300451!2d74.7865261!3d35.3340033!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e6677f985923b3%3A0xe54930113c246f90!2sAstore!5e0!3m2!1sen!2s!4v1700000000000!5m2!1sen!2s" style="width:100%; height:200px; border-radius:15px; border:none;" allowfullscreen="" loading="lazy"></iframe>
    </div>

    <a href="https://wa.me/923171588489" class="btn-wa">
        <i class="fab fa-whatsapp"></i> <span id="wa-btn">BOOK 4x4 JEEP NOW</span>
    </a>

</div>

<footer>
    <p>© 2026 Official Astore Tourist Information Hub</p>
    <p>Everything you need for a perfect trip.</p>
</footer>

<script>
    // 1. Progress Bar Logic
    window.onscroll = () => {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
        let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        document.getElementById("pBar").style.width = (winScroll / height) * 100 + "%";
    };

    // 2. Real-time Clock
    setInterval(() => { 
        document.getElementById('clock').innerText = new Date().toLocaleTimeString(); 
    }, 1000);

    // 3. Language Translation Logic
    let isUr = false;
    function toggleLang() {
        isUr = !isUr;
        const content = {
            ur: { 
                h1: "استور انسائیکلوپیڈیا", p: "ہر تفصیل جو آپ کو جاننا ضروری ہے", 
                dest: "اہم سیاحتی مقامات",
                d1t: "منی مرگ اور برزل پاس", d1d: "اونچائی: 13,800 فٹ۔ یہ ایک حساس علاقہ ہے جہاں رینبو لیک واقع ہے۔ شناختی کارڈ لازمی ہے۔",
                d2t: "راما میڈوز اور جھیل", d2d: "استور کا سوئٹزرلینڈ۔ گھنے جنگلات اور نانگا پربت کے سائے میں ایک خوبصورت مقام۔",
                d3t: "تراشنگ گاؤں", d3d: "نانگا پربت کا گیٹ وے۔ یہاں سے دنیا کے نویں بلند ترین پہاڑ کا گلیشیئر شروع ہوتا ہے۔",
                check: "سفر کے لیے ضروری سامان",
                reach: "راستہ اور فاصلہ",
                map: "لائیو نقشہ گائیڈ",
                wa: "ابھی جیپ بک کریں", ind: "EN"
            },
            en: { 
                h1: "Astore Encyclopedia", p: "Every Detail You Need in One Place", 
                dest: "Major Destinations",
                d1t: "Minimarg & Burzil Pass", d1d: "Height: 13,800 ft. A high-security zone near the LOC. Famous for 'Rainbow Lake'. CNIC is required.",
                d2t: "Rama Meadows & Lake", d2d: "The 'Switzerland of Astore'. Surrounded by pine forests and Nanga Parbat views.",
                d3t: "Tarashing Village", d3d: "The gateway to Nanga Parbat and home to the massive Rupal Glacier.",
                check: "Essential Checklist",
                reach: "Getting There",
                map: "Interactive Map",
                wa: "BOOK 4x4 JEEP NOW", ind: "UR"
            }
        };
        const active = isUr ? content.ur : content.en;
        document.getElementById('hero-h1').innerText = active.h1;
        document.getElementById('hero-p').innerText = active.p;
        document.getElementById('h-dest').innerHTML = `<i class="fas fa-mountain"></i> ${active.dest}`;
        document.getElementById('d1-t').innerText = active.d1t; document.getElementById('d1-d').innerText = active.d1d;
        document.getElementById('d2-t').innerText = active.d2t; document.getElementById('d2-d').innerText = active.d2d;
        document.getElementById('d3-t').innerText = active.d3t; document.getElementById('d3-d').innerText = active.d3d;
        document.getElementById('h-check').innerHTML = `<i class="fas fa-clipboard-check"></i> ${active.check}`;
        document.getElementById('h-reach').innerHTML = `<i class="fas fa-car"></i> ${active.reach}`;
        document.getElementById('h-map').innerHTML = `<i class="fas fa-map-marked-alt"></i> ${active.map}`;
        document.getElementById('wa-btn').innerText = active.wa;
        document.getElementById('l-ind').innerText = active.ind;
        document.body.style.direction = isUr ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
