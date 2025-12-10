<ASTORE TOURIST HUB>
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
}

/* Animated Neon Gradient */
.bg-animate {
    position: fixed;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, #001f3f, #003a75, #007bff, #00d4ff);
    background-size: 400% 400%;
    animation: gradient 12s ease infinite;
    z-index: -1;
}
@keyframes gradient {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

/* Card */
.container {
    max-width: 900px;
    margin: 90px auto;
    background: rgba(0,0,0,0.35);
    padding: 30px;
    border-radius: 20px;
    backdrop-filter: blur(7px);
    box-shadow: 0 0 20px #00eaff;
}

h1 {
    text-align: center;
    text-shadow: 0 0 15px #00eaff;
    font-size: 38px;
}

.section-title {
    margin-top: 25px;
    font-size: 24px;
    text-shadow: 0 0 10px #00eaff;
}

label {
    margin-top: 15px;
    display: block;
    font-weight: 500;
}

input, select {
    width: 100%;
    padding: 12px;
    margin-top: 6px;
    border-radius: 10px;
    background: rgba(255,255,255,0.2);
    border: none;
    color: #fff;
}

button {
    width: 100%;
    padding: 14px;
    margin-top: 20px;
    background: #00eaff;
    color: #000;
    border-radius: 10px;
    font-weight: 600;
    font-size: 18px;
    border: none;
    cursor: pointer;
}
button:hover {background: #00c7d6;}

/* Floating WhatsApp */
.whatsapp-btn {
    position: fixed;
    right: 20px;
    bottom: 20px;
    background: #25d366;
    padding: 16px 18px;
    border-radius: 50%;
    font-size: 30px;
    color: #fff;
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
        Premium Tourism Services • Rooms • Cars • Local Guide  
        <br>Owner: <b>Asim Khanzai</b>
        <br>WhatsApp: <b>03171588489</b>
    </p>

    <h2 class="section-title">Online Booking Form</h2>

    <form id="bookingForm">
        <label>Name</label>
        <input type="text" id="name" required>

        <label>Phone</label>
        <input type="text" id="phone" required>

        <label>Booking Type</label>
        <select id="type" required>
            <option>Room Booking</option>
            <option>Car Booking</option>
            <option>Tour Package</option>
        </select>

        <label>Date</label>
        <input type="date" id="date" required>

        <button type="submit">Send Booking Request</button>
    </form>
</div>

<!-- WhatsApp Button -->
<a class="whatsapp-btn" href="https://wa.me/923171588489">💬</a>

<script>
document.getElementById("bookingForm").addEventListener("submit", function(e){
    e.preventDefault();

    let name = document.getElementById("name").value;
    let phone = document.getElementById("phone").value;
    let type = document.getElementById("type").value;
    let date = document.getElementById("date").value;

    let msg =
        "New Booking Request:%0A" +
        "Name: " + name + "%0A" +
        "Phone: " + phone + "%0A" +
        "Booking Type: " + type + "%0A" +
        "Date: " + date + "%0A%0A" +
        "Kindly confirm my booking.";

    window.location.href = "https://wa.me/923171588489?text=" + msg;
});
</script>

</body>
</html>
