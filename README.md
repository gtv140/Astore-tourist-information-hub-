<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Official</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --gold: #f59e0b; --light: #f9fafb; }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', sans-serif; }
        body { background: var(--light); color: #1f2937; line-height: 1.5; }

        /* Fix Header */
        nav { 
            background: white; padding: 15px 20px; display: flex; 
            justify-content: space-between; align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-weight: 800; color: var(--primary); font-size: 1.2rem; text-decoration: none; }

        /* Full-Width Mobile Hero */
        .hero { 
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=800');
            background-size: cover; background-position: center;
            height: 60vh; display: flex; flex-direction: column; 
            justify-content: center; align-items: center; text-align: center; color: white; padding: 20px;
        }
        .hero h1 { font-size: 2.2rem; margin-bottom: 10px; }
        .hero p { font-size: 1rem; opacity: 0.9; }

        /* Content Container */
        .container { padding: 30px 15px; max-width: 600px; margin: auto; }
        .section-title { font-size: 1.6rem; color: var(--primary); text-align: center; margin-bottom: 25px; }

        /* Clean Destination Cards */
        .card { 
            background: white; border-radius: 15px; overflow: hidden; 
            margin-bottom: 25px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: 1px solid #eee;
        }
        .card img { width: 100%; height: 200px; object-fit: cover; background: #ddd; }
        .card-body { padding: 20px; }
        .card-body h3 { font-size: 1.3rem; margin-bottom: 8px; color: var(--primary); }
        .card-body p { font-size: 0.9rem; color: #6b7280; margin-bottom: 15px; }
        .meta { display: flex; justify-content: space-between; font-weight: bold; font-size: 0.85rem; color: var(--gold); }

        /* Centered Booking Form */
        .booking-section { 
            background: var(--primary); border-radius: 20px; padding: 30px 20px; 
            color: white; margin-top: 20px;
        }
        .booking-section h2 { text-align: center; margin-bottom: 20px; font-size: 1.5rem; }
        .input-group { margin-bottom: 15px; }
        input, select { 
            width: 100%; padding: 14px; border-radius: 10px; border: none; 
            font-size: 1rem; outline: none; margin-top: 5px;
        }
        .submit-btn { 
            width: 100%; padding: 16px; background: #25d366; color: white; 
            border: none; border-radius: 10px; font-size: 1.1rem; font-weight: bold;
            cursor: pointer; margin-top: 10px; display: flex; align-items: center; justify-content: center; gap: 10px;
        }

        /* Float WhatsApp */
        .wa-float { 
            position: fixed; bottom: 20px; right: 20px; background: #25d366; 
            color: white; width: 55px; height: 55px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 28px; box-shadow: 0 4px 15px rgba(0,0,0,0.2); z-index: 2000;
        }

        footer { text-align: center; padding: 40px 20px; font-size: 0.8rem; color: #9ca3af; }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <a href="tel:+923171588489" style="color:var(--primary);"><i class="fas fa-phone-alt"></i></a>
</nav>

<div class="hero">
    <h1>Astore Valley</h1>
    <p>Premium 4x4 Jeep & Tour Services</p>
</div>

<div class="container">
    <h2 class="section-title">Top Destinations</h2>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama Meadows">
        <div class="card-body">
            <h3>Rama Meadows</h3>
            <p>Experience the lush green valley at the base of Nanga Parbat.</p>
            <div class="meta">
                <span><i class="fas fa-clock"></i> Full Day</span>
                <span>Rs. 8,500</span>
            </div>
        </div>
    </div>

    <div class="card">
        <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
        <div class="card-body">
            <h3>Minimarg Valley</h3>
            <p>Visit the iconic Rainbow Lake near the border mountains.</p>
            <div class="meta">
                <span><i class="fas fa-clock"></i> Full Day</span>
                <span>Rs. 14,000</span>
            </div>
        </div>
    </div>

    <div class="booking-section">
        <h2>Quick Booking</h2>
        <div class="input-group">
            <input type="text" id="name" placeholder="Your Full Name">
        </div>
        <div class="input-group">
            <select id="loc">
                <option>Rama Meadows</option>
                <option>Minimarg & Rainbow Lake</option>
                <option>Deosai Plains</option>
            </select>
        </div>
        <button class="submit-btn" onclick="bookNow()">
            <i class="fab fa-whatsapp"></i> WhatsApp Booking
        </button>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<footer>
    <p>Main Bazar Astore, Gilgit-Baltistan</p>
    <p>+92 317 1588489</p>
    <p style="margin-top:10px;">© 2026 Astore Tourist Hub</p>
</footer>

<script>
    function bookNow() {
        const name = document.getElementById('name').value;
        const loc = document.getElementById('loc').value;
        if(!name) { alert('Please enter your name'); return; }
        const text = `Hi, I am ${name}. I want to book a trip to ${loc}. Please guide me.`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(text)}`, '_blank');
    }
</script>

</body>
</html>
