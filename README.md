<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>حساب إجمالي النقود</title>
  <style>
    body { font-family: Tahoma; text-align: center; background-color: #f4f4f4; }
    .container { display: flex; flex-wrap: wrap; justify-content: center; }
    .box {
      width: 200px; margin: 10px; padding: 20px; border-radius: 10px;
      color: #fff; font-size: 18px;
    }
    #box200 { background-color: #e74c3c; }
    #box100 { background-color: #3498db; }
    #box50  { background-color: #2ecc71; }
    #box20  { background-color: #f39c12; }
    input { width: 80%; padding: 5px; margin-top: 10px; }
    #result { margin-top: 20px; font-size: 22px; color: #2c3e50; }
  </style>
</head>
<body>
  <h1>حاسبة النقود</h1>
  <div class="container">
    <div class="box" id="box200">
      <p>عدد أوراق 200 جنيه</p>
      <input type="number" id="num200" value="0" oninput="calculateTotal()">
    </div>
    <div class="box" id="box100">
      <p>عدد أوراق 100 جنيه</p>
      <input type="number" id="num100" value="0" oninput="calculateTotal()">
    </div>
    <div class="box" id="box50">
      <p>عدد أوراق 50 جنيه</p>
      <input type="number" id="num50" value="0" oninput="calculateTotal()">
    </div>
    <div class="box" id="box20">
      <p>عدد أوراق 20 جنيه</p>
      <input type="number" id="num20" value="0" oninput="calculateTotal()">
    </div>
  </div>
  <div id="result">الإجمالي: 0 جنيه</div>

  <script>
    function calculateTotal() {
      let num200 = document.getElementById("num200").value || 0;
      let num100 = document.getElementById("num100").value || 0;
      let num50  = document.getElementById("num50").value || 0;
      let num20  = document.getElementById("num20").value || 0;

      let total = (num200 * 200) + (num100 * 100) + (num50 * 50) + (num20 * 20);
      document.getElementById("result").innerText = "الإجمالي: " + total + " جنيه";
    }
  </script>
</body>
</html># -
