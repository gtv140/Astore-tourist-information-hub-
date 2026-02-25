<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | The Ultimate Travel Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #0b3d2e; --accent: #d4af37; --light: #f4f7f6; --text: #2d3436; }
        * { box-sizing: border-box; scroll-behavior: smooth; }
        body { font-family: 'Playfair Display', serif; font-family: 'Poppins', sans-serif; margin: 0; background: var(--light); color: var(--text); }

        /* Header & Navigation */
        nav { background: white; padding: 1rem 5%; display: flex; justify-content: space-between; align-items: center; box-shadow: 0 2px 10px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 1000; }
        .logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); text-decoration: none; letter-spacing: 1px; }
        .nav-links a { text-decoration: none; color: var(--text); margin-left: 25px; font-weight: 500; font-size: 0.9rem; transition: 0.3s; }
        .nav-links a:hover { color: var(--accent); }

        /* Hero Section */
        .hero { 
            height: 80vh; 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?auto=format&fit=crop&q=80&w=1500'); 
            background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; padding: 0 20px;
        }
        .hero h1 { font-size: clamp(2.5rem, 6vw, 5rem); margin: 0; text-shadow: 2px 2px 10px rgba(0,0,0,0.3); }
        .hero p { font-size: 1.2rem; max-width: 700px; margin-top: 15px; }

        /* General Container */
        .container { max-width: 1200px; margin: auto; padding: 80px 20px; }
        .section-title { text-align: center; margin-bottom: 50px; }
        .section-title h2 { font-size: 2.5rem; color: var(--primary); margin: 0; }
        .section-title .bar { width: 50px; height: 3px; background: var(--accent); margin: 15px auto; }

        /* Features Grid */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .card { background: white; border-radius: 15px; overflow: hidden; box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
        .card img { width: 100%; height: 250px; object-fit: cover; transition: 0.5s; }
        .card:hover img { transform: scale(1.1); }
        .card-content { padding: 25px; }

        /* Itinerary Section */
        .itinerary-box { background: white; padding: 30px; border-left: 5px solid var(--primary); margin-bottom: 20px; }

        /* Testimonials */
        .testimonial-card { background: #fff; padding: 30px; border-radius: 10px; text-align: center; font-style: italic; border: 1px solid #eee; }
        .stars { color: var(--accent); margin-bottom: 10px; }

        /* Newsletter */
        .newsletter { background: var(--primary); color: white; text-align: center; padding: 60px 20px; border-radius: 20px; }
        .newsletter input { padding: 12px 20px; width: 250px; border-radius: 50px; border: none; outline: none; }
        .newsletter button { padding: 12px 30px; border-radius: 50px; border: none; background: var(--accent); color: white; font-weight: bold; cursor: pointer; }

        /* Floating Buttons */
        .wa-float { position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); z-index: 1000; text-decoration: none; }
        .back-top { position: fixed; bottom: 100px; right: 35px; background: #333; color: white; padding: 10px; border-radius: 5px; cursor: pointer; display: none; }

        footer { background: #1a1a1a; color: #999; padding: 60px 5% 20px; text-align: center; }
        .social-links a { color: white; margin: 0 10px; font-size: 1.5rem; text-decoration: none; }

        @media (max-width: 768px) { nav { flex-direction: column; } .nav-links { margin-top: 15px; } .nav-links a { margin: 0 10px; } }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <div class="nav-links">
        <a href="#destinations">Destinations</a>
        <a href="#itinerary">Trip Plans</a>
        <a href="#reviews">Reviews</a>
        <a href="#contact">Contact</a>
    </div>
</nav>

<section class="hero">
    <h1>Experience the Majestic Astore</h1>
    <p>From the crystalline waters of Rainbow Lake to the vastness of Deosai, your authentic northern adventure starts here.</p>
    <a href="https://wa.me/923171588489" style="background: var(--accent); color:white; padding: 15px 40px; text-decoration:none; border-radius:50px; font-weight:bold; margin-top:20px;">Book a Jeep Now</a>
</section>

<div class="container" id="destinations">
    <div class="section-title">
        <h2>Top Sightseeing</h2>
        <div class="bar"></div>
    </div>
    <div class="grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" alt="Rama">
            <div class="card-content"><h3>Rama Meadows</h3><p>Aik pur-sukoon wadi jahan Nanga Parbat ka rukh ankhon ko thandak deta hai.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" alt="Minimarg">
            <div class="card-content"><h3>Minimarg & Rainbow</h3><p>Pakistan ki sarhad par waqiye jannat ka tukra. Rainbow Lake lazmi dekhein.</p></div>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b" alt="Deosai">
            <div class="card-content"><h3>Deosai Plains</h3><p>High altitude plateau jahan dunya khatam hoti mehsoos hoti hai.</p></div>
        </div>
    </div>
</div>

<div class="container" id="itinerary" style="background: #fdfdfd;">
    <div class="section-title">
        <h2>Sample 3-Day Plan</h2>
        <div class="bar"></div>
    </div>
    <div class="itinerary-box">
        <h4>Day 1: Arrival & Rama Meadows</h4>
        <p>Astore city arrival, check-in to hotel, and afternoon visit to Rama Lake.</p>
    </div>
    <div class="itinerary-box">
        <h4>Day 2: Minimarg & Rainbow Lake</h4>
        <p>Early morning departure for Minimarg via Burzil Pass. Full day exploration.</p>
    </div>
    <div class="itinerary-box">
        <h4>Day 3: Deosai to Skardu / Return</h4>
        <p>Crossing Chillum Gate to Sheosar Lake and exploring the giants' land.</p>
    </div>
</div>

<div class="container" id="reviews">
    <div class="section-title">
        <h2>Guest Reviews</h2>
        <div class="bar"></div>
    </div>
    <div class="grid">
        <div class="testimonial-card">
            <div class="stars">★★★★★</div>
            <p>"Zabardast service! Inhon ne hamari Minimarg ki trip bohot asaan bana di."</p>
            <strong>- Salman from Islamabad</strong>
        </div>
        <div class="testimonial-card">
            <div class="stars">★★★★★</div>
            <p>"Highly recommended jeep drivers and guides. Very polite and helpful."</p>
            <strong>- Amna from Karachi</strong>
        </div>
    </div>
</div>

<div class="container">
    <div class="newsletter">
        <h2>Stay Updated</h2>
        <p>Subscribe to get road updates and seasonal discount alerts.</p>
        <input type="email" placeholder="Enter your email">
        <button>Subscribe</button>
    </div>
</div>

<footer id="contact">
    <div class="social-links">
        <a href="#"><i class="fab fa-facebook"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
        <a href="#"><i class="fab fa-youtube"></i></a>
    </div>
    <p style="margin-top: 20px;">Contact: +92 317 1588489 | Email: info@astorehub.com</p>
    <p>&copy; 2026 Astore Tourist Hub. All Rights Reserved.</p>
</footer>

<a href="https://wa.me/923171588489" class="wa-float" target="_blank"><i class="fab fa-whatsapp"></i></a>

<script>
    // Show back to top button on scroll
    window.onscroll = function() {
        if (document.body.scrollTop > 500 || document.documentElement.scrollTop > 500) {
            document.querySelector('.back-top').style.display = "block";
        } else {
            document.querySelector('.back-top').style.display = "none";
        }
    };
</script>

</body>
</html>
