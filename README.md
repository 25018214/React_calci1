
## Ex04 Simple Calculator - React Project

## Date:25/11/2026

## Name :Akash A

## Reg No :212225230008


## AIM

To develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM

# STEP 1

Create a React App.

# STEP 2

Open a terminal and run:

npx create-react-app simple-calculator
cd simple-calculator
npm start

# STEP 3

Inside the src/ folder, create a new file Calculator.js and define the basic structure.

# STEP 4

Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

# STEP 5

Create a new file Calculator.css in src/ and add the styling.

# STEP 6

Open src/App.js and modify it.

# STEP 7

Start the development server. npm start

# STEP 8

Open http://localhost:3000/ in the browser.

# STEP 9

Test the calculator by entering numbers and operations.

# STEP 10

Fix styling issues and refine content placement.

# STEP 11

Deploy the website.

# STEP 12

Upload to GitHub Pages for free hosting.

## PROGRAM

# css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #66b5ea, #4b9ca2);
}

.calculator {
  width: 350px;
  padding: 30px;
  background-color: rgb(255, 255, 255);
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
}

.calculator h1 {
  color: #333;
  margin-bottom: 10px;
}

.calculator p {
  color: gray;
  margin-bottom: 20px;
}

.calculator input {
  width: 100%;
  padding: 12px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 8px;
  font-size: 16px;
}

.buttons {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  margin: 20px 0;
}

.buttons button {
  flex: 1;
  padding: 12px;
  border: none;
  border-radius: 8px;
  background-color: #66d6ea;
  color: white;
  font-size: 22px;
  cursor: pointer;
}

.buttons button:hover {
  background-color: #4ca8c4;
}

.calculator h2 {
  margin: 20px 0;
  color: #333;
  overflow-wrap: anywhere;
}

.clear {
  width: 100%;
  padding: 12px;
  background-color: #e74c3c;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
}

.clear:hover {
  background-color: #c02b2b;
}
```
# jsx
```


import React, { useState } from "react";
import "./App.css";

function App() {
  const [num1, setNum1] = useState("");
  const [num2, setNum2] = useState("");
  const [result, setResult] = useState("");

  const calculate = (operator) => {
    const a = Number(num1);
    const b = Number(num2);

    if (num1 === "" || num2 === "") {
      setResult("Please enter both numbers");
      return;
    }

    switch (operator) {
      case "+":
        setResult(a + b);
        break;

      case "-":
        setResult(a - b);
        break;

      case "*":
        setResult(a * b);
        break;

      case "/":
        setResult(b === 0 ? "Cannot divide by zero" : a / b);
        break;

      default:
        setResult("");
    }
  };

  const clear = () => {
    setNum1("");
    setNum2("");
    setResult("");
  };

  return (
    <div className="container">
      <div className="calculator">
        <h1>Simple Calculator</h1>
        <p>Perform basic mathematical operations</p>

        <input
          type="number"
          placeholder="Enter first number"
          value={num1}
          onChange={(e) => setNum1(e.target.value)}
        />

        <input
          type="number"
          placeholder="Enter second number"
          value={num2}
          onChange={(e) => setNum2(e.target.value)}
        />

        <div className="buttons">
          <button onClick={() => calculate("+")}>+</button>
          <button onClick={() => calculate("-")}>-</button>
          <button onClick={() => calculate("*")}>×</button>
          <button onClick={() => calculate("/")}>÷</button>
        </div>

        <h2>Result: {result}</h2>

        <button className="clear" onClick={clear}>
          Clear
        </button>
      </div>
    </div>
  );
}

export default App;
```

## OUTPUT

![alt text](<Screenshot 2026-11-25 135031-1.png>)

![alt text](<Screenshot 2026-11-25 135057.png>)

## RESULT

The program for developing a simple calculator in React.js is executed successfully.