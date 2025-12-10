<ASTORE>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Hub</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Montserrat:wght@700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{background:#000;color:#fff;overflow-x:hidden;}
.hero{
    background:url('https://images.unsplash.com/photo-1508261303786-0b39a5ca2dba?auto=format&fit=crop&w=1950&q=80');
    background-size:cover;background-position:center;
    height:360px;display:flex;flex-direction:column;
    justify-content:center;align-items:center;
    text-align:center;padding:20px;
    position:relative;
}
.hero::after{
    content:"";position:absolute;width:100%;height:100%;
    background:rgba(0,0,0,0.55);top:0;left:0;
}
.hero h1{
    position:relative;font-size:42px;font-weight:700;
    text-shadow:0 0 25px #00eaff;margin-bottom:10px;
}
.hero p{
    position:relative;font-size:16px;color:#dffbfd;
}
.container{padding:20px;max-width:900px;margin:auto;padding-bottom:120px;}
.section{display:none;margin-top:20px;}
.section-card{
    background:rgba(0,0,0,0.55);
    border:1px solid #00eaff;
    border-radius:15px;padding:25px;
    box-shadow:0 0 20px #00eaff;
    transition:0.3s;
}
.section-card:hover{transform:scale(1.03);}
.section-card h2{text-align:center;color:#00eaff;text-shadow:0 0 10px #00ffff;margin-bottom:10px;}
label{margin-top:10px;display:block;font-weight:500;}
input,select,button{
    width:100%;padding:12px;margin-top:5px;
    border-radius:10px;border:none;
    background:rgba(255,255,255,0.15);
    color:#fff;
}
button{
    background:#00eaff;color:#000;font-weight:700;
    margin-top:15px;cursor:pointer;
}
.package-grid{
    display:grid;gap:18px;
    grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
}
.package{
    background:rgba(0,0,0,0.55);
    padding:20px;border-radius:15px;
    border:1px solid #00eaff;
    text-align:center;transition:0.3s;
}
.package:hover{transform:scale(1.05);}
.package i{font-size:40px;color:#00eaff;margin-bottom:10px;}
.icon-menu{
    display:flex;justify-content:space-around;
    position:fixed;bottom:0;left:0;width:100%;
    background:rgba(0,0,0,0.7);
    padding:10px 0;border-top:1px solid #00eaff;
}
.icon-item{text-align:center;color:#00eaff;}
.icon-item i{
    font-size:28px;cursor:pointer;
    transition:0.3s;
}
.icon-item i:hover{transform:scale(1.2);color:#00ffff;}
.footer{
    text-align:center;margin-top:40px;color:#aeefff;font-size:14px;
}
a{color:#00eaff;text-decoration:none;}
a:hover{text-decoration:underline;}
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
    <h1>Astore Tourist Hub</h1>
    <p>Explore Paradise | Book Rooms, Cars & Travel Packages</p>
</div>

<div class="container">

<!-- DEFAULT SECTION -->
<div id="home" class="section" style="display:block;">
<div class="section-card">
    <h2>Welcome to Astore Tourist Hub</h2>
    <p style="text-align:center;color:#aeefff;">
        Tourist booking center for Room, Car, Jeep Tours & complete Astore guidance.<br><br>
        <b>Owner:</b> Asim Khanzai<br>
        <b>Phone:</b> <a href="tel:03171588489">0317-1588489</a><br>
        <b>Email:</b> <a href="mailto:mohammadasimkhan2746@gmail.com">mohammadasimkhan2746@gmail.com</a><br>
        <b>WhatsApp:</b> <a href="https://wa.me/923171588489">Click to Chat</a><br>
        <b>Facebook:</b> <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Astore Tourist Hub</a>
    </p>
</div>
</div>

<!-- ROOM -->
<div id="room" class="section">
<div class="section-card">
    <h2>Room Booking</h2>
    <form id="roomForm">
        <label>Name</label><input id="rname" required>
        <label>Phone</label><input id="rphone" required>
        <label>Check-in</label><input type="date" id="rcheckin" required>
        <label>Check-out</label><input type="date" id="rcheckout" required>
        <label>Room Type</label>
        <select id="rtype">
            <option>Standard Room</option>
            <option>Luxury Room</option>
            <option>Family Suite</option>
        </select>
        <button type="submit"><i class="fa-brands fa-whatsapp"></i> Send WhatsApp Booking</button>
    </form>
</div>
</div>

<!-- CAR -->
<div id="car" class="section">
<div class="section-card">
    <h2>Car / Jeep Booking</h2>
    <form id="carForm">
        <label>Name</label><input id="cname" required>
        <label>Phone</label><input id="cphone" required>
        <label>Pickup Date</label><input type="date" id="cdate" required>
        <label>Select Vehicle</label>
        <select id="ctype">
            <option>Corolla</option>
            <option>Hiace</option>
            <option>Local Jeep</option>
            <option>Prado</option>
        </select>
        <button type="submit"><i class="fa-brands fa-whatsapp"></i> Send WhatsApp Booking</button>
    </form>
</div>
</div>

<!-- PACKAGES -->
<div id="packages" class="section">
<h2 style="text-align:center;color:#00eaff;text-shadow:0 0 10px #00eaff;">Travel Packages</h2>
<div class="package-grid">
    <div class="package">
        <i class="fa-solid fa-mountain"></i>
        <h3>Basic Package</h3>
        <p>2 Nights / 3 Days<br>Standard Room + Guide</p>
    </div>

    <div class="package">
        <i class="fa-solid fa-car"></i>
        <h3>Luxury Package</h3>
        <p>4 Nights / 5 Days<br>Luxury Room + Car + Guide</p>
    </div>

    <div class="package">
        <i class="fa-solid fa-person-hiking"></i>
        <h3>Adventure Tour</h3>
        <p>Jeep Tour + Hiking + Camping</p>
    </div>
</div>
</div>

<!-- MAP -->
<div id="map" class="section">
<div class="section-card">
    <h2>Location</h2>
    <iframe src="https://www.google.com/maps?q=Astore+Pakistan&output=embed"
        width="100%" height="330" style="border:0;border-radius:15px;"></iframe>
</div>
</div>

<!-- CONTACT -->
<div id="contact" class="section">
<div class="section-card">
    <h2>Contact</h2>
    <p style="text-align:center;color:#aeefff;">
        <b>WhatsApp:</b> <a href="https://wa.me/923171588489">Tap to Chat</a><br>
        <b>Email:</b> <a href="mailto:mohammadasimkhan2746@gmail.com">Send Email</a><br>
        <b>Facebook:</b> <a href="https://www.facebook.com/share/1BoG9YCsZN/?mibextid=wwXIfr">Official Page</a>
    </p>
</div>
</div>

<div class="footer">Astore Tourist Hub © 2025 | All Rights Reserved</div>

</div>

<!-- MENU -->
<div class="icon-menu">
    <div class="icon-item" onclick="show('home')"><i class="fa-solid fa-house"></i><span>Home</span></div>
    <div class="icon-item" onclick="show('room')"><i class="fa-solid fa-bed"></i><span>Room</span></div>
    <div class="icon-item" onclick="show('car')"><i class="fa-solid fa-car"></i><span>Car</span></div>
    <div class="icon-item" onclick="show('packages')"><i class="fa-solid fa-mountain"></i><span>Packages</span></div>
    <div class="icon-item" onclick="show('map')"><i class="fa-solid fa-map-location-dot"></i><span>Map</span></div>
    <div class="icon-item" onclick="show('contact')"><i class="fa-solid fa-envelope"></i><span>Contact</span></div>
</div>

<script>
function show(id){
    document.querySelectorAll(".section").forEach(s=>s.style.display="none");
    document.getElementById(id).style.display="block";
}

// ROOM WhatsApp
roomForm.addEventListener("submit",e=>{
    e.preventDefault();
    let msg=`Room Booking Request:
Name: ${rname.value}
Phone: ${rphone.value}
Check-in: ${rcheckin.value}
Check-out: ${rcheckout.value}
Room Type: ${rtype.value}`;
    window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
});

// CAR WhatsApp
carForm.addEventListener("submit",e=>{
    e.preventDefault();
    let msg=`Car / Jeep Booking:
Name: ${cname.value}
Phone: ${cphone.value}
Pickup Date: ${cdate.value}
Vehicle: ${ctype.value}`;
    window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`);
});
</script>

</body>
</html>
