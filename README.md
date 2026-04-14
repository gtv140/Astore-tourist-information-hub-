<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Powered by Prime Solutions</title>
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
        .hero img { width: 100%; height: 100%; object-fit: cover; animation: scale 20s infinite alternate; }
        @keyframes scale { from { transform: scale(1); } to { transform: scale(1.1); } }

        .section { padding: 15px 20px; }
        .section-title { font-weight: 800; font-size: 1.2rem; margin-bottom: 15px; display: flex; align-items: center; gap: 10px; color: var(--primary); }

        .card { background: var(--card); border-radius: 20px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); margin-bottom: 15px; }
        
        /* Places List */
        .place-item { border-bottom: 1px solid rgba(255,255,255,0.05); padding: 15px 0; cursor: pointer; }
        .place-item h4 { color: var(--accent); display: flex; justify-content: space-between; }
        .place-item p { font-size: 0.85rem; opacity: 0.7; margin-top: 8px; display: none; }
        .place-item.active p { display: block; }

        /* Booking Form */
        label { font-size: 0.8rem; font-weight: 600; opacity: 0.8; }
        input, select, textarea { width: 100%; padding: 12px; margin: 8px 0 15px; border-radius: 12px; border: 1px solid rgba(255,255,255,0.1); background: rgba(255,255,255,0.03); color: white; font-size: 0.9rem; }
        .submit-btn { background: var(--primary); color: white; width: 100%; padding: 16px; border-radius: 15px; border: none; font-weight: 800; font-size: 1rem; cursor: pointer; box-shadow: 0 10px 20px rgba(16, 185, 129, 0.2); }

        /* Footer & Branding */
        .footer { background: #000; padding: 40px 20px; text-align: center; border-top: 1px solid var(--primary); margin-top: 30px; }
        .footer h3 { color: var(--primary); letter-spacing: 2px; }
        .footer p { font-size: 0.8rem; opacity: 0.6; margin-top: 5px; }
        
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
    <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Astore">
</div>

<div id="en-hub">
    <div class="section">
        <div class="section-title"><i class="fa-solid fa-map-location-dot"></i> Detailed Destinations</div>
        <div class="card">
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Rama Meadows <span>11 KM</span></h4>
                <p>A lush green valley surrounded by pine forests. It's the gateway to Rama Lake and offers stunning views of Nanga Parbat. Ideal for family camping and trekking.</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Minimarg & Rainbow Lake <span>65 KM</span></h4>
                <p>The hidden heaven of Astore. Access requires crossing Burzil Pass. Known for the crystal clear Rainbow Lake. Note: Original CNIC is mandatory for Army checkpoints.</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>Deosai National Park <span>45 KM</span></h4>
                <p>The Land of Giants. It is the second-highest plateau in the world. Famous for wildflowers, brown bears, and Sheosar Lake. Best visited in July-August.</p>
            </div>
        </div>
    </div>

    <div class="section">
        <div class="section-title"><i class="fa-solid fa-calendar-check"></i> Instant Booking Form</div>
        <div class="card">
            <form id="bookEn">
                <label>Full Name</label>
                <input type="text" id="nameEn" placeholder="Enter your name" required>
                <label>Select Service</label>
                <select id="svcEn">
                    <option>4x4 Jeep Rental</option>
                    <option>Hotel Booking</option>
                    <option>Full Tour Package</option>
                    <option>Local Tour Guide</option>
                </select>
                <label>Travel Date</label>
                <input type="date" id="dateEn" required>
                <button type="button" class="submit-btn" onclick="sendEn()">Send Request to Muhammad Nazim</button>
            </form>
        </div>
    </div>
</div>

<div id="ur-hub" class="hidden urdu-text">
    <div class="section">
        <div class="section-title"><i class="fa-solid fa-map-location-dot"></i> مقامات کی تفصیل</div>
        <div class="card">
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>راما میڈوز <span>۱۱ کلومیٹر</span></h4>
                <p>چیڑ کے جنگلات سے گھری ہوئی ایک سرسبز وادی۔ یہ راما جھیل کا راستہ ہے اور یہاں سے نانگا پربت کا نظارہ کیا جا سکتا ہے۔ فیملی کیمپنگ کے لیے بہترین جگہ ہے۔</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>منی مرگ اور رینبو جھیل <span>۶۵ کلومیٹر</span></h4>
                <p>استور کی پوشیدہ جنت! یہاں پہنچنے کے لیے برزل پاس عبور کرنا پڑتا ہے۔ یہاں کی رینبو جھیل دنیا بھر میں مشہور ہے۔ نوٹ: آرمی چیک پوسٹ کے لیے اصل شناختی کارڈ لازمی ہے۔</p>
            </div>
            <div class="place-item" onclick="this.classList.toggle('active')">
                <h4>دیوسائی نیشنل پارک <span>۴۵ کلومیٹر</span></h4>
                <p>دیو قامت میدان! یہ دنیا کا دوسرا بلند ترین سطح مرتفع ہے۔ یہ اپنے جنگلی پھولوں، بھورے ریچھوں اور شیوسر جھیل کے لیے مشہور ہے۔</p>
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
                    <option>لوکل ٹور گائیڈ</option>
                </select>
                <label>آمد کی تاریخ</label>
                <input type="date" id="dateUr" required>
                <button type="button" class="submit-btn" onclick="sendUr()">محمد ناظم سے رابطہ کریں</button>
            </form>
        </div>
    </div>
</div>

<div class="section">
    <div class="card" style="font-size: 0.8rem; opacity: 0.7;">
        <h4 id="priv-h">Privacy & Company Policy</h4>
        <p id="priv-p">This platform is a property of Prime Solutions. All travel services are supervised by Muhammad Nazim. We ensure your personal data is only used for travel coordination.</p>
    </div>
</div>

<footer class="footer">
    <h3>PRIME SOLUTIONS</h3>
    <p>Founder: Muhammad Nazim</p>
    <p>Quality Web & App Solutions</p>
    <p style="margin-top: 15px; color: var(--primary); font-weight: 800;">© 2026 OFFICIAL ASTORE HUB</p>
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
            ph.innerText = "پرائیویسی اور کمپنی پالیسی";
            pp.innerText = "یہ پلیٹ فارم پرائم سلوشنز کی ملکیت ہے۔ تمام سفری سہولیات محمد ناظم کی زیر نگرانی فراہم کی جاتی ہیں۔ ہم آپ کے ڈیٹا کی مکمل حفاظت کی ضمانت دیتے ہیں۔";
        } else {
            ph.innerText = "Privacy & Company Policy";
            pp.innerText = "This platform is a property of Prime Solutions. All travel services are supervised by Muhammad Nazim. We ensure your personal data is only used for travel coordination.";
        }
    }

    function sendEn() {
        const n = document.getElementById('nameEn').value;
        const s = document.getElementById('svcEn').value;
        const d = document.getElementById('dateEn').value;
        if(!n || !d) { alert("Please fill all fields, sweetie! 😘"); return; }
        const msg = encodeURIComponent(`*New Booking Request*\n*Client:* ${n}\n*Service:* ${s}\n*Date:* ${d}\n---\n_Managed by Prime Solutions_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }

    function sendUr() {
        const n = document.getElementById('nameUr').value;
        const s = document.getElementById('svcUr').value;
        const d = document.getElementById('dateUr').value;
        if(!n || !d) { alert("براہ کرم تمام معلومات فراہم کریں، سویٹی! 😘"); return; }
        const msg = encodeURIComponent(`*بکنگ کی نئی درخواست*\n*نام:* ${n}\n*سروس:* ${s}\n*تاریخ:* ${d}\n---\n_پرائم سلوشنز_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }
</script>

</body>
</html>
