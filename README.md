<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Ultimate Experience</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #064e3b; --accent: #fbbf24; --bg: #f3f4f6; }
        body { font-family: 'Segoe UI', Roboto, sans-serif; margin: 0; background: var(--bg); scroll-behavior: smooth; overflow-x: hidden; }

        /* Modern Video Hero */
        .hero { 
            position: relative; height: 85vh; color: white; 
            display: flex; flex-direction: column; justify-content: center; align-items: center; 
            text-align: center; background: #000;
        }
        .hero-overlay { 
            position: absolute; top: 0; left: 0; width: 100%; height: 100%; 
            background: rgba(0,0,0,0.5); z-index: 1; 
        }
        .hero-content { z-index: 2; padding: 20px; }
        .hero h1 { font-size: 4.5rem; margin: 0; font-weight: 800; letter-spacing: -2px; }

        /* Safety Checklist Section */
        .checklist { background: white; padding: 40px; border-radius: 20px; border-left: 10px solid #ef4444; margin-top: -60px; position: relative; z-index: 5; box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1); }
        
        /* Auto-Slider/Gallery */
        .slider-container { display: flex; overflow-x: auto; gap: 20px; padding: 20px 0; scroll-snap-type: x mandatory; }
        .slide { min-width: 300px; height: 400px; border-radius: 20px; scroll-snap-align: start; position: relative; overflow: hidden; }
        .slide img { width: 100%; height: 100%; object-fit: cover; transition: 0.5s; }
        .slide:hover img { transform: scale(1.1); }
        .slide-text { position: absolute; bottom: 0; padding: 20px; background: linear-gradient(transparent, rgba(0,0,0,0.8)); color: white; width: 100%; }

        /* Video Section */
        .video-box { position: relative; padding-bottom: 56.25%; height: 0; border-radius: 20px; overflow: hidden; margin: 40px 0; }
        .video-box iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }

        /* WhatsApp Button Pulse Effect */
        .pulse { animation: pulse-animation 2s infinite; }
        @keyframes pulse-animation {
            0% { box-shadow: 0 0 0 0px rgba(37, 211, 102, 0.7); }
            100% { box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
        }

        .fab-wa { position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white; width: 70px; height: 70px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 35px; z-index: 9999; text-decoration: none; }
        .container { max-width: 1200px; margin: auto; padding: 40px 20px; }
    </style>
</head>
<body>

<div class="hero">
    <div class="hero-overlay"></div>
    <div class="hero-content">
        <h1>EXPLORE ASTORE</h1>
        <p style="font-size: 1.5rem;">Where the Mountains Meet the Soul</p>
        <a href="tel:+923171588489" style="background: var(--accent); color: black; padding: 15px 40px; border-radius: 50px; text-decoration: none; font-weight: bold; font-size: 1.2rem;">Book Your Jeep Now</a>
    </div>
</div>

<div class="container">
    <div class="checklist">
        <h2 style="color: #ef4444; margin-top: 0;"><i class="fas fa-exclamation-triangle"></i> Essential Travel Checklist</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px;">
            <div>✅ CNIC Originals (For Checkposts)</div>
            <div>✅ Warm Clothes (Even in Summer)</div>
            <div>✅ Motion Sickness Medicines</div>
            <div>✅ Power Banks (Electricity issues)</div>
        </div>
    </div>

    <h2 style="text-align: center; margin-top: 80px;">Astore Visual Journey</h2>
    <div class="video-box">
        <iframe src="https://www.youtube.com/embed/P-9_p_9U16k" frameborder="0" allowfullscreen></iframe>
    </div>

    <h2 style="text-align: center;">Our Location Hub</h2>
    <div style="border-radius: 20px; overflow: hidden; box-shadow: 0 10px 15px rgba(0,0,0,0.1);">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d105263.344447477!2d74.78772921660157!3d35.33400266056589!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38e663da67184285%3A0x6b043d9a3e63989c!2sAstore%20Valley!5e0!3m2!1sen!2spk!4v1700000000000!5m2!1sen!2spk" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </div>
</div>

<div class="container">
    <h2 style="text-align: center;">Quick Gallery</h2>
    <div class="slider-container">
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?q=80&w=1000" alt="Rama">
            <div class="slide-text"><h3>Rama Lake</h3><p>Peaceful & Serene</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?q=80&w=1000" alt="Minimarg">
            <div class="slide-text"><h3>Minimarg</h3><p>The Green Heaven</p></div>
        </div>
        <div class="slide">
            <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?q=80&w=1000" alt="Deosai">
            <div class="slide-text"><h3>Deosai</h3><p>Roof of the World</p></div>
        </div>
    </div>
</div>

<div style="background: var(--primary); color: white; padding: 80px 20px; text-align: center; margin-top: 50px;">
    <h2>Need a Custom Tour Plan?</h2>
    <p>923171588489 - Dial for 24/7 Information</p>
    <a href="https://wa.me/923171588489" style="background: white; color: var(--primary); padding: 15px 40px; border-radius: 50px; text-decoration: none; font-weight: bold;">Get a Quote</a>
</div>

<a href="https://wa.me/923171588489" class="fab-wa pulse" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<footer style="text-align: center; padding: 40px; color: #666;">
    <p>&copy; 2026 Astore Tourist Hub | Built for the Mountains</p>
</footer>

</body>
</html>
