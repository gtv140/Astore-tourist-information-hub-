<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Travel Hub | Powered by Prime Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu:wght@400;700&family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #10b981; --accent: #fbbf24; --bg: #020617; --card: rgba(255, 255, 255, 0.05); --text: #f8fafc; }
        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        .urdu-text { font-family: 'Noto Nastaliq Urdu', serif !important; line-height: 2.2; direction: rtl; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.9); backdrop-filter: blur(15px); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .lang-btn { background: var(--primary); color: white; border: none; padding: 8px 16px; border-radius: 12px; font-weight: 800; cursor: pointer; transition: 0.3s; }

        .hero { height: 28vh; margin: 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .hero img { width: 100%; height: 100%; object-fit: cover; }

        .section { padding: 15px 20px; }
        .section-title { font-weight: 800; font-size: 1.2rem; margin-bottom: 15px; display: flex; align-items: center; gap: 10px; color: var(--primary); }
        .card { background: var(--card); border-radius: 20px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); margin-bottom: 15px; }
        
        /* Places List */
        .place-item { border-bottom: 1px solid rgba(255,255,255,0.05); padding: 15px 0; cursor: pointer; }
        .place-item h4 { color: var(--accent); display: flex; justify-content: space-between; }
        .place-item p { font-size: 0.85rem; opacity: 0.7; margin-top: 8px; display: none; }
        .place-item.active p { display: block; }

        /* Form Styling */
        label { font-size: 0.8rem; font-weight: 600; opacity: 0.8; }
        input, select { width: 100%; padding: 12px; margin: 8px 0 15px; border-radius: 12px; border: 1px solid rgba(255,255,255,0.1); background: rgba(255,255,255,0.03); color: white; font-size: 0.9rem; }
        .submit-btn { background: var(--primary); color: white; width: 100%; padding: 16px; border-radius: 15px; border: none; font-weight: 800; font-size: 1rem; cursor: pointer; box-shadow: 0 10px 20px rgba(16, 185, 129, 0.2); }

        .footer { background: #000; padding: 40px 20px; text-align: center; border-top: 1px solid var(--primary); margin-top: 30px; }
        .footer h3 { color: var(--primary); letter-spacing: 2px; }
        .hidden { display: none; }
        .sos-btn { position: fixed; bottom: 30px; right: 20px; background: #ef4444; width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; z-index: 1000; text-decoration: none; box-shadow: 0 10px 20px rgba(239, 68, 68, 0.3); }
    </style>
</head>
<body>

<header>
    <div id="logo-text" style="font-weight: 800; font-size: 1.1rem;">ASTORE HUB</div>
    <button class="lang-btn" onclick="toggleLang()">اردو</button>
</header>

<div class="hero">
    <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Astore Valley">
</div>

<div id="en-hub">
    <div class="section">
        <div class="section-title"><i class="fa-solid fa-map-location-dot"></i> Destinations Guide</div>
        <div class="card">
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Rama Meadows <span>11 KM</span></h4>
                <p>A forested valley with stunning views of Nanga Parbat. It is the gateway to Rama Lake and offers high-altitude pine beauty.</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Minimarg & Rainbow Lake <span>65 KM</span></h4>
                <p>Known for its emerald waters and lush green plains. Access requires an army permit and an original CNIC card.</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Deosai Plains <span>45 KM</span></h4>
                <p>The Land of Giants. It is one of the highest plateaus in the world, famous for its golden marmots and wildflowers.</p>
            </div>
        </div>
    </div>

    <div class="section">
        <div class="section-title"><i class="fa-solid fa-calendar-check"></i> Plan Your Trip</div>
        <div class="card">
            <form id="bookEn">
                <label>Full Name</label>
                <input type="text" id="nameEn" placeholder="Your Name" required>
                <label>Service Type</label>
                <select id="svcEn">
                    <option>4x4 Jeep Rental</option>
                    <option>Hotel Room Booking</option>
                    <option>Complete Tour Package</option>
                </select>
                <label>Date of Visit</label>
                <input type="date" id="dateEn" required>
                <button type="button" class="submit-btn" onclick="sendEn()">Request Booking with Muhammad Nazim</button>
            </form>
        </div>
    </div>
</div>

<div id="ur-hub" class="hidden urdu-text">
    <div class="section">
        <div class="section-title"><i class="fa-solid fa-map-location-dot"></i> سیاحتی مقامات</div>
        <div class="card">
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>راما میڈوز <span>۱۱ کلومیٹر</span></h4>
                <p>چیڑ کے جنگلات اور نانگا پربت کے نظاروں سے بھری ہوئی وادی۔ یہ راما جھیل کا مرکزی راستہ ہے۔</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>منی مرگ اور رینبو جھیل <span>۶۵ کلومیٹر</span></h4>
                <p>اپنی سبزہ زاروں اور شفاف پانی کی جھیل کے لیے مشہور۔ یہاں جانے کے لیے اصل شناختی کارڈ اور آرمی اجازت نامہ ضروری ہے۔</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>دیوسائی کے میدان <span>۴۵ کلومیٹر</span></h4>
                <p>دنیا کا بلند ترین سطح مرتفع، جو اپنے جنگلی پھولوں اور خوبصورت جھیل شیوسر کے لیے مشہور ہے۔</p>
            </div>
        </div>
    </div>

    <div class="section">
        <div class="section-title"><i class="fa-solid fa-calendar-check"></i> بکنگ فارم</div>
        <div class="card">
            <form id="bookUr">
                <label>مکمل نام</label>
                <input type="text" id="nameUr" placeholder="اپنا نام لکھیں" required class="urdu-text">
                <label>سروس کا انتخاب</label>
                <select id="svcUr" class="urdu-text">
                    <option>جیپ کرایہ پر لیں</option>
                    <option>ہوٹل کی بکنگ</option>
                    <option>مکمل ٹور پیکیج</option>
                </select>
                <label>آمد کی تاریخ</label>
                <input type="date" id="dateUr" required>
                <button type="button" class="submit-btn" onclick="sendUr()">محمد ناظم سے بکنگ کی درخواست کریں</button>
            </form>
        </div>
    </div>
</div>

<div class="section">
    <div class="card" style="font-size: 0.8rem; opacity: 0.7;">
        <h4 id="priv-h">About Prime Solutions</h4>
        <p id="priv-p">Astore Hub is an official platform managed by Muhammad Nazim at Prime Solutions. We ensure professional travel services and data privacy for all tourists.</p>
    </div>
</div>

<footer class="footer">
    <h3>PRIME SOLUTIONS</h3>
    <p>Founder: Muhammad Nazim</p>
    <p>© 2026 Official Astore Tourist Hub</p>
</footer>

<a href="tel:923171588489" class="sos-btn"><i class="fa-solid fa-phone-volume"></i></a>

<script>
    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        document.getElementById('en-hub').classList.toggle('hidden');
        document.getElementById('ur-hub').classList.toggle('hidden');
        document.querySelector('.lang-btn').innerText = isUrdu ? "English" : "اردو";
        document.getElementById('logo-text').innerText = isUrdu ? "استور ہب" : "ASTORE HUB";
        
        const ph = document.getElementById('priv-h');
        const pp = document.getElementById('priv-p');
        if(isUrdu) {
            ph.innerText = "پرائم سلوشنز کے بارے میں";
            pp.innerText = "استور ہب محمد ناظم کی زیر نگرانی پرائم سلوشنز کا آفیشل پلیٹ فارم ہے۔ ہم تمام سیاحوں کو پیشہ ورانہ سفری خدمات فراہم کرتے ہیں۔";
        } else {
            ph.innerText = "About Prime Solutions";
            pp.innerText = "Astore Hub is managed by Muhammad Nazim at Prime Solutions. We ensure professional travel services and data privacy.";
        }
    }

    function sendEn() {
        const n = document.getElementById('nameEn').value;
        const s = document.getElementById('svcEn').value;
        const d = document.getElementById('dateEn').value;
        if(!n || !d) { alert("Fill all details, sweetie!"); return; }
        window.open(`https://wa.me/923171588489?text=*New Request*\nName: ${n}\nService: ${s}\nDate: ${d}\nManaged by Prime Solutions`);
    }

    function sendUr() {
        const n = document.getElementById('nameUr').value;
        const s = document.getElementById('svcUr').value;
        const d = document.getElementById('dateUr').value;
        if(!n || !d) { alert("براہ کرم تمام معلومات لکھیں"); return; }
        window.open(`https://wa.me/923171588489?text=*بکنگ درخواست*\nنام: ${n}\nسروس: ${s}\nتاریخ: ${d}\nپرائم سلوشنز`);
    }
</script>

</body>
</html>
