<Astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
body{margin:0;font-family:'Poppins',sans-serif;background:#000;color:#fff;overflow-x:hidden;}
.container{max-width:1000px;margin:20px auto;padding:20px;background:rgba(0,0,0,0.5);border-radius:15px;backdrop-filter:blur(10px);}
.logo{text-align:center;font-size:40px;font-family:'Orbitron',sans-serif;color:#0ff;text-shadow:0 0 10px #0ff,0 0 20px #0ff;margin-bottom:10px;}
.hero-text{text-align:center;font-size:16px;margin-bottom:15px;color:#0ff;}
input,select,button{width:100%;padding:10px;margin-top:6px;border-radius:8px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
button{background:#0ff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#0aa;}
.dashboard-section{margin-top:20px;display:none;}
img.tourist-photo{width:100%;border-radius:12px;margin-top:10px;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:10px;width:100%;background:rgba(0,0,0,0.3);padding:8px 0;border-radius:15px;z-index:999;}
.icon-item{text-align:center;}
.icon-item i{font-size:24px;color:#0ff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;color:#0ff;}
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:14px 16px;border-radius:50%;color:#fff;font-size:26px;text-decoration:none;}
#logoutBtn{position:fixed;top:10px;right:10px;background:#f44;color:#fff;border:none;border-radius:50%;width:40px;height:40px;font-size:18px;cursor:pointer;}
</style>
</head>
<body>

<div class="container" id="dashboard">
<h2 class="logo">Astore Tourist Hub</h2>
<div class="hero-text">Explore the beauty of Astore! Contact: Asim Khanzai | WhatsApp: <a href="https://wa.me/923171588489" style="color:#0ff;">03171588489</a> | Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#0ff;">mohammadasimkhan2746@gmail.com</a></div>

<button id="logoutBtn" onclick="alert('Thanks for visiting Astore Hub!')"><i class="fa-solid fa-right-from-bracket"></i></button>

<div id="room" class="dashboard-section">
<h3>🏨 Room Booking</h3>
<img src="https://source.unsplash.com/400x200/?hotel" class="tourist-photo">
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
<img src="https://source.unsplash.com/400x200/?car" class="tourist-photo">
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

<div id="packages" class="dashboard-section">
<h3>🏔 Tours & Packages</h3>
<img src="https://source.unsplash.com/400x200/?mountain,travel" class="tourist-photo">
<div style="margin-top:10px;">
<p>Basic Tour: 2 Nights, 3 Days, Standard Room + Local Guide</p>
<p>Luxury Tour: 4 Nights, 5 Days, Luxury Room + Car + Guide</p>
<p>Adventure Tour: 5 Nights, 6 Days, Family Suite + Jeep Tour + Hiking</p>
</div>
</div>

<div id="map" class="dashboard-section">
<h3>📍 Location</h3>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="200" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<div id="contact" class="dashboard-section">
<h3>📧 Contact</h3>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#0ff;">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#0ff;">03171588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#0ff;">Astore Hub Page</a></p>
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
function showSection(section){
  document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");
  document.getElementById(section).style.display="block";
}

// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const name=document.getElementById("rname").value;
  const phone=document.getElementById("rphone").value;
  const checkin=document.getElementById("rcheckin").value;
  const checkout=document.getElementById("rcheckout").value;
  const room=document.getElementById("rtype").value;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(`Room Booking:\nName:${name}\nPhone:${phone}\nCheck-in:${checkin}\nCheck-out:${checkout}\nRoom:${room}`)}`, "_blank");
  this.reset();
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const name=document.getElementById("cname").value;
  const phone=document.getElementById("cphone").value;
  const date=document.getElementById("cdate").value;
  const car=document.getElementById("ctype").value;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(`Car Booking:\nName:${name}\nPhone:${phone}\nPickup Date:${date}\nCar:${car}`)}`, "_blank");
  this.reset();
});

// Initialize default section
showSection('room');
</script>

</body>
</html>
