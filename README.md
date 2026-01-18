<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;background:#000;overflow-x:hidden;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000000,#0f0f0f,#001f3f,#000000);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
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
.logo{text-align:center;font-size:36px;font-weight:700;color:#00eaff;text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;margin:15px 0;font-family:'Orbitron',sans-serif;}
.hero-text{text-align:center;margin-bottom:20px;font-size:16px;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.container{max-width:1000px;margin:0 auto;padding:15px;}
.dashboard-section{display:none;margin-bottom:60px;}
input,select,button{width:100%;padding:10px;margin:6px 0;border-radius:8px;border:none;font-size:14px;}
button{background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;box-shadow:0 0 10px #00eaff;}
button:hover{background:#00bcd4;box-shadow:0 0 20px #00ffff;}
.package{background:rgba(0,0,0,0.4);padding:15px;margin:10px 0;border-radius:12px;box-shadow:0 0 15px #00eaff;}
.package h3{color:#00ffff;}
.package p{color:#a7f5ff;font-size:13px;}
.package i{font-size:28px;color:#00eaff;margin-bottom:8px;display:block;}
.map-container iframe{width:100%;height:250px;border-radius:10px;border:0;}
.contact p{font-size:14px;margin:5px 0;color:#00eaff;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:0;left:0;width:100%;background:rgba(0,0,0,0.5);padding:8px 0;box-shadow:0 0 10px #00eaff;border-radius:15px 15px 0 0;z-index:999;}
.icon-item{text-align:center;}
.icon-item i{font-size:24px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:11px;margin-top:2px;}
#historyList div{border:1px solid #00eaff;padding:6px;margin:5px;border-radius:6px;font-size:13px;}
.whatsapp-btn{position:fixed;bottom:60px;right:15px;background:#25d366;padding:14px 16px;border-radius:50%;color:#fff;font-size:26px;text-decoration:none;box-shadow:0 0 15px #25d366;z-index:999;}
#logoutBtn{position:fixed;top:10px;right:10px;width:40px;height:40px;font-size:18px;padding:0;background:#ff4444;border:none;border-radius:50%;color:#fff;box-shadow:0 0 12px #ff6666;cursor:pointer;display:flex;align-items:center;justify-content:center;z-index:999;}
#logoutBtn:hover{transform:scale(1.1);}
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
  p.style.animationDuration=(6+Math.random()*6)+"s";
  p.style.opacity=Math.random()*0.7+0.3;
  document.body.appendChild(p);
}
</script>

<div class="container">
<h1 class="logo">Astore Tourist Hub</h1>
<div class="hero-text">Explore the beauty of Astore! Book rooms, cars, and packages easily. Contact via WhatsApp or email anytime.</div>

<!-- Room Booking -->
<div id="room" class="dashboard-section" style="display:block;">
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
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Room via WhatsApp</button>
</form>
</div>

<!-- Car Booking -->
<div id="car" class="dashboard-section">
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
<button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Car via WhatsApp</button>
</form>
</div>

<!-- Packages -->
<div id="packages" class="dashboard-section">
<div class="package"><i class="fa-solid fa-mountain"></i><h3>Adventure Package</h3><p>3 Nights, 4 Days<br>Luxury Room + Jeep Tour + Hiking</p></div>
<div class="package"><i class="fa-solid fa-person-hiking"></i><h3>Explorer Package</h3><p>2 Nights, 3 Days<br>Standard Room + Local Guide</p></div>
<div class="package"><i class="fa-solid fa-car"></i><h3>Family Package</h3><p>4 Nights, 5 Days<br>Family Suite + Car + Tour</p></div>
</div>

<!-- Map -->
<div id="map" class="dashboard-section map-container">
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" allowfullscreen="" loading="lazy"></iframe>
</div>

<!-- Contact -->
<div id="contact" class="dashboard-section contact">
<p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:#00ffcc;">mohammadasimkhan2746@gmail.com</a></p>
<p>Owner: Asim Khanzai | WhatsApp: <a href="https://wa.me/923171588489" style="color:#00ffcc;">03171588489</a></p>
<p>Follow on Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" style="color:#00ffcc;">Click Here</a></p>
</div>

<!-- Booking History -->
<div id="historySection" class="dashboard-section">
<h3>Booking History</h3>
<div id="historyList"></div>
</div>

<!-- Navigation Icons -->
<div class="icon-menu">
<div class="icon-item"><i class="fa-solid fa-bed" onclick="showSection('room')"></i><span>Room</span></div>
<div class="icon-item"><i class="fa-solid fa-car" onclick="showSection('car')"></i><span>Car</span></div>
<div class="icon-item"><i class="fa-solid fa-mountain" onclick="showSection('packages')"></i><span>Packages</span></div>
<div class="icon-item"><i class="fa-solid fa-map-location-dot" onclick="showSection('map')"></i><span>Map</span></div>
<div class="icon-item"><i class="fa-solid fa-envelope" onclick="showSection('contact')"></i><span>Contact</span></div>
</div>

<!-- WhatsApp -->
<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Show sections
function showSection(section){
  document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");
  document.getElementById(section).style.display="block";
}

// Booking storage
function saveBooking(type,data){
  let history=JSON.parse(localStorage.getItem("history"))||[];
  history.push({type,...data});
  localStorage.setItem("history",JSON.stringify(history));
  renderHistory();
}

// Render history
function renderHistory(){
  let history=JSON.parse(localStorage.getItem("history"))||[];
  const list=document.getElementById("historyList");
  list.innerHTML="";
  history.forEach(b=>{
    const div=document.createElement("div");
    if(b.type==="Room"){
      div.innerHTML=`Room Booking:<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Check-in: ${b.checkin}<br>Check-out: ${b.checkout}<br>Room: ${b.room}`;
    } else {
      div.innerHTML=`Car Booking:<br>Name: ${b.name}<br>Phone: ${b.phone}<br>Date: ${b.date}<br>Car: ${b.car}`;
    }
    list.appendChild(div);
  });
}

// Room form
document.getElementById("roomForm").addEventListener("submit",e=>{
  e.preventDefault();
  const data={
    name:document.getElementById("rname").value,
    phone:document.getElementById("rphone").value,
    checkin:document.getElementById("rcheckin").value,
    checkout:document.getElementById("rcheckout").value,
    room:document.getElementById("rtype").value
  };
  saveBooking("Room",data);
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent("Room Booking:\nName: "+data.name+"\nPhone: "+data.phone+"\nCheck-in: "+data.checkin+"\nCheck-out: "+data.checkout+"\nRoom: "+data.room)}`, "_blank");
  e.target.reset();
});

// Car form
document.getElementById("carForm").addEventListener("submit",e=>{
  e.preventDefault();
  const data={
    name:document.getElementById("cname").value,
    phone:document.getElementById("cphone").value,
    date:document.getElementById("cdate").value,
    car:document.getElementById("ctype").value
  };
  saveBooking("Car",data);
  window.open(`https://wa.me/923171588489?text=${encodeURIComponent("Car Booking:\nName: "+data.name+"\nPhone: "+data.phone+"\nDate: "+data.date+"\nCar: "+data.car)}`, "_blank");
  e.target.reset();
});

// Initial render
renderHistory();
</script>
</body>
</html>
