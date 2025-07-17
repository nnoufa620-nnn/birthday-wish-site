# birthday-wish-site 
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
  <title>Send Birthday Wish</title>
  <style>
    body { font-family: Arial; text-align: center; background-color: #ffeaea; padding: 30px; }
    input, textarea { margin: 10px; padding: 10px; width: 80%; }
    button { padding: 10px 20px; background: pink; border: none; font-size: 16px; }
  </style>
</head>
<body>
  <h1>🎉 Send a Birthday Wish 🎉</h1>
  <form id="wishForm">
    <input type="text" id="sender" placeholder="Your Name" required><br>
    <input type="text" id="receiver" placeholder="Recipient's Name" required><br>
    <textarea id="message" placeholder="Your Birthday Message" rows="4" required></textarea><br>
    <button type="submit">Create Wish</button>
  </form>

  <script>
    document.getElementById("wishForm").addEventListener("submit", function(e) {
      e.preventDefault();
      const sender = document.getElementById("sender").value;
      const receiver = document.getElementById("receiver").value;
      const message = document.getElementById("message").value;

      const url = `wish.html?sender=${encodeURIComponent(sender)}&receiver=${encodeURIComponent(receiver)}&message=${encodeURIComponent(message)}`;
      window.location.href = url;
    });
  </script>
</body>
</html>
