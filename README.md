# Online Calculator

## Description
This project demonstrates how to implement a simple online calculator using HTML, CSS, and JavaScript. The calculator can perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## Design
![image](https://github.com/ASD-Are/Online-Calculator/assets/93379106/ed57e691-cea9-4b2c-bb62-3b5f21a45acc)

### Step 1: Create the HTML Structure
- Define the basic structure of the calculator using HTML.
- Create a form with buttons for numbers and operations.


### Step 2: Style the Calculator with CSS
- Use CSS to style the calculator for a better user experience.
- Add styles for the table, buttons, and input fields.

### Step 3: Implement Calculator Logic with JavaScript
- Create functions to handle button clicks, clear the screen, and perform calculations.
  - `addToScreen(value)`: Appends the clicked button's value to the current value on the display screen.
  - `clearScreen()`: Clears the display screen.
  - `calculateResult()`: Evaluates the expression on the display screen and shows the result. Displays "Error" for invalid expressions.

## Implementation
### HTML
The HTML file defines the structure of the calculator. It includes a form with a table layout for buttons and an input field for the display.
First, lets create the HTML document in a code editor such as VS Code. We will use a table to organize the calculator's display and buttons. The key elements here are the `<table>, <tr> for rows, <td> for cells, and <input>` for the buttons and display screen. This structure helps us to easily layout the calculator interface. For different tags, we will use different column span to create the required layout" 
```plaintext
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
</head>
<body>
    <br/>
    <div>
        <form name="calculator">
            <table>
                <tr>
                    <th colspan="5"> <input type="textfield" id="screen" name="screen" value=""></th>
                </tr>
                <tr>
                    <td colspan="2"><input type="button" value="Clear" onclick="clearScreen()"></td>
                    <td> 
                        <input type="button" value="=" onclick="calculateResult()">
                    </td>
                    <td> 
                        <input type="button" value="(" onclick="addToScreen('(')">
                    </td>
                    <td> 
                        <input type="button" value=")" onclick="addToScreen(')')">
                    </td>
                </tr>
                <tr>
                    <td> 
                        <input type="button" value="*" onclick="addToScreen('*')">
                    </td>
                    <td>
                        <input type="button" value="/" onclick="addToScreen('/')">
                    </td>
                    <td>
                        <input type="button" value="+" onclick="addToScreen('+')">
                    </td>
                    <td>
                        <input type="button" value="-" onclick="addToScreen('-')">
                    </td>
                    <td>
                        <input type="button" value="." onclick="addToScreen('.')">
                    </td>
                </tr>
                <tr>
                    <td> <input type="button" value="1" onclick="addToScreen('1')">
                    </td>
                    <td> <input type="button" value="2" onclick="addToScreen('2')">
                    </td>
                    <td> <input type="button" value="3" onclick="addToScreen('3')">
                    </td>
                    <td> <input type="button" value="4" onclick="addToScreen('4')">
                    </td>
                    <td> <input type="button" value="5" onclick="addToScreen('5')">
                    </td>
                </tr>
                <tr>
                    <td> 
                        <input type="button" value="6" onclick="addToScreen('6')">
                    </td>
                    <td>            
                        <input type="button" value="7" onclick="addToScreen('7')">
                    </td>
                    <td>            
                        <input type="button" value="8" onclick="addToScreen('8')">
                    </td>
                    <td>            
                        <input type="button" value="9" onclick="addToScreen('9')">
                    </td>
                    <td>
                        <input type="button" value="0" onclick="addToScreen('0')">
                    </td>
                </tr>
            </table>
        </form>
    </div>
</body>
</html>

```

### CSS
We set a double border for the table, add spacing between elements, and margins for better layout.
```
<style>
        table {
            border: 2px double black;
            border-spacing: 10px;
        }
        tr {
            margin: 50px;
        }

    </style>
```
### Javascript
- addToScreen(value)
    - Description: Adds the specified value to the calculator screen.
    - Parameters:
        - value: The value to be added to the screen.

- clearScreen()
    - Description: Clears the calculator screen.
    - Example Usage:
  

- calculateResult()
    - Description: Calculates the result of the expression entered on the calculator screen. This function will use the eval() function to perform calculation on the value in the text field or it will raise an error.
   
```
 <script>
        function addToScreen(value) {
            var screen = document.getElementById("screen");
            screen.value += value;
        }

        function clearScreen() {
            document.getElementById("screen").value = "";
        }

        function calculateResult() {
            var screen = document.getElementById("screen");
            try {
                screen.value = eval(screen.value);
            } catch (error) {
                screen.value = "Error";
            }
        }
    </script>
```
### Requirements
- A web browser
- Code editor (e.g., VS Code)
![image](https://github.com/ASD-Are/Online-Calculator/assets/93379106/67249ca0-d646-432d-a1dc-a4c3b0aeba2c)


### Getting Started
To get a local copy up and running, follow these simple steps.

### Installation
1. Clone the repo
   ```sh
   git clone https://github.com/your-username/online-calculator.git
   ```
### Detail Design Presentation
[Online Calculator](https://docs.google.com/presentation/d/16SqyLfCqg1LEsncLdDXd0Ahd3FosdzBE8qV-jV2zhqI/edit?usp=sharing)

