<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
/* Reset & Body */
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#0a0a0a;overflow-x:hidden;}

/* Container */
.container{max-width:1000px;margin:60px auto;padding:20px;background:rgba(0,0,0,0.5);border-radius:15px;backdrop-filter:blur(10px);}

/* Logo & Hero Text */
.logo{text-align:center;font-size:36px;font-weight:700;color:#00eaff;margin-bottom:10px;font-family:'Orbitron',sans-serif;text-shadow:0 0 10px #00fff0;}
.hero-text{text-align:center;font-size:15px;margin-bottom:20px;color:#00fff0;line-height:1.5;}

/* Sections */
section{margin-bottom:30px;}
section h2{color:#00eaff;margin-bottom:10px;text-shadow:0 0 8px #00fff0;font-family:'Orbitron',sans-serif;}
section p{font-size:14px;color:#a7f5ff;line-height:1.5;}
section img{width:100%;border-radius:12px;box-shadow:0 0 15px #00eaff;margin-top:10px;}

/* Forms */
form{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
input,select,button{padding:10px;border-radius:10px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}

/* Booking History */
#historyList div{border:1px solid #00eaff;padding:8px;margin:5px;border-radius:8px;color:#a7f5ff;}

/* Fixed Bottom Icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.5);padding:10px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:26px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:3px;color:#00fff0;}

/* WhatsApp button */
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}

/* Offers/Ads */
.offer{background:#ff4444;color:#fff;padding:10px;border-radius:8px;text-align:center;margin:15px 0;font-weight:600;box-shadow:0 0 10px #ff6666;}
</style>
</head>
<body>

<div class="container" id="dashboard">
<h1 class="logo">Astore Tourist Hub</h1>
<div class="hero-text">
Discover the breathtaking beauty of Astore Valley! Explore mountains, rivers, glaciers, and cultural landmarks with guided tours, cozy rooms, and rental cars for a perfect adventure.<br>
Owner: Asim Khanzai | <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00fff0;text-decoration:underline;">Email</a> | <a href="https://wa.me/923171588489" style="color:#00fff0;text-decoration:underline;">WhatsApp</a>
</div>

<!-- Offer Banner -->
<div class="offer">🔥 Limited Time Offer: Book Adventure Package and Get Free Jeep Ride! 🔥</div>

<!-- About Section -->
<section id="about">
<h2>About Astore Tourist Hub</h2>
<p>We provide tourists with a seamless experience exploring Gilgit-Baltistan's natural wonders. Cozy accommodations, adventure packages, and car rentals make your stay unforgettable.</p>
<img src="https://picsum.photos/id/1015/600/300" alt="Mountain View">
<img src="https://picsum.photos/id/1016/600/300" alt="River View">
<img src="https://picsum.photos/id/1018/600/300" alt="Valley View">
</section>

<!-- Rooms Section -->
<section id="room">
<h2>Room Booking</h2>
<form id="roomForm">
<input type="text" id="rname" placeholder="Your Name" required>
<input type="text" id="rphone" placeholder="Phone Number" required>
<input type="date" id="rcheckin" required>
<input type="date" id="rcheckout" required>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</section>

<!-- Car Section -->
<section id="car">
<h2>Car Booking</h2>
<form id="carForm">
<input type="text" id="cname" placeholder="Your Name" required>
<input type="text" id="cphone" placeholder="Phone Number" required>
<input type="date" id="cdate" required>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Local Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</section>

<!-- Packages Section -->
<section id="packages">
<h2>Adventure Packages</h2>
<div style="display:flex;flex-direction:column;gap:10px;">
<div style="background:rgba(0,0,0,0.3);padding:10px;border-radius:10px;">
<i class="fa-solid fa-mountain" style="color:#00fff0;font-size:22px;"></i>
<p><strong>Basic Package:</strong> 2 Nights, 3 Days | Standard Room + Local Guide</p>
</div>
<div style="background:rgba(0,0,0,0.3);padding:10px;border-radius:10px;">
<i class="fa-solid fa-car" style="color:#00fff0;font-size:22px;"></i>
<p><strong>Luxury Package:</strong> 4 Nights, 5 Days | Luxury Room + Car + Guide</p>
</div>
<div style="background:rgba(0,0,0,0.3);padding:10px;border-radius:10px;">
<i class="fa-solid fa-person-hiking" style="color:#00fff0;font-size:22px;"></i>
<p><strong>Adventure Package:</strong> 5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p>
</div>
</div>
</section>

<!-- Map Section -->
<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:15px;"></iframe>
</section>

<!-- Contact Section -->
<section id="contact">
<h2>Contact</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00fff0;">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#00fff0;">0317-1588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#00fff0;">Visit Page</a></p>
</section>

<!-- Booking History -->
<section id="history">
<h2>Booking History</h2>
<div id="historyList"></div>
</section>

<!-- Floating Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="scrollToSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={
    type:"Room",
    name:document.getElementById("rname").value,
    phone:document.getElementById("rphone").value,
    checkin:document.getElementById("rcheckin").value,
    checkout:document.getElementById("rcheckout").value,
    room:document.getElementById("rtype").value
  };
  const msg=`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
  this.reset();
  addHistory(booking);
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={
    type:"Car",
    name:document.getElementById("cname").value,
    phone:document.getElementById("cphone").value,
    date:document.getElementById("cdate").value,
    car:document.getElementById("ctype").value
  };
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
  this.reset();
  addHistory(booking);
});

// Booking History
function addHistory(booking){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  history.push(booking);
  localStorage.setItem("tourHistory",JSON.stringify(history));
  loadHistory();
}
function loadHistory(){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  const list=document.getElementById("historyList");
  list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");
    let content="";
    if(b.type==="Room") content=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") content=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    div.innerHTML=content;
    list.appendChild(div);
  });
}
loadHistory();

// Scroll to section
function scrollToSection(id){
  document.getElementById(id).scrollIntoView({behavior:'smooth'});
}
</script>
</body>
</html>
