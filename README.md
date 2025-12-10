<ASTORE TOURIST HUB>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
<style>
/* Basic reset & fonts */
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;transition:0.5s;}
a{text-decoration:none;color:inherit;}
/* Neon animated background */
body{background:#000;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#000000,#001f3f,#000000,#0f0f0f);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-3;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}

/* Floating particles */
.particle{position:fixed;width:6px;height:6px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}

/* Containers */
.container{max-width:700px;margin:40px auto;background:rgba(0,0,0,0.4);padding:25px;border-radius:20px;backdrop-filter:blur(10px);box-shadow:0 0 25px #00eaff;text-align:center;}
h2,h3{color:#00eaff;font-family:'Orbitron',sans-serif;margin-bottom:15px;text-shadow:0 0 15px #00eaff,0 0 30px #00ffff;}

/* Inputs & buttons */
input,select{width:100%;padding:10px;margin:8px 0;border-radius:10px;border:none;background:rgba(255,255,255,0.1);color:#fff;}
input:focus,select:focus{outline:none;background:rgba(255,255,255,0.25);}
button{padding:10px 16px;margin-top:10px;border:none;border-radius:10px;background:#00eaff;color:#000;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:#00bcd4;box-shadow:0 0 20px #00ffff;}

/* Logout */
#logoutBtn{background:#ff4d6d;color:#fff;}

/* Booking history */
.booking-history{margin-top:20px;text-align:left;background:rgba(0,0,0,0.3);padding:15px;border-radius:15px;max-height:200px;overflow-y:auto;}
.booking-history h4{margin-bottom:10px;text-shadow:0 0 10px #00eaff;}
.booking-history p{margin:5px 0;color:#a7f5ff;}
.icon{margin-right:8px;color:#00eaff;}

/* WhatsApp button */
.whatsapp-btn{position:fixed;right:20px;bottom:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 20px #25d366;transition:0.3s;}
.whatsapp-btn:hover{transform:scale(1.1);}

/* Map container */
.map-container{margin-top:25px;border-radius:15px;overflow:hidden;box-shadow:0 0 25px #00eaff;}
</style>
</head>
<body>
<div class="bg-animate"></div>
<script>
// Floating particles
for(let i=0;i<60;i++){
    let p=document.createElement("div");
    p.className="particle";
    p.style.left=Math.random()*100+"vw";
    p.style.animationDuration=(8+Math.random()*7)+"s";
    p.style.opacity=Math.random()*0.7+0.3;
    document.body.appendChild(p);
}
</script>

<div class="container" id="authContainer">
<h2>Astore Tourist Hub <i class="fa-solid fa-location-dot icon"></i></h2>

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

<div class="container" id="dashboard" style="display:none;">
<h2>Welcome, <span id="userDisplay"></span>! <i class="fa-solid fa-user icon"></i></h2>
<button id="logoutBtn" onclick="logout()">Logout <i class="fa-solid fa-right-from-bracket icon"></i></button>

<h3>Book a Room <i class="fa-solid fa-bed icon"></i></h3>
<input type="text" id="roomName" placeholder="Room Type">
<button onclick="bookRoom()">Book Room</button>

<h3>Book a Car <i class="fa-solid fa-car icon"></i></h3>
<input type="text" id="carType" placeholder="Car Type">
<button onclick="bookCar()">Book Car</button>

<div class="booking-history">
<h4>Booking History <i class="fa-solid fa-history icon"></i></h4>
<div id="historyList"></div>
</div>

<div class="map-container">
<iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>

<div style="margin-top:15px;text-align:center;">
<a href="https://wa.me/03171588489" target="_blank" class="whatsapp-btn"><i class="fa-brands fa-whatsapp"></i></a>
</div>
</div>

<script>
// Signup/Login system using localStorage
function signup(){
    const username = document.getElementById("signupUsername").value.trim();
    const password = document.getElementById("signupPassword").value.trim();
    if(!username || !password){alert("Fill all fields."); return;}
    let users = JSON.parse(localStorage.getItem("users")) || {};
    if(users[username]){alert("Username exists!"); return;}
    users[username] = {password, history: []};
    localStorage.setItem("users", JSON.stringify(users));
    alert("Signup successful! Please login.");
    showLogin();
}

function login(){
    const username = document.getElementById("loginUsername").value.trim();
    const password = document.getElementById("loginPassword").value.trim();
    let users = JSON.parse(localStorage.getItem("users")) || {};
    if(users[username] && users[username].password===password){
        localStorage.setItem("loggedInUser", username);
        showDashboard();
    } else{ alert("Invalid credentials!"); }
}

function logout(){ localStorage.removeItem("loggedInUser"); showLogin(); }

function showDashboard(){
    const username = localStorage.getItem("loggedInUser");
    if(!username) return showLogin();
    document.getElementById("userDisplay").textContent = username;
    document.getElementById("authContainer").style.display="none";
    document.getElementById("dashboard").style.display="block";
    displayHistory();
}

function showLogin(){ document.getElementById("signupDiv").style.display="none"; document.getElementById("loginDiv").style.display="block"; document.getElementById("dashboard").style.display="none";}
function showSignup(){ document.getElementById("signupDiv").style.display="block"; document.getElementById("loginDiv").style.display="none"; document.getElementById("dashboard").style.display="none";}

// Booking system
function bookRoom(){
    const room = document.getElementById("roomName").value.trim();
    if(!room){ alert("Enter room type"); return; }
    addHistory(`Room booked: ${room}`);
    document.getElementById("roomName").value="";
}
function bookCar(){
    const car = document.getElementById("carType").value.trim();
    if(!car){ alert("Enter car type"); return; }
    addHistory(`Car booked: ${car}`);
    document.getElementById("carType").value="";
}

function addHistory(action){
    const username = localStorage.getItem("loggedInUser");
    let users = JSON.parse(localStorage.getItem("users")) || {};
    if(!users[username]) return;
    const timestamp = new Date().toLocaleString();
    users[username].history.push(`${timestamp} - ${action}`);
    localStorage.setItem("users", JSON.stringify(users));
    displayHistory();
}

function displayHistory(){
    const username = localStorage.getItem("loggedInUser");
    const historyDiv = document.getElementById("historyList");
    historyDiv.innerHTML="";
    let users = JSON.parse(localStorage.getItem("users")) || {};
    if(users[username] && users[username].history.length>0){
        users[username].history.slice().reverse().forEach(item=>{
            let p = document.createElement("p"); p.textContent = item; historyDiv.appendChild(p);
        });
    } else{ historyDiv.innerHTML="<p>No bookings yet.</p>"; }
}

// Auto-login check
if(localStorage.getItem("loggedInUser")) showDashboard();
else showLogin();
</script>
</body>
</html>
