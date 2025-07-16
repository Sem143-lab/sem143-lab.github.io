 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Special For You 💌</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
  <style>
    body {
      background: linear-gradient(to right, #ffecd2, #fcb69f);
      font-family: 'Arial', sans-serif;
      text-align: center;
      padding-top: 500px;
    }

    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .heading {
      font-family: 'Pacifico', cursive;
      font-size: 106px;
      color: #007BFF;
      text-shadow: 1 2 40px #007BFF;
      -webkit-text-stroke: 2px #0056b3;
      margin-bottom: 70px;
    }

    .envelope {
      width: 800px;
      height: 300px;
      background-color: #ff6f91;
      border-radius: 50px;
      box-shadow: 10px 20px 50px rgba(0, 0, 0, 0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 240px;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .envelope:hover {
      transform: scale(1.05);
    }

    #message {
      font-family: 'Pacifico', cursive;
      font-size: 70px;
      color: #d41a1a;
      margin-top: 90px;
      display: none;
    }

    .buttons {
      margin-top: 50px;
      display: none;
    }

    .buttons button {
      padding: 30px 60px;
      margin: 20px;
      font-size: 50px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 10px 20px 40px rgba(0,0,0,0.2);
      transition: background-color 0.3s;
    }

    .yes-btn {
      background-color: #28a745;
      color: white;
    }

    .yes-btn:hover {
      background-color: #218838;
    }

    .no-btn {
      background-color: #dc3545;
      color: white;
    }

    .no-btn:hover {
      background-color: #c82333;
    }
  </style>
</head>
<body>

  <!-- 🎵 Background Music -->
  <audio id="bgMusic" loop>
    <source src="Tuhi_Ye_Mujhko_Bata_De.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <div class="container">

    <!-- 💙 Welcome Heading -->
    <div class="heading">Welcome to Sandesh's web</div>

    <!-- 💌 Envelope Button -->
    <div class="envelope" onclick="showMessage()">
      <span>Click Me 💌</span>
    </div>

    <!-- 🥰 Main Message -->
    <p id="message">Do you like me? 😍</p>

    <!-- ❤️ Yes / 💔 No Buttons -->
    <div class="buttons" id="responseButtons">
      <button class="yes-btn" onclick="replyLove()">Yes ❤️</button>
      <button class="no-btn" onclick="redirectToWhatsApp()">No 💔</button>
    </div>
  </div>

  <script>
    function showMessage() {
      const audio = document.getElementById("bgMusic");
      const message = document.getElementById("message");
      const buttons = document.getElementById("responseButtons");

      audio.play().catch(() => {
        console.warn("Autoplay blocked. Playing after interaction.");
      });

      message.style.display = "block";
      buttons.style.display = "flex";
    }

    function replyLove() {
      const message = document.getElementById("message");
      message.innerText = "I love you too ❤️";
      document.getElementById("responseButtons").style.display = "none";

      // Redirect to WhatsApp with "Operation successful"
      window.location.href = "https://wa.me/917804072977?text=I%20Like You";
    }

    function redirectToWhatsApp() {
      // Redirect to WhatsApp with "Why you are not like me?"
      window.location.href = "https://wa.me/919407351379?text=I%20Dont%20Like%20You%3F";
    }

    window.onload = function () {
      const audio = document.getElementById("bgMusic");
      audio.play().catch(() => {
        // Music will play on click
      });
    };
  </script>

</body>
</html
