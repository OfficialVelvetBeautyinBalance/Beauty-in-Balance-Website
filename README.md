# Beauty-in-Balance-Website
Official Beauty In Balance Clothing Brand Website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Beauty In Balance | Clothing Brand</title>
  <link rel="stylesheet" href="css/style.css">
  <script src="https://js.stripe.com/v3/"></script>
</head>
<body>
  <!-- Header -->
  <header>
    <h1>Beauty In Balance</h1>
    <nav>
      <a href="#shop">Shop</a>
      <a href="#contact">Contact</a>
      <button id="cart-btn">🛒 Cart (<span id="cart-count">0</span>)</button>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero">
    <h2>Fashion for Everyone</h2>
    <p>Unisex • Comfortable • Stylish</p>
    <a href="#shop" class="btn">Shop Now</a>
  </section>

  <!-- Products -->
  <section id="shop" class="products">
    <h2>Our Collection</h2>
    <div class="product-grid">

      <div class="product">
        <img src="images/men_tee.jpg" alt="Men Tee">
        <h3>Men Tee</h3>
        <p>$25</p>
        <button onclick="addToCart('Men Tee')">Add to Cart</button>
      </div>

      <div class="product">
        <img src="images/men_joggers.jpg" alt="Men Joggers">
        <h3>Men Joggers</h3>
        <p>$35</p>
        <button onclick="addToCart('Men Joggers')">Add to Cart</button>
      </div>

      <div class="product">
        <img src="images/women_tank.jpg" alt="Women Tank">
        <h3>Women Tank</h3>
        <p>$30</p>
        <button onclick="addToCart('Women Tank')">Add to Cart</button>
      </div>

      <div class="product">
        <img src="images/unisex_hoodie.jpg" alt="Unisex Hoodie">
        <h3>Unisex Hoodie</h3>
        <p>$45</p>
        <button onclick="addToCart('Unisex Hoodie')">Add to Cart</button>
      </div>

      <div class="product">
        <img src="images/unisex_tee.jpg" alt="Unisex Tee">
        <h3>Unisex Tee</h3>
        <p>$25</p>
        <button onclick="addToCart('Unisex Tee')">Add to Cart</button>
      </div>

    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <form name="contact" method="POST" data-netlify="true">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <!-- Cart Sidebar -->
  <aside id="cart-sidebar">
    <h2>Your Cart</h2>
    <ul id="cart-items"></ul>
    <p>Total: $<span id="cart-total">0</span></p>
    <button id="checkout-btn">Checkout</button>
    <button onclick="toggleCart()">Close</button>
  </aside>

  <script src="js/main.js"></script>
</body>
</html>
