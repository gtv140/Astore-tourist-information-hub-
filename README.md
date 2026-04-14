<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Master Travel Hub | Prime Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu:wght@400;700&family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #10b981; --accent: #fbbf24; --bg: #020617; --card: rgba(255, 255, 255, 0.05); --text: #f8fafc; }
        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        .urdu-text { font-family: 'Noto Nastaliq Urdu', serif !important; line-height: 2.5; direction: rtl; }
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        header { position: sticky; top: 0; z-index: 1000; padding: 15px 20px; background: rgba(2, 6, 23, 0.9); backdrop-filter: blur(15px); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .lang-btn { background: var(--primary); color: white; border: none; padding: 8px 16px; border-radius: 12px; font-weight: 800; cursor: pointer; box-shadow: 0 4px 10px rgba(16, 185, 129, 0.3); }

        /* --- Dynamic Hero Slider --- */
        .hero-container { margin: 15px; border-radius: 25px; overflow: hidden; height: 35vh; position: relative; box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
        .hero-slider { display: flex; width: 400%; height: 100%; animation: slide 25s infinite ease-in-out; }
        .slide { width: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; }
        .slide-overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(2,6,23,0.8), transparent); display: flex; align-items: flex-end; padding: 20px; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        /* --- Feature Grid --- */
        .feature-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; padding: 10px 20px; }
        .feature-card { background: var(--card); border-radius: 20px; padding: 15px; border: 1px solid rgba(255,255,255,0.05); text-align: center; }
        .feature-card i { font-size: 1.5rem; color: var(--accent); margin-bottom: 8px; }
        .feature-card h4 { font-size: 0.75rem; font-weight: 800; }

        .section { padding: 20px; }
        .section-title { font-weight: 800; font-size: 1.3rem; margin-bottom: 15px; color: var(--primary); display: flex; align-items: center; gap: 10px; }
        .card { background: var(--card); border-radius: 25px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); margin-bottom: 20px; }

        /* --- Places Explorer --- */
        .place-box { border-bottom: 1px solid rgba(255,255,255,0.05); padding: 15px 0; }
        .place-header { display: flex; justify-content: space-between; align-items: center; cursor: pointer; }
        .place-details { display: none; padding-top: 15px; font-size: 0.85rem; opacity: 0.8; line-height: 1.6; }
        .place-box.active .place-details { display: block; }
        .tag { background: rgba(16, 185, 129, 0.1); color: var(--primary); padding: 4px 10px; border-radius: 8px; font-size: 0.7rem; font-weight: 700; }

        /* --- Advanced Form --- */
        label { font-size: 0.8rem; font-weight: 700; margin-top: 15px; display: block; opacity: 0.9; }
        input, select, textarea { width: 100%; padding: 14px; margin-top: 8px; border-radius: 15px; border: 1px solid rgba(255,255,255,0.1); background: rgba(0,0,0,0.3); color: white; font-size: 0.9rem; }
        .submit-btn { background: linear-gradient(135deg, var(--primary), #059669); color: white; width: 100%; padding: 18px; border-radius: 18px; border: none; font-weight: 800; font-size: 1.1rem; margin-top: 20px; cursor: pointer; transition: 0.3s; }
        .submit-btn:active { transform: scale(0.96); opacity: 0.9; }

        /* --- Weather/Notice Banner --- */
        .notice-bar { background: #064e3b; margin: 15px 20px; padding: 12px; border-radius: 15px; font-size: 0.75rem; border: 1px dashed var(--primary); display: flex; align-items: center; gap: 10px; }

        .footer { background: #000; padding: 50px 20px; text-align: center; border-top: 2px solid var(--primary); margin-top: 40px; }
        .footer-logo { font-weight: 800; color: var(--primary); font-size: 1.4rem; letter-spacing: 2px; }
        .hidden { display: none; }
        
        /* Floating Contact */
        .float-btns { position: fixed; bottom: 30px; right: 20px; display: flex; flex-direction: column; gap: 12px; z-index: 2000; }
        .f-btn { width: 55px; height: 55px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; text-decoration: none; box-shadow: 0 10px 20px rgba(0,0,0,0.4); font-size: 1.4rem; }
        .b-wa { background: #25d366; }
        .b-sos { background: #ef4444; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
    </style>
</head>
<body>

<header>
    <div id="logo-main" style="font-weight: 800; font-size: 1.2rem; letter-spacing: -0.5px;">ASTORE HUB <span style="color:var(--primary)">PRO</span></div>
    <button class="lang-btn" onclick="toggleLang()">اردو</button>
</header>

<div class="hero-container">
    <div class="hero-slider">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Mountain">
            <div class="slide-overlay"><h3>Rama Meadows</h3></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800" alt="Lake">
            <div class="slide-overlay"><h3>Rainbow Lake</h3></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800" alt="Nature">
            <div class="slide-overlay"><h3>Minimarg Valley</h3></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?w=800" alt="Valley">
            <div class="slide-overlay"><h3>Deosai Plains</h3></div>
        </div>
    </div>
</div>

<div class="notice-bar">
    <i class="fa-solid fa-cloud-sun"></i>
    <span id="t-alert">Current Status: All roads open. SCOM signals active in Minimarg.</span>
</div>

<div id="en-sec">
    <div class="feature-grid">
        <div class="feature-card"><i class="fa-solid fa-gas-pump"></i><h4>Fuel Tips</h4></div>
        <div class="feature-card"><i class="fa-solid fa-atm"></i><h4>ATM Info</h4></div>
        <div class="feature-card"><i class="fa-solid fa-shield-check"></i><h4>Safe Route</h4></div>
        <div class="feature-card"><i class="fa-solid fa-kit-medical"></i><h4>Medical</h4></div>
    </div>

    <div class="section">
        <div class="section-title"><i class="fa-solid fa-location-dot"></i> Detailed Destination Guide</div>
        <div class="card">
            <div class="place-box" onclick="this.classList.toggle('active')">
                <div class="place-header"><h4>Rama Meadows <span class="tag">11 KM</span></h4><i class="fa-solid fa-chevron-down"></i></div>
                <div class="place-details">
                    The crown of Astore. Famous for deep pine forests and Rama Lake. High-clearance cars can reach, but 4x4 is recommended for the lake trek.
                </div>
            </div>
            <div class="place-box" onclick="this.classList.toggle('active')">
                <div class="place-header"><h4>Minimarg (Rainbow Lake) <span class="tag">65 KM</span></h4><i class="fa-solid fa-chevron-down"></i></div>
                <div class="place-details">
                    A paradise near the border. Requires Burzil Pass crossing. <b>Note:</b> You must carry original CNIC for military checkposts.
                </div>
            </div>
            <div class="place-box" onclick="this.classList.toggle('active')">
                <div class="place-header"><h4>Deosai Plains <span class="tag">45 KM</span></h4><i class="fa-solid fa-chevron-down"></i></div>
                <div class="place-details">
                    "The Land of Giants". Famous for Sheosar Lake and brown bears. July to September is the best time for blooming flowers.
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <div class="section-title"><i class="fa-solid fa-calendar-check"></i> Request Booking & Service</div>
        <div class="card">
            <form id="formEn">
                <label>Full Name</label>
                <input type="text" id="nEn" placeholder="Enter your full name" required>
                <label>Select Service</label>
                <select id="sEn">
                    <option>4x4 Jeep with Driver</option>
                    <option>Luxury/Standard Hotel Room</option>
                    <option>Complete Tour Package</option>
                    <option>Professional Tour Guide</option>
                </select>
                <label>Number of People</label>
                <input type="number" id="pEn" placeholder="e.g. 4">
                <label>Arrival Date</label>
                <input type="date" id="dEn" required>
                <button type="button" class="submit-btn" onclick="goEn()">Confirm Booking via WhatsApp</button>
            </form>
        </div>
    </div>
</div>

<div id="ur-sec" class="hidden urdu-text">
    <div class="section">
        <div class="section-title">سیاحتی مقامات کی مکمل تفصیل</div>
        <div class="card">
            <div class="place-box" onclick="this.classList.toggle('active')">
                <div class="place-header"><h4>راما میڈوز (۱۱ کلومیٹر)</h4><i class="fa-solid fa-chevron-down"></i></div>
                <div class="place-details">
                    استور کی سب سے سرسبز وادی۔ یہاں راما جھیل اور دیو قامت چیڑ کے جنگلات سیاحوں کی توجہ کا مرکز ہیں۔
                </div>
            </div>
            <div class="place-box" onclick="this.classList.toggle('active')">
                <div class="place-header"><h4>منی مرگ اور رینبو جھیل (۶۵ کلومیٹر)</h4><i class="fa-solid fa-chevron-down"></i></div>
                <div class="place-details">
                    برزل پاس کے پار ایک خوبصورت جنت۔ یاد رہے کہ یہاں جانے کے لیے اصل شناختی کارڈ ساتھ رکھنا لازمی ہے۔
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <div class="section-title">بکنگ اور رابطہ فارم</div>
        <div class="card">
            <form id="formUr">
                <label>مکمل نام</label>
                <input type="text" id="nUr" placeholder="اپنا نام لکھیں" class="urdu-text">
                <label>سروس کا انتخاب</label>
                <select id="sUr" class="urdu-text">
                    <option>جیپ کرایہ پر لیں</option>
                    <option>ہوٹل کی بکنگ</option>
                    <option>مکمل ٹور پیکیج</option>
                </select>
                <label>آمد کی تاریخ</label>
                <input type="date" id="dUr">
                <button type="button" class="submit-btn" onclick="goUr()">محمد ناظم سے رابطہ کریں</button>
            </form>
        </div>
    </div>
</div>

<div class="section">
    <div class="card" style="font-size: 0.8rem; border: 1px solid var(--primary);">
        <h4 id="t-abt">About Muhammad Nazim & Prime Solutions</h4>
        <p id="t-abt-p" style="margin-top:10px; opacity:0.7;">This travel ecosystem is developed and managed by <b>Prime Solutions</b>. Under the leadership of <b>Muhammad Nazim</b>, we aim to provide high-end digital solutions and real-world travel assistance to explore the beauty of Gilgit-Baltistan.</p>
    </div>
</div>

<footer class="footer">
    <div class="footer-logo">PRIME SOLUTIONS</div>
    <p>Powered by Muhammad Nazim</p>
    <p style="margin-top:20px; font-size:0.7rem; opacity:0.5;">© 2026 ASTORE TRAVEL HUB PRO. All Rights Reserved.</p>
</footer>

<div class="float-btns">
    <a href="https://wa.me/923171588489" class="f-btn b-wa"><i class="fa-brands fa-whatsapp"></i></a>
    <a href="tel:923171588489" class="f-btn b-sos"><i class="fa-solid fa-phone"></i></a>
</div>

<script>
    let isUr = false;
    function toggleLang() {
        isUr = !isUr;
        document.getElementById('en-sec').classList.toggle('hidden');
        document.getElementById('ur-sec').classList.toggle('hidden');
        document.querySelector('.lang-btn').innerText = isUr ? "English" : "اردو";
        document.getElementById('logo-main').innerHTML = isUr ? "استور ہب <span style='color:var(--primary)'>پرو</span>" : "ASTORE HUB <span style='color:var(--primary)'>PRO</span>";
        
        const alt = document.getElementById('t-alert');
        const abtH = document.getElementById('t-abt');
        const abtP = document.getElementById('t-abt-p');

        if(isUr) {
            alt.innerText = "تازہ ترین: تمام راستے کھلے ہیں۔ منی مرگ میں سگنلز موجود ہیں۔";
            abtH.innerText = "پرائم سلوشنز اور محمد ناظم کے بارے میں";
            abtP.innerText = "یہ پلیٹ فارم پرائم سلوشنز کے تحت محمد ناظم کی نگرانی میں چلایا جا رہا ہے۔ ہمارا مقصد گلگت بلتستان کی سیاحت کو ڈیجیٹل دور کے مطابق بہتر بنانا ہے۔";
        } else {
            alt.innerText = "Current Status: All roads open. SCOM signals active in Minimarg.";
            abtH.innerText = "About Muhammad Nazim & Prime Solutions";
            abtP.innerText = "This travel ecosystem is developed and managed by Prime Solutions. Under the leadership of Muhammad Nazim, we provide high-end travel assistance.";
        }
    }

    function goEn() {
        const n = document.getElementById('nEn').value;
        const s = document.getElementById('sEn').value;
        const d = document.getElementById('dEn').value;
        const p = document.getElementById('pEn').value || "1";
        if(!n || !d) { alert("Please fill your name and date, sweetie!"); return; }
        const msg = encodeURIComponent(`*New Astore Trip Request*\n*Name:* ${n}\n*Service:* ${s}\n*Guests:* ${p}\n*Date:* ${d}\n---\n_Via Prime Solutions_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }

    function goUr() {
        const n = document.getElementById('nUr').value;
        const s = document.getElementById('sUr').value;
        const d = document.getElementById('dUr').value;
        if(!n || !d) { alert("براہ کرم تمام خانے پُر کریں"); return; }
        const msg = encodeURIComponent(`*بکنگ کی درخواست*\n*نام:* ${n}\n*سروس:* ${s}\n*تاریخ:* ${d}\n---\n_پرائم سلوشنز_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }
</script>

</body>
</html>
