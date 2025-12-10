<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#000;overflow-x:hidden;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000,#0f0f0f,#001f3f,#000);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
.stripes{position:fixed;width:100%;height:100%;z-index:-1;overflow:hidden;}
.stripe{position:absolute;width:3px;height:200%;background:rgba(0,255,255,0.05);top:-50%;animation:moveStripe linear infinite;}
.stripe:nth-child(1){left:10%;animation-duration:18s;}
.stripe:nth-child(2){left:25%;animation-duration:22s;}
.stripe:nth-child(3){left:40%;animation-duration:20s;}
.stripe:nth-child(4){left:60%;animation-duration:25s;}
.stripe:nth-child(5){left:80%;animation-duration:19s;}
@keyframes moveStripe{0%{transform:translateY(0) rotate(20deg);}100%{transform:translateY(100%) rotate(20deg);}}
.particle{position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
h2.logo{text-align:center;font-size:50px;font-family:'Orbitron',sans-serif;color:#00eaff;text-shadow:0 0 20px #00eaff,0 0 40px #00ffff;animation:glowPulse 2s infinite alternate;margin-top:40px;}
@keyframes glowPulse{0%{text-shadow:0 0 20px #00eaff,0 0 40px #00ffff;}100%{text-shadow:0 0 40px #00eaff,0 0 80px #00ffff;}}
.hero-text{text-align:center;font-size:18px;font-weight:500;margin:20px auto;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
#dashboard{max-width:900px;margin:20px auto;padding-bottom:120px;}
.dashboard-section{display:none;margin:20px 0;}
.section-card{background:rgba(0,0,0,0.4);padding:25px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;transition:0.3s;cursor:pointer;}
.section-card:hover{transform:scale(1.05);box-shadow:0 0 40px #00ffff;}
.section-card h3{text-align:center;margin-bottom:10px;color:#00eaff;text-shadow:0 0 10px #00eaff;}
.section-card p{text-align:center;color:#a7f5ff;font-size:15px;}
label{display:block;margin-top:10px;font-weight:500;}
input,select,button{width:100%;padding:12px;margin-top:5px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;font-size:15px;transition:0.3s;}
input:focus,select:focus{background:rgba(255,255,255,0.25);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s, box-shadow 0.5s;border-radius:12px;}
button:hover{background:#00bcd4;box-shadow:0 0 25px #00ffff;}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;margin-top:10px;}
.package{background:rgba(0,0,0,0.4);padding:20px;border-radius:15px;box-shadow:0 0 25px #00eaff;text-align:center;transition:0.3s, transform 0.5s;}
.package:hover{transform:scale(1.05);box-shadow:0 0 40px #00ffff;}
.package h3{text-shadow:0 0 15px #00eaff;font-family:'Orbitron',sans-serif;}
.package p{font-size:14px;color:#a7f5ff;}
.package i{font-size:36px;color:#00eaff;margin-bottom:10px;display:block;}
.map-container{margin-top:20px;border-radius:15px;overflow:hidden;box-shadow:0 0 25px #00eaff;}
.contact{margin-top:20px;text-align:center;font-size:16px;color:#00eaff;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:0;left:0;width:100%;background:rgba(0,0,0,0.4);padding:10px 0;box-shadow:0 0 20px #00eaff;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:28px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:4px;}
.whatsapp-btn{position:fixed;bottom:80px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s, box-shadow 0.5s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>
<div class="bg-animate"></div>
<div class="stripes"><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div></div>
<script>
for(let i=0;i<60;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(8+Math.random()*7)+"s";
  p.style.opacity=Math.random()*0.7+0.3;
  document.body.appendChild(p);
}
</script>

<div id="dashboard">
<h2 class="logo">Astore Tourist Hub</h2>
<div class="hero-text">Owner: Asim Khanzai | WhatsApp: 03171588489 | Email: mohammadasimkhan2746@gmail.com</div>

<!-- Room Booking -->
<div id="room" class="dashboard-section" style="display:block;">
<h2>Room Booking</h2>
<form id="roomForm">
<label>Name</label><input type="text" id="rname" placeholder="Your Name" required>
<label>Phone</label><input type="text" id="rphone" placeholder="Phone Number" required>
<label>Check-in</label><input type="date" id="rcheckin" required>
<label>Check-out</label><input type="date" id="rcheckout" required>
<label>Room Type</label>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Room via WhatsApp</button>
</form>
</div>

<!-- Car Booking -->
<div id="car" class="dashboard-section">
<h2>Car Booking</h2>
<form id="carForm">
<label>Name</label><input type="text" id="cname" placeholder="Your Name" required>
<label>Phone</label><input type="text" id="cphone" placeholder="Phone Number" required>
<label>Pickup Date</label><input type="date" id="cdate" required>
<label>Car Type</label>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Local Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Car via WhatsApp</button>
</form>
</div>

<!-- Packages -->
<div id="packages" class="dashboard-section packages">
<div class="package"><i class="fa-solid fa-mountain"></i><h3>Basic Package</h3><p>2 Nights, 3 Days<br>Standard Room + Local Guide</p></div>
<div class="package"><i class="fa-solid fa-car"></i><h3>Luxury Package</h3><p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p></div>
<div class="package"><i class="fa-solid fa-person-hiking"></i><h3>Adventure Package</h3><p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p></div>
</div>

<!-- Map -->
<div id="map" class="dashboard-section map-container">
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<!-- Contact -->
<div id="contact" class="dashboard-section contact">
<p>Email: mohammadasimkhan2746@gmail.com</p>
<p>Owner: Asim Khanzai | WhatsApp: 03171588489</p>
</div>

<!-- ICON MENU -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="showSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="showSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="showSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="showSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="showSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
function showSection(section){
  document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");
  document.getElementById(section).style.display="block";
}

// Room WhatsApp
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
});

// Car WhatsApp
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
});
</script>
</body>
</html>
