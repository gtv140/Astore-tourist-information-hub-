<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Tourist Information Hub | Official Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #042f2e; --accent: #d97706; --bg: #f8fafc; --white: #ffffff; }
        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }
        body { font-family: 'Inter', sans-serif; background: var(--bg); color: #334155; transition: 0.3s; }

        /* 1. Live Ticker */
        .ticker-wrap { background: #b91c1c; color: white; padding: 10px 0; position: sticky; top: 0; z-index: 3000; overflow: hidden; font-size: 0.8rem; font-weight: bold; }
        .ticker { display: inline-block; white-space: nowrap; animation: scroll 25s linear infinite; }
        @keyframes scroll { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        /* 2. Navigation */
        nav { background: white; padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 38px; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 800; color: var(--primary); text-decoration: none; font-size: 1.3rem; }

        /* 3. Lang Switcher */
        #lang-switcher { position: fixed; top: 100px; right: 10px; z-index: 2000; display: flex; box-shadow: 0 4px 10px rgba(0,0,0,0.1); border-radius: 20px; overflow: hidden; }
        .lang-btn { padding: 8px 15px; border: none; cursor: pointer; font-weight: bold; font-size: 0.7rem; }
        .active-lang { background: var(--primary); color: white; }
        .inactive-lang { background: white; color: var(--primary); }

        /* 4. Hero */
        .hero { height: 50vh; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800'); background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px; }
        
        /* 5. Main Content */
        .container { width: 100%; max-width: 550px; margin: 0 auto; padding: 30px 15px; }
        .section-card { background: white; padding: 25px; border-radius: 20px; margin-bottom: 25px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); }
        
        /* 6. Interactive Ratings */
        .rating-box { text-align: center; margin: 20px 0; }
        .stars i { font-size: 1.5rem; color: #cbd5e1; cursor: pointer; margin: 0 5px; }
        .stars i.active { color: var(--accent); }

        /* 7. Gallery Grid */
        .gallery-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin: 15px 0; }
        .gallery-img { width: 100%; height: 120px; object-fit: cover; border-radius: 12px; }

        /* 8. Booking Form */
        .booking-form { background: var(--primary); color: white; padding: 30px 20px; border-radius: 25px; text-align: center; }
        input, select { width: 100%; padding: 14px; border-radius: 12px; border: none; margin-bottom: 15px; font-size: 1rem; }
        .wa-btn { background: #25d366; color: white; width: 100%; padding: 16px; border-radius: 12px; border: none; font-weight: 800; font-size: 1.1rem; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; }

        /* 9. Floating Buttons */
        .wa-float { position: fixed; bottom: 80px; right: 20px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); z-index: 1000; }

        .mobile-nav { position: fixed; bottom: 0; width: 100%; background: white; display: flex; justify-content: space-around; padding: 15px; box-shadow: 0 -2px 10px rgba(0,0,0,0.1); z-index: 2000; }
        .mobile-nav a { color: var(--primary); text-decoration: none; font-size: 0.8rem; text-align: center; font-weight: bold; }

        footer { text-align: center; padding: 40px 20px 100px; color: #94a3b8; font-size: 0.8rem; }
    </style>
</head>
<body id="main-body">

    <div class="ticker-wrap">
        <div class="ticker" id="ticker-content">
            ⚠️ ROAD UPDATE: Astore to Gilgit road is OPEN. | Minimarg/Burzil Pass requires 4x4 Jeep only. | Carry your original CNIC for security checkposts. | Welcome to Astore Valley!
        </div>
    </div>

    <div id="lang-switcher">
        <button onclick="changeLang('en')" id="en-btn" class="lang-btn active-lang">EN</button>
        <button onclick="changeLang('ur')" id="ur-btn" class="lang-btn inactive-lang">اردو</button>
    </div>

    <nav>
        <a href="#" class="logo">ASTORE HUB</a>
        <a href="tel:+923171588489" style="color:var(--primary)"><i class="fas fa-phone-alt"></i></a>
    </nav>

    <div class="hero">
        <h1 id="hero-h">Explore Astore Valley</h1>
        <p id="hero-p">The First Digital Portal of Astore History & Tourism</p>
    </div>

    <div class="container">
        
        <div class="section-card">
            <h2 id="hist-h" style="color:var(--primary); margin-bottom:10px;">The History</h2>
            <p id="hist-p" style="font-size: 0.9rem; line-height: 1.6;">Astore is a historic gateway linking Gilgit to Kashmir via the ancient Burzil Pass. Known for its brave people and the majestic Nanga Parbat views, it remains the most vital strategic valley in the North.</p>
        </div>

        <div class="section-card rating-box">
            <h3 id="rate-h">Rate Your Experience</h3>
            <div class="stars" id="star-container">
                <i class="fas fa-star" onclick="rate(1)"></i>
                <i class="fas fa-star" onclick="rate(2)"></i>
                <i class="fas fa-star" onclick="rate(3)"></i>
                <i class="fas fa-star" onclick="rate(4)"></i>
                <i class="fas fa-star" onclick="rate(5)"></i>
            </div>
            <p id="rate-status" style="font-size:0.7rem; margin-top:5px; color:var(--accent)">How was your trip?</p>
        </div>

        <div class="section-card">
            <h3 id="gall-h">Travelers Gallery</h3>
            <div class="gallery-grid">
                <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=400" class="gallery-img">
                <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833?q=80&w=400" class="gallery-img">
            </div>
            <button style="width:100%; padding:10px; border:1px dashed var(--primary); background:none; border-radius:10px; font-size:0.8rem; cursor:pointer;">+ Share Your Photo</button>
        </div>

        <div class="booking-form" id="book">
            <h2 id="book-h">Book Your Jeep</h2>
            <input type="text" id="name" placeholder="Full Name">
            <select id="dest">
                <option>Minimarg & Rainbow Lake</option>
                <option>Rama Meadows</option>
                <option>Deosai Plains Crossing</option>
            </select>
            <button class="wa-btn" onclick="sendWA()">
                <i class="fab fa-whatsapp"></i> <span id="wa-text">Book on WhatsApp</span>
            </button>
        </div>
    </div>

    <a href="https://wa.me/923171588489" class="wa-float"><i class="fab fa-whatsapp"></i></a>

    <div class="mobile-nav">
        <a href="#"><i class="fas fa-home"></i><br>Home</a>
        <a href="#book"><i class="fas fa-car"></i><br>Booking</a>
        <a href="tel:+923171588489"><i class="fas fa-headset"></i><br>Support</a>
    </div>

    <footer>
        <p>© 2026 Astore Tourist Information Hub</p>
        <p>Managed by Local Union Astore | +92 317 1588489</p>
    </footer>

    <script>
        const data = {
            en: {
                heroH: "Explore Astore Valley",
                heroP: "The First Digital Portal of Astore History & Tourism",
                histH: "The History",
                histP: "Astore is a historic gateway linking Gilgit to Kashmir via the ancient Burzil Pass. Known for its brave people and the majestic Nanga Parbat views, it remains the most vital strategic valley in the North.",
                rateH: "Rate Your Experience",
                gallH: "Travelers Gallery",
                bookH: "Book Your Jeep",
                waText: "Book on WhatsApp",
                ticker: "⚠️ ROAD UPDATE: Astore to Gilgit road is OPEN. | Minimarg/Burzil Pass requires 4x4 Jeep only. | Carry your original CNIC for checkposts."
            },
            ur: {
                heroH: "وادئ استور کی سیر کریں",
                heroP: "استور کی تاریخ اور سیاحت کا پہلا ڈیجیٹل پورٹل",
                histH: "تاریخ",
                histP: "استور ایک تاریخی راستہ ہے جو قدیم برزل پاس کے ذریعے گلگت کو کشمیر سے جوڑتا ہے۔ اپنے بہادر لوگوں اور نانگا پربت کے خوبصورت مناظر کے لیے مشہور، یہ شمال کی سب سے اہم وادی ہے۔",
                rateH: "اپنے تجربے کی درجہ بندی کریں",
                gallH: "سیاحوں کی گیلری",
                bookH: "جیپ بک کریں",
                waText: "واٹس ایپ پر رابطہ کریں",
                ticker: "تازہ ترین اپڈیٹ: استور گلگت روڈ ٹریفک کے لیے کھلی ہے۔ | منی مرگ کے لیے فور بائے فور جیپ لازمی ہے۔ | اپنا شناختی کارڈ ساتھ رکھیں۔"
            }
        };

        function changeLang(l) {
            document.getElementById('hero-h').innerText = data[l].heroH;
            document.getElementById('hero-p').innerText = data[l].heroP;
            document.getElementById('hist-h').innerText = data[l].histH;
            document.getElementById('hist-p').innerText = data[l].histP;
            document.getElementById('rate-h').innerText = data[l].rateH;
            document.getElementById('gall-h').innerText = data[l].gallH;
            document.getElementById('book-h').innerText = data[l].bookH;
            document.getElementById('wa-text').innerText = data[l].waText;
            document.getElementById('ticker-content').innerText = data[l].ticker;

            if(l === 'ur') {
                document.getElementById('main-body').style.direction = 'rtl';
                document.getElementById('ur-btn').className = 'lang-btn active-lang';
                document.getElementById('en-btn').className = 'lang-btn inactive-lang';
            } else {
                document.getElementById('main-body').style.direction = 'ltr';
                document.getElementById('en-btn').className = 'lang-btn active-lang';
                document.getElementById('ur-btn').className = 'lang-btn inactive-lang';
            }
        }

        function rate(s) {
            const stars = document.querySelectorAll('.stars i');
            stars.forEach((star, index) => {
                star.classList.toggle('active', index < s);
            });
            document.getElementById('rate-status').innerText = "Thanks for rating: " + s + " Stars!";
        }

        function sendWA() {
            const name = document.getElementById('name').value;
            const dest = document.getElementById('dest').value;
            if(!name) return alert("Please enter name, sweetie!");
            window.open(`https://wa.me/923171588489?text=Hi, I am ${name}. I want to book a trip to ${dest}.`, '_blank');
        }
    </script>
</body>
</html>
