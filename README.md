
# RoyalFlavours Food Delivery System

**Student Name:** Alan Benny  
**Student ID:** 35642348  
**Live Demo:** [royalflavours.store](https://royalflavours.store)  
**Public IP:** `13.250.220.174`  
**Domain Provider:** Namecheap.com  
**GitHub Repository:** [GitHub Repo](https://github.com/alanbennny/royalflavours)

---

## 🌐 Overview

RoyalFlavours is a modern, responsive food delivery website built using HTML, CSS, and JavaScript. It features a persistent shopping cart, secure checkout, and order confirmation system. The project is deployed on an Amazon EC2 instance and accessible via a custom domain with HTTPS enabled.

---

## 📁 Project Structure

```
royalflavours/
├── css/
│   └── style.css                # Website styles
├── js/
│   ├── cart.js                  # Cart management logic
│   └── checkout.js              # Checkout and order persistence
├── images/                      # Product images, branding assets
├── index.html                   # Homepage
├── menu.html                    # Product listing page
├── about.html                   # About the service
├── contact.html                 # Contact form
├── checkout.html                # Order form and customer info
└── order-confirmation.html      # Receipt and confirmation page
```

---

## 📄 HTML Pages Description

### `index.html`
- Landing page with menu categories, offers, and highlights.

index.html

<!DOCTYPE html> <html lang="en"> <head> <title>RoyalFlavours - Food Takeaway System</title> <meta charset="utf-8"> <meta name="viewport" content="width=device-width, initial-scale=1.0"> <meta name="description" content="RoyalFlavours: Food takeaway system with cash on delivery only"> <style> :root { --primary: #4a6bdf; --light: #f8f9fa; --dark: #1a1a极a; --darker: #121212; --light-text: #e0e0e0; --success: #28a745; --warning: #ffc107; --danger: #dc3545; --font-main: 'Inter', sans-serif; --font-heading: 'Inter', sans-serif; } body { font-family: var(--font-main); background-color: var(--dark); color: var(--light-text); margin: 0; padding: 0; line-height: 1.6; } header { background: var(--darker); box-shadow: 0 2px 10px rgba(0,0,0,0.2); padding: 10px 0; position: sticky; top: 极; z-index: 1000; } .container { max-width: 1200px; margin: 0 auto; padding: 0 15px; } .logo { height: 60px; width: auto; margin-right: 10px; } .nav-link { color: var(--light-text); text-decoration: none; margin: 0 10px; font-weight: 500; transition: color 0.2s; } .nav-link:hover { color: var(--primary); } .nav-link.active { color: var(--primary); font-weight: 600; } .btn { background: var(--primary); color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer; transition: background 0.2s, transform 0.2s; text-decoration: none; display: inline-block; } .btn:hover { background: #3a5ac8; transform: translateY(-2px); } .hero { background: linear-gradient(135deg, var(--dark) 0%, var(--darker) 100%); color: var(--light-text); padding: 60px 0; text-align: center; } .hero h1 { font-size: 2.5rem; margin-bottom: 20px; } .menu-categories { display: flex; flex-direction: column; gap: 10px; } .menu-categories a { padding: 10px 15px; border-radius: 5px; background: var(--darker); color: var(--light-text); text-decoration: none; transition: background 0.2s; } .menu-categories a:hover { background: #2a2a2a; } .menu-categories a.active { background: var(--primary); color: white; } .product-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; margin: 20px 0; } .product-item { background: var(--darker); border-radius: 10px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); overflow: hidden; transition: transform 0.2s, box-shadow 0.2s; } .product-item:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0,0,0,0.2); } .product-item img { width: 100%; height: 150px; object-fit: cover; } .product-item .card-body { padding: 15px; } .rating { color: var(--warning); } .discount-banner { background: linear-gradient(135deg, #ffb347 0%, #ffcc33 100%); color: var(--dark); padding: 30px; margin: 20px 0; border-radius: 10px; text-align: center; } .features { display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; padding: 30px 0; background: var(--darker); } .feature { flex: 1 1 300px; background: var(--dark); padding: 20px; border-radius: 10px; box-shadow: 极 2px 10px rgba(0,0,0,0.1); text-align: center; color: var(--light-text); } footer { background: var(--darker); color: var(--light-text); padding: 30px 0; text-align: center; margin-top: 40px; } .social-links { display: flex; gap: 15px; justify-content: center; margin: 20px 0; } .social-links a { color: var(--light-text); font-size: 1.5rem; text-decoration: none; } @media (max-width: 768px) { .product-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); } } </style> </head> <body> <header> <div class="container"> <div style="display: flex; align-items: center; justify-content: space-between;"> <div style="display: flex; align-items: center;"> <a href="index.html"> <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJq极yYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo"> </a> </div> <nav style="display: flex; align-items: center;"> <a href="index.html" class="nav-link active">Home</a> <a href="menu.html" class="nav-link">Menu</a> <a href="about.html" class="nav-link">About</a> <a href="contact.html" class="nav-link">Contact</a> <a href="#" class="nav-link" style="color: var(--danger);">Cash on Delivery Only</a> </nav> </div> </div> </header> <section class="hero"> <div class="container"> <h1>RoyalFlavours</h1> <p>Delicious Food, Delivered Fast</p> <a href="menu.html极 class="btn">Order Now</a> </div> </section> <section class="container" style="margin-top: 40px; display: flex; gap: 20px;"> <div style="flex: 0 0 200px;"> <h3>Menu Categories</h3> <div class="menu-categories"> <a href="menu.html#burgers" class="active">Burgers</a> <a href="menu.html#pizza">Pizza</a> <a href="menu.html#asian">Asian</a> <a href="menu.html#desserts">Desserts</a> <a href="menu.html#drinks">Drinks</a> </div> </div> <div style="flex: 1;"> <h2>Best Selling Dishes</h2> <div class="product-grid"> <div class="product-item"> <img src="https://via.placeholder.com/300x200?text=Royal+Burger" alt="Royal Burger"> <div class="card-body"> <h3>Royal Burger</h3> <div class="rating">★★★★☆ (222)</div> <div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;"> <del>$24.00</del> <span style="font-weight: bold;">$18.00</span> </div> <a href="menu.html#burgers" class="btn" style="width: 100%; margin-top: 10px; display: block; text-align: center;">Add to Cart</a> </div> </div> <div class="product-item"> <img src="https://via.placeholder.com/300x200?text=Pizza" alt="Pizza"> <div class="card-body"> <h3>Pizza</h3> <div class="rating">★★★★★ (189)</div> <div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;"> <span style="font-weight: bold;">$16.00</span> </div> <a href="menu.html#pizza" class="btn" style="width: 100%; margin-top: 10px; display: block; text-align: center;">Add to Cart</a> </div> </div> <!-- Add more products as needed --> </div> </div> </section> <section class="discount-banner"> <div class="container"> <h2>Get <span style="color: var(--dark);">25% Discount</span> on your first order</h2> <p>Just Sign Up & Register to become a member.</p> <form action="menu.html" style="极ax-width: 400px; margin: 0 auto;"> <input type="email" placeholder="Email" style="width: 100%; padding: 10px; margin-bottom: 10px; border: none; border-radius: 5px;"> <button type="submit" class="btn" style="width: 100%;">Subscribe</button> </form> </div> </section> <section class="features"> <div class="feature"> <h3极Free Delivery</h3> <p>Fast and reliable delivery to your doorstep.</p> </div> <div class="feature"> <h3>Cash on Delivery Only</h3> <p>Pay in cash when your order arrives.</p> </div> <div class="feature"> <h3>Quality Guarantee</h3> <p>Fresh ingredients and delicious meals every time.</p> </div> </section> <footer> <div class="container"> <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo"> <div class="social-links"> <a href="#">Facebook</a> <a href="#">Twitter</a> <a href="#">Instagram</a> </div> <p>© 2024 RoyalFlavours. All rights reserved.</p> <p>Made by Alan Benny</p> </div> </footer> </body> </html> ```
### `menu.html`
- Displays all food items by category.
- "Add to Cart" functionality integrated.
  index.html

<!DOCTYPE html> <html lang="en"> <head> <title>RoyalFlavours - Food Takeaway System</title> <meta charset="utf-8"> <meta name="viewport" content="width=device-width, initial-scale=1.0"> <meta name="description" content="RoyalFlavours: Food takeaway system with cash on delivery only"> <style> :root { --primary: #4a6bdf; --light: #f8f9fa; --dark: #1a1a极a; --darker: #121212; --light-text: #e0e0e0; --success: #28a745; --warning: #ffc107; --danger: #dc3545; --font-main: 'Inter', sans-serif; --font-heading: 'Inter', sans-serif; } body { font-family: var(--font-main); background-color: var(--dark); color: var(--light-text); margin: 0; padding: 0; line-height: 1.6; } header { background: var(--darker); box-shadow: 0 2px 10px rgba(0,0,0,0.2); padding: 10px 0; position: sticky; top: 极; z-index: 1000; } .container { max-width: 1200px; margin: 0 auto; padding: 0 15px; } .logo { height: 60px; width: auto; margin-right: 10px; } .nav-link { color: var(--light-text); text-decoration: none; margin: 0 10px; font-weight: 500; transition: color 0.2s; } .nav-link:hover { color: var(--primary); } .nav-link.active { color: var(--primary); font-weight: 600; } .btn { background: var(--primary); color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer; transition: background 0.2s, transform 0.2s; text-decoration: none; display: inline-block; } .btn:hover { background: #3a5ac8; transform: translateY(-2px); } .hero { background: linear-gradient(135deg, var(--dark) 0%, var(--darker) 100%); color: var(--light-text); padding: 60px 0; text-align: center; } .hero h1 { font-size: 2.5rem; margin-bottom: 20px; } .menu-categories { display: flex; flex-direction: column; gap: 10px; } .menu-categories a { padding: 10px 15px; border-radius: 5px; background: var(--darker); color: var(--light-text); text-decoration: none; transition: background 0.2s; } .menu-categories a:hover { background: #2a2a2a; } .menu-categories a.active { background: var(--primary); color: white; } .product-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; margin: 20px 0; } .product-item { background: var(--darker); border-radius: 10px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); overflow: hidden; transition: transform 0.2s, box-shadow 0.2s; } .product-item:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0,0,0,0.2); } .product-item img { width: 100%; height: 150px; object-fit: cover; } .product-item .card-body { padding: 15px; } .rating { color: var(--warning); } .discount-banner { background: linear-gradient(135deg, #ffb347 0%, #ffcc33 100%); color: var(--dark); padding: 30px; margin: 20px 0; border-radius: 10px; text-align: center; } .features { display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; padding: 30px 0; background: var(--darker); } .feature { flex: 1 1 300px; background: var(--dark); padding: 20px; border-radius: 10px; box-shadow: 极 2px 10px rgba(0,0,0,0.1); text-align: center; color: var(--light-text); } footer { background: var(--darker); color: var(--light-text); padding: 30px 0; text-align: center; margin-top: 40px; } .social-links { display: flex; gap: 15px; justify-content: center; margin: 20px 0; } .social-links a { color: var(--light-text); font-size: 1.5rem; text-decoration: none; } @media (max-width: 768px) { .product-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); } } </style> </head> <body> <header> <div class="container"> <div style="display: flex; align-items: center; justify-content: space-between;"> <div style="display: flex; align-items: center;"> <a href="index.html"> <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJq极yYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo"> </a> </div> <nav style="display: flex; align-items: center;"> <a href="index.html" class="nav-link active">Home</a> <a href="menu.html" class="nav-link">Menu</a> <a href="about.html" class="nav-link">About</a> <a href="contact.html" class="nav-link">Contact</a> <a href="#" class="nav-link" style="color: var(--danger);">Cash on Delivery Only</a> </nav> </div> </div> </header> <section class="hero"> <div class="container"> <h1>RoyalFlavours</h1> <p>Delicious Food, Delivered Fast</p> <a href="menu.html极 class="btn">Order Now</a> </div> </section> <section class="container" style="margin-top: 40px; display: flex; gap: 20px;"> <div style="flex: 0 0 200px;"> <h3>Menu Categories</h3> <div class="menu-categories"> <a href="menu.html#burgers" class="active">Burgers</a> <a href="menu.html#pizza">Pizza</a> <a href="menu.html#asian">Asian</a> <a href="menu.html#desserts">Desserts</a> <a href="menu.html#drinks">Drinks</a> </div> </div> <div style="flex: 1;"> <h2>Best Selling Dishes</h2> <div class="product-grid"> <div class="product-item"> <img src="https://via.placeholder.com/300x200?text=Royal+Burger" alt="Royal Burger"> <div class="card-body"> <h3>Royal Burger</h3> <div class="rating">★★★★☆ (222)</div> <div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;"> <del>$24.00</del> <span style="font-weight: bold;">$18.00</span> </div> <a href="menu.html#burgers" class="btn" style="width: 100%; margin-top: 10px; display: block; text-align: center;">Add to Cart</a> </div> </div> <div class="product-item"> <img src="https://via.placeholder.com/300x200?text=Pizza" alt="Pizza"> <div class="card-body"> <h3>Pizza</h3> <div class="rating">★★★★★ (189)</div> <div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;"> <span style="font-weight: bold;">$16.00</span> </div> <a href="menu.html#pizza" class="btn" style="width: 100%; margin-top: 10px; display: block; text-align: center;">Add to Cart</a> </div> </div> <!-- Add more products as needed --> </div> </div> </section> <section class="discount-banner"> <div class="container"> <h2>Get <span style="color: var(--dark);">25% Discount</span> on your first order</h2> <p>Just Sign Up & Register to become a member.</p> <form action="menu.html" style="极ax-width: 400px; margin: 0 auto;"> <input type="email" placeholder="Email" style="width: 100%; padding: 10px; margin-bottom: 10px; border: none; border-radius: 5px;"> <button type="submit" class="btn" style="width: 100%;">Subscribe</button> </form> </div> </section> <section class="features"> <div class="feature"> <h3极Free Delivery</h3> <p>Fast and reliable delivery to your doorstep.</p> </div> <div class="feature"> <h3>Cash on Delivery Only</h3> <p>Pay in cash when your order arrives.</p> </div> <div class="feature"> <h3>Quality Guarantee</h3> <p>Fresh ingredients and delicious meals every time.</p> </div> </section> <footer> <div class="container"> <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo"> <div class="social-links"> <a href="#">Facebook</a> <a href="#">Twitter</a> <a href="#">Instagram</a> </div> <p>© 2024 RoyalFlavours. All rights reserved.</p> <p>Made by Alan Benny</p> </div> </footer> </body> </html> ```

### `about.html`
- Brief overview of RoyalFlavours, mission, and services.
<!DOCTYPE html>
<html lang="en">
<head>
  <title>RoyalFlavours - About</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="css/style.css" rel="stylesheet">
</head>
<body>
  <header>
    <div class="container">
      <div style="display: flex; align-items: center; justify-content: space-between;">
        <div style="display: flex; align-items: center;">
          <a href="index.html">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
          </a>
        </div>
        <nav style="display: flex; align-items: center;">
          <a href="index.html" class="nav-link">Home</a>
          <a href="menu.html" class="nav-link">Menu</a>
          <a href="about.html" class="nav-link active">About</a>
          <a href="contact.html" class="nav-link">Contact</a>
          <a href="#" class="nav-link" style="color: var(--danger);">Cash on Delivery Only</a>
        </nav>
      </div>
    </div>
  </header>

  <main class="container">
    <h1>About Us</h1>
    <p>RoyalFlavours is your premier destination for delicious food, delivered fast and fresh right to your doorstep. We pride ourselves on quality ingredients and exceptional service.</p>
    <p>Choose us for your next meal and experience the Royal difference!</p>
  </main>

  <footer>
    <div class="container">
      <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9极Yczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
      <div class="social-links">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">Instagram</a>
      </div>
      <p>© 2024 RoyalFlavours. All rights reserved.</p>
      <p>Made by Alan Benny</p>
    </div>
  </footer>
</body>
</html>

### `contact.html`
- User contact and feedback form.
  <!DOCTYPE html>
<html lang="en">
<head>
  <title>RoyalFlavours - Contact</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="css/style.css" rel="stylesheet">
</head>
<body>
  <header>
    <div class="container">
      <div style="display: flex; align-items: center; justify-content: space-between;">
        <div style="display: flex; align-items: center;">
          <a href="极ndex.html">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
          </a>
        </div>
        <nav style="display: flex; align-items: center;">
          <a href="index.html" class="nav-link">Home</a>
          <a href="menu.html" class="nav-link">Menu</a>
          <a href="about.html" class="nav-link">About</a>
          <a href="contact.html" class="nav-link active">Contact</a>
          <a href="#" class="nav-link" style="color: var(--danger);">Cash on Delivery Only</a>
        </nav>
      </div>
    </div>
  </header>

  <main class="container">
    <h1>Contact Us</h1>
    <p>Have questions or feedback? Reach out to us!</p>
    <form style="max-width: 500px; margin: 0 auto;">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" required>
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" required>
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" rows="4" required></textarea>
      </div>
      <button type="submit" class="btn">Send Message</button>
    </form>
  </main>

  <footer>
    <div class="container">
      <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
      <div class="social-links">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">Instagram</a>
      </div>
      <p>© 2024 RoyalFlavours. All rights reserved.</p>
      <p>Made by Alan Benny</p>
    </div>
  </footer>
</body>
</html>


### `checkout.html`
- Captures customer details and order summary.
- LocalStorage-enabled order persistence.
  <!DOCTYPE html>
<html lang="en">
<head>
  <title>RoyalFlavours - Checkout</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="css/style.css" rel="stylesheet">
</head>
<body>
  <header>
    <div class="container">
      <div style="display: flex; align-items: center; justify-content: space-between;">
        <div style="display: flex; align-items: center;">
          <a href="index.html">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
          </a>
        </div>
        <nav style="display: flex; align-items: center;">
          <a href="index.html" class="nav-link">Home</a>
          <a href="menu.html" class="nav-link">Menu</a>
          <a href="about.html" class="nav-link">About</a>
          <a href="contact.html" class="nav-link">Contact</a>
          <a href="#" class="nav-link" style="color: var(--danger);">Cash on Delivery Only</a>
        </nav>
      </div>
    </div>
  </header>

  <main class="container">
    <h1>Checkout</h1>
    <div class="checkout-grid">
      <form id="checkout-form" onsubmit="submitOrder(event)">
        <div class="form-section">
          <h2>Contact Information</h2>
          <div class="form-group">
            <label for="full_name">Full Name *</label>
            <input type="text" id="full_name" name="full_name" required>
          </div>
          <div class="form-group">
            <label for="phone">Phone Number *</label>
            <input type="tel" id="phone" name="phone" required>
          </div>
        </div>

        <div class="form-section">
          <h2>Delivery Information</h2>
          <div class="form-group">
            <label for="address">Delivery Address *</label>
            <textarea id="address" name="address" required></textarea>
          </div>
          <div class="form-group">
            <label for="city">City *</label>
            <input type="text" id="city" name="city" required>
          </div>
          <div class="form-group">
            <label for="postcode">Postcode *</label>
            <input type="text" id="postcode" name="postcode" required>
          </div>
        </div>

        <div class="form-section">
          <h2>Additional Information</h2>
          <div class="form-group">
            <label for="instructions">Delivery Instructions</label>
            <textarea id="instructions" name="instructions"></textarea>
          </div>
          <div class="form-group">
            <label for="special_requests">Special Requests</label>
            <textarea id="special_requests" name="special_requests"></textarea>
          </div>
        </div>

        <button type="submit" class="btn">Place Order</button>
      </form>

      <div class="order-summary">
        <h2>Your Order</h2>
        <div id="cart-items-preview"></div>
        <div id="cart-total-preview"></div>
      </div>
    </div>
  </main>

  <footer>
    <div class="container">
      <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
      <div class="social-links">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">Instagram</a>
      </div>
      <p>© 2024 RoyalFlavours. All rights reserved.</p>
      <p>Made by Alan Benny</p>
    </div>
  </footer>

  <script>
    // Load cart from localStorage
    const cart = JSON.parse(localStorage.getItem('cart')) || [];
    const cartItemsPreview = document.getElementById('cart-items-preview');
    const cartTotalPreview = document.getElementById('cart-total-preview');

    let total = 0;
    cartItemsPreview.innerHTML = '';
    cart.forEach(item => {
      total += item.price * item.quantity;
      cartItemsPreview.innerHTML += `
        <div class="cart-item">
          <span>${item.name} x${item.quantity}</span>
          <span>$${(item.price * item.quantity).toFixed(2)}</span>
        </div>
      `;
    });
    cartTotalPreview.textContent = `Total: $${total.toFixed(2)}`;

    // Save order and redirect
    function submitOrder(event) {
      event.preventDefault();
      // Save order data to localStorage
      const orderData = {
        order_id: Date.now(),
        items: cart,
        total: total,
        customer_name: document.getElementById('full_name').value,
        delivery_address: document.getElementById('address').value,
        city: document.getElementById('city').value,
        postcode: document.getElementById('postcode').value,
        phone: document.getElementById('phone').value,
        instructions: document.getElementById('instructions').value,
        special_requests: document.getElementById('special_requests').value
      };
      localStorage.setItem('order', JSON.stringify(orderData));
      // Clear cart and redirect
      localStorage.removeItem('cart');
      window.location.href = 'order-confirmation.html';
    }
  </script>
</body>
</html>


### `order-confirmation.html`
- Displays final order summary and downloadable receipt.
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Order Confirmed - RoyalFlavours</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="css/style.css" rel="stylesheet">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
</head>
<body>
  <header>
    <div class="container">
      <div style="display: flex; align-items: center; justify-content: space-between;">
        <div style="display: flex; align-items: center;">
          <a href="index.html">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
          </a>
        </div>
        <nav style="display: flex; align-items: center;">
          <a href="index.html" class="nav-link">Home</a>
          <a href="menu.html" class="nav-link">Menu</a>
          <a href="about.html" class="nav-link">About</a>
          <a href="contact.html" class="nav-link">Contact</a>
        </nav>
      </div>
    </div>
  </header>

  <main class="container">
    <div class="confirmation-message" id="capture">
      <h1>Order Confirmed! 🎉</h1>
      <div class="order-details">
        <h3>Order Summary</h3>
        <div id="order-items"></div>
        <div class="receipt-total">
          <span>Total:</span>
          <span id="order-total"></span>
        </div>
        
        <h3 style="margin-top: 1.5rem;">Delivery Information</h3>
        <p id="delivery-address"></p>
      </div>
      
      <div class="button-group">
        <button onclick="downloadReceipt()" class="btn">Download Receipt</button>
        <a href="index.html" class="btn">Back to Home</a>
      </div>
    </div>
  </main>

  <footer>
    <div class="container">
      <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQs9ICmqwuJP95Kk3i9HyZjYczy-SULiZ7evCLwMxUX92mhq5GRzaXYsRMsQKXfs3qEVdhzOODWJ57VpRBfm_rGOts1rsRF9mcu1sNOT4GfvoAgjNWpe5EOtsn84E0Zrpb7lZsSknD0l8vnQqK1GDIXkE1qb7K4gJ21ksya-w3zUJqgyYs_V8RnmILOis/s3126/RFRoyal_flavours_sphere.png" alt="RoyalFlavours Logo" class="logo">
      <div class="social-links">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">Instagram</a>
      </div>
      <p>© 2024 RoyalFlavours. All rights reserved.</p>
      <p>Made by Alan Benny</p>
    </div>
  </footer>

  <script>
    // Load order from localStorage
    const orderData = JSON.parse(localStorage.getItem('order')) || {};
    const orderItems = document.getElementById('order-items');
    const orderTotal = document.getElementById('order-total');
    const deliveryAddressElement = document.getElementById('delivery-address');

    let total = 0;
    orderItems.innerHTML = '';
    (orderData.items || []).forEach(item => {
      total += item.price * item.quantity;
      orderItems.innerHTML += `
        <div class="receipt-item">
          <span>${item.name} x${item.quantity}</span>
          <span>$${(item.price * item.quantity).toFixed(2)}</span>
        </div>
      `;
    });
    orderTotal.textContent = `$${total.toFixed(2)}`;
    deliveryAddressElement.textContent = `${orderData.delivery_address || ''}, ${orderData.city || ''}, ${orderData.postcode || ''}`;

    // Download receipt as image
    function downloadReceipt() {
      html2canvas(document.querySelector("#capture"), {
        backgroundColor: '#1a1a1a',
        scale: 2
      }).then(canvas => {
        const link = document.createElement('a');
        link.download = `royalflavours-receipt-${Date.now()}.png`;
        link.href = canvas.toDataURL();
        link.click();
      });
    }
  </script>
</body>
</html>

---

## 🛒 Core JavaScript: `cart.js`

Handles cart initialization, item add/remove, quantity update, and localStorage operations.

```javascript
let cart = JSON.parse(localStorage.getItem('cart')) || [];

function addToCart(name, price) {
  const existing = cart.find(item => item.name === name);
  if (existing) existing.quantity++;
  else cart.push({ name, price: parseFloat(price), quantity: 1 });
  updateCart();
}

function updateCart() {
  localStorage.setItem('cart', JSON.stringify(cart));
  const cartItems = document.getElementById('cart-items');
  const cartTotal = document.getElementById('cart-total');
  if (!cartItems || !cartTotal) return;

  cartItems.innerHTML = '';
  let total = 0;
  cart.forEach(item => {
    total += item.price * item.quantity;
    cartItems.innerHTML += `<li>${item.name} x${item.quantity} 
    <button class="remove-item" data-name="${item.name}">×</button></li>`;
  });
  cartTotal.textContent = `Total: $${total.toFixed(2)}`;

  document.querySelectorAll('.remove-item').forEach(button => {
    button.addEventListener('click', removeCartItem);
  });
}

function removeCartItem(e) {
  const itemName = e.target.dataset.name;
  cart = cart.filter(item => item.name !== itemName);
  updateCart();
}

updateCart();
```

---

## 🚀 Deployment Guide

### Step 1: Launch EC2 Instance
- Instance Type: `t2.micro`
- OS: Amazon Linux 2023 or Ubuntu 22.04 LTS
- Security Group: Allow HTTP(80), HTTPS(443), SSH(22)

### Step 2: Connect to Instance
```bash
chmod 400 royalflavours-key.pem
ssh -i "royalflavours-key.pem" ec2-user@13.250.220.174
# Use 'ubuntu' if Ubuntu OS
```

### Step 3: Install Apache & Upload Files
```bash
# Amazon Linux
sudo yum update -y && sudo yum install httpd -y
# Ubuntu
sudo apt update && sudo apt install apache2 -y

# Upload or clone files
sudo git clone https://github.com/[yourusername]/royalflavours.git /var/www/html/

# Set permissions
sudo chown -R apache:apache /var/www/html     # For Amazon Linux
sudo chown -R www-data:www-data /var/www/html # For Ubuntu
sudo chmod -R 755 /var/www/html

# Start Apache
sudo systemctl start httpd     # Amazon Linux
sudo systemctl start apache2   # Ubuntu
sudo systemctl enable httpd
sudo systemctl enable apache2
```

### Step 4: Configure Apache Document Root
```apache
DocumentRoot "/var/www/html"
<Directory "/var/www/html">
    AllowOverride All
    Require all granted
</Directory>
```

### Step 5: Configure DNS (Namecheap)
- A Record:
  - Host: `@`
  - Value: `13.250.220.174`
- Optional CNAME:
  - Host: `www`
  - Value: `royalflavours.store`

### Step 6: Install SSL (Let's Encrypt)
```bash
# Amazon Linux
sudo yum install certbot python3-certbot-apache -y
# Ubuntu
sudo apt install certbot python3-certbot-apache -y

# Run Certbot
sudo certbot --apache -d royalflavours.store
```

---

## ✅ Verification

```bash
curl -I http://localhost
# Should return HTTP/1.1 200 OK
```

---

## 🛠 Troubleshooting

| Issue | Solution |
|-------|----------|
| Connection Refused | Verify EC2 security group |
| 403 Forbidden | Check file/folder permissions |
| Cart Not Saving | Enable localStorage in browser |
| SSL Issue | `sudo certbot renew` and restart Apache |

---

## 📅 Development Timeline

| Week | Milestone |
|------|-----------|
| 1    | HTML/CSS base setup |
| 2    | JS cart functionality |
| 3    | Checkout form and localStorage |
| 4    | EC2 deployment & domain integration |

---


## 🔗 References

- [AWS EC2 Docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/)
- [Certbot (Let's Encrypt)](https://certbot.eff.org/)
- [GitHub Docs](https://docs.github.com/)
- [Namecheap DNS Guide](https://www.namecheap.com/support/knowledgebase/article.aspx/319/2237/how-can-i-set-up-an-a-address-record-for-my-domain/)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
