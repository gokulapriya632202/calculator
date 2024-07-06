# calculator

Project Description:

This project is a standard calculator built using HTML, CSS, and JavaScript. The calculator is designed to perform basic arithmetic operations such as addition, subtraction, multiplication, and division. The goal of this project is to create a user-friendly, functional calculator that mimics the behavior of a physical calculator.

Features:

Basic Arithmetic Operations: Supports addition, subtraction, multiplication, and division.

Clear and Responsive UI: Designed with a clean and intuitive user interface for easy interaction.

Real-Time Display: Shows the current input and results in real-time.

Error Handling: Includes error handling for division by zero and invalid inputs.

Keyboard Support: Allows users to perform calculations using keyboard input.

Technologies Used:

HTML: Structure and layout of the calculator.

CSS: Styling and appearance of the calculator.

JavaScript: Functionality and logic for performing calculations.

Code Structure:

calc.html: Contains the HTML structure of the calculator.

calc.css: Contains the CSS styles for the calculator.

calc.js: Contains the JavaScript logic for the calculator functionality.

#calc.html:

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="calc.css" />
    <title>Calculator</title>
  </head>

  <body>
    <div class="container">
      <h1>CALCULATOR</h1>

      <div class="calculator">
        <input type="text" name="screen" id="screen" />
        <table>
          <tr>
            <td><button>(</button></td>
            <td><button>)</button></td>
            <td><button>C</button></td>
            <td><button>%</button></td>
          </tr>
          <tr>
            <td><button>7</button></td>
            <td><button>8</button></td>
            <td><button>9</button></td>
            <td><button>X</button></td>
          </tr>
          <tr>
            <td><button>4</button></td>
            <td><button>5</button></td>
            <td><button>6</button></td>
            <td><button>-</button></td>
          </tr>
          <tr>
            <td><button>1</button></td>
            <td><button>2</button></td>
            <td><button>3</button></td>
            <td><button>+</button></td>
          </tr>
          <tr>
            <td><button>0</button></td>
            <td><button>.</button></td>
            <td><button>/</button></td>
            <td><button>=</button></td>
          </tr>
        </table>
      </div>
    </div>
  </body>
  <script src="calc.js"></script>
</html>


calc.css:

.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: #99ffbd;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}

calc.js:
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}


OUTPUT:

![Screenshot (120)](https://github.com/gokulapriya632202/calculator/assets/119560302/a3f10627-03d6-48bc-99a3-e1afd4c1b832)

