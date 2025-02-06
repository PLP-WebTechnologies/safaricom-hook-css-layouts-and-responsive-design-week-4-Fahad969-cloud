# Assignment: Responsive Web Design

## Objective:
Create a responsive webpage using modern CSS techniques, specifically Flexbox, Grid, and Media Queries. The goal is to ensure the webpage adapts gracefully to various screen sizes.

## Assignment Tasks

### Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links).
Main content area (with two columns: one for text content and the other for an image).
Footer (with links to social media and a copyright notice).
b. Use Flexbox to style the navigation menu in the header.
c. Use CSS Grid to structure the main content area.
<!DOCtml>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop in Ukunda</title>

    <!-- Internal CSS -->
    <style>
        /* Reset default styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body and general page styles */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f8f8f8;
        }

        /* Header */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            background-color: #333;
            color: white;
        }

        header .logo img {
            width: 100px;
        }

        nav ul {
            display: flex;
            list-style-type: none;
        }

        nav ul li {
            margin-right: 20px;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
        }

        /* Sections */
        section {
            padding: 20px;
            margin: 20px 0;
        }

        .home, .about, .services, .contact {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .home h1, .about h2, .services h2, .contact h2 {
            color: #333;
        }

        /* Services List */
        .services ul {
            list-style-type: none;
        }

        .services ul li {
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px;
        }

        footer .social-media a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
        }

        footer p {
            margin-top: 10px;
        }

        /* Media Query for mobile responsiveness */
        @media (max-width: 768px) {
            /* Stack header items vertically */
            header {
                flex-direction: column;
                align-items: flex-start;
            }

            /* Stack sections vertically on smaller screens */
            section {
                margin: 10px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <img src="Al Amin Stores Ukunda.webp" alt="Shop Logo">
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="home">
        <h1>Welcome to Our Shop in Ukunda</h1>
        <p>Your one-stop shop for fresh foodstuffs and more!</p>
    </section>

    <section id="about" class="about">
        <h2>About Us</h2>
        <p>We are a local shop in Ukunda, committed to providing fresh and affordable foodstuffs to our community. Whether you're looking for fruits, vegetables, or packaged goods, we've got you covered!</p>
    </section>

    <section id="services" class="services">
        <h2>Our Services</h2>
        <ul>
            <li>Fresh Fruits and Vegetables</li>
            <li>Packaged Food and Snacks</li>
            <li>Wholesale Supplies</li>
            <li>Home Delivery (within Ukunda)</li>
        </ul>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>Have any questions or want to place an order? Reach out to us:</p>
        <p>Phone: <a href="tel:+254722780939">+254 722 780 939</a></p>
        <p>Email: <a href="mailto:alaminshop@gmail.com">alaminshop@gmail.com</a></p>
    </section>

    <footer>
        <div class="social-media">
           | <a href="https://x.com/fahaddiisow?t=QlKUL7g057BDp9emRezylg&s=09">Twitter</a> | <a href="https://www.instagram.com/fuad_bare?igsh=MTFtMDF2YnIxd3ljag==">Instagram</a>
        </div>
        <p>&copy; 2025 Shop in Ukunda. All rights reserved.</p>
    </footer>
</body>
</html>

### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

### Bonus

Add animations or transitions when resizing the screen.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop in Ukunda</title>

    <style>
        /* Reset default styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body and general page styles */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f8f8f8;
            transition: all 0.3s ease; /* Smooth transition for resizing */
        }

        /* Header */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            background-color: #333;
            color: white;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: padding 0.3s ease;
        }

        header .logo img {
            width: 150px;  /* Set the width of the logo image */
            height: auto;  /* Maintain aspect ratio */
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        header .logo img:hover {
            transform: scale(1.1);  /* Slightly enlarge logo on hover */
        }

        nav ul {
            display: flex;
            list-style-type: none;
        }

        nav ul li {
            margin-right: 20px;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            text-transform: uppercase;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ff6347;  /* Change link color on hover */
        }

        /* Sections */
        section {
            padding: 20px;
            margin: 20px 0;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: margin 0.3s ease, padding 0.3s ease;
        }

        .home h1, .about h2, .services h2, .contact h2 {
            color: #333;
        }

        .services ul {
            list-style-type: none;
        }

        .services ul li {
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px;
            transition: padding 0.3s ease;
        }

        footer .social-media a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            font-size: 18px;
        }

        footer p {
            margin-top: 10px;
        }

        /* Media Queries for Different Screen Sizes */

        /* Small Screens (up to 600px) */
        @media (max-width: 600px) {
            header {
                flex-direction: column;
                align-items: center;
                text-align: center;
                padding: 15px;
            }

            nav ul {
                flex-direction: column;
                margin-top: 10px;
            }

            nav ul li {
                margin-bottom: 10px;
            }

            section {
                margin: 10px 0;
                padding: 15px;
            }

            .home, .about, .services, .contact {
                padding: 15px;
            }

            footer {
                padding: 15px;
            }
        }

        /* Medium Screens (601px to 1024px) */
        @media (min-width: 601px) and (max-width: 1024px) {
            header {
                flex-direction: row;
                justify-content: space-between;
                align-items: center;
                padding: 20px;
            }

            nav ul {
                flex-direction: row;
            }

            section {
                display: block;
                margin-top: 20px;
                padding: 20px;
            }

            .home, .about, .services, .contact {
                padding: 20px;
            }

            footer {
                padding: 20px;
            }

            .services ul li {
                font-size: 16px;
            }
        }

        /* Large Screens (above 1024px) */
        @media (min-width: 1025px) {
            header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 20px;
            }

            nav ul {
                display: flex;
                list-style-type: none;
            }

            section {
                display: grid;
                grid-template-columns: 1fr 1fr; /* Two columns for text and image */
                gap: 20px;
                padding: 20px;
            }

            .home, .about, .services, .contact {
                padding: 20px;
            }

            footer {
                padding: 20px;
            }

            .services ul li {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">
            <img src="Al Amin Stores Ukunda.webp" alt="Shop Logo">
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="home">
        <h1>Welcome to Our Shop in Ukunda</h1>
        <p>Your one-stop shop for fresh foodstuffs and more! We provide a variety of groceries and home essentials, from fresh vegetables to packaged goods, all available at affordable prices.</p>
    </section>

    <section id="about" class="about">
        <h2>About Us</h2>
        <p>We are a local shop in Ukunda, committed to providing fresh and affordable foodstuffs to our community. Whether you're looking for fruits, vegetables, or packaged goods, we've got you covered! We are passionate about quality and convenience, offering our products to help families maintain a healthy lifestyle.</p>
    </section>

    <section id="services" class="services">
        <h2>Our Services</h2>
        <ul>
            <li>Fresh Fruits and Vegetables</li>
            <li>Packaged Food and Snacks</li>
            <li>Wholesale Supplies</li>
            <li>Home Delivery (within Ukunda)</li>
        </ul>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>Have any questions or want to place an order? Reach out to us:</p>
        <p>Phone: <a href="tel:+254722780939">+254 722 780 939</a></p>
        <p>Email: <a href="mailto:alamin@gmail.com.com">alamin@gmail.com</a></p>
    </section>

    <footer>
        <div class="social-media">
      | <a href="https://x.com/fahaddiisow?t=QlKUL7g057BDp9emRezylg&s=09">Twitter</a> | <a href="https://www.instagram.com/fuad_bare?igsh=MTFtMDF2YnIxd3ljag==">Instagram</a>
        </div>
        <p>&copy; 2025 Shop in Ukunda. All rights reserved.</p>
    </footer>

</body>
</html>
