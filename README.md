<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<style>
/* ANIMATED BACKGROUND */
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(-45deg, #000814, #001233, #001845, #003566);
    background-size: 400% 400%;
    animation: bgMove 10s ease infinite;
    color: #fff;
}
@keyframes bgMove {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

/* PREMIUM NEON TITLE */
.neon-title {
    font-size: 32px;
    font-weight: bold;
    text-align: center;
    color: #00eaff;
    margin: 0;
    text-shadow: 
        0 0 10px #00eaff,
        0 0 20px #00bcd4,
        0 0 35px #0088aa,
        0 0 60px #004d66;
}

/* SUBTITLE */
.sub {
    text-align: center;
    color: #b2f2ff;
    font-size: 14px;
}

/* CARD SECTION */
.section {
    background: rgba(0,0,0,0.30);
    margin: 20px;
    padding: 20px;
    border-radius: 12px;
    backdrop-filter: blur(6px);
    box-shadow: 0 0 18px #00eaff55;
}

/* FORM */
input, select {
    width: 100%;
    padding: 12px;
    background: rgba(255,255,255,0.1);
    border: 1px solid #00eaff99;
    border-radius: 8px;
    margin-bottom: 15px;
    color: white;
}
input::placeholder {color: #ccc;}

/* BUTTON */
button {
    width: 100%;
    padding: 14px;
    background: #00eaff;
    color: #000;
    border: none;
    font-size: 16px;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
    box-shadow: 0 0 10px #00eaff, 0 0 20px #0088aa;
}
button:hover {background: #00cce0;}

/* GALLERY */
.gallery img {
    width: 100%;
    border-radius: 12px;
    margin-bottom: 15px;
    box-shadow: 0 0 12px #00eaff55;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 15px;
    color: #00eaff;
    font-size: 14px;
}
</style>

<script>
/* WHATSAPP ROOM BOOKING */
function sendRoomBooking(){
    let name = document.getElementById("rname").value;
    let phone = document.getElementById("rphone").value;
    let cin = document.getElementById("rcheckin").value;
    let cot = document.getElementById("rcheckout").value;
    let room = document.getElementById("rtype").value;

    let msg = `Room Booking Request:
Name: ${name}
Phone: ${phone}
Check-in: ${cin}
Check-out: ${cot}
Room Type: ${room}`;

    window.open("https://wa.me/923555396518?text=" + encodeURIComponent(msg));
}

/* WHATSAPP CAR BOOKING */
function sendCarBooking(){
    let name = document.getElementById("cname").value;
    let phone = document.getElementById("cphone").value;
    let date = document.getElementById("cdate").value;
    let car = document.getElementById("ctype").value;

    let msg = `Car Booking Request:
Name: ${name}
Phone: ${phone}
Pickup Date: ${date}
Car Type: ${car}`;

    window.open("https://wa.me/923555396518?text=" + encodeURIComponent(msg));
}
</script>

</head>
<body>

<!-- HEADER -->
<header style="padding:25px;">
    <h1 class="neon-title">Astore Tourist Information Hub</h1>
    <p class="sub">Owner: Asim Khanzai — Contact: 03555396518</p>
</header>

<!-- ROOM BOOKING -->
<div class="section">
    <h2 style="color:#00eaff; text-shadow:0 0 8px #00eaff;">Room Booking</h2>

    <input id="rname" type="text" placeholder="Your Name" required>
    <input id="rphone" type="text" placeholder="03XXXXXXXXX" required>

    <label>Check-in Date</label>
    <input id="rcheckin" type="date" required>

    <label>Check-out Date</label>
    <input id="rcheckout" type="date" required>

    <select id="rtype" required>
        <option>Standard Room</option>
        <option>Luxury Room</option>
        <option>Family Suite</option>
    </select>

    <button onclick="sendRoomBooking()">Book Room on WhatsApp</button>
</div>

<!-- CAR BOOKING -->
<div class="section">
    <h2 style="color:#00eaff; text-shadow:0 0 8px #00eaff;">Car Booking</h2>

    <input id="cname" type="text" placeholder="Your Name" required>
    <input id="cphone" type="text" placeholder="03XXXXXXXXX" required>

    <label>Pickup Date</label>
    <input id="cdate" type="date" required>

    <select id="ctype" required>
        <option>Corolla</option>
        <option>Hiace</option>
        <option>Prado</option>
        <option>Astore Local Jeep</option>
    </select>

    <button onclick="sendCarBooking()">Book Car on WhatsApp</button>
</div>

<!-- GALLERY -->
<div class="section">
    <h2 style="color:#00eaff; text-shadow:0 0 8px #00eaff;">Astore Tourist Gallery</h2>

    <div class="gallery">
        <img src="https://i.ibb.co/2jL0MDK/mountains.jpg">
        <img src="https://i.ibb.co/s3Xs1H0/lake.jpg">
        <img src="https://i.ibb.co/x3tFLYc/valley.jpg">
    </div>
</div>

<!-- FOOTER -->
<footer>
    © 2025 Astore Tourist Hub — All Rights Reserved
</footer>

</body>
</html>
