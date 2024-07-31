---
title: More Functions & Control Flow
description: This post shows a JavaScript learning exercise I completed.
date: 2024-06-20
tags:
  - JavaScript
  - Functions
  - Functional Programming
  - Logic
---

In our second, more practical session on Functions & Control Flow, we worked on the three following tasks to push our learning and problem solving a little further.

<h2>Task 1 - Percentage Calculator</h2>
<h3>Instructions</h3>
<ul>
    <li><p>Create a function that is able to return a specific percentage of any number. For example you want to know what 30% of 135 is.</p></li>
    <li><p>Create a function named percentageCalculator</p></li>
    <li><p>Add 2 arguments for “number” and “percentage”</p></li>
    <li><p>Do the maths required to work out a percentage with the arguments</p></li>
    <li><p>Return the result of the maths</p></li>
    <li><p>Console.log the returned value</p></li>
</ul>

<h3>My result</h3>

<form id="percentageForm">
    <fieldset class="percentage">
        <legend>Percentage Calculator</legend>
        <label for="number">Number:</label><br>
        <input id="number" type="text"><br>
        <label for="percentage">Percentage:</label><br>
        <input id="percentage" type="percentage"><br>
        <button onclick="percentageCalculator(event)">Enter</button><br><br>
        <div class="resultElements">
            <label for="resultLabel">Result:</label>
            <p id="result"></p>
        </div>
    </fieldset>
</form>
<br>

<h3>My code</h3> 

```html
<form id="percentageForm">
    <fieldset class="percentage">
        <legend>Percentage Calculator</legend>
        <label for="number">Number:</label><br>
        <input id="number" type="text"><br>
        <label for="percentage">Percentage:</label><br>
        <input id="percentage" type="percentage"><br>
        <button onclick="percentageCalculator(event)">Enter</button><br><br>
        <div class="resultElements">
            <label for="resultLabel">Result:</label>
            <p id="result"></p>
        </div>
    </fieldset>
</form>
<script>
    function percentageCalculator(event) {
        event.preventDefault();
        var number = document.getElementById("number").value;
        var percentage = document.getElementById("percentage").value;
        var result = number / 100 * percentage; 
        console.log(percentage + '% of ' + number + ' is ' + result);
        document.getElementById("result").innerHTML = result;
    }   
</script>
```


<h2>Task 2 - Switch Statement</h2>
<h3>Instructions</h3>
<ul>
    <li><p>Customers can order 3 different types of drink and also select 3 sizes: Cola, Lemonade and Orangeade, and Small, Medium and Large</p></li>
    <li><p>The button they press have the values “cola”,”lemon”,”orange”</p></li>
    <li><p>Create a function that named drinkOrder will output the message “You have ordered a {size} of {softDrinkLabel}”</p></li>
    <li><p>Add 2 arguments for “size” and “drink”</p></li>
    <li><p>Use a switch statement to determine where the functional code needs to be written</p></li>
    <li><p>Create a message in each case statement to be returned</p></li>
    <li><p>Console.log the returned message</p></li>
</ul>

<h3>My result</h3>

<p>CodePen: <a href="https://codepen.io/hannahbooth/pen/BagpJON" target="_blank">https://codepen.io/hannahbooth/pen/BagpJON</a></p>


<h2>Task 3 - Calculator</h2>

<h3>Instructions</h3>
<ul>
    <li><p>We need to create a function capable of using the addition, subtraction, multiply, divider or modulus operator on 2 numbers provided.</p></li>
    <li><p>Create a function named calculator</p></li>
    <li><p>Add 3 arguments for “number1”, “number2” and “operator”</p></li>
    <li><p>Use a switch statement to determine which operator to use</p></li>
    <li><p>Add the math code for each operator in the case statement to return the value</p></li>
    <li><p>Console.log a message “{number1} {operator} {number2} = {value}”</p></li>
</ul>

<h3>My code</h3>

```js
function calculator(number1, operator, number2) {
    switch (operator) {
        case "+":
            console.log(`${number1} ${operator} ${number2} = ` + (number1 + number2));
            break;
        case "-":
            console.log(`${number1} ${operator} ${number2} = ` + (number1 - number2));
            break;
        case "x":
            console.log(`${number1} ${operator} ${number2} = ` + (number1 * number2));
            break;
        case ":":
            console.log(`${number1} ${operator} ${number2} = ` + (number1 / number2));
            break;
    }
}

calculator(1, "+", 2);
```

<h3>My result</h3>





<script>
    function percentageCalculator(event) {
        event.preventDefault();
        var number = document.getElementById("number").value;
        var percentage = document.getElementById("percentage").value;
        var result = number / 100 * percentage; 
        console.log(percentage + '% of ' + number + ' is ' + result);
        document.getElementById("result").innerHTML = result;
    }   
</script>