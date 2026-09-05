<!DOCTYPE html>
<html>

<head>
  <title>Invoice</title>
  <script>
    function totalinvoice() {
      let price = parseFloat(document.getElementById("price").value);
      let qty = parseInt(document.getElementById("qty").value);

      if (isNaN(price) || isNaN(qty)) {
        alert("enter a correct value");
        return;
      }

      let total = price * qty;

      let table = `
        <table border="1">
          <tr>
            <th>السعر</th>
            <th>الكمية</th>
            <th>المجموع</th>
          </tr>
          <tr>
            <td>${price}</td>
            <td>${qty}</td>
            <td>${total}</td>
          </tr>
        </table>
      `;

      document.getElementById("result").innerHTML = table;
    }
  </script>
</head>

<body>
  <h2>فاتورة مبيعات</h2>

  السعر:
  <input type="text" id="price"><br><br>

  الكمية:
  <input type="text" id="qty"><br><br>

  <button onclick="totalinvoice()">إنشاء الفاتورة</button>

  <div id="result"></div>
</body>

</html>
