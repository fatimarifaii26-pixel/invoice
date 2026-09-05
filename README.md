
<html>

<head>
  <title>Invoice</title>
  <style>
    body {
 font-size: 24px; 
 font-family: Arial, sans-serif;
  margin: 0;
  font-family: "Amiri", serif;
  background-color: #f5f5dc; 
  color: #2f4f4f; 
  display: flex;
    justify-content: center; 
    align-items: center;     
    height: 100vh;           
    margin: 0;
    font-size: 24px;         
    font-family: Arial, sans-serif;
    background-color: #fffacd; 
  }

  .container {
    text-align: center; 
  }


  label, input, button {
    font-size: 24px; 
  }

.header {
  background-color: #2f4f4f;
  color: #f5f5dc;
  text-align: center;
  padding: 20px;
}

.logo {
  max-width: 120px;
  margin-bottom: 10px;
  background-color: rgb(126, 177, 160);
  border-top: none;
  border-color: black;
  border-radius: 2px;
  box-shadow: #a8dff1;
  border-style: dotted;
}

.nav {
  background-color: #3b5d5d;
  text-align: center;
  padding: 10px;
}

.nav a {
  color: #f5f5dc;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
}

.hero {
  
  padding: 50px 20px;
  background: linear-gradient(rgba(47,79,79,0.8), rgba(47,79,79,0.8)), url('mosque.jpg') center/cover no-repeat;
  color: #f5f5dc;
}

.hero h1 {
  font-size: 2.5em;
}

.btn {
  background-color: #f5f5dc;
  color: #2f4f4f;
  padding: 10px 20px;
  margin-top: 20px;
  border-radius: 5px;
  text-decoration: none;
  font-weight: bold;
  box-shadow: #cafafa;
}

.register {
  padding: 30px;
  text-align: center;
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: auto;
  
}

.register input, .register select, .register button {
  margin: 10px 0;
  padding: 10px;
  font-size: 1em;
}

.footer {
  background-color: #2f4f4f;
  color: #f5f5dc;
  text-align: center;
  padding: 15px;
  margin-top: 30px;
}

  </style>
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
    <div class="container">
  <h1>فاتورة مبيعات</h1>

  السعر:
  <input class="nav" type="text" id="price" placeholder="ادخل السعر"><br><br>

  الكمية:
  <input class="nav" type="text" id="qty" placeholder="ادخل الكمية المطلوبة"><br><br>

  <button class="btn" onclick="totalinvoice()">إنشاء الفاتورة</button>

  <div class="register" id="result"></div>
  </div>
</body>

</html>
