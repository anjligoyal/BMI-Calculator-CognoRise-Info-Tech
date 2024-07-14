# BMI-Calculator-CognoRise-Info-Tech
HTML Structure:
Start by creating the basic HTML structure for your BMI calculator. You’ll need input fields for height and weight, along with a button to calculate BMI.
Here’s a simplified version of the HTML code:
HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>BMI Calculator</title>
</head>
<body>
    <h1>BMI Calculator</h1>
    <div class="input-container">
        <label for="height">Height (cm):</label>
        <input type="number" id="height" placeholder="Enter height in cm">
    </div>
    <div class="input-container">
        <label for="weight">Weight (kg):</label>
        <input type="number" id="weight" placeholder="Enter weight in kg">
    </div>
    <button id="calculate">Calculate BMI</button>
    <div id="result"></div>
    <script src="script.js"></script>
</body>
</html>
AI-generated code. Review and use carefully. More info on FAQ.
In this snippet:
We define input fields for height and weight.
The calculate button triggers the BMI calculation.
The result will be displayed in the <div id="result">.
CSS Styling:
Create a styles.css file to style your calculator. You can center it on the page, adjust fonts, colors, and layout.
For instance, you might want to style the input fields and center-align the entire calculator.
JavaScript Logic:
In your script.js file, write the JavaScript logic to calculate BMI.
Here’s a basic example:
JavaScript

const heightInput = document.getElementById('height');
const weightInput = document.getElementById('weight');
const calculateButton = document.getElementById('calculate');
const resultDiv = document.getElementById('result');

calculateButton.addEventListener('click', () => {
    const height = parseFloat(heightInput.value);
    const weight = parseFloat(weightInput.value);
    const bmi = weight / ((height / 100) ** 2); // BMI formula
    resultDiv.textContent = `Your BMI: ${bmi.toFixed(2)}`;
});
AI-generated code. Review and use carefully. More info on FAQ.
BMI Formula:
The BMI formula is: BMI = weight (kg) / (height (m))^2.
Make sure to convert height from centimeters to meters (divide by 100).
Displaying the Result:
When the user clicks the “Calculate BMI” button, compute the BMI and display it in the designated result area.
