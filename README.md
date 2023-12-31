<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Year Greeting</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #000; /* Set background to black */
            color: #ffd700; /* Set text color to golden */
            text-align: center;
            margin: 0;
            padding: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        .container {
            max-width: 400px;
            padding: 20px;
            background-color: #000; /* Set container background to black */
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #ffd700; /* Set heading color to golden */
            font-size: 2em;
            margin-bottom: 20px;
        }

        input {
            width: calc(100% - 20px);
            padding: 10px;
            margin-bottom: 10px;
            box-sizing: border-box;
            border: 1px solid #ffd700; /* Set border color to golden */
            border-radius: 4px;
            font-size: 1em;
            color: #000; /* Set text color to black */
        }

        button {
            background-color: #ffd700; /* Set button background to golden */
            color: #000; /* Set button text color to black */
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1em;
        }

        button:hover {
            background-color: #cca800; /* Darken the hover color slightly for contrast */
        }

        .greeting {
            margin-top: 20px;
            font-size: 1.5em;
            color: #ffd700; /* Set greeting text color to golden */
        }

        #new-year-message {
            color: #ffd700; /* Set new year message color to golden */
            font-weight: bold;
            margin-bottom: 10px;
        }

        #user-name {
            color: #ffd700; /* Set user name color to golden */
        }
    </style>
</head>
<body>
    <div class="container" id="login-container">
        <h1>Login</h1>
        <form id="login-form" onsubmit="login(event)">
            <input type="text" id="name" name="name" placeholder="Your Name" required>
            <br>
            <input type="password" id="password" name="password" placeholder="Password" required>
            <br>
            <button type="submit">Login</button>
        </form>
    </div>

    <div class="container" id="greeting-container" style="display: none;">
        <div class="greeting" id="greeting-message">
            <p id="new-year-message">HAPPY NEW YEAR 2024 FROM MOHAMMED ZAID KANKUDTI</p>
            <p id="user-name"></p>
        </div>
    </div>

    <script>
        function login(event) {
            event.preventDefault();

            var loginContainer = document.getElementById("login-container");
            var greetingContainer = document.getElementById("greeting-container");
            var nameInput = document.getElementById("name");
            var passwordInput = document.getElementById("password");
            var greetingMessage = document.getElementById("greeting-message");
            var userNameElement = document.getElementById("user-name");

            if (passwordInput.value.toUpperCase() === "FAMILY") {
                // Display personalized greeting
                userNameElement.textContent = nameInput.value;
                greetingContainer.style.display = "block";
                loginContainer.style.display = "none";
            } else {
                alert("Incorrect password. Please try again.");
            }
        }
    </script>
