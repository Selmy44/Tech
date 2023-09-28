<!DOCTYPE html>
<html>
<head>
    <title>Temperature Measurement</title>
</head>
<body>
    <h1>Temperature Measurement</h1>
    
    <div id="temperatureDisplay">
        <p id="temperatureValue">--°C</p>
        <button id="getTemperatureButton">Get Temperature</button>
    </div>

    <script>
        // Function to generate a random temperature between -10°C and 40°C
        function getRandomTemperature() {
            return Math.floor(Math.random() * 51) - 10;
        }

        // Function to update the temperature display
        function updateTemperatureDisplay() {
            const temperatureValueElement = document.getElementById("temperatureValue");
            const temperature = getRandomTemperature();
            temperatureValueElement.textContent = temperature + "°C";
        }

        // Add a click event listener to the "Get Temperature" button
        const getTemperatureButton = document.getElementById("getTemperatureButton");
        getTemperatureButton.addEventListener("click", updateTemperatureDisplay);
    </script>

    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        h1 {
            color: #333;
        }

        #temperatureDisplay {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            padding: 20px;
            margin: 20px auto;
            width: 200px;
        }

        #temperatureValue {
            font-size: 24px;
            font-weight: bold;
        }

        #getTemperatureButton {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        #getTemperatureButton:hover {
            background-color: #0056b3;
        }
    </style>
</body>
</html>
