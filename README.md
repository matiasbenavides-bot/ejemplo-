<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Convertidor USD a CLP</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f3f3f3;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #0072b1;
    }
    input {
      padding: 8px;
      width: 150px;
      font-size: 16px;
    }
    button {
      padding: 8px 15px;
      margin-left: 10px;
      font-size: 16px;
      background-color: #0072b1;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #005f91;
    }
    p {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <h1>💵 Convertidor USD → CLP</h1>
  
  <input id="dolares" type="number" placeholder="Ingresa dólares">
  <button onclick="convertir()">Convertir</button>

  <p id="resultado"></p>

  <script>
    function convertir() {
      const valorDolar = 1000; // Puedes actualizar el valor del dólar aquí
      const dolares = document.getElementById("dolares").value;
      
      if (dolares === "" || isNaN(dolares)) {
        document.getElementById("resultado").innerText = "Por favor, ingresa un número válido.";
        return;
      }

      const pesos = dolares * valorDolar;
      document.getElementById("resultado").innerText = `${dolares} USD son ${pesos.toLocaleString("es-CL")} CLP`;
    }
  </script>

</body>
</html>
