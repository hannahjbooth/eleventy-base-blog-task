---
title: More Loops, Arrays and Objects
description: 
date: 2024-07-11
tags:
  - JavaScript
  - Functions
---
A second, more practical session on Loops, Arrays and Objects involved two slightly more in depth exercises.


<h2>Title</h2>
<h3>Instructions</h3>


<h2>Task 1 - Shopping Cart</h2>
<h3>Instructions</h3>
<p>We are going to be using an array of objects provided as a simple shopping cart example.
We need to work out the total cost of the items in the shopping cart.</p>

<p><b>My code:</b><a href=""></a></p>
<div id="accordion">
    <!-- Part 1 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse1" aria-expanded="false" aria-controls="collapseExample">
                    Part 1
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse1">
        <div class="card card-body">
            <p>Create a function that takes 1 argument (the array)
            Create a variable inside the function called “totalPrice”
            Loop through each item in the array and add the value of the item to the total price, remember to account for the quantity.
            Return the totalPrice Variable
            Console.log the returned value</p>
            <p><b>My code:</b><a href="https://codepen.io/hannahbooth/pen/bGPNPzx" target="_blank">https://codepen.io/hannahbooth/pen/bGPNPzx</a></p>
        
        </div>
    </div>
    <!-- Part 2 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse2" aria-expanded="false" aria-controls="collapseExample">
                    Part 2
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse2">
        <div class="card card-body">
            <p>Create a function that takes 1 argument (the array)
            Create a variable inside the function called “totalPrice”
            Loop through each item in the array and add the value of the item to the total price, remember to account for the quantity. 
            If the item has a type of “food” the total price is 20% less
            Return the totalPrice Variable</p>
            <p><b>My code:</b><a href="https://codepen.io/hannahbooth/pen/qBzEzwq" target="_blank">https://codepen.io/hannahbooth/pen/qBzEzwq</a></p>
        
        </div>
    </div>
    <!-- Part 3 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse3" aria-expanded="false" aria-controls="collapseExample">
                    Part 3
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse3">
        <div class="card card-body">
            <p>Add 2 extra arguments to the function for “discountAmount” and “type”
            Replace the logic that takes off 20% for object.type == “food” for object.type == type and allow the 20% to be the {discountAmount}%
            Create logic so that if type == “any” all products have a discount applied</p>
            <p><b>My code:</b><a href="https://codepen.io/hannahbooth/pen/RwzNzXx" target="_blank">https://codepen.io/hannahbooth/pen/RwzNzXx</a></p>
        </div>
    </div>
    <!-- Part 4 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse4" aria-expanded="false" aria-controls="collapseExample">
                    Part 4
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse4">
        <div class="card card-body">
            <p>We are going to be using an array of objects provided as a simple shopping cart example.</p>
            <p>We need to be able to work out which items cost between 2 price points. So for example, we need the cart to be returned by which products cost more than £2 but less than £5.</p>
            <p>Create a function that has 3 arguments “cart”, “lowPrice” and “highPrice”</p>
            <p>Create an empty array called arrItems at the start of the function.</p>
            <p>Loop through each item of the array</p>
            <p>If the price value is higher than or equal to the lowPrice and lower than or equal to the highPrice push to arrItems</p>
            <p><b>My code:</b><a href="https://codepen.io/hannahbooth/pen/RwzNXbx" target="_blank">https://codepen.io/hannahbooth/pen/RwzNXbx</a></p>
        </div>
    </div>
    <!-- Part 5 -->
    <div class="card">
        <div class="card-header" id="headingOne">
            <h5 class="mb-0">
                <button class="btn" type="button" data-bs-toggle="collapse" data-bs-target="#collapse5" aria-expanded="false" aria-controls="collapseExample">
                    Part 5
                </button>
        </div>
    </div>
    <div class="collapse" id="collapse5">
        <div class="card card-body">
            <p>Add an additional argument to the function “quantity” this is going to be a boolean</p>
            <p>If quantity == true then account for the total price with the quantity included as being between lowPrice and highPrice</p>
            <p><b>My code:</b><a href="https://codepen.io/hannahbooth/pen/WNqbVNm" target="_blank">https://codepen.io/hannahbooth/pen/WNqbVNm</a></p>
        </div>
    </div>    
</div>

<h2>Task 2 - Mode, Median and Mean</h2>

<h3>Instructions</h3>
<p>We are going to be creating a function that is able to take all of the values of an array and return the average.</p>


Part 1
The function will be able to return the mode, median or mean of the numbers.

Create an array of random numbers
Create a function that takes 1 argument (the array) which can work out the mean of the numbers provided
Create a function which can work out the mode of the numbers provided
Create a function which can work out the median of the numbers provided
Part 2

Create a new function which takes 2 arguments (the array and a type variable).
Create a switch statement which has the cases ‘mode’, ‘median’ and ‘mean’
Copy and paste the functionality from your 3 previous functions into the case statement
Return the required number based on the arguments passed.

<h2>Title</h2>
<h3>Instructions</h3>
<h3>My code</h3>

```diff-js

```
<h3>My result</h3>