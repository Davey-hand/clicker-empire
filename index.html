
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clicker Empire</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #10152e, #30205b);
  color: white;
  text-align: center;
  min-height: 100vh;
}

header {
  padding: 28px 12px 10px;
}

h1 {
  font-size: 38px;
  margin: 0 0 8px;
}

p {
  color: #c9c9e8;
}

main {
  width: min(92%, 520px);
  margin: 20px auto;
}

.panel {
  background: #211e43;
  border: 1px solid #51447e;
  border-radius: 18px;
  padding: 22px;
  margin-bottom: 16px;
}

.coins {
  color: #ffe477;
  font-size: 38px;
  font-weight: bold;
  margin: 12px;
}

.score {
  color: #8dffcc;
  font-size: 28px;
  font-weight: bold;
  margin: 10px;
}

#clicker {
  width: 175px;
  height: 175px;
  border: 0;
  border-radius: 50%;
  background: linear-gradient(145deg, #ffe477, #ff9e39);
  font-size: 75px;
  cursor: pointer;
  box-shadow: 0 8px 0 #a95a28;
  transition: transform 0.1s;
}

#clicker:active {
  transform: scale(0.94);
  box-shadow: 0 3px 0 #a95a28;
}

.upgrade {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  text-align: left;
  margin-top: 12px;
  background: #302b59;
  border-radius: 12px;
  padding: 14px;
}

.upgrade button, .reset {
  border: 0;
  border-radius: 9px;
  padding: 11px 14px;
  background: #8d78ff;
  color: white;
  font-weight: bold;
  cursor: pointer;
}

.upgrade button:disabled {
  background: #56516d;
  cursor: not-allowed;
}

.small {
  font-size: 13px;
  color: #c9c9e8;
}

#message {
  min-height: 20px;
  color: #ffe477;
}

.notice {
  font-size: 12px;
  color: #aaa6d5;
}
</style>
</head>

<body>

<header>
  <h1>👑 Clicker Empire</h1>
  <p>Start with nothing. Build a fortune.</p>
</header>

<main>

  <section class="panel">
    <h2>⭐ Your Points</h2>
    <div class="score" id="points">0</div>
    <p>Personal high score: <b id="highScore">0</b></p>
    <p>Level: <b id="level">1</b></p>
    <p class="small">Points never decrease when you buy upgrades!</p>
  </section>

  <section class="panel">
    <p>Your spendable coins</p>
    <div class="coins">🪙 <span id="coins">0</span></div>
    <p>Per click: <b id="power">1</b> coins</p>
    <p>Automatic income: <b id="income">0</b> coins/second</p>

    <button id="clicker" onclick="earnCoins()">🪙</button>
    <p>Tap the coin to make money and earn points!</p>
    <p id="message"></p>
  </section>

  <section class="panel">
    <h2>🏪 Upgrade Shop</h2>

    <div class="upgrade">
      <div>
        <b>💪 Stronger Clicks</b>
        <div class="small">Earn more coins per click</div>
        <div class="small">Level: <span id="clickLevel">0</span></div>
      </div>
      <button id="clickBuy" onclick="buyUpgrade('click')">
        25 🪙
      </button>
    </div>

    <div class="upgrade">
      <div>
        <b>🏭 Coin Factory</b>
        <div class="small">Earn coins automatically</div>
        <div class="small">Level: <span id="factoryLevel">0</span></div>
      </div>
      <button id="factoryBuy" onclick="buyUpgrade('factory')">
        50 🪙
      </button>
    </div>

    <div class="upgrade">
      <div>
        <b>🚀 Money Multiplier</b>
        <div class="small">Double your click power</div>
        <div class="small">Level: <span id="multiplierLevel">0</span></div>
      </div>
      <button id="multiplierBuy" onclick="buyUpgrade('multiplier')">
        250 🪙
      </button>
    </div>
  </section>

  <section class="panel">
    <h2>🏆 Achievements</h2>
    <p id="bronze">🔒 Bronze: Earn 100 points</p>
    <p id="silver">🔒 Silver: Earn 1,000 points</p>
    <p id="gold">🔒 Gold: Earn 10,000 points</p>
  </section>

  <section class="panel">
    <h2>📊 Your Stats</h2>
    <p>Total points earned: <b id="totalPoints">0</b></p>
    <p>Total coins earned: <b id="totalCoins">0</b></p>
    <p>Coins per second: <b id="incomeStat">0</b></p>
    <button class="reset" onclick="resetGame()">Reset Game</button>
    <p class="notice">
      Your scores and progress are saved only in this browser
      on this device. They are not shared with other devices.
    </p>
  </section>

</main>

<script>
let game = {
  coins: 0,
  totalCoins: 0,
  points: 0,
  highScore: 0,
  clickLevel: 0,
  factoryLevel: 0,
  multiplierLevel: 0
};

function loadGame() {
  try {
    let saved = localStorage.getItem("clickerEmpire");

    if (saved) {
      let data = JSON.parse(saved);

      if (data && typeof data === "object") {
        for (let key in game) {
          if (Number.isSafeInteger(data[key]) &&
              data[key] >= 0) {
            game[key] = data[key];
          }
        }
      }
    }
  } catch (error) {
    console.log("Starting a new game.");
  }

  game.highScore = Math.max(game.highScore, game.points);
}

function saveGame() {
  try {
    localStorage.setItem("clickerEmpire", JSON.stringify(game));
  } catch (error) {
    console.log("Could not save progress.");
  }
}

function clickPower() {
  return (1 + game.clickLevel) *
    Math.pow(2, game.multiplierLevel);
}

function factoryIncome() {
  return game.factoryLevel * 2;
}

function earnCoins() {
  let amount = clickPower();

  game.coins += amount;
  game.totalCoins += amount;
  game.points += amount;

  document.getElementById("message").textContent =
    "+" + amount + " coins and points!";

  updateScreen();
}

function upgradeCost(type) {
  if (type === "click") {
    return Math.floor(25 * Math.pow(1.7, game.clickLevel));
  }

  if (type === "factory") {
    return Math.floor(50 * Math.pow(1.8, game.factoryLevel));
  }

  return Math.floor(250 * Math.pow(3, game.multiplierLevel));
}

function buyUpgrade(type) {
  let cost = upgradeCost(type);

  if (game.coins < cost) {
    document.getElementById("message").textContent =
      "Not enough coins yet!";
    return;
  }

  game.coins -= cost;

  if (type === "click") {
    game.clickLevel++;
  }

  if (type === "factory") {
    game.factoryLevel++;
  }

  if (type === "multiplier") {
    game.multiplierLevel++;
  }

  document.getElementById("message").textContent =
    "Upgrade purchased! Keep earning points.";

  updateScreen();
}

function updateScreen() {
  game.highScore = Math.max(game.highScore, game.points);

  document.getElementById("coins").textContent =
    Math.floor(game.coins).toLocaleString();

  document.getElementById("points").textContent =
    game.points.toLocaleString();

  document.getElementById("highScore").textContent =
    game.highScore.toLocaleString();

  document.getElementById("totalPoints").textContent =
    game.points.toLocaleString();

  document.getElementById("totalCoins").textContent =
    game.totalCoins.toLocaleString();

  document.getElementById("power").textContent =
    clickPower().toLocaleString();

  document.getElementById("income").textContent =
    factoryIncome().toLocaleString();

  document.getElementById("incomeStat").textContent =
    factoryIncome().toLocaleString();

  document.getElementById("clickLevel").textContent =
    game.clickLevel;

  document.getElementById("factoryLevel").textContent =
    game.factoryLevel;

  document.getElementById("multiplierLevel").textContent =
    game.multiplierLevel;

  document.getElementById("level").textContent =
    Math.floor(game.points / 100) + 1;

  document.getElementById("clickBuy").textContent =
    upgradeCost("click").toLocaleString() + " 🪙";

  document.getElementById("factoryBuy").textContent =
    upgradeCost("factory").toLocaleString() + " 🪙";

  document.getElementById("multiplierBuy").textContent =
    upgradeCost("multiplier").toLocaleString() + " 🪙";

  document.getElementById("clickBuy").disabled =
    game.coins < upgradeCost("click");

  document.getElementById("factoryBuy").disabled =
    game.coins < upgradeCost("factory");

  document.getElementById("multiplierBuy").disabled =
    game.coins < upgradeCost("multiplier");

  document.getElementById("bronze").textContent =
    game.points >= 100 ? "🥉 Bronze achievement unlocked!" :
    "🔒 Bronze: Earn 100 points";

  document.getElementById("silver").textContent =
    game.points >= 1000 ? "🥈 Silver achievement unlocked!" :
    "🔒 Silver: Earn 1,000 points";

  document.getElementById("gold").textContent =
    game.points >= 10000 ? "🥇 Gold achievement unlocked!" :
    "🔒 Gold: Earn 10,000 points";

  saveGame();
}

function resetGame() {
  if (confirm("Reset all coins, points, upgrades, and your high score?")) {
    game = {
      coins: 0,
      totalCoins: 0,
      points: 0,
      highScore: 0,
      clickLevel: 0,
      factoryLevel: 0,
      multiplierLevel: 0
    };

    updateScreen();

    document.getElementById("message").textContent =
      "A new empire begins!";
  }
}

loadGame();
updateScreen();

setInterval(function() {
  let earned = factoryIncome();

  if (earned > 0) {
    game.coins += earned;
    game.totalCoins += earned;
    game.points += earned;
    updateScreen();
  }
}, 1000);
</script>

</body>
</html>
