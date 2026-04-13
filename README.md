<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Master Hub | PRO</title><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet"><style>
:root { 
    --primary:#065f46; 
    --accent:#fbbf24; 
    --bg:#f1f5f9; 
    --card:#fff; 
    --text:#0f172a;
}
.dark {
    --bg:#020617;
    --card:#1e293b;
    --text:#f8fafc;
    --primary:#34d399;
}
*{margin:0;padding:0;box-sizing:border-box;font-family:'Plus Jakarta Sans',sans-serif;transition:.3s}
body{background:var(--bg);color:var(--text)}

#loader{
position:fixed;inset:0;background:#000;color:#fff;
display:flex;align-items:center;justify-content:center;
z-index:9999;font-weight:800
}

.alert-top{
background:var(--accent);padding:8px;text-align:center;
font-size:.7rem;font-weight:800
}

header{
position:sticky;top:0;background:rgba(255,255,255,.8);
backdrop-filter:blur(10px);
display:flex;justify-content:space-between;
padding:10px 15px;font-weight:800
}

.hero{height:35vh;overflow:hidden}
.slider{display:flex;width:400%;height:100%;animation:slide 16s infinite}
.slide img{width:100%;height:100%;object-fit:cover}

@keyframes slide{
0%,20%{transform:translateX(0)}
25%,45%{transform:translateX(-25%)}
50%,70%{transform:translateX(-50%)}
75%,95%{transform:translateX(-75%)}
}

.container{padding:15px}

.grid{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:10px
}

.feature-box{
background:var(--card);
padding:15px;text-align:center;
border-radius:15px;
box-shadow:0 5px 10px rgba(0,0,0,.05)
}

.btn{
background:#25d366;
color:#fff;padding:12px;
border:none;width:100%;
border-radius:10px;font-weight:800
}

.fab{
position:fixed;bottom:20px;right:20px;
background:var(--primary);
color:#fff;padding:15px;
border-radius:50%
}
</style></head><body><div id="loader">Loading Astore Hub...</div><div class="alert-top">
Road to Minimarg OPEN • SCOM Working • Stay Safe
</div><header>
<div>ASTORE HUB</div>
<div id="time"></div>
</header><section class="hero">
<div class="slider">
<div class="slide"><img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b"></div>
<div class="slide"><img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb"></div>
<div class="slide"><img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e"></div>
<div class="slide"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e"></div>
</div>
</section><div class="container"><h3>Services</h3><div class="grid">
<div class="feature-box">Jeep</div>
<div class="feature-box">Hotel</div>
<div class="feature-box">Guide</div>
<div class="feature-box">Food</div>
<div class="feature-box">Camping</div>
<div class="feature-box">Photo</div>
</div><br><input type="date" id="dt"><br><br>

<button class="btn" onclick="book()">WhatsApp Booking</button>

</div><button class="fab" onclick="toggleDark()">🌙</button>

<audio id="clickSound" src="https://www.soundjay.com/buttons/sounds/button-16.mp3"></audio>

<script>

// Loader
window.onload = ()=>document.getElementById('loader').style.display='none'

// Clock
setInterval(()=>{
document.getElementById('time').innerText=
new Date().toLocaleTimeString([], {hour:'2-digit',minute:'2-digit'})
},1000)

// Dark mode auto
if(window.matchMedia('(prefers-color-scheme: dark)').matches){
document.body.classList.add('dark')
}

// Toggle
function toggleDark(){
document.body.classList.toggle('dark')
}

// Date auto
document.getElementById('dt').valueAsDate=new Date()

// Click sound
document.querySelectorAll('button,.feature-box').forEach(el=>{
el.addEventListener('click',()=>{
document.getElementById('clickSound').play()
})
})

// Slider pause on touch
let slider=document.querySelector('.slider')
slider.addEventListener('touchstart',()=>slider.style.animationPlayState='paused')
slider.addEventListener('touchend',()=>slider.style.animationPlayState='running')

// Booking
function book(){
let d=document.getElementById('dt').value
let msg=`Booking for ${d || 'upcoming'}`
window.open(`https://wa.me/923171588489?text=${encodeURIComponent(msg)}`)
}

// Install popup
let deferredPrompt
window.addEventListener('beforeinstallprompt', (e)=>{
e.preventDefault()
deferredPrompt=e
setTimeout(()=>{
if(confirm("Install App?")) deferredPrompt.prompt()
},3000)
})

</script></body>
</html>
