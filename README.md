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
body{font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;background:#000;transition:0.5s;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000000,#0f0f0f,#001f3f,#000000);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
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
.container{max-width:1100px;margin:60px auto;background:rgba(0,0,0,0.4);padding:30px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;transition:0.5s;}
.logo{text-align:center;font-size:46px;font-weight:700;color:#00eaff;text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;margin-bottom:20px;font-family:'Orbitron',sans-serif;animation:glowPulse 2s infinite alternate;}
@keyframes glowPulse{0%{text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;}100%{text-shadow:0 0 30px #00eaff,0 0 60px #00ffff;}}
.hero-text{text-align:center;margin-bottom:30px;font-size:18px;font-weight:500;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;opacity:1;}
label{margin-top:12px;display:block;font-weight:500;}
input,select,button{width:100%;padding:12px;margin-top:6px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;font-size:15px;transition:0.3s;}
input:focus,select:focus{background:rgba(255,255,255,0.25);outline:none;}
button{background:#00eaff;color:#000;font-size:16px;font-weight:600;cursor:pointer;transition:0.3s,box-shadow 0.5s;animation:btnPulse 2s infinite alternate;}
button:hover{background:#00bcd4;box-shadow:0 0 25px #00ffff;}
@keyframes btnPulse{0%{box-shadow:0 0 15px #00eaff;}100%{box-shadow:0 0 30px #00ffff;}}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;margin-top:20px;}
.package{background:rgba(0,0,0,0.4);padding:20px;border-radius:15px;box-shadow:0 0 25px #00eaff;text-align:center;transition:0.3s, transform 0.5s;}
.package:hover{transform:scale(1.05);box-shadow:0 0 40px #00ffff;}
.package h3{text-shadow:0 0 15px #00eaff;font-family:'Orbitron',sans-serif;}
.package p{font-size:14px;color:#a7f5ff;}
.package i{font-size:36px;margin-bottom:10px;display:block;}
.map-container{margin-top:20px;border-radius:15px;overflow:hidden;box-shadow:0 0 25px #00eaff;}
.contact{margin-top:20px;text-align:center;font-size:16px;color:#00eaff;}
#dashboard{max-width:700px;margin:40px auto;background:rgba(0,0,0,0.4);padding:25px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;text-align:center;position:relative;}
.dashboard-section{display:none;margin-top:20px;}
#logoutBtn{position:absolute;top:15px;right:15px;width:45px;height:45px;font-size:20px;padding:0;background:#ff4444;border:none;border-radius:50%;box-shadow:0 0 15px #ff6666;color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;z-index:9999;transition:0.3s;}
#logoutBtn:hover{transform:scale(1.1);}
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s, box-shadow 0.5s;}
.whatsapp-btn:hover{transform:scale(1.1);}
.icon-menu-left,.icon-menu-right{position:fixed;top:50%;transform:translateY(-50%);display:flex;flex-direction:column;gap:15px;z-index:9999;}
.icon-menu-left{left:5px;}
.icon-menu-right{right:5px;}
.icon-menu-left i,.icon-menu-right i{font-size:28px;cursor:pointer;transition:0.3s;}
.icon-menu-left i:hover,.icon-menu-right i:hover{transform:scale(1.2);}
.icon-menu-left i{color:#ff5eff;}
.icon-menu-right i{color:#00eaff;}
@media(max-width:600px){.container,#dashboard{padding:15px;}.packages{grid-template-columns:1fr;}.hero-text{font-size:16px;}}
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
<h2>Welcome to Astore Tourist Hub!</h2>
<p style="margin-bottom:10px;">Explore the breathtaking valleys, mountains & culture of Astore. Book rooms, cars, and adventure packages easily!</p>
<button id="logoutBtn" onclick="alert('Logged out')"><i class="fa-solid fa-right-from-bracket"></i></button>

<div id="rooms" class="dashboard-section" style="display:block;">
<h3>Room Booking</h3>
<label>Name</label><input type="text" placeholder="Your Name">
<label>Phone</label><input type="text" placeholder="Phone Number">
<label>Check-in</label><input type="date">
<label>Check-out</label><input type="date">
<label>Room Type</label>
<select><option>Standard Room</option><option>Luxury Room</option><option>Family Suite</option></select>
<button><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>

<div id="cars" class="dashboard-section">
<h3>Car Booking</h3>
<label>Name</label><input type="text" placeholder="Your Name">
<label>Phone</label><input type="text" placeholder="Phone Number">
<label>Pickup Date</label><input type="date">
<label>Car Type</label>
<select><option>Corolla</option><option>Hiace</option><option>Prado</option><option>Jeep</option></select>
<button><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</div>

<div id="packages" class="dashboard-section packages">
<div class="package"><i class="fa-solid fa-mountain"></i><h3>Adventure Package</h3><p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p></div>
<div class="package"><i class="fa-solid fa-car"></i><h3>Luxury Package</h3><p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p></div>
<div class="package"><i class="fa-solid fa-person-hiking"></i><h3>Basic Package</h3><p>2 Nights, 3 Days<br>Standard Room + Local Guide</p></div>
</div>

<div id="map" class="dashboard-section map-container">
<iframe src="https://www.google.com/maps?q=Astore,+Pakistan&output=embed" width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<div id="contact" class="dashboard-section contact">
<p>Email: info@astorehub.com</p>
<p>WhatsApp: +92 317 1588489</p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">Visit</a></p>
</div>
</div>

<div class="icon-menu-left">
<i class="fa-solid fa-bed" onclick="showSection('rooms')"></i>
<i class="fa-solid fa-car" onclick="showSection('cars')"></i>
</div>
<div class="icon-menu-right">
<i class="fa-solid fa-mountain" onclick="showSection('packages')"></i>
<i class="fa-solid fa-map-location-dot" onclick="showSection('map')"></i>
<i class="fa-solid fa-envelope" onclick="showSection('contact')"></i>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
function showSection(id){
  document.querySelectorAll('.dashboard-section').forEach(s=>s.style.display='none');
  document.getElementById(id).style.display='block';
}
</script>
</body>
</html>
