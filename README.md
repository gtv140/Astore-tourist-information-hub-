<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Astore Hub Pro | Astore Tourist Information Hub</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Georgia&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<style>
  :root{
    --ink:#182420; --paper:#F3EFE4; --pine:#3E5C46; --glacier:#7FA6AC;
    --clay:#C1723D; --line:rgba(24,36,32,.12); --card:#ffffff;
  }
  *{box-sizing:border-box;}
  body{margin:0;font-family:'Source Sans 3','Segoe UI',system-ui,sans-serif;background:var(--paper);color:var(--ink);}
  h1,h2,h3{font-family:Georgia,'Times New Roman',serif;margin:0;}
  a{color:inherit;}
  section{padding:56px 20px;max-width:1100px;margin:0 auto;}
  .eyebrow{display:block;font-size:12px;letter-spacing:.14em;text-transform:uppercase;color:var(--pine);margin-bottom:6px;}

  /* ---------- HEADER ---------- */
  header{display:flex;align-items:center;justify-content:space-between;padding:16px 20px;background:var(--ink);color:var(--paper);position:sticky;top:0;z-index:50;}
  header .brand{font-weight:700;letter-spacing:.05em;}
  header nav{display:flex;gap:18px;align-items:center;font-size:14px;}
  header nav a{text-decoration:none;opacity:.85;}
  header nav a:hover{opacity:1;}
  #langToggle{background:transparent;border:1px solid rgba(243,239,228,.35);color:var(--paper);padding:6px 12px;border-radius:999px;cursor:pointer;font-size:13px;}

  /* ---------- HERO ---------- */
  .hero{position:relative;min-height:60vh;display:flex;align-items:flex-end;background:linear-gradient(rgba(24,36,32,.45),rgba(24,36,32,.75)),url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=1600') center/cover;color:var(--paper);}
  .hero-inner{padding:48px 20px;max-width:1100px;margin:0 auto;width:100%;}
  .hero h1{font-size:clamp(30px,5vw,52px);}
  .hero p{max-width:480px;margin-top:10px;color:rgba(243,239,228,.85);}

  /* ---------- WEATHER WIDGET ---------- */
  .weather-bar{background:var(--pine);color:var(--paper);}
  .weather-bar section{padding:18px 20px;display:flex;flex-wrap:wrap;gap:24px;align-items:center;}
  .weather-bar .wx-stat{font-size:14px;}
  .weather-bar .wx-stat b{font-size:18px;display:block;}

  /* ---------- SEARCH / FILTER ---------- */
  .search-row{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:24px;}
  .search-row input[type="text"]{flex:1;min-width:200px;padding:10px 14px;border-radius:8px;border:1px solid var(--line);font-size:14px;}
  .chip{appearance:none;border:1px solid var(--line);background:transparent;color:var(--ink);padding:8px 16px;border-radius:999px;font-size:13px;cursor:pointer;}
  .chip[aria-pressed="true"]{background:var(--clay);border-color:var(--clay);color:#fff;font-weight:600;}

  /* ---------- PLACES ---------- */
  .place-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px;}
  .place-card{background:var(--card);border-radius:10px;overflow:hidden;border:1px solid var(--line);}
  .place-card img{width:100%;height:160px;object-fit:cover;display:block;}
  .place-card .body{padding:14px 16px;}
  .place-card h3{font-size:18px;margin-bottom:6px;}
  .place-card p{font-size:14px;color:#4b5750;line-height:1.5;margin:0;}

  /* ---------- MAP ---------- */
  #map{height:380px;border-radius:10px;border:1px solid var(--line);}

  /* ---------- GALLERY (dark) ---------- */
  #gallery{background:var(--ink);color:var(--paper);max-width:none;padding:56px 20px;}
  #gallery .inner{max-width:1100px;margin:0 auto;}
  .filters{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:24px;}
  .filters .chip{border-color:rgba(243,239,228,.25);color:var(--paper);}
  .filters .chip[aria-pressed="true"]{background:var(--clay);border-color:var(--clay);}
  .grid{display:grid;grid-template-columns:repeat(4,1fr);grid-auto-rows:130px;gap:10px;}
  .g-item{position:relative;overflow:hidden;border-radius:6px;cursor:pointer;background:#10201a;border:none;padding:0;grid-row:span 2;}
  .g-item.tall{grid-row:span 3;} .g-item.wide{grid-column:span 2;}
  .g-item img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .5s ease;}
  .g-item:hover img{transform:scale(1.06);}
  .g-tag{position:absolute;left:8px;bottom:8px;font-size:11px;background:rgba(24,36,32,.72);color:var(--paper);padding:4px 9px;border-radius:999px;}
  @media (max-width:720px){.grid{grid-template-columns:repeat(2,1fr);grid-auto-rows:110px;}}
  .lightbox{position:fixed;inset:0;background:rgba(10,16,13,.94);display:none;align-items:center;justify-content:center;z-index:9999;padding:24px;}
  .lightbox.open{display:flex;}
  .lightbox figure{margin:0;max-width:900px;width:100%;}
  .lightbox img{width:100%;max-height:72vh;object-fit:contain;border-radius:4px;display:block;}
  .lightbox figcaption{display:flex;justify-content:space-between;font-size:14px;margin-top:12px;border-top:1px solid rgba(243,239,228,.2);padding-top:10px;}
  .lb-btn{position:absolute;top:50%;transform:translateY(-50%);background:transparent;border:1px solid rgba(243,239,228,.3);color:var(--paper);width:42px;height:42px;border-radius:50%;font-size:18px;cursor:pointer;}
  .lb-prev{left:16px;} .lb-next{right:16px;}
  .lb-close{position:absolute;top:18px;right:18px;background:transparent;border:none;color:var(--paper);font-size:26px;cursor:pointer;}

  /* ---------- BOOKING ---------- */
  .booking-card{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:24px;max-width:560px;}
  .booking-card label{display:block;font-size:13px;margin:14px 0 6px;color:#4b5750;}
  .booking-card input,.booking-card select,.booking-card textarea{width:100%;padding:10px 12px;border-radius:8px;border:1px solid var(--line);font-size:14px;font-family:inherit;}
  .btn-primary{margin-top:20px;background:var(--clay);color:#fff;border:none;padding:12px 22px;border-radius:999px;font-size:15px;cursor:pointer;font-weight:600;}
  .btn-primary:hover{opacity:.92;}
  .field-error{color:#b3342a;font-size:12px;margin-top:4px;display:none;}

  /* ---------- REVIEWS ---------- */
  .review-list{display:grid;gap:14px;margin-bottom:24px;}
  .review-card{background:var(--card);border:1px solid var(--line);border-radius:10px;padding:14px 16px;}
  .review-card .stars{color:var(--clay);font-size:14px;}
  .review-card .meta{font-size:12px;color:#7a8079;margin-top:4px;}
  .review-form{display:grid;gap:10px;max-width:480px;}
  .review-form input,.review-form select,.review-form textarea{padding:10px 12px;border-radius:8px;border:1px solid var(--line);font-family:inherit;font-size:14px;}

  footer{background:var(--ink);color:rgba(243,239,228,.7);text-align:center;padding:32px 20px;font-size:13px;}
  footer a{color:var(--glacier);}

  [data-lang="ur"]{display:none;}
  html[dir="rtl"] [data-lang="en"]{display:none;}
  html[dir="rtl"] [data-lang="ur"]{display:inline;}
  html[dir="rtl"] body{font-family:'Noto Nastaliq Urdu','Segoe UI',sans-serif;}
</style>
</head>
<body>

<header>
  <div class="brand">ASTORE HUB PRO</div>
  <nav>
    <a href="#places" data-lang="en">Places</a><a href="#places" data-lang="ur">مقامات</a>
    <a href="#gallery" data-lang="en">Gallery</a><a href="#gallery" data-lang="ur">تصاویر</a>
    <a href="#booking" data-lang="en">Book Now</a><a href="#booking" data-lang="ur">بکنگ</a>
    <a href="#reviews" data-lang="en">Reviews</a><a href="#reviews" data-lang="ur">آراء</a>
    <button id="langToggle" type="button">اردو / EN</button>
  </nav>
</header>

<div class="hero">
  <div class="hero-inner">
    <span class="eyebrow" data-lang="en">Gilgit-Baltistan, Pakistan</span>
    <span class="eyebrow" data-lang="ur">گلگت بلتستان، پاکستان</span>
    <h1 data-lang="en">Welcome to Astore Valley</h1>
    <h1 data-lang="ur">وادی آستور میں خوش آمدید</h1>
    <p data-lang="en">Jeep rentals, hotels, and everything you need to explore Rama Meadows, Minimarg and Rainbow Lake.</p>
    <p data-lang="ur">جیپ کرایہ، ہوٹلز اور رامہ میڈوز، منی مرگ اور رین بو جھیل کی سیر کے لیے ہر سہولت۔</p>
  </div>
</div>

<!-- ===================== WEATHER WIDGET ===================== -->
<div class="weather-bar">
  <section id="weather">
    <span class="eyebrow" style="color:var(--glacier);margin:0;" data-lang="en">Right now in Astore</span>
    <span class="eyebrow" style="color:var(--glacier);margin:0;" data-lang="ur">آستور کا موجودہ موسم</span>
    <div class="wx-stat"><b id="wxTemp">—</b><span data-lang="en">Temperature</span><span data-lang="ur">درجہ حرارت</span></div>
    <div class="wx-stat"><b id="wxCond">—</b><span data-lang="en">Condition</span><span data-lang="ur">حالت</span></div>
    <div class="wx-stat"><b id="wxWind">—</b><span data-lang="en">Wind</span><span data-lang="ur">ہوا</span></div>
  </section>
</div>

<!-- ===================== MUST VISIT PLACES + SEARCH ===================== -->
<section id="places">
  <span class="eyebrow" data-lang="en">Explore</span><span class="eyebrow" data-lang="ur">سیر کریں</span>
  <h2 data-lang="en" style="margin-bottom:20px;">Must Visit Places</h2>
  <h2 data-lang="ur" style="margin-bottom:20px;">ضرور دیکھنے کی جگہیں</h2>

  <div class="search-row">
    <input type="text" id="placeSearch" placeholder="Search places, e.g. Rama, Minimarg..." aria-label="Search places">
    <button class="chip" data-cat="all" aria-pressed="true">All</button>
    <button class="chip" data-cat="hotel">Hotels</button>
    <button class="chip" data-cat="nature">Nature</button>
  </div>

  <div class="place-grid" id="placeGrid"></div>
</section>

<!-- ===================== MAP ===================== -->
<section id="map-section">
  <span class="eyebrow" data-lang="en">Find your way</span><span class="eyebrow" data-lang="ur">راستہ تلاش کریں</span>
  <h2 style="margin-bottom:16px;" data-lang="en">Explore on the Map</h2>
  <h2 style="margin-bottom:16px;" data-lang="ur">نقشے پر دیکھیں</h2>
  <div id="map"></div>
</section>

<!-- ===================== GALLERY ===================== -->
<section id="gallery">
  <div class="inner">
    <span class="eyebrow" style="color:var(--glacier);">Astore Hub Pro</span>
    <h2 style="margin-bottom:20px;">The Valley, in Pictures</h2>
    <div class="filters" role="group" aria-label="Filter gallery by location">
      <button class="chip" data-filter="all" aria-pressed="true">All</button>
      <button class="chip" data-filter="valley" aria-pressed="false">Astore Valley</button>
      <button class="chip" data-filter="rama" aria-pressed="false">Rama Meadows</button>
      <button class="chip" data-filter="minimarg" aria-pressed="false">Minimarg &amp; Rainbow Lake</button>
    </div>
    <div class="grid" id="ahGrid"></div>
  </div>

  <div class="lightbox" id="ahLightbox" role="dialog" aria-modal="true" aria-label="Photo viewer">
    <button class="lb-btn lb-prev" aria-label="Previous photo">&#8592;</button>
    <figure>
      <img id="ahLbImg" src="" alt="">
      <figcaption><span id="ahLbCaption"></span><span id="ahLbCount"></span></figcaption>
    </figure>
    <button class="lb-btn lb-next" aria-label="Next photo">&#8594;</button>
    <button class="lb-close" aria-label="Close">&times;</button>
  </div>
</section>

<!-- ===================== BOOKING ===================== -->
<section id="booking">
  <span class="eyebrow" data-lang="en">Plan your trip</span><span class="eyebrow" data-lang="ur">اپنا سفر ترتیب دیں</span>
  <h2 style="margin-bottom:18px;" data-lang="en">Book Your Trip</h2>
  <h2 style="margin-bottom:18px;" data-lang="ur">اپنی بکنگ کروائیں</h2>

  <div class="booking-card">
    <label for="bkName" data-lang="en">Full name</label><label for="bkName" data-lang="ur">پورا نام</label>
    <input type="text" id="bkName" placeholder="Your name">
    <span class="field-error" id="errName">Enter your name first.</span>

    <label for="bkPhone" data-lang="en">Phone / WhatsApp</label><label for="bkPhone" data-lang="ur">فون / واٹس ایپ</label>
    <input type="tel" id="bkPhone" placeholder="+92 3XX XXXXXXX">
    <span class="field-error" id="errPhone">Enter a valid phone number.</span>

    <label for="bkType" data-lang="en">Service</label><label for="bkType" data-lang="ur">سروس</label>
    <select id="bkType">
      <option value="Jeep 4x4 Rental">Jeep 4x4 Rental</option>
      <option value="Hotel/Room Booking">Hotel/Room Booking</option>
      <option value="Full Tour Package">Full Tour Package</option>
    </select>

    <label for="bkDate" data-lang="en">Travel date</label><label for="bkDate" data-lang="ur">سفر کی تاریخ</label>
    <input type="date" id="bkDate">

    <label for="bkNotes" data-lang="en">Notes</label><label for="bkNotes" data-lang="ur">تفصیلات</label>
    <textarea id="bkNotes" rows="3" placeholder="Number of people, pickup point, etc."></textarea>

    <button class="btn-primary" id="bkSubmit" type="button" data-lang="en">Send via WhatsApp</button>
    <button class="btn-primary" id="bkSubmitUr" type="button" data-lang="ur">واٹس ایپ پر بھیجیں</button>
  </div>
</section>

<!-- ===================== REVIEWS ===================== -->
<section id="reviews">
  <span class="eyebrow" data-lang="en">Traveler voices</span><span class="eyebrow" data-lang="ur">مسافروں کی رائے</span>
  <h2 style="margin-bottom:18px;" data-lang="en">Reviews</h2>
  <h2 style="margin-bottom:18px;" data-lang="ur">تبصرے</h2>

  <div class="review-list" id="reviewList"></div>

  <div class="review-form">
    <input type="text" id="rvName" placeholder="Your name">
    <select id="rvRating">
      <option value="5">★★★★★ Excellent</option>
      <option value="4">★★★★ Good</option>
      <option value="3">★★★ Average</option>
      <option value="2">★★ Poor</option>
      <option value="1">★ Very poor</option>
    </select>
    <textarea id="rvText" rows="3" placeholder="Share your experience..."></textarea>
    <span class="field-error" id="errReview">Add your name and a short review first.</span>
    <button class="btn-primary" id="rvSubmit" type="button" data-lang="en">Post review</button>
    <button class="btn-primary" id="rvSubmitUr" type="button" data-lang="ur">تبصرہ شامل کریں</button>
  </div>
</section>

<footer>
  <p>Astore Hub Pro | Developed by <strong>PRIMESOLUTIONS</strong></p>
  <p><a href="https://web-hub-code.github.io/Web-hub/">Web-hub</a> &middot; <a href="https://web-hub-code.github.io/PRIMESOLUTIONS/">Prime Solutions</a> &middot; <a href="https://wa.me/923171588489">WhatsApp</a></p>
</footer>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
/* ---------------- LANGUAGE TOGGLE ---------------- */
document.getElementById('langToggle').addEventListener('click', function(){
  var html = document.documentElement;
  html.dir = html.dir === 'rtl' ? 'ltr' : 'rtl';
  html.lang = html.dir === 'rtl' ? 'ur' : 'en';
});

/* ---------------- WEATHER (Open-Meteo, no key needed) ---------------- */
fetch('https://api.open-meteo.com/v1/forecast?latitude=35.37&longitude=74.9&current=temperature_2m,wind_speed_10m,weather_code&timezone=auto')
  .then(function(r){ return r.json(); })
  .then(function(d){
    var c = d.current;
    var codes = {0:'Clear sky',1:'Mainly clear',2:'Partly cloudy',3:'Overcast',45:'Fog',51:'Light drizzle',61:'Light rain',71:'Snow',73:'Snow',75:'Heavy snow',80:'Rain showers',95:'Thunderstorm'};
    document.getElementById('wxTemp').textContent = Math.round(c.temperature_2m) + '°C';
    document.getElementById('wxCond').textContent = codes[c.weather_code] || 'Mountain weather';
    document.getElementById('wxWind').textContent = Math.round(c.wind_speed_10m) + ' km/h';
  })
  .catch(function(){
    document.getElementById('wxTemp').textContent = 'N/A';
    document.getElementById('wxCond').textContent = 'Unavailable';
    document.getElementById('wxWind').textContent = 'N/A';
  });

/* ---------------- PLACES + SEARCH/FILTER ---------------- */
var places = [
  {name:'Rama Meadows', cat:'nature', img:'https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800', desc:'Heavenly forests and the gateway to Rama Lake. Perfect for camping and nature lovers.'},
  {name:'Minimarg & Rainbow Lake', cat:'nature', img:'https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800', desc:'Hidden gem of Astore. Requires army clearance and a 4x4 jeep to reach this paradise.'},
  {name:'Astore Valley Guest House', cat:'hotel', img:'https://images.unsplash.com/photo-1501117716987-c8e1ecb210d3?w=800', desc:'Comfortable rooms with valley views, close to the main bazaar.'},
  {name:'Rama Lake Camp Site', cat:'hotel', img:'https://images.unsplash.com/photo-1445308394109-4ec2920981b1?w=800', desc:'Tented camps beside the forest, ideal for an overnight stay near the lake.'}
];
var grid = document.getElementById('placeGrid');
var searchInput = document.getElementById('placeSearch');
var catChips = document.querySelectorAll('#places .chip');
var activeCat = 'all';

function renderPlaces(){
  var q = searchInput.value.trim().toLowerCase();
  var filtered = places.filter(function(p){
    var matchesCat = activeCat === 'all' || p.cat === activeCat;
    var matchesQ = !q || p.name.toLowerCase().indexOf(q) !== -1;
    return matchesCat && matchesQ;
  });
  grid.innerHTML = filtered.length ? '' : '<p style="color:#7a8079;">No places match your search.</p>';
  filtered.forEach(function(p){
    var card = document.createElement('div');
    card.className = 'place-card';
    card.innerHTML = '<img src="'+p.img+'" alt="'+p.name+'"><div class="body"><h3>'+p.name+'</h3><p>'+p.desc+'</p></div>';
    grid.appendChild(card);
  });
}
searchInput.addEventListener('input', renderPlaces);
catChips.forEach(function(chip){
  chip.addEventListener('click', function(){
    catChips.forEach(function(c){ c.setAttribute('aria-pressed','false'); });
    chip.setAttribute('aria-pressed','true');
    activeCat = chip.dataset.cat;
    renderPlaces();
  });
});
renderPlaces();

/* ---------------- MAP ---------------- */
var map = L.map('map').setView([35.37, 74.9], 10);
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
  attribution: '&copy; OpenStreetMap contributors'
}).addTo(map);
var markers = [
  {name:'Astore Town', lat:35.3667, lng:74.9, note:'Main town and starting point.'},
  {name:'Rama Meadows', lat:35.2989, lng:74.8494, note:'Forest meadows and gateway to Rama Lake.'},
  {name:'Rama Lake', lat:35.2833, lng:74.85, note:'Alpine lake reached via jeep track and short hike.'},
  {name:'Minimarg', lat:35.0, lng:74.8, note:'Requires army clearance and a 4x4 jeep.'}
];
markers.forEach(function(m){
  L.marker([m.lat, m.lng]).addTo(map).bindPopup('<strong>'+m.name+'</strong><br>'+m.note);
});

/* ---------------- GALLERY ---------------- */
(function(){
  var ahPhotos = [
    { src: "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=1200", cat: "valley", caption: "Astore Valley at golden hour", size: "wide" },
    { src: "https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=1200", cat: "rama", caption: "Rama Meadows pine forest", size: "tall" },
    { src: "https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=1200", cat: "minimarg", caption: "The track toward Minimarg", size: "" },
    { src: "https://images.unsplash.com/photo-1454496522488-7a8e488e8606?w=1200", cat: "rama", caption: "Camping ground near Rama Lake", size: "" },
    { src: "https://images.unsplash.com/photo-1519681393784-d120267933ba?w=1200", cat: "valley", caption: "River cutting through the valley floor", size: "" },
    { src: "https://images.unsplash.com/photo-1483728642387-6c3bdd6c93e5?w=1200", cat: "minimarg", caption: "Rainbow Lake, a hidden gem", size: "tall" },
    { src: "https://images.unsplash.com/photo-1508264165352-258db2ebd59b?w=1200", cat: "valley", caption: "Sunrise over the peaks", size: "wide" },
    { src: "https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=1200", cat: "rama", caption: "Alpine wildflowers along the trail", size: "" }
  ];
  var grid2 = document.getElementById('ahGrid');
  var chips2 = document.querySelectorAll('#gallery .filters .chip');
  var lb = document.getElementById('ahLightbox');
  var lbImg = document.getElementById('ahLbImg');
  var lbCaption = document.getElementById('ahLbCaption');
  var lbCount = document.getElementById('ahLbCount');
  var currentIndex = 0, visible = ahPhotos.slice();

  function labelFor(cat){ return cat==='valley'?'Astore Valley':cat==='rama'?'Rama Meadows':'Minimarg'; }
  function render(filter){
    visible = filter==='all' ? ahPhotos.slice() : ahPhotos.filter(function(p){ return p.cat===filter; });
    grid2.innerHTML = '';
    visible.forEach(function(photo, i){
      var btn = document.createElement('button');
      btn.className = 'g-item ' + (photo.size||'');
      btn.setAttribute('aria-label','View photo: '+photo.caption);
      btn.innerHTML = '<img src="'+photo.src+'" alt="'+photo.caption+'" loading="lazy"><span class="g-tag">'+labelFor(photo.cat)+'</span>';
      btn.addEventListener('click', function(){ openLightbox(i); });
      grid2.appendChild(btn);
    });
  }
  chips2.forEach(function(chip){
    chip.addEventListener('click', function(){
      chips2.forEach(function(c){ c.setAttribute('aria-pressed','false'); });
      chip.setAttribute('aria-pressed','true');
      render(chip.dataset.filter);
    });
  });
  function openLightbox(i){ currentIndex=i; updateLightbox(); lb.classList.add('open'); }
  function updateLightbox(){
    var p = visible[currentIndex];
    lbImg.src = p.src; lbImg.alt = p.caption;
    lbCaption.textContent = p.caption;
    lbCount.textContent = (currentIndex+1)+' / '+visible.length;
  }
  function closeLightbox(){ lb.classList.remove('open'); }
  function step(dir){ currentIndex=(currentIndex+dir+visible.length)%visible.length; updateLightbox(); }
  document.querySelector('.lb-close').addEventListener('click', closeLightbox);
  document.querySelector('.lb-prev').addEventListener('click', function(){ step(-1); });
  document.querySelector('.lb-next').addEventListener('click', function(){ step(1); });
  lb.addEventListener('click', function(e){ if(e.target===lb) closeLightbox(); });
  document.addEventListener('keydown', function(e){
    if(!lb.classList.contains('open')) return;
    if(e.key==='Escape') closeLightbox();
    if(e.key==='ArrowRight') step(1);
    if(e.key==='ArrowLeft') step(-1);
  });
  render('all');
})();

/* ---------------- BOOKING (WhatsApp handoff) ---------------- */
function submitBooking(){
  var name = document.getElementById('bkName').value.trim();
  var phone = document.getElementById('bkPhone').value.trim();
  var errName = document.getElementById('errName');
  var errPhone = document.getElementById('errPhone');
  errName.style.display = name ? 'none' : 'block';
  errPhone.style.display = phone.length >= 7 ? 'none' : 'block';
  if(!name || phone.length < 7) return;

  var type = document.getElementById('bkType').value;
  var date = document.getElementById('bkDate').value || 'not specified';
  var notes = document.getElementById('bkNotes').value.trim() || 'none';
  var msg = 'New booking request\nName: '+name+'\nPhone: '+phone+'\nService: '+type+'\nDate: '+date+'\nNotes: '+notes;
  window.open('https://wa.me/923171588489?text='+encodeURIComponent(msg), '_blank');
}
document.getElementById('bkSubmit').addEventListener('click', submitBooking);
document.getElementById('bkSubmitUr').addEventListener('click', submitBooking);

/* ---------------- REVIEWS (saved in this browser via localStorage) ---------------- */
var reviewList = document.getElementById('reviewList');
function loadReviews(){
  var stored = [];
  try { stored = JSON.parse(localStorage.getItem('astoreReviews') || '[]'); } catch(e){ stored = []; }
  var seed = [
    {name:'Bilal K.', rating:5, text:'Rama Meadows took my breath away. Jeep pickup was on time.'},
    {name:'Sana A.', rating:4, text:'Minimarg trip needed patience for the army clearance but totally worth it.'}
  ];
  var all = seed.concat(stored);
  reviewList.innerHTML = '';
  all.forEach(function(r){
    var card = document.createElement('div');
    card.className = 'review-card';
    var stars = '★'.repeat(r.rating) + '☆'.repeat(5 - r.rating);
    card.innerHTML = '<div class="stars">'+stars+'</div><p style="margin:6px 0;">'+r.text+'</p><div class="meta">'+r.name+'</div>';
    reviewList.appendChild(card);
  });
}
function submitReview(){
  var name = document.getElementById('rvName').value.trim();
  var text = document.getElementById('rvText').value.trim();
  var err = document.getElementById('errReview');
  if(!name || !text){ err.style.display = 'block'; return; }
  err.style.display = 'none';
  var rating = parseInt(document.getElementById('rvRating').value, 10);
  var stored = [];
  try { stored = JSON.parse(localStorage.getItem('astoreReviews') || '[]'); } catch(e){ stored = []; }
  stored.push({name:name, rating:rating, text:text});
  localStorage.setItem('astoreReviews', JSON.stringify(stored));
  document.getElementById('rvName').value = '';
  document.getElementById('rvText').value = '';
  loadReviews();
}
document.getElementById('rvSubmit').addEventListener('click', submitReview);
document.getElementById('rvSubmitUr').addEventListener('click', submitReview);
loadReviews();
</script>
</body>
</html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Hub Pro | Developed by PRIMESOLUTIONS</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu:wght@400;700&family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">
    
    <style>
        :root { 
            --primary: #10b981; 
            --accent: #fbbf24; 
            --bg: #020617; 
            --card: rgba(255, 255, 255, 0.05); 
            --text: #f8fafc; 
            --glass: blur(15px);
        }

        * { margin:0; padding:0; box-sizing:border-box; font-family:'Plus Jakarta Sans',sans-serif; -webkit-tap-highlight-color: transparent; }
        .urdu-font { font-family: 'Noto Nastaliq Urdu', serif !important; line-height: 2.5; direction: rtl; }
        
        body { background: var(--bg); color: var(--text); background-image: radial-gradient(circle at 50% -20%, #1e293b, #020617); min-height: 100vh; overflow-x: hidden; }

        /* --- Header --- */
        header { position: sticky; top: 0; z-index: 1000; padding: 15px 20px; background: rgba(2, 6, 23, 0.9); backdrop-filter: var(--glass); display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .logo { font-weight: 800; font-size: 1.2rem; letter-spacing: -0.5px; }
        .lang-btn { background: var(--primary); color: white; border: none; padding: 6px 14px; border-radius: 10px; font-weight: 700; font-size: 0.75rem; cursor: pointer; }

        /* --- Page Transitions --- */
        .page { display: none; animation: fadeIn 0.4s ease; padding-bottom: 100px; }
        .page.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        /* --- Hero / Gallery --- */
        .hero-box { margin: 15px; border-radius: 25px; overflow: hidden; height: 28vh; position: relative; box-shadow: 0 15px 35px rgba(0,0,0,0.5); }
        .hero-box img { width: 100%; height: 100%; object-fit: cover; }
        .hero-label { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.8)); padding: 20px; font-weight: 800; }

        /* --- Grid & Cards --- */
        .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; padding: 0 20px; }
        .feature-card { background: var(--card); border-radius: 20px; padding: 20px; border: 1px solid rgba(255,255,255,0.05); text-align: center; transition: 0.3s; }
        .feature-card i { font-size: 1.8rem; color: var(--primary); margin-bottom: 10px; }
        .feature-card h4 { font-size: 0.8rem; font-weight: 700; }

        .section-title { padding: 25px 20px 15px; font-weight: 800; font-size: 1.1rem; display: flex; align-items: center; gap: 10px; }

        /* --- Destinations List --- */
        .place-card { background: var(--card); margin: 0 20px 15px; border-radius: 20px; overflow: hidden; border: 1px solid rgba(255,255,255,0.05); }
        .place-img { height: 150px; width: 100%; object-fit: cover; }
        .place-info { padding: 15px; }
        .place-info h3 { font-size: 1rem; color: var(--accent); margin-bottom: 5px; }
        .place-info p { font-size: 0.8rem; opacity: 0.7; line-height: 1.5; }

        /* --- Forms --- */
        .form-group { padding: 0 20px; }
        input, select, textarea { width: 100%; padding: 14px; margin-bottom: 15px; border-radius: 12px; border: 1px solid rgba(255,255,255,0.1); background: rgba(0,0,0,0.3); color: white; font-size: 0.9rem; }
        .main-btn { background: var(--primary); color: white; width: 100%; padding: 16px; border-radius: 15px; border: none; font-weight: 800; font-size: 1rem; cursor: pointer; box-shadow: 0 8px 20px rgba(16, 185, 129, 0.2); }

        /* --- Branding --- */
        .branding-card { margin: 20px; background: rgba(16, 185, 129, 0.05); border: 1px dashed var(--primary); border-radius: 20px; padding: 20px; text-align: center; }
        .brand-link { color: var(--text); text-decoration: none; font-weight: 800; display: inline-flex; align-items: center; gap: 6px; margin: 5px 0; }
        .brand-link i { color: var(--primary); font-size: 0.8rem; }

        /* --- Navigation Bar --- */
        .nav-bar { position: fixed; bottom: 20px; left: 20px; right: 20px; background: rgba(255,255,255,0.08); backdrop-filter: var(--glass); display: flex; justify-content: space-around; padding: 15px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.1); z-index: 1000; }
        .nav-item { color: rgba(255,255,255,0.4); font-size: 1.3rem; transition: 0.3s; cursor: pointer; }
        .nav-item.active { color: var(--primary); transform: translateY(-5px); }

        /* --- SOS --- */
        .sos-btn { position: fixed; bottom: 100px; right: 20px; background: #ef4444; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; box-shadow: 0 10px 20px rgba(239, 68, 68, 0.3); z-index: 999; text-decoration: none; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
    </style>
</head>
<body>

<header>
    <div class="logo">ASTORE <span style="color:var(--primary)">HUB PRO</span></div>
    <button class="lang-btn" onclick="toggleLanguage()">اردو</button>
</header>

<div id="home" class="page active">
    <div class="hero-box">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800" alt="Astore">
        <div class="hero-label"><span id="h-welcome">Welcome to Astore Valley</span></div>
    </div>

    <div class="section-title"><i class="fa-solid fa-star"></i> <span id="h-services">Top Services</span></div>
    <div class="grid">
        <div class="feature-card" onclick="showPage('booking')"><i class="fa-solid fa-truck-monster"></i><h4>Jeep 4x4</h4></div>
        <div class="feature-card" onclick="showPage('booking')"><i class="fa-solid fa-hotel"></i><h4>Hotels</h4></div>
        <div class="feature-card" onclick="showPage('explore')"><i class="fa-solid fa-map-marked-alt"></i><h4>Places</h4></div>
        <div class="feature-card" onclick="showPage('about')"><i class="fa-solid fa-id-badge"></i><h4>Prime Dev</h4></div>
    </div>

    <div class="branding-card">
        <p id="h-managed" style="font-size: 0.75rem; opacity: 0.6; margin-bottom: 5px;">Supervised & Developed By</p>
        <a href="https://web-hub-code.github.io/Web-hub/" target="_blank" class="brand-link">Web-hub<i class="fa-solid fa-external-link-alt"></i></a><br>
        <a href="https://web-hub-code.github.io/PRIMESOLUTIONS/" target="_blank" class="brand-link">Prime Solutions <i class="fa-solid fa-external-link-alt"></i></a>
    </div>
</div>

<div id="explore" class="page">
    <div class="section-title"><i class="fa-solid fa-compass"></i> <span id="e-title">Must Visit Places</span></div>
    
    <div class="place-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=800" class="place-img">
        <div class="place-info">
            <h3>Rama Meadows</h3>
            <p id="e-rama">Heavenly forests and the gateway to Rama Lake. Perfect for camping and nature lovers.</p>
        </div>
    </div>

    <div class="place-card">
        <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=800" class="place-img">
        <div class="place-info">
            <h3>Minimarg & Rainbow Lake</h3>
            <p id="e-mini">Hidden gem of Astore. Requires army clearance and a 4x4 jeep to reach this paradise.</p>
        </div>
    </div>
</div>

<div id="booking" class="page">
    <div class="section-title"><i class="fa-solid fa-calendar-check"></i> <span id="b-title">Book Your Trip</span></div>
    <div class="form-group">
        <input type="text" id="custName" placeholder="Enter Full Name" required>
        <select id="svcType">
            <option value="4x4 Jeep Rental">Jeep 4x4 Rental</option>
            <option value="Hotel Booking">Hotel/Room Booking</option>
            <option value="Full Tour Package">Full Tour Package</option>
        </select>
        <input type="date" id="tripDate" required>
        <textarea id="extraReq" rows="3" placeholder="Any extra requirements?"></textarea>
        <button class="main-btn" onclick="sendWhatsApp()"><i class="fa-brands fa-whatsapp"></i> <span id="b-btn">Book Now</span></button>
    </div>
</div>

<div id="about" class="page">
    <div class="section-title"><i class="fa-solid fa-code"></i> <span id="a-title">Developer Details</span></div>
    <div class="card" style="margin: 0 20px; padding: 25px; background: var(--card); border-radius: 25px; text-align: center;">
        <h3 style="color:var(--primary)">Prime Solutions</h3>
        <p style="font-size: 0.85rem; opacity: 0.7; margin: 15px 0;">Founder of Prime Solutions. Professional Web & App Developer specialized in creating high-performance digital hubs.</p>
        <div style="display: flex; justify-content: center; gap: 20px; font-size: 1.5rem; margin-top: 10px;">
            <a href="https://web-hub-code.github.io/Web-hub/" target="_blank" style="color:white"><i class="fa-solid fa-globe"></i></a>
            <a href="https://wa.me/923171588489" style="color:var(--primary)"><i class="fa-brands fa-whatsapp"></i></a>
        </div>
    </div>
</div>

<div class="nav-bar">
    <div class="nav-item active" onclick="showPage('home')"><i class="fa-solid fa-house"></i></div>
    <div class="nav-item" onclick="showPage('explore')"><i class="fa-solid fa-mountain-sun"></i></div>
    <div class="nav-item" onclick="showPage('booking')"><i class="fa-solid fa-calendar-day"></i></div>
    <div class="nav-item" onclick="showPage('about')"><i class="fa-solid fa-user-gear"></i></div>
</div>

<a href="tel:923171588489" class="sos-btn"><i class="fa-solid fa-phone-volume"></i></a>

<script>
    // Page Management Logic
    function showPage(pageId) {
        document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
        document.getElementById(pageId).classList.add('active');
        
        // Update Nav Icons
        document.querySelectorAll('.nav-item').forEach(nav => nav.classList.remove('active'));
        const index = ['home', 'explore', 'booking', 'about'].indexOf(pageId);
        document.querySelectorAll('.nav-item')[index].classList.add('active');
        
        window.scrollTo(0,0);
        if(navigator.vibrate) navigator.vibrate(30);
    }

    // Language Toggle Logic
    let isUrdu = false;
    function toggleLanguage() {
        isUrdu = !isUrdu;
        const body = document.body;
        const btn = document.querySelector('.lang-btn');
        
        if(isUrdu) {
            body.classList.add('urdu-font');
            btn.innerText = "ENGLISH";
            document.getElementById('h-welcome').innerText = "استور ہب میں خوش آمدید";
            document.getElementById('h-services').innerText = "ہماری سہولیات";
            document.getElementById('h-managed').innerText = "زیرِ نگرانی و تخلیق";
            document.getElementById('e-title').innerText = "مشہور سیاحتی مقامات";
            document.getElementById('b-title').innerText = "بکنگ فارم";
            document.getElementById('b-btn').innerText = "ابھی رابطہ کریں";
            document.getElementById('a-title').innerText = "ڈویلپر کی تفصیلات";
        } else {
            body.classList.remove('urdu-font');
            btn.innerText = "اردو";
            document.getElementById('h-welcome').innerText = "Welcome to Astore Valley";
            document.getElementById('h-services').innerText = "Top Services";
            document.getElementById('h-managed').innerText = "Supervised & Developed By";
            document.getElementById('e-title').innerText = "Must Visit Places";
            document.getElementById('b-title').innerText = "Book Your Trip";
            document.getElementById('b-btn').innerText = "Book Now";
            document.getElementById('a-title').innerText = "Developer Details";
        }
    }

    // Booking Function
    function sendWhatsApp() {
        const name = document.getElementById('custName').value;
        const svc = document.getElementById('svcType').value;
        const date = document.getElementById('tripDate').value;
        const req = document.getElementById('extraReq').value;

        if(!name || !date) {
            alert(isUrdu ? "براہ کرم تمام خانے پُر کریں، سویٹی! 😘" : "Please fill all fields, ! 😘");
            return;
        }

        const message = `*ASTORE HUB PRO BOOKING*\n\n*Name:* ${name}\n*Service:* ${svc}\n*Date:* ${date}\n*Request:* ${req}\n\n_System Generated via Prime Solutions_`;
        window.open(`https://wa.me/923171588489?text=${encodeURIComponent(message)}`);
    }
</script>

</body>
</html>
