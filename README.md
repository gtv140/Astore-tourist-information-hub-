<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Fixed & Live</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;700&family=Syne:wght@800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

    <style>
        :root { --primary: #00f2ff; --bg: #0b0f1a; --card: #161b2b; }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; }

        /* --- Header --- */
        nav { 
            padding: 20px; background: rgba(11, 15, 26, 0.95); 
            position: sticky; top: 0; z-index: 100; border-bottom: 1px solid rgba(255,255,255,0.1);
            text-align: center;
        }
        .logo { font-family: 'Syne'; font-size: 22px; color: var(--primary); text-transform: uppercase; }

        /* --- Hero --- */
        .hero {
            padding: 80px 20px; text-align: center;
            background: linear-gradient(rgba(0,0,0,0.5), var(--bg)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800&q=80');
            background-size: cover; background-position: center;
        }
        .hero h1 { font-family: 'Syne'; font-size: 45px; line-height: 1; margin-bottom: 10px; }

        /* --- Content --- */
        .container { padding: 20px; max-width: 800px; margin: 0 auto; }
        .section-title { font-family: 'Syne'; margin: 30px 0 20px; border-left: 4px solid var(--primary); padding-left: 10px; }

        /* --- Cards --- */
        .card { background: var(--card); border-radius: 20px; overflow: hidden; margin-bottom: 25px; border: 1px solid rgba(255,255,255,0.05); }
        .card img { width: 100%; height: 200px; object-fit: cover; }
        .card-body { padding: 20px; }
        .card-body h3 { color: var(--primary); margin-bottom: 10px; }

        /* --- Form --- */
        .form-box { background: #1f2937; padding: 25px; border-radius: 20px; margin-bottom: 100px; }
        input, select, textarea { width: 100%; padding: 15px; margin-bottom: 15px; border-radius: 10px; border: none; background: #0b0f1a; color: #fff; }
        .btn { width: 100%; padding: 15px; background: var(--primary); border: none; border-radius: 10px; font-weight: bold; color: #000; cursor: pointer; }

        /* --- Bottom Nav --- */
        .bottom-nav {
            position: fixed; bottom: 0; width: 100%; background: #000;
            display: flex; justify-content: space-around; padding: 20px;
            border-top: 1px solid rgba(255,255,255,0.1); z-index: 1000;
        }
        .bottom-nav a { color: #fff; opacity: 0.6; font-size: 22px; }
        .bottom-nav a.active { color: var(--primary); opacity: 1; }
    </style>
</head>
<body>

    <nav><div class="logo">ASTORE HUB</div></nav>

    <section class="hero">
        <p style="letter-spacing: 3px; font-size: 12px;">EXPLORE THE NORTH</p>
        <h1>BEYOND THE PEAKS</h1>
    </section>

    <div class="container">
        <h2 class="section-title">Destinations</h2>
        
        <div class="card">
            <img src="https://images.unsplash.com/photo-1627548613747-42506c11760c?auto=format&fit=crop&w=800&q=80" alt="Rama">
            <div class="card-body">
                <h3>Rama Meadows</h3>
                <p>Green paradise in the heart of Astore valley.</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1596465492651-789a68e36780?auto=format&fit=crop&w=800&q=80" alt="Hunza">
            <div class="card-body">
                <h3>Hunza Valley</h3>
                <p>Experience the culture and beauty of the Silk Road.</p>
            </div>
        </div>

        <h2 class="section-title" id="book">Book Your Tour</h2>
        <div class="form-box">
            <form id="tourForm">
                <input type="text" id="name" placeholder="Full Name" required>
                <input type="tel" id="phone" placeholder="WhatsApp Number" required>
                <select id="tour">
                    <option>Astore & Deosai</option>
                    <option>Hunza Valley</option>
                    <option>Skardu Trip</option>
                </select>
                <button type="submit" class="btn">Send Inquiry</button>
            </form>
        </div>
    </div>

    <div class="bottom-nav">
        <a href="#" class="active"><i class="fa-solid fa-house"></i></a>
        <a href="#book"><i class="fa-solid fa-map-location-dot"></i></a>
        <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
    </nav>

    <script>
        document.getElementById('tourForm').onsubmit = function(e) {
            e.preventDefault();
            const n = document.getElementById('name').value;
            const t = document.getElementById('tour').value;
            window.open(`https://wa.me/923171588489?text=Hi, I am ${n}. I want to book ${t} tour.`, '_blank');
        };
    </script>
</body>
</html>
