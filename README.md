# Project Responsive Web Design using Bootstrap
# Date:
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
home.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }
       
        header {
            background: white;
            color: black;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 80px;
        }

        header img {
            height: 50px;
            width: auto;
        }

        header nav a {
            padding: 10px 15px;
            text-decoration: none;
            color: black;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }
        
        .banner {
            position: relative;
            overflow: hidden;
            height: 550px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
        }        

        .banner video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: 1;
            transform: translate(-50%, -50%);
            object-fit: cover;
        }

        .banner-content {
            position: relative;
            z-index: 2;
            max-width: 50%;
        }

        .banner-content h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .banner-content p {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        footer {
            background: white;
            color: rgb(0, 0, 0);
            text-align: center;
            padding: 10px 0;
            margin-top: 100px;
            font-size: larger;
        }

        @media (max-width: 768px) {
            .banner {
                height: auto;
                text-align: center;
            }

            .banner-content {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>

    <header>
        <img src="logo.png" alt="Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="explore.html">Explore</a>
            <a href="cart.html">Cart</a>
            <a href="contact.html">Contact Us</a>
        </nav>
        <nav>
            <a href="signup.html">Sign Up</a>
            <a href="login.html">Log In</a>
        </nav>
    </header>
    
    <div class="banner">
        <img src="azar.png" width="100%"> 
    </div>
<h1><center>Discover the world’s top products</center></h1>
<h3>Explore a curated collection of premium items designed to elevate your lifestyle. Experience quality, creativity, and confidence through our exclusive selection of world-class products.</h3>

    
       <center> <p>Designed by: Mohamed Asarudeen (25005844)</p></center>
    
     
</body>
</html>

cart.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Cart - Online Store</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #ffffff;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: white;
            color: black;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 80px;
            width: 100%;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        header img {
            height: 50px;
            width: auto;
        }

        header nav a {
            padding: 10px 15px;
            text-decoration: none;
            color: black;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #000;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            border-bottom: 1px solid #ccc;
        }

        .cart-item:last-child {
            border-bottom: none;
        }

        .item-details {
            display: flex;
            align-items: center;
        }

        .item-details img {
            height: 100px;
            width: auto;
            margin-right: 15px;
        }

        .item-info {
            display: flex;
            flex-direction: column;
        }

        .item-quantity {
            width: 60px;
            margin-left: 20px;
        }

        .total {
            font-size: 1.5rem;
            margin-top: 20px;
            text-align: right;
        }

        .buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        .buttons button {
            background: #ff5722;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s ease;
        }

        .buttons button:hover {
            background: #e64a19;
        }

        .remove-item {
            color: #ff5722;
            cursor: pointer;
            font-size: 0.9rem;
            margin-left: 20px;
        }
    </style>
</head>
<body>

    <header>
        <img src="logo.png" alt="Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="explore.html">Explore</a>
            <a href="cart.html">Cart</a>
            <a href="contact.html">Contact Us</a>
        </nav>
        <nav>
            <a href="signup.html">Sign Up</a>
            <a href="login.html">Log In</a>
        </nav>
    </header>

    <div class="cart-container">
        <h1>Your Cart</h1>
        
        <div class="cart-item">
            <div class="item-details">
                <img src="item1.png" alt="Mobile">
                <div class="item-info">
                    <h3>Samsung Galaxy S23 Ultra 5G AI Smartphone (Phantom Black, 12GB, 256GB Storage)</h3>
                    <p>-51% ₹72,999<br>M.R.P.: ₹1,49,999.00</p>
                </div>
            </div>
            <input type="number" class="item-quantity" value="1" min="1">
            <p>₹72,999.00</p>
            <span class="remove-item">Remove</span>
        </div>
        <div class="cart-item">
            <div class="item-details">
                <img src="item2.png" alt="Mobile Cover">
                <div class="item-info">
                    <h3>Spigen Liquid Air Back Cover Case Compatible with Galaxy S23 Ultra (TPU | Matte Black)</h3>
                    <p>-35% ₹1,104<br>M.R.P.: ₹1,699.00</p>
                </div>
            </div>
            <input type="number" class="item-quantity" value="1" min="1">
            <p>₹1,104.00</p>
            <span class="remove-item">Remove</span>
        </div>
        <div class="total">
            <strong>Total: ₹74,103.00</strong>
        </div>
        <div class="buttons">
            <button onclick="window.location.href='checkout.html'">Proceed to Checkout</button>
            <button onclick="window.location.href='home.html'">Continue Shopping</button>
        </div>
    </div>

</body>
</html>

contact.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 100vh;
            color: #333;
        }

        header {
            background: white;
            color: black;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 80px;
            width: 100%;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        header img {
            height: 50px;
            width: auto;
        }

        header nav a {
            padding: 10px 15px;
            text-decoration: none;
            color: black;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        .contact-container {
            background: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 400px;
            text-align: center;
            margin-top: 20px;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #000;
        }

        p {
            font-size: 1.1rem;
            margin-bottom: 30px;
        }

        input[type="text"], input[type="email"], textarea {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: #f9f9f9;
            color: #333;
        }

        textarea {
            height: 100px;
            resize: none;
        }

        input[type="submit"] {
            background: #000;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1.2rem;
            transition: background 0.3s ease;
            width: 100%;
        }

        input[type="submit"]:hover {
            background: #444;
        }

        .social-links {
            margin-top: 20px;
            font-size: 1.2rem;
            text-align: left;
        }

        .social-links p {
            margin: 5px 0;
        }

        .social-links a {
            text-decoration: none;
            color: #000;
        }

        .social-links a:hover {
            color: #ff5722;
        }
    </style>
</head>
<body>

    <header>
        <img src="logo.png" alt="Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="explore.html">Explore</a>
            <a href="cart.html">Cart</a>
            <a href="contact.html">Contact Us</a>
        </nav>
        <nav>
            <a href="signup.html">Sign Up</a> 
            <a href="login.html">Log In</a>
        </nav>
    </header>

    <div class="contact-container">
        <h1>Contact Us</h1>
        <p>We'd love to hear from you! Please fill out the form below.</p>
        <form action="submit-contact.html" method="POST">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <input type="submit" value="Send Message">
        </form>
        <div class="social-links">
            <p>Follow us on:</p>
            <p>Instagram: @dribble27</p>
            <p>Facebook: @dribble27</p>
            <p>X: @dribble27</p>
        </div>
    </div>

</body>
</html>

explore.html

z<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Explore</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            box-sizing: border-box;
            background-color: #f4f4f4;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: white;
            color: black;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 80px;
        }

        header img {
            height: 50px;
            width: auto;
        }

        header nav a {
            padding: 10px 15px;
            text-decoration: none;
            color: black;
            font-weight: bold;
            margin: 0 10px;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        .explore-container {
            padding: 40px 20px;
            text-align: center;
        }

        .explore-container h1 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 20px;
        }

        .explore-items {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .explore-item {
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            width: 300px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .explore-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .explore-item:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }

        .explore-details {
            padding: 15px;
        }

        .explore-details h3 {
            font-size: 1.5rem;
            color: #000000;
            margin-bottom: 8px;
        }

        .explore-details p {
            font-size: 1rem;
            color: #555;
            margin-bottom: 10px;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 15px 0;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5rem;
            }

            .explore-items {
                flex-direction: column;
                gap: 20px;
            }

            .explore-item {
                width: 100%;
            }

            header nav a {
                margin: 0 5px;
            }
        }
    </style>
</head>
<body>

    <header>
        <img src="logo.png" alt="Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="explore.html">Explore</a>
            <a href="cart.html">Cart</a>
            <a href="contact.html">Contact Us</a>
        </nav>
        <nav>
            <a href="signup.html">Sign Up</a>
            <a href="login.html">Log In</a>
        </nav>
    </header>

    <div class="explore-container">
        <h1>Explore Our Products</h1>
        <div class="explore-items">
            <div class="explore-item">
                <img src="electronics.png" alt="Electronics">
                <div class="explore-details">
                    <h3>Electronics</h3>
                    <p>Latest gadgets and devices.</p>
                </div>
            </div>
            <div class="explore-item">
                <img src="fashion.png" alt="Fashion">
                <div class="explore-details">
                    <h3>Fashion</h3>
                    <p>Trendy clothing and accessories.</p>
                </div>
            </div>
            <div class="explore-item">
                <img src="furniture.png" alt="Furniture">
                <div class="explore-details">
                    <h3>Furniture</h3>
                    <p>Stylish and comfortable furniture.</p>
                </div>
            </div>
            <div class="explore-item">
                <img src="toys.png" alt="Toys">
                <div class="explore-details">
                    <h3>Toys</h3>
                    <p>Fun and educational toys for kids.</p>
                </div>
            </div>
            <div class="explore-item">
                <img src="grocery.png" alt="Grocery">
                <div class="explore-details">
                    <h3>Grocery</h3>
                    <p>Fresh and quality grocery items.</p>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>Designed by: Mohamed Asarudeen (25005844)</p>
    </footer>
        
</body>
</html>

login.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: #333;
        }

        .login-container {
            background: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #000;
        }

        input[type="email"], input[type="password"] {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: #f9f9f9;
            color: #333;
        }

        input[type="submit"] {
            background: #000;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s ease;
            width: 100%;
        }

        input[type="submit"]:hover {
            background: #444;
        }

        .links {
            margin-top: 15px;
        }

        .links a {
            text-decoration: none;
            color: #000;
            font-weight: bold;
        }

        .links a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="login-container">
        <h1>Login</h1>
        <form action="dashboard.html" method="POST">
            <input type="email" placeholder="Email" required>
            <input type="password" placeholder="Password" required>
            <input type="submit" value="Login">
        </form>
        <div class="links">
            <p><a href="signup.html">Don't have an account? Sign Up</a></p>
            <p><a href="reset.html">Forgot Password?</a></p>
            <p><a href="home.html">Return Home</a></p>
        </div>
    </div>

</body>
</html>

reset.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reset Password</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: #333;
        }

        .reset-container {
            background: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #000;
        }

        input[type="email"] {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: #f9f9f9;
            color: #333;
        }

        input[type="submit"] {
            background: #000;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s ease;
            width: 100%;
        }

        input[type="submit"]:hover {
            background: #444;
        }

        .links {
            margin-top: 15px;
        }

        .links a {
            text-decoration: none;
            color: #000;
            font-weight: bold;
        }

        .links a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="reset-container">
        <h1>Reset Password</h1>
        <form action="send-reset-link.html" method="POST">
            <input type="email" placeholder="Enter your email" required>
            <input type="submit" value="Send Reset Link">
        </form>
        <div class="links">
            <p><a href="login.html">Back to Login</a></p>
        </div>
    </div>

</body>
</html>

signup.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: #333;
        }

        .signup-container {
            background: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #000;
        }

        input[type="text"], input[type="email"], input[type="password"] {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: #f9f9f9;
            color: #333;
        }

        input[type="submit"] {
            background: #000;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s ease;
            width: 100%;
        }

        input[type="submit"]:hover {
            background: #444;
        }

        .links {
            margin-top: 15px;
        }

        .links a {
            text-decoration: none;
            color: #000;
            font-weight: bold;
        }

        .links a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="signup-container">
        <h1>Sign Up</h1>
        <form action="welcome.html" method="POST">
            <input type="text" placeholder="Full Name" required>
            <input type="email" placeholder="Email" required>
            <input type="password" placeholder="Password" required>
            <input type="submit" value="Sign Up">
        </form>
        <div class="links">
            <p><a href="login.html">Already have an account? Log In</a></p>
        </div>
    </div>

</body>
</html>
# OUTPUT:
<img width="816" height="346" alt="image" src="https://github.com/user-attachments/assets/eba9a3a3-a3fd-40f4-a403-ec82454106ba" />
<img width="820" height="304" alt="image" src="https://github.com/user-attachments/assets/f37acbb9-db10-4352-af94-91379e199833" />
<img width="815" height="352" alt="image" src="https://github.com/user-attachments/assets/40ade6d5-ddba-4b40-9120-56f49d47be86" />
<img width="815" height="407" alt="image" src="https://github.com/user-attachments/assets/acb3a092-4c9d-4cf5-bd65-b9cf7237dca4" />
<img width="818" height="417" alt="image" src="https://github.com/user-attachments/assets/b0fa8078-2d91-4625-b5e0-fb9e4132120e" />
<img width="820" height="408" alt="image" src="https://github.com/user-attachments/assets/3a4e2afa-8a86-463d-b193-ba8463baea43" />
<img width="808" height="406" alt="image" src="https://github.com/user-attachments/assets/c0f63ce4-efd2-4a0f-bc20-c79137a0126f" />





# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
