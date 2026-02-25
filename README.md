<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astore Hub | GB Ultimate Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@400;700&family=Outfit:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"/>
    <style>
        :root { --primary: #00d2ff; --bg: #010409; --border: rgba(255, 255, 255, 0.1); }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Outfit', sans-serif; background: var(--bg); color: #fff; overflow-x: hidden; }

        /* Hero Image */
        .hero {
            height: 70vh; width: 100%;
            background: linear-gradient(rgba(0,0,0,0.5), var(--bg)), 
                        url('https://loremflickr.com/1280/720/mountains,pakistan') no-repeat center center/cover;
            display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;
        }

        .hero h1 { font-family: 'Unbounded', sans-serif; font-size: 40px; color: var(--primary); }

        /* Destination Grid */
        .dest-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; padding: 20px; max-width: 1200px; margin: 0 auto; }
        
        .dest-card {
            height: 350px; border-radius: 20px; overflow: hidden; position: relative;
            border: 1px solid var(--border); background: #111;
        }
        
        /* High Performance Image Styling */
        .dest-card img { 
            width: 100%; height: 100%; object-fit: cover; 
            display: block; /* Ensures visibility */
        }
        
        .dest-overlay {
            position: absolute; bottom: 0; left: 0; right: 0; padding: 20px;
            background: linear-gradient(transparent, rgba(0,0,0,0.9));
        }

        .dock {
            position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
            background: rgba(0,0,0,0.8); padding: 15px 30px; border-radius: 50px;
            display: flex; gap: 30px; border: 1px solid var(--border);
        }
    </style>
</head>
<body>

    <section class="hero">
        <h1>ASTORE HUB</h1>
        <p>Gilgit-Baltistan Tourist Information</p>
    </section>

    <div class="dest-grid">
        <div class="dest-card">
            <img src="https://picsum.photos/id/1015/600/400" alt="Astore Valley">
            <div class="dest-overlay">
                <h3>Rama Meadows</h3>
                <p>Heart of Astore</p>
            </div>
        </div>

        <div class="dest-card">
            <img src="https://picsum.photos/id/1016/600/400" alt="Skardu">
            <div class="dest-overlay">
                <h3>Deosai Plains</h3>
                <p>The Roof of the World</p>
            </div>
        </div>

        <div class="dest-card">
            <img src="https://picsum.photos/id/1018/600/400" alt="Hunza">
            <div class="dest-overlay">
                <h3>Hunza Valley</h3>
                <p>Culture and Peaks</p>
            </div>
        </div>
    </div>

    <div style="text-align: center; padding: 40px;">
        <p>If photos still don't show, please check your internet connection.</p>
        <button onclick="location.reload()" style="padding:10px 20px; margin-top:10px; cursor:pointer;">Refresh Page</button>
    </div>

    <nav class="dock">
        <a href="https://wa.me/923171588489" style="color:#25d366; font-size:25px;"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/share/1BoG9YCsZN/" style="color:#1877f2; font-size:25px;"><i class="fa-brands fa-facebook"></i></a>
    </nav>

</body>
</html>
