<Astore Tourist>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<meta name="description" content="Astore Tourist Information Hub by Asim Khanzai. Book rooms, cars, and tour packages easily. Explore Astore with professional guide.">
<meta name="keywords" content="Astore, Tourism, Tourist Hub, Room Booking, Car Booking, Tour Packages, Asim Khanzai">
<meta name="author" content="Asim Khanzai">
<!-- Open Graph -->
<meta property="og:title" content="Astore Tourist Information Hub">
<meta property="og:description" content="Book rooms, cars, and tours in Astore with Asim Khanzai. Professional tourist guide services.">
<meta property="og:image" content="https://i.ibb.co/2jL0MDK/mountains.jpg">
<meta property="og:url" content="https://yourwebsite.com">
<meta property="og:type" content="website">
<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Astore Tourist Information Hub">
<meta name="twitter:description" content="Book rooms, cars, and tours in Astore with Asim Khanzai. Professional tourist guide services.">
<meta name="twitter:image" content="https://i.ibb.co/2jL0MDK/mountains.jpg">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" integrity="sha512-Mr0r0kI3u0RZy+qg0xL1/E8Nx5TP6xk5Xq3s8sR0G9q0xk5Wq+zY5N5z9Yz0b1Y0Hk5v0Z0" crossorigin="anonymous" referrerpolicy="no-referrer" />

<style>
body{margin:0;font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;}
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#001f3f,#003f7f,#007bff,#00d4ff);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-2;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
.particle{position:fixed;width:8px;height:8px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
.container{max-width:1000px;margin:60px auto;background:rgba(0,0,0,0.35);padding:30px;border-radius:20px;backdrop-filter:blur(6px);box-shadow:0 0 20px #00eaff;}
.logo{text-align:center;font-size:36px;font-weight:700;color:#00eaff;text-shadow:0 0 12px #00eaff;margin-bottom:15px;}
.hero-text{text-align:center;margin-bottom:30px;}
.hero-text p{font-size:16px;color:#a7f5ff;}
label{margin-top:12px;display:block;}
input,select{width:100%;padding:12px;margin-top:6px;border-radius:8px;border:none;background:rgba(255,255,255,0.15);color:#fff;font-size:15px;}
button{width:100%;padding:14px;margin-top:18px;border:none;border-radius:8px;background:#00eaff;color:#000;font-size:18px;font-weight:600;cursor:pointer;}
button:hover{background:#00bcd4;}
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:15px;margin-top:20px;}
.package{background:rgba(0,0,0,0.3);padding:20px;border-radius:12px;box-shadow:0 0 15px #00eaff;}
.package h3{text-align:center;margin-bottom:10px;text-shadow:0 0 8px #00eaff;}
.package p{text-align:center;font-size:14px;}
.map-container{margin-top:30px;border-radius:12px;overflow:hidden;box-shadow:0 0 15px #00eaff;}
.contact{margin-top:30px;text-align:center;font-size:16px;}
.contact i{margin-right:8px;color:#00eaff;}
.social-share{margin-top:20px;text-align:center;}
.social-share a{margin:0 10px;font-size:24px;color:#00eaff;text-decoration:none;}
.social-share a:hover{color:#00fff0;}
.whatsapp-btn{position:fixed;right:20px;bottom:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 15px #25d366;}
</style>
</head>
<body>
<div class="bg-animate"></div>
<script>
for(let i=0;i<40;i++){
    let p=document.createElement("div");
    p.className="particle";
    p.style.left=Math.random()*100+"vw";
    p.style.animationDuration=(8+Math.random()*7)+"s";
    p.style.opacity=Math.random()*0.7+0.3;
    document.body.appendChild(p);
}
</script>

<div class="container">
    <div class="logo">Astore Tourist Hub</div>
    <div class="hero-text">
        <p>Owner: Asim Khanzai | WhatsApp: 03171588489 | Email: mohammadasimkhan2746@gmail.com</p>
    </div>

    <!-- Room Booking -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Room Booking</h2>
    <form id="roomForm">
        <label><i class="fa-solid fa-user"></i> Name</label><input type="text" id="rname" required>
        <label><i class="fa-solid fa-phone"></i> Phone</label><input type="text" id="rphone" required>
        <label><i class="fa-solid fa-calendar-days"></i> Check-in Date</label><input type="date" id="rcheckin" required>
        <label><i class="fa-solid fa-calendar-days"></i> Check-out Date</label><input type="date" id="rcheckout" required>
        <label><i class="fa-solid fa-bed"></i> Room Type</label>
        <select id="rtype" required>
            <option>Standard Room</option>
            <option>Luxury Room</option>
            <option>Family Suite</option>
        </select>
        <button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Room on WhatsApp</button>
    </form>

    <!-- Car Booking -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Car Booking</h2>
    <form id="carForm">
        <label><i class="fa-solid fa-user"></i> Name</label><input type="text" id="cname" required>
        <label><i class="fa-solid fa-phone"></i> Phone</label><input type="text" id="cphone" required>
        <label><i class="fa-solid fa-calendar-days"></i> Pickup Date</label><input type="date" id="cdate" required>
        <label><i class="fa-solid fa-car"></i> Car Type</label>
        <select id="ctype" required>
            <option>Corolla</option>
            <option>Hiace</option>
            <option>Prado</option>
            <option>Astore Local Jeep</option>
        </select>
        <button type="submit"><i class="fa-brands fa-whatsapp"></i> Book Car on WhatsApp</button>
    </form>

    <!-- Packages -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Tour Packages</h2>
    <div class="packages">
        <div class="package">
            <h3>Basic Package</h3>
            <p>2 Nights, 3 Days<br>Standard Room + Local Guide</p>
        </div>
        <div class="package">
            <h3>Luxury Package</h3>
            <p>4 Nights, 5 Days<br>Luxury Room + Car + Guide</p>
        </div>
        <div class="package">
            <h3>Adventure Package</h3>
            <p>5 Nights, 6 Days<br>Family Suite + Jeep Tour + Hiking</p>
        </div>
    </div>

    <!-- Map -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Our Location</h2>
    <div class="map-container">
        <iframe src="https://www.google.com/maps?q=Asim+KhanZai+Social+Worker,+near+DC+house,+Eidgah,+Astore,+14300&output=embed" width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </div>

    <!-- Contact -->
    <div class="contact">
        <p><i class="fa-solid fa-envelope"></i> Email: mohammadasimkhan2746@gmail.com</p>
    </div>

    <!-- Social Share -->
    <div class="social-share">
        <a href="https://wa.me/923171588489" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/sharer/sharer.php?u=https://yourwebsite.com" target="_blank"><i class="fa-brands fa-facebook"></i></a>
        <a href="https://twitter.com/intent/tweet?url=https://yourwebsite.com&text=Astore+Tourist+Information+Hub" target="_blank"><i class="fa-brands fa-twitter"></i></a>
    </div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489"><i class="fa-brands fa-whatsapp"></i></a>

<script>
// Particles
for(let i=0;i<40;i++){
    let p=document.createElement("div");
    p.className="particle";
    p.style.left=Math.random()*100+"vw";
    p.style.animationDuration=(8+Math.random()*7)+"s";
    p.style.opacity=Math.random()*0.7+0.3;
    document.body.appendChild(p);
}

// Booking Forms WhatsApp
document.getElementById("roomForm").addEventListener("submit",function(e){
    e.preventDefault();
    let msg=`Room Booking Request:%0AName: ${document.getElementById("rname").value}%0APhone: ${document.getElementById("rphone").value}%0ACheck-in: ${document.getElementById("rcheckin").value}%0ACheck-out: ${document.getElementById("rcheckout").value}%0ARoom Type: ${document.getElementById("rtype").value}`;
    window.location.href="https://wa.me/923171588489?text="+msg;
});
document.getElementById("carForm").addEventListener("submit",function(e){
    e.preventDefault();
    let msg=`Car Booking Request:%0AName: ${document.getElementById("cname").value}%0APhone: ${document.getElementById("cphone").value}%0APickup Date: ${document.getElementById("cdate").value}%0ACar Type: ${document.getElementById("ctype").value}`;
    window.location.href="https://wa.me/923171588489?text="+msg;
});
</script>
</body>
</html>
