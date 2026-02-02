<!DOCTYPE html>
<html>
<head>
  <title>Hey You 💘</title>
  <style>
    body {
      background: linear-gradient(to bottom, #fff0f5, #ffd9e6);
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 80px;
      overflow: hidden;
    }
    h1 {
      color: #ff3366;
      font-size: 34px;
    }
    p {
      font-size: 22px;
      color: #444;
    }
    button {
      font-size: 20px;
      padding: 12px 30px;
      margin: 20px;
      border: none;
      border-radius: 14px;
      cursor: pointer;
    }
    #yes {
      background-color: #ff4d79;
      color: white;
      transition: transform 0.2s;
    }
    #yes:hover {
      transform: scale(1.1);
    }
    #no {
      background-color: #cfcfcf;
      position: absolute;
    }

    /* POPUP */
    #popup {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.6);
      display: none;
      align-items: center;
      justify-content: center;
    }
    #popupContent {
      background: #fff;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      animation: pop 0.4s ease;
    }
    @keyframes pop {
      0% { transform: scale(0.5); }
      100% { transform: scale(1); }
    }
  </style>
</head>

<body>

  <h1>Will you be my Valentine? 💕</h1>
  <p id="msg">Mujhe already lag raha hai tum YES hi bolne wali ho 😌</p>

  <button id="yes" onclick="yesClicked()">YES 😍</button>
  <button id="no" onclick="noClicked()">NO 🙄</button>

  <!-- POPUP -->
  <div id="popup">
    <div id="popupContent">
      <h1>❤️ I LOVE YOU ❤️</h1>
      <p>Bas kehna tha… aur ab keh diya 😌</p>
      <p>Forever starts here 💖</p>
    </div>
  </div>

  <script>
    let count = 0;
    const messages = [
      "Acha sach batao… thoda sa toh mann hai na 😏",
      "Itni cute ho, NO tumpe suit hi nahi karta 🥺",
      "Are you suree ?😞",
       "Dil todogi ka be 😩", 
      " mana icecream is better option  but what about chumii 👉🏻👈🏻",
      "Tum NO dabha rahi ho aur mera dil bhaag raha hai 💓",
      "Bas kar yaar… ab YES bol bhi do 😍"
    ];

    function noClicked() {
      const noBtn = document.getElementById("no");
      const msg = document.getElementById("msg");

      const x = Math.random() * (window.innerWidth - 120);
      const y = Math.random() * (window.innerHeight - 120);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";

      if (count < messages.length) {
        msg.innerText = messages[count];
      }
      count++;
    }

    function yesClicked() {
      document.getElementById("popup").style.display = "flex";
    }
  </script>

</body>
</html>
