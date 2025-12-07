<!DOCTYPE html>
<html>
<head>
    <title>PadPros – Custom Mouse Pads</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <style>
        body {
            margin: 0;
            font-family: "Segoe UI", Arial, sans-serif;
            background: #f5f5f5;
        }

        header {
            background: linear-gradient(90deg, #111, #444);
            color: white;
            padding: 25px;
            text-align: center;
            font-size: 34px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        nav {
            background: #222;
            padding: 12px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 22px;
            font-size: 18px;
            transition: 0.2s;
            cursor: pointer;
        }

        nav a:hover {
            color: #00c8ff;
        }

        .page {
            display: none;
            max-width: 900px;
            margin: auto;
            background: white;
            padding: 35px;
            margin-top: 40px;
            border-radius: 14px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.15);
            animation: fadeIn 0.4s ease;
        }

        @keyframes fadeIn {
            from {opacity: 0; transform: translateY(10px);}
            to {opacity: 1; transform: translateY(0);}
        }

        h2 {
            font-size: 28px;
            color: #222;
            margin-top: 0;
        }

        p {
            font-size: 18px;
            line-height: 1.6;
        }

        input, textarea, button {
            width: 100%;
            padding: 14px;
            margin-top: 12px;
            border-radius: 8px;
            border: 1px solid #bbb;
            font-size: 16px;
        }

        button {
            background: #222;
            color: white;
            font-size: 18px;
            border: none;
            margin-top: 18px;
            transition: 0.25s;
        }

        button:hover {
            background: #00aaff;
        }

        .success {
            text-align: center;
            color: green;
            font-size: 22px;
            font-weight: bold;
            margin-top: 20px;
        }
    </style>

</head>
<body>

<header>PadPros</header>

<nav>
    <a onclick="showPage('home')">Home</a>
    <a onclick="showPage('about')">About</a>
    <a onclick="showPage('order')">Order</a>
    <a onclick="showPage('contact')">Contact</a>
</nav>

<!-- HOME PAGE -->
<div id="home" class="page" style="display:block;">
    <h2>Welcome to PadPros</h2>
    <p>
        PadPros creates premium, high-quality custom mouse pads designed exactly how you want them.
        Upload your design, enter your shipping info, and we will print and deliver your custom mouse pad straight to your home.
    </p>
    <p>
        Whether you need a gaming pad, a sports-themed pad, a gift, or a personal design — PadPros brings your ideas to life.
    </p>
</div>

<!-- ABOUT PAGE -->
<div id="about" class="page">
    <h2>About PadPros</h2>
    <p>
        PadPros specializes in custom mouse pads for gamers, students, creators, and professionals.
        Every pad is printed using high-resolution technology for crisp colors and long-lasting durability.
    </p>
    <p>
        Our mission is simple: to help you make your setup unique and stylish.  
        Your desk, your style — made by PadPros.
    </p>
</div>

<!-- ORDER PAGE -->
<div id="order" class="page">
    <h2>Order a Custom Mouse Pad</h2>
    <p>
        Fill out the form below to place your order. All order details will be emailed automatically to PadPros.
    </p>

    <form action="https://formsubmit.co/jakevoto10@gmail.com" method="POST" enctype="multipart/form-data">

        <!-- FormSubmit Settings -->
        <input type="hidden" name="_captcha" value="false">
        <input type="hidden" name="_template" value="box">
        <input type="hidden" name="_next" value="https://google.com">

        <label>Your Name</label>
        <input type="text" name="name" required>

        <label>Your Address</label>
        <textarea name="address" required></textarea>

        <label>Upload Your Custom Design</label>
        <input type="file" name="attachment" accept="image/*" required>

        <label>Extra Notes (Optional)</label>
        <textarea name="notes"></textarea>

        <button type="submit">Submit Order</button>
    </form>

    <p class="success">After submitting, your order will be sent directly to PadPros!</p>
</div>

<!-- CONTACT PAGE -->
<div id="contact" class="page">
    <h2>Contact PadPros</h2>
    <p><strong>Email:</strong> jakevoto10@gmail.com</p>
    <p><strong>Business Name:</strong> PadPros Custom Mouse Pads</p>
    <p>
        For questions, design help, or shipping information, email us anytime.
    </p>
</div>

<script>
    function showPage(pageId) {
        document.querySelectorAll('.page').forEach(page => {
            page.style.display = "none";
        });
        document.getElementById(pageId).style.display = "block";
        window.scrollTo(0, 0);
    }
</script>

</body>
</html>
