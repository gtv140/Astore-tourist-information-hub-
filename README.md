<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Astore Tourist Information Hub | Official Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #042f2e; --accent: #d97706; --bg-light: #f8fafc; --text-main: #334155; }
        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }
        body { font-family: 'Inter', sans-serif; background: var(--bg-light); color: var(--text-main); }

        /* Announcement Bar */
        .top-bar { background: var(--primary); color: white; text-align: center; padding: 8px; font-size: 0.75rem; letter-spacing: 1px; }

        /* Sticky Navigation */
        nav { background: white; padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .logo { font-weight: 800; font-size: 1.4rem; color: var(--primary); text-decoration: none; }
        .nav-links { display: none; } /* Mobile first: hidden */

        /* Hero with Parallax Feel */
        .hero { 
            height: 65vh; background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1596395819057-e37f55a8516b?q=80&w=1000');
            background-size: cover; background-position: center; display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; padding: 20px;
        }
        .hero h1 { font-size: 2.8rem; margin-bottom: 15px; line-height: 1; }
        .hero p { font-size: 1.1rem; max-width: 400px; opacity: 0.9; }

        .container { width: 100%; max-width: 600px; margin: 0 auto; padding: 40px 15px; }

        /* History Section */
        .history-card { background: white; padding: 30px; border-radius: 25px; margin-bottom: 40px; border-top: 6px solid var(--accent); box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
        .history-card h2 { color: var(--primary); margin-bottom: 15px; }
        .history-card p { font-size: 0.95rem; text-align: justify; color: #475569; }

        /* Information Grid */
        .info-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 40px; }
        .info-item { background: white; padding: 20px; border-radius: 20px; text-align: center; box-shadow: 0 4px 6px rgba(0,0,0,0.03); }
        .info-item i { font-size: 1.5rem; color: var(--accent); margin-bottom: 10px; }
        .info-item h4 { font-size: 0.8rem; text-transform: uppercase; color: #94a3b8; }
        .info-item p { font-weight: bold; color: var(--primary); }

        /* Packages Table */
        .package-list { background: #134e4a; color: white; padding: 30px 20px; border-radius: 30px; margin-bottom: 40px; }
        .package-row { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.1); font-size: 0.9rem; }
        .package-row:last-child { border: none; }

        /* Culture Section */
        .culture-box { background: #fffbeb; padding: 25px; border-radius: 25px; border: 1px dashed var(--accent); margin-bottom: 40px; }
        .culture-box h3 { color: #92400e; margin-bottom: 10px; }

        /* Emergency Contacts */
        .emergency { background: #fee2e2; padding: 20px; border-radius: 20px; color: #991b1b; }
        .emergency h4 { margin-bottom: 10px; display: flex; align-items: center; gap: 10px; }

        /* Fixed Booking Bar for Mobile */
        .mobile-cta { position: fixed; bottom: 0; left: 0; width: 100%; background: white; padding: 15px; display: flex; gap: 10px; box-shadow: 0 -5px 20px rgba(0,0,0,0.1); z-index: 999; }
        .btn-call { flex: 1; background: #e2e8f0; color: var(--primary); padding: 12px; border-radius: 12px; text-align: center; text-decoration: none; font-weight: bold; }
        .btn-wa { flex: 2; background: #25d366; color: white; padding: 12px; border-radius: 12px; text-align: center; text-decoration: none; font-weight: bold; display: flex; align-items: center; justify-content: center; gap: 8px; }

        footer { text-align: center; padding: 60px 20px 100px; background: white; font-size: 0.8rem; color: #64748b; }
    </style>
</head>
<body>

<div class="top-bar">WELCOME TO THE LAND OF MOUNTAINS</div>

<nav>
    <a href="#" class="logo">ASTORE HUB</a>
    <a href="tel:+923171588489" style="color: var(--primary); font-size: 1.2rem;"><i class="fas fa-phone"></i></a>
</nav>

<section class="hero">
    <h1>Discover Astore Valley</h1>
    <p>Official Information & Premium Jeep Services</p>
    <div style="margin-top: 20px;">
        <i class="fas fa-star" style="color:var(--accent)"></i>
        <i class="fas fa-star" style="color:var(--accent)"></i>
        <i class="fas fa-star" style="color:var(--accent)"></i>
        <i class="fas fa-star" style="color:var(--accent)"></i>
        <i class="fas fa-star" style="color:var(--accent)"></i>
        <span style="display:block; font-size: 0.8rem;">Trusted by 500+ Travelers</span>
    </div>
</section>

<div class="container">

    <div class="history-card">
        <h2><i class="fas fa-landmark"></i> The History</h2>
        <p>Astore ki tareekh bohot purani hai. Ye purane zamane mein Gilgit aur Srinagar ke darmiyan aik ahem tijarati rasta (Silk Route link) tha. British raj ke dauran iski jagah bohot ahem thi kyunke ye "Burzil Pass" ke zariye Kashmir se juda tha. Aaj ye apni sakhawat aur Nanga Parbat ke haseen manazir ki wajah se jana jata hai.</p>
    </div>

    <div class="info-grid">
        <div class="info-item"><i class="fas fa-cloud-sun"></i><h4>Mausam</h4><p>May-Oct</p></div>
        <div class="info-item"><i class="fas fa-road"></i><h4>Access</h4><p>4x4 Jeep</p></div>
        <div class="info-item"><i class="fas fa-map-pin"></i><h4>Dist. Gilgit</h4><p>110 KM</p></div>
        <div class="info-item"><i class="fas fa-id-card"></i><h4>NOC</h4><p>Required</p></div>
    </div>

    <h2 style="margin-bottom: 20px; color: var(--primary);">Main Attractions</h2>
    
    <div style="margin-bottom: 40px;">
        <div style="background: white; border-radius: 20px; margin-bottom: 20px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
            <img src="https://images.unsplash.com/photo-1533130061792-64b345e4e833" style="width: 100%; height: 200px; object-fit: cover;">
            <div style="padding: 20px;">
                <h3>Minimarg & Rainbow Lake</h3>
                <p style="font-size: 0.9rem; margin: 10px 0;">Ye Astore ka sab se haseen aur pur-asrar hissa hai. Rainbow lake ka pani dunya mein mashhoor hai.</p>
            </div>
        </div>

        <div style="background: white; border-radius: 20px; margin-bottom: 20px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
            <img src="https://images.unsplash.com/photo-1627896157734-4d7d4388f28b" style="width: 100%; height: 200px; object-fit: cover;">
            <div style="padding: 20px;">
                <h3>Rama Meadows</h3>
                <p style="font-size: 0.9rem; margin: 10px 0;">Nanga Parbat ka itna qareebi aur haseen view aapko sirf Rama mein milega.</p>
            </div>
        </div>
    </div>

    <div class="culture-box">
        <h3><i class="fas fa-utensils"></i> Local Taste & Culture</h3>
        <p style="font-size: 0.9rem;">Astore ke log bohot mehman nawaz hain. Yahan ka **"Shapik"** (Local bread) aur desi makhni chai bohot mashhoor hai. Tour par aayein toh yahan ka local pattu (hand-woven wool) zaroor dekhein.</p>
    </div>

    <div class="package-list">
        <h3 style="margin-bottom: 20px; color: var(--accent);">Standard Jeep Rates</h3>
        <div class="package-row"><span>Rama Meadows (Return)</span><b>Rs. 8,000</b></div>
        <div class="package-row"><span>Minimarg & Rainbow Lake</span><b>Rs. 14,000</b></div>
        <div class="package-row"><span>Deosai Plains Crossing</span><b>Rs. 18,000</b></div>
        <div class="package-row"><span>Tarashing (Nanga Parbat Base)</span><b>Rs. 10,000</b></div>
        <p style="font-size: 0.7rem; margin-top: 15px; opacity: 0.7;">*Rates can vary based on fuel prices and seasonal demand.</p>
    </div>

    <div class="emergency">
        <h4><i class="fas fa-exclamation-triangle"></i> Emergency Contacts</h4>
        <div style="font-size: 0.85rem; display: flex; flex-direction: column; gap: 5px;">
            <p>🚑 DHQ Hospital Astore: 05817-920100</p>
            <p>👮 Police Station: 05817-920101</p>
            <p>🚜 Road Assistance: +92 317 1588489</p>
        </div>
    </div>

</div>

<div class="mobile-cta">
    <a href="tel:+923171588489" class="btn-call"><i class="fas fa-phone-alt"></i> Call</a>
    <a href="https://wa.me/923171588489" class="btn-wa"><i class="fab fa-whatsapp"></i> Book via WhatsApp</a>
</div>

<footer>
    <p><b>Astore Tourist Information Hub</b></p>
    <p>Preserving Culture, Promoting Tourism.</p>
    <p style="margin-top: 15px;">© 2026 Official Portal | Gilgit-Baltistan</p>
</footer>

</body>
</html>
