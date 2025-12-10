<Astore>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Astore Tourist Information Hub</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    color: #fff;
    overflow-x: hidden;
}

/* Animated Neon Gradient Background */
.bg-animate {
    position: fixed;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, #001f3f, #003f7f, #007bff, #00d4ff);
    background-size: 400% 400%;
    animation: gradient 12s ease infinite;
    z-index: -1;
}

@keyframes gradient {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

/* Neon Container */
.container {
    max-width: 900px;
    margin: 90px auto;
    background: rgba(0, 0, 0, 0.35);
    padding: 30px;
    border-radius: 20px;
    backdrop-filter: blur(6px);
    box-shadow: 0 0 20px #00eaff;
    animation: fade 1.2s ease-in-out;
}

@keyframes fade {
    from {opacity: 0;}
    to {opacity: 1;}
}

h1 {
    text-align: center;
    font-size: 38px;
    font-weight: 600;
    text-shadow: 0 0 12px #00eaff;
}

.section-title {
    font-size: 24px;
    margin-top: 30px;
    text-shadow: 0 0 8px #00eaff;
}

/* Booking Form */
input, select {
    width: 100%;
    padding: 12px;
    margin-top: 10px;
    border-radius: 8px;
    border: none;
    outline: none;
    background: rgba(255,255,255,0.1);
    color: #fff;
}

button {
    width: 100%;
    padding: 14px;
    margin-top: 20px;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    background: #00eaff;
    color: #000;
    font-size: 18px;
    font-weight: 600;
    transition: 0.3s;
}

button:hover {
    background: #00bcd4;
}

/* WhatsApp Floating Button */
.whatsapp-btn {
    position: fixed;
    right: 20px;
    bottom: 20px;
    background: #25d366;
    padding: 15px 18px;
    border-radius: 50%;
    color: #fff;
    font-size: 28px;
    text-decoration: none;
    box-shadow: 0 0 15px #25d366;
}
</style>
</head>

<body>

<div class="bg-animate"></div>

<div class="container">
    <h1>Astore Tourist Information Hub</h1>
    
    <p style="text-align:center; font-size:17px;">
        Premium Booking • Rooms • Cars • Local Guide  
        <br>Owner: <b>Asim Khanzai</b>  
        <br>Contact: <b>03171588489</b>
    </p>

    <h2 class="section-title">Room & Car Booking Form</h2>

    <form>
        <label>Name</label>
        <input type="text" placeholder="Enter your name" required>

        <label>Phone</label>
        <input type="text" placeholder="03XX-XXXXXXX" required>

        <label>Booking Type</label>
        <select required>
            <option>Room Booking</option>
            <option>Car Booking</option>
            <option>Tour Package</option>
        </select>

        <label>Date</label>
        <input type="date" required>

        <button type="submit">Confirm Booking</button>
    </form>
</div>

<!-- WhatsApp Contact -->
<a class="whatsapp-btn" href="https://wa.me/923171588489">💬</a>

</body>
</html>
