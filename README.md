<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
/* General */
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{background:#000;color:#fff;overflow-x:hidden;}
a{text-decoration:none;color:#00fff0;}
.container{max-width:1000px;margin:60px auto;padding:20px;background:rgba(0,0,0,0.4);border-radius:15px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;}
h1,h2,h3{font-family:'Orbitron',sans-serif;color:#00eaff;}
.hero-text{color:#00fff0;text-align:center;margin-bottom:20px;}
section{margin-bottom:30px;}
section img{width:100%;border-radius:15px;box-shadow:0 0 20px #00eaff;margin-top:10px;}
section p{line-height:1.5;color:#a7f5ff;font-size:14px;}

/* Buttons & Forms */
form{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
input,select,button{padding:10px;border-radius:10px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}

/* Packages & Cards */
.card{background:rgba(0,0,0,0.3);padding:10px;border-radius:10px;display:flex;align-items:center;gap:10px;box-shadow:0 0 15px #00eaff;}
.card i{font-size:22px;color:#00fff0;}

/* Booking History */
#historyList div{border:1px solid #00eaff;padding:8px;margin:5px;border-radius:8px;color:#a7f5ff;}

/* Fixed Bottom Icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.5);padding:10px 0;border-top:2px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;flex:1;}
.icon-item i{font-size:28px;cursor:pointer;transition:0.3s;}
.icon-item i:hover{transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:4px;color:#00fff0;}

/* WhatsApp Button */
.whatsapp-btn{position:fixed;bottom:80px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}

/* Background gradient animation */
.bg-animate{
  position:fixed;width:100%;height:100%;
  background:linear-gradient(270deg,#000000,#0f0f0f,#001f3f,#000000);
  background-size:800% 800%;
  animation:gradientBG 20s ease infinite;
  z-index:-3;
}
@keyframes gradientBG{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

/* Floating particles */
.particle{position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
</style>
</head>
<body>
<div class="bg-animate"></div>
<script>
for(let i=0;i<40;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(6+Math.random()*6)+"s";
  p.style.opacity=Math.random()*0.7+0.3;
  document.body.appendChild(p);
}
</script>

<div class="container" id="dashboard">
<h1>Astore Tourist Hub</h1>
<div class="hero-text">
Explore Gilgit-Baltistan's natural beauty! | Owner: Asim Khanzai | 
<a href="mailto:mohammadasimkhan2746@gmail.com">Email</a> | 
<a href="https://wa.me/923171588489">WhatsApp</a>
</div>

<!-- About -->
<section id="about">
<h2>About Us</h2>
<p>Discover the mountains, rivers, and valleys of Astore. Our hub offers guided tours, cozy rooms, car rentals, and adventure packages for families, solo travelers, and adventure seekers. Enjoy scenic views, local culture, and comfortable stays with premium service.</p>
<img src="https://picsum.photos/id/1015/600/300" alt="Mountain View">
<img src="https://picsum.photos/id/1016/600/300" alt="River View">
</section>

<!-- Rooms -->
<section id="room">
<h2>Rooms & Stays</h2>
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
<div class="card"><i class="fa-solid fa-bed"></i><p>Standard Room: 2 Nights, 3 Days | Free Breakfast</p></div>
<div class="card"><i class="fa-solid fa-bed"></i><p>Luxury Room: 4 Nights, 5 Days | Mountain View + Breakfast</p></div>
<div class="card"><i class="fa-solid fa-bed"></i><p>Family Suite: 5 Nights, 6 Days | Jacuzzi + Guide Included</p></div>
</section>

<!-- Cars -->
<section id="car">
<h2>Car Rentals</h2>
<form id="carForm">
<input type="text" id="cname" placeholder="Your Name" required>
<input type="text" id="cphone" placeholder="Phone Number" required>
<input type="date" id="cdate" required>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
<div class="card"><i class="fa-solid fa-car"></i><p>Corolla: 1 Day | AC + Driver</p></div>
<div class="card"><i class="fa-solid fa-car"></i><p>Prado: 1 Day | Mountain Adventure Ready</p></div>
<div class="card"><i class="fa-solid fa-car"></i><p>Hiace: 1 Day | Group Travel 12 Seats</p></div>
</section>

<!-- Adventure Packages -->
<section id="packages">
<h2>Adventure Packages</h2>
<div class="card"><i class="fa-solid fa-person-hiking"></i><p>Basic: 2 Nights, 3 Days | Guide Included</p></div>
<div class="card"><i class="fa-solid fa-person-hiking"></i><p>Luxury: 4 Nights, 5 Days | Car + Guide</p></div>
<div class="card"><i class="fa-solid fa-person-hiking"></i><p>Family Adventure: 5 Nights, 6 Days | Jeep Tour + Hiking</p></div>
</section>

<!-- Map -->
<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:15px;"></iframe>
</section>

<!-- Contact -->
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

<!-- Bottom Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('room')"></i><span>Rooms</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('car')"></i><span>Cars</span></div>
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
  this.reset();addHistory(booking);
});

// Car Booking
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nDate: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset();addHistory(booking);
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
  const list=document.getElementById("historyList");list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");let content="";
    if(b.type==="Room") content=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") content=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    div.innerHTML=content;list.appendChild(div);
  });
}
loadHistory();

// Scroll to Section
function scrollToSection(id){document.getElementById(id).scrollIntoView({behavior:'smooth'});}
</script>
</body>
</html>
