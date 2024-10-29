<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login - Lindzee Top 5 Private</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f5f5f5;
        }
        .login-container, .fan-card {
            width: 300px;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
            display: none;
        }
        .login-container.active, .fan-card.active {
            display: block;
        }
        .login-container h2 {
            font-size: 1.5em;
            color: #333;
            margin-bottom: 20px;
        }
        .login-container input, .login-container button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .login-container button {
            background-color: #333;
            color: #ffffff;
            border: none;
            cursor: pointer;
        }
        .login-container button:hover {
            background-color: #555;
        }
        .show-password {
            font-size: 0.9em;
            color: #555;
            cursor: pointer;
            display: inline-block;
            margin-top: -10px;
        }
        .forgot-password {
            font-size: 0.9em;
            color: #007bff;
            text-decoration: none;
            display: block;
            margin-top: 10px;
        }
        .forgot-password:hover {
            text-decoration: underline;
        }
        .fan-card img {
            width: 100%;
            height: auto;
            border-bottom: 2px solid #333;
        }
        .fan-card h2 {
            font-size: 1.5em;
            margin: 10px 0;
            color: #333;
        }
        .fan-card p.quote {
            font-style: italic;
            color: #777;
            padding: 0 15px;
        }
        .fan-card .details {
            padding: 15px;
            background-color: #f0f0f0;
        }
        .fan-card .details p {
            margin: 5px 0;
            color: #555;
        }
        .fan-card button {
            margin: 15px 0;
            padding: 10px 20px;
            border: none;
            background-color: #333;
            color: #ffffff;
            font-size: 1em;
            border-radius: 5px;
            cursor: pointer;
        }
        .fan-card button:hover {
            background-color: #555;
        }
        .error-message {
            color: red;
            display: none;
        }
    </style>
</head>
<body>
    <!-- Login Page -->
    <div class="login-container active" id="login-container">
        <h2>LINDZEE TOP 5 PRIVATE</h2>
        <input type="text" id="username" placeholder="Username">
        <input type="password" id="password" placeholder="Password">
        <label class="show-password">
            <input type="checkbox" onclick="togglePassword()"> Show Password
        </label>
        <button onclick="login()">Login</button>
        <a href="#" class="forgot-password">Forgot Password?</a>
        <p id="error-message" class="error-message">Invalid credentials, please try again.</p>
    </div>

    <!-- Fan Card Page -->
    <div class="fan-card" id="fan-card">
        <img src="/mnt/data/new id card .png" alt="Fan Profile Picture">
        <h2>James Beard</h2>
        <p class="quote">"MY STYLE MY WORLD"</p>
        <div class="details">
            <p>Age: 53</p>
            <p>Fan Code: XX8679T-N</p>
            <p>Fan Status: Private 3 of 5</p>
            <p>Contact Preference: Phone - 512*****18</p>
        </div>
        <button>Connect</button>
    </div>

    <script>
        function togglePassword() {
            const passwordField = document.getElementById('password');
            passwordField.type = passwordField.type === 'password' ? 'text' : 'password';
        }

        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const errorMessage = document.getElementById('error-message');

            // Check credentials
            if (username === 'James') {
                if (password === '5125750618') {
                    // Hide login and show fan card
                    document.getElementById('login-container').classList.remove('active');
                    document.getElementById('fan-card').classList.add('active');
                    errorMessage.style.display = 'none';
                } else {
                    errorMessage.innerText = 'Incorrect password';
                    errorMessage.style.display = 'block';
                }
            } else {
                errorMessage.innerText = 'Incorrect username';
                errorMessage.style.display = 'block';
            }
        }
    </script>
</body>
</html>
