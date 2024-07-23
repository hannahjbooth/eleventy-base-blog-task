---
title: Functions & Control Flow
description: This post shows a JavaScript learning exercise I completed.
date: 2024-06-20
tags:
  - JavaScript
  - Functions
  - Functional Programming
  - Logic
---

Following our introduction to core programming concepts within JavaScript, we covered the notions of logic and control flow within the context of functional programming. We learnt to write and call functions, pass arguments to a function, and return values. We also learnt to apply logic to those arguments within the function in order to return a particular result, making use of variable scope, boolean values, if statements and comparison operators.

<h2>Practical Tasks</h2>
Here are four tasks I completed for this lesson. For the first three, you will find firstly my JavaScript code, and then how the result appears in the DevTools Console.
<br><br>
<h3>Task 1:</h3>
<p>Write a function that outputs a sentence. Then invoke that function later in your code.</p>

```diff-js
function writeSentence() {
  console.log(`This function writes sentences`);
}
writeSentence();
```
<div class=row>
<img class="col-12" src="/assets/images/fns-control-flow/task1.png" alt="Screenshot of the result in the DevTools Console">
</div>

<h3>Task 2:</h3>
<p>Write a simple program to combine a first name and a last name inside a function. Then update the function to accept a first and last name as arguments.</p>

```diff-js
function fullName(firstName, lastName) {
  console.log(`My name is ${firstName} ${lastName}`);
}
fullName('Hannah','Booth');
```
<div class=row>
<img class="col-12" src="/assets/images/fns-control-flow/task2.png" alt="Screenshot of the result in the DevTools Console">
</div>

<h3>Task 3:</h3>
<p>Add a return statement to your 'name' function. Use that function to set the value of a variable.</p>

```diff-js
function fullName(firstName = 'first', lastName = 'last') {
  return `My name is ${firstName} ${lastName}`;
}
let myName = (fullName('Hannah', 'Booth'));
console.log(myName);
```
<div class=row>
<img class="col-12" src="/assets/images/fns-control-flow/task3.png" alt="Screenshot of the result in the DevTools Console">
</div>

<h3>Task 4:</h3>

Update: Having learnt about the DOM since this lesson, I have upgraded my original code for this exercise, so as to integrate it to this page.

01. Make a variable called "temperature". Write some code that tells you to put on a coat if it is below 50 degrees.
02. Extend the Program to show the following:

<p>If it's less than 50 degrees, wear a coat.</p> 
<p>If it's less than 30 degrees, wear a coat and a hat.</p>
<p>If it's less than 0 degrees, stay inside.</p>
<p>Otherwise, just pants and vest is fine.</p>

03. Add a logical operator to your ‘Shall I wear a coat?’ program

<div id="task4">
  <form id="temperatureForm">
		<label for="temperature">Type a temperature (°C):</label>
		<input id="temperature" type="text">
	</form>

	<p>What to wear: <span id="instruction"></span></p>
</div>

<h4>The code:</h4>

Firstly, here is the function that returns an instruction according to the temperature inputted by the user:

```diff-js
whatClothes = (temperature) => {
  if (temperature < 0) {
    return 'Stay inside.';
  } else if (temperature < 50 && temperature > 30) {
    return 'Wear a coat and a hat.';
  } else if (temperature < 50) {
    return 'Wear a coat.';
  } else {
    return 'Just pants and a vest is fine.';
  }
}
```
Next, here is the logic which I've applied to a submit event listener on the user's input box, including the variables I created to make it work:

```diff-js
  // variable that holds the form
  const temperatureForm = document.forms.temperatureForm;

  // variable that holds the form input box	
  const temperatureInput = temperatureForm.elements.temperature;

  // variable that holds the span element which will display the final instruction
  const instructionSpan = document.getElementById("instruction");

  temperatureForm.addEventListener("submit", function(event) {
  // this form event listener will:

    // 1. prevent default behaviour
    event.preventDefault();

    // 2. clear the instruction span of any previous input
    instructionSpan.textContent = "";

    // 3. assign the inputted temperature to a variable
    var temperature = temperatureInput.value;
    console.log(temperature);

    // 4. pass this variable to the whatClothes function
    // 5. assign the result of the whatClothes function to a variable
    const whatToWear = whatClothes(temperature);

    // 6. create a text node which will display whatToWear
    const insertedInstruction = document.createTextNode(whatToWear);

    // 7. append text node to the span element set to display it
    instructionSpan.appendChild(insertedInstruction);

})

```
<script>

  // variable that holds the form
  const temperatureForm = document.forms.temperatureForm;

  // variable that holds the form input box
  const temperatureInput = temperatureForm.elements.temperature;

  // variable that holds the span element which will display the final instruction
  const instructionSpan = document.getElementById("instruction");

  // function that returns instruction according to inputted temperature
  whatClothes = (temperature) => {
    if (temperature < 0) {
      return 'Stay inside.';
    } else if (temperature < 50 && temperature > 30) {
      return 'Wear a coat and a hat.';
    } else if (temperature < 50) {
      return 'Wear a coat.';
    } else {
      return 'Just pants and a vest is fine.';
    }
  }

  temperatureForm.addEventListener("submit", function(event) {
    // form event listener will:

    // 1. prevent default behaviour
    event.preventDefault();

    // 2. clear the instruction span of any previous input
    instructionSpan.textContent = "";

    // 3. assign the inputted temperature to a variable
    var temperature = temperatureInput.value;
    console.log(temperature);

    // 4. pass this variable to the whatClothes function
    // 5. assign the result of the whatClothes function to a variable
    const whatToWear = whatClothes(temperature);

    // 6. create a text node which will display whatToWear
    const insertedInstruction = document.createTextNode(whatToWear);

    // 7. append text node to the span element set to display it
    instructionSpan.appendChild(insertedInstruction);

  })

</script>