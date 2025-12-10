<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Orbitron:wght@600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{
    font-family:'Poppins',sans-serif;
    background:#000;
    color:#fff;
    overflow-x:hidden;
}
header{
    text-align:center;
    padding:40px 20px 10px;
}
.logo{
    font-size:48px;
    font-family:'Orbitron',sans-serif;
    color:#00eaff;
    text-shadow:0 0 20px #00eaff;
}
.tagline{
    margin-top:5px;
    font-size:15px;
    color:#aef9ff;
}
.links a{
    display:block;
    margin-top:8px;
    color:#00eaff;
    font-size:15px;
    text-decoration:none;
}
.section-title{
    text-align:center;
    margin:20px 0 10px;
    font-size:22px;
    color:#00eaff;
}
.dashboard{
    width:92%;
    margin:auto;
    padding-bottom:120px;
}
.section-card{
    background:rgba(255,255,255,0.06);
    padding:20px;
    margin-top:20px;
    border-radius:15px;
    box-shadow:0 0 20px #00eaff55;
    transition:.3s;
}
.section-card:hover{
    transform:scale(1.03);
    box-shadow:0 0 30px #00ffff;
}
.section-card h3{
    text-align:center;
    margin-bottom:10px;
    color:#00eaff;
}
input,select,button{
    width:100%;
    padding:12px;
    margin-top:10px;
    border:none;
    border-radius:10px;
    background:rgba(255,255,255,0.15);
    color:#fff;
    font-size:15px;
}
button{
    background:#00eaff;
    color:#000;
    font-weight:600;
    cursor:pointer;
}
.packages{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:15px;
}
.package-box{
    background:rgba(255,255,255,0.08);
    padding:20px;
    border-radius:15px;
    text-align:center;
    box-shadow:0 0 20px #00eaff33;
    transition:.3s;
}
.package-box:hover{
    transform:scale(1.05);
    box-shadow:0 0 25px #00ffff;
}
.package-box i{
    font-size:38px;
    color:#00eaff;
    margin-bottom:10px;
}
.map-box{
    border-radius:15px;
    overflow:hidden;
    box-shadow:0 0 20px #00eaff55;
    margin:20px 0;
}
.icon-menu{
    position:fixed;
    bottom:0;
    left:0;
    width:100%;
    display:flex;
    justify-content:space-around;
    background:rgba(0,0,0,0.6);
    padding:10px 0;
    border-top:1px solid #00eaff;
    box-shadow:0 0 25px #00eaff;
}
.icon-menu div{
    text-align:center;
}
.icon-menu i{
    font-size:26px;
    color:#00eaff;
}
.icon-menu span{
    font-size:12px;
    color:#fff;
    display:block;
}
#dashboard section{
    display:none;
}
#room{display:block;}
</style>
</head>

<body>

<header>
    <h1 class="logo">Astore Tourist Hub</h1>
    <p class="tagline">Premium Rooms • Car Rentals • Adventure Tours</p>

    <div class="links">
        <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr" target="_blank">
            <i class="fa-brands fa-facebook"></i> Facebook Page
        </a>
        <a href="https://wa.me/923171588489" target="_blank">
            <i class="fa-brands fa-whatsapp"></i> WhatsApp: 0317-1588489
        </a>
        <a href="mailto:mohammadasimkhan2746@gmail.com">
            <i class="fa-solid fa-envelope"></i> Email Us
        </a>
    </div>
</header>

<div class="dashboard" id="dashboard">

    <!-- ROOM BOOKING -->
    <section id="room">
        <div class="section-title">🏨 Room Booking</div>

        <div class="section-card">
            <h3>Book Your Stay</h3>

            <input type="text" id="rname" placeholder="Your Name">
            <input type="text" id="rphone" placeholder="Phone Number">
            <input type="date" id="rcheckin">
            <input type="date" id="rcheckout">

            <select id="rtype">
                <option>Standard Room</option>
                <option>Luxury Room</option>
                <option>Family Suite</option>
            </select>

            <button onclick="roomSend()">Send on WhatsApp</button>
        </div>
    </section>

    <!-- CAR BOOKING -->
    <section id="car">
        <div class="section-title">🚗 Car Booking</div>

        <div class="section-card">
            <h3>Rent a Car</h3>

            <input type="text" id="cname" placeholder="Your Name">
            <input type="text" id="cphone" placeholder="Phone Number">
            <input type="date" id="cdate">

            <select id="ctype">
                <option>Corolla</option>
                <option>Hiace</option>
                <option>Prado</option>
                <option>Astore Jeep</option>
            </select>

            <button onclick="carSend()">Send on WhatsApp</button>
        </div>
    </section>

    <!-- PACKAGES -->
    <section id="packages">
        <div class="section-title">🌄 Astore Travel Packages</div>

        <div class="packages">
            <div class="package-box">
                <i class="fa-solid fa-mountain"></i>
                <h3>Basic</h3>
                <p>2 Nights, 3 Days</p>
            </div>
            <div class="package-box">
                <i class="fa-solid fa-car"></i>
                <h3>Luxury</h3>
                <p>4 Nights, 5 Days</p>
            </div>
            <div class="package-box">
                <i class="fa-solid fa-person-hiking"></i>
                <h3>Adventure</h3>
                <p>Jeep + Hiking + Camps</p>
            </div>
        </div>
    </section>

    <!-- MAP -->
    <section id="map">
        <div class="section-title">📍 Location</div>

        <div class="map-box">
            <iframe width="100%" height="350" loading="lazy" style="border:0;"
                src="https://www.google.com/maps?q=Astore,+Pakistan&output=embed">
            </iframe>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
        <div class="section-title">📞 Contact Info</div>

        <div class="section-card">
            <p><b>Owner:</b> Asim Khanzai</p>
            <p><b>WhatsApp:</b> <a style="color:#00eaff" href="https://wa.me/923171588489">0317-1588489</a></p>
            <p><b>Email:</b> <a style="color:#00eaff" href="mailto:mohammadasimkhan2746@gmail.com">Click Here</a></p>
        </div>
    </section>

</div>

<!-- FIXED BOTTOM MENU -->
<div class="icon-menu">
    <div onclick="show('room')"><i class="fa-solid fa-bed"></i><span>Room</span></div>
    <div onclick="show('car')"><i class="fa-solid fa-car"></i><span>Car</span></div>
    <div onclick="show('packages')"><i class="fa-solid fa-mountain"></i><span>Packages</span></div>
    <div onclick="show('map')"><i class="fa-solid fa-map"></i><span>Map</span></div>
    <div onclick="show('contact')"><i class="fa-solid fa-phone"></i><span>Contact</span></div>
</div>

<script>
function show(id){
    document.querySelectorAll("#dashboard section").forEach(sec => sec.style.display="none");
    document.getElementById(id).style.display="block";
}
function roomSend(){
    let msg =
    "Room Booking:\n" +
    "Name: " + rname.value + "\n" +
    "Phone: " + rphone.value + "\n" +
    "Check-in: " + rcheckin.value + "\n" +
    "Check-out: " + rcheckout.value + "\n" +
    "Room Type: " + rtype.value;

    window.open("https://wa.me/923171588489?text=" + encodeURIComponent(msg));
}
function carSend(){
    let msg =
    "Car Booking:\n" +
    "Name: " + cname.value + "\n" +
    "Phone: " + cphone.value + "\n" +
    "Pickup Date: " + cdate.value + "\n" +
    "Car Type: " + ctype.value;

    window.open("https://wa.me/923171588489?text=" + encodeURIComponent(msg));
}
</script>

</body>
</html>
