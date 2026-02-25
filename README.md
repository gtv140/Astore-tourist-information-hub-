<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | The Ultimate Diamond Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #1e293b; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; transition: 0.4s ease; font-family: 'Inter', sans-serif; }
        body { background: var(--bg); color: var(--text); line-height: 1.6; overflow-x: hidden; }

        /* Progress & Ticker */
        .progress-bar { position: fixed; top: 0; z-index: 6000; height: 6px; background: linear-gradient(to right, var(--accent), #fbbf24); width: 0%; }
        .ticker-bar { background: #b91c1c; color: white; padding: 12px; font-size: 0.85rem; overflow: hidden; position: sticky; top: 0; z-index: 5000; font-weight: bold; box-shadow: 0 4px 10px rgba(0,0,0,0.2); }
        .ticker-text { display: inline-block; white-space: nowrap; animation: move 25s linear infinite; }
        @keyframes move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        nav { background: var(--card); padding: 18px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 40px; z-index: 4500; box-shadow: 0 2px 15px rgba(0,0,0,0.1); border-radius: 0 0 20px 20px; }
        .logo { font-weight: 900; color: var(--primary); font-size: 1.3rem; letter-spacing: -1px; }

        /* Floating Controls */
        .float-controls { position: fixed; top: 130px; right: 15px; z-index: 5500; display: flex; flex-direction: column; gap: 12px; }
        .circle-btn { width: 50px; height: 50px; border-radius: 50%; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; border: none; cursor: pointer; box-shadow: 0 8px 20px rgba(0,0,0,0.2); font-size: 1.2rem; }

        .hero { height: 50vh; background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1200'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; clip-path: ellipse(150% 100% at 50% 0%); }
        .hero h1 { font-size: 2.8rem; font-weight: 900; text-shadow: 2px 2px 10px rgba(0,0,0,0.5); }

        .container { max-width: 550px; margin: 0 auto; padding: 30px 15px; }
        .card { background: var(--card); padding: 25px; border-radius: 30px; margin-bottom: 30px; box-shadow: 0 15px 35px rgba(0,0,0,0.05); border: 1px solid rgba(0,0,0,0.02); overflow: hidden; position: relative; }
        
        /* Attractive Detail Badges */
        .badge { display: inline-block; padding: 4px 12px; border-radius: 50px; font-size: 0.7rem; font-weight: bold; background: #f1f5f9; color: var(--primary); margin-bottom: 10px; text-transform: uppercase; }
        .detail-card h3 { font-size: 1.4rem; color: var(--primary); margin-bottom: 15px; border-bottom: 2px solid #f1f5f9; padding-bottom: 10px; }
        
        .spot-guide { margin-bottom: 20px; }
        .spot-guide h4 { font-size: 1.1rem; display: flex; align-items: center; gap: 8px; color: var(--text); }
        .spot-guide p { font-size: 0.9rem; color: #64748b; margin-top: 5px; }

        /* Weather Section */
        .weather-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 15px; }
        .weather-box { background: #f8fafc; padding: 15px; border-radius: 20px; text-align: center; border: 1px solid #e2e8f0; }
        .weather-box i { font-size: 1.5rem; color: var(--accent); margin-bottom: 5px; }

        .btn-wa { background: #25d366; color: white; padding: 20px; border-radius: 20px; display: flex; align-items: center; justify-content: center; gap: 12px; text-decoration: none; font-weight: 900; font-size: 1.2rem; box-shadow: 0 15px 30px rgba(37,211,102,0.4); transform: translateY(0); }
        .btn-wa:active { transform: scale(0.95); }

        .sos-btn { background: #ef4444; color: white; padding: 15px; border-radius: 20px; display: flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; font-weight: bold; margin-bottom: 25px; box-shadow: 0 10px 20px rgba(239,68,68,0.3); }

        footer { text-align: center; padding: 50px 20px 120px; opacity: 0.6; font-size: 0.8rem; }
    </style>
</head>
<body id="master-body">

<div class="progress-bar" id="pBar"></div>

<div class="ticker-bar">
    <div class="ticker-text" id="ticker-data">
        ✨ WELCOME TO ASTORE: Rainbow Lake is reflecting 7 colors today! | 🏔️ Road to Deosai is open for tourists. | 🍖 Try Local Mamtoo & Chapshuro! | Call: +92 317 1588489
    </div>
</div>

<nav>
    <a href="#" class="logo"><i class="fas fa-snowflake"></i> ASTORE HUB</a>
    <div id="clock" style="font-size: 0.8rem; font-weight: 900; color: var(--primary);">00:00:00</div>
</nav>

<div class="float-controls">
    <button class="circle-btn" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>
    <button class="circle-btn" onclick="toggleLang()"><b id="l-ind">UR</b></button>
</div>

<header class="hero">
    <div class="badge" style="background: rgba(255,255,255,0.2); color: white; backdrop-filter: blur(5px);">Official Travel Portal</div>
    <h1 id="hero-h1">The Swiss of Pakistan</h1>
    <p id="hero-p">Astore Valley: Where Mountains Touch the Sky</p>
</header>

<div class="container">
    
    <a href="tel:+923171588489" class="sos-btn">
        <i class="fas fa-headset"></i> 24/7 TOURIST HELPLINE
    </a>

    <div class="card detail-card">
        <h3 id="h-vibe"><i class="fas fa-heart"></i> The Astore Vibe</h3>
        <p id="vibe-p" style="font-size: 0.95rem; color: #475569;">Imagine waking up to the roar of a turquoise river and the sight of Nanga Parbat's silver peaks. Astore isn't just a place; it's a feeling of pure, untouched peace.</p>
        
        <div class="weather-grid">
            <div class="weather-box">
                <i class="fas fa-sun"></i>
                <div style="font-size: 0.7rem; font-weight: bold;">SUMMER</div>
                <div style="font-size: 0.8rem;">15°C - 25°C</div>
            </div>
            <div class="weather-box">
                <i class="fas fa-snowflake"></i>
                <div style="font-size: 0.7rem; font-weight: bold;">WINTER</div>
                <div style="font-size: 0.8rem;">-10°C - 5°C</div>
            </div>
        </div>
    </div>

    <div class="card detail-card">
        <h3 id="h-spots"><i class="fas fa-star"></i> Magical Spots</h3>
        
        <div class="spot-guide">
            <div class="badge">Most Popular</div>
            <h4 id="s1-t"><i class="fas fa-water"></i> Minimarg & Rainbow Lake</h4>
            <p id="s1-d">Hidden behind the Burzil Pass, this valley feels like a fairytale. The lake changes colors from blue to emerald under the sun.</p>
        </div>

        <div class="spot-guide">
            <div class="badge">Perfect for Camping</div>
            <h4 id="s2-t"><i class="fas fa-tree"></i> Rama Meadows</h4>
            <h4 id="s2-t"><i class="fas fa-tree"></i> Rama Meadows</h4>
            <p id="s2-d">A massive green carpet surrounded by ancient pine trees. The "Rama Lake" is just a short trek away and is pure magic.</p>
        </div>
    </div>

    <div class="card detail-card">
        <h3 id="h-culture"><i class="fas fa-utensils"></i> Culture & Taste</h3>
        <p id="cult-p" style="font-size: 0.9rem;">The people of Astore are famous for their hospitality. Don't leave without trying:</p>
        <ul style="padding-left: 20px; font-size: 0.85rem; margin-top: 10px; color: #64748b;">
            <li id="c1"><b>Mamtoo:</b> Traditional steamed dumplings.</li>
            <li id="c2"><b>Local Herbal Tea:</b> Brewed from mountain flowers.</li>
            <li id="c3"><b>Shina Music:</b> The heartbeat of the valley.</li>
        </ul>
    </div>

    <div class="card detail-card" style="background: var(--primary); color: white;">
        <h3 style="color: white;"><i class="fas fa-tasks"></i> Pro Traveler Tip</h3>
        <p id="tip-p" style="font-size: 0.85rem; opacity: 0.9;">"Always carry your original CNIC and a high-clearance 4x4 Jeep. Astore's beauty is wild, and the roads are adventures themselves!"</p>
    </div>

    <a href="https://wa.me/923171588489" class="btn-wa">
        <i class="fab fa-whatsapp fa-lg"></i> <span id="wa-btn">LET'S START THE JOURNEY</span>
    </a>

</div>

<footer>
    <p>© 2026 Official Astore Tourist Portal</p>
    <p>Handcrafted for Astore Lovers 🏔️✨</p>
</footer>

<script>
    window.onscroll = () => {
        let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
        let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        document.getElementById("pBar").style.width = (winScroll / height) * 100 + "%";
    };

    setInterval(() => { 
        document.getElementById('clock').innerText = new Date().toLocaleTimeString(); 
    }, 1000);

    let isUr = false;
    function toggleLang() {
        isUr = !isUr;
        const content = {
            ur: { 
                h1: "پاکستان کا سوئٹزرلینڈ", p: "وادئ استور: جہاں پہاڑ آسمان کو چھوتے ہیں", 
                vibe: "استور کا احساس", vibeP: "استور صرف ایک جگہ نہیں، یہ سکون کا دوسرا نام ہے۔ دریائے استور کا شور اور نانگا پربت کی چاندی جیسی چوٹیاں آپ کا استقبال کرتی ہیں۔",
                spots: "جادوئی مقامات", s1t: "منی مرگ اور رینبو لیک", s1d: "برزل پاس کے پیچھے چھپی یہ وادی کسی پریوں کی کہانی جیسی لگتی ہے۔",
                s2t: "راما میڈوز", s2d: "قدیم صنوبر کے درختوں کے درمیان ایک بڑا سبز قالین، جہاں سے راما جھیل کا راستہ جاتا ہے۔",
                cult: "ثقافت اور ذائقہ", cultP: "استور کے لوگ اپنی مہمان نوازی کے لیے مشہور ہیں۔ یہ چیزیں ضرور آزمائیں:",
                c1: "ممتو: روایتی اسٹیمڈ ڈمپلنگز۔", c2: "مقامی ہربل چائے: پہاڑی پھولوں سے تیار کردہ۔", c3: "شنا موسیقی: وادی کی دھڑکن۔",
                tip: "پرو ٹریولر ٹپ: ہمیشہ اپنا اصل شناختی کارڈ اور 4x4 جیپ ساتھ رکھیں کیونکہ استور کی خوبصورتی جتنی دلکش ہے، راستے اتنے ہی ایڈونچر سے بھرپور ہیں۔",
                wa: "سفر کا آغاز کریں", ind: "EN"
            },
            en: { 
                h1: "The Swiss of Pakistan", p: "Astore Valley: Where Mountains Touch the Sky", 
                vibe: "The Astore Vibe", vibeP: "Astore isn't just a place; it's a feeling of pure, untouched peace. Wake up to the roar of turquoise rivers and silver peaks.",
                spots: "Magical Spots", s1t: "Minimarg & Rainbow Lake", s1d: "Hidden behind the Burzil Pass, this valley feels like a fairytale landscape.",
                s2t: "Rama Meadows", s2d: "A massive green carpet surrounded by pine trees. Rama Lake is pure magic.",
                cult: "Culture & Taste", cultP: "The people of Astore are famous for their hospitality. Don't leave without trying:",
                c1: "Mamtoo: Traditional steamed dumplings.", c2: "Local Herbal Tea: Brewed from mountain flowers.", c3: "Shina Music: The heartbeat of the valley.",
                tip: "\"Always carry your original CNIC and a high-clearance 4x4 Jeep. Astore's beauty is wild, and the roads are adventures!\"",
                wa: "LET'S START THE JOURNEY", ind: "UR"
            }
        };
        const active = isUr ? content.ur : content.en;
        document.getElementById('hero-h1').innerText = active.h1;
        document.getElementById('hero-p').innerText = active.p;
        document.getElementById('h-vibe').innerHTML = `<i class="fas fa-heart"></i> ${active.vibe}`;
        document.getElementById('vibe-p').innerText = active.vibeP;
        document.getElementById('h-spots').innerHTML = `<i class="fas fa-star"></i> ${active.spots}`;
        document.getElementById('s1-t').innerHTML = `<i class="fas fa-water"></i> ${active.s1t}`;
        document.getElementById('s1-d').innerText = active.s1d;
        document.getElementById('s2-t').innerHTML = `<i class="fas fa-tree"></i> ${active.s2t}`;
        document.getElementById('s2-d').innerText = active.s2d;
        document.getElementById('h-culture').innerHTML = `<i class="fas fa-utensils"></i> ${active.cult}`;
        document.getElementById('cult-p').innerText = active.cultP;
        document.getElementById('c1').innerHTML = `<b>${active.c1.split(':')[0]}:</b> ${active.c1.split(':')[1]}`;
        document.getElementById('c2').innerHTML = `<b>${active.c2.split(':')[0]}:</b> ${active.c2.split(':')[1]}`;
        document.getElementById('c3').innerHTML = `<b>${active.c3.split(':')[0]}:</b> ${active.c3.split(':')[1]}`;
        document.getElementById('tip-p').innerText = active.tip;
        document.getElementById('wa-btn').innerText = active.wa;
        document.getElementById('l-ind').innerText = active.ind;
        document.body.style.direction = isUr ? 'rtl' : 'ltr';
    }
</script>

</body>
</html>
