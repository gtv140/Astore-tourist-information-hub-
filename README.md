<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | The Peak of Luxury</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&family=Poppins:wght@200;400;600&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #d4af37; --emerald: #064e3b; --dark: #0a0a0a; }
        * { box-sizing: border-box; }
        body { margin: 0; background: var(--dark); color: white; font-family: 'Poppins', sans-serif; overflow-x: hidden; }

        /* Cinematic Hero Section */
        .hero {
            height: 100vh; width: 100%;
            position: relative; overflow: hidden;
            display: flex; flex-direction: column; justify-content: center; align-items: center;
        }
        
        /* Background Parallax Image */
        .hero-bg {
            position: absolute; top: 0; left: 0; width: 100%; height: 120%;
            background: linear-gradient(to bottom, rgba(0,0,0,0.2), var(--dark)), 
                        url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=2000');
            background-size: cover; background-position: center;
            z-index: -1; transform: translateY(0); transition: 0.1s;
        }

        .hero-content { text-align: center; z-index: 10; padding: 20px; }
        .hero-content h1 { 
            font-family: 'Playfair Display', serif; font-size: clamp(3rem, 12vw, 8rem); 
            margin: 0; line-height: 0.9; color: var(--gold); font-style: italic;
            text-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
        .hero-content p { font-weight: 200; letter-spacing: 10px; text-transform: uppercase; margin-top: 20px; }

        /* Floating Cards Section */
        .container { max-width: 1200px; margin: -100px auto 100px; position: relative; z-index: 20; padding: 0 20px; }
        
        .luxury-card {
            background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1); border-radius: 40px;
            padding: 50px; display: grid; grid-template-columns: 1fr 1fr;
            gap: 50px; align-items: center; margin-bottom: 50px;
            box-shadow: 0 40px 100px rgba(0,0,0,0.5);
        }

        .luxury-card img { width: 100%; border-radius: 30px; transform: rotate(-2deg); box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
        .luxury-card:nth-child(even) { direction: rtl; }
        .luxury-card:nth-child(even) .text-box { direction: ltr; }

        .text-box h2 { font-family: 'Playfair Display'; font-size: 3rem; color: var(--gold); margin-bottom: 10px; }
        .text-box p { font-size: 1.1rem; line-height: 1.8; color: #ccc; }

        /* WhatsApp Pulse Button */
        .wa-button {
            position: fixed; bottom: 40px; right: 40px; background: #25d366;
            width: 70px; height: 70px; border-radius: 50%; display: flex;
            align-items: center; justify-content: center; font-size: 35px;
            color: white; text-decoration: none; z-index: 1000;
            box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7);
            animation: pulse-wa 2s infinite;
        }

        @keyframes pulse-wa {
            0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { transform: scale(1); box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
            100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }

        /* Responsive Mobile */
        @media (max-width: 768px) {
            .luxury-card { grid-template-columns: 1fr; padding: 30px; text-align: center; border-radius: 20px; }
            .luxury-card img { transform: rotate(0); }
            .hero-content h1 { font-size: 4rem; }
        }

        .scroll-down { position: absolute; bottom: 30px; left: 50%; transform: translateX(-50%); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 20%, 50%, 80%, 100% {transform: translateY(0) translateX(-50%);} 40% {transform: translateY(-10px) translateX(-50%);} 60% {transform: translateY(-5px) translateX(-50%);} }
    </style>
</head>
<body>

<section class="hero">
    <div class="hero-bg" id="parallax"></div>
    <div class="hero-content">
        <p>Heaven on Earth</p>
        <h1>Astore Valley</h1>
        <p>Premium 4x4 Adventures</p>
    </div>
    <div class="scroll-down"><i class="fas fa-chevron-down fa-2x" style="color:var(--gold)"></i></div>
</section>

<div class="container">
    <div class="luxury-card">
        <div class="text-box">
            <h2>Rama Lake</h2>
            <p>Jahan pine ke darakhton ki khushbu aur Nanga Parbat ka aks aapka intezar kar rahe hain. Humari premium jeeps aapko Rama Meadows tak sukoon se le jayengi.</p>
            <a href="https://wa.me/923171588489" style="color:var(--gold); text-decoration:none; font-weight:bold;">DISCOVER MORE →</a>
        </div>
        <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
    </div>

    <div class="luxury-card">
        <div class="text-box">
            <h2>Minimarg</h2>
            <p>Border area ki wo haseen wadi jahan Rainbow Lake apna rang badalti hai. Hum aapke NOC se lekar safar tak har cheez ka khayal rakhte hain.</p>
            <a href="https://wa.me/923171588489" style="color:var(--gold); text-decoration:none; font-weight:bold;">DISCOVER MORE →</a>
        </div>
        <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
    </div>

    <div style="background:var(--gold); color:black; padding:60px; border-radius:40px; text-align:center; margin-top:50px;">
        <h2 style="font-family:'Playfair Display'; font-size:3rem; margin:0;">Start Your Journey</h2>
        <p style="font-size:1.2rem; font-weight:bold;">923171588489 | Direct Booking Agency</p>
        <a href="tel:+923171588489" style="display:inline-block; padding:20px 50px; background:black; color:white; border-radius:50px; text-decoration:none; font-weight:bold; margin-top:20px;">CALL NOW</a>
    </div>
</div>

<a href="https://wa.me/923171588489" class="wa-button"><i class="fab fa-whatsapp"></i></a>

<script>
    window.addEventListener('scroll', function() {
        let offset = window.pageYOffset;
        document.getElementById('parallax').style.transform = 'translateY(' + (offset * 0.5) + 'px)';
    });
</script>

</body>
</html>
