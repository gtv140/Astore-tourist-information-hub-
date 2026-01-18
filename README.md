<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
  font-family:Arial,Helvetica,sans-serif;
  background:#f5f7fa;
  color:#222;
}

/* ===== HEADER ===== */
header{
  background:#0b1d33;
  color:#fff;
  padding:18px;
  text-align:center;
}
header h1{font-size:22px;margin-bottom:6px}
header p{font-size:14px;opacity:.9}

/* ===== SLIDER ===== */
.slider{
  width:100%;
  height:220px;
  overflow:hidden;
}
.slide{
  display:none;
}
.slide img{
  width:100%;
  height:220px;
  object-fit:cover;
}

/* ===== CONTAINER ===== */
.container{
  padding:15px;
  padding-bottom:90px;
}

/* ===== SECTIONS ===== */
section{
  display:none;
  background:#fff;
  border-radius:12px;
  padding:15px;
  margin-bottom:15px;
  box-shadow:0 4px 12px rgba(0,0,0,.08);
}
section h2{
  font-size:18px;
  margin-bottom:10px;
  color:#0b1d33;
}
section p{
  font-size:14px;
  line-height:1.6;
  margin-bottom:10px;
}

/* ===== FORMS ===== */
input,select,button{
  width:100%;
  padding:10px;
  margin-bottom:10px;
  border-radius:8px;
  border:1px solid #ccc;
  font-size:14px;
}
button{
  background:#25d366;
  color:#fff;
  border:none;
  font-weight:bold;
}
button i{margin-right:6px}

/* ===== IMAGE CARD ===== */
.card-img{
  width:100%;
  height:160px;
  object-fit:cover;
  border-radius:10px;
  margin-bottom:10px;
}

/* ===== BOTTOM NAV ===== */
.bottom-nav{
  position:fixed;
  bottom:0;
  left:0;
  width:100%;
  background:#fff;
  border-top:1px solid #ddd;
  display:flex;
  justify-content:space-around;
  padding:8px 0;
}
.nav-item{
  text-align:center;
  font-size:12px;
  color:#333;
}
.nav-item i{
  font-size:20px;
  display:block;
  margin-bottom:3px;
  color:#0b1d33;
}

/* ===== WHATSAPP FLOAT ===== */
.whatsapp{
  position:fixed;
  right:15px;
  bottom:90px;
  background:#25d366;
  color:#fff;
  padding:14px;
  border-radius:50%;
  font-size:22px;
}
</style>
</head>

<body>

<header>
  <h1>Astore Tourist Information Hub</h1>
  <p>Explore Gilgit Baltistan • Mountains • Nature • Peace</p>
</header>

<!-- SLIDER -->
<div class="slider">
  <div class="slide"><img src="https://picsum.photos/800/400?1"></div>
  <div class="slide"><img src="https://picsum.photos/800/400?2"></div>
  <div class="slide"><img src="https://picsum.photos/800/400?3"></div>
</div>

<div class="container">

<!-- HOME -->
<section id="home" style="display:block">
  <h2>Welcome</h2>
  <p>
    Astore is one of the most beautiful regions of Gilgit Baltistan.
    Snow‑covered mountains, lakes, rivers and peaceful valleys make it
    a perfect destination for tourists.
  </p>
  <img class="card-img" src="https://picsum.photos/600/400?mountain">
  <p>
    We provide **rooms, cars, and guided tour packages**
    for families, friends and solo travelers.
  </p>
</section>

<!-- ROOMS -->
<section id="rooms">
  <h2>Room Booking</h2>
  <img class="card-img" src="https://picsum.photos/600/400?hotel">
  <form onsubmit="bookRoom(event)">
    <input placeholder="Your Name" required>
    <input placeholder="Phone Number" required>
    <select>
      <option>Standard Room</option>
      <option>Luxury Room</option>
      <option>Family Room</option>
    </select>
    <button><i class="fa-brands fa-whatsapp"></i>Book via WhatsApp</button>
  </form>
</section>

<!-- CARS -->
<section id="cars">
  <h2>Car Rental</h2>
  <img class="card-img" src="https://picsum.photos/600/400?car">
  <form onsubmit="bookCar(event)">
    <input placeholder="Your Name" required>
    <input placeholder="Phone Number" required>
    <select>
      <option>Corolla</option>
      <option>Hiace</option>
      <option>Prado</option>
      <option>Jeep</option>
    </select>
    <button><i class="fa-brands fa-whatsapp"></i>Book via WhatsApp</button>
  </form>
</section>

<!-- PACKAGES -->
<section id="packages">
  <h2>Tour Packages</h2>
  <img class="card-img" src="https://picsum.photos/600/400?nature">
  <p>• 3 Days Astore Valley Tour</p>
  <p>• Rama Lake & Deosai Tour</p>
  <p>• Family & Honeymoon Packages</p>
</section>

<!-- CONTACT -->
<section id="contact">
  <h2>Contact Us</h2>
  <p>Email: mohammadasimkhan2746@gmail.com</p>
  <p>WhatsApp: 0317‑1588489</p>
  <p>Location: Near DC House, Eidgah, Astore</p>
</section>

</div>

<!-- BOTTOM NAV -->
<div class="bottom-nav">
  <div class="nav-item" onclick="show('home')"><i class="fa fa-home"></i>Home</div>
  <div class="nav-item" onclick="show('rooms')"><i class="fa fa-bed"></i>Rooms</div>
  <div class="nav-item" onclick="show('cars')"><i class="fa fa-car"></i>Cars</div>
  <div class="nav-item" onclick="show('packages')"><i class="fa fa-mountain"></i>Tours</div>
  <div class="nav-item" onclick="show('contact')"><i class="fa fa-phone"></i>Contact</div>
</div>

<a class="whatsapp" href="https://wa.me/923171588489">
  <i class="fa-brands fa-whatsapp"></i>
</a>

<script>
/* slider */
let i=0;
const slides=document.querySelectorAll(".slide");
function slider(){
  slides.forEach(s=>s.style.display="none");
  i=(i+1)%slides.length;
  slides[i].style.display="block";
}
slider(); setInterval(slider,3500);

/* section switch */
function show(id){
  document.querySelectorAll("section").forEach(s=>s.style.display="none");
  document.getElementById(id).style.display="block";
}

/* whatsapp */
function bookRoom(e){e.preventDefault();window.open("https://wa.me/923171588489")}
function bookCar(e){e.preventDefault();window.open("https://wa.me/923171588489")}
</script>

</body>
</html>
