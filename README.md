<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .login-container {
      background: blur("blue");
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
      width: 300px;
    }
    .login-container h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }
    .login-container input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .login-container button {
      width: 100%;
      padding: 10px;
      background: #4facfe;
      border: none;
      border-radius: 5px;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    .login-container button:hover {
      background: rgb(red, green, blue);
    }
    .error {
      color: red;
      font-size: 14px;
      text-align: center;
    }
  </style>
</head>
<body background="istock.jpg">
  <div class="login-container">
    <h2>Login</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Username" required>
      <input type="password" id="password" placeholder="Password" required>
      <button type="submit">Login</button>
      <p class="error" id="errorMsg"></p>
    </form>
  </div>

  <script>
    const loginForm = document.getElementById("loginForm");
    const errorMsg = document.getElementById("errorMsg");

    loginForm.addEventListener("submit", function(event) {
      event.preventDefault();

      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      // Example validation (replace with real authentication logic)
      if (username == "admin" && password == "1234") {
        alert("Login successful!");
        window.location.href = "https://mail.google.com/mail/u/0/?tab=rm&ogbl"; // Redirect after login
      } else {
        errorMsg.textContent = "Invalid username or password!";
      }
    });
  </script>
</body>
</html>
