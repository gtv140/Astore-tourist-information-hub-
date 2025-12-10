<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
body {
  margin: 0;
  font-family: Poppins, sans-serif;
  color: white;
  background: black;
  overflow-x: hidden;
}

/* Neon animated BG */
body::before {
  content:"";
  position: fixed;
  top:0; left:0;
  width:100%; height:100%;
  background: radial-gradient(circle, rgba(0,180,255,0.25), transparent),
              radial-gradient(circle at bottom, rgba(0,80,255,0.2), transparent);
  animation: glow 6s infinite alternate;
  z-index:-1;
}
@keyframes glow {
  from { filter: blur(20px); }
  to { filter: blur(40px); }
}

/* Page container */
.container{
  padding: 20px;
  padding-bottom: 120px;
}

/* Sections */
.section{
  background: rgba(0,0,0,0.35);
  border: 1px solid #00eaff;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 15px;
  box-shadow: 0 0 15px #00eaff;
}

/* Headings */
.section h2{
  color: #00eaff;
  text-shadow: 0 0 10px #00eaff;
  font-size: 22px;
}

/* Inputs */
input, select{
  width: 100%;
  padding: 10px;
  margin-top: 8px;
  border-radius: 10px;
  border: 1px solid #00eaff;
  background: rgba(0,0,0,0.45);
  color: white;
}

button{
  width: 100%;
  margin-top: 12px;
  padding: 12px;
  border: none;
  border-radius: 12px;
  background: #00eaff;
  color: black;
  font-size: 16px;
  font-weight: bold;
  box-shadow: 0 0 10px #00eaff;
}

/* Fixed bottom menu */
.icon-menu{
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: rgba(0,0,0,0.65);
  padding: 12px 0;
  display: flex;
  justify-content: space-around;
  border-top: 1px solid #00eaff;
  box-shadow: 0 0 15px #00eaff;
  z-index: 999;
}

.icon-menu div{
  text-align: center;
  color: white;
  font-size: 12px;
}

.icon-menu i{
  font-size: 22px;
  margin-bottom: 3px;
  color: #00eaff;
  text-shadow: 0 0 10px #00eaff;
}

/* Clickable links */
a{
  color: #00eaff;
  text-decoration: none;
  font-weight: bold;
}
</style>
</head>
<body>

<div class="container">

  <div class="section">
    <h2>🌄 Astore Tourist Information Hub</h2>
    <p>
      Welcome to Astore — a paradise of valleys, mountains, lakes, and natural beauty.  
      This website helps tourists book rooms, hire cars, and get all travel information quickly.
    </p>
  </div>

  <div class="section">
    <h2>🏠 Room Booking</h2>
    <input id="rname" placeholder="Your Name">
    <input id="rphone" placeholder="Phone Number">
    <label>Check-In:</label>
    <input type="date" id="rcheckin">
    <label>Check-Out:</label>
    <input type="date" id="rcheckout">
    <select id="rroom">
      <option value="Single Room">Single Room</option>
      <option value="Double Room">Double Room</option>
      <option value="Family Room">Family Room</option>
    </select>
    <button onclick="roomBook()">Book via WhatsApp</button>
  </div>

  <div class="section">
    <h2>🚗 Car Booking</h2>
    <input id="cname" placeholder="Your Name">
    <input id="cphone" placeholder="Phone Number">
    <label>Pickup Date:</label>
    <input type="date" id="cdate">
    <select id="ccar">
      <option value="Corolla">Corolla</option>
      <option value="Hiace">Hiace</option>
      <option value="Jeep">Jeep</option>
      <option value="APV">APV</option>
    </select>
    <button onclick="carBook()">Book via WhatsApp</button>
  </div>

  <div class="section">
    <h2>ℹ About Astore</h2>
    <p>
      Astore Valley is one of Pakistan’s most beautiful mountain regions, famous for Rama Lake, Nanga Parbat viewpoint, 
      Deosai access, lush green meadows, crystal rivers, and peaceful weather.
    </p>
  </div>

  <div class="section">
    <h2>👤 Owner Details</h2>
    <p>
      <b>Name:</b> Asim Khanzai (Social Worker)<br>
      <b>Phone:</b> <a href="tel:03171588489">0317-1588489</a><br>
      <b>WhatsApp:</b> <a href="https://wa.me/03171588489">Click to Chat</a><br>
      <b>Email:</b> <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a><br>
      <b>Facebook:</b> 
      <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Click to Open</a><br>
      <b>Location:</b>  
      <a href="https://maps.google.com/?q=Asim KhanZai Social Worker, DC House, Eidgah, Astore">
        View on Google Maps
      </a>
    </p>
  </div>

</div>

<!-- Bottom fixed menu -->
<div class="icon-menu">
  <div><i class="fa-solid fa-house"></i><br>Home</div>
  <div><i class="fa-solid fa-bed"></i><br>Rooms</div>
  <div><i class="fa-solid fa-car"></i><br>Cars</div>
  <div><i class="fa-solid fa-user"></i><br>Owner</div>
</div>

<script>
function roomBook(){
  let n=document.getElementById("rname").value;
  let p=document.getElementById("rphone").value;
  let ci=document.getElementById("rcheckin").value;
  let co=document.getElementById("rcheckout").value;
  let r=document.getElementById("rroom").value;
  let msg=`Room Booking Request:%0AName: ${n}%0APhone: ${p}%0ACheck-in: ${ci}%0ACheck-out: ${co}%0ARoom: ${r}`;
  window.open(`https://wa.me/03171588489?text=${msg}`,'_blank');
}

function carBook(){
  let n=document.getElementById("cname").value;
  let p=document.getElementById("cphone").value;
  let d=document.getElementById("cdate").value;
  let c=document.getElementById("ccar").value;
  let msg=`Car Booking Request:%0AName: ${n}%0APhone: ${p}%0APickup Date: ${d}%0ACar: ${c}`;
  window.open(`https://wa.me/03171588489?text=${msg}`,'_blank');
}
</script>

</body>
</html>
