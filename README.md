# Calculator Web App

This is a simple calculator web application built using HTML, CSS, and JavaScript. It allows users to perform basic arithmetic operations like addition, subtraction, multiplication, and division.

## Features

- Addition
- Subtraction
- Multiplication
- Division
- Clear input

## File Structure

- `index.html`: The main HTML file containing the structure of the calculator.
- `style.css`: Contains the styling for the calculator.
- `script.js`: Contains the JavaScript code for the calculator's functionality.

## Usage

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/calculator.git
    ```

2. **Navigate to the project directory:**

    ```bash
    cd calculator
    ```

3. **Open the `index.html` file in your browser:**

    ```bash
    open index.html
    ```

## Code Explanation

### HTML

The HTML file defines the structure of the calculator, including the display and buttons for digits and operations.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>calculator</title>
    <style>
        div {
            background-color: rgb(0,0,0,0.5);
            width: 180px;
            padding: 10px;
        }
        input {
            width: 40px;
        }
        #s {
            width: 165px;
        }
    </style>
</head>
<body>
    <div>
        <form name="f">
            <input type="text" name="box" id="s"><br>
            <input type="button" value="1" onclick="f.box.value+=1">
            <input type="button" value="2" onclick="f.box.value+=2">
            <input type="button" value="3" onclick="f.box.value+=3">
            <input type="button" value="+" onclick="add()"><br>
            <input type="button" value="4" onclick="f.box.value+=4">
            <input type="button" value="5" onclick="f.box.value+=5">
            <input type="button" value="6" onclick="f.box.value+=6">
            <input type="button" value="-" onclick="sub()"><br>
            <input type="button" value="7" onclick="f.box.value+=7">
            <input type="button" value="8" onclick="f.box.value+=8">
            <input type="button" value="9" onclick="f.box.value+=9">
            <input type="button" value="*" onclick="mul()"><br>
            <input type="button" value="c" onclick="f.box.value=''">
            <input type="button" value="0" onclick="f.box.value+=0">
            <input type="button" value="=" onclick="f.box.value=eval(f.box.value)">
            <input type="button" value="/" onclick="di()">
        </form>
    </div>

    <script>
        function add() {
            let a = 0, b = 0;
            a = f.box.value;
            b = a.charAt(a.length-1);
            if (b == '+' || b == '-' || b == '*' || b == '/') {
                f.box.value = a.substring(0, a.length-1);
                f.box.value += '+';
            } else {
                f.box.value += '+';
            }
        }

        function sub() {
            let a = 0, b = 0;
            a = f.box.value;
            b = a.charAt(a.length-1);
            if (b == '+' || b == '-' || b == '*' || b == '/') {
                f.box.value = a.substring(0, a.length-1);
                f.box.value += '-';
            } else {
                f.box.value += '-';
            }
        }

        function mul() {
            let a = 0, b = 0;
            a = f.box.value;
            b = a.charAt(a.length-1);
            if (b == '+' || b == '-' || b == '*' || b == '/') {
                f.box.value = a.substring(0, a.length-1);
                f.box.value += '*';
            } else {
                f.box.value += '*';
            }
        }

        function di() {
            let a = 0, b = 0;
            a = f.box.value;
            b = a.charAt(a.length-1);
            if (b == '+' || b == '-' || b == '*' || b == '/') {
                f.box.value = a.substring(0, a.length-1);
                f.box.value += '/';
            } else {
                f.box.value += '/';
            }
        }
    </script>
</body>
</html>
```

### CSS

The CSS is included within the HTML file and styles the calculator's appearance.

### JavaScript

The JavaScript functions handle the calculator's arithmetic operations and ensure that only one operator is added at a time.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
