<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nagababu Platform</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f4f4f4;
            text-align: center;
        }

        header {
            background: #0078D7;
            color: white;
            padding: 20px;
        }

        .container {
            margin: 50px auto;
            width: 80%;
        }

        .card {
            background: white;
            padding: 20px;
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }

        footer {
            background: #222;
            color: white;
            padding: 15px;
            margin-top: 40px;
        }

        button {
            padding: 10px 20px;
            font-size: 18px;
            background: green;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: darkgreen;
        }
    </style>
</head>
<body>

<header>
    <h1>Welcome to Nagababu Platform</h1>
    <p>My First Website Hosted on Render</p>
</header>

<div class="container">

    <div class="card">
        <h2>About Me</h2>
        <p>Hello! I am Nagababu. I am learning HTML, CSS, JavaScript, Node.js, Express, MongoDB and Web Development.</p>
    </div>

    <div class="card">
        <h2>Projects</h2>
        <p>✔ Frontend Development</p>
        <p>✔ Backend Development</p>
        <p>✔ MongoDB Database</p>
        <p>✔ Apache Server</p>
    </div>

    <button onclick="showMessage()">Click Me</button>

    <p id="msg"></p>

</div>

<footer>
    <p>© 2026 Nagababu Platform. All Rights Reserved.</p>
</footer>

<script>
function showMessage() {
    document.getElementById("msg").innerHTML =
    "🎉 Welcome! Your website is running successfully on Render.";
}
</script>

</body>
</html>
