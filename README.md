<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Platinum | Complete Travel Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; transition: 0.4s ease; font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text); line-height: 1.6; overflow-x: hidden; }

        /* Progress & Ticker */
        .progress-bar { position: fixed; top: 0; z-index: 6000; height: 4px; background: var(--accent); width: 0%; }
        .ticker-bar { background: #b91c1c; color: white; padding: 10px; font-size: 0.8rem; overflow: hidden; position: sticky; top: 0; z-index: 5000; font-weight: bold; border-bottom: 2px solid var(--accent); }
        .ticker-text { display: inline-block; white-space: nowrap; animation: move 25s linear infinite; }
        @keyframes move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        nav { background: var(--card); padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 38px; z-index: 4500; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 900; color: var(--primary); font-size: 1.2rem; text-decoration: none; }

        .float-controls { position: fixed; top: 120px; right: 15px; z-index: 5500; display: flex; flex-direction: column; gap: 10px; }
        .circle-btn { width: 45px; height: 45px; border-radius: 50%; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; border: none; cursor: pointer; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }

        .hero { height: 40vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }

        .container { max-width: 500px; margin: 0 auto; padding: 25px 15px; }
        .card { background: var(--card); padding: 22px; border-radius: 24px; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); }
        
        /* Travel List Decor */
        .spot-item { border-left: 4px solid var(--primary); padding-left: 15px; margin: 15px 0; }
        .spot-item h4 { color: var(--primary); margin-bottom: 5px; }
        .spot-item p { font-size: 0.85rem; color: #64748b; }

        .btn-wa { background: #25d366; color: white; padding: 18px; border-radius: 16px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: 800; font-size: 1.1rem; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }
        .sos-btn { background: #ef4444; color: white; padding: 14px; border-radius: 14px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: bold; margin-bottom: 20px; font-size: 0.9rem; }

        footer { text-align: center; padding: 40px 20px 100px; opacity: 0.6; font-size: 0.75rem; border-top: 1px solid #eee; }
    </style>
</head>
<body id="master-body">

<div class="progress-bar" id="pBar"></div>

<div class="ticker-bar">
    <div class="ticker-text" id="ticker-data">
        ⛰️ TRAVEL ADVISORY: Rama Meadows road is fully accessible. | Original CNIC is a MUST for Minimarg. | Group tours starting from Rs. 5000/head. | WhatsApp: +92 317 1588489
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
    <h1 id="hero-h1">Astore: The Hidden Gem</h1>
    <p id="hero-p">Your Complete Guide to Nature's Paradise</p>
</header>

<div class="container">
    
    <a href="tel:+923171588489" class="sos-btn">
        <i class="fas fa-phone-alt"></i> EMERGENCY SOS SUPPORT
    </a>

    <div class="card">
        <h3 id="spots-h3"><i class="fas fa-map-marked-alt"></i> Top Tourist Spots</h3>
        
        <div class="spot-item">
            <h4 id="s1-h">1. Minimarg & Rainbow Lake</h4>
            <p id="s1-p">Located near the Line of Control, this is a dreamland accessible via Burzil Pass (13,800 ft). Its lush green meadows and the multi-colored Rainbow Lake are world-famous.</p>
        </div>

        <div class="spot-item">
            <h4 id="s2-h">2. Rama Meadows & Lake</h4>
            <p id="s2-p">Just 11km from Astore city, Rama is a pine-forested heaven. The Rama Lake offers a breathtaking view of the eastern face of Nanga Parbat.</p>
        </div>

        <div class="spot-item">
            <h4 id="s3-h">3. Deosai Plains (Astore Side)</h4>
            <p id="s3-p">The "Land of Giants" is the second-highest plateau in the world. Entering from Astore gives you a unique view of the Sheosar Lake.</p>
        </div>

        <div class="spot-item">
            <h4 id="s4-h">4. Tarashing (Nanga Parbat Base)</h4>
            <p id="s4-p">The starting point for Rupal face trekkers. Tarashing is a beautiful village where you can touch the glaciers of the 9th highest mountain on Earth.</p>
        </div>
    </div>

    <div class="card">
        <h3 id="hist-h3"><i class="fas fa-history"></i> Rich History</h3>
        <p id="hist-p" style="font-size: 0.85rem; margin-top:10px; text-align: justify;">Astore has been a central administrative hub since the British Raj. It served as the main supply route to Gilgit for centuries. The people of Astore are known for their bravery, hospitality, and deep-rooted Shina culture.</p>
    </div>

    <div class="card">
        <h3 id="map-h3">Live Map Guide</h3>
        <iframe src="http://googleusercontent.com/maps.google.com/3" style="width:100%; height:180px; border-radius:15px; border:none; margin-top:10px;" allowfullscreen="" loading="lazy"></iframe>
    </div>

    <a href="https://wa.me/923171588489" class="btn-wa">
        <i class="fab fa-whatsapp"></i> <span id="wa-btn">BOOK YOUR ADVENTURE</span>
    </a>

</div>

<footer>
    <p>© 2026 Official Astore Tourist Information Hub</p>
    <p>Providing Authentic Information Since 2022</p>
</footer>

<script>
    window.onscroll = () => {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
        let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        document.getElementById("pBar").style.width = (winScroll / height) * 100 + "%";
    };
    setInterval(() => { document.getElementById('clock').innerText = new Date().toLocaleTimeString(); }, 1000);

    let isUr = false;
    function toggleLang() {
        isUr = !isUr;
        const content = {
            ur: { 
                h1: "استور: چھپا ہوا ہیرا", p: "فطرت کی جنت کے لیے آپ کی مکمل گائیڈ", 
                spots: "مشہور سیاحتی مقامات",
                s1h: "1. منی مرگ اور رینبو لیک", s1p: "برزل پاس کے قریب واقع یہ جگہ اپنی ہریالی اور رنگ بدلتی جھیل کے لیے مشہور ہے۔",
                s2h: "2. راما میڈوز اور جھیل", s2p: "استور شہر سے 11 کلومیٹر دور، یہاں سے نانگا پربت کا خوبصورت منظر نظر آتا ہے۔",
                s3h: "3. دیوسائی (استور کی طرف سے)", s3p: "دنیا کی دوسری بلند ترین سطح مرتفع، جہاں سے شیوسر جھیل کا راستہ جاتا ہے۔",
                s4h: "4. تراشنگ (نانگا پربت بیس)", s4p: "گلیشیئرز اور پہاڑوں کے دامن میں واقع ایک خوبصورت گاؤں۔",
                histH: "تاریخی پس منظر", histP: "استور صدیوں سے گلگت کا انتظامی مرکز رہا ہے۔ یہاں کے لوگ اپنی بہادری اور مہمان نوازی کے لیے پہچانے جاتے ہیں۔",
                wa: "ابھی اپنا سفر بک کریں", ind: "EN" 
            },
            en: { 
                h1: "Astore: The Hidden Gem", p: "Your Complete Guide to Nature's Paradise", 
                spots: "Top Tourist Spots",
                s1h: "1. Minimarg & Rainbow Lake", s1p: "Dreamland accessible via Burzil Pass. Famous for lush green meadows.",
                s2h: "2. Rama Meadows & Lake", s2p: "11km from Astore city, offering a breathtaking view of Nanga Parbat.",
                s3h: "3. Deosai Plains (Astore Side)", s3p: "The second-highest plateau in the world, entry point to Sheosar Lake.",
                s4h: "4. Tarashing (Nanga Parbat Base)", s4p: "Start point for Rupal face trekkers and home to massive glaciers.",
                histH: "Rich History", histP: "Astore has been a central hub since the British Raj. Known for bravery and hospitality.",
                wa: "BOOK YOUR ADVENTURE", ind: "UR" 
            }
        };
        const active = isUr ? content.ur : content.en;
        document.getElementById('hero-h1').innerText = active.h1;
        document.getElementById('hero-p').innerText = active.p;
        document.getElementById('spots-h3').innerText = active.spots;
        document.getElementById('s1-h').innerText = active.s1h; document.getElementById('s1-p').innerText = active.s1p;
        document.getElementById('s2-h').innerText = active.s2h; document.getElementById('s2-p').innerText = active.s2p;
        document.getElementById('s3-h').innerText = active.s3h; document.getElementById('s3-p').innerText = active.s3p;
        document.getElementById('s4-h').innerText = active.s4h; document.getElementById('s4-p').innerText = active.s4p;
        document.getElementById('hist-h3').innerText = active.histH;
        document.getElementById('hist-p').innerText = active.histP;
        document.getElementById('wa-btn').innerText = active.wa;
        document.getElementById('l-ind').innerText = active.ind;
        document.body.style.direction = isUr ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
