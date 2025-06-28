// チンチロ計算アプリ（レート可変・複数人対応・スマホ対応）
<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>チンチロ計算機（可変レート対応）</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 10px;
      padding: 10px;
    }
    input[type=number] {
      width: 60px;
      margin: 3px;
    }
    button {
      margin-top: 10px;
      padding: 10px;
      font-size: 16px;
    }
    h2, h4 {
      margin-bottom: 5px;
    }
    #results {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h2>チンチロ計算（レートと人数設定可）</h2>

  <label>レート（円）:<br><input type="number" id="rate" value="1000" min="1"></label><br><br>
  <label>プレイヤー人数:<br><input type="number" id="numPlayers" value="2" min="2"></label><br><br>
  <label>親の番号（1〜人数）:<br><input type="number" id="oyaIndex" value="1" min="1"></label><br><br>

  <div id="playersInput"></div>

  <button onclick="generateInputs()">プレイヤー入力欄を作成</button>
  <button onclick="calculateAll()">判定実行</button>

  <div id="results"></div>

  <script>
    function generateInputs() {
      const num = parseInt(document.getElementById('numPlayers').value);
      const container = document.getElementById('playersInput');
      container.innerHTML = '';
      for (let i = 1; i <= num; i++) {
        container.innerHTML += `<h4>プレイヤー${i}:</h4>
          <input type="number" id="p${i}_die1" min="1" max="6"> 
          <input type="number" id="p${i}_die2" min="1" max="6"> 
          <input type="number" id="p${i}_die3" min="1" max="6"><br><br>`;
      }
    }

    function calculateAll() {
      const rate = parseInt(document.getElementById('rate').value);
      const num = parseInt(document.getElementById('numPlayers').value);
      const oya = parseInt(document.getElementById('oyaIndex').value);
      const resultsDiv = document.getElementById('results');
      resultsDiv.innerHTML = '';

      let scores = [];

      for (let i = 1; i <= num; i++) {
        let d1 = parseInt(document.getElementById(`p${i}_die1`).value);
        let d2 = parseInt(document.getElementById(`p${i}_die2`).value);
        let d3 = parseInt(document.getElementById(`p${i}_die3`).value);

        const dice = [d1, d2, d3].sort();
        let text = '';
        let multiplier = 0;

        if (dice.some(d => isNaN(d) || d < 1 || d > 6)) {
          text = '⚠️ 入力不正';
        } else if (dice[0] === dice[1] && dice[1] === dice[2]) {
          multiplier = (dice[0] === 1) ? 5 : 3;
          text = (dice[0] === 1) ? 'ピンゾロ！（5倍）' : 'ゾロ目（3倍）';
        } else if (dice.includes(1) && dice.includes(2) && dice.includes(3)) {
          multiplier = -2;
          text = 'ヒフミ（負け、2倍支払い）';
        } else if (dice.includes(4) && dice.includes(5) && dice.includes(6)) {
          multiplier = 2;
          text = 'シゴロ（勝ち、2倍）';
        } else if (dice[0] === dice[1]) {
          multiplier = 1;
          text = `${dice[2]}の目（1倍）`;
        } else if (dice[1] === dice[2]) {
          multiplier = 1;
          text = `${dice[0]}の目（1倍）`;
        } else {
          multiplier = 0;
          text = '役なし（振り直し）';
        }

        scores.push({ player: i, multiplier: multiplier, text: text });
      }

      const oyaScore = scores[oya - 1];
      scores.forEach(score => {
        let result = `<h4>プレイヤー${score.player}</h4>${score.text}<br>`;
        if (score.player !== oya) {
          let diff = score.multiplier - oyaScore.multiplier;
          let money = rate * Math.abs(diff);
          if (diff > 0) {
            result += `→ 親から ${money}円 勝ち！`;
          } else if (diff < 0) {
            result += `→ 親に ${money}円 支払い…`;
          } else {
            result += '→ 引き分け';
          }
        } else {
          result += '(親)';
        }
        resultsDiv.innerHTML += result + '<hr>';
      });
    }
  </script>
</body>
</html>
