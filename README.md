<astore tourist>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
body{margin:0;font-family:'Poppins',sans-serif;color:#fff;overflow-x:hidden;background:#001f3f;}
/* Background gradient + animation */
.bg-animate{position:fixed;width:100%;height:100%;background:linear-gradient(270deg,#001f3f,#003f7f,#007bff,#00d4ff);background-size:800% 800%;animation:gradientBG 20s ease infinite;z-index:-2;}
@keyframes gradientBG{0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
/* Particles */
.particle{position:fixed;width:8px;height:8px;background:#00eaff;border-radius:50%;opacity:0.7;animation:floatUp linear infinite;}
@keyframes floatUp{0%{transform:translateY(110vh);}100%{transform:translateY(-10vh);}}
/* Container */
.container{max-width:1000px;margin:60px auto;background:rgba(0,0,0,0.35);padding:30px;border-radius:20px;backdrop-filter:blur(6px);box-shadow:0 0 20px #00eaff;}
/* Hero Slideshow */
.slideshow-container{position:relative;margin: auto;overflow:hidden;border-radius:15px;box-shadow:0 0 20px #00eaff;margin-bottom:30px;}
.slide{display:none;}
.slide img{width:100%;border-radius:15px;}
/* Hero text */
.hero-text{text-align:center;margin-bottom:15px;}
.hero-text h1{font-size:42px;text-shadow:0 0 12px #00eaff;}
.hero-text p{font-size:18px;color:#a7f5ff;}
/* Forms */
label{margin-top:12px;display:block;}
input,select{width:100%;padding:12px;margin-top:6px;border-radius:8px;border:none;background:rgba(255,255,255,0.15);color:#fff;font-size:15px;}
button{width:100%;padding:14px;margin-top:18px;border:none;border-radius:8px;background:#00eaff;color:#000;font-size:18px;font-weight:600;cursor:pointer;}
button:hover{background:#00bcd4;}
/* Gallery */
.gallery{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:15px;margin-top:20px;}
.gallery img{width:100%;border-radius:12px;box-shadow:0 0 15px #00eaff55;}
/* Pricing cards */
.packages{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:15px;margin-top:20px;}
.package{background:rgba(0,0,0,0.3);padding:20px;border-radius:12px;box-shadow:0 0 15px #00eaff;}
.package h3{text-align:center;margin-bottom:10px;text-shadow:0 0 8px #00eaff;}
.package p{text-align:center;}
/* Map */
.map-container{margin-top:30px;border-radius:12px;overflow:hidden;box-shadow:0 0 15px #00eaff;}
/* WhatsApp Button */
.whatsapp-btn{position:fixed;right:20px;bottom:20px;background:#25d366;padding:16px 18px;border-radius:50%;color:#fff;font-size:28px;text-decoration:none;box-shadow:0 0 15px #25d366;}
</style>
</head>
<body>
<div class="bg-animate"></div>
<!-- Particles -->
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
    <div class="hero-text">
        <h1>Astore Tourist Information Hub</h1>
        <p>Owner: Asim Khanzai | WhatsApp: 03171588489</p>
    </div>

    <!-- Hero Slideshow -->
    <div class="slideshow-container">
        <div class="slide"><img src="https://i.ibb.co/2jL0MDK/mountains.jpg" alt="Mountains"></div>
        <div class="slide"><img src="https://i.ibb.co/s3Xs1H0/lake.jpg" alt="Lake"></div>
        <div class="slide"><img src="https://i.ibb.co/x3tFLYc/valley.jpg" alt="Valley"></div>
    </div>

    <!-- Room Booking -->
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

    <!-- Car Booking -->
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

    <!-- Gallery -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Tourist Gallery</h2>
    <div class="gallery">
        <img src="https://i.ibb.co/2jL0MDK/mountains.jpg" alt="Mountains">
        <img src="https://i.ibb.co/s3Xs1H0/lake.jpg" alt="Lake">
        <img src="https://i.ibb.co/x3tFLYc/valley.jpg" alt="Valley">
        <img src="https://i.ibb.co/jJxZTcZ/river.jpg" alt="River">
        <img src="https://i.ibb.co/mJ9xXrF/forest.jpg" alt="Forest">
        <img src="https://i.ibb.co/G0r6yCJ/hills.jpg" alt="Hills">
    </div>

    <!-- Map -->
    <h2 style="text-shadow:0 0 8px #00eaff;">Our Location</h2>
    <div class="map-container">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3221.142479537711!2d74.5048195!3d35.365046!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38df1b66a4f1d8b1%3A0x7b0d46b3e823f1c5!2sAstore%2C%20Gilgit-Baltistan!5e0!3m2!1sen!2s!4v1700000000000!5m2!1sen!2s" width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </div>
</div>

<a class="whatsapp-btn" href="https://wa.me/923171588489">💬</a>

<script>
// Slideshow
let slideIndex=0;
showSlides();
function showSlides(){
    let slides=document.getElementsByClassName("slide");
    for(let i=0;i<slides.length;i++){slides[i].style.display="none";}
    slideIndex++;
    if(slideIndex>slides.length){slideIndex=1;}
    slides[slideIndex-1].style.display="block";
    setTimeout(showSlides,4000);
}

// Particles already added above
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
