# dahuasecurity-pi
Pi Network Dahua Security App
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Dahua Security - Pi App</title>
  <script src="https://sdk.minepi.com/pi-sdk.js"></script>
</head>
<body>
  <h1>Dahua Security</h1>
  <button onclick="login()">Login with Pi</button>

  <script>
    Pi.init({ version: "2.0" });

    function login() {
      Pi.authenticate(
        ["username", "payments"],
        function(auth) {
          alert("Welcome " + auth.user.username);
        },
        function(error) {
          alert("Error: " + error);
        }
      );
    }
  </script>
</body>
</html>
