# MWAD-EXP_04-Simple-caluculator
## Date: 22.09.2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
calculator.jsx:

```
import React, { useState } from 'react';
import './calculator.css';

function Calculator() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setInput(eval(input).toString());
      } catch {
        setInput('Error');
      }
    } else if (value === 'C') {
      setInput('');
    } else {
      setInput(input + value);
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || '0'}</div>
      <div className="buttons">
        {['7','8','9','/','4','5','6','*','1','2','3','-','0','.','=','+','C'].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>{btn}</button>
        ))}
      </div>
    </div>
  );
}

export default Calculator;
```

calculator.css:

```
.calculator {
  width: 300px;
  margin: 50px auto;
  padding: 20px;
  background: #f4f4f4;
  border-radius: 10px;
  box-shadow: 0 0 10px #ccc;
}

.display {
  height: 50px;
  background: #222;
  color: #fff;
  font-size: 24px;
  text-align: right;
  padding: 10px;
  border-radius: 5px;
  margin-bottom: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 18px;
  color: #000;
  border: none;
  background: #eee;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background: #ddd;
}
```

App.jsx:

```
import { useState } from 'react'
import Calculator from './calculator'

function App() {

  return (
    <div className="App">
      <Calculator />
    </div>
  )
}

export default App
```
## OUTPUT

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/19757054-8e54-41c6-ad26-b0f5d4065f89" />

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/bd3c75ca-bf31-412e-a504-012d6f5b3886" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
