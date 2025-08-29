export default function Dashboard() {
  const handleFakePayment = (method) => {
    alert(`Payment Successful via ${method}!`);
  };

  return (
    <div style={{ textAlign: "center", marginTop: "50px" }}>
      <h1>Your Flipkart Card</h1>
      <p>Card Number: 1234 5678 9012 3456</p>
      <p>Expiry: 12/28</p>
      <p>CVV: 123</p>

      <h2>Make Payment</h2>
      <button onClick={() => handleFakePayment("UPI")}>Pay with UPI</button>
      <button onClick={() => handleFakePayment("Google Pay")}>Pay with Google Pay</button>
      <button onClick={() => handleFakePayment("PhonePe")}>Pay with PhonePe</button>
    </div>
  );
}




import { useState } from "react";
import { auth, provider } from "../firebase";
import { signInWithPopup } from "firebase/auth";
import { useRouter } from "next/router";

export default function Login() {
  const [phone, setPhone] = useState("");
  const router = useRouter();

  const handleGoogleLogin = async () => {
    try {
      await signInWithPopup(auth, provider);
      alert("Google Login Successful!");
      router.push("/dashboard");
    } catch (err) {
      alert("Login Failed!");
    }
  };

  const handlePhoneLogin = () => {
    alert(`Fake OTP sent to ${phone}. Logged in successfully!`);
    router.push("/dashboard");
  };

  return (
    <div style={{ textAlign: "center", marginTop: "100px" }}>
      <h1>Login</h1>
      <input
        type="text"
        placeholder="Enter Phone Number"
        value={phone}
        onChange={(e) => setPhone(e.target.value)}
      />
      <button onClick={handlePhoneLogin}>Login with Phone</button>
      <hr />
      <button onClick={handleGoogleLogin}>Login with Google</button>
    </div>
  );
}






{
  "name": "flipkart-card-project",
  "version": "1.0.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  },
  "dependencies": {
    "next": "13.5.0",
    "react": "18.2.0",
    "react-dom": "18.2.0",
    "firebase": "^10.10.0"
  }
}





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
