<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Astore Tourist Information Hub</title>
<style>
 body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(270deg,#000814,#001d3d,#000814,#001d3d);
  background-size: 800% 800%;
  animation: gradientBG 20s ease infinite;
  color: #fff;
  overflow-x: hidden;
 }
 @keyframes gradientBG {
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
 }
 header {
  text-align: center;
  padding: 25px 10px;
  font-size: 26px;
  font-weight: bold;
  text-shadow: 0 0 20px #00eaff, 0 0 40px #00ffff;
 }
 .about-box, .card {
  margin: 15px;
  padding: 18px;
  background: rgba(0,0,0,0.3);
  border-radius: 15px;
  box-shadow: 0 0 15px #00eaff, 0 0 25px #00ffff;
  animation: glowPulse 3s infinite alternate;
 }
 @keyframes glowPulse {
  0%{box-shadow:0 0 15px #00eaff,0 0 25px #00ffff;}
  100%{box-shadow:0 0 25px #00eaff,0 0 50px #00ffff;}
 }
 a { color: #00eaff; text-decoration:none; }
 .icon-menu {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-around;
  padding: 14px 0;
  background: rgba(0,0,0,0.6);
  backdrop-filter: blur(8px);
  border-top: 1px solid #00eaff;
  box-shadow: 0 0 20px #00eaff, 0 0 40px #00ffff;
  z-index: 9999;
 }
 .icon-menu button {
  background: none;
  border: none;
  color: #00eaff;
  font-size: 14px;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: transform 0.3s;
 }
 .icon-menu button:hover { transform: scale(1.2); color:#00ffff; }
 .hidden-section { display: none; margin: 15px; padding-bottom: 100px; }
</style>
</head>
<body>
<header>Astore Tourist Information Hub</header>

<div class="about-box" id="about">
 <h3>About Us</h3>
 <p>Astore Tourist Information Hub provides premium guidance for exploring Astore Valley, Gilgit Baltistan. We offer travel info, hotels, cars, route guidance, and weather updates with neon glow animations for an immersive experience.</p>
 <p>Contact: <a href="tel:03171588489">03171588489</a> | Email: <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a></p>
 <p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Click Here</a></p>
 <p>Location: <a href="https://maps.google.com/?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore">View on Google Maps</a></p>
</div>

<div id="services" class="hidden-section">
 <div class="card">
  <h3>Hotel & Room Info</h3>
  <p>Find best hotels, guest houses, and room availability in Astore.</p>
  <a href="https://wa.me/03171588489?text=Hi,+I+need+room+details">Book on WhatsApp</a>
 </div>
 <div class="card">
  <h3>Car Rentals</h3>
  <p>Book Prado, Corolla, HiAce, Jeep & Coaster for all destinations.</p>
  <a href="https://wa.me/03171588489?text=Hi,+I+need+car+details">Book a Car</a>
 </div>
 <div class="card">
  <h3>Travel Guidance</h3>
  <p>Weather, road conditions, routes, and travel safety updates.</p>
 </div>
</div>

<div id="contact" class="hidden-section">
 <div class="card">
  <h3>Contact Us</h3>
  <p>WhatsApp: <a href="https://wa.me/03171588489">03171588489</a></p>
  <p>Email: <a href="mailto:mohammadasimkhan2746@gmail.com">Send Email</a></p>
  <p>Facebook: <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Open</a></p>
 </div>
</div>

<div class="icon-menu">
 <button onclick="show('services')">🗺️<br>Services</button>
 <button onclick="show('contact')">📞<br>Contact</button>
 <button onclick="show('about')">ℹ️<br>About</button>
</div>

<script>
function show(section){
 document.querySelectorAll('.hidden-section').forEach(s=>s.style.display='none');
 if(section==='about') window.scrollTo({top:0,behavior:'smooth'});
 else { document.getElementById(section).style.display='block'; window.scrollTo({top:0,behavior:'smooth'}); }
}
</script>
</body>
</html>
