<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{background:#f9f9f9;color:#111;line-height:1.6;}
a{text-decoration:none;color:#111;}
h2,h3{font-family:'Orbitron',sans-serif;color:#222;}
.container{max-width:1100px;margin:20px auto;padding:15px;}
header{background:#1e90ff;color:#fff;padding:15px 10px;text-align:center;border-radius:10px;}
header h1{font-size:28px;}
nav{margin-top:10px;text-align:center;}
nav a{margin:0 10px;color:#1e90ff;font-weight:600;}
section{margin:30px 0;padding:15px;background:#fff;border-radius:10px;box-shadow:0 0 10px rgba(0,0,0,0.1);}
.section-title{margin-bottom:15px;color:#1e90ff;}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:15px;}
.card{border-radius:10px;overflow:hidden;box-shadow:0 0 10px rgba(0,0,0,0.1);transition:0.3s;}
.card img{width:100%;display:block;}
.card-body{padding:10px;}
.card-body h3{color:#1e90ff;margin-bottom:5px;}
.card-body p{font-size:14px;color:#555;}
.button{display:inline-block;background:#1e90ff;color:#fff;padding:8px 12px;margin-top:10px;border-radius:5px;font-weight:600;transition:0.3s;}
.button:hover{background:#0b60c3;}
footer{margin-top:30px;text-align:center;color:#555;font-size:14px;}
.contact-info a{display:block;color:#1e90ff;margin:5px 0;}
@media(max-width:600px){.cards{grid-template-columns:1fr;}}
</style>
</head>
<body>

<header>
  <h1>Astore Tourist Information Hub</h1>
  <p>Explore the beauty of Astore Valley | Owner: Asim KhanZai</p>
  <nav>
    <a href="#rooms">Rooms</a>
    <a href="#cars">Car Booking</a>
    <a href="#packages">Packages</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<div class="container">

<section id="rooms">
  <h2 class="section-title">Room Booking</h2>
  <div class="cards">
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?hotel,room" alt="Standard Room">
      <div class="card-body">
        <h3>Standard Room</h3>
        <p>Comfortable room with basic amenities. Suitable for 2 persons.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Standard Room">Book via WhatsApp</a>
      </div>
    </div>
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?luxury,room" alt="Luxury Room">
      <div class="card-body">
        <h3>Luxury Room</h3>
        <p>Spacious room with premium amenities. Includes breakfast and WiFi.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Luxury Room">Book via WhatsApp</a>
      </div>
    </div>
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?suite,hotel" alt="Family Suite">
      <div class="card-body">
        <h3>Family Suite</h3>
        <p>Perfect for family stay with multiple beds and living area.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Family Suite">Book via WhatsApp</a>
      </div>
    </div>
  </div>
</section>

<section id="cars">
  <h2 class="section-title">Car Booking</h2>
  <div class="cards">
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?car,sedan" alt="Corolla">
      <div class="card-body">
        <h3>Corolla</h3>
        <p>Comfortable 4-seater car for city rides and nearby sightseeing.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Corolla">Book via WhatsApp</a>
      </div>
    </div>
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?car,SUV" alt="Prado">
      <div class="card-body">
        <h3>Prado</h3>
        <p>Premium SUV suitable for hilly terrain and group trips.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Prado">Book via WhatsApp</a>
      </div>
    </div>
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?van,hiace" alt="Hiace">
      <div class="card-body">
        <h3>Hiace</h3>
        <p>Van for group travel, 8-10 passengers comfortable seating.</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Hiace">Book via WhatsApp</a>
      </div>
    </div>
  </div>
</section>

<section id="packages">
  <h2 class="section-title">Tour Packages</h2>
  <div class="cards">
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?mountain,travel" alt="Adventure">
      <div class="card-body">
        <h3>Adventure Package</h3>
        <p>5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking | Explore valleys & mountains</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Adventure Package">Book via WhatsApp</a>
      </div>
    </div>
    <div class="card">
      <img src="https://source.unsplash.com/400x250/?luxury,travel" alt="Luxury">
      <div class="card-body">
        <h3>Luxury Package</h3>
        <p>4 Nights, 5 Days | Luxury Room + Car + Guide | Premium sightseeing</p>
        <a class="button" href="https://wa.me/923171588489?text=I want to book Luxury Package">Book via WhatsApp</a>
      </div>
    </div>
  </div>
</section>

<section id="gallery">
  <h2 class="section-title">Gallery</h2>
  <div class="cards">
    <div class="card"><img src="https://source.unsplash.com/400x250/?mountain" alt="Astore Mountain"></div>
    <div class="card"><img src="https://source.unsplash.com/400x250/?river" alt="River"></div>
    <div class="card"><img src="https://source.unsplash.com/400x250/?valley" alt="Valley"></div>
    <div class="card"><img src="https://source.unsplash.com/400x250/?hiking" alt="Hiking"></div>
  </div>
</section>

<section id="contact">
  <h2 class="section-title">Contact & Info</h2>
  <p>Astore Tourist Information Hub provides guided tours, hotel bookings, and transport in Astore Valley.</p>
  <div class="contact-info">
    <a href="mailto:mohammadasimkhan2746@gmail.com"><i class="fa-solid fa-envelope"></i> Email</a>
    <a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i> WhatsApp</a>
    <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr"><i class="fa-brands fa-facebook"></i> Facebook</a>
    <a href="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300" target="_blank"><i class="fa-solid fa-map-location-dot"></i> Location</a>
  </div>
</section>

</div>

<footer>
  &copy; 2026 Astore Tourist Hub | Designed by Sweetie
</footer>

</body>
</html>
