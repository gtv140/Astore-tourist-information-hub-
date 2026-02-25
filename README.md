<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | Official Tourist Guide</title>
    <style>
        :root { --primary: #1b4332; --secondary: #2d6a4f; --accent: #95d5b2; --light: #f8f9fa; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; background: var(--light); color: #333; scroll-behavior: smooth; }
        
        /* Navigation */
        nav { background: var(--primary); padding: 15px; position: sticky; top: 0; z-index: 1000; display: flex; justify-content: space-around; flex-wrap: wrap; box-shadow: 0 2px 10px rgba(0,0,0,0.2); }
        nav a { color: white; text-decoration: none; font-weight: bold; margin: 5px 15px; }

        /* Hero Section */
        header { background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1589308454676-40742d45903b?q=80&w=1000') no-repeat center center/cover; height: 60vh; color: white; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; padding: 20px; }
        header h1 { font-size: 3rem; margin: 0; }

        /* Grid System */
        .container { max-width: 1200px; margin: auto; padding: 40px 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .card { background: white; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: 0.3s; border-bottom: 4px solid var(--secondary); }
        .card:hover { transform: translateY(-10px); }
        .card-content { padding: 20px; }
        .tag { background: var(--secondary); color: white; padding: 4px 10px; border-radius: 5px; font-size: 12px; text-transform: uppercase; }

        /* Table Style */
        .table-container { overflow-x: auto; background: white; padding: 20px; border-radius: 12px; margin-top: 20px; }
        table { width: 100%; border-collapse: collapse; text-align: left; }
        th, td { padding: 15px; border-bottom: 1px solid #ddd; }
        th { background: var(--secondary); color: white; }

        /* Contact & WhatsApp */
        .whatsapp-float { position: fixed; bottom: 20px; right: 20px; background: #25d366; color: white; padding: 15px 25px; border-radius: 50px; text-decoration: none; font-weight: bold; box-shadow: 0 4px 10px rgba(0,0,0,0.3); z-index: 2000; }
        .contact-box { background: var(--primary); color: white; padding: 50px 20px; text-align: center; border-radius: 15px; margin-top: 40px; }
        .call-btn { background: white; color: var(--primary); padding: 12px 30px; border-radius: 8px; text-decoration: none; display: inline-block; margin-top: 20px; font-weight: bold; }

        footer { text-align: center; padding: 30px; color: #777; font-size: 14px; }
    </style>
</head>
<body>

<nav>
    <a href="#home">Home</a>
    <a href="#destinations">Places</a>
    <a href="#hotels">Hotels & Rates</a>
    <a href="#itinerary">Road Updates</a>
    <a href="#contact">Contact Support</a>
</nav>

<header id="home">
    <h1>Astore Tourist Hub</h1>
    <p>Get Real-time Information & Local Guides for Your Trip</p>
    <a href="tel:+923171588489" class="call-btn" style="background: #25d366; color: white; border: none;">Call Now for Booking</a>
</header>

<div class="container" id="destinations">
    <h2 style="text-align: center; margin-bottom: 40px;">Top Places to Visit</h2>
    <div class="grid">
        <div class="card">
            <div class="card-content">
                <span class="tag">Highlight</span>
                <h3>Rama Meadows & Lake</h3>
                <p>Nanga Parbat ka perfect view aur ghane jungle. Astore se sirf 11km door.</p>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <span class="tag">Border Area</span>
                <h3>Minimarg & Rainbow Lake</h3>
                <p>Jannat-nazeer jagah. Rainbow Lake ka pani rang badalta hai. (NOC Required)</p>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <span class="tag">High Plateau</span>
                <h3>Deosai Plains (Chillum)</h3>
                <p>Dunya ka doosra buland tareen maidan. Sheosar Lake aur brown bears ke liye mashhoor.</p>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <span class="tag">Base Camp</span>
                <h3>Rupal Valley</h3>
                <p>Tarashing se hiking shuru hoti hai. Nanga Parbat ka "Rupal Face" yahan se nazar aata hai.</p>
            </div>
        </div>
    </div>
</div>

<div class="container" id="hotels">
    <h2 style="text-align: center;">Estimated Rates (Hotels & Jeeps)</h2>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>Service Type</th>
                    <th>Average Rate (PKR)</th>
                    <th>Notes</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Standard Hotel Room</td>
                    <td>4,000 - 6,000</td>
                    <td>Astore City / Rama</td>
                </tr>
                <tr>
                    <td>Camping (Per Night)</td>
                    <td>1,500 - 2,500</td>
                    <td>Rama / Rainbow Lake</td>
                </tr>
                <tr>
                    <td>Jeep Rent (4x4)</td>
                    <td>10,000 - 15,000</td>
                    <td>Full Day for Deosai/Minimarg</td>
                </tr>
                <tr>
                    <td>Local Guide</td>
                    <td>2,000 - 3,000</td>
                    <td>Daily Basis</td>
                </tr>
            </tbody>
        </table>
    </div>
</div>

<div class="container" id="itinerary">
    <div style="background: #fff; padding: 30px; border-radius: 12px; border-left: 8px solid #f39c12;">
        <h3>⚠️ Important Road Updates</h3>
        <ul>
            <li><strong>Burzil Pass:</strong> Sirf June se October tak khula rehta hai.</li>
            <li><strong>Jeep Rental:</strong> Minimarg ke liye sirf Astore ki local jeeps ko permission milti hai.</li>
            <li><strong>Fuel:</strong> Astore city mein akhri Petrol Pump hai, aage fuel nahi milta.</li>
        </ul>
    </div>
</div>

<div class="container" id="contact">
    <div class="contact-box">
        <h2>24/7 Information Desk</h2>
        <p>Aapko NOC chahiye, Jeep rent karni hai ya Hotel booking? Humein call karein.</p>
        <p style="font-size: 24px;">📞 +92 317 1588489</p>
        <a href="tel:+923171588489" class="call-btn">Contact Agent Now</a>
        <br><br>
        <p>Email: info@astorehub.com</p>
    </div>
</div>

<a href="https://wa.me/923171588489?text=Hi, I am planning a trip to Astore. Please guide me." class="whatsapp-float" target="_blank">
    💬 WhatsApp Hub
</a>

<footer>
    <p>&copy; 2026 Astore Tourist Information Hub. All Rights Reserved.</p>
    <p>Powered by Local Community of Astore</p>
</footer>

</body>
</html>
