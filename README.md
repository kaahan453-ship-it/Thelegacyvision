# sample-web-project
Sample web project used to showcase a deployment process with Flightplan.js and git

The full article is available at http://usersnap.com/blog/deploying-static-websites-flightplan/
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gourmet Cafe | Table Booking</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #6F4E37; /* Coffee Brown */
            --secondary: #ECB176; /* Warm Tan */
            --light: #FED8B1; /* Cream */
            --dark: #2D2424;
            --white: #ffffff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: #fffaf5;
        }

        /* Navigation */
        nav {
            background: var(--white);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: var(--primary);
            text-decoration: none;
        }

        .nav-links a {
            margin-left: 20px;
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1501339847302-ac426a4a7cbb?auto=format&fit=crop&q=80&w=1470');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            margin-bottom: 10px;
        }

        .btn-main {
            background: var(--primary);
            color: var(--white);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 30px;
            margin-top: 20px;
            font-weight: 600;
            transition: 0.3s;
        }

        .btn-main:hover {
            background: var(--secondary);
        }

        /* Sections Styling */
        section {
            padding: 80px 10%;
        }

        .section-title {
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: var(--primary);
        }

        /* Menu Grid */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .menu-item {
            background: var(--white);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
        }

        /* Booking Form */
        .booking-container {
            max-width: 600px;
            margin: 0 auto;
            background: var(--white);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }

        .whatsapp-btn {
            width: 100%;
            background: #25D366;
            color: white;
            border: none;
            padding: 15px;
            font-size: 1.1rem;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        .whatsapp-btn:hover {
            background: #128C7E;
        }

        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 20px;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            section { padding: 50px 5%; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

    <nav>
        <a href="#" class="logo">The Local Cafe</a>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#menu">Menu</a>
            <a href="#booking">Book a Table</a>
        </div>
    </nav>

    <header class="hero">
        <h1>Crafted Coffee & Cozy Vibes</h1>
        <p>Freshly brewed memories, one cup at a time.</p>
        <a href="#booking" class="btn-main">Reserve Your Spot</a>
    </header>

    <section id="about">
        <h2 class="section-title">Our Story</h2>
        <p style="text-align: center; max-width: 800px; margin: 0 auto;">
            Located in the heart of the city, we pride ourselves on sourcing the finest organic beans and creating a sanctuary for foodies and coffee lovers alike.
        </p>
    </section>

    <section id="menu" style="background: #fdf6ee;">
        <h2 class="section-title">Digital Menu</h2>
        <div class="menu-grid">
            <div class="menu-item">
                <h3>Espresso</h3>
                <p>Rich and bold signature roast.</p>
            </div>
            <div class="menu-item">
                <h3>Caramel Latte</h3>
                <p>Sweet, creamy, and topped with gold.</p>
            </div>
            <div class="menu-item">
                <h3>Avocado Toast</h3>
                <p>Sourdough with fresh smashed avocado.</p>
            </div>
        </div>
    </section>

    <section id="booking">
        <h2 class="section-title">Book a Table</h2>
        <div class="booking-container">
            <form id="reservationForm">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" id="custName" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <label>Phone Number</label>
                    <input type="tel" id="custPhone" placeholder="Mobile Number" required>
                </div>
                <div class="form-group">
                    <label>Number of Guests</label>
                    <select id="guests">
                        <option value="1">1 Person</option>
                        <option value="2">2 People</option>
                        <option value="3">3 People</option>
                        <option value="4">4 People</option>
                        <option value="5+">5+ People</option>
                    </select>
                </div>
                <div style="display: flex; gap: 15px;">
                    <div class="form-group" style="flex: 1;">
                        <label>Select Date</label>
                        <input type="date" id="bookDate" required>
                    </div>
                    <div class="form-group" style="flex: 1;">
                        <label>Time Slot</label>
                        <select id="bookTime">
                            <option value="09:00 AM">09:00 AM</option>
                            <option value="11:00 AM">11:00 AM</option>
                            <option value="01:00 PM">01:00 PM</option>
                            <option value="04:00 PM">04:00 PM</option>
                            <option value="07:00 PM">07:00 PM</option>
                        </select>
                    </div>
                </div>
                <button type="button" onclick="sendToWhatsApp()" class="whatsapp-btn">
                    Confirm Booking on WhatsApp
                </button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 The Local Cafe. Contact: +91 9548337625</p>
    </footer>

    <script>
        function sendToWhatsApp() {
            // Get form values
            const name = document.getElementById('custName').value;
            const phone = document.getElementById('custPhone').value;
            const guests = document.getElementById('guests').value;
            const date = document.getElementById('bookDate').value;
            const time = document.getElementById('bookTime').value;

            // Simple validation
            if (!name || !phone || !date) {
                alert("Please fill in all details before booking.");
                return;
            }

            // Define Business Number
            const businessNumber = "919548337625";

            // Format the message
            const message = `Hello, I want to book a table. 
Name: ${name}
Guests: ${guests}
Date: ${date}
Time: ${time}
My Contact: ${phone}`;

            // Encode message for URL
            const encodedMessage = encodeURIComponent(message);

            // Redirect to WhatsApp
            const whatsappURL = `https://wa.me/${businessNumber}?text=${encodedMessage}`;
            window.open(whatsappURL, '_blank');
        }
    </script>
</body>
</html>
