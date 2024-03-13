# Svelte Styled Calculator App

This project is a Svelte-based calculator application with a stylish and responsive design. Users can input two values, select a mathematical operation from a dropdown menu, and calculate the result with a visually appealing interface.

## Table of Contents

- [JavaScript Logic](#javascript-logic)
- [CSS Styling](#css-styling)
- [User Interface](#user-interface)
- [Usage](#usage)
- [Important Notes](#important-notes)

## JavaScript Logic

The calculator logic is implemented in the `script.js` file. The `calculate` function processes arithmetic operations based on the selected operation (`add`, `sub`, `mult`, `div`). The result is dynamically updated.

```javascript
let value1 = 0;
let value2 = 0;
let operation = "add";
let result = 0;

function calculate() {
  switch (operation) {
    case "add":
      result = value1 + value2;
      break;
    case "sub":
      result = value1 - value2;
      break;
    case "mult":
      result = value1 * value2;
      break;
    case "div":
      result = value1 / value2;
      break;
    default:
      result = 0;
  }
}
```

## CSS Styling

The styling is defined in the `styles.css` file, enhancing the visual appeal of the calculator. It includes styles for the container, labels, input fields, dropdown, button, and result display.

```css
div {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

/* ... other styles ... */
```

## User Interface

The user interface is designed for a seamless user experience. It includes input fields for two values, a dropdown menu for selecting the operation, a "Calculate" button, and a readonly input field to display the result.

```html
<div class="max-w-400 mx-auto p-20 border border-gray-300 rounded shadow-md">
  <!-- ... input fields, dropdown, and result display ... -->
</div>
```

## Usage

1. Open the Svelte application in a web browser.
2. Input numerical values into the "Enter value 1" and "Enter value 2" fields.
3. Choose a mathematical operation from the dropdown menu.
4. Click the "Calculate" button to perform the selected operation.
5. The result will be dynamically displayed in the "Result" input field.

## Important Notes

- The application expects valid numerical inputs from the user.
- Division by zero is not handled in the provided code.
- The result is displayed directly in the input field without additional formatting or validation.

Explore and enjoy using this stylish calculator for basic arithmetic calculations!
