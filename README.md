<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#000;overflow-x:hidden;}
.container{max-width:1000px;margin:0 auto;padding:20px;}
.logo{text-align:center;font-size:36px;color:#00eaff;font-family:'Orbitron',sans-serif;text-shadow:0 0 15px #00eaff;margin-top:15px;}
.hero-text{text-align:center;font-size:16px;color:#00fff0;margin:10px auto;max-width:90%;}
/* Slideshow */
.slideshow-container{position:relative;width:100%;max-height:300px;margin:20px auto;overflow:hidden;border-radius:15px;box-shadow:0 0 25px #00eaff;}
.slide{display:none;width:100%;}
.slide img{width:100%;height:300px;object-fit:cover;border-radius:15px;}
/* Sections */
section{display:none;padding:15px;margin-top:10px;background:rgba(0,0,0,0.3);border-radius:15px;box-shadow:0 0 20px #00eaff;}
section h2{color:#00eaff;text-shadow:0 0 10px #00fff0;margin-bottom:10px;}
section p{color:#a7f5ff;font-size:14px;line-height:1.5;}
section img{width:100%;border-radius:10px;margin-top:10px;box-shadow:0 0 15px #00eaff;}
/* Forms */
form{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
input,select,button{padding:10px;border-radius:10px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}
/* Booking History */
#historyList div{border:1px solid #00eaff;padding:8px;margin:5px;border-radius:8px;color:#a7f5ff;}
/* Bottom icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.4);padding:10px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:26px;cursor:pointer;transition:0.3s;}
.icon-item i.room{color:#00ff99;}
.icon-item i.car{color:#ff9900;}
.icon-item i.packages{color:#ff33cc;}
.icon-item i.map{color:#33ccff;}
.icon-item i.contact{color:#ff3333;}
.icon-item i:hover{transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;color:#fff;margin-top:3px;text-shadow:0 0 5px #000;}
/* WhatsApp */
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>

<div class="container">
<h1 class="logo">Welcome to Astore Tourist Information Hub</h1>
<div class="hero-text">Discover the breathtaking beauty of Gilgit-Baltistan, explore majestic mountains, rivers, and local culture. Plan your stay with us—rooms, cars, adventure packages, and more.</div>

<!-- Slideshow -->
<div class="slideshow-container">
<div class="slide"><img src="https://picsum.photos/id/1015/800/300" alt="Mountain"></div>
<div class="slide"><img src="https://picsum.photos/id/1025/800/300" alt="River"></div>
<div class="slide"><img src="https://picsum.photos/id/1035/800/300" alt="Valley"></div>
<div class="slide"><img src="https://picsum.photos/id/1045/800/300" alt="Nature"></div>
</div>

<!-- Sections -->
<section id="room">
<h2>Room Booking</h2>
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

<section id="car">
<h2>Car Booking</h2>
<form id="carForm">
<input type="text" id="cname" placeholder="Your Name" required>
<input type="text" id="cphone" placeholder="Phone Number" required>
<input type="date" id="cdate" required>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Local Jeep</option>
</select>
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book via WhatsApp</button>
</form>
</section>

<section id="packages">
<h2>Adventure Packages</h2>
<p><strong>Basic Package:</strong> 2 Nights, 3 Days | Standard Room + Local Guide</p>
<p><strong>Luxury Package:</strong> 4 Nights, 5 Days | Luxury Room + Car + Guide</p>
<p><strong>Adventure Package:</strong> 5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p>
</section>

<section id="map">
<h2>Find Us</h2>
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:15px;"></iframe>
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

</div>

<!-- Fixed Bottom Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed room" onclick="showSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car car" onclick="showSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain packages" onclick="showSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot map" onclick="showSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope contact" onclick="showSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Slideshow
let slideIndex=0;
showSlides();
function showSlides(){
  let slides=document.getElementsByClassName("slide");
  for(let i=0;i<slides.length;i++){slides[i].style.display="none";}
  slideIndex++;
  if(slideIndex>slides.length){slideIndex=1;}
  slides[slideIndex-1].style.display="block";
  setTimeout(showSlides,4000);
}

// Show section on icon click
function showSection(id){
  document.querySelectorAll("section").forEach(s=>s.style.display="none");
  document.getElementById(id).style.display="block";
}

// Room Booking WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Room",name:document.getElementById("rname").value,phone:document.getElementById("rphone").value,checkin:document.getElementById("rcheckin").value,checkout:document.getElementById("rcheckout").value,room:document.getElementById("rtype").value};
  const msg=`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
});

// Car Booking WhatsApp
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  const msg=`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`;
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`,"_blank");
  this.reset(); addHistory(booking);
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
  const list=document.getElementById("historyList");
  list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");
    if(b.type==="Room") div.innerHTML=`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`;
    if(b.type==="Car") div.innerHTML=`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    list.appendChild(div);
  });
}
loadHistory();
</script>

</body>
</html>
