<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Master Hub | NextGen</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root { 
            --primary: #10b981; 
            --accent: #fbbf24; 
            --bg: #0f172a; 
            --card: rgba(255, 255, 255, 0.05); 
            --text: #f8fafc;
            --glass: blur(12px);
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; }
        
        body { 
            background: var(--bg); 
            color: var(--text); 
            overflow-x: hidden;
            background-image: radial-gradient(circle at top right, #1e293b, #0f172a);
        }

        /* Modern Loader */
        #loader {
            position: fixed; inset: 0; background: #000; 
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            z-index: 9999; transition: 0.8s ease-out;
        }
        .spinner {
            width: 50px; height: 50px; border: 5px solid var(--card);
            border-top-color: var(--primary); border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin { to { transform: rotate(360deg); } }

        header {
            position: sticky; top: 0; z-index: 100;
            background: rgba(15, 23, 42, 0.7); backdrop-filter: var(--glass);
            display: flex; justify-content: space-between; padding: 15px 20px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        /* Animated Hero Section */
        .hero { height: 40vh; position: relative; overflow: hidden; border-radius: 0 0 30px 30px; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 20s infinite cubic-bezier(0.4, 0, 0.2, 1); }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7); }

        @keyframes slide {
            0%, 20% { transform: translateX(0); }
            25%, 45% { transform: translateX(-25%); }
            50%, 70% { transform: translateX(-50%); }
            75%, 95% { transform: translateX(-75%); }
        }

        .container { padding: 20px; margin-bottom: 80px; }

        /* Modern Grid with Hover Effects */
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; margin-top: 20px; }
        .feature-box {
            background: var(--card); backdrop-filter: var(--glass);
            padding: 20px 10px; text-align: center; border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.1);
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: pointer;
        }
        .feature-box i { font-size: 1.5rem; color: var(--primary); margin-bottom: 8px; display: block; }
        .feature-box:hover { transform: translateY(-10px); background: rgba(255,255,255,0.1); border-color: var(--primary); }
        .feature-box.selected { background: var(--primary); color: white; border-color: white; }
        .feature-box.selected i { color: white; }

        /* Booking Card */
        .booking-card {
            background: linear-gradient(135deg, #1e293b, #334155);
            padding: 20px; border-radius: 25px; margin-top: 25px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        input[type="date"] {
            width: 100%; padding: 12px; border-radius: 12px; border: none;
            background: rgba(255,255,255,0.1); color: white; outline: none; margin: 10px 0;
        }

        .btn {
            background: linear-gradient(90deg, #25d366, #128c7e);
            color: #fff; padding: 15px; border: none; width: 100%;
            border-radius: 15px; font-weight: 800; font-size: 1rem;
            cursor: pointer; box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
        }
        .btn:active { transform: scale(0.98); }

        /* Floating Bottom Nav */
        .bottom-nav {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            width: 90%; background: rgba(255,255,255,0.1); backdrop-filter: blur(20px);
            display: flex; justify-content: space-around; padding: 15px;
            border-radius: 25px; border: 1px solid rgba(255,255,255,0.2); z-index: 1000;
        }
        .nav-item { color: rgba(255,255,255,0.6); font-size: 1.2rem; cursor: pointer; }
        .nav-item.active { color: var(--primary); }

    </style>
</head>
<body>

<div id="loader">
    <div class="spinner"></div>
    <p style="margin-top: 15px; letter-spacing: 2px;">ASTORE MASTER HUB</p>
</div>

<header>
    <div style="font-weight: 800; color: var(--primary);">ASTORE <span style="color:white">PRO</span></div>
    <div id="time" style="font-size: 0.9rem; opacity: 0.8;"></div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=800"></div>
    </div>
</section>

<div class="container">
    <h3 style="margin-bottom: 5px;">Premium Services</h3>
    <p style="font-size: 0.8rem; opacity: 0.6; margin-bottom: 20px;">Select a service to start booking</p>

    <div class="grid">
        <div class="feature-box" onclick="selectService(this, 'Jeep')"><i class="fa-solid fa-car"></i>Jeep</div>
        <div class="feature-box" onclick="selectService(this, 'Hotel')"><i class="fa-solid fa-hotel"></i>Hotel</div>
        <div class="feature-box" onclick="selectService(this, 'Guide')"><i class="fa-solid fa-map-location-dot"></i>Guide</div>
        <div class="feature-box" onclick="selectService(this, 'Food')"><i class="fa-solid fa-utensils"></i>Food</div>
        <div class="feature-box" onclick="selectService(this, 'Camping')"><i class="fa-solid fa-tents"></i>Camp</div>
        <div class="feature-box" onclick="selectService(this, 'Photo')"><i class="fa-solid fa-camera"></i>Photo</div>
    </div>

    <div class="booking-card">
        <label style="font-size: 0.8rem; opacity: 0.8;">Travel Date</label>
        <input type="date" id="dt">
        <button class="btn" onclick="book()">Confirm via WhatsApp</button>
    </div>
</div>

<div class="bottom-nav">
    <div class="nav-item active"><i class="fa-solid fa-house"></i></div>
    <div class="nav-item"><i class="fa-solid fa-compass"></i></div>
    <div class="nav-item"><i class="fa-solid fa-calendar-check"></i></div>
    <div class="nav-item"><i class="fa-solid fa-user"></i></div>
</div>

<script>
    // Smooth Loader
    window.onload = () => {
        setTimeout(() => {
            document.getElementById('loader').style.opacity = '0';
            setTimeout(() => document.getElementById('loader').style.display='none', 800);
        }, 1500);
        
        // Block Past Dates
        document.getElementById('dt').min = new Date().toISOString().split("T")[0];
        document.getElementById('dt').valueAsDate = new Date();
    };

    // Digital Clock
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour:'2-digit', minute:'2-digit'});
    }, 1000);

    // Selection Logic
    let selectedService = "None";
    function selectService(el, service) {
        document.querySelectorAll('.feature-box').forEach(box => box.classList.remove('selected'));
        el.classList.add('selected');
        selectedService = service;
        
        // Haptic-like effect for mobile
        if(window.navigator.vibrate) window.navigator.vibrate(50);
    }

    // Advanced Booking
    function book() {
        let d = document.getElementById('dt').value;
        if(selectedService === "None") {
            alert("Please select a service first, sweetie!");
            return;
        }
        let msg = `*Astore Master Hub - New Booking*%0A---------------------------%0A*Service:* ${selectedService}%0A*Date:* ${d}%0A*Status:* Urgent Inquiry`;
        window.open(`https://wa.me/923171588489?text=${msg}`);
    }
</script>

</body>
</html>
