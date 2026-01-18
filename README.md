<Astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
body{margin:0;font-family:'Poppins',sans-serif;color:#333;background:#f2f2f2;}
a{text-decoration:none;color:inherit;}
header{position:relative;text-align:center;color:#fff;}
header img{width:100%;max-height:250px;object-fit:cover;filter:brightness(0.6);}
header h1{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);font-size:28px;background:rgba(0,0,0,0.4);padding:10px 20px;border-radius:10px;}
section{padding:20px;}
h2{color:#004080;margin-bottom:15px;text-align:center;}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:15px;}
.package{background:#fff;border-radius:10px;box-shadow:0 0 10px rgba(0,0,0,0.1);overflow:hidden;transition:0.3s;}
.package img{width:100%;height:130px;object-fit:cover;}
.package h3{padding:10px;color:#004080;font-size:18px;}
.package p{padding:0 10px 10px;color:#555;font-size:14px;}
button.whatsapp-btn{width:100%;padding:12px;background:#25d366;color:#fff;border:none;border-radius:8px;font-size:16px;margin:10px 0;cursor:pointer;transition:0.3s;}
button.whatsapp-btn:hover{background:#1ebe57;}
.contact-info{display:flex;flex-direction:column;gap:8px;text-align:center;margin-top:10px;}
.contact-info a{color:#004080;transition:0.3s;}
.contact-info a:hover{color:#0077cc;}
@media(max-width:500px){header h1{font-size:20px;}}
</style>
</head>
<body>

<header>
<img src="https://images.unsplash.com/photo-1587502536263-9bfb22b504b2?auto=format&fit=crop&w=1200&q=80" alt="Astore Mountains">
<h1>Astore Tourist Hub</h1>
</header>

<section id="about">
<h2>About Astore Tourist Hub</h2>
<p style="text-align:center;max-width:500px;margin:0 auto;">Discover the breathtaking valleys, majestic mountains, and unique culture of Astore. Our hub provides essential tourist information, local guidance, accommodation details, and car rentals to make your journey safe and unforgettable.</p>
</section>

<section id="packages">
<h2>Tour Packages</h2>
<div class="packages">
  <div class="package">
    <img src="https://images.unsplash.com/photo-1578271315466-080c02d0e6b5?auto=format&fit=crop&w=400&q=80" alt="Basic Package">
    <h3>Basic Package</h3>
    <p>2 Nights, 3 Days<br>Standard Room + Local Guide</p>
    <button class="whatsapp-btn" onclick="bookWhatsApp('Basic Package')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
  </div>
  <div class="package">
    <img src="https://images.unsplash.com/photo-1613414518245-0b9da6e9e44e?auto=format&fit=crop&w=400&q=80" alt="Luxury Package">
    <h3>Luxury Package</h3>
    <p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p>
    <button class="whatsapp-btn" onclick="bookWhatsApp('Luxury Package')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
  </div>
  <div class="package">
    <img src="https://images.unsplash.com/photo-1608897013034-b7e0d5b4c146?auto=format&fit=crop&w=400&q=80" alt="Adventure Package">
    <h3>Adventure Package</h3>
    <p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p>
    <button class="whatsapp-btn" onclick="bookWhatsApp('Adventure Package')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
  </div>
</div>
</section>

<section id="contact">
<h2>Contact & Bookings</h2>
<div class="contact-info">
<a href="mailto:mohammadasimkhan2746@gmail.com"><i class="fa-solid fa-envelope"></i> Email Us</a>
<a href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i> WhatsApp</a>
<a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank"><i class="fa-brands fa-facebook"></i> Facebook</a>
</div>
</section>

<section id="map">
<h2>Find Us on Map</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</section>

<script>
function bookWhatsApp(packageName){
  const msg=`Hello! I want to book the ${packageName} at Astore Tourist Hub.`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
}
</script>

</body>
</html>
