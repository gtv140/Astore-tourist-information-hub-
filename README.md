<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Pro | Developed by PRIMESOLUTIONS</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu:wght@400;700&family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    
    <style>
        :root { 
            --primary: #10b981; 
            --accent: #fbbf24; 
            --bg: #020617; 
            --card: rgba(255, 255, 255, 0.05); 
            --text: #f8fafc; 
            --glass: blur(15px);
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        .urdu-font { font-family: 'Noto Nastaliq Urdu', serif !important; line-height: 2.5; direction: rtl; }
        
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        /* --- Header --- */
        header { position: sticky; top: 0; z-index: 1000; padding: 15px 20px; background: rgba(2, 6, 23, 0.9); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .logo { font-weight: 800; font-size: 1.2rem; letter-spacing: -0.5px; }
        .lang-btn { background: var(--primary); color: white; border: none; padding: 6px 14px; border-radius: 10px; font-weight: 700; font-size: 0.75rem; cursor: pointer; }

        /* --- Page Transitions --- */
        .page { display: none; animation: fadeIn 0.4s ease; padding-bottom: 100px; }
        .page.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        /* --- Hero / Gallery --- */
        .hero-box { margin: 15px; border-radius: 25px; overflow: hidden; height: 28vh; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .hero-box img { width: 100%; height: 100%; object-fit: cover; }
        .hero-label { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.8)); padding: 20px; font-weight: 800; }

        /* --- Grid & Cards --- */
        .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; padding: 0 20px; }
        .feature-card { background: var(--card); border-radius: 20px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); text-align: center; transition: 0.3s; }
        .feature-card i { font-size: 1.8rem; color: var(--primary); margin-bottom: 10px; }
        .feature-card h4 { font-size: 0.8rem; font-weight: 700; }

        .section-title { padding: 25px 20px 15px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 10px; }

        /* --- Destinations List --- */
        .place-card { background: var(--card); margin: 0 20px 15px; border-radius: 20px; overflow: hidden; border: 1px solid rgba(255,255,255,0.05); }
        .place-img { height: 150px; width: 100%; object-fit: cover; }
        .place-info { padding: 15px; }
        .place-info h3 { font-size: 1rem; color: var(--accent); margin-bottom: 5px; }
        .place-info p { font-size: 0.8rem; opacity: 0.7; line-height: 1.5; }

        /* --- Forms --- */
        .form-group { padding: 0 20px; }
        input, select, textarea { width: 100%; padding: 14px; margin-bottom: 15px; border-radius: 12px; border: 1px solid rgba(255,255,255,0.1); background: rgba(0,0,0,0.3); color: white; font-size: 0.9rem; }
        .main-btn { background: var(--primary); color: white; width: 100%; padding: 16px; border-radius: 15px; border: none; font-weight: 800; font-size: 1rem; cursor: pointer; box-shadow: 0 8px 20px rgba(16, 185, 129, 0.2); }

        /* --- Branding --- */
        .branding-card { margin: 20px; background: rgba(16, 185, 129, 0.05); border: 1px dashed var(--primary); border-radius: 20px; padding: 20px; text-align: center; }
        .brand-link { color: var(--text); text-decoration: none; font-weight: 800; display: inline-flex; align-items: center; gap: 6px; margin: 5px 0; }
        .brand-link i { color: var(--primary); font-size: 0.8rem; }

        /* --- Navigation Bar --- */
        .nav-bar { position: fixed; bottom: 20px; left: 20px; right: 20px; background: rgba(255,255,255,0.08); backdrop-filter: var(--glass); display: flex; justify-content: space-around; padding: 15px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-item { color: rgba(255,255,255,0.4); font-size: 1.3rem; transition: 0.3s; cursor: pointer; }
        .nav-item.active { color: var(--primary); transform: translateY(-5px); }

        /* --- SOS --- */
        .sos-btn { position: fixed; bottom: 100px; right: 20px; background: #ef4444; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; box-shadow: 0 10px 20px rgba(239, 68, 68, 0.3); z-index: 999; text-decoration: none; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
    </style>
</head>
<body>

<header>
    <div class="logo">ASTORE <span style="color:var(--primary)">HUB PRO</span></div>
    <button class="lang-btn" onclick="toggleLanguage()">اردو</button>
</header>

<div id="home" class="page active">
    <div class="hero-box">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Astore">
        <div class="hero-label"><span id="h-welcome">Welcome to Astore Valley</span></div>
    </div>

    <div class="section-title"><i class="fa-solid fa-star"></i> <span id="h-services">Top Services</span></div>
    <div class="grid">
        <div class="feature-card" onclick="showPage('booking')"><i class="fa-solid fa-truck-monster"></i><h4>Jeep 4x4</h4></div>
        <div class="feature-card" onclick="showPage('booking')"><i class="fa-solid fa-hotel"></i><h4>Hotels</h4></div>
        <div class="feature-card" onclick="showPage('explore')"><i class="fa-solid fa-map-marked-alt"></i><h4>Places</h4></div>
        <div class="feature-card" onclick="showPage('about')"><i class="fa-solid fa-id-badge"></i><h4>Prime Dev</h4></div>
    </div>

    <div class="branding-card">
        <p id="h-managed" style="font-size: 0.75rem; opacity: 0.6; margin-bottom: 5px;">Supervised & Developed By</p>
        <a href="https://web-hub-code.github.io/Web-hub/" target="_blank" class="brand-link">Prime Solutions<i class="fa-solid fa-external-link-alt"></i></a><br>
        <a href="https://web-hub-code.github.io/PRIMESOLUTIONS/" target="_blank" class="brand-link">Prime Solutions <i class="fa-solid fa-external-link-alt"></i></a>
    </div>
</div>

<div id="explore" class="page">
    <div class="section-title"><i class="fa-solid fa-compass"></i> <span id="e-title">Must Visit Places</span></div>
    
    <div class="place-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800" class="place-img">
        <div class="place-info">
            <h3>Rama Meadows</h3>
            <p id="e-rama">Heavenly forests and the gateway to Rama Lake. Perfect for camping and nature lovers.</p>
        </div>
    </div>

    <div class="place-card">
        <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800" class="place-img">
        <div class="place-info">
            <h3>Minimarg & Rainbow Lake</h3>
            <p id="e-mini">Hidden gem of Astore. Requires army clearance and a 4x4 jeep to reach this paradise.</p>
        </div>
    </div>
</div>

<div id="booking" class="page">
    <div class="section-title"><i class="fa-solid fa-calendar-check"></i> <span id="b-title">Book Your Trip</span></div>
    <div class="form-group">
        <input type="text" id="custName" placeholder="Enter Full Name" required>
        <select id="svcType">
            <option value="4x4 Jeep Rental">Jeep 4x4 Rental</option>
            <option value="Hotel Booking">Hotel/Room Booking</option>
            <option value="Full Tour Package">Full Tour Package</option>
        </select>
        <input type="date" id="tripDate" required>
        <textarea id="extraReq" rows="3" placeholder="Any extra requirements?"></textarea>
        <button class="main-btn" onclick="sendWhatsApp()"><i class="fa-brands fa-whatsapp"></i> <span id="b-btn">Book Now</span></button>
    </div>
</div>

<div id="about" class="page">
    <div class="section-title"><i class="fa-solid fa-code"></i> <span id="a-title">Developer Details</span></div>
    <div class="card" style="margin: 0 20px; padding: 25px; background: var(--card); border-radius: 25px; text-align: center;">
        <h3 style="color:var(--primary)">Prime Solutions</h3>
        <p style="font-size: 0.85rem; opacity: 0.7; margin: 15px 0;">Founder of Prime Solutions. Professional Web & App Developer specialized in creating high-performance digital hubs.</p>
        <div style="display: flex; justify-content: center; gap: 20px; font-size: 1.5rem; margin-top: 10px;">
            <a href="https://web-hub-code.github.io/Web-hub/" target="_blank" style="color:white"><i class="fa-solid fa-globe"></i></a>
            <a href="https://wa.me/923171588489" style="color:var(--primary)"><i class="fa-brands fa-whatsapp"></i></a>
        </div>
    </div>
</div>

<div class="nav-bar">
    <div class="nav-item active" onclick="showPage('home')"><i class="fa-solid fa-house"></i></div>
    <div class="nav-item" onclick="showPage('explore')"><i class="fa-solid fa-mountain-sun"></i></div>
    <div class="nav-item" onclick="showPage('booking')"><i class="fa-solid fa-calendar-day"></i></div>
    <div class="nav-item" onclick="showPage('about')"><i class="fa-solid fa-user-gear"></i></div>
</div>

<a href="tel:923171588489" class="sos-btn"><i class="fa-solid fa-phone-volume"></i></a>

<script>
    // Page Management Logic
    function showPage(pageId) {
        document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
        document.getElementById(pageId).classList.add('active');
        
        // Update Nav Icons
        document.querySelectorAll('.nav-item').forEach(nav => nav.classList.remove('active'));
        const index = ['home', 'explore', 'booking', 'about'].indexOf(pageId);
        document.querySelectorAll('.nav-item')[index].classList.add('active');
        
        window.scrollTo(0,0);
        if(navigator.vibrate) navigator.vibrate(30);
    }

    // Language Toggle Logic
    let isUrdu = false;
    function toggleLanguage() {
        isUrdu = !isUrdu;
        const body = document.body;
        const btn = document.querySelector('.lang-btn');
        
        if(isUrdu) {
            body.classList.add('urdu-font');
            btn.innerText = "ENGLISH";
            document.getElementById('h-welcome').innerText = "استور ہب میں خوش آمدید";
            document.getElementById('h-services').innerText = "ہماری سہولیات";
            document.getElementById('h-managed').innerText = "زیرِ نگرانی و تخلیق";
            document.getElementById('e-title').innerText = "مشہور سیاحتی مقامات";
            document.getElementById('b-title').innerText = "بکنگ فارم";
            document.getElementById('b-btn').innerText = "ابھی رابطہ کریں";
            document.getElementById('a-title').innerText = "ڈویلپر کی تفصیلات";
        } else {
            body.classList.remove('urdu-font');
            btn.innerText = "اردو";
            document.getElementById('h-welcome').innerText = "Welcome to Astore Valley";
            document.getElementById('h-services').innerText = "Top Services";
            document.getElementById('h-managed').innerText = "Supervised & Developed By";
            document.getElementById('e-title').innerText = "Must Visit Places";
            document.getElementById('b-title').innerText = "Book Your Trip";
            document.getElementById('b-btn').innerText = "Book Now";
            document.getElementById('a-title').innerText = "Developer Details";
        }
    }

    // Booking Function
    function sendWhatsApp() {
        const name = document.getElementById('custName').value;
        const svc = document.getElementById('svcType').value;
        const date = document.getElementById('tripDate').value;
        const req = document.getElementById('extraReq').value;

        if(!name || !date) {
            alert(isUrdu ? "براہ کرم تمام خانے پُر کریں، سویٹی! 😘" : "Please fill all fields, ! 😘");
            return;
        }

        const message = `*ASTORE HUB PRO BOOKING*\n\n*Name:* ${name}\n*Service:* ${svc}\n*Date:* ${date}\n*Request:* ${req}\n\n_System Generated via Prime Solutions_`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(message)}`);
    }
</script>

</body>
</html>
