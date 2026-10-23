<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Discover timeless fashion, accessories and lifestyle essentials at FamaLuxe.">
  <title>FamaLuxe | Luxury Fashion</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    :root {
      --dark: #171713;
      --gold: #c5a46d;
      --cream: #f8f5ef;
      --white: #ffffff;
      --muted: #77776f;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--dark);
      background: var(--white);
      line-height: 1.6;
    }

    button, input {
      font: inherit;
    }

    button {
      cursor: pointer;
    }

    header {
      background: var(--dark);
      color: white;
    }

    .announcement {
      text-align: center;
      padding: 8px 12px;
      font-size: 11px;
      letter-spacing: 2px;
      background: #292920;
      color: #e5d5b5;
    }

    .navbar {
      min-height: 76px;
      max-width: 1200px;
      margin: auto;
      padding: 16px 24px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .logo {
      color: var(--gold);
      font-family: Georgia, serif;
      font-size: 29px;
      letter-spacing: 3px;
      font-weight: bold;
    }

    nav {
      display: flex;
      gap: 22px;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 13px;
    }

    nav a:hover {
      color: var(--gold);
    }

    .bag {
      border: 1px solid var(--gold);
      padding: 8px 13px;
      color: white;
      background: transparent;
      border-radius: 2px;
    }

    .hero {
      min-height: 470px;
      display: flex;
      align-items: center;
      padding: 60px max(7%, 24px);
      color: white;
      background:
        linear-gradient(90deg, rgba(15,15,12,.88), rgba(15,15,12,.22)),
        url("https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=1800&q=85")
        center 38% / cover no-repeat;
    }

    .hero-content {
      max-width: 570px;
    }

    .eyebrow {
      color: var(--gold);
      font-size: 12px;
      letter-spacing: 4px;
      text-transform: uppercase;
      margin-bottom: 18px;
    }

    h1 {
      font-family: Georgia, serif;
      font-size: clamp(38px, 6vw, 68px);
      line-height: 1.12;
      font-weight: normal;
      margin-bottom: 20px;
    }

    .hero p {
      max-width: 440px;
      color: #e6e3dc;
      margin-bottom: 28px;
    }

    .primary-btn {
      display: inline-block;
      border: 1px solid var(--gold);
      background: var(--gold);
      color: #171713;
      text-decoration: none;
      padding: 12px 24px;
      font-weight: bold;
      font-size: 12px;
      letter-spacing: 1px;
    }

    .primary-btn:hover {
      background: #e1c798;
    }

    .benefits {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      text-align: center;
      gap: 18px;
      padding: 27px 20px;
      background: var(--cream);
    }

    .benefits strong {
      display: block;
      font-family: Georgia, serif;
      font-size: 17px;
      font-weight: normal;
    }

    .benefits span {
      font-size: 12px;
      color: var(--muted);
    }

    .shop {
      max-width: 1200px;
      margin: auto;
      padding: 70px 24px;
    }

    .section-heading {
      text-align: center;
      margin-bottom: 30px;
    }

    .section-heading p {
      color: var(--muted);
      font-size: 14px;
    }

    h2 {
      font-family: Georgia, serif;
      font-size: clamp(29px, 4vw, 40px);
      font-weight: normal;
      margin-bottom: 8px;
    }

    .tools {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
      margin-bottom: 28px;
    }

    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .filter-btn {
      background: white;
      border: 1px solid #ddd8cd;
      padding: 9px 14px;
      font-size: 12px;
    }

    .filter-btn.active,
    .filter-btn:hover {
      background: var(--dark);
      color: white;
      border-color: var(--dark);
    }

    .search {
      width: 230px;
      max-width: 100%;
      padding: 10px 12px;
      border: 1px solid #ddd8cd;
      outline-color: var(--gold);
    }

    .products {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 22px;
    }

    .product {
      min-width: 0;
    }

    .product-image {
      height: 280px;
      position: relative;
      overflow: hidden;
      background: var(--cream);
    }

    .product-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform .35s ease;
    }

    .product:hover img {
      transform: scale(1.05);
    }

    .tag {
      position: absolute;
      left: 10px;
      top: 10px;
      background: white;
      padding: 4px 8px;
      font-size: 10px;
      letter-spacing: 1px;
    }

    .product-info {
      padding: 14px 2px;
    }

    .product-info h3 {
      font-size: 15px;
      font-weight: normal;
      margin-bottom: 4px;
    }

    .category {
      color: var(--muted);
      font-size: 12px;
    }

    .price {
      margin: 8px 0 12px;
      font-weight: bold;
    }

    .add-btn {
      width: 100%;
      padding: 10px;
      background: white;
      border: 1px solid var(--dark);
      font-size: 12px;
      letter-spacing: 1px;
    }

    .add-btn:hover {
      background: var(--dark);
      color: white;
    }

    .empty {
      display: none;
      text-align: center;
      padding: 30px;
      color: var(--muted);
      grid-column: 1 / -1;
    }

    .story {
      background: var(--cream);
      padding: 65px 24px;
      text-align: center;
    }

    .story-inner {
      max-width: 650px;
      margin: auto;
    }

    .story p {
      color: #62625a;
      margin: 14px 0 24px;
    }

    footer {
      background: var(--dark);
      color: white;
      text-align: center;
      padding: 36px 20px;
    }

    footer .logo {
      margin-bottom: 12px;
    }

    footer p {
      color: #c9c7bd;
      font-size: 13px;
      margin: 5px;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: var(--dark);
      color: white;
      padding: 13px 22px;
      z-index: 10;
      display: none;
      box-shadow: 0 4px 20px #0002;
      width: max-content;
      max-width: 90%;
    }

    @media (max-width: 900px) {
      .products {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .product-image {
        height: 300px;
      }
    }

    @media (max-width: 520px) {
      .navbar {
        justify-content: center;
        text-align: center;
      }

      nav {
        justify-content: center;
        gap: 14px;
      }

      .hero {
        min-height: 430px;
        padding: 45px 22px;
      }

      .benefits {
        grid-template-columns: 1fr;
        gap: 20px;
      }

      .shop {
        padding: 48px 15px;
      }

      .tools {
        align-items: stretch;
      }

      .filters {
        width: 100%;
      }

      .search {
        width: 100%;
      }

      .product-image {
        height: 220px;
      }

      .products {
        gap: 14px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="announcement">
      DISCOVER YOUR STYLE · WELCOME TO FAMALUXE
    </div>

    <div class="navbar">
      <div class="logo">FamaLuxe</div>

      <nav>
        <a href="#home">Home</a>
        <a href="#shop">Shop</a>
        <a href="#story">Our Story</a>
      </nav>

      <button class="bag" onclick="showBag()">
        Bag (<span id="bag-count">0</span>)
      </button>
    </div>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="hero-content">
        <div class="eyebrow">Style with distinction</div>
        <h1>Luxury is in the details.</h1>
        <p>
          Discover timeless fashion and everyday essentials
          selected for those who appreciate elegance,
          confidence and individuality.
        </p>
        <a class="primary-btn" href="#shop">EXPLORE COLLECTION</a>
      </div>
    </section>

    <section class="benefits">
      <div>
        <strong>Timeless Style</strong>
        <span>Pieces made to inspire</span>
      </div>
      <div>
        <strong>Curated Collection</strong>
        <span>Style meets simplicity</span>
      </div>
      <div>
        <strong>Customer First</strong>
        <span>Your experience matters</span>
      </div>
    </section>

    <section class="shop" id="shop">
      <div class="section-heading">
        <div class="eyebrow">The FamaLuxe edit</div>
        <h2>Explore Our Collection</h2>
        <p>Find your next favourite piece.</p>
      </div>

      <div class="tools">
        <div class="filters">
          <button class="filter-btn active"
            onclick="setCategory('All', this)">All</button>
          <button class="filter-btn"
            onclick="setCategory('Fashion', this)">Fashion</button>
          <button class="filter-btn"
            onclick="setCategory('Accessories', this)">Accessories</button>
          <button class="filter-btn"
            onclick="setCategory('Lifestyle', this)">Lifestyle</button>
        </div>

        <input
          class="search"
          id="search"
          type="search"
          placeholder="Search products..."
          aria-label="Search products"
          oninput="renderProducts()">
      </div>

      <div class="products" id="products"></div>
    </section>

    <section class="story" id="story">
      <div class="story-inner">
        <div class="eyebrow">The FamaLuxe philosophy</div>
        <h2>Elegance. Confidence. You.</h2>
        <p>
          FamaLuxe is built around a simple idea:
          personal style should feel effortless.
          Explore thoughtfully selected pieces that
          bring a touch of sophistication to everyday life.
        </p>
        <a class="primary-btn" href="#shop">SHOP THE COLLECTION</a>
      </div>
    </section>
  </main>

  <footer>
    <div class="logo">FamaLuxe</div>
    <p>Timeless style for modern living.</p>
    <p>Contact: Replace this text with your business email.</p>
    <p>&copy; <span id="year"></span> FamaLuxe. All rights reserved.</p>
  </footer>

  <div class="toast" id="toast" role="status"></div>

  <script>
    const products = [
      {
        id: 1,
        name: "Classic Beige Blazer",
        category: "Fashion",
        price: 8500,
        tag: "BESTSELLER",
        image: "https://images.unsplash.com/photo-1591047139829-d91aecb6caea?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 2,
        name: "Elegant Everyday Outfit",
        category: "Fashion",
        price: 6200,
        tag: "NEW",
        image: "https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 3,
        name: "Minimalist Handbag",
        category: "Accessories",
        price: 4800,
        tag: "POPULAR",
        image: "https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 4,
        name: "Classic Wristwatch",
        category: "Accessories",
        price: 5500,
        tag: "TIMELESS",
        image: "https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 5,
        name: "Signature Sunglasses",
        category: "Accessories",
        price: 2800,
        tag: "ESSENTIAL",
        image: "https://images.unsplash.com/photo-1511499767150-a48a237f0083?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 6,
        name: "Modern Casual Sneakers",
        category: "Fashion",
        price: 7200,
        tag: "FEATURED",
        image: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 7,
        name: "Everyday Coffee Cup",
        category: "Lifestyle",
        price: 1200,
        tag: "SIMPLE LIVING",
        image: "https://images.unsplash.com/photo-1514228742587-6b1558fcca3d?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 8,
        name: "Premium Travel Bag",
        category: "Lifestyle",
        price: 6500,
        tag: "TRAVEL",
        image: "https://images.unsplash.com/photo-1553062407-98eeb64c6a62?auto=format&fit=crop&w=700&q=80"
      }
    ];

    let selectedCategory = "All";
    let bag = [];

    const money = amount =>
      "Rs. " + amount.toLocaleString("en-PK");

    function renderProducts() {
      const container = document.getElementById("products");
      const searchTerm = document.getElementById("search")
        .value.trim().toLowerCase();

      const filtered = products.filter(product => {
        const matchesCategory =
          selectedCategory === "All" ||
          product.category === selectedCategory;

        const matchesSearch =
          product.name.toLowerCase().includes(searchTerm) ||
          product.category.toLowerCase().includes(searchTerm);

        return matchesCategory && matchesSearch;
      });

      container.innerHTML = "";

      if (filtered.length === 0) {
        container.innerHTML =
          '<p class="empty" style="display:block">No matching products found.</p>';
        return;
      }

      filtered.forEach(product => {
        const card = document.createElement("article");
        card.className = "product";

        card.innerHTML = `
          <div class="product-image">
            <img
              src="${product.image}"
              alt="${product.name}"
              loading="lazy">
            <span class="tag">${product.tag}</span>
          </div>
          <div class="product-info">
            <h3>${product.name}</h3>
            <div class="category">${product.category}</div>
            <div class="price">${money(product.price)}</div>
            <button class="add-btn" data-product="${product.id}">
              ADD TO BAG
            </button>
          </div>
        `;

        card.querySelector(".add-btn").addEventListener("click", () => {
          addToBag(product.id);
        });

        container.appendChild(card);
      });
    }

    function setCategory(category, button) {
      selectedCategory = category;

      document.querySelectorAll(".filter-btn").forEach(item => {
        item.classList.remove("active");
      });

      button.classList.add("active");
      renderProducts();
    }

    function addToBag(id) {
      const product = products.find(item => item.id === id);
      bag.push(product);

      document.getElementById("bag-count").textContent = bag.length;
      showToast(product.name + " added to your bag.");
    }

    function showBag() {
      if (bag.length === 0) {
        showToast("Your bag is empty. Explore our collection!");
        return;
      }

      const total = bag.reduce((sum, item) => sum + item.price, 0);
      const summary = bag.map(item => item.name).join(", ");

      alert(
        "YOUR FAMALUXE BAG\n\n" +
        summary +
        "\n\nItems: " + bag.length +
        "\nTotal: " + money(total) +
        "\n\nThis is a demo bag. Online checkout is not connected yet."
      );
    }

    let toastTimer;

    function showToast(message) {
      const toast = document.getElementById("toast");
      toast.textContent = message;
      toast.style.display = "block";

      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => {
        toast.style.display = "none";
      }, 2500);
    }

    document.getElementById("year").textContent =
      new Date().getFullYear();

    renderProducts();
  </script>

</body>
</html>
