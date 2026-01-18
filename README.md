<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
/* General Reset & Body */
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#000;overflow-x:hidden;line-height:1.5;}
a{text-decoration:none;color:#00fff0;}

/* Logo / Header */
header{display:flex;justify-content:center;align-items:center;padding:10px 0;font-family:'Orbitron',sans-serif;font-size:20px;color:#00eaff;font-weight:700;}
header span{font-size:14px;color:#00fff0;margin-left:10px;}

/* Hero Slider */
#hero{position:relative;width:100%;height:250px;overflow:hidden;border-bottom:2px solid #00eaff;border-radius:10px;margin:10px 0;}
#hero img{width:100%;height:250px;object-fit:cover;position:absolute;opacity:0;transition:opacity 1s ease;}
#hero img.active{opacity:1;}
#hero-overlay{position:absolute;width:100%;height:100%;background:rgba(0,0,0,0.4);display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;padding:10px;}
#hero-overlay h1{font-size:22px;color:#00fff0;margin-bottom:5px;}
#hero-overlay p{font-size:14px;color:#a7f5ff;}

/* Sections */
.container{padding:10px 15px;}
section{margin-bottom:20px;}
section h2{color:#00eaff;margin-bottom:10px;font-family:'Orbitron',sans-serif;font-size:18px;}
section p{font-size:13px;color:#a7f5ff;margin-bottom:8px;}
section img{width:100%;border-radius:10px;margin-top:5px;box-shadow:0 0 10px #00eaff;}

/* Cards for packages */
.cards{display:flex;flex-wrap:wrap;gap:10px;}
.card{flex:1 1 48%;background:rgba(0,0,0,0.4);padding:8px;border-radius:10px;box-shadow:0 0 15px #00eaff;}
.card i{font-size:18px;color:#00fff0;margin-bottom:5px;display:block;}

/* Forms */
form{display:flex;flex-direction:column;gap:5px;margin-top:5px;}
input,select,button{padding:8px;border-radius:8px;border:none;font-size:14px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}

/* Booking History */
#historyList div{border:1px solid #00eaff;padding:6px;margin:4px;border-radius:6px;color:#a7f5ff;font-size:13px;}

/* Fixed Bottom Icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.6);padding:8px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:10px 10px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:24px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.3);}
.icon-item span{display:block;font-size:11px;margin-top:2px;color:#00fff0;}

/* WhatsApp button */
.whatsapp-btn{position:fixed;bottom:60px;right:15px;background:#25d366;padding:14px 16px;border-radius:50%;color:#fff;font-size:26px;text-decoration:none;box-shadow:0 0 15px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>

<header>
Astore Tourist Hub <span>Created by CrazyKhanTV</span>
</header>

<!-- Hero Slider -->
<div id="hero">
<img src="https://picsum.photos/id/1015/600/250" class="active" alt="Nature1">
<img src="https://picsum.photos/id/1016/600/250" alt="Nature2">
<img src="https://picsum.photos/id/1018/600/250" alt="Nature3">
<div id="hero-overlay">
<h1>Welcome to Gilgit-Baltistan</h1>
<p>Explore mountains, rivers, and culture with Astore Tourist Hub. Adventure, comfort, and guided tours await you.</p>
</div>
</div>

<div class="container">

<!-- About Section -->
<section id="about">
<h2>About Us</h2>
<p>Astore Tourist Hub provides tourists an amazing experience in Gilgit-Baltistan with guided tours, cozy rooms, and car rentals. Enjoy adventure packages, local culture, and premium services.</p>
<img src="https://picsum.photos/id/1025/600/300" alt="Gilgit Nature">
</section>

<!-- Rooms Section -->
<section id="room">
<h2>Rooms Booking</h2>
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
<div class="cards">
<div class="card"><i class="fa-solid fa-mountain"></i><p><strong>Basic:</strong> 2 Nights, 3 Days | Standard Room + Guide</p></div>
<div class="card"><i class="fa-solid fa-car"></i><p><strong>Luxury:</strong> 4 Nights, 5 Days | Luxury Room + Car + Guide</p></div>
<div class="card"><i class="fa-solid fa-person-hiking"></i><p><strong>Adventure:</strong> 5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p></div>
</div>
</section>

<!-- Map Section -->
<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="200" style="border:0;border-radius:10px;"></iframe>
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

</div>

<!-- Bottom Icons -->
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
let slides = document.querySelectorAll('#hero img'); let index=0;
setInterval(()=>{slides[index].classList.remove('active'); index=(index+1)%slides.length; slides[index].classList.add('active');},4000);

// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Room",name:document.getElementById("rname").value,phone:document.getElementById("rphone").value,checkin:document.getElementById("rcheckin").value,checkout:document.getElementById("rcheckout").value,room:document.getElementById("rtype").value};
  const msg=`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
});

// Booking History
function addHistory(booking){let history=JSON.parse(localStorage.getItem("tourHistory"))||[];history.push(booking);localStorage.setItem("tourHistory",JSON.stringify(history));loadHistory();}
function loadHistory(){let history=JSON.parse(localStorage.getItem("tourHistory"))||[];const list=document.getElementById("historyList");list.innerHTML="";history.forEach(b=>{const div=document.createElement("div");div.innerHTML=b.type==="Room"?`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`:`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;list.appendChild(div);});}
loadHistory();

// Scroll to section
function scrollToSection(id){document.getElementById(id).scrollIntoView({behavior:'smooth'});}
</script>
</body>
</html>
