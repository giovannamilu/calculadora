# calculadora
calculadora com operações simples mas com ótima funcionalidade, feita com linguagens de html, css e javascript 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #87CEEB; /* Cor de fundo azul claro */
            color: #333; /* Cor do texto */
            margin: 0;
            padding: 0;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        .calculator {
            width: 300px;
            text-align: center;
            padding: 20px;
            border: 1px solid #ccc;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            background-color: white; /* Cor de fundo branca */
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            background-color: #f2f2f2; /* Cor de fundo cinza claro */
            color: #333; /* Cor do texto */
            border: none;
        }
        input[type="button"] {
            width: 50px;
            height: 50px;
            font-size: 18px;
            margin: 5px;
            background-color: #ff8c00; /* Cor laranja para números */
            color: white; /* Cor do texto branco */
            border: none;
        }
        .operator {
            background-color: #ff0000; /* Cor vermelha para operadores */
        }
        .footer {
            text-align: right;
            padding: 10px;
            font-weight: bold;
            color: #333; /* Cor do texto */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="calculator">
            <input type="text" id="display" readonly>
            <br>
            <input type="button" value="7" onclick="addToDisplay('7')">
            <input type="button" value="8" onclick="addToDisplay('8')">
            <input type="button" value="9" onclick="addToDisplay('9')">
            <input type="button" class="operator" value="/" onclick="addToDisplay('/')">
            <br>
            <input type="button" value="4" onclick="addToDisplay('4')">
            <input type="button" value="5" onclick="addToDisplay('5')">
            <input type="button" value="6" onclick="addToDisplay('6')">
            <input type="button" class="operator" value="*" onclick="addToDisplay('*')">
            <br>
            <input type="button" value="1" onclick="addToDisplay('1')">
            <input type="button" value="2" onclick="addToDisplay('2')">
            <input type="button" value="3" onclick="addToDisplay('3')">
            <input type="button" class="operator" value="-" onclick="addToDisplay('-')">
            <br>
            <input type="button" value="C" onclick="clearDisplay()">
            <input type="button" value="0" onclick="addToDisplay('0')">
            <input type="button" value="=" class="operator" onclick="calculate()">
            <input type="button" class="operator" value="+" onclick="addToDisplay('+')">
        </div>
        <div class="footer">
            Giovanna Milu
        </div>
    </div>
    <script>
        function addToDisplay(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = "";
        }

        function calculate() {
            try {
                document.getElementById("display").value = eval(document.getElementById("display").value);
            } catch (error) {
                document.getElementById("display").value = "Erro";
            }
        }
    </script>
</body>
</html>
