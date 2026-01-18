<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth;font-family:'Poppins',sans-serif;}
body{background:#000;color:#fff;}
a{text-decoration:none;color:#00eaff;}
.container{max-width:1100px;margin:50px auto;padding:20px;}
h1,h2,h3{color:#00eaff;}
button{cursor:pointer;border:none;border-radius:8px;padding:10px 15px;background:#00eaff;color:#000;font-weight:600;margin-top:10px;transition:0.3s;}
button:hover{background:#00bcd4;}
input,select{width:100%;padding:10px;margin-top:5px;border-radius:8px;border:none;background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
.dashboard-section{margin-top:30px;}
.photo-gallery{display:flex;overflow-x:auto;gap:15px;margin-top:15px;padding-bottom:10px;}
.photo-gallery img{width:200px;height:140px;border-radius:12px;object-fit:cover;flex-shrink:0;}
.icon-menu{display:flex;justify-content:space-around;background:rgba(0,0,0,0.6);padding:12px 0;position:fixed;bottom:0;width:100%;z-index:999;border-top:1px solid #00eaff;}
.icon-item{text-align:center;color:#00eaff;}
.icon-item i{font-size:24px;}
.icon-item span{display:block;font-size:12px;margin-top:3px;}
#logoutBtn{position:fixed;top:15px;right:15px;background:#ff4444;color:#fff;width:40px;height:40px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:18px;}
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:14px 16px;border-radius:50%;color:#fff;font-size:26px;}
/* Scrollbar for gallery */
.photo-gallery::-webkit-scrollbar{height:6px;}
.photo-gallery::-webkit-scrollbar-thumb{background:#00eaff;border-radius:3px;}
</style>
</head>
<body>
<div class="container">
<h1>Astore Tourist Hub</h1>
<p>Explore Astore's breathtaking valleys, rivers, and mountains. Book rooms or cars easily and discover adventure packages!</p>

<!-- Dashboard -->
<div id="dashboard">
<h2>Welcome, <span id="userDisplay">Guest</span>!</h2>
<button id="logoutBtn" onclick="logout()"><i class="fa-solid fa-right-from-bracket"></i></button>

<!-- Rooms -->
<div id="room" class="dashboard-section">
<h2>Room Booking</h2>
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
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Room via WhatsApp</button>
</form>
</div>

<!-- Cars -->
<div id="car" class="dashboard-section">
<h2>Car Booking</h2>
<form id="carForm">
<label>Name</label><input type="text" id="cname" required>
<label>Phone</label><input type="text" id="cphone" required>
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
<div id="packages" class="dashboard-section">
<h2>Adventure Packages</h2>
<div class="photo-gallery">
<img src="https://source.unsplash.com/300x200/?mountain" alt="Mountain">
<img src="https://source.unsplash.com/300x200/?valley" alt="Valley">
<img src="https://source.unsplash.com/300x200/?river" alt="River">
<img src="https://source.unsplash.com/300x200/?forest" alt="Forest">
<img src="https://source.unsplash.com/300x200/?hiking" alt="Hiking">
</div>
<p>Choose from Basic, Luxury, or Adventure packages with rooms, guides, and jeep tours included.</p>
</div>

<!-- Map -->
<div id="map" class="dashboard-section">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Astore,+Pakistan&output=embed" width="100%" height="250" style="border:0;"></iframe>
</div>

<!-- Contact -->
<div id="contact" class="dashboard-section">
<h2>Contact</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489" target="_blank">0317-1588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/" target="_blank">Our Page</a></p>
</div>

<!-- Booking History -->
<div id="historySection" class="dashboard-section">
<h2>Booking History</h2>
<div id="historyList"></div>
</div>
</div>

<!-- Icon Menu -->
<div class="icon-menu">
<div class="icon-item" onclick="showSection('room')"><i class="fa-solid fa-bed"></i><span>Rooms</span></div>
<div class="icon-item" onclick="showSection('car')"><i class="fa-solid fa-car"></i><span>Cars</span></div>
<div class="icon-item" onclick="showSection('packages')"><i class="fa-solid fa-mountain"></i><span>Packages</span></div>
<div class="icon-item" onclick="showSection('map')"><i class="fa-solid fa-map-location-dot"></i><span>Map</span></div>
<div class="icon-item" onclick="showSection('contact')"><i class="fa-solid fa-envelope"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Guest default
document.getElementById("userDisplay").textContent = "Guest";

// Sections
function showSection(section){
document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");
document.getElementById(section).style.display="block";
}

// Logout
function logout(){alert("You are now logged out");}

// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
e.preventDefault();
const booking=`Room Booking:
Name: ${document.getElementById("rname").value}
Phone: ${document.getElementById("rphone").value}
Check-in: ${document.getElementById("rcheckin").value}
Check-out: ${document.getElementById("rcheckout").value}
Room: ${document.getElementById("rtype").value}`;
window.open(`https://wa.me/923171588489?text=${encodeURIComponent(booking)}`,"_blank");
this.reset();
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
e.preventDefault();
const booking=`Car Booking:
Name: ${document.getElementById("cname").value}
Phone: ${document.getElementById("cphone").value}
Pickup Date: ${document.getElementById("cdate").value}
Car: ${document.getElementById("ctype").value}`;
window.open(`https://wa.me/923171588489?text=${encodeURIComponent(booking)}`,"_blank");
this.reset();
});
</script>
</body>
</html>
