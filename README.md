<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Official Digital Guide</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;700&family=Syne:wght@800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root { --primary: #00f2ff; --bg: #05070a; --card: #111827; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; scroll-behavior: smooth; }

        /* Navigation */
        nav { padding: 15px 20px; background: rgba(5,7,10,0.95); position: sticky; top: 0; z-index: 1000; border-bottom: 1px solid rgba(255,255,255,0.1); display: flex; justify-content: space-between; align-items: center; }
        .logo { font-family: 'Syne'; font-size: 18px; color: var(--primary); letter-spacing: 1px; }

        /* Hero */
        .hero { padding: 120px 20px 60px; text-align: center; background: linear-gradient(rgba(0,0,0,0.7), var(--bg)), url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=1200&q=80'); background-size: cover; background-position: center; }
        .hero h1 { font-family: 'Syne'; font-size: 45px; text-transform: uppercase; margin-bottom: 10px; }

        .container { padding: 20px; max-width: 1000px; margin: 0 auto; }
        .section-title { font-family: 'Syne'; margin: 40px 0 20px; border-left: 5px solid var(--primary); padding-left: 15px; font-size: 24px; text-transform: uppercase; }

        /* About & Trust Section */
        .about-box { background: var(--card); padding: 25px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.05); line-height: 1.6; }
        .trust-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 15px; margin-top: 25px; }
        .trust-item { text-align: center; font-size: 12px; opacity: 0.8; }
        .trust-item i { font-size: 25px; color: var(--primary); margin-bottom: 10px; display: block; }

        /* Gallery */
        .gallery { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; }
        .gallery img { width: 100%; height: 160px; object-fit: cover; border-radius: 15px; transition: 0.3s; }
        .gallery img:hover { transform: scale(1.02); }

        /* FAQ Section */
        .faq-item { background: rgba(255,255,255,0.03); padding: 15px; border-radius: 12px; margin-bottom: 10px; border: 1px solid rgba(255,255,255,0.05); }
        .faq-item h4 { font-size: 14px; color: var(--primary); margin-bottom: 5px; }
        .faq-item p { font-size: 13px; opacity: 0.7; }

        /* Form */
        .form-box { background: var(--card); padding: 30px; border-radius: 25px; margin: 40px 0 100px; border: 1px solid var(--primary); }
        input, select, textarea { width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px; border: none; background: #05070a; color: #fff; font-size: 16px; outline: none; }
        .btn { width: 100%; padding: 18px; background: var(--primary); border: none; border-radius: 12px; font-weight: 800; color: #000; cursor: pointer; text-transform: uppercase; letter-spacing: 1px; }

        /* Mobile Dock */
        .dock { position: fixed; bottom: 0; width: 100%; background: #000; display: flex; justify-content: space-around; padding: 12px 0 25px; border-top: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .dock a { color: #fff; opacity: 0.5; font-size: 18px; display: flex; flex-direction: column; align-items: center; text-decoration: none; }
        .dock a span { font-size: 9px; margin-top: 5px; text-transform: uppercase; letter-spacing: 1px; }
        .dock a.active { color: var(--primary); opacity: 1; }

        /* Map Fix */
        .map-frame { height: 300px; border-radius: 20px; overflow: hidden; margin-top: 30px; border: 1px solid rgba(255,255,255,0.1); }
        .map-frame iframe { filter: invert(90%) hue-rotate(180deg) brightness(0.9); }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE<span>HUB</span></div>
        <a href="tel:+923171588489" style="color:var(--primary); font-size: 20px;"><i class="fa-solid fa-phone-volume"></i></a>
    </nav>

    <section class="hero">
        <p style="letter-spacing: 6px; font-size: 9px; opacity: 0.7; font-weight: bold;">OFFICIAL TOURISM GUIDE</p>
        <h1>THE ASTORE HUB</h1>
    </section>

    <div class="container">
        
        <h2 class="section-title">About Our Hub</h2>
        <div class="about-box">
            <p>Welcome to <strong>Astore Tourist Information Hub</strong>. We are a local initiative dedicated to showcasing the hidden beauty of Gilgit-Baltistan. Our mission is to provide authentic travel information and seamless tour services for explorers worldwide.</p>
            <div class="trust-grid">
                <div class="trust-item"><i class="fa-solid fa-shield-halved"></i><p>Safe Travel</p></div>
                <div class="trust-item"><i class="fa-solid fa-map-pin"></i><p>Local Guides</p></div>
                <div class="trust-item"><i class="fa-solid fa-clock"></i><p>24/7 Support</p></div>
            </div>
        </div>

        <h2 class="section-title">Visual Tour</h2>
        <div class="gallery">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&w=500" alt="Rama Meadows">
            <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?auto=format&w=500" alt="Hunza Valley">
            <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&w=500" alt="Deosai Plains">
            <img src="https://images.unsplash.com/photo-1622324341735-906567087679?auto=format&w=500" alt="Skardu">
        </div>

        <h2 class="section-title">Travel FAQs</h2>
        <div class="faq-item">
            <h4>Best time to visit?</h4>
            <p>May to October is ideal for Astore and Deosai as the roads are clear from snow.</p>
        </div>
        <div class="faq-item">
            <h4>Is 4x4 Jeep mandatory?</h4>
            <p>For Rama Meadows and Deosai, a 4x4 Jeep is highly recommended due to off-road tracks.</p>
        </div>

        <h2 class="section-title" id="book">Reserve Your Spot</h2>
        <div class="form-box">
            <form id="proForm">
                <input type="text" id="name" placeholder="Enter Your Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai Explorer</option>
                    <option>Hunza Valley Grand Tour</option>
                    <option>Skardu Adventure</option>
                    <option>Custom GB Trip</option>
                </select>
                <textarea id="msg" placeholder="Tell us about your group size and dates..."></textarea>
                <button type="submit" class="btn">Connect to Hub</button>
            </form>
        </div>

        <div class="map-frame">
            <iframe src="http://googleusercontent.com/maps.google.com/6" width="100%" height="100%" frameborder="0"></iframe>
        </div>

    </div>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house"></i><span>Home</span></a>
        <a href="#book"><i class="fa-solid fa-compass"></i><span>Explore</span></a>
        <a href="#book"><i class="fa-solid fa-calendar-plus"></i><span>Book</span></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i><span>WhatsApp</span></a>
    </div>

    <script>
        document.getElementById('proForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            const text = `*HUB INQUIRY*\nName: ${n}\nTour: ${t}\nSent from Astore Hub Website.`;
            window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
        };
    </script>
</body>
</html>
