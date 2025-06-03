<!-- calculator.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Calculator</title>
  <style>
    input, button { margin: 5px; padding: 10px; font-size: 16px; }
  </style>
</head>
<body>
  <h2>Simple Calculator</h2>
  <input type="number" id="num1" placeholder="Number 1">
  <input type="number" id="num2" placeholder="Number 2"><br>
  <button onclick="calculate('+')">+</button>
  <button onclick="calculate('-')">-</button>
  <button onclick="calculate('*')">*</button>
  <button onclick="calculate('/')">/</button>
  <p id="result"></p>

  <script>
    function calculate(op) {
      const n1 = parseFloat(document.getElementById('num1').value);
      const n2 = parseFloat(document.getElementById('num2').value);
      let res = 0;
      if (op === '+') res = n1 + n2;
      if (op === '-') res = n1 - n2;
      if (op === '*') res = n1 * n2;
      if (op === '/') res = n1 / n2;
      document.getElementById('result').innerText = `Result: ${res}`;
    }
  </script>
</body>
</html>
