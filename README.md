# TemperatureConvertor
# HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="task3.css">
</head>
<body>
    <header>
        <h1>Temperature Converter</h1>
    </header>

    <main>
        <div class="converter">
            <label for="celsius">Celsius</label>
            <input type="number" id="celsius" placeholder="Enter Celsius temperature">
            <button onclick="convertToFar()">Convert to Fahrenheit</button>
        </div>

        <div class="converter">
            <label for="fahrenheit">Fahrenheit</label>
            <input type="number" id="fahrenheit" placeholder="Enter Fahrenheit temperature">
            <button onclick="convertToCel()">Convert to Celsius</button>
        </div>
    </main>

    <script src="script3.js"></script>
</body>
</html>


# css

body, h1, label, input, button {
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

h1 {
    font-size: 30px;
    margin-bottom: 10px;
}

main {
    max-width: 400px;
    margin: 20px auto;
    padding: 20px;
    background-color: #fff;
}

.converter {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 10px;
}

input {
    display: block;
    padding: 10px;
    width: 100%;
    margin-bottom: 10px;
}

button {
    background-color: #333;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}



# JAVASCRIPT


function Convert() {
    var celsiusInput = document.getElementById("celsius");
    var fahrenheitInput = document.getElementById("fahrenheit");

    var celsius = parseFloat(celsiusInput.value);
    var fahrenheit = (celsius * 9/5) + 32;

    fahrenheitInput.value = fahrenheit.toFixed(2);
}

function convertToCel() {
    var celsiusInput = document.getElementById("celsius");
    var fahrenheitInput = document.getElementById("fahrenheit");

    var fahrenheit = parseFloat(fahrenheitInput.value);
    var celsius = (fahrenheit - 32) * 5/9;

    celsiusInput.value = celsius.toFixed(2);
}
