<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
/* ========== GLOBAL STYLING ========== */
body{
  margin:0;
  padding:0;
  font-family: Arial, sans-serif;
  color:white;
  overflow-x:hidden;
  background:#000;
}

/* Neon animated background */
@keyframes neonBG {
  0%{ background:#000022; }
  50%{ background:#001133; }
  100%{ background:#000022; }
}

html,body{
  height:100%;
  animation:neonBG 6s infinite alternate ease-in-out;
}

/* Header */
header{
  text-align:center;
  padding:25px 15px;
  font-size:28px;
  font-weight:bold;
  letter-spacing:1px;
  text-shadow:0 0 15px #00eaff;
}

/* Section Boxes */
.section{
  margin:15px;
  padding:20px;
  background:rgba(0,0,0,0.4);
  border-radius:20px;
  box-shadow:0 0 20px #00eaff;
  backdrop-filter: blur(5px);
}

/* Section titles */
.section h2{
  margin:0 0 10px 0;
  font-size:22px;
  text-shadow:0 0 10px #00eaff;
}

/* Form inputs */
input, select{
  width:100%;
  padding:12px;
  margin:8px 0;
  border:none;
  border-radius:10px;
  background:#0a0a1f;
  color:white;
  box-shadow:0 0 10px #00bfff;
}

/* Buttons */
button{
  width:100%;
  padding:12px;
  background:#00eaff;
  color:#000;
  border:none;
  border-radius:10px;
  font-size:18px;
  margin-top:10px;
  box-shadow:0 0 15px #00eaff;
  font-weight:bold;
}

/* Contact links */
a{
  color:#00eaff;
  font-size:18px;
  text-decoration:none;
}

/* Fixed bottom icons menu */
.icon-menu{
  position:fixed;
  bottom:0;
  width:100%;
  display:flex;
  justify-content:space-around;
  background:rgba(0,0,20,0.8);
  padding:10px 0;
  box-shadow:0 0 20px #00eaff;
  border-top:1px solid #00eaff;
}

.icon-menu div{
  text-align:center;
}

.icon-menu i{
  font-size:22px;
  color:#00eaff;
}

.icon-menu p{
  margin:2px 0 0 0;
  font-size:12px;
}

/* Dashboard Welcome */
#welcome{
  font-size:20px;
  text-align:center;
  margin:10px;
  text-shadow:0 0 10px #0088ff;
}
</style>
</head>
<body>

<header>Astore Tourist Information Hub</header>

<div id="welcome">
  Welcome to Astore — The Land of Peace, Beauty & Adventure 🌄<br>
  Discover Rooms, Cars, Tourist Spots & Local Guide Services!
</div>

<!-- ========== CONTACT SECTION ========== -->
<div class="section">
  <h2>Contact & Social Links</h2>

  <p><i class="fa-solid fa-phone"></i> WhatsApp: 
     <a href="https://wa.me/03171588489" target="_blank">0317-1588489</a></p>

  <p><i class="fa-solid fa-envelope"></i> Email:  
     <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>

  <p><i class="fa-brands fa-facebook"></i> Facebook:
     <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">
     Astore Info Hub Official Page</a></p>

  <p><i class="fa-solid fa-location-dot"></i> Google Map:  
     <a href="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300" target="_blank">
     View Location</a></p>
</div>

<!-- ========== ROOM BOOKING ========== -->
<div class="section">
  <h2>Room Booking</h2>
  <input id="rname" placeholder="Your Name">
  <input id="rphone" placeholder="Phone Number">
  <input type="date" id="rcheckin">
  <input type="date" id="rcheckout">
  <select id="rroom">
    <option disabled selected>Select Room Type</option>
    <option>Standard Room</option>
    <option>Luxury Room</option>
    <option>Family Room</option>
  </select>
  <button onclick="sendRoom()">Book via WhatsApp</button>
</div>

<!-- ========== CAR BOOKING ========== -->
<div class="section">
  <h2>Car Booking</h2>
  <input id="cname" placeholder="Your Name">
  <input id="cphone" placeholder="Phone Number">
  <input type="date" id="cdate">
  <select id="ccar">
    <option disabled selected>Select Car Type</option>
    <option>Prado</option>
    <option>Toyota Corolla</option>
    <option>HiAce</option>
    <option>Jeep for Mountains</option>
  </select>
  <button onclick="sendCar()">Book via WhatsApp</button>
</div>

<!-- ========== TOURIST INFO ========== -->
<div class="section">
  <h2>Astore Tourism Highlights</h2>
  <p>📍 Rama Meadows</p>
  <p>📍 Minimarg</p>
  <p>📍 Rainbow Lake</p>
  <p>📍 Tarishing Valley</p>
  <p>📍 Deosai Plains Access</p>
  <p>📍 Chillam Valley</p>
</div>

<!-- ========== FIXED ICON MENU ========== -->
<div class="icon-menu">
  <div><i class="fa-solid fa-hotel"></i><p>Rooms</p></div>
  <div><i class="fa-solid fa-car"></i><p>Cars</p></div>
  <div><i class="fa-solid fa-map"></i><p>Places</p></div>
  <div><i class="fa-solid fa-phone"></i><p>Contact</p></div>
</div>

<script>
function sendRoom(){
  let n = document.getElementById("rname").value;
  let p = document.getElementById("rphone").value;
  let ci = document.getElementById("rcheckin").value;
  let co = document.getElementById("rcheckout").value;
  let r = document.getElementById("rroom").value;

  let msg = 
 `Room Booking Request:
Name: ${n}
Phone: ${p}
Check-in: ${ci}
Check-out: ${co}
Room Type: ${r}`;

  window.open(`https://wa.me/03171588489?text=${encodeURIComponent(msg)}`);
}

function sendCar(){
  let n = document.getElementById("cname").value;
  let p = document.getElementById("cphone").value;
  let d = document.getElementById("cdate").value;
  let c = document.getElementById("ccar").value;

  let msg =
`Car Booking Request:
Name: ${n}
Phone: ${p}
Pickup Date: ${d}
Car Type: ${c}`;

  window.open(`https://wa.me/03171588489?text=${encodeURIComponent(msg)}`);
}
</script>

</body>
</html>
