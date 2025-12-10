<Astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth;}
body{font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;transition:0.5s;}
:root{--bg-gradient:linear-gradient(270deg,#000000,#0f0f0f,#001f3f,#000000);--text-color:#00eaff;--card-bg:rgba(0,0,0,0.4);--card-shadow:0 0 25px #00eaff;--button-bg:#00eaff;}
body.light-mode{--bg-gradient:linear-gradient(270deg,#e0f7fa,#80deea,#4dd0e1,#e0f7fa);--text-color:#004e92;--card-bg:rgba(255,255,255,0.85);--card-shadow:0 0 20px #004e92;--button-bg:#004e92;}
.bg-animate{position:fixed;width:100%;height:100%;background:var(--bg-gradient);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
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
.container{max-width:1100px;margin:60px auto;background:var(--card-bg);padding:30px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:var(--card-shadow);transition:0.5s;}
.logo{text-align:center;font-size:46px;font-weight:700;color:var(--text-color);text-shadow:0 0 15px var(--text-color),0 0 30px #00ffff;margin-bottom:20px;font-family:'Orbitron',sans-serif;animation:glowPulse 2s infinite alternate;}
@keyframes glowPulse{0%{text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;}100%{text-shadow:0 0 30px #00eaff,0 0 60px #00ffff;}}
.hero-text{text-align:center;margin-bottom:30px;font-size:18px;font-weight:500;background:linear-gradient(90deg,#00eaff,#00ff99,#ff00ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;opacity:0;transform:translateY(30px);transition:1s;}
.hero-text.show{opacity:1;transform:translateY(0);}
label{margin-top:12px;display:block;font-weight:500;}
input,select{width:100%;padding:12px;margin-top:6px;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;font-size:15px;transition:0.3s;}
input:focus,select:focus{background:rgba(255,255,255,0.25);outline:none;}
button{width:100%;padding:14px;margin-top:18px;border:none;border-radius:10px;background:var(--button-bg);color:#000;font-size:18px;font-weight:600;cursor:pointer;transition:0.3s, box-shadow 0.5s;animation:btnPulse 2s infinite alternate;}
button:hover{background:#00bcd4;box-shadow:0 0 25px #00ffff;}
@keyframes btnPulse{0%{box-shadow:0 0 15px #00eaff;}100%{box-shadow:0 0 30px #00ffff;}}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;margin-top:20px;}
.package{background:var(--card-bg);padding:20px;border-radius:15px;box-shadow:var(--card-shadow);text-align:center;transition:0.3s, transform 0.5s;opacity:0;transform:translateY(30px);}
.package.show{opacity:1;transform:translateY(0);}
.package:hover{transform:scale(1.05);box-shadow:0 0 40px #00ffff;animation:packagePulse 1.5s infinite alternate;}
.package h3{text-shadow:0 0 15px #00eaff;font-family:'Orbitron',sans-serif;}
.package p{font-size:14px;color:#a7f5ff;}
.package i{font-size:36px;color:#00eaff;margin-bottom:10px;display:block;animation:iconPulse 2s infinite alternate;}
@keyframes packagePulse{0%{box-shadow:0 0 30px #00eaff;}100%{box-shadow:0 0 50px #00ffff;}}
@keyframes iconPulse{0%{text-shadow:0 0 10px #00eaff,0 0 20px #00ffff;}100%{text-shadow:0 0 20px #00eaff,0 0 40px #00ffff;}}
.map-container{margin-top:30px;border-radius:15px;overflow:hidden;box-shadow:var(--card-shadow);transition:0.5s;opacity:0;transform:translateY(30px);}
.map-container.show{opacity:1;transform:translateY(0);}
.contact{margin-top:30px;text-align:center;font-size:16px;opacity:0;transform:translateY(30px);transition:1s;}
.contact.show{opacity:1;transform:translateY(0);}
.contact i{margin-right:8px;color:var(--text-color);}
.social-share{margin-top:20px;text-align:center;opacity:0;transform:translateY(30px);transition:1s;}
.social-share.show{opacity:1;transform:translateY(0);}
.social-share a{margin:0 10px;font-size:28px;color:var(--text-color);text-decoration:none;transition:0.3s;}
.social-share a:hover{color:#00fff0;transform:scale(1.3);}
.whatsapp-btn{position:fixed;right:20px;bottom:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s, box-shadow 0.5s;animation:whatsappPulse 2s infinite alternate;}
.whatsapp-btn:hover{transform:scale(1.1);}
@keyframes whatsappPulse{0%{box-shadow:0 0 15px #25d366;}100%{box-shadow:0 0 30px #00ff99;}}
.mode-toggle{position:fixed;top:20px;right:20px;padding:10px 14px;background:#00eaff;color:#000;border:none;border-radius:10px;cursor:pointer;z-index:999;transition:0.3s;}
.mode-toggle:hover{background:#00bcd4;}
#authContainer,#dashboard{max-width:700px;margin:40px auto;background:var(--card-bg);padding:25px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:var(--card-shadow);text-align:center;}
</style>
</head>
<body>
<div class="bg-animate"></div>
<div class="stripes">
  <div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div><div class="stripe"></div>
</div>
<button class="mode-toggle" onclick="toggleMode()">Toggle Dark/Light</button>
<script>
for(let i=0;i<60;i++){let p=document.createElement("div");p.className="particle";p.style.left=Math.random()*100+"vw";p.style.animationDuration=(8+Math.random()*7)+"s";p.style.opacity=Math.random()*0.7+0.3;document.body.appendChild(p);}
</script>

<div id="authContainer">
<h2 class="logo">Astore Tourist Hub</h2>
<div class="hero-text show">Owner: Asim Khanzai | WhatsApp: 03171588489 | Email: mohammadasimkhan2746@gmail.com</div>

<div id="signupDiv">
<h3>Signup <i class="fa-solid fa-user-plus icon"></i></h3>
<input type="text" id="signupUsername" placeholder="Username" required>
<input type="password" id="signupPassword" placeholder="Password" required>
<button onclick="signup()">Signup</button>
<p class="message">Already have an account? <a href="#" onclick="showLogin()">Login</a></p>
</div>

<div id="loginDiv" style="display:none;">
<h3>Login <i class="fa-solid fa-right-to-bracket icon"></i></h3>
<input type="text" id="loginUsername" placeholder="Username" required>
<input type="password" id="loginPassword" placeholder="Password" required>
<button onclick="login()">Login</button>
<p class="message">Don't have an account? <a href="#" onclick="showSignup()">Signup</a></p>
</div>
</div>

<div id="dashboard" style="display:none;">
<h2>Welcome, <span id="userDisplay"></span>! <i class="fa-solid fa-user icon"></i></h2>
<button id="logoutBtn" onclick="logout()">Logout <i class="fa-solid fa-right-from-bracket icon"></i></button>

<h2 style="text-shadow:0 0 12px #00eaff;">Room Booking</h2>
<form id="roomForm">
<label><i class="fa-solid fa-bed"></i> Room Type</label>
<select id="rtype" required>
<option>Standard Room</option>
<option>Luxury Room</option>
<option>Family Suite</option>
</select>
<button type="submit">Book Room</button>
</form>

<h2 style="text-shadow:0 0 12px #00eaff;">Car Booking</h2>
<form id="carForm">
<label><i class="fa-solid fa-car"></i> Car Type</label>
<select id="ctype" required>
<option>Corolla</option>
<option>Hiace</option>
<option>Prado</option>
<option>Astore Local Jeep</option>
</select>
<button type="submit">Book Car</button>
</form>

<div class="booking-history">
<h4>Booking History <i class="fa-solid fa-history icon"></i></h4>
<div id="historyList"></div>
</div>

<div class="map-container">
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<div class="contact"><p><i class="fa-solid fa-envelope"></i> Email: mohammadasimkhan2746@gmail.com</p></div>
<div class="social-share">
<a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
<a href="https://www.facebook.com/sharer/sharer.php?u=https://yourwebsite.com" target="_blank"><i class="fa-brands fa-facebook"></i></a>
<a href="https://twitter.com/intent/tweet?url=https://yourwebsite.com&text=Astore+Tourist+Information+Hub" target="_blank"><i class="fa-brands fa-twitter"></i></a>
</div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Toggle dark/light
function toggleMode(){document.body.classList.toggle("light-mode");}

// localStorage login/signup
function signup(){
  const u=document.getElementById("signupUsername").value.trim();
  const p=document.getElementById("signupPassword").value.trim();
  if(!u||!p){alert("Fill all fields."); return;}
  let users=JSON.parse(localStorage.getItem("users"))||{};
  if(users[u]){alert("Username exists!");return;}
  users[u]={password:p,history:[]};
  localStorage.setItem("users",JSON.stringify(users));
  alert("Signup successful! Login now.");showLogin();
}
function login(){
  const u=document.getElementById("loginUsername").value.trim();
  const p=document.getElementById("loginPassword").value.trim();
  let users=JSON.parse(localStorage.getItem("users"))||{};
  if(users[u]&&users[u].password===p){localStorage.setItem("loggedInUser",u);showDashboard();}
  else{alert("Invalid credentials!");}
}
function logout(){localStorage.removeItem("loggedInUser");showLogin();}
function showDashboard(){
  const u=localStorage.getItem("loggedInUser");
  if(!u)return showLogin();
  document.getElementById("userDisplay").textContent=u;
  document.getElementById("authContainer").style.display="none";
  document.getElementById("dashboard").style.display="block";
  displayHistory();
}
function showLogin(){document.getElementById("signupDiv").style.display="none";document.getElementById("loginDiv").style.display="block";document.getElementById("dashboard").style.display="none";}
function showSignup(){document.getElementById("signupDiv").style.display="block";document.getElementById("loginDiv").style.display="none";document.getElementById("dashboard").style.display="none";}

// Booking
document.getElementById("roomForm").addEventListener("submit",function(e){
  e.preventDefault();
  const u=localStorage.getItem("loggedInUser");
  if(!u){alert("Login first!");return;}
  let r=document.getElementById("rtype").value;
  addHistory(`Room booked: ${r}`);
});
document.getElementById("carForm").addEventListener("submit",function(e){
  e.preventDefault();
  const u=localStorage.getItem("loggedInUser");
  if(!u){alert("Login first!");return;}
  let c=document.getElementById("ctype").value;
  addHistory(`Car booked: ${c}`);
});

function addHistory(action){
  const u=localStorage.getItem("loggedInUser");
  let users=JSON.parse(localStorage.getItem("users"))||{};
  if(!users[u])return;
  const t=new Date().toLocaleString();
  users[u].history.push(`${t} - ${action}`);
  localStorage.setItem("users",JSON.stringify(users));
  displayHistory();
}
function displayHistory(){
  const u=localStorage.getItem("loggedInUser");
  const h=document.getElementById("historyList");h.innerHTML="";
  let users=JSON.parse(localStorage.getItem("users"))||{};
  if(users[u]&&users[u].history.length>0){users[u].history.slice().reverse().forEach(i=>{let p=document.createElement("p");p.textContent=i;h.appendChild(p);});}
  else{h.innerHTML="<p>No bookings yet.</p>";}
}
if(localStorage.getItem("loggedInUser")) showDashboard();
else showLogin();
</script>
</body>
</html>
