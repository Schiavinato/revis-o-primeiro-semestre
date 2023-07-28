# revis-o-primeiro-semestre

<!DOCTYPE html>
<html>
<head>
  <style>
body {
    background-color: #f7f7f7;
    font-family: Arial, sans-serif;
    font-size: 16px;
    line-height: 1.5;
    margin: 0;
    padding: 0;
  }
  
  /* Estilo para o cabeçalho */
  h1 {
    color: #333;
    font-size: 36px;
    font-weight: bold;
    margin-bottom: 20px;
    text-align: center;
    text-transform: uppercase;
  }
  
  /* Estilo para os rótulos */
  label {
    display: inline-block;
    font-size: 18px;
    margin-bottom: 5px;
  }
  
  /* Estilo para as entradas de texto e números */
  input[type="text"], input[type="number"] {
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 18px;
    padding: 10px;
    width: 100%;
    
  }
  
  /* Estilo para o botão */
  button {
    background-color: #333;
    border: none;
    border-radius: 5px;
    color: #fff;
    cursor: pointer;
    font-size: 18px;
    margin-top: 10px;
    padding: 10px 20px;
    text-transform: uppercase;
    transition: background-color 0.2s ease-in-out;
    width: 100%;
  }
  
  button:hover {
    background-color: #555;
  }
  
  /* Estilo para o resultado */
  #resultado {
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 18px;
    margin-top: 20px;
    padding: 20px;
    text-align: center;
  }
  
  </style>
  <title>Ver sua idade</title>
  <meta charset="UTF-8">
  <script>
    function verificarFaseVida() {
      
      var nome = document.getElementById("nome").value;
      var idade = parseInt(document.getElementById("idade").value);

      
      if (idade <= 11) {
        var fase = "Criança";
      } else if (idade >= 12 && idade <= 20) {
        var fase = "Adolescente";
      } else if (idade >= 21 && idade <= 65) {
        var fase = "Adulto";
      } else {
        var fase = "Idoso";
      }

      
      document.getElementById("resultado").innerHTML = nome + ", você está na fase da vida: " + fase;
    }
  </script>
</head>
<body>
  <h1>Ver sua idade</h1>
  <label for="nome">Nome:</label>
  <input type="text" id="nome"><br>
  <label for="idade">Idade:</label>
  <input type="number" id="idade"><br>
  <button onclick="verificarFaseVida()">Verificar</button>
  <div id="resultado"></div>
</body>
</html>
