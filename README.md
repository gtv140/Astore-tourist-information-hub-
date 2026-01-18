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
body{font-family:'Poppins',sans-serif;background:#000;color:#fff;overflow-x:hidden;}

/* Header Logo */
header{display:flex;justify-content:space-between;align-items:center;padding:10px 20px;background:rgba(0,0,0,0.5);border-bottom:1px solid #00eaff;}
header .logo{font-family:'Orbitron',sans-serif;font-size:22px;color:#00eaff;font-weight:700;}
header .creator{font-size:12px;color:#00fff0;}

/* Hero / Slider */
.hero{position:relative;width:100%;height:250px;overflow:hidden;border-radius:15px;margin:15px 0;}
.hero img{width:100%;height:100%;object-fit:cover;position:absolute;opacity:0;transition:opacity 1s ease-in-out;}
.hero img.active{opacity:1;}
.hero-text{position:absolute;bottom:15px;left:20px;color:#00fff0;font-size:16px;text-shadow:0 0 10px #00eaff;}

/* Sections */
section{margin:15px 10px;}
section h2{color:#00eaff;font-family:'Orbitron',sans-serif;margin-bottom:8px;}
section p{font-size:14px;color:#a7f5ff;line-height:1.5;}
section img{width:100%;border-radius:10px;margin-top:8px;}

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

/* WhatsApp Button */
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>

<header>
  <div class="logo">Astore Tourist Hub</div>
  <div class="creator">Created by CrazyKhanTV</div>
</header>

<!-- Hero Slider -->
<div class="hero">
  <img src="https://picsum.photos/id/1015/600/250" class="active" alt="Mountain">
  <img src="https://picsum.photos/id/1020/600/250" alt="River">
  <img src="https://picsum.photos/id/1024/600/250" alt="Valley">
  <div class="hero-text">Welcome to Gilgit-Baltistan | Explore Nature & Adventure</div>
</div>

<div class="container">

<!-- About Section -->
<section id="about">
<h2>About Astore Tourist Hub</h2>
<p>Discover the natural beauty of Gilgit-Baltistan with our curated tours, cozy accommodations, and vehicle rentals. Experience adventure packages, family-friendly stays, and expert guidance on your journey through mountains, rivers, and cultural sites.</p>
<img src="https://picsum.photos/id/1035/600/300" alt="Nature View">
</section>

<!-- Room Booking -->
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

<!-- Car Booking -->
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

<!-- Adventure Packages -->
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

<!-- Map -->
<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:10px;"></iframe>
</section>

<!-- Contact -->
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

</div>

<!-- Fixed Bottom Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="scrollToSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Hero Slider
let slides=document.querySelectorAll('.hero img');
let current=0;
setInterval(()=>{
  slides[current].classList.remove('active');
  current=(current+1)%slides.length;
  slides[current].classList.add('active');
},4000);

// Booking Forms
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Room",name:document.getElementById("rname").value,phone:document.getElementById("rphone").value,checkin:document.getElementById("rcheckin").value,checkout:document.getElementById("rcheckout").value,room:document.getElementById("rtype").value};
  const msg=`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset();
  addHistory(booking);
});

document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
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
    if(b.type==="Room") div.innerHTML=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") div.innerHTML=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
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
