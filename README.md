<Astore Tourist>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<meta name="description" content="Astore Tourist Information Hub by Asim Khanzai. Book rooms, cars, and tour packages easily. Explore Astore with professional guide.">
<meta name="keywords" content="Astore, Tourism, Tourist Hub, Room Booking, Car Booking, Tour Packages, Asim Khanzai">
<meta name="author" content="Asim Khanzai">

<!-- Open Graph -->
<meta property="og:title" content="Astore Tourist Information Hub">
<meta property="og:description" content="Book rooms, cars, and tours in Astore with Asim Khanzai. Professional tourist guide services.">
<meta property="og:image" content="https://i.ibb.co/2jL0MDK/mountains.jpg">
<meta property="og:url" content="https://yourwebsite.com">
<meta property="og:type" content="website">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Astore Tourist Information Hub">
<meta name="twitter:description" content="Book rooms, cars, and tours in Astore with Asim Khanzai. Professional tourist guide services.">
<meta name="twitter:image" content="https://i.ibb.co/2jL0MDK/mountains.jpg">

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

<style>
/* Reset */
*{margin:0;padding:0;box-sizing:border-box;}

/* Body & font */
body{font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;}

/* Premium neon animated background */
.bg-animate{
  position:fixed;width:100%;height:100%;
  background:linear-gradient(270deg,#000428,#004e92,#001f3f,#000428);
  background-size:800% 800%;
  animation:gradientBG 20s ease infinite;
  z-index:-2;
}
@keyframes gradientBG{
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
}

/* Floating particles */
.particle{
  position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;
  opacity:0.7;animation:floatUp linear infinite;
}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}

/* Container */
.container{
  max-width:1100px;margin:60px auto;
  background:rgba(0,0,0,0.4);padding:30px;
  border-radius:20px;backdrop-filter:blur(8px);box-shadow:0 0 30px #00eaff;
}

/* Logo & text */
.logo{
  text-align:center;font-size:42px;font-weight:700;
  color:#00eaff;text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;
  margin-bottom:20px;font-family:'Orbitron',sans-serif;
}

/* Hero slideshow */
.slideshow-container{position:relative;margin:auto;overflow:hidden;border-radius:15px;box-shadow:0 0 30px #00eaff;margin-bottom:30px;}
.slide{display:none;}
.slide img{width:100%;border-radius:15px;transition:all 1s ease-in-out;}

/* Hero text */
.hero-text{text-align:center;margin-bottom:30px;}
.hero-text p{font-size:17px;color:#a7f5ff;text-shadow:0 0 8px #00eaff;}

/* Forms */
label{margin-top:12px;display:block;font-weight:500;}
input,select{width:100%;padding:12px;margin-top:6px;border-radius:10px;border:none;background:rgba(255,255,255,0.15);color:#fff;font-size:15px;}
button{width:100%;padding:14px;margin-top:18px;border:none;border-radius:10px;background:#00eaff;color:#000;font-size:18px;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00bcd4;}

/* Packages */
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;margin-top:20px;}
.package{
  background:rgba(0,0,0,0.35);padding:20px;border-radius:15px;
  box-shadow:0 0 20px #00eaff;
  text-align:center;transition:0.3s;
}
.package:hover{transform:scale(1.05);box-shadow:0 0 30px #00ffff;}
.package h3{text-shadow:0 0 10px #00eaff;font-family:'Orbitron',sans-serif;}
.package p{font-size:14px;color:#a7f5ff;}

/* Map */
.map-container{margin-top:30px;border-radius:15px;overflow:hidden;box-shadow:0 0 25px #00eaff;}

/* Contact */
.contact{margin-top:30px;text-align:center;font-size:16px;}
.contact i{margin-right:8px;color:#00eaff;}

/* Social share */
.social-share{margin-top:20px;text-align:center;}
.social-share a{margin:0 10px;font-size:28px;color:#00eaff;text-decoration:none;transition:0.3s;}
.social-share a:hover{color:#00fff0;transform:scale(1.2);}

/* WhatsApp button */
.whatsapp-btn{position:fixed;right:20px;bottom:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
@media (max-width:768px){.logo{font-size:32px;}.packages{grid-template-columns:1fr;}}
</style>
</head>
<body>
<div class="bg-animate"></div>

<!-- Floating particles -->
<script>
for(let i=0;i<50;i++){
    let p=document.createElement("div");
    p.className="particle";
    p.style.left=Math.random()*100+"vw";
    p.style.animationDuration=(8+Math.random()*7)+"s";
    p.style.opacity=Math.random()*0.7+0.3;
    document.body.appendChild(p);
}
</script>

<div class="container">
  <div class="logo">Astore Tourist Hub</div>

  <!-- Hero slideshow -->
  <div class="slideshow-container">
      <div class="slide"><img src="https://i.ibb.co/2jL0MDK/mountains.jpg" alt="Mountains"></div>
      <div class="slide"><img src="https://i.ibb.co/s3Xs1H0/lake.jpg" alt="Lake"></div>
      <div class="slide"><img src="https://i.ibb.co/x3tFLYc/valley.jpg" alt="Valley"></div>
  </div>

  <div class="hero-text">
      <p>Owner: Asim Khanzai | WhatsApp: 03171588489 | Email: mohammadasimkhan2746@gmail.com</p>
  </div>

  <!-- Room Booking -->
  <h2 style="text-shadow:0 0 10px #00eaff;">Room Booking</h2>
  <form id="roomForm">
      <label><i class="fa-solid fa-user"></i> Name</label><input type="text" id="rname" required>
      <label><i class="fa-solid fa-phone"></i> Phone</label><input type="text" id="rphone" required>
      <label><i class="fa-solid fa-calendar-days"></i> Check-in Date</label><input type="date" id="rcheckin" required>
      <label><i class="fa-solid fa-calendar-days"></i> Check-out Date</label><input type="date" id="rcheckout" required>
      <label><i class="fa-solid fa-bed"></i> Room Type</label>
      <select id="rtype" required>
          <option>Standard Room</option>
          <option>Luxury Room</option>
          <option>Family Suite</option>
      </select>
      <button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Room on WhatsApp</button>
  </form>

  <!-- Car Booking -->
  <h2 style="text-shadow:0 0 10px #00eaff;">Car Booking</h2>
  <form id="carForm">
      <label><i class="fa-solid fa-user"></i> Name</label><input type="text" id="cname" required>
      <label><i class="fa-solid fa-phone"></i> Phone</label><input type="text" id="cphone" required>
      <label><i class="fa-solid fa-calendar-days"></i> Pickup Date</label><input type="date" id="cdate" required>
      <label><i class="fa-solid fa-car"></i> Car Type</label>
      <select id="ctype" required>
          <option>Corolla</option>
          <option>Hiace</option>
          <option>Prado</option>
          <option>Astore Local Jeep</option>
      </select>
      <button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Car on WhatsApp</button>
  </form>

  <!-- Packages -->
  <h2 style="text-shadow:0 0 10px #00eaff;">Tour Packages</h2>
  <div class="packages">
      <div class="package">
          <h3>Basic Package</h3>
          <p>2 Nights, 3 Days<br>Standard Room + Local Guide</p>
      </div>
      <div class="package">
          <h3>Luxury Package</h3>
          <p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p>
      </div>
      <div class="package">
          <h3>Adventure Package</h3>
          <p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p>
      </div>
  </div>

  <!-- Map -->
  <h2 style="text-shadow:0 0 10px #00eaff;">Our Location</h2>
  <div class="map-container">
      <iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
  </div>

  <!-- Contact -->
  <div class="contact">
      <p><i class="fa-solid fa-envelope"></i> Email: mohammadasimkhan2746@gmail.com</p>
  </div>

  <!-- Social Share -->
  <div class="social-share">
      <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
      <a href="https://www.facebook.com/sharer/sharer.php?u=https://yourwebsite.com" target="_blank"><i class="fa-brands fa-facebook"></i></a>
      <a href="https://twitter.com/intent/tweet?url=https://yourwebsite.com&text=Astore+Tourist+Information+Hub" target="_blank"><i class="fa-brands fa-twitter"></i></a>
  </div>
</div>

<!-- Floating WhatsApp Button -->
<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Hero slideshow
let slideIndex=0;
showSlides();
function showSlides(){
    let slides=document.getElementsByClassName("slide");
    for(let i=0;i<slides.length;i++){slides[i].style.display="none";}
    slideIndex++;
    if(slideIndex>slides.length){slideIndex=1;}
    slides[slideIndex-1].style.display="block";
    setTimeout(showSlides,4000);
}

// Booking Forms WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
    e.preventDefault();
    let msg=`Room Booking Request:%0AName: ${document.getElementById("rname").value}%0APhone: ${document.getElementById("rphone").value}%0ACheck-in: ${document.getElementById("rcheckin").value}%0ACheck-out: ${document.getElementById("rcheckout").value}%0ARoom Type: ${document.getElementById("rtype").value}`;
    window.location.href="https://wa.me/923171588489?text="+msg;
});
document.getElementById("carForm").addEventListener("submit",function(e){
    e.preventDefault();
    let msg=`Car Booking Request:%0AName: ${document.getElementById("cname").value}%0APhone: ${document.getElementById("cphone").value}%0APickup Date: ${document.getElementById("cdate").value}%0ACar Type: ${document.getElementById("ctype").value}`;
    window.location.href="https://wa.me/923171588489?text="+msg;
});
</script>

</body>
</html>
