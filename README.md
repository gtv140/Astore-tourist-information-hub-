<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Astore Tourist Information Hub</title>

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>

<style>
/* Background Neon Animation */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: black;
  color: white;
  overflow-x: hidden;
}

.neon-bg {
  position: fixed;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle,#00111a,#000000);
  animation: glow 6s infinite alternate;
  z-index: -1;
}
@keyframes glow {
  0% { filter: hue-rotate(0deg) brightness(1); }
  100% { filter: hue-rotate(90deg) brightness(1.4); }
}

/* Header */
header {
  text-align: center;
  padding: 25px;
  font-size: 26px;
  font-weight: bold;
  text-shadow: 0 0 10px #00eaff;
}

/* Dashboard Content */
.container {
  padding: 20px;
  margin-bottom: 90px;
}

.section {
  display: none;
  padding: 20px;
  background: rgba(0,0,0,0.4);
  border-radius: 12px;
  box-shadow: 0 0 15px #00eaff;
  margin-bottom: 20px;
}

.section h2 {
  text-align: center;
  text-shadow: 0 0 10px #00eaff;
}

/* Fixed Bottom Icon Menu */
.icon-menu {
  display: flex;
  justify-content: space-around;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 12px 0;
  background: rgba(0,0,0,0.6);
  border-top: 1px solid #00eaff;
  box-shadow: 0 0 15px #00eaff;
  z-index: 9999;
}

.icon-menu div {
  color: #00eaff;
  text-align: center;
  font-size: 22px;
}

.icon-menu div span {
  font-size: 12px;
  display: block;
  margin-top: 3px;
}

/* Buttons */
button {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  background: #00eaff;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  font-weight: bold;
  color: black;
  box-shadow: 0 0 10px #00eaff;
}
button:hover {
  filter: brightness(1.2);
}

/* Forms */
input, select {
  width: 100%;
  padding: 12px;
  margin-top: 8px;
  border-radius: 6px;
  border: none;
  outline: none;
}

a {
  color: #00eaff;
  text-decoration: none;
}
a:hover {
  text-shadow: 0 0 10px #00eaff;
}
</style>
</head>

<body>

<div class="neon-bg"></div>

<header>
  🌌 ASTORE TOURIST INFORMATION HUB 🌌  
  <div style="font-size:14px;margin-top:5px;">Owner: Asim Khanzai</div>
</header>

<div class="container">

<!-- ABOUT SECTION -->
<div id="about" class="section" style="display:block;">
<h2>About Astore Tourist Information Hub</h2>
<p style="line-height:1.6; font-size:15px;">
Astore Tourist Information Hub is your trusted gateway to the breathtaking valleys of Astore,
Gilgit-Baltistan — a paradise of mountains, lakes, meadows and unforgettable adventure.
<br><br>
We provide complete assistance for:
<br>✔ Room Booking  
<br>✔ Car / Jeep Booking  
<br>✔ Tourist Guidance  
<br>✔ Local Area Information  
<br>✔ Family Tours & Private Trips  
<br><br>
Our mission is to make your journey smooth, safe and memorable. Whether you are exploring  
Rama Lake, Minimarg, Deosai, Chillam, Tarishing or Rupal — we guide you with real and reliable information.
</p>

<h3>📍 Contact Information</h3>
<p>
<b>Facebook:</b>  
<a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">
Visit Page <i class="fa-brands fa-facebook"></i>
</a><br><br>

<b>WhatsApp:</b>  
<a href="https://wa.me/03171588489" target="_blank">
0317-1588489 <i class="fa-brands fa-whatsapp"></i>
</a><br><br>

<b>Email:</b>  
<a href="mailto:mohammadasimkhan2746@gmail.com">
mohammadasimkhan2746@gmail.com <i class="fa-solid fa-envelope"></i>
</a><br><br>

<b>Google Map:</b><br>
<a href="https://maps.google.com/?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore+14300" target="_blank">
Open Location <i class="fa-solid fa-map-location-dot"></i>
</a>
</p>
</div>

<!-- ROOM BOOKING -->
<div id="rooms" class="section">
<h2>Room Booking</h2>
<input id="rname" placeholder="Your Name">
<input id="rphone" placeholder="Phone Number">
<input id="rcheckin" type="date">
<input id="rcheckout" type="date">
<select id="rroom">
<option>Single Room</option>
<option>Double Room</option>
<option>Family Suite</option>
<option>Luxury Room</option>
</select>
<button onclick="roomBooking()">Book on WhatsApp</button>
</div>

<!-- CAR BOOKING -->
<div id="cars" class="section">
<h2>Car / Jeep Booking</h2>
<input id="cname" placeholder="Your Name">
<input id="cphone" placeholder="Phone Number">
<input id="cdate" type="date">
<select id="ccar">
<option>Jeep (4×4 – Astore Local)</option>
<option>Prado</option>
<option>Corolla</option>
<option>Hiace</option>
</select>
<button onclick="carBooking()">Book on WhatsApp</button>
</div>

<!-- CONTACT SECTION -->
<div id="contact" class="section">
<h2>Contact Us</h2>
<p style="text-align:center;">Feel free to reach us anytime.</p>
<p><b>Owner:</b> Asim Khanzai</p>
<p><b>Phone/WhatsApp:</b> 0317-1588489</p>
<p><b>Email:</b> <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
<p><b>Facebook:</b>  
<a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Facebook Page</a></p>
</div>

</div>

<!-- FIXED BOTTOM ICON MENU -->
<div class="icon-menu">
  <div onclick="show('about')"><i class="fa-solid fa-house"></i><span>Home</span></div>
  <div onclick="show('rooms')"><i class="fa-solid fa-bed"></i><span>Rooms</span></div>
  <div onclick="show('cars')"><i class="fa-solid fa-car"></i><span>Cars</span></div>
  <div onclick="show('contact')"><i class="fa-solid fa-phone"></i><span>Contact</span></div>
</div>

<script>
function show(sec){
  document.querySelectorAll('.section').forEach(s=>s.style.display="none");
  document.getElementById(sec).style.display="block";
}

function roomBooking(){
  let name = rname.value;
  let phone = rphone.value;
  let ci = rcheckin.value;
  let co = rcheckout.value;
  let room = rroom.value;

  let msg = `Room Booking Request:
Name: ${name}
Phone: ${phone}
Check-in: ${ci}
Check-out: ${co}
Room Type: ${room}`;

  window.open(`https://wa.me/03171588489?text=${encodeURIComponent(msg)}`);
}

function carBooking(){
  let name = cname.value;
  let phone = cphone.value;
  let date = cdate.value;
  let car = ccar.value;

  let msg = `Car Booking Request:
Name: ${name}
Phone: ${phone}
Pickup Date: ${date}
Car Type: ${car}`;

  window.open(`https://wa.me/03171588489?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
