# BurgerShopLandingpage<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Burger Bliss - Taste the Joy</title>
  <style>
    /* Reset & base styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background-color: #fffdf7;
      color: #333;
    }

    a {
      text-decoration: none;
    }

    /* Navbar & Hero */
    .hero {
      background: url('https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      height: 100vh;
      position: relative;
      color: white;
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      background: rgba(0, 0, 0, 0.5);
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 25px;
    }

    .nav-links li a {
      color: white;
      font-weight: 500;
    }

    .hero-content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
    }

    .hero-content h1 {
      font-size: 3rem;
      margin-bottom: 15px;
    }

    .hero-content h1 span {
      color: #f8cb2e;
    }

    .hero-content p {
      font-size: 1.2rem;
      margin-bottom: 20px;
    }

    .cta-btn {
      background: #f8cb2e;
      color: #222;
      padding: 12px 25px;
      font-weight: bold;
      border-radius: 30px;
      transition: 0.3s;
      display: inline-block;
    }

    .cta-btn:hover {
      background: #ffd500;
      transform: scale(1.05);
    }

    /* About Section */
    .about-section {
      display: flex;
      flex-wrap: wrap;
      padding: 60px 10%;
      align-items: center;
      background: #fff;
    }

    .about-text {
      flex: 1;
      padding-right: 40px;
    }

    .about-text h2 {
      font-size: 2.2rem;
      margin-bottom: 15px;
    }

    .about-img img {
      max-width: 100%;
      border-radius: 12px;
    }

    /* Menu Section */
    .menu-section {
      background-color: #fef6e4;
      padding: 60px 10%;
      text-align: center;
    }

    .menu-section h2 {
      font-size: 2.2rem;
      margin-bottom: 30px;
    }

    .menu-grid {
      display: flex;
      gap: 30px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .menu-item {
      background: #fff;
      border-radius: 12px;
      padding: 20px;
      max-width: 250px;
      transition: all 0.4s ease;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      cursor: pointer;
    }

    .menu-item:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
    }

    .menu-item img {
      width: 100%;
      border-radius: 8px;
      transition: 0.4s ease;
    }

    .menu-item:hover img {
      filter: brightness(1.1);
    }

    /* CTA Section */
    .cta-section {
      background: #222;
      color: #fff;
      text-align: center;
      padding: 60px 20px;
    }

    .cta-section h2 {
      font-size: 2.2rem;
      margin-bottom: 20px;
    }

    .cta-section p {
      margin-bottom: 20px;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: #111;
      color: #ccc;
      font-size: 0.9rem;
    }

    /* Reviews Section */
    .reviews-section {
      background: #fefefe;
      padding: 40px 20px;
      text-align: center;
    }

    .reviews-section h2 {
      font-size: 1.8rem;
      margin-bottom: 20px;
      color: #222;
    }

    .reviews-marquee {
      overflow: hidden;
      position: relative;
      height: 60px;
      background: #fff9ec;
      border-top: 1px solid #ddd;
      border-bottom: 1px solid #ddd;
    }

    .review-track {
      display: flex;
      width: max-content;
      animation: scrollReviews 20s linear infinite;
    }

    .review {
      flex: none;
      padding: 0 50px;
      font-weight: 500;
      font-size: 1rem;
      color: #444;
      white-space: nowrap;
    }

    @keyframes scrollReviews {
      0% { transform: translateX(0); }
      100% { transform: translateX(-100%); }
    }

    /* Reveal animation for elements */
    .reveal {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.6s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        gap: 15px;
      }

      .about-section {
        flex-direction: column;
      }

      .about-text {
        padding-right: 0;
        margin-bottom: 30px;
      }

      .hero-content h1 {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <header class="hero">
    <nav>
      <div class="logo">🍔 Burger Bliss</div>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#order">Order Now</a></li>
      </ul>
    </nav>
    <div class="hero-content">
      <h1><span>Crafted</span> Burgers, <span>Unmatched</span> Flavor</h1>
      <p>Your new burger obsession starts here 🍟</p>
      <a href="#order" class="cta-btn">Order Now</a>
    </div>
  </header>

  <!-- About Section -->
  <section id="about" class="about-section">
    <div class="about-text reveal">
      <h2>Why Choose Us?</h2>
      <p>At Burger Bliss, we grill with passion and serve happiness in every bite. Made with 100% organic beef, hand-picked veggies, and secret sauces.</p>
    </div>
    <div class="about-img reveal">
      <img src="https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=800&q=80" alt="Burger Image">
    </div>
  </section>

  <!-- Menu Section -->
  <section id="menu" class="menu-section">
    <h2>Signature Burgers</h2>
    <div class="menu-grid">
      <div class="menu-item reveal">
        <img src="https://images.unsplash.com/photo-1550317138-10000687a72b?auto=format&fit=crop&w=600&q=80" alt="Classic Burger">
        <h3>Classic Bliss</h3>
        <p>Cheddar, lettuce, tomato, secret sauce</p>
      </div>
      <div class="menu-item reveal">
        <img src="https://images.unsplash.com/photo-1586190848861-99aa4a171e90?auto=format&fit=crop&w=600&q=80" alt="Spicy Burger">
        <h3>Blazing Hot</h3>
        <p>Jalapeños, chipotle mayo, double cheese</p>
      </div>
      <div class="menu-item reveal">
        <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80" alt="Veggie Burger">
        <h3>Green Goodness</h3>
        <p>Grilled mushroom, avocado, veggie patty</p>
      </div>
    </div>
  </section>

  <!-- Call to Action -->
  <section id="order" class="cta-section">
    <h2>Craving Already?</h2>
    <p>Order online and get it delivered hot and fresh to your doorstep.</p>
    <a href="#" class="cta-btn">Order on Zomato</a>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Burger Bliss. All rights reserved.</p>
  </footer>

  <!-- Reviews -->
  <section class="reviews-section">
    <h2>What Our Customers Say</h2>
    <div class="reviews-marquee">
      <div class="review-track">
        <div class="review">🔥 “Best burger I've ever had. Unreal!” – Rahul M.</div>
        <div class="review">🍔 “The Green Goodness is my new obsession!” – Sneha K.</div>
        <div class="review">⭐ “Tastes homemade, looks gourmet. Loved it.” – Arjun D.</div>
        <div class="review">😋 “Juicy, cheesy, spicy – total bliss!” – Tanya V.</div>
        <div class="review">👍 “Delivery was fast and the burger was still hot.” – Dev P.</div>
      </div>
    </div>
  </section>

  <!-- Script -->
  <script>
    // Scroll reveal effect
    const reveals = document.querySelectorAll(".reveal");

    window.addEventListener("scroll", () => {
      for (let el of reveals) {
        const windowHeight = window.innerHeight;
        const revealTop = el.getBoundingClientRect().top;
        const revealPoint = 150;

        if (revealTop < windowHeight - revealPoint) {
          el.classList.add("active");
        } else {
          el.classList.remove("active");
        }
      }
    });
  </script>
</body>
</html>
