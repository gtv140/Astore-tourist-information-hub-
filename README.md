<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub | Official Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #f59e0b; --bg: #f8fafc; --card: #ffffff; --text: #0f172a; }
        .dark { --bg: #0f172a; --card: #1e293b; --text: #f8fafc; --primary: #10b981; }
        
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
        body { background: var(--bg); color: var(--text); overflow-x: hidden; font-size: 14px; }

        header { position: sticky; top: 0; z-index: 9000; background: rgba(255,255,255,0.95); backdrop-filter: blur(10px); padding: 8px 15px; display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(0,0,0,0.05); }

        /* Smooth Slider Fix */
        .hero { position: relative; height: 30vh; width: 100%; overflow: hidden; background: #000; }
        .slider { display: flex; width: 400%; height: 100%; animation: slide 12s infinite ease-in-out; }
        .slide { width: 100%; height: 100%; position: relative; }
        .slide img { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.75); }
        
        @keyframes slide { 
            0%, 20% { transform: translateX(0%); } 
            25%, 45% { transform: translateX(-25%); } 
            50%, 70% { transform: translateX(-50%); } 
            75%, 95% { transform: translateX(-75%); } 
            100% { transform: translateX(0%); } 
        }

        .container { padding: 10px 15px; }

        .card { background: var(--card); border-radius: 15px; padding: 15px; margin-bottom: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); }

        .section-title { margin: 15px 0 8px; font-size: 1rem; font-weight: 800; color: var(--primary); display: flex; align-items: center; gap: 6px; }

        /* Compact Booking UI */
        .booking-ui { background: var(--primary); color: white; border-radius: 20px; padding: 18px; }
        .booking-ui label { font-size: 0.7rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; }
        input, select { width: 100%; padding: 10px; border-radius: 10px; border: none; margin: 5px 0 12px; font-size: 0.85rem; }

        .btn { padding: 12px; border-radius: 12px; text-decoration: none; font-weight: 700; display: flex; align-items: center; justify-content: center; gap: 8px; border: none; width: 100%; cursor: pointer; }
        .wa-btn { background: #25d366; color: white; }

        .fab { position: fixed; bottom: 15px; right: 15px; width: 44px; height: 44px; border-radius: 12px; background: var(--primary); color: white; display: flex; align-items: center; justify-content: center; box-shadow: 0 5px 15px rgba(0,0,0,0.2); z-index: 9999; border: none; }

        footer { text-align: center; padding: 20px; opacity: 0.6; font-size: 0.7rem; }
    </style>
</head>
<body>

<header>
    <div style="font-weight: 900; font-size: 0.95rem;">ASTORE <span style="color:var(--primary)">HUB</span></div>
    <div id="time" style="font-size: 0.7rem; font-weight: 700; color: var(--primary);">--:--</div>
</header>

<section class="hero">
    <div class="slider">
        <div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800"></div>
        <div class="slide"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=800"></div>
    </div>
</section>

<div class="container">
    <div class="section-title"><i class="fas fa-calendar-alt"></i> Quick Booking</div>
    <div class="booking-ui">
        <label>Destination</label>
        <select id="srv">
            <option>Minimarg & Rainbow Lake</option>
            <option>Rama Meadows Night</option>
            <option>Deosai Safari</option>
        </select>
        <label>Travel Date</label>
        <input type="date" id="dt">
        <button class="btn wa-btn" onclick="book()">
            <i class="fab fa-whatsapp"></i> REQUEST QUOTE
        </button>
    </div>
</div>

<button class="fab" onclick="document.body.classList.toggle('dark')"><i class="fas fa-moon"></i></button>

<footer>
    © 2026 ASTORE HUB | Built for Mobile<br>
    Sweetie, isse update karo aur screenshots check karo! 😘
</footer>

<script>
    setInterval(() => {
        document.getElementById('time').innerText = new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }, 1000);

    function book() {
        const s = document.getElementById('srv').value;
        const d = document.getElementById('dt').value;
        const msg = `Hi! Booking for ${s} on ${d || 'soon'}. Guide me sweetie!`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
    }
</script>
</body>
</html>
