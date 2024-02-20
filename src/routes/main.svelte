
    <script>
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
      </script>
      
      <style>
        /* styles.css */

div {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
select,
button {
  margin-bottom: 10px;
  padding: 8px;
  width: 100%;
  box-sizing: border-box;
}

button {
  background-color: magenta;
  color: #fff;
  cursor: pointer;
  border: none;
  border-radius: 5px;
  padding: 10px;
}

button:hover {
  background-color: darkmagenta;
}

input[readonly] {
  background-color: #f0f0f0;
  cursor: not-allowed;
}

      </style>
      <div>
        <!-- Label and input for the first value -->
        <label for="value1">Enter value 1:</label>
        <input type="number" bind:value={value1}>
        <br /><br />
      
        <!-- Label and input for the second value -->
        <label for="value2">Enter Value 2:</label>
        <input type="number" bind:value={value2}>
        <br /><br />
      
        <!-- Select element for choosing the mathematical operation -->
        <label for="math">Choose an operation:</label>
        <select bind:value={operation} on:change={calculate}>
          <!-- Group for addition and subtraction operations -->
          <optgroup label="Add and Subtract">
            <option value="add">+</option>
            <option value="sub">−</option>
          </optgroup>
          <!-- Group for division and multiplication operations -->
          <optgroup label="Divide and Multiply">
            <option value="div">÷</option>
            <option value="mult">×</option>
          </optgroup>
        </select>
        <!-- Button to trigger calculation -->
        <button on:click={calculate}>Calculate</button>
        <br /><br />
      
        <!-- Displaying the result -->
        <label for="result">Result:</label>
        <input type="number" bind:value={result} readonly>
      </div>