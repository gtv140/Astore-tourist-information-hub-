<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Platinum | All-in-One Official Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; transition: 0.3s ease; font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text); line-height: 1.6; }

        /* 1. Progress Bar */
        .progress-container { position: fixed; top: 0; z-index: 6000; width: 100%; height: 4px; background: transparent; }
        .progress-bar { height: 4px; background: var(--accent); width: 0%; }

        /* 2. News Ticker */
        .ticker-bar { background: #b91c1c; color: white; padding: 10px; font-size: 0.8rem; overflow: hidden; position: sticky; top: 4px; z-index: 5000; font-weight: bold; border-bottom: 2px solid var(--accent); }
        .ticker-text { display: inline-block; white-space: nowrap; animation: move 25s linear infinite; }
        @keyframes move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        /* 3. Navigation */
        nav { background: var(--card); padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 42px; z-index: 4500; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 900; color: var(--primary); font-size: 1.2rem; text-decoration: none; }

        /* 4. Controls (Floating) */
        .float-controls { position: fixed; top: 120px; right: 15px; z-index: 5500; display: flex; flex-direction: column; gap: 10px; }
        .circle-btn { width: 45px; height: 45px; border-radius: 50%; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; border: none; cursor: pointer; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }

        /* 5. Hero */
        .hero { height: 45vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }
        .hero h1 { font-size: 2.5rem; letter-spacing: -1px; }

        /* 6. Main Container */
        .container { max-width: 500px; margin: 0 auto; padding: 25px 15px; }
        .card { background: var(--card); padding: 22px; border-radius: 24px; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); border: 1px solid rgba(0,0,0,0.03); }
        
        /* 7. Specific Feature Styles */
        .status-pill { display: inline-flex; align-items: center; gap: 6px; background: #dcfce7; color: #166534; padding: 6px 14px; border-radius: 50px; font-size: 0.7rem; font-weight: bold; margin-bottom: 15px; }
        .stars i { font-size: 1.8rem; color: #cbd5e1; cursor: pointer; margin: 0 5px; }
        .stars i.active { color: var(--accent); }
        .faq-item { border-bottom: 1px solid #f1f5f9; padding: 12px 0; cursor: pointer; }
        .faq-answer { display: none; font-size: 0.85rem; color: #64748b; padding-top: 8px; }
        .gallery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 15px; }
        .gallery-img { width: 100%; height: 130px; object-fit: cover; border-radius: 15px; border: 2px solid var(--white); }

        /* 8. Inputs & Buttons */
        input, select { width: 100%; padding: 14px; border-radius: 14px; border: 1px solid #e2e8f0; margin-bottom: 15px; background: #f8fafc; color: #1e293b; }
        .btn-wa { background: #25d366; color: white; padding: 18px; border-radius: 16px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: 800; font-size: 1.1rem; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #ef4444; color: white; padding: 14px; border-radius: 14px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: bold; margin-bottom: 20px; font-size: 0.9rem; }

        /* 9. Notification Pop-up */
        #live-toast { position: fixed; bottom: 90px; left: 15px; background: var(--card); padding: 12px 18px; border-radius: 15px; font-size: 0.8rem; border-left: 5px solid var(--primary); box-shadow: 0 10px 30px rgba(0,0,0,0.1); transform: translateX(-150%); transition: 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275); z-index: 6000; }

        footer { text-align: center; padding: 40px 20px 100px; opacity: 0.6; font-size: 0.75rem; border-top: 1px solid #eee; }
    </style>
</head>
<body id="master-body">

<div class="progress-container"><div class="progress-bar" id="pBar"></div></div>

<div class="ticker-bar">
    <div class="ticker-text" id="ticker-txt">
        🚀 2026 SEASON: Road to Minimarg & Rama is CLEAR. | Special 4x4 Jeep Discounts available. | Use SOS for Emergency. | Contact: +92 317 1588489
    </div>
</div>

<nav>
    <a href="#" class="logo">ASTORE HUB PRO</a>
    <div id="clock" style="font-size: 0.75rem; font-weight: bold; color: var(--primary);">00:00:00</div>
</nav>

<div class="float-controls">
    <button class="circle-btn" onclick="toggleTheme()"><i class="fas fa-adjust"></i></button>
    <button class="circle-btn" onclick="toggleLang()"><b id="l-ind">UR</b></button>
    <button class="circle-btn" style="background:#25d366" onclick="copySite()"><i class="fas fa-share-alt"></i></button>
</div>

<header class="hero">
    <div class="status-pill"><i class="fas fa-check-circle"></i> TOURISM SEASON ACTIVE</div>
    <h1 id="hero-h1">Visit Astore Valley</h1>
    <p id="hero-p">History, Nature, and Adventure Await</p>
</header>

<div class="container">
    
    <a href="tel:+923171588489" class="sos-btn">
        <i class="fas fa-phone-alt"></i> EMERGENCY SOS SUPPORT
    </a>

    <div class="card">
        <h3 id="hist-h3"><i class="fas fa-history"></i> Astore History</h3>
        <p id="hist-p" style="font-size: 0.9rem; margin-top:10px; text-align: justify;">Astore is a historic gateway linking Gilgit to Srinagar. Known as the oldest district, it features the majestic Nanga Parbat and the legendary Burzil Pass. It remains a vital hub of culture and bravery in the North.</p>
    </div>

    <div class="card">
        <h3><i class="fas fa-calculator"></i> Trip Planner</h3>
        <p style="font-size:0.75rem; margin-bottom:10px;">Estimate Distance & Per Head Cost:</p>
        <select onchange="planner(this.value)">
            <option value="">Choose City...</option>
            <option value="490">Islamabad</option>
            <option value="850">Lahore</option>
            <option value="110">Gilgit</option>
        </select>
        <input type="number" id="pCount" placeholder="Number of persons" oninput="calcPrice()">
        <div id="plan-res" style="font-weight:bold; color:var(--primary); font-size:0.9rem;"></div>
    </div>

    <div class="card">
        <h3 id="gall-h3">Travelers Gallery</h3>
        <div class="gallery-grid">
            <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=300" class="gallery-img">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833?q=80&w=300" class="gallery-img">
        </div>
    </div>

    <div class="card">
        <h3 id="faq-h3">Frequently Asked</h3>
        <div class="faq-item" onclick="faq(1)">
            <b>Required Documents?</b>
            <div class="faq-answer" id="f1">Original CNIC is mandatory for all checkposts (Chilum, Minimarg).</div>
        </div>
        <div class="faq-item" onclick="faq(2)">
            <b>Best Jeep for Deosai?</b>
            <div class="faq-answer" id="f2">Only 4x4 Prado or specialized Jeeps are recommended due to rocky terrain.</div>
        </div>
    </div>

    <div class="card" style="text-align:center;">
        <h3 id="rate-h3">Rate the Beauty</h3>
        <div class="stars" id="starBox">
            <i class="fas fa-star" onclick="rate(1)"></i>
            <i class="fas fa-star" onclick="rate(2)"></i>
            <i class="fas fa-star" onclick="rate(3)"></i>
            <i class="fas fa-star" onclick="rate(4)"></i>
            <i class="fas fa-star" onclick="rate(5)"></i>
        </div>
        <p id="star-t" style="font-size:0.7rem; color:var(--accent); margin-top:5px;">Help us promote Astore!</p>
    </div>

    <a href="https://wa.me/923171588489" class="btn-wa">
        <i class="fab fa-whatsapp"></i> <span id="wa-btn">BOOK YOUR JEEP NOW</span>
    </a>

</div>

<div id="live-toast"><b>Someone from Punjab</b> just booked a tour! 🏔️</div>

<footer>
    <p>© 2026 Official Astore Tourist Information Hub</p>
    <p>Empowering Local Tourism | +92 317 1588489</p>
</footer>

<script>
    // 1. Progress Bar & Clock
    window.onscroll = () => {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
        let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        document.getElementById("pBar").style.width = (winScroll / height) * 100 + "%";
    };
    setInterval(() => { document.getElementById('clock').innerText = new Date().toLocaleTimeString(); }, 1000);

    // 2. Planner & Budget Logic
    let dist = 0;
    function planner(v) { dist = v; calcPrice(); }
    function calcPrice() {
        const p = document.getElementById('pCount').value;
        const res = document.getElementById('plan-res');
        if(dist && p > 0) {
            let perHead = Math.round(14000 / p);
            res.innerHTML = `📍 Distance: ${dist} KM<br>💰 Minimarg Estimate: Rs. ${perHead}/head`;
        }
    }

    // 3. Theme & Lang
    function toggleTheme() { document.body.classList.toggle('dark'); }
    let lang = 'en';
    const content = {
        ur: { h1: "وادئ استور", p: "تاریخ، فطرت اور ایڈونچر آپ کا منتظر ہے", histH: "استور کی تاریخ", histP: "استور ایک تاریخی راستہ ہے جو قدیم برزل پاس کے ذریعے گلگت کو کشمیر سے جوڑتا ہے۔ نانگا پربت کے دامن میں واقع یہ وادی اپنی خوبصورتی کے لیے مشہور ہے۔", wa: "ابھی جیپ بک کریں", lInd: "EN", tick: "تازہ ترین: استور اور راما کے راستے کھلے ہیں۔ | جیپ بکنگ پر رعایت دستیاب ہے۔ | رابطہ: +92 317 1588489" },
        en: { h1: "Visit Astore Valley", p: "History, Nature, and Adventure Await", histH: "Astore History", histP: "Astore is a historic gateway linking Gilgit to Srinagar. Known as the oldest district, it features the majestic Nanga Parbat and the legendary Burzil Pass.", wa: "BOOK YOUR JEEP NOW", lInd: "UR", tick: "🚀 2026 SEASON: Road to Minimarg & Rama is CLEAR. | Special 4x4 Jeep Discounts available. | Contact: +92 317 1588489" }
    };
    function toggleLang() {
        lang = (lang === 'en') ? 'ur' : 'en';
        document.getElementById('hero-h1').innerText = content[lang].h1;
        document.getElementById('hero-p').innerText = content[lang].p;
        document.getElementById('hist-h3').innerText = content[lang].histH;
        document.getElementById('hist-p').innerText = content[lang].histP;
        document.getElementById('wa-btn').innerText = content[lang].wa;
        document.getElementById('l-ind').innerText = content[lang].lInd;
        document.getElementById('ticker-txt').innerText = content[lang].tick;
        document.getElementById('master-body').style.direction = (lang === 'ur') ? 'rtl' : 'ltr';
    }

    // 4. Extra Interactive Features
    function faq(id) { let a = document.getElementById('f'+id); a.style.display = (a.style.display === 'block') ? 'none' : 'block'; }
    function rate(s) { document.querySelectorAll('#starBox i').forEach((x, i) => x.classList.toggle('active', i < s)); document.getElementById('star-t').innerText = "Thanks for " + s + " Stars!"; }
    function copySite() { navigator.clipboard.writeText(window.location.href); alert("Link Copied! Share it with friends, sweetie! 😘"); }
    
    // 5. Live Notification
    setTimeout(() => { document.getElementById('live-toast').style.transform = "translateX(0)"; setTimeout(() => { document.getElementById('live-toast').style.transform = "translateX(-150%)"; }, 5000); }, 3000);
</script>

</body>
</html>
