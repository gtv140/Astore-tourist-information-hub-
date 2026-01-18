<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth;}
body{font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;background:#000;transition:0.5s;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000,#0f0f0f,#001f3f,#000);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
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

.container{max-width:1100px;margin:60px auto;background:rgba(0,0,0,0.4);padding:20px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;transition:0.5s;}
.logo{text-align:center;font-size:46px;font-weight:700;color:#00eaff;text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;margin-bottom:15px;font-family:'Orbitron',sans-serif;animation:glowPulse 2s infinite alternate;}
@keyframes glowPulse{0%{text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;}100%{text-shadow:0 0 30px #00eaff,0 0 60px #00ffff;}}
.hero-text{text-align:center;margin-bottom:20px;font-size:16px;font-weight:500;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;}

label{margin-top:12px;display:block;font-weight:500;}
input,select,button{width:100%;padding:10px;margin-top:6px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;font-size:15px;transition:0.3s;}
input:focus,select:focus{background:rgba(255,255,255,0.25);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s,box-shadow 0.5s;animation:btnPulse 2s infinite alternate;}
button:hover{background:#00bcd4;box-shadow:0 0 25px #00ffff;}
@keyframes btnPulse{0%{box-shadow:0 0 15px #00eaff;}100%{box-shadow:0 0 30px #00ffff;}}

.dashboard-section{display:none;margin-top:20px;}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:15px;margin-top:10px;}
.package{background:rgba(0,0,0,0.4);padding:15px;border-radius:15px;box-shadow:0 0 20px #00eaff;text-align:center;transition:0.3s, transform 0.5s;}
.package:hover{transform:scale(1.05);box-shadow:0 0 35px #00ffff;}
.package h3{text-shadow:0 0 15px #00eaff;font-family:'Orbitron',sans-serif;}
.package p{font-size:14px;color:#a7f5ff;}
.package i{font-size:32px;color:#00eaff;margin-bottom:8px;display:block;}

.map-container{margin-top:15px;border-radius:15px;overflow:hidden;box-shadow:0 0 25px #00eaff;}
.contact{margin-top:15px;text-align:center;font-size:14px;color:#00eaff;}

.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:15px;left:0;width:100%;background:rgba(0,0,0,0.3);padding:8px 0;box-shadow:0 0 15px #00eaff;border-radius:20px;z-index:9999;}
.icon-item{text-align:center;position:relative;}
.icon-item i{font-size:26px;cursor:pointer;transition:0.3s;}
.icon-item i:hover{transform:scale(1.2);}
.icon-item span{display:block;font-size:11px;margin-top:2px;color:#00ffff;text-shadow:0 0 5px #00eaff;}

#logoutBtn{position:fixed;top:15px;right:15px;width:40px;height:40px;font-size:18px;padding:0;background:#ff4444;border:none;border-radius:50%;box-shadow:0 0 12px #ff6666;color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;z-index:9999;transition:0.3s;}
#logoutBtn:hover{transform:scale(1.1);}

.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:14px 16px;border-radius:50%;color:#fff;font-size:26px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s, box-shadow 0.5s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>
<div class="bg-animate"></div>
<div class="stripes">
  <div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div>
</div>
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

<div class="container" id="dashboard">
<h2 class="logo">Astore Tourist Hub</h2>
<div class="hero-text">Explore Astore with our guided tours, comfortable rooms, and local transport options! Contact Owner: Asim Khanzai | WhatsApp: 03171588489 | Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00ffff;">mohammadasimkhan2746@gmail.com</a></div>

<button id="logoutBtn" onclick="logout()"><i class="fa-solid fa-right-from-bracket"></i></button>

<div id="room" class="dashboard-section">
<h3>🏨 Room Booking</h3>
<form id="roomForm">
<label>Name</label><input type="text" id="rname" required>
<label>Phone</label><input type="text" id="rphone" required>
<label>Check-in</label><input type="date" id="rcheckin" required>
<label>Check-out</label><input type="date" id="rcheckout" required>
<label>Room Type</label>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</div>

<div id="car" class="dashboard-section">
<h3>🚗 Car Booking</h3>
<form id="carForm">
<label>Name</label><input type="text" id="cname" required>
<label>Phone</label><input type="text" id="cphone" required>
<label>Pickup Date</label><input type="date" id="cdate" required>
<label>Car Type</label>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</div>

<div id="packages" class="dashboard-section packages">
<div class="package"><i class="fa-solid fa-mountain"></i><h3>Basic Tour</h3><p>2 Nights, 3 Days<br>Standard Room + Local Guide</p></div>
<div class="package"><i class="fa-solid fa-car"></i><h3>Luxury Tour</h3><p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p></div>
<div class="package"><i class="fa-solid fa-person-hiking"></i><h3>Adventure Tour</h3><p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p></div>
</div>

<div id="map" class="dashboard-section map-container">
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<div id="contact" class="dashboard-section contact">
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00ffff;">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#00ff99;">03171588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#00ffff;">Astore Hub Page</a></p>
</div>

<!-- ICON MENU -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="showSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="showSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="showSection('packages')"></i><span>Tours</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="showSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="showSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Dashboard functionality
function showSection(section){
  document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");
  document.getElementById(section).style.display="block";
}
function logout(){alert('Thanks for visiting Astore Hub!');}

// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const name=document.getElementById("rname").value;
  const phone=document.getElementById("rphone").value;
  const checkin=document.getElementById("rcheckin").value;
  const checkout=document.getElementById("rcheckout").value;
  const room=document.getElementById("rtype").value;
  const msg=`Room Booking:\nName: ${name}\nPhone: ${phone}\nCheck-in: ${checkin}\nCheck-out: ${checkout}\nRoom: ${room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
  this.reset();
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const name=document.getElementById("cname").value;
  const phone=document.getElementById("cphone").value;
  const date=document.getElementById("cdate").value;
  const car=document.getElementById("ctype").value;
  const msg=`Car Booking:\nName: ${name}\nPhone: ${phone}\nPickup Date: ${date}\nCar: ${car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
  this.reset();
});

// Initialize default section
showSection('room');
</script>
</body>
</html>
