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
body{font-family:'Poppins',sans-serif;background:#0a0f1b;color:#fff;overflow-x:hidden;}
.container{max-width:1000px;margin:70px auto;padding:20px;background:rgba(0,0,0,0.5);border-radius:20px;}
.logo{text-align:center;font-size:36px;font-family:'Orbitron',sans-serif;color:#00cfff;margin-bottom:10px;}
.hero-text{text-align:center;color:#00eaff;font-size:16px;margin-bottom:25px;}
section{margin-bottom:30px;}
section h2{color:#00eaff;margin-bottom:15px;font-family:'Orbitron',sans-serif;}
section p{color:#a7f5ff;line-height:1.5;margin-bottom:10px;}
section img{width:100%;border-radius:15px;margin-top:10px;box-shadow:0 0 15px #00eaff;}
form{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
input,select,button{padding:10px;border-radius:10px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}
#historyList div{border:1px solid #00eaff;padding:8px;margin:5px;border-radius:8px;color:#a7f5ff;}
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.6);padding:10px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:26px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:3px;color:#00fff0;}
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
.gallery{display:flex;overflow-x:auto;gap:10px;margin-top:10px;}
.gallery img{height:150px;border-radius:10px;cursor:pointer;transition:0.3s;}
.gallery img:hover{transform:scale(1.1);}
.offer-card{background:rgba(0,0,0,0.4);padding:10px;border-radius:10px;box-shadow:0 0 15px #00eaff;margin-bottom:10px;}
.review-card{background:rgba(0,0,0,0.3);padding:10px;border-radius:10px;margin-bottom:10px;color:#a7f5ff;}
</style>
</head>
<body>

<div class="container" id="dashboard">
<h1 class="logo">Astore Tourist Hub</h1>
<div class="hero-text">Owner: Asim Khanzai | <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00fff0;">Email</a> | <a href="https://wa.me/923171588489" style="color:#00fff0;">WhatsApp</a></div>

<section id="about">
<h2>About Us</h2>
<p>Discover Astore's hidden gems with guided tours, comfortable stays, and car rentals. Enjoy mountain views, rivers, local culture, and adventure packages for families and solo travelers alike.</p>
<div class="gallery">
<img src="https://picsum.photos/id/1015/300/200" alt="Mountain">
<img src="https://picsum.photos/id/1025/300/200" alt="River">
<img src="https://picsum.photos/id/1035/300/200" alt="Valley">
<img src="https://picsum.photos/id/1045/300/200" alt="Local Tour">
</div>
</section>

<section id="rooms">
<h2>Rooms</h2>
<p>Standard Room: Comfortable for 2 | Luxury Room: Premium stay | Family Suite: Spacious for 4+</p>
<div class="gallery">
<img src="https://picsum.photos/id/1055/300/200" alt="Standard Room">
<img src="https://picsum.photos/id/1065/300/200" alt="Luxury Room">
<img src="https://picsum.photos/id/1075/300/200" alt="Family Suite">
</div>
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

<section id="cars">
<h2>Car Rentals</h2>
<p>Corolla, Hiace, Prado, Local Jeep – convenient and safe transport options.</p>
<div class="gallery">
<img src="https://picsum.photos/id/1085/300/200" alt="Corolla">
<img src="https://picsum.photos/id/1095/300/200" alt="Hiace">
<img src="https://picsum.photos/id/1105/300/200" alt="Prado">
<img src="https://picsum.photos/id/1115/300/200" alt="Jeep">
</div>
<form id="carForm">
<input type="text" id="cname" placeholder="Your Name" required>
<input type="text" id="cphone" placeholder="Phone Number" required>
<input type="date" id="cdate" required>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Local Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</section>

<section id="packages">
<h2>Adventure Packages</h2>
<div class="offer-card">
<p><strong>Basic:</strong> 2 Nights, 3 Days | Standard Room + Guide</p>
</div>
<div class="offer-card">
<p><strong>Luxury:</strong> 4 Nights, 5 Days | Luxury Room + Car + Guide</p>
</div>
<div class="offer-card">
<p><strong>Adventure:</strong> 5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p>
</div>
</section>

<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:15px;"></iframe>
</section>

<section id="reviews">
<h2>Reviews</h2>
<div class="review-card">
<p>"Amazing tour and very comfortable rooms!" – Ali</p>
</div>
<div class="review-card">
<p>"Helpful staff, great car rentals." – Sara</p>
</div>
</section>

<section id="contact">
<h2>Contact</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00fff0;">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#00fff0;">0317-1588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#00fff0;">Visit Page</a></p>
</section>

<section id="history">
<h2>Booking History</h2>
<div id="historyList"></div>
</section>

<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('rooms')"></i><span>Rooms</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('cars')"></i><span>Cars</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="scrollToSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Room Booking
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Room",name:document.getElementById("rname").value,phone:document.getElementById("rphone").value,checkin:document.getElementById("rcheckin").value,checkout:document.getElementById("rcheckout").value,room:document.getElementById("rtype").value};
  const msg=`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
});

// Car Booking
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
});

// Booking History
function addHistory(b){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  history.push(b); localStorage.setItem("tourHistory",JSON.stringify(history)); loadHistory();
}
function loadHistory(){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  const list=document.getElementById("historyList"); list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div"); 
    let content="";
    if(b.type==="Room") content=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") content=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    div.innerHTML=content; list.appendChild(div);
  });
}
loadHistory();

// Scroll to section
function scrollToSection(id){document.getElementById(id).scrollIntoView({behavior:'smooth'});}
</script>

</body>
</html>
