<ASTORE>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<!-- Icons -->
<script src="https://kit.fontawesome.com/a2d041e5c5.js" crossorigin="anonymous"></script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #000;
  overflow-x: hidden;
  color: #fff;
}

/* Neon Animated BG */
@keyframes neonBg {
  0% { background: linear-gradient(135deg,#000428,#004e92); }
  50% { background: linear-gradient(135deg,#020111,#001f3f); }
  100% { background: linear-gradient(135deg,#000428,#004e92); }
}
body {
  animation: neonBg 10s infinite alternate;
}

/* HEADER */
header {
  text-align: center;
  padding: 25px;
  font-size: 28px;
  color: cyan;
  text-shadow: 0 0 15px cyan;
  font-weight: bold;
}

/* DASHBOARD TEXT */
#dashboard {
  padding: 20px;
  text-align: center;
}

/* DETAILS BOX */
.detail-box {
  background: rgba(0,0,0,0.4);
  padding: 20px;
  margin: 10px;
  border-radius: 15px;
  box-shadow: 0 0 15px cyan;
  font-size: 16px;
  line-height: 1.5;
}

/* FORMS */
form {
  background: rgba(255,255,255,0.05);
  padding: 15px;
  margin: 10px;
  border-radius: 12px;
  box-shadow: 0 0 10px cyan;
}
input, select {
  width: 95%;
  padding: 10px;
  margin: 6px 0;
  border-radius: 10px;
  border: none;
}
button {
  background: cyan;
  border: none;
  padding: 12px;
  border-radius: 10px;
  width: 100%;
  margin-top: 10px;
  cursor: pointer;
  font-weight: bold;
}

/* FIXED BOTTOM MENU */
.icon-menu {
  position: fixed;
  bottom: 0;
  width: 100%;
  background: rgba(0,0,0,0.5);
  backdrop-filter: blur(5px);
  display: flex;
  justify-content: space-around;
  padding: 10px 0;
  border-top: 2px solid cyan;
  box-shadow: 0 -2px 15px cyan;
}
.icon-menu div {
  text-align: center;
  color: cyan;
  font-size: 12px;
}
.icon-menu i {
  font-size: 22px;
  display: block;
  margin-bottom: 3px;
}

/* HIDE ALL PAGES */
.page { display: none; }
</style>
</head>

<body>

<header>Astore Tourist Information Hub</header>

<!-- DASHBOARD PAGE -->
<div id="pageDashboard" class="page" style="display:block;">
  <div class="detail-box">
    <h2 style="color:cyan;">Welcome to Astore Valley ❄️</h2>
    <p>
      Astore Pakistan ka ek sab se khubsurat tourist paradise hai —  
      yahan ki mountains, greenery, fresh air aur lakes har visitor ko ek  
      unforgettable experience deti hain.  
      <br><br>
      Hamari service aap ko provide karti hai:
    </p>
    <ul style="text-align:left;">
      <li>🏨 Room Booking (Hotels, Guest Houses, Camps)</li>
      <li>🚗 Car Booking (Jeep, Prado, GLi, Hiace)</li>
      <li>📍 Astore Tourist Guide Assistance</li>
      <li>📞 24/7 Contact & Support</li>
    </ul>
  </div>

  <div class="detail-box">
    <h3 style="color:cyan;">Contact & Social Links</h3>

    <p><b>Owner:</b> Asim KhanZai</p>

    <p><b>Phone:</b> <a href="https://wa.me/03171588489" style="color:cyan;">0317-1588489</a></p>

    <p><b>Email:</b>  
       <a href="mailto:mohammadasimkhan2746@gmail.com" style="color:cyan;">
       mohammadasimkhan2746@gmail.com</a>
    </p>

    <p><b>Facebook:</b>  
    <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" style="color:cyan;">
      Visit Page
    </a></p>

    <p><b>Location:</b><br>
      <a href="https://maps.app.goo.gl/D7fEwdZ9wJf1T8y57" style="color:cyan;">
        Asim KhanZai Social Worker, Near DC House, Eidgah, Astore  
      </a>
    </p>
  </div>
</div>

<!-- ROOM BOOKING -->
<div id="pageRoom" class="page">
  <form onsubmit="sendRoom(event)">
    <h3 style="text-align:center;color:cyan;">Room Booking</h3>
    <input id="rname" placeholder="Your Name" required>
    <input id="rphone" placeholder="Phone Number" required>
    <label style="color:cyan;">Check-in:</label>
    <input type="date" id="rcheckin" required>
    <label style="color:cyan;">Check-out:</label>
    <input type="date" id="rcheckout" required>
    <select id="rroom">
      <option value="Standard Room">Standard Room</option>
      <option value="Luxury Room">Luxury Room</option>
      <option value="Family Room">Family Room</option>
    </select>
    <button>Book on WhatsApp</button>
  </form>
</div>

<!-- CAR BOOKING -->
<div id="pageCar" class="page">
  <form onsubmit="sendCar(event)">
    <h3 style="text-align:center;color:cyan;">Car Booking</h3>
    <input id="cname" placeholder="Your Name" required>
    <input id="cphone" placeholder="Phone Number" required>
    <label style="color:cyan;">Pickup Date:</label>
    <input type="date" id="cdate" required>
    <select id="ccar">
      <option>Jeep</option>
      <option>Prado</option>
      <option>GLI</option>
      <option>Hiace</option>
    </select>
    <button>Book on WhatsApp</button>
  </form>
</div>

<!-- HISTORY -->
<div id="pageHistory" class="page">
  <div class="detail-box">
    <h3 style="color:cyan;">Booking History</h3>
    <div id="historyList"></div>
  </div>
</div>

<!-- FIXED ICON MENU -->
<div class="icon-menu">
  <div onclick="openPage('Dashboard')">
    <i class="fa-solid fa-house"></i> Home
  </div>
  <div onclick="openPage('Room')">
    <i class="fa-solid fa-bed"></i> Room
  </div>
  <div onclick="openPage('Car')">
    <i class="fa-solid fa-car"></i> Car
  </div>
  <div onclick="openPage('History')">
    <i class="fa-solid fa-clock-rotate-left"></i> History
  </div>
</div>

<script>
function openPage(name){
  document.querySelectorAll('.page').forEach(p=>p.style.display="none");
  document.querySelector('#page'+name).style.display="block";
}

/* ROOM BOOKING */
function sendRoom(e){
  e.preventDefault();
  let name = rname.value;
  let phone = rphone.value;
  let ci = rcheckin.value;
  let co = rcheckout.value;
  let room = rroom.value;

  let msg = `Room Booking:%0AName: ${name}%0APhone: ${phone}%0ACheck-in: ${ci}%0ACheck-out: ${co}%0ARoom: ${room}`;

  window.open("https://wa.me/03171588489?text=" + msg, "_blank");

  saveHistory(`Room → ${name} | ${room} | ${ci} to ${co}`);
}

/* CAR BOOKING */
function sendCar(e){
  e.preventDefault();
  let name = cname.value;
  let phone = cphone.value;
  let date = cdate.value;
  let car = ccar.value;

  let msg = `Car Booking:%0AName: ${name}%0APhone: ${phone}%0APickup: ${date}%0ACar: ${car}`;

  window.open("https://wa.me/03171588489?text=" + msg, "_blank");

  saveHistory(`Car → ${name} | ${car} | ${date}`);
}

/* SAVE HISTORY */
function saveHistory(item){
  let h = JSON.parse(localStorage.getItem("history") || "[]");
  h.push(item);
  localStorage.setItem("history", JSON.stringify(h));
  loadHistory();
}

/* LOAD HISTORY */
function loadHistory(){
  let list = document.getElementById("historyList");
  list.innerHTML = "";
  let h = JSON.parse(localStorage.getItem("history") || "[]");
  h.forEach(x=>{
    let div = document.createElement("div");
    div.style.margin="10px 0";
    div.style.padding="10px";
    div.style.border="1px solid cyan";
    div.style.borderRadius="10px";
    div.innerHTML = x;
    list.appendChild(div);
  });
}
loadHistory();
</script>

</body>
</html>
