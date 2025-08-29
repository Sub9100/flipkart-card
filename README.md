flipkart-card-project/
├─ pages/
│  ├─ index.js           # Redirects to login
│  ├─ login.js           # Login page
│  ├─ dashboard.js       # Card + Fake Payment
├─ firebase.js           # Firebase config
├─ package.json
├─ next.config.js
└─ README.md




# flipkart-card
Flipkart card ssc html 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flipkart Style Card</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f1f3f6;
      font-family: Arial, sans-serif;
    }
    .card {
      width: 250px;
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      padding: 15px;
      text-align: center;
    }
    .card img {
      max-width: 100%;
      border-radius: 8px;
    }
    .title {
      font-size: 18px;
      font-weight: bold;
      margin: 10px 0;
    }
    .price {
      color: green;
      font-size: 16px;
      margin: 5px 0;
    }
    .btn {
      background: #2874f0;
      color: white;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .btn:hover {
      background: #0a4abf;
    }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://via.placeholder.com/200" alt="Product">
    <div class="title">Sample Product</div>
    <div class="price">₹999</div>
    <button class="btn">Add to Cart</button>
  </div>
</body>
</html>
