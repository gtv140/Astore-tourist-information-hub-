<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Explore Astore - Tourist Information Hub</title>
    <style>
        :root { --primary: #2c5f2d; --accent: #97bc62; --light: #f4f4f4; }
        body { font-family: 'Segoe UI', sans-serif; margin: 0; line-height: 1.6; color: #333; }
        header { background: var(--primary); color: white; padding: 2rem; text-align: center; }
        nav { background: #333; color: white; padding: 10px; text-align: center; position: sticky; top: 0; }
        nav a { color: white; margin: 0 15px; text-decoration: none; font-weight: bold; }
        .hero { background: #e0e0e0; padding: 60px 20px; text-align: center; }
        .container { max-width: 1100px; margin: auto; padding: 20px; }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .card { border: 1px solid #ddd; border-radius: 8px; overflow: hidden; background: white; transition: 0.3s; }
        .card:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        .card img { width: 100%; height: 200px; object-fit: cover; background: #ccc; }
        .card-content { padding: 15px; }
        .tag { background: var(--accent); color: white; padding: 3px 8px; border-radius: 4px; font-size: 12px; }
        
        footer { background: #222; color: white; text-align: center; padding: 20px; margin-top: 40px; }
    </style>
</head>
<body>

<header>
    <h1>Astore Tourist Information Hub</h1>
    <p>The Gateway to Deosai and the Hidden Gems of Gilgit-Baltistan</p>
</header>

<nav>
    <a href="#destinations">Destinations</a>
    <a href="#itinerary">Plans</a>
    <a href="#contact">Emergency Contacts</a>
</nav>

<div class="container" id="destinations">
    <h2 style="text-align: center; border-bottom: 2px solid var(--primary); padding-bottom: 10px;">Explore All Places in Astore</h2>
    
    <div class="grid">
        <div class="card">
            <div class="card-content">
                <span class="tag">Most Popular</span>
                <h3>Rama Meadows & Lake</h3>
                <p>Astore se 30 mins ki drive par. Pine trees aur Nanga Parbat ke view ke liye best jagah.</p>
            </div>
        </div>

        <div class="card">
            <div class="card-content">
                <span class="tag">Border Area</span>
                <h3>Minimarg & Rainbow Lake</h3>
                <p>Burzil Pass ke zariye rasta jata hai. Rainbow Lake apni khoobsurti ki wajah se mashhoor hai.</p>
            </div>
        </div>

        <div class="card">
            <div class="card-content">
                <span class="tag">High Altitude</span>
                <h3>Deosai (Chillum Gate)</h3>
                <p>Astore side se Deosai enter hone ka rasta Chillum se hai. Sheosar Lake raste mein aati hai.</p>
            </div>
        </div>

        <div class="card">
            <div class="card-content">
                <span class="tag">Base Camp</span>
                <h3>Rupal Valley (Nanga Parbat)</h3>
                <p>Tarashing village se hiking shuru hoti hai Nanga Parbat ke Rupal Face ki taraf.</p>
            </div>
        </div>

        <div class="card">
            <div class="card-content">
                <span class="tag">Hidden Gem</span>
                <h3>Parishing Valley</h3>
                <p>Kam log jate hain magar ye valley apni greenery aur waterfalls ke liye jani jati hai.</p>
            </div>
        </div>

        <div class="card">
            <div class="card-content">
                <span class="tag">Skiing Hub</span>
                <h3>Rattu Valley</h3>
                <p>Sardiyon mein skiing ke liye mashhoor aur garmiyon mein sukoon deh maqam.</p>
            </div>
        </div>
        
        <div class="card">
            <div class="card-content">
                <span class="tag">Trekking</span>
                <h3>Kamri Top / Pass</h3>
                <p>Purana rasta jo Astore ko Neelum Valley (Kashmir) se milata hai.</p>
            </div>
        </div>
    </div>
</div>

<div class="container" id="itinerary" style="background: #f9f9f9; padding: 40px; border-radius: 10px;">
    <h3>Important Travel Tips for Astore:</h3>
    <ul>
        <li>**Roads:** Astore-Gilgit road aksar landslide ki wajah se band hoti hai, update lekar niklen.</li>
        <li>**4x4 Required:** Minimarg aur Deosai ke liye 4x4 Jeep zaroori hai.</li>
        <li>**NOC:** Minimarg jane ke liye Army se NOC/Permission leni parti hai.</li>
    </ul>
</div>

<footer id="contact">
    <p>Astore Tourist Information Hub &copy; 2026</p>
    <p>Helping you explore the heart of Gilgit-Baltistan.</p>
</footer>

</body>
</html>
