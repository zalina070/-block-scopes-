# -block-scopes-
<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <title>Области видимости в JavaScript</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        
        .section {
            border: 2px solid #ccc;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
        }
        
        button {
            margin-top: 10px;
            padding: 8px 12px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <h2>🌐 Области видимости в JavaScript</h2>

    <div class="section">
        <h3>🌍 Global Scope (Международный закон)</h3>
        <p id="globalOutput"></p>
    </div>

    <div class="section">
        <h3>🏛️ Function Scope (Национальный закон)</h3>
        <button onclick="showFunctionScope()">Показать национальный закон</button>
        <p id="functionOutput"></p>
    </div>

    <div class="section">
        <h3>🏙️ Block Scope (Закон штата)</h3>
        <button onclick="showBlockScope()">Показать закон штата</button>
        <p id="blockOutput"></p>
    </div>

    <script>
        // Глобальная переменная
        let humanRight = "🌐 No slavery (Нет рабства)";
        document.getElementById("globalOutput").textContent = humanRight;

        // Функция с локальной переменной
        function showFunctionScope() {
            let drinkingAge = 21; // только внутри функции
            document.getElementById("functionOutput").textContent =
                `Must be ${drinkingAge} to drink 🍷 (Национальный закон)`;
        }

        // Функция с блочной переменной
        function showBlockScope() {
            if (true) {
                let barClosingTime = "2AM";
                document.getElementById("blockOutput").textContent =
                    `Bars must close at ${barClosingTime} 🕑 (Закон штата)`;
            }
        }
    </script>
</body>

</html>
