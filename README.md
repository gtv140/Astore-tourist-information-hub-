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
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; }

        header { position: sticky; top: 0; z-index: 100; padding: 15px 20px; background: rgba(2, 6, 23, 0.9); backdrop-filter: blur(15px); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .lang-btn { background: var(--primary); color: white; border: none; padding: 8px 16px; border-radius: 12px; font-weight: 800; cursor: pointer; }

        .hero { height: 25vh; margin: 15px; border-radius: 25px; overflow: hidden; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .hero img { width: 100%; height: 100%; object-fit: cover; }

        .section { padding: 20px; }
        .card { background: var(--card); border-radius: 20px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); margin-bottom: 15px; }
        
        /* Form Styling */
        input, select, textarea { width: 100%; padding: 12px; margin-top: 8px; border-radius: 10px; border: 1px solid rgba(255,255,255,0.1); background: rgba(0,0,0,0.2); color: white; }
        .submit-btn { background: var(--primary); color: white; width: 100%; padding: 15px; border-radius: 15px; border: none; font-weight: 800; margin-top: 15px; cursor: pointer; }

        .footer { background: #000; padding: 40px 20px; text-align: center; border-top: 1px solid var(--primary); margin-top: 30px; }
        .footer h3 { color: var(--primary); margin-bottom: 10px; }
        .footer p { font-size: 0.8rem; opacity: 0.6; line-height: 1.6; }

        .hidden { display: none; }
    </style>
</head>
<body>

<header>
    <div style="font-weight: 800;" id="main-logo">ASTORE HUB</div>
    <button class="lang-btn" onclick="toggleLang()">اردو</button>
</header>

<div class="hero">
    <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Astore Valley">
</div>

<div id="en-content">
    <div class="section">
        <h2 style="color: var(--primary); margin-bottom: 10px;">Plan Your Trip</h2>
        <div class="card">
            <form id="bookingForm">
                <label>Full Name</label>
                <input type="text" id="name" placeholder="Enter your name" required>
                
                <label style="display:block; margin-top:15px;">Destination</label>
                <select id="dest">
                    <option>Rama Meadows</option>
                    <option>Minimarg & Rainbow Lake</option>
                    <option>Deosai Plains</option>
                    <option>Rupal Face</option>
                </select>

                <label style="display:block; margin-top:15px;">Date of Arrival</label>
                <input type="date" id="date" required>

                <button type="button" class="submit-btn" onclick="sendFormEn()">Book Now via WhatsApp</button>
            </form>
        </div>
    </div>

    <div class="section">
        <h3>About Us</h3>
        <p style="font-size: 0.9rem; opacity: 0.7; margin-top: 10px;">Astore Travel Hub is a premium project by <b>Prime Solutions</b>, founded by <b>Muhammad Nazim</b>. We specialize in providing authentic information and seamless travel arrangements in the Astore Valley.</p>
    </div>
</div>

<div id="ur-content" class="hidden urdu-text">
    <div class="section">
        <h2 style="color: var(--primary); margin-bottom: 10px;">اپنے سفر کا منصوبہ بنائیں</h2>
        <div class="card">
            <form id="bookingFormUr">
                <label>مکمل نام</label>
                <input type="text" id="name-ur" placeholder="اپنا نام لکھیں" required class="urdu-text">
                
                <label style="display:block; margin-top:15px;">مقام کا انتخاب</label>
                <select id="dest-ur" class="urdu-text">
                    <option>راما میڈوز</option>
                    <option>منی مرگ اور رینبو جھیل</option>
                    <option>دیوسائی کے میدان</option>
                    <option>روپل فیس</option>
                </select>

                <label style="display:block; margin-top:15px;">آمد کی تاریخ</label>
                <input type="date" id="date-ur" required>

                <button type="button" class="submit-btn" onclick="sendFormUr()">ابھی بکنگ کریں</button>
            </form>
        </div>
    </div>

    <div class="section">
        <h3>ہمارے بارے میں</h3>
        <p style="font-size: 1rem; opacity: 0.8; margin-top: 10px;">استور ٹریول ہب <b>پرائم سلوشنز</b> کا ایک ممتاز منصوبہ ہے، جس کے بانی <b>محمد ناظم</b> ہیں۔ ہمارا مقصد سیاحوں کو استور کی وادی میں بہترین معلومات اور سفری سہولیات فراہم کرنا ہے۔</p>
    </div>
</div>

<div class="section">
    <div class="card" style="font-size: 0.75rem; opacity: 0.6;">
        <h4 id="t-priv">Privacy Policy</h4>
        <p id="t-priv-p">Your data is safe with us. We only collect your name and travel details to provide the best services. All information is managed by Prime Solutions under the supervision of Muhammad Nazim.</p>
    </div>
</div>

<footer class="footer">
    <h3>PRIME SOLUTIONS</h3>
    <p>Founder & CEO: Muhammad Nazim</p>
    <p>Astore, Gilgit-Baltistan, Pakistan</p>
    <p style="margin-top: 10px; color: var(--primary);">© 2026 All Rights Reserved</p>
</footer>

<script>
    let isUrdu = false;
    function toggleLang() {
        isUrdu = !isUrdu;
        document.getElementById('en-content').classList.toggle('hidden');
        document.getElementById('ur-content').classList.toggle('hidden');
        document.querySelector('.lang-btn').innerText = isUrdu ? "English" : "اردو";
        document.getElementById('main-logo').innerText = isUrdu ? "استور ہب" : "ASTORE HUB";
        
        // Update Privacy Section Text
        if(isUrdu) {
            document.getElementById('t-priv').innerText = "پرائیویسی پالیسی";
            document.getElementById('t-priv-p').innerText = "آپ کا ڈیٹا ہمارے پاس محفوظ ہے۔ ہم صرف آپ کا نام اور سفری تفصیلات بہترین خدمات فراہم کرنے کے لیے حاصل کرتے ہیں۔ تمام معلومات محمد ناظم کی زیر نگرانی پرائم سلوشنز کے ذریعے محفوظ رکھی جاتی ہیں۔";
        } else {
            document.getElementById('t-priv').innerText = "Privacy Policy";
            document.getElementById('t-priv-p').innerText = "Your data is safe with us. We only collect your name and travel details to provide the best services. All information is managed by Prime Solutions under the supervision of Muhammad Nazim.";
        }
    }

    function sendFormEn() {
        const name = document.getElementById('name').value;
        const dest = document.getElementById('dest').value;
        const date = document.getElementById('date').value;
        if(!name || !date) { alert("Please fill all details, sweetie!"); return; }
        
        const msg = encodeURIComponent(`*New Booking Request*\n*Name:* ${name}\n*Destination:* ${dest}\n*Date:* ${date}\n---\n_Via Prime Solutions_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }

    function sendFormUr() {
        const name = document.getElementById('name-ur').value;
        const dest = document.getElementById('dest-ur').value;
        const date = document.getElementById('date-ur').value;
        if(!name || !date) { alert("براہ کرم تمام معلومات فراہم کریں"); return; }
        
        const msg = encodeURIComponent(`*نئی بکنگ درخواست*\n*نام:* ${name}\n*مقام:* ${dest}\n*تاریخ:* ${date}\n---\n_پرائم سلوشنز_`);
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }
</script>

</body>
</html>
