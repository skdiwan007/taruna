<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For You ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
    }.card {
  background: white;
  padding: 30px 20px;
  border-radius: 20px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
  max-width: 350px;
  width: 90%;
  animation: fadeIn 1s ease;
}

h1 {
  color: #ff4b5c;
}

p {
  font-size: 18px;
  color: #444;
}

button {
  padding: 10px 20px;
  margin: 10px;
  border: none;
  border-radius: 20px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
}

.yes {
  background: #ff4b5c;
  color: white;
}

.yes:hover {
  background: #e63b4a;
}

.no {
  background: #ccc;
  color: #333;
}

.no:hover {
  background: #aaa;
}

.flowers {
  font-size: 40px;
  animation: float 2s infinite ease-in-out;
}

@keyframes fadeIn {
  from {opacity: 0; transform: scale(0.9);} 
  to {opacity: 1; transform: scale(1);} 
}

@keyframes float {
  0% {transform: translateY(0);} 
  50% {transform: translateY(-10px);} 
  100% {transform: translateY(0);} 
}

  </style>
</head>
<body> <div class="card" id="card">
    <h1>Hey Taruna ❤️</h1>
    <p id="question"> Can we start again?</p><div id="buttons">
  <button class="yes" onclick="yesClick()">Yes 😍</button>
  <button class="no" onclick="noClick()">No 🙈</button>
</div>

  </div> <script>
    let noCount = 0;

    const questions = [
      "Are you sure? 😢",
      "Please think again 🥺",
      "I’ll make you smile every day 💕",
      "Last chance... please? 😭",
      "Okay… one more time 😘"
    ];

    function noClick() {
      noCount++;

      if (noCount < questions.length) {
        document.getElementById("question").innerText = questions[noCount];
      } else {
        showFlowers();
      }
    }

    function yesClick() {
      document.getElementById("card").innerHTML = `
        <h1>Yayyy! 😍❤️</h1>
        <p>You just made me the happiest person! 💖</p>
        <div class="flowers">🌸🌹🌷🌺💐</div>
        <p>These flowers are for you 🌼</p>
      `;
    }

    function showFlowers() {
      document.getElementById("card").innerHTML = `
        <h1>I Still Love You 💔❤️</h1>
        <p>Even if you say no… you deserve flowers 🌸</p>
        <div class="flowers">🌹🌷🌺💐🌸</div>
        <p>Always special to me 💕</p>
      `;
    }
  </script></body>
</html>
