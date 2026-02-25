<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Official Tourism Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --white: #ffffff; }
        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }
        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); color: #334155; transition: 0.3s; }

        /* 1. News Ticker */
        .ticker-wrap { background: #b91c1c; color: white; padding: 10px 0; position: sticky; top: 0; z-index: 3000; overflow: hidden; font-size: 0.8rem; font-weight: bold; border-bottom: 2px solid var(--accent); }
        .ticker { display: inline-block; white-space: nowrap; animation: scroll 25s linear infinite; }
        @keyframes scroll { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        /* 2. Navigation */
        nav { background: white; padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 38px; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 800; color: var(--primary); text-decoration: none; font-size: 1.3rem; letter-spacing: -1px; }

        /* 3. Language Switcher */
        #lang-switcher { position: fixed; top: 100px; right: 10px; z-index: 2000; display: flex; box-shadow: 0 4px 10px rgba(0,0,0,0.1); border-radius: 20px; overflow: hidden; }
        .lang-btn { padding: 8px 15px; border: none; cursor: pointer; font-weight: bold; font-size: 0.75rem; transition: 0.3s; }
        .active-lang { background: var(--primary); color: white; }
        .inactive-lang { background: white; color: var(--primary); }

        /* 4. Hero Section */
        .hero { height: 55vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }
        .weather-info { background: rgba(255,255,255,0.2); backdrop-filter: blur(5px); padding: 5px 15px; border-radius: 50px; font-size: 0.8rem; margin-bottom: 15px; border: 1px solid rgba(255,255,255,0.3); }

        /* 5. Main Content Container */
        .container { width: 100%; max-width: 550px; margin: 0 auto; padding: 30px 15px; }
        .section-card { background: white; padding: 25px; border-radius: 25px; margin-bottom: 25px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); border: 1px solid #f1f5f9; }
        
        /* 6. History Details */
        .history-text { font-size: 0.95rem; line-height: 1.7; color: #475569; text-align: justify; }

        /* 7. Interactive Ratings */
        .rating-box { text-align: center; }
        .stars i { font-size: 1.8rem; color: #cbd5e1; cursor: pointer; margin: 0 5px; transition: 0.2s; }
        .stars i.active { color: var(--accent); transform: scale(1.1); }

        /* 8. Modern Gallery */
        .gallery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin: 15px 0; }
        .gallery-img { width: 100%; height: 140px; object-fit: cover; border-radius: 15px; transition: 0.3s; border: 2px solid white; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }

        /* 9. Pro Booking Form */
        .booking-box { background: var(--primary); color: white; padding: 35px 25px; border-radius: 30px; text-align: center; }
        label { display: block; text-align: left; font-size: 0.8rem; margin-bottom: 5px; opacity: 0.8; }
        input, select { width: 100%; padding: 15px; border-radius: 12px; border: none; margin-bottom: 15px; font-size: 1rem; background: #f0fdf4; color: #064e3b; }
        .book-btn { background: #25d366; color: white; width: 100%; padding: 18px; border-radius: 12px; border: none; font-weight: 800; font-size: 1.1rem; cursor: pointer; transition: 0.3s; display: flex; align-items: center; justify-content: center; gap: 10px; box-shadow: 0 10px 20px rgba(37,211,102,0.3); }

        /* 10. Floating Elements */
        .wa-float { position: fixed; bottom: 85px; right: 20px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 8px 20px rgba(0,0,0,0.2); z-index: 2000; text-decoration: none; }
        
        /* Bottom Navigation Bar */
        .bottom-nav { position: fixed; bottom: 0; left: 0; width: 100%; background: white; display: flex; justify-content: space-around; padding: 12px 0; box-shadow: 0 -5px 15px rgba(0,0,0,0.05); z-index: 2500; border-top: 1px solid #f1f5f9; }
        .nav-item { color: #64748b; text-decoration: none; font-size: 0.75rem; text-align: center; flex: 1; }
        .nav-item i { font-size: 1.2rem; margin-bottom: 4px; display: block; }
        .nav-item.active { color: var(--primary); font-weight: bold; }

        footer { text-align: center; padding: 40px 20px 110px; color: #94a3b8; font-size: 0.8rem; border-top: 1px solid #eee; background: white; }
    </style>
</head>
<body id="page-body">

    <div class="ticker-wrap">
        <div class="ticker" id="ticker-data">
            ⛰️ ASTORE UPDATE: Road to Rama Meadows is CLEAR. | Minimarg Checkpost requires Original CNIC. | Current Temp in Astore: 12°C. | Contact for 4x4 Jeep Bookings: +92 317 1588489.
        </div>
    </div>

    <div id="lang-switcher">
        <button onclick="changeLang('en')" id="en-btn" class="lang-btn active-lang">EN</button>
        <button onclick="changeLang('ur')" id="ur-btn" class="lang-btn inactive-lang">اردو</button>
    </div>

    <nav>
        <a href="#" class="logo"><i class="fas fa-mountain"></i> ASTORE HUB</a>
        <a href="tel:+923171588489" style="color:var(--primary); font-size: 1.2rem;"><i class="fas fa-phone-alt"></i></a>
    </nav>

    <section class="hero">
        <div class="weather-info"><i class="fas fa-sun"></i> <span id="weather-text">Astore: Sunny | 12°C</span></div>
        <h1 id="hero-h1">Welcome to Astore</h1>
        <p id="hero-p">The First Digital Gateway to Astore's History & Beauty</p>
    </section>

    <div class="container">
        
        <div class="section-card">
            <h2 id="hist-h2" style="color:var(--primary); margin-bottom:12px; display:flex; align-items:center; gap:10px;">
                <i class="fas fa-landmark"></i> History of Astore
            </h2>
            <p id="hist-p" class="history-text">
                Astore valley has been a strategic corridor for centuries, linking the ancient Silk Route to the plains of Kashmir via the legendary Burzil Pass. Known as the "Land of Giants" due to its proximity to Nanga Parbat, it served as a vital administrative hub during the British Raj. Today, it stands as a symbol of untouched beauty and hospitality.
            </p>
        </div>

        <div class="section-card">
            <h3 id="gall-h3" style="margin-bottom:15px; color:var(--primary);"><i class="fas fa-camera-retro"></i> Travelers Gallery</h3>
            <div class="gallery-grid">
                <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=400" class="gallery-img">
                <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833?q=80&w=400" class="gallery-img">
            </div>
            <button onclick="alert('Photo upload feature coming soon, sweetie!')" style="width:100%; padding:12px; border:2px dashed #cbd5e1; background:none; border-radius:15px; font-size:0.85rem; cursor:pointer; font-weight:bold; color:#64748b;">
                <i class="fas fa-plus-circle"></i> Share Your Memory
            </button>
        </div>

        <div class="section-card rating-box">
            <h3 id="rate-h3">Rate Your Experience</h3>
            <div class="stars" id="stars">
                <i class="fas fa-star" onclick="setRate(1)"></i>
                <i class="fas fa-star" onclick="setRate(2)"></i>
                <i class="fas fa-star" onclick="setRate(3)"></i>
                <i class="fas fa-star" onclick="setRate(4)"></i>
                <i class="fas fa-star" onclick="setRate(5)"></i>
            </div>
            <p id="rate-tag" style="font-size:0.75rem; margin-top:8px; color:var(--accent); font-weight:bold;">Tap to rate us!</p>
        </div>

        <div class="booking-box" id="booking">
            <h2 id="book-h2">Quick Reservation</h2>
            <div style="margin-top:20px;">
                <label id="lbl-name">Full Name</label>
                <input type="text" id="cust-name" placeholder="Enter your name">
                
                <label id="lbl-dest">Select Destination</label>
                <select id="cust-dest">
                    <option>Minimarg & Rainbow Lake</option>
                    <option>Rama Meadows & Lake</option>
                    <option>Deosai Plains Crossing</option>
                    <option>Tarashing / Nanga Parbat Base</option>
                </select>

                <button class="book-btn" onclick="sendBooking()">
                    <i class="fab fa-whatsapp"></i> <span id="wa-btn-text">Confirm on WhatsApp</span>
                </button>
            </div>
        </div>

    </div>

    <a href="https://wa.me/923171588489" class="wa-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <div class="bottom-nav">
        <a href="#" class="nav-item active"><i class="fas fa-home"></i>Home</a>
        <a href="#booking" class="nav-item"><i class="fas fa-car"></i>Tours</a>
        <a href="tel:+923171588489" class="nav-item"><i class="fas fa-phone"></i>Call</a>
    </div>

    <footer>
        <p><b>Astore Tourist Information Hub</b></p>
        <p>Official Digital Guide | Gilgit-Baltistan</p>
        <p style="margin-top:10px; opacity:0.6;">Contact: +92 317 1588489</p>
    </footer>

    <script>
        const translations = {
            en: {
                ticker: "⛰️ ASTORE UPDATE: Road to Rama Meadows is CLEAR. | Minimarg Checkpost requires Original CNIC. | Current Temp in Astore: 12°C. | Contact for 4x4 Jeep Bookings: +92 317 1588489.",
                heroH1: "Welcome to Astore",
                heroP: "The First Digital Gateway to Astore's History & Beauty",
                weather: "Astore: Sunny | 12°C",
                histH2: "History of Astore",
                histP: "Astore valley has been a strategic corridor for centuries, linking the ancient Silk Route to the plains of Kashmir via the legendary Burzil Pass. Known as the 'Land of Giants' due to its proximity to Nanga Parbat, it served as a vital administrative hub during the British Raj. Today, it stands as a symbol of untouched beauty and hospitality.",
                gallH3: "Travelers Gallery",
                rateH3: "Rate Your Experience",
                rateTag: "Tap to rate us!",
                bookH2: "Quick Reservation",
                lblName: "Full Name",
                lblDest: "Select Destination",
                waBtn: "Confirm on WhatsApp"
            },
            ur: {
                ticker: "تازہ ترین اپڈیٹ: راما میڈوز روڈ کھلا ہے۔ | منی مرگ جانے کے لیے اصل شناختی کارڈ لازمی ہے۔ | استور کا درجہ حرارت: 12 ڈگری۔ | جیپ بکنگ کے لیے رابطہ کریں: +92 317 1588489",
                heroH1: "استور میں خوش آمدید",
                heroP: "استور کی تاریخ اور خوبصورتی کا پہلا ڈیجیٹل پورٹل",
                weather: "استور: مطلع صاف ہے | 12°C",
                histH2: "استور کی تاریخ",
                histP: "وادئ استور صدیوں سے ایک اہم راستہ رہی ہے، جو قدیم شاہراہ ریشم کو برزل پاس کے ذریعے کشمیر سے ملاتی ہے۔ نانگا پربت کے قریب ہونے کی وجہ سے اسے 'دیوؤں کی سرزمین' بھی کہا جاتا ہے۔ برطانوی راج کے دوران یہ ایک اہم انتظامی مرکز تھا۔ آج یہ اپنی بے مثال خوبصورتی اور مہمان نوازی کے لیے مشہور ہے۔",
                gallH3: "سیاحوں کی گیلری",
                rateH3: "اپنے تجربے کی درجہ بندی کریں",
                rateTag: "درجہ بندی کے لیے اسٹارز پر کلک کریں",
                bookH2: "فوری بکنگ",
                lblName: "آپ کا نام",
                lblDest: "منزل کا انتخاب کریں",
                waBtn: "واٹس ایپ پر تصدیق کریں"
            }
        };

        function changeLang(lang) {
            document.getElementById('ticker-data').innerText = translations[lang].ticker;
            document.getElementById('hero-h1').innerText = translations[lang].heroH1;
            document.getElementById('hero-p').innerText = translations[lang].heroP;
            document.getElementById('weather-text').innerText = translations[lang].weather;
            document.getElementById('hist-h2').innerHTML = `<i class="fas fa-landmark"></i> ${translations[lang].histH2}`;
            document.getElementById('hist-p').innerText = translations[lang].histP;
            document.getElementById('gall-h3').innerHTML = `<i class="fas fa-camera-retro"></i> ${translations[lang].gallH3}`;
            document.getElementById('rate-h3').innerText = translations[lang].rateH3;
            document.getElementById('rate-tag').innerText = translations[lang].rateTag;
            document.getElementById('book-h2').innerText = translations[lang].bookH2;
            document.getElementById('lbl-name').innerText = translations[lang].lblName;
            document.getElementById('lbl-dest').innerText = translations[lang].lblDest;
            document.getElementById('wa-btn-text').innerText = translations[lang].waBtn;

            if(lang === 'ur') {
                document.getElementById('page-body').style.direction = 'rtl';
                document.getElementById('ur-btn').className = 'lang-btn active-lang';
                document.getElementById('en-btn').className = 'lang-btn inactive-lang';
            } else {
                document.getElementById('page-body').style.direction = 'ltr';
                document.getElementById('en-btn').className = 'lang-btn active-lang';
                document.getElementById('ur-btn').className = 'lang-btn inactive-lang';
            }
        }

        function setRate(stars) {
            const starIcons = document.querySelectorAll('.stars i');
            starIcons.forEach((s, i) => {
                s.classList.toggle('active', i < stars);
            });
            document.getElementById('rate-tag').innerText = "Thank you for " + stars + " stars!";
        }

        function sendBooking() {
            const name = document.getElementById('cust-name').value;
            const dest = document.getElementById('cust-dest').value;
            if(!name) return alert("Please enter your name, sweetie!");
            const msg = `Assalam-o-Alaikum! My name is ${name}. I want to book a trip to ${dest}. Please guide me further.`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, '_blank');
        }
    </script>
</body>
</html>
