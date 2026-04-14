<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Master Hub | Ultimate Pro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #10b981;
            --accent: #fbbf24;
            --danger: #ef4444;
            --bg: #020617;
            --card: rgba(255, 255, 255, 0.05);
            --glass: blur(15px);
            --text: #f8fafc;
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        
        body { 
            background: var(--bg); 
            color: var(--text); 
            background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617);
            min-height: 100vh;
        }

        /* --- UI Components --- */
        #loader {
            position: fixed; inset: 0; background: #000; z-index: 9999;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            transition: 0.8s ease-out;
        }
        .spinner { width: 40px; height: 40px; border: 4px solid var(--card); border-top-color: var(--primary); border-radius: 50%; animation: spin 1s linear infinite; }
        @keyframes spin { to { transform: rotate(360deg); } }

        .top-alert {
            background: rgba(251, 191, 36, 0.1); color: var(--accent);
            padding: 8px; font-size: 0.75rem; text-align: center; font-weight: 700;
            border-bottom: 1px solid rgba(251, 191, 36, 0.2);
        }

        header {
            position: sticky; top: 0; z-index: 100; padding: 15px 20px;
            background: rgba(2, 6, 23, 0.7); backdrop-filter: var(--glass);
            display: flex; justify-content: space-between; align-items: center;
        }

        /* --- Weather & Road Status --- */
        .status-bar {
            display: flex; gap: 10px; padding: 15px; overflow-x: auto; scrollbar-width: none;
        }
        .status-card {
            background: var(--card); padding: 12px 20px; border-radius: 20px;
            white-space: nowrap; border: 1px solid rgba(255,255,255,0.1);
            display: flex; align-items: center; gap: 10px; font-size: 0.85rem;
        }
        .dot { height: 8px; width: 8px; border-radius: 50%; display: inline-block; }
        .dot-green { background: #22c55e; box-shadow: 0 0 10px #22c55e; }

        /* --- Hero Slider --- */
        .hero { height: 35vh; margin: 0 15px; border-radius: 25px; overflow: hidden; position: relative; box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 20s infinite cubic-bezier(0.4, 0, 0.2, 1); }
        .slide img { width: 25%; height: 100%; object-fit: cover; }
        @keyframes slide { 0%, 20% { transform: translateX(0); } 25%, 45% { transform: translateX(-25%); } 50%, 70% { transform: translateX(-50%); } 75%, 95% { transform: translateX(-75%); } }

        /* --- Services Grid --- */
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; padding: 20px; }
        .feature-box {
            background: var(--card); backdrop-filter: var(--glass);
            padding: 20px 10px; text-align: center; border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.05); transition: 0.3s; cursor: pointer;
        }
        .feature-box i { font-size: 1.6rem; color: var(--primary); margin-bottom: 10px; display: block; }
        .feature-box:active { transform: scale(0.9); background: var(--primary); }
        .feature-box.active { border-color: var(--primary); background: rgba(16, 185, 129, 0.2); }

        /* --- Booking & Safety --- */
        .action-card { background: var(--card); margin: 0 20px 20px; padding: 20px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); }
        .btn {
            background: linear-gradient(135deg, #10b981, #059669); color: white;
            padding: 15px; border: none; width: 100%; border-radius: 15px;
            font-weight: 800; font-size: 1rem; cursor: pointer; margin-top: 10px;
        }
        .btn-emergency { background: linear-gradient(135deg, #ef4444, #b91c1c); margin-top: 20px; }

        /* --- Bottom Nav --- */
        .bottom-nav {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; background: rgba(255,255,255,0.05); backdrop-filter: blur(20px);
            display: flex; justify-content: space-around; padding: 18px;
            border-radius: 30px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000;
        }
        .nav-item { color: rgba(255,255,255,0.5); font-size: 1.3rem; }
        .nav-item.active { color: var(--primary); }
    </style>
</head>
<body>

<div id="loader">
    <div class="spinner"></div>
    <p style="margin-top:15px; font-weight:600; letter-spacing:3px;">ASTORE MASTER HUB</p>
</div>

<div class="top-alert">
    <i class="fa-solid fa-triangle-exclamation"></i> DEOSAI ROAD CLOSED DUE TO SNOWFALL
</div>

<header>
    <div style="font-weight: 800; font-size: 1.2rem;">ASTORE <span style="color:var(--primary)">PRO</span></div>
    <div id="time" style="font-weight: 600; opacity: 0.7;"></div>
</header>

<div class="status-bar">
    <div class="status-card">
        <span class="dot dot-green"></span> Minimarg: Open
    </div>
    <div class="status-card">
        <i class="fa-solid fa-cloud-sun" style="color:var(--accent)"></i> 12°C Astore
    </div>
    <div class="status-card">
        <i class="fa-solid fa-tower-cell" style="color:var(--primary)"></i> SCOM Active
    </div>
</div>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=800"></div>
    </div>
</section>

<div class="grid">
    <div class="feature-box" onclick="setService(this, 'Jeep')"><i class="fa-solid fa-truck-monster"></i>Jeep</div>
    <div class="feature-box" onclick="setService(this, 'Hotel')"><i class="fa-solid fa-bed"></i>Hotel</div>
    <div class="feature-box" onclick="setService(this, 'Guide')"><i class="fa-solid fa-person-hiking"></i>Guide</div>
    <div class="feature-box" onclick="setService(this, 'Camping')"><i class="fa-solid fa-tent"></i>Camp</div>
    <div class="feature-box" onclick="setService(this, 'Food')"><i class="fa-solid fa-plate-wheat"></i>Food</div>
    <div class="feature-box" onclick="setService(this, 'Photo')"><i class="fa-solid fa-camera-retro"></i>Photo</div>
</div>

<div class="action-card">
    <h4 style="margin-bottom:10px">Quick Booking</h4>
    <input type="date" id="bookingDate" style="width:100%; padding:12px; border-radius:12px; border:none; background:rgba(255,255,255,0.1); color:white; margin-bottom:10px;">
    <button class="btn" onclick="sendWhatsApp()"><i class="fa-brands fa-whatsapp"></i> Book Now</button>
    
    <button class="btn btn-emergency" onclick="window.location.href='tel:1122'">
        <i class="fa-solid fa-phone-flip"></i> Emergency Rescue (1122)
    </button>
</div>

<div style="height: 100px;"></div>

<nav class="bottom-nav">
    <div class="nav-item active"><i class="fa-solid fa-house-chimney"></i></div>
    <div class="nav-item"><i class="fa-solid fa-map-pin"></i></div>
    <div class="nav-item" onclick="alert('Offline Map Downloaded!')"><i class="fa-solid fa-circle-arrow-down"></i></div>
    <div class="nav-item"><i class="fa-solid fa-gear"></i></div>
</nav>

<audio id="tapSound" src="https://www.soundjay.com/buttons/sounds/button-16.mp3"></audio>

<script>
    // Remove Loader
    window.onload = () => {
        setTimeout(() => {
            const loader = document.getElementById('loader');
            loader.style.opacity = '0';
            setTimeout(() => loader.remove(), 800);
        }, 1200);
        document.getElementById('bookingDate').valueAsDate = new Date();
    };

    // Clock
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour:'2-digit', minute:'2-digit'});
    }, 1000);

    // Selection Logic
    let currentService = "";
    function setService(el, name) {
        document.querySelectorAll('.feature-box').forEach(b => b.classList.remove('active'));
        el.classList.add('active');
        currentService = name;
        document.getElementById('tapSound').play();
        if(navigator.vibrate) navigator.vibrate(40);
    }

    // Booking Logic
    function sendWhatsApp() {
        const date = document.getElementById('bookingDate').value;
        if(!currentService) {
            alert("Pehle service select karein, sweetie!");
            return;
        }
        const text = `*NEW BOOKING - ASTORE HUB*%0A--------------------------%0A*Service:* ${currentService}%0A*Date:* ${date}%0A*Status:* Urgent Inquiry`;
        window.open(`https://wa.me/923171588489?text=${text}`);
    }
</script>

</body>
</html>
