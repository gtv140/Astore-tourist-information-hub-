<astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#0a0a0a;overflow-x:hidden;line-height:1.5;}
.container{max-width:1000px;margin:0 auto;padding:20px;}
.logo{text-align:center;font-size:36px;color:#00eaff;font-weight:700;margin-top:15px;font-family:'Orbitron',sans-serif;}
.hero-text{text-align:center;margin:10px 0 30px;font-size:16px;color:#00fff0;}
.slider{position:relative;width:100%;overflow:hidden;border-radius:15px;margin-bottom:30px;}
.slide{width:100%;display:none;}
.slide img{width:100%;border-radius:15px;}

/* Section styling */
section{margin-bottom:30px;}
section h2{color:#00eaff;margin-bottom:10px;font-family:'Orbitron',sans-serif;}
section p{color:#a7f5ff;font-size:14px;}

/* Cards */
.cards{display:flex;flex-direction:column;gap:10px;}
.card{background:rgba(0,0,0,0.3);padding:15px;border-radius:10px;box-shadow:0 0 15px #00eaff;}
.card img{width:100%;border-radius:10px;margin-top:10px;}

/* Forms */
form{display:flex;flex-direction:column;gap:10px;margin-top:10px;}
input,select,button{padding:10px;border-radius:10px;border:none;font-size:15px;}
input,select{background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{background:rgba(255,255,255,0.2);outline:none;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00fff0;}

/* Bottom Icons */
.icon-menu{position:fixed;bottom:0;left:0;width:100%;display:flex;justify-content:space-around;background:rgba(0,0,0,0.6);padding:10px 0;border-top:1px solid #00eaff;z-index:9999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;}
.icon-item i{font-size:28px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:12px;margin-top:3px;color:#00fff0;}

/* WhatsApp */
.whatsapp-btn{position:fixed;bottom:70px;right:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}
</style>
</head>
<body>

<div class="container">
  <h1 class="logo">Astore Tourist Hub</h1>
  <div class="hero-text">Welcome to Gilgit-Baltistan! Explore mountains, rivers & culture | Created by CrazyKhanTV</div>

  <!-- Slider -->
  <div class="slider">
    <div class="slide"><img src="https://picsum.photos/id/1015/600/300" alt="Mountain View"></div>
    <div class="slide"><img src="https://picsum.photos/id/1016/600/300" alt="Lake View"></div>
    <div class="slide"><img src="https://picsum.photos/id/1021/600/300" alt="River View"></div>
  </div>

  <!-- About -->
  <section id="about">
    <h2>About Astore Tourist Hub</h2>
    <p>We provide guided tours, cozy rooms, and convenient car rentals in Astore. Enjoy adventure packages, family-friendly stays, and local expertise. Discover mountains, rivers, and culture with premium services at affordable rates.</p>
    <img src="https://picsum.photos/id/1022/600/300" alt="Nature">
  </section>

  <!-- Rooms -->
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

  <!-- Cars -->
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

  <!-- Packages -->
  <section id="packages">
    <h2>Adventure Packages</h2>
    <div class="cards">
      <div class="card"><i class="fa-solid fa-mountain" style="color:#00fff0;font-size:22px;"></i>
        <p><strong>Basic Package:</strong> 2 Nights, 3 Days | Standard Room + Local Guide</p>
        <img src="https://picsum.photos/id/1018/600/300" alt="Basic Package">
      </div>
      <div class="card"><i class="fa-solid fa-car" style="color:#00fff0;font-size:22px;"></i>
        <p><strong>Luxury Package:</strong> 4 Nights, 5 Days | Luxury Room + Car + Guide</p>
        <img src="https://picsum.photos/id/1020/600/300" alt="Luxury Package">
      </div>
      <div class="card"><i class="fa-solid fa-person-hiking" style="color:#00fff0;font-size:22px;"></i>
        <p><strong>Adventure Package:</strong> 5 Nights, 6 Days | Family Suite + Jeep Tour + Hiking</p>
        <img src="https://picsum.photos/id/1023/600/300" alt="Adventure Package">
      </div>
    </div>
  </section>

  <!-- Map -->
  <section id="map">
    <h2>Find Us</h2>
    <iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="250" style="border:0;border-radius:15px;"></iframe>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00fff0;">mohammadasimkhan2746@gmail.com</a></p>
    <p>WhatsApp: <a href="https://wa.me/923171588489" style="color:#00fff0;">0317-1588489</a></p>
    <p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank" style="color:#00fff0;">Visit Page</a></p>
  </section>

  <!-- Booking History -->
  <section id="history">
    <h2>Booking History</h2>
    <div id="historyList"></div>
  </section>
</div>

<!-- Slider JS -->
<script>
let slideIndex = 0;
function showSlides(){
  let slides = document.getElementsByClassName("slide");
  for(let i=0;i<slides.length;i++) slides[i].style.display="none";
  slideIndex++;
  if(slideIndex>slides.length) slideIndex=1;
  slides[slideIndex-1].style.display="block";
  setTimeout(showSlides,4000);
}
showSlides();

// Room Booking
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Room",name:document.getElementById("rname").value,phone:document.getElementById("rphone").value,checkin:document.getElementById("rcheckin").value,checkout:document.getElementById("rcheckout").value,room:document.getElementById("rtype").value};
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(`Room Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nCheck-in: ${booking.checkin}\nCheck-out: ${booking.checkout}\nRoom: ${booking.room}`)}`,"_blank");
  addHistory(booking);
  this.reset();
});

// Car Booking
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const booking={type:"Car",name:document.getElementById("cname").value,phone:document.getElementById("cphone").value,date:document.getElementById("cdate").value,car:document.getElementById("ctype").value};
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent(`Car Booking:\nName: ${booking.name}\nPhone: ${booking.phone}\nPickup Date: ${booking.date}\nCar: ${booking.car}`)}`,"_blank");
  addHistory(booking);
  this.reset();
});

// Booking history
function addHistory(b){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  history.push(b);
  localStorage.setItem("tourHistory",JSON.stringify(history));
  loadHistory();
}
function loadHistory(){
  let history=JSON.parse(localStorage.getItem("tourHistory"))||[];
  const list=document.getElementById("historyList");
  list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");
    div.style.border="1px solid #00eaff"; div.style.padding="8px"; div.style.margin="5px"; div.style.borderRadius="8px";
    div.innerHTML = b.type==="Room"?`Room: ${b.room}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}`:`Car: ${b.car}<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}`;
    list.appendChild(div);
  });
}
loadHistory();

// Scroll to section
function scrollToSection(id){document.getElementById(id).scrollIntoView({behavior:'smooth'});}
</script>

<!-- Bottom Icons -->
<div class="icon-menu">
  <div class="icon-item"><i class="fa-solid fa-bed" onclick="scrollToSection('room')"></i><span>Room</span></div>
  <div class="icon-item"><i class="fa-solid fa-car" onclick="scrollToSection('car')"></i><span>Car</span></div>
  <div class="icon-item"><i class="fa-solid fa-mountain" onclick="scrollToSection('packages')"></i><span>Packages</span></div>
  <div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="scrollToSection('map')"></i><span>Map</span></div>
  <div class="icon-item"><i class="fa-solid fa-envelope" onclick="scrollToSection('contact')"></i><span>Contact</span></div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>
</body>
</html>
