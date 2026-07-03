<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Signature Tour & Travel Agency</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: #f4f6f9;
}

/* HEADER */
header {
    background: linear-gradient(90deg, #1e3c72, #2a5298);
    color: white;
    text-align: center;
    padding: 25px 15px;
}

header h1 {
    margin: 0;
    font-size: 28px;
}

header p {
    margin-top: 5px;
    font-size: 14px;
}

/* HERO */
.hero {
    background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') no-repeat center/cover;
    height: 260px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
}

.hero h2 {
    background: rgba(0,0,0,0.4);
    padding: 10px 15px;
    border-radius: 6px;
}

/* CONTENT */
.container {
    padding: 20px;
}

.section-title {
    text-align: center;
    color: #2a5298;
}

/* FEATURES */
.features {
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 10px;
    margin-bottom: 20px;
}

.feature-box {
    background: white;
    padding: 12px;
    text-align: center;
    border-radius: 8px;
    font-size: 13px;
    box-shadow: 0 0 8px rgba(0,0,0,0.08);
}

/* FORM */
.form-box {
    background: white;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 0 12px rgba(0,0,0,0.1);
}

input, select, textarea {
    width: 100%;
    padding: 10px;
    margin: 8px 0;
    border-radius: 6px;
    border: 1px solid #ccc;
}

button {
    width: 100%;
    background: #2a5298;
    color: white;
    padding: 14px;
    border: none;
    border-radius: 6px;
    font-size: 16px;
    font-weight: bold;
}

button:hover {
    background: #1e3c72;
}

/* WHATSAPP FLOAT */
.whatsapp-btn {
    position: fixed;
    bottom: 15px;
    right: 15px;
    background: #25D366;
    color: white;
    padding: 16px;
    border-radius: 50%;
    text-decoration: none;
    font-size: 22px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 12px;
    background: #1e3c72;
    color: white;
    margin-top: 20px;
}
</style>
</head>

<body>

<header>
    <h1>Signature Tour & Travel</h1>
    <p>Your Trusted Travel Partner</p>
</header>

<div class="hero">
    <h2>Explore Assam • Meghalaya • Arunachal with Comfort</h2>
</div>

<div class="container">

    <h2 class="section-title">Why Choose Us?</h2>

    <div class="features">
        <div class="feature-box">🚗 Comfortable Cars</div>
        <div class="feature-box">💰 Best Price Deals</div>
        <div class="feature-box">🧭 Expert Drivers</div>
        <div class="feature-box">📍 Custom Tours</div>
    </div>

    <h2 class="section-title">Book Your Trip</h2>

    <div class="form-box">
        <form onsubmit="sendToWhatsApp(); return false;">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="tel" id="phone" placeholder="Phone Number" required>

            <select id="destination">
                <option>Shillong</option>
                <option>Kaziranga</option>
                <option>Tawang</option>
                <option>Custom Tour</option>
            </select>

            <input type="date" id="date" required>
            <input type="number" id="pax" placeholder="Number of Persons" required>

            <textarea id="message" placeholder="Extra Details"></textarea>

            <button type="submit">📲 Book Now on WhatsApp</button>
        </form>
    </div>

</div>

<a class="whatsapp-btn" href="https://wa.me/918472081110" target="_blank">💬</a>

<footer>
    <p>📞 Call/WhatsApp: 8472081110</p>
</footer>

<script>
function sendToWhatsApp() {
    var name = document.getElementById("name").value;
    var phone = document.getElementById("phone").value;
    var destination = document.getElementById("destination").value;
    var date = document.getElementById("date").value;
    var pax = document.getElementById("pax").value;
    var message = document.getElementById("message").value;

    var text = `New Booking Request:
Name: ${name}
Phone: ${phone}
Destination: ${destination}
Date: ${date}
Persons: ${pax}
Message: ${message}`;

    var url = "https://wa.me/918472081110?text=" + encodeURIComponent(text);

    window.open(url, "_blank");
}
</script>

</body>
</html>