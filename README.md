<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;background:#000;color:#fff;overflow-x:hidden;line-height:1.6;}
a{text-decoration:none;color:#00fff0;}

/* Background */
.bg{
  position:fixed;width:100%;height:100%;
  background:linear-gradient(135deg,#000,#001f3f,#000);
  background-size:400% 400%;animation:bgAnim 30s ease infinite;
  z-index:-3;
}
@keyframes bgAnim{0%{background-position:0 50%;}50%{background-position:100% 50%;}100%{background-position:0 50%;}}

/* Header */
header{text-align:center;padding:20px;}
header h1{font-family:'Orbitron',sans-serif;font-size:36px;color:#00eaff;text-shadow:0 0 20px #00fff0;}
header p{font-size:16px;color:#00fff0;}

/* Sections */
section{padding:20px;margin:15px auto;max-width:1000px;background:rgba(0,0,0,0.5);border-radius:15px;backdrop-filter:blur(8px);}
section h2{font-family:'Orbitron',sans-serif;color:#00eaff;margin-bottom:10px;}
section p{color:#a7f5ff;font-size:14px;}

/* Gallery */
.gallery{display:flex;overflow-x:auto;gap:10px;margin-top:10px;}
.gallery img{height:180px;border-radius:12px;flex-shrink:0;box-shadow:0 0 15px #00eaff;transition:0.3s;}
.gallery img:hover{transform:scale(1.05);}

/* Booking Cards */
.card-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:15px;margin-top:15px;}
.card{background:rgba(0,0,0,0.4);padding:15px;border-radius:12px;box-shadow:0 0 20px #00fff0;transition:0.3s;}
.card h3{color:#00fff0;margin-bottom:8px;}
.card p{color:#a7f5ff;font-size:14px;margin-bottom:10px;}
.card button{padding:10px;border:none;border-radius:10px;background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
.card button:hover{background:#00fff0;}

/* Forms */
form{display:flex;flex-direction:column;gap:10px;}
input,select{padding:10px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}

/* Booking history */
#historyList div{border:1px solid #00eaff;padding:10px;margin:5px;border-radius:10px;color:#a7f5ff;}

/* Floating icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.5);padding:10px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:26px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:3px;color:#00fff0;}

/* WhatsApp button */
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>
<div class="bg"></div>

<header>
<h1>Astore Tourist Hub</h1>
<p>Discover Astore's mountains, rivers, and culture | <a href="mailto:mohammadasimkhan2746@gmail.com">Email</a> | <a href="https://wa.me/923171588489">WhatsApp</a></p>
</header>

<!-- About Section -->
<section id="about">
<h2>About Astore Tourist Hub</h2>
<p>Experience the best of Gilgit-Baltistan at Astore Tourist Hub! Cozy rooms, adventurous tours, local jeep rides, and guided excursions. Explore mountain valleys, rivers, and local culture with family-friendly and premium options.</p>
<div class="gallery">
<img src="https://picsum.photos/id/1015/400/250" alt="Mountain">
<img src="https://picsum.photos/id/1016/400/250" alt="River">
<img src="https://picsum.photos/id/1018/400/250" alt="Valley">
<img src="https://picsum.photos/id/1021/400/250" alt="Lake">
<img src="https://picsum.photos/id/1022/400/250" alt="Nature">
</div>
</section>

<!-- Rooms Section -->
<section id="room">
<h2>Room Booking</h2>
<div class="card-container">
<div class="card">
<h3>Standard Room</h3>
<p>2 Nights, 3 Days | Cozy and budget-friendly room with basic amenities</p>
<button onclick="bookRoom('Standard Room')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
<div class="card">
<h3>Luxury Room</h3>
<p>4 Nights, 5 Days | Premium room with mountain view and breakfast included</p>
<button onclick="bookRoom('Luxury Room')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
<div class="card">
<h3>Family Suite</h3>
<p>5 Nights, 6 Days | Spacious suite for family with local guide</p>
<button onclick="bookRoom('Family Suite')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
</div>
</section>

<!-- Car Section -->
<section id="car">
<h2>Car Booking</h2>
<div class="card-container">
<div class="card">
<h3>Corolla</h3>
<p>Daily rental | Ideal for couples or small families</p>
<button onclick="bookCar('Corolla')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
<div class="card">
<h3>Hiace</h3>
<p>Daily rental | Group trips or extended tours</p>
<button onclick="bookCar('Hiace')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
<div class="card">
<h3>Prado</h3>
<p>Daily rental | Premium SUV for mountain trips</p>
<button onclick="bookCar('Prado')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
<div class="card">
<h3>Astore Local Jeep</h3>
<p>Daily rental | Perfect for adventure trails and rough roads</p>
<button onclick="bookCar('Astore Local Jeep')"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>
</div>
</section>

<!-- Packages Section -->
<section id="packages">
<h2>Adventure Packages</h2>
<div class="card-container">
<div class="card">
<h3>Basic Package</h3>
<p>2 Nights, 3 Days | Standard Room + Local Guide</p>
</div>
<div class="card">
<h3>Luxury Package</h3>
<p>4 Nights, 5 Days | Luxury Room + Car + Guide</p>
</div>
<div class="card">
<h3>Adventure Package</h3>
<p>5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p>
</div>
</div>
</section>

<!-- Map Section -->
<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:12px;"></iframe>
</section>

<!-- Contact Section -->
<section id="contact">
<h2>Contact</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489">0317-1588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">Visit Page</a></p>
</section>

<!-- Booking History -->
<section id="history">
<h2>Booking History</h2>
<div id="historyList"></div>
</section>

<!-- Floating Bottom Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="scrollToSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Booking via WhatsApp functions
function bookRoom(type){
  let name=prompt("Enter Your Name");
  let phone=prompt("Enter Phone Number");
  let checkin=prompt("Check-in Date (YYYY-MM-DD)");
  let checkout=prompt("Check-out Date (YYYY-MM-DD)");
  if(!name||!phone||!checkin||!checkout) return;
  let msg=`Room Booking:\nType: ${type}\nName: ${name}\nPhone: ${phone}\nCheck-in: ${checkin}\nCheck-out: ${checkout}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  addHistory({type:"Room",room:type,name,phone,checkin,checkout});
}

function bookCar(type){
  let name=prompt("Enter Your Name");
  let phone=prompt("Enter Phone Number");
  let date=prompt("Pickup Date (YYYY-MM-DD)");
  if(!name||!phone||!date) return;
  let msg=`Car Booking:\nType: ${type}\nName: ${name}\nPhone: ${phone}\nPickup Date: ${date}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  addHistory({type:"Car",car:type,name,phone,date});
}

// Booking History
function addHistory(b){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  history.push(b);
  localStorage.setItem("tourHistory",JSON.stringify(history));
  loadHistory();
}

function loadHistory(){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  const list=document.getElementById("historyList");
  list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");
    if(b.type==="Room") div.innerHTML=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") div.innerHTML=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    list.appendChild(div);
  });
}
loadHistory();

// Scroll to sections
function scrollToSection(id){
  document.getElementById(id).scrollIntoView({behavior:'smooth'});
}
</script>
</body>
</html>
