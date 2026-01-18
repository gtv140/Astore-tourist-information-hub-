<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{background:#f5f5f5;color:#333;line-height:1.6;}
header{background:#00bcd4;color:#fff;padding:20px;text-align:center;}
header h1{margin-bottom:5px;}
header p{font-size:14px;}
.container{max-width:1000px;margin:20px auto;padding:10px;}
section{margin-bottom:40px;}
h2{margin-bottom:15px;color:#00bcd4;text-align:center;}
button, input, select{padding:10px;margin-top:5px;width:100%;border-radius:8px;border:1px solid #ccc;}
button{background:#00bcd4;color:#fff;font-weight:600;cursor:pointer;}
button:hover{background:#0097a7;}
input, select{border:1px solid #999;}
.package{border:1px solid #00bcd4;border-radius:10px;padding:15px;margin:10px 0;background:#e0f7fa;}
.package h3{color:#007c91;}
.package p{font-size:14px;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:0;width:100%;background:#00bcd4;padding:10px 0;color:#fff;z-index:999;}
.icon-item{text-align:center;}
.icon-item i{font-size:24px;cursor:pointer;}
.icon-item span{display:block;font-size:12px;margin-top:2px;}
.gallery{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:10px;}
.gallery img{width:100%;border-radius:8px;}
.booking-history div{border:1px solid #00bcd4;padding:8px;margin:5px;border-radius:8px;background:#e0f7fa;}
.contact a{color:#00bcd4;text-decoration:none;}
</style>
</head>
<body>

<header>
<h1>Astore Tourist Information Hub</h1>
<p>Owner: Asim Khanzai | WhatsApp: <a href="https://wa.me/923171588489">03171588489</a> | Email: <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
</header>

<div class="container">

<section id="about">
<h2>About Astore</h2>
<p>Astore is a beautiful valley in northern Pakistan, known for its breathtaking mountains, serene lakes, and vibrant local culture. Our Tourist Information Hub helps visitors explore the best spots, book rooms, hire cars, and discover local adventure packages.</p>
</section>

<section id="gallery">
<h2>Gallery</h2>
<div class="gallery">
<img src="https://source.unsplash.com/300x200/?mountain" alt="Mountain">
<img src="https://source.unsplash.com/300x200/?lake" alt="Lake">
<img src="https://source.unsplash.com/300x200/?forest" alt="Forest">
<img src="https://source.unsplash.com/300x200/?river" alt="River">
<img src="https://source.unsplash.com/300x200/?tourist" alt="Tourist">
<img src="https://source.unsplash.com/300x200/?hiking" alt="Hiking">
</div>
</section>

<section id="rooms">
<h2>Room Booking</h2>
<form id="roomForm">
<input type="text" id="rname" placeholder="Your Name" required>
<input type="text" id="rphone" placeholder="Phone Number" required>
<label>Check-in</label><input type="date" id="rcheckin" required>
<label>Check-out</label><input type="date" id="rcheckout" required>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</section>

<section id="cars">
<h2>Car Booking</h2>
<form id="carForm">
<input type="text" id="cname" placeholder="Your Name" required>
<input type="text" id="cphone" placeholder="Phone Number" required>
<label>Pickup Date</label><input type="date" id="cdate" required>
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
<h2>Tour Packages</h2>
<div class="package">
<h3>Basic Package</h3>
<p>2 Nights, 3 Days<br>Standard Room + Local Guide</p>
</div>
<div class="package">
<h3>Luxury Package</h3>
<p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p>
</div>
<div class="package">
<h3>Adventure Package</h3>
<p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p>
</div>
</section>

<section id="map">
<h2>Location</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;"></iframe>
</section>

<section id="contact">
<h2>Contact</h2>
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
<p>WhatsApp: <a href="https://wa.me/923171588489">03171588489</a></p>
<p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Click Here</a></p>
</section>

<section id="history">
<h2>Booking History</h2>
<div class="booking-history" id="historyList">No bookings yet</div>
</section>

</div>

<div class="icon-menu">
<div class="icon-item" onclick="scrollToSection('rooms')"><i class="fa-solid fa-bed"></i><span>Room</span></div>
<div class="icon-item" onclick="scrollToSection('cars')"><i class="fa-solid fa-car"></i><span>Car</span></div>
<div class="icon-item" onclick="scrollToSection('packages')"><i class="fa-solid fa-mountain"></i><span>Packages</span></div>
<div class="icon-item" onclick="scrollToSection('map')"><i class="fa-solid fa-map-location-dot"></i><span>Map</span></div>
<div class="icon-item" onclick="scrollToSection('contact')"><i class="fa-solid fa-envelope"></i><span>Contact</span></div>
</div>

<script>
// Smooth scroll
function scrollToSection(id){
document.getElementById(id).scrollIntoView({behavior:'smooth'});
}

// Room booking WhatsApp
document.getElementById("roomForm").addEventListener("submit", function(e){
e.preventDefault();
const name = document.getElementById("rname").value;
const phone = document.getElementById("rphone").value;
const checkin = document.getElementById("rcheckin").value;
const checkout = document.getElementById("rcheckout").value;
const room = document.getElementById("rtype").value;
const msg = `Room Booking:\nName: ${name}\nPhone: ${phone}\nCheck-in: ${checkin}\nCheck-out: ${checkout}\nRoom: ${room}`;
window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
this.reset();
});

// Car booking WhatsApp
document.getElementById("carForm").addEventListener("submit", function(e){
e.preventDefault();
const name = document.getElementById("cname").value;
const phone = document.getElementById("cphone").value;
const date = document.getElementById("cdate").value;
const car = document.getElementById("ctype").value;
const msg = `Car Booking:\nName: ${name}\nPhone: ${phone}\nPickup Date: ${date}\nCar: ${car}`;
window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`, "_blank");
this.reset();
});
</script>

</body>
</html>
