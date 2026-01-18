<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;scroll-behavior:smooth;}
body{background:#000;color:#fff;overflow-x:hidden;}
.bg-gradient{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000000,#0f0f0f,#001f3f,#000000);background-size:800% 800%;animation:gradientBG 25s ease infinite;z-index:-3;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
.stripes{position:fixed;width:100%;height:100%;z-index:-2;overflow:hidden;}
.stripe{position:absolute;width:3px;height:200%;background:rgba(0,255,255,0.05);top:-50%;animation:moveStripe linear infinite;}
.stripe:nth-child(1){left:10%;animation-duration:18s;}
.stripe:nth-child(2){left:25%;animation-duration:22s;}
.stripe:nth-child(3){left:40%;animation-duration:20s;}
.stripe:nth-child(4){left:60%;animation-duration:25s;}
.stripe:nth-child(5){left:80%;animation-duration:19s;}
@keyframes moveStripe{0%{transform:translateY(0) rotate(20deg);}100%{transform:translateY(100%) rotate(20deg);}}
.particle{position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
header{padding:20px;text-align:center;font-size:32px;color:#00eaff;text-shadow:0 0 10px #00ffff,0 0 25px #00eaff;font-family:'Orbitron',sans-serif;}
section{max-width:1000px;margin:20px auto;background:rgba(0,0,0,0.6);border-radius:15px;padding:20px;backdrop-filter:blur(5px);box-shadow:0 0 25px #00eaff;}
h2{color:#00ffff;text-shadow:0 0 10px #00ffff;}
p{color:#a7f5ff;}
button{padding:12px 20px;margin-top:10px;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);border:none;color:#000;font-weight:600;border-radius:10px;cursor:pointer;transition:0.3s;box-shadow:0 0 15px #00ffff;}
button:hover{box-shadow:0 0 30px #00ffff;transform:scale(1.05);}
.img-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:10px;margin-top:10px;}
.img-grid img{width:100%;border-radius:10px;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:0;width:100%;background:rgba(0,0,0,0.6);padding:10px 0;box-shadow:0 0 25px #00eaff;border-top:1px solid #00ffff;z-index:999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:28px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.3);}
.icon-item span{display:block;font-size:12px;color:#00f5ff;}
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>
<div class="bg-gradient"></div>
<div class="stripes"><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div></div>
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

<header>Astore Tourist Hub</header>

<section id="about">
<h2>About Us</h2>
<p>Welcome to Astore Tourist Hub – your gateway to the majestic mountains and breathtaking landscapes of Astore Valley. Explore cozy rooms, reliable car rentals, adventure packages, and local guides for an unforgettable journey. Stay connected and book via WhatsApp or Email instantly!</p>
</section>

<section id="rooms">
<h2>Rooms & Accommodation</h2>
<p>Choose from Standard Rooms, Luxury Rooms, and Family Suites. All rooms are equipped with free Wi-Fi, comfortable beds, and scenic views.</p>
<div class="img-grid">
<img src="https://source.unsplash.com/400x300/?hotel" alt="Room 1">
<img src="https://source.unsplash.com/400x300/?resort" alt="Room 2">
<img src="https://source.unsplash.com/400x300/?suite" alt="Room 3">
</div>
<button onclick="window.open('https://wa.me/923171588489?text=I want to book a room','_blank')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</section>

<section id="cars">
<h2>Car Rentals</h2>
<p>We provide local jeep rentals, Hiace, Corolla, and Prado for your trips. Flexible pickup and drop options available.</p>
<div class="img-grid">
<img src="https://source.unsplash.com/400x300/?jeep" alt="Car 1">
<img src="https://source.unsplash.com/400x300/?suv" alt="Car 2">
<img src="https://source.unsplash.com/400x300/?car" alt="Car 3">
</div>
<button onclick="window.open('https://wa.me/923171588489?text=I want to rent a car','_blank')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</section>

<section id="packages">
<h2>Packages & Tours</h2>
<p>Adventure Package, Luxury Package, Family Package – tailored trips with local guides, jeep tours, and mountain treks.</p>
<div class="img-grid">
<img src="https://source.unsplash.com/400x300/?mountain,adventure" alt="Adventure 1">
<img src="https://source.unsplash.com/400x300/?nature,tour" alt="Adventure 2">
<img src="https://source.unsplash.com/400x300/?travel" alt="Adventure 3">
</div>
</section>

<section id="offers">
<h2>Special Offers</h2>
<p>Get up to 20% off on long stays, early bookings, and package deals! Limited time offers available.</p>
<div class="img-grid">
<img src="https://source.unsplash.com/400x300/?discount" alt="Offer 1">
<img src="https://source.unsplash.com/400x300/?promo" alt="Offer 2">
<img src="https://source.unsplash.com/400x300/?travel,discount" alt="Offer 3">
</div>
</section>

<section id="contact">
<h2>Contact Us</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00ffff;">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#00ffff;">03171588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#00ffff;">Visit Page</a></p>
</section>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-house" onclick="scrollToSection('about')"></i><span>About</span></div>
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('rooms')"></i><span>Rooms</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('cars')"></i><span>Cars</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-tag" onclick="scrollToSection('offers')"></i><span>Offers</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<script>
function scrollToSection(id){
  document.getElementById(id).scrollIntoView({behavior:'smooth'});
}
</script>
</body>
</html>
