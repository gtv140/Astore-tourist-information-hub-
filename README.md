<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Premium GB Guide</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;700&family=Syne:wght@800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root { --primary: #00f2ff; --bg: #05070a; --card: #111827; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; scroll-behavior: smooth; }

        /* Navigation */
        nav { padding: 20px; background: rgba(5,7,10,0.9); position: sticky; top: 0; z-index: 100; border-bottom: 1px solid rgba(255,255,255,0.1); display: flex; justify-content: space-between; align-items: center; }
        .logo { font-family: 'Syne'; font-size: 20px; color: var(--primary); }

        /* Hero */
        .hero { padding: 100px 20px; text-align: center; background: linear-gradient(rgba(0,0,0,0.7), var(--bg)), url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=1200&q=80'); background-size: cover; background-position: center; }
        .hero h1 { font-family: 'Syne'; font-size: 50px; margin-bottom: 10px; text-transform: uppercase; }

        .container { padding: 20px; max-width: 1100px; margin: 0 auto; }
        .section-title { font-family: 'Syne'; margin: 40px 0 20px; border-left: 5px solid var(--primary); padding-left: 15px; font-size: 28px; }

        /* Services Row */
        .services { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 15px; margin-bottom: 40px; }
        .service-card { background: var(--card); padding: 20px; border-radius: 15px; text-align: center; border: 1px solid rgba(255,255,255,0.05); }
        .service-card i { font-size: 30px; color: var(--primary); margin-bottom: 10px; }
        .service-card p { font-size: 12px; font-weight: bold; }

        /* Photo Gallery */
        .gallery { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; }
        .gallery img { width: 100%; height: 150px; object-fit: cover; border-radius: 10px; }

        /* Booking Form */
        .form-box { background: var(--card); padding: 30px; border-radius: 25px; margin: 40px 0 100px; border: 1px solid var(--primary); }
        input, select, textarea { width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 12px; border: none; background: #05070a; color: #fff; font-size: 16px; }
        .btn { width: 100%; padding: 18px; background: var(--primary); border: none; border-radius: 12px; font-weight: 800; color: #000; cursor: pointer; text-transform: uppercase; }

        /* Bottom Navigation Icons */
        .dock { position: fixed; bottom: 0; width: 100%; background: #000; display: flex; justify-content: space-around; padding: 15px; border-top: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .dock a { color: #fff; opacity: 0.6; font-size: 20px; display: flex; flex-direction: column; align-items: center; text-decoration: none; }
        .dock a span { font-size: 10px; margin-top: 5px; }
        .dock a.active { color: var(--primary); opacity: 1; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">ASTORE HUB</div>
        <a href="tel:+923171588489" style="color:var(--primary); text-decoration:none;"><i class="fa-solid fa-phone"></i></a>
    </nav>

    <section class="hero">
        <p style="letter-spacing: 5px; font-size: 10px;">WELCOME TO THE NORTH</p>
        <h1>ASTORE VALLEY</h1>
    </section>

    <div class="container">
        
        <div class="services">
            <div class="service-card"><i class="fa-solid fa-jeep"></i><p>4x4 Jeeps</p></div>
            <div class="service-card"><i class="fa-solid fa-hotel"></i><p>Hotel Booking</p></div>
            <div class="service-card"><i class="fa-solid fa-person-hiking"></i><p>Tours Guide</p></div>
        </div>

        <h2 class="section-title">Destinations Gallery</h2>
        <div class="gallery">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&w=400" alt="Rama">
            <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?auto=format&w=400" alt="Hunza">
            <img src="https://images.unsplash.com/photo-1549410148-97171f644be3?auto=format&w=400" alt="Deosai">
            <img src="https://images.unsplash.com/photo-1622324341735-906567087679?auto=format&w=400" alt="Skardu">
        </div>

        <h2 class="section-title" id="book">Plan Your Adventure</h2>
        <div class="form-box">
            <form id="tourForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai safari</option>
                    <option>Hunza Valley Trip</option>
                    <option>Skardu Adventure</option>
                    <option>Custom Tour</option>
                </select>
                <textarea id="msg" placeholder="Tell us more about your group..."></textarea>
                <button type="submit" class="btn">Book Now</button>
            </form>
        </div>
    </div>

    <div class="dock">
        <a href="#" class="active"><i class="fa-solid fa-house"></i><span>Home</span></a>
        <a href="#book"><i class="fa-solid fa-map"></i><span>Explore</span></a>
        <a href="#book"><i class="fa-solid fa-calendar-check"></i><span>Book</span></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i><span>Chat</span></a>
    </div>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            window.open(`https://wa.me/923171588489?text=Hi, I am ${n}. I am interested in ${t}.`, '_blank');
        };
    </script>
</body>
</html>
