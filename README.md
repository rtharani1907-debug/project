# Project Responsive Web Design using Bootstrap
# Date: 08-10-2025
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
```
pro.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>trend Store - Your Online Store</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <header>
    <nav class="navbar">
      <div class="logo">Trend store</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="shop.html">Shop</a></li>
        <li><a href="#">About</a></li>
        <li><a href="shop.html">Contact</a></li>
        <li><a href="#">Cart 🛒</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h1>Welcome to Trend Store</h1>
    <p>Discover the latest trends and deals!</p>
    <a href="shop.html" class="btn">Shop Now</a>
  </section>

  <section class="products">
    <h2>Featured Products</h2>
    <div class="product-grid">
      <div class="product-card">
        <img src="sneakers.png" alt="Product 1" />
        <h3>Stylish Sneakers</h3>
        <p>₹2,499</p>
        <button>Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="watch.png" alt="Product 2" />
        <h3>Smart Watch</h3>
        <p>₹3,999</p>
        <button>Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="earbuds.png" alt="Product 3" />
        <h3>Wireless Earbuds</h3>
        <p>₹1,799</p>
        <button>Add to Cart</button>
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; Trend Store 2025 . All rights reserved.</p>
  </footer>

</body>
</html>

shop.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Product Grid</title>
  <style>
    .product-card {
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 15px;
      transition: box-shadow 0.3s ease;
    }
    .product-card:hover {
      box-shadow: 0 0 10px rgba(0,0,0,0.15);
    }
    .product-image {
      height: 200px;
      object-fit: contain;
      margin-bottom: 10px;
    }
    .rating {
      color: #f5c518;
    }
  </style>
</head>
<body>
  <div class="container py-4">
    <h2 class="mb-4">Featured Products</h2>
    <div class="row row-cols-1 row-cols-md-3 g-4">
      
      
      <div class="col">
        <div class="product-card text-center">
          <img src="bag.png" class="product-image" alt="Product 1">
          <h5 class="mt-2">BAG</h5>
          <p class="text-success fw-bold">₹2,499</p>
          <p class="rating">★★★★☆ (4.2)</p>
          <button class="btn btn-primary">Add to Cart</button>
        </div>
      </div>

      <div class="col">
        <div class="product-card text-center">
          <img src="sandle.png" class="product-image" alt="Product 2">
          <h5 class="mt-2">SANDLES</h5>
          <p class="text-success fw-bold">₹5,999</p>
          <p class="rating">★★★★★ (4.8)</p>
          <button class="btn btn-primary">Add to Cart</button>
        </div>
      </div>

      <div class="col">
        <div class="product-card text-center">
          <img src="phone.png" class="product-image" alt="Product 3">
          <h5 class="mt-2">PHONE</h5>
          <p class="text-success fw-bold">₹1,299</p>
          <p class="rating">★★★☆☆ (3.9)</p>
          <button class="btn btn-primary">Add to Cart</button>
        </div>
      </div>

      <div class="col">
        <div class="product-card text-center">
          <img src="bottle.png" class="product-image" alt="Product 3">
          <h5 class="mt-2">WATER BOTTLE</h5>
          <p class="text-success fw-bold">₹1,299</p>
          <p class="rating">★★★☆☆ (3.9)</p>
          <button class="btn btn-primary">Add to Cart</button>
        </div>
      </div>

    </div>
  </div>
</body>
</html>

style.css


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #f9f9f9;
  color: #333;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #222;
  padding: 1rem 2rem;
  color: #fff;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}
.nav-links a {
  color: #fff;
  text-decoration: none;
}

.hero {
  text-align: center;
  padding: 4rem 2rem;
  background: linear-gradient(to right, #ff6a00, #ee0979);
  color: white;
}
.hero .btn {
  background-color: white;
  color: #ee0979;
  border: none;
  cursor: pointer;
  margin-top: 1rem;
}
.products {
  padding: 2rem;
}
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 2rem;
}
.product-card {
  background-color: white;
  padding: 1rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  text-align: center;
}
.product-card img {
  width: 200px;
  height: 200px;
  border-radius: 4px;
}
.product-card button {
  margin-top: 0.5rem;
  padding: 0.5rem 1rem;
  background-color: #ee0979;
  color: white;
  border: none;
  cursor: pointer;
}
footer {
  text-align: center;
  padding: 1rem;
  background-color: #222;
  color: white;
}

```
# OUTPUT:
![alt text](<Screenshot (97).png>)
![alt text](<Screenshot (81).png>)
![alt text](<Screenshot (82).png>)
![alt text](<Screenshot (83).png>)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
