<ASTORE TOURIST HUB>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{color:#fff;overflow-x:hidden;font-size:14px;transition:0.5s; background:#000;}
:root{--bg-gradient:linear-gradient(270deg,#000,#0f0f0f,#001f3f,#000);--text-color:#00eaff;--card-bg:rgba(0,0,0,0.4);--card-shadow:0 0 20px #00eaff;--button-bg:#00eaff;}
body.light-mode{--bg-gradient:linear-gradient(270deg,#e0f7fa,#80deea,#4dd0e1,#e0f7fa);--text-color:#004e92;--card-bg:rgba(255,255,255,0.85);--card-shadow:0 0 15px #004e92;--button-bg:#004e92;}
.bg-animate{position:fixed;width:100%;height:100%;background:var(--bg-gradient);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
.stripes{position:fixed;width:100%;height:100%;z-index:-1;overflow:hidden;}
.stripe{position:absolute;width:2px;height:200%;background:rgba(0,255,255,0.05);top:-50%;animation:moveStripe linear infinite;}
.stripe:nth-child(1){left:10%;animation-duration:18s;}
.stripe:nth-child(2){left:25%;animation-duration:22s;}
.stripe:nth-child(3){left:40%;animation-duration:20s;}
.stripe:nth-child(4){left:60%;animation-duration:25s;}
.stripe:nth-child(5){left:80%;animation-duration:19s;}
@keyframes moveStripe{0%{transform:translateY(0) rotate(20deg);}100%{transform:translateY(100%) rotate(20deg);}}
.particle{position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
.logo{text-align:center;font-size:36px;font-weight:700;color:var(--text-color);text-shadow:0 0 15px var(--text-color),0 0 25px #00ffff;margin-bottom:15px;font-family:'Orbitron',sans-serif;animation:glowPulse 2s infinite alternate;}
@keyframes glowPulse{0%{text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;}100%{text-shadow:0 0 25px #00eaff,0 0 50px #00ffff;}}
.hero-text{text-align:center;margin-bottom:20px;font-size:14px;font-weight:500;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;opacity:0;transform:translateY(20px);transition:1s;}
.hero-text.show{opacity:1;transform:translateY(0);}
input,select{width:100%;padding:10px;margin-top:6px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;font-size:14px;transition:0.3s;}
input:focus,select:focus{background:rgba(255,255,255,0.25);outline:none;}
button{cursor:pointer;transition:0.3s;}
button:hover{transform:scale(1.05);}
.container,#authContainer,#dashboard{max-width:400px;margin:20px auto;background:var(--card-bg);padding:20px;border-radius:15px;backdrop-filter:blur(8px);box-shadow:var(--card-shadow);text-align:center;}
.dashboard-section{display:none;margin-bottom:20px;}
.icon-menu{display:flex;justify-content:space-around;position:fixed;bottom:0;width:100%;background:rgba(0,0,0,0.5);padding:10px 0;box-shadow:0 0 15px #00eaff;border-top:1px solid #00eaff;z-index:999;border-radius:15px 15px 0 0;}
.icon-item{text-align:center;position:relative;}
.icon-item i{font-size:24px;color:#00eaff;cursor:pointer;transition:0.3s;}
.icon-item i:hover{color:#00fff0;transform:scale(1.2);}
.icon-item span{display:block;font-size:10px;margin-top:2px;}
#logoutBtn{position:fixed;bottom:60px;left:50%;transform:translateX(-50%);padding:10px 18px;font-size:16px;background:red;border:none;border-radius:10px;box-shadow:0 0 15px #ff5555;color:#fff;}
.whatsapp-btn{display:block;width:100%;padding:10px 0;margin-top:8px;background:#25d366;border:none;border-radius:10px;color:#fff;font-weight:600;box-shadow:0 0 12px #25d366;}
.whatsapp-btn:hover{background:#1ebe5d;box-shadow:0 0 20px #1efc7d;}
.package{background:rgba(0,255,255,0.1);padding:12px;margin:8px 0;border-radius:12px;box-shadow:0 0 12px #00eaff;}
</style>
</head>
<body>
<div class="bg-animate"></div>
<div class="stripes"><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div></div>
<button class="mode-toggle" onclick="toggleMode()">Toggle</button>
<script>
for(let i=0;i<50;i++){let p=document.createElement("div");p.className="particle";p.style.left=Math.random()*100+"vw";p.style.animationDuration=(6+Math.random()*6)+"s";p.style.opacity=Math.random()*0.7+0.3;document.body.appendChild(p);}
</script>

<div id="authContainer">
<h2 class="logo">Astore Tourist Hub</h2>
<div class="hero-text show">Owner: Asim Khanzai | WhatsApp: 03171588489</div>

<div id="signupDiv">
<h3>Signup <i class="fa-solid fa-user-plus icon"></i></h3>
<input type="text" id="signupUsername" placeholder="Username">
<input type="password" id="signupPassword" placeholder="Password">
<button onclick="signup()">Signup</button>
<p class="message">Already have an account? <a href="#" onclick="showLogin()">Login</a></p>
</div>

<div id="loginDiv" style="display:none;">
<h3>Login <i class="fa-solid fa-right-to-bracket icon"></i></h3>
<input type="text" id="loginUsername" placeholder="Username">
<input type="password" id="loginPassword" placeholder="Password">
<button onclick="login()">Login</button>
<p class="message">Don't have an account? <a href="#" onclick="showSignup()">Signup</a></p>
</div>
</div>

<div id="dashboard" style="display:none;">
<h2>Welcome, <span id="userDisplay"></span>!</h2>

<div id="room" class="dashboard-section">
<h3>Room Booking</h3>
<input type="text" id="rname" placeholder="Name" required>
<input type="text" id="rphone" placeholder="Phone" required>
<input type="date" id="rcheckin" required>
<input type="date" id="rcheckout" required>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button class="whatsapp-btn" onclick="bookRoom()">Book via WhatsApp</button>
</div>

<div id="car" class="dashboard-section">
<h3>Car Booking</h3>
<input type="text" id="cname" placeholder="Name" required>
<input type="text" id="cphone" placeholder="Phone" required>
<input type="date" id="cdate" required>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Local Jeep</option>
</select>
<button class="whatsapp-btn" onclick="bookCar()">Book via WhatsApp</button>
</div>

<div id="packages" class="dashboard-section">
<h3>Packages</h3>
<div class="package"><strong>Basic</strong><br>2 Nights, 3 Days<br>Standard Room + Local Guide<br><button class="whatsapp-btn" onclick="bookPackage('Basic')">Book via WhatsApp</button></div>
<div class="package"><strong>Luxury</strong><br>4 Nights, 5 Days<br>Luxury Room + Car + Guide<br><button class="whatsapp-btn" onclick="bookPackage('Luxury')">Book via WhatsApp</button></div>
<div class="package"><strong>Adventure</strong><br>5 Nights, 6 Days<br>Family Suite + Jeep + Hiking<br><button class="whatsapp-btn" onclick="bookPackage('Adventure')">Book via WhatsApp</button></div>
</div>

<div id="historySection" class="dashboard-section">
<h3>Booking History</h3>
<div id="historyList"></div>
</div>

<div class="icon-menu">
<div class="icon-item" onclick="showSection('room')"><i class="fa-solid fa-bed"></i><span>Room</span></div>
<div class="icon-item" onclick="showSection('car')"><i class="fa-solid fa-car"></i><span>Car</span></div>
<div class="icon-item" onclick="showSection('packages')"><i class="fa-solid fa-mountain"></i><span>Packages</span></div>
<div class="icon-item" onclick="showSection('historySection')"><i class="fa-solid fa-list"></i><span>History</span></div>
</div>

<button id="logoutBtn" onclick="logout()">Logout</button>

<script>
const GROUP_WA = "923171588489";
function toggleMode(){document.body.classList.toggle("light-mode");}
function signup(){const u=document.getElementById("signupUsername").value.trim();const p=document.getElementById("signupPassword").value.trim();if(!u||!p){alert("Fill all");return;}let users=JSON.parse(localStorage.getItem("users"))||{};if(users[u]){alert("Username exists");return;}users[u]={history:[],password:p};localStorage.setItem("users",JSON.stringify(users));alert("Signup success!"); showLogin();}
function login(){const u=document.getElementById("loginUsername").value.trim();const p=document.getElementById("loginPassword").value.trim();let users=JSON.parse(localStorage.getItem("users"))||{};if(users[u] && users[u].password===p){localStorage.setItem("loggedInUser",u); showDashboard();} else{alert("Invalid");}}
function logout(){localStorage.removeItem("loggedInUser"); showLogin();}
function showSignup(){document.getElementById("signupDiv").style.display="block";document.getElementById("loginDiv").style.display="none";document.getElementById("authContainer").style.display="block";document.getElementById("dashboard").style.display="none";}
function showLogin(){document.getElementById("signupDiv").style.display="none";document.getElementById("loginDiv").style.display="block";document.getElementById("authContainer").style.display="block";document.getElementById("dashboard").style.display="none";}
function showDashboard(){const u=localStorage.getItem("loggedInUser");if(!u){showLogin();return;}document.getElementById("authContainer").style.display="none";document.getElementById("dashboard").style.display="block";document.getElementById("userDisplay").textContent=u;showSection('room');loadHistory();}
function showSection(section){document.querySelectorAll(".dashboard-section").forEach(s=>s.style.display="none");document.getElementById(section).style.display="block";}
function saveHistory(entry){const u=localStorage.getItem("loggedInUser");if(!u)return;let users=JSON.parse(localStorage.getItem("users"))||{};users[u].history.push(entry);localStorage.setItem("users",JSON.stringify(users));loadHistory();}
function loadHistory(){const u=localStorage.getItem("loggedInUser");if(!u)return;let users=JSON.parse(localStorage.getItem("users"))||{};const h=document.getElementById("historyList");h.innerHTML="";if(users[u].history.length===0){h.innerHTML="<p>No bookings yet.</p>";return;}users[u].history.slice().reverse().forEach(b=>{const div=document.createElement("div");div.style.background="rgba(0,255,255,0.1)";div.style.padding="8px";div.style.margin="6px 0";div.style.borderRadius="8px";div.innerHTML=`<strong>${b.type} Booking</strong><br>Name: ${b.name}<br>Phone: ${b.phone}<br>${b.details}<br>Date: ${b.date}`;h.appendChild(div);});}

// Booking functions
function bookRoom(){const name=document.getElementById("rname").value, phone=document.getElementById("rphone").value, checkin=document.getElementById("rcheckin").value, checkout=document.getElementById("rcheckout").value, rtype=document.getElementById("rtype").value;if(!name||!phone||!checkin||!checkout)return alert("Fill all");const msg=`Room Booking: ${rtype}, Check-in: ${checkin}, Check-out: ${checkout}. Name: ${name}, Phone: ${phone}`;saveHistory({type:"Room",name,phone,details:`Room: ${rtype}, Check-in: ${checkin}, Check-out: ${checkout}`,date:new Date().toLocaleString()});window.open(`https://wa.me/${GROUP_WA}?text=${encodeURIComponent(msg)}`);}
function bookCar(){const name=document.getElementById("cname").value, phone=document.getElementById("cphone").value, date=document.getElementById("cdate").value, ctype=document.getElementById("ctype").value;if(!name||!phone||!date)return alert("Fill all");const msg=`Car Booking: ${ctype}, Pickup: ${date}. Name: ${name}, Phone: ${phone}`;saveHistory({type:"Car",name,phone,details:`Car: ${ctype}, Pickup: ${date}`,date:new Date().toLocaleString()});window.open(`https://wa.me/${GROUP_WA}?text=${encodeURIComponent(msg)}`);}
function bookPackage(pkg){const u=localStorage.getItem("loggedInUser");if(!u)return;const msg=`Package Booking: ${pkg}. User: ${u}`;saveHistory({type:"Package",name:u,phone:"-",details:`Package: ${pkg}`,date:new Date().toLocaleString()});window.open(`https://wa.me/${GROUP_WA}?text=${encodeURIComponent(msg)}`);}
window.addEventListener("load",()=>{if(localStorage.getItem("loggedInUser")) showDashboard();});
</script>
</body>
</html>
