<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Gaming Page</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: linear-gradient(120deg, #1f1c2c, #928dab);
  color: white;
  text-align: center;
}

.header {
  padding: 30px;
  font-size: 30px;
  font-weight: bold;
}

.box {
  margin-top: 50px;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  background: yellow;
  font-weight: bold;
}

button:hover {
  background: orange;
}

#score {
  font-size: 25px;
  margin-top: 20px;
}

#result {
  font-size: 30px;
  margin-top: 20px;
}
</style>

</head>

<body>

<div class="header">🎮 Simple Gaming Page</div>

<div class="box">
  <h2>🔥 Click Game</h2>
  <p>Button চাপলে score বাড়বে 😎</p>

  <button onclick="playGame()">Click Me</button>

  <div id="score">Score: 0</div>
  <div id="result"></div>
</div>

<script>
let score = 0;

function playGame() {
  score++;

  document.getElementById("score").innerHTML = "Score: " + score;

  if(score % 5 === 0) {
    document.getElementById("result").innerHTML = "🎉 Level Up!";
  } else {
    document.getElementById("result").innerHTML = "👍 Keep Playing!";
  }
}
</script>

</body>
</html>