<Astore tourist hub>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    color: #fff;
    overflow-x: hidden;
    background: #001f3f;
}

/* Animated Gradient Background */
.bg-animate {
    position: fixed;
    width: 100%;
    height: 100%;
    background: linear-gradient(270deg, #001f3f, #003f7f, #007bff, #00d4ff);
    background-size: 800% 800%;
    animation: gradientBG 20s ease infinite;
    z-index: -1;
}
@keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

/* Container */
.container {
    max-width: 1000px;
    margin: 80px auto;
    background: rgba(0,0,0,0.4);
    padding: 30px;
    border-radius: 20px;
    backdrop-filter: blur(6px);
    box-shadow: 0 0 20px #00eaff;
}

/* Hero Section */
.hero {
    text-align: center;
    padding: 20px;
}
.hero h1 {
    font-size: 42px;
    font-weight: 600;
    text-shadow: 0 0 12px #00eaff;
}
.hero p {
    font-size: 18px;
    color: #a7f5ff;
}

/* Booking Forms */
label {margin-top: 12px; display:block;}
input, select {width:100%; padding:12px; margin-top:6px; border-radius:8px; border:none; background:rgba(255,255,255,0.15); color:#fff;}
button {width:100%; padding:14px; margin-top:18px; border:none; border-radius:8px; background:#00eaff; color:#000; font-size:18px; font-weight:600; cursor:pointer;}
button:hover {background:#00bcd4;}

/* Gallery */
.gallery {display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:15px; margin-top:20px;}
.gallery img {width:100%; border-radius:12px; box-shadow:0 0 15px #00eaff55;}

/* WhatsApp Button */
.whatsapp-btn {
    position: fixed;
    right: 20px;
    bottom: 20px;
    background: #25d366;
    padding: 16px 18px;
    border-radius:50%;
    color: #fff;
    font-size:28px;
    text-decoration:none;
    box-shadow:0 0 15px #25d366;
}
</style>
</head>
<body>
<div class="bg-animate"></div>

<div class="container">
    <div class="hero">
        <h1>Astore Tourist Information Hub</h1>
        <p>Owner: Asim Khanzai | WhatsApp: 03171588489</p>
    </div>

    <h2 style="text-shadow:0 0 8px #00eaff;">Room Booking</h2>
    <form id="roomForm">
        <label>Name</label><input type="text" id="rname" required>
        <label>Phone</label><input type="text" id="rphone" required>
        <label>Check-in Date</label><input type="date" id="rcheckin" required>
        <label>Check-out Date</label><input type="date" id="rcheckout" required>
        <label>Room Type</label>
        <select id="rtype" required>
            <option>Standard Room</option>
            <option>Luxury Room</option>
            <option>Family Suite</option>
        </select>
        <button type="submit">Book Room on WhatsApp</button>
    </form>

    <h2 style="text-shadow:0 0 8px #00eaff;">Car Booking</h2>
    <form id="carForm">
        <label>Name</label><input type="text" id="cname" required>
        <label>Phone</label><input type="text" id="cphone" required>
        <label>Pickup Date</label><input type="date" id="cdate" required>
        <label>Car Type</label>
        <select id="ctype" required>
            <option>Corolla</option>
            <option>Hiace</option>
            <option>Prado</option>
            <option>Astore Local Jeep</option>
        </select>
        <button type="submit">Book Car on WhatsApp</button>
    </form>

    <h2 style="text-shadow:0 0 8px #00eaff;">Tourist Gallery</h2>
    <div class="gallery">
        <img src="https://i.ibb.co/2jL0MDK/mountains.jpg">
        <img src="https://i.ibb.co/s3Xs1H0/lake.jpg">
        <img src="https://i.ibb.co/x3tFLYc/valley.jpg">
        <img src="https://i.ibb.co/jJxZTcZ/river.jpg">
        <img src="https://i.ibb.co/mJ9xXrF/forest.jpg">
        <img src="https://i.ibb.co/G0r6yCJ/hills.jpg">
    </div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489">💬</a>

<script>
document.getElementById("roomForm").addEventListener("submit", function(e){
    e.preventDefault();
    let msg = `Room Booking Request:%0AName: ${document.getElementById("rname").value}%0APhone: ${document.getElementById("rphone").value}%0ACheck-in: ${document.getElementById("rcheckin").value}%0ACheck-out: ${document.getElementById("rcheckout").value}%0ARoom Type: ${document.getElementById("rtype").value}`;
    window.location.href = "https://wa.me/923171588489?text=" + msg;
});
document.getElementById("carForm").addEventListener("submit", function(e){
    e.preventDefault();
    let msg = `Car Booking Request:%0AName: ${document.getElementById("cname").value}%0APhone: ${document.getElementById("cphone").value}%0APickup Date: ${document.getElementById("cdate").value}%0ACar Type: ${document.getElementById("ctype").value}`;
    window.location.href = "https://wa.me/923171588489?text=" + msg;
});
</script>
</body>
</html>
