<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Explore the Heaven</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Poppins:wght@300;500&display=swap');

        :root { --primary: #0a3d31; --accent: #f39c12; --light: #fdfdfd; }
        * { box-sizing: border-box; }
        body { font-family: 'Poppins', sans-serif; margin: 0; background: #f0f2f1; color: #333; scroll-behavior: smooth; }

        /* Announcement Bar */
        .road-alert { background: #d32f2f; color: white; padding: 10px; font-size: 14px; position: fixed; top: 0; width: 100%; z-index: 2000; overflow: hidden; }

        /* Header & Hero */
        header { 
            height: 90vh; 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1621849400072-f554417f7051?auto=format&fit=crop&q=80&w=1500'); 
            background-size: cover; background-position: center; 
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; margin-top: 40px;
        }
        header h1 { font-family: 'Montserrat', sans-serif; font-size: clamp(2.5rem, 8vw, 5rem); margin: 0; }
        header p { font-size: 1.2rem; background: rgba(0,0,0,0.3); padding: 5px 20px; border-radius: 20px; }

        /* Weather Section */
        .weather-card { background: white; padding: 20px; border-radius: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); margin-top: -50px; display: inline-block; position: relative; z-index: 10; border-bottom: 5px solid var(--accent); }

        /* Content Container */
        .container { max-width: 1200px; margin: auto; padding: 60px 20px; }
        .section-title { text-align: center; font-family: 'Montserrat'; font-size: 2.5rem; color: var(--primary); margin-bottom: 50px; }

        /* Grid Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .card { background: white; border-radius: 20px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.08); transition: 0.5s; }
        .card:hover { transform: scale(1.03); }
        .card img { width: 100%; height: 250px; object-fit: cover; }
        .card-info { padding: 25px; }
        .card-info h3 { margin: 0; color: var(--primary); font-size: 1.5rem; }

        /* Booking Section */
        .booking-box { background: var(--primary); color: white; border-radius: 30px; padding: 50px; text-align: center; margin-top: 50px; }
        .btn { padding: 15px 40px; border-radius: 50px; text-decoration: none; font-weight: bold; display: inline-block; margin: 10px; transition: 0.3s; }
        .btn-wa { background: #25d366; color: white; border: 2px solid #25d366; }
        .btn-wa:hover { background: transparent; }
        .btn-call { background: var(--accent); color: white; }

        /* Floating Contact */
        .fab-wa { position: fixed; bottom: 20px; right: 20px; background: #25d366; color: white; width: 65px; height: 65px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 35px; box-shadow: 0 10px 20px rgba(0,0,0,0.2); z-index: 3000; }

        footer { background: #1a1a1a; color: white; text-align: center; padding: 50px 20px; margin-top: 100px; }
    </style>
</head>
<body>

<div class="road-alert">
    <marquee>⚠️ <strong>Road Update:</strong> Burzil Pass is currently open. 4x4 vehicles highly recommended for Minimarg. Contact us for NOC assistance.</marquee>
</div>

<header>
    <p>Welcome to Gilgit-Baltistan's Best Kept Secret</p>
    <h1>ASTORE VALLEY</h1>
    <div class="weather-card">
        <strong>Today's Forecast:</strong> <span id="weather">Loading Astore Weather...</span>
    </div>
</header>

<div class="container">
    <h2 class="section-title">Major Destinations</h2>
    <div class="grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1000" alt="Rama Lake">
            <div class="card-info">
                <h3>Rama Meadows</h3>
                <p>Jannat ka nazaara, ghane pine forests aur Nanga Parbat ke thandi hawayein.</p>
            </div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833?q=80&w=1000" alt="Rainbow Lake">
            <div class="card-info">
                <h3>Rainbow Lake</h3>
                <p>Dunya ki khoobsurat tareen lakes mein se aik, jo Minimarg ki wadi mein waqiye hai.</p>
            </div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1000" alt="Deosai">
            <div class="card-info">
                <h3>Deosai National Park</h3>
                <p>Land of Giants. Astore side se rasta Chillum se shuru hota hai.</p>
            </div>
        </div>
    </div>
</div>

<div class="container" id="services">
    <h2 class="section-title">Why Travel With Us?</h2>
    <div class="grid" style="text-align: center;">
        <div><i class="fas fa-jeep fa-3x" style="color:var(--accent)"></i><h3>Local Jeeps</h3><p>Authorized 4x4 drivers for Minimarg & Deosai.</p></div>
        <div><i class="fas fa-hotel fa-3x" style="color:var(--accent)"></i><h3>Hotels</h3><p>Best rates in Astore & Rama Guest Houses.</p></div>
        <div><i class="fas fa-id-card fa-3x" style="color:var(--accent)"></i><h3>NOC Support</h3><p>We help you with travel permissions for border areas.</p></div>
    </div>
</div>

<div class="container">
    <div class="booking-box">
        <h2>Ready for the Adventure of a Lifetime?</h2>
        <p>Humein abhi rabta karein aur apna Astore tour customize karwayein.</p>
        <a href="tel:+923171588489" class="btn btn-call"><i class="fas fa-phone"></i> Call +92 317 1588489</a>
        <a href="https://wa.me/923171588489?text=Hi, I saw your website. Help me plan my Astore trip!" class="btn btn-wa"><i class="fab fa-whatsapp"></i> WhatsApp Booking</a>
    </div>
</div>

<a href="https://wa.me/923171588489" class="fab-wa" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<footer>
    <p><strong>Astore Tourist Information Hub</strong></p>
    <p>Email: booking@astorehub.com | Contact: +92 317 1588489</p>
    <p style="opacity: 0.5; font-size: 12px; margin-top: 20px;">Designed for the people of Astore & Travelers worldwide.</p>
</footer>

<script>
    // Simple placeholder for weather - you can link this to a real API later
    document.getElementById('weather').innerText = "12°C - Sunny & Clear";
</script>

</body>
</html>
