<!DOCTYPE html>
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
  font-family: Arial, sans-serif;
  background: black;
  color: white;
  overflow-x: hidden;
}

/* Neon Gradient Animated Background */
.bg {
  position: fixed;
  top:0; left:0;
  width:100%; height:100%;
  background: linear-gradient(45deg,#00111f,#002a3d,#000000,#00334d);
  background-size: 400% 400%;
  animation: neonbg 10s infinite alternate;
  z-index:-1;
}
@keyframes neonbg {
  0% {background-position:0% 50%;}
  100% {background-position:100% 50%;}
}

/* Header Title */
.header {
  text-align:center;
  padding:25px 10px;
  font-size:28px;
  font-weight:900;
  text-shadow:0 0 12px #00eaff;
  letter-spacing:2px;
}

/* Dashboard Box */
.box {
  width:90%;
  margin:15px auto;
  padding:18px;
  background:rgba(0,0,0,0.45);
  border-radius:15px;
  box-shadow:0 0 18px #00eaff;
  backdrop-filter: blur(4px);
}

/* Fixed Bottom Menu Icons */
.menu {
  position:fixed;
  bottom:0;
  left:0;
  width:100%;
  display:flex;
  justify-content:space-around;
  background:rgba(0,0,0,0.55);
  padding:10px 0;
  border-top:1px solid #00eaff;
  box-shadow:0 0 15px #00eaff;
  z-index:99;
}

.menu div {
  text-align:center;
  font-size:12px;
  color:#00eaff;
}

.menu i {
  font-size:22px;
  margin-bottom:4px;
}

/* Buttons */
.btn {
  display:block;
  width:100%;
  margin:8px 0;
  padding:12px;
  background:#00eaff;
  border:none;
  border-radius:10px;
  color:black;
  font-weight:bold;
  font-size:16px;
  box-shadow:0 0 10px #00eaff;
}

/* Clickable Links */
a {
  color:#00eaff;
  text-decoration:none;
  font-weight:bold;
}
</style>
</head>

<body>

<div class="bg"></div>

<div class="header">🌄 ASTORE TOURIST INFORMATION HUB</div>

<div class="box">
  <h2 style="margin-top:0; text-shadow:0 0 10px #00eaff;">WELCOME TO ASTORE</h2>
  <p>
    Astore Gilgit-Baltistan ka sab se khoobsurat tourist spot mana jata hai.  
    Hamari service ka maqsad hai ke tourists ko:
    <br><br>
    ✔ Room Booking  
    ✔ Car / Jeep Booking  
    ✔ Tourist Guide  
    ✔ Location Assistance  
    ✔ Travel Support  
    <br><br>
    Sab kuch **ek hi jagah** provide kiya jaye.
  </p>
</div>

<div class="box">
  <h3 style="text-shadow:0 0 10px #00eaff;">📍 Contact Details</h3>

  <p><i class="fa-brands fa-whatsapp"></i>  
  <a href="https://wa.me/923171588489" target="_blank">WhatsApp: 0317-1588489</a></p>

  <p><i class="fa-regular fa-envelope"></i>  
  <a href="mailto:mohammadasimkhan2746@gmail.com">Email: mohammadasimkhan2746@gmail.com</a></p>

  <p><i class="fa-brands fa-facebook"></i>  
  <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">
  Facebook Profile</a></p>

  <p><i class="fa-solid fa-location-dot"></i>  
  <a href="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore+14300" target="_blank">
  Google Map Location</a></p>
</div>

<div class="box">
  <h3 style="text-shadow:0 0 10px #00eaff;">🚗 Quick Booking Options</h3>

  <button class="btn" onclick="room()">Book Room</button>
  <button class="btn" onclick="car()">Book Car / Jeep</button>
  <button class="btn" onclick="guide()">Tourist Guide Info</button>
</div>

<!-- Fixed Bottom Menu -->
<div class="menu">
  <div><i class="fa-solid fa-house"></i><br>Home</div>
  <div><i class="fa-solid fa-bed"></i><br>Rooms</div>
  <div><i class="fa-solid fa-car"></i><br>Cars</div>
  <div><i class="fa-solid fa-map"></i><br>Guide</div>
  <div><i class="fa-solid fa-phone"></i><br>Contact</div>
</div>

<script>
function room(){
  window.open("https://wa.me/923171588489?text=Room%20Booking%20Required","_blank");
}
function car(){
  window.open("https://wa.me/923171588489?text=Car%20or%20Jeep%20Booking%20Required","_blank");
}
function guide(){
  window.open("https://wa.me/923171588489?text=Need%20a%20Tourist%20Guide","_blank");
}
</script>

</body>
</html>
