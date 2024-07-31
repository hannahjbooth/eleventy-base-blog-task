---
title: Pseudocode & Comments
description: This post shows a JavaScript learning exercise I completed.
date: 2024-06-27
tags:
  - Pseudocode
  - Comments
  - Modular Programming
  - Logic
  - DRY
---
<p>Learning about <b>pseudocode</b> when JavaScript was very new to me was incredibly helpful. Pseudocode serves to break down <b>logic</b> into both very granular and readable instructions, which in turn helps to understand a problem, and draft a solution. In the case of complex code, it can remain throughout in the form of <b>comments</b>.</p>
<p>As a very literal and granular thinker myself, applying this approach of breaking down the code into a modular sequence of single actions has really helped get to grips with JavaScript.</p>

<p>Below are two exercises I completed following our learning session. They required us to produce a pseudocode response to a challenge, and then use it to write the relevant code.</p>

<h2>Reading List</h2>

<h3>Instructions</h3>

<ul>
  <li><p>Keep track of which books you read and which books you want to read!</p></li>
  <li><p>Create an array of objects, where each object describes a book and has properties for the title (a string), author (a string), and already read (a boolean indicating if you read it yet).</p></li>
  <li><p>Iterate through the array of books. For each book, log the book title and book author like so: “The Hobbit by J.R.R. Tolkien”.</p></li>
  <li><p>Now use an if/else statement to change the output depending on whether you read it yet or not. If you read it, log a string like ‘You already read “The Hobbit” by J.R.R. Tolkien’, and if not, log a string like ‘You still need to read “The Lord of the Rings” by J.R.R. Tolkien.’</p></li>
</ul>

<h3>My pseudocode</h3>

```diff-js
 // LET an array contain:
 //     objects:
 //         describing a book
 //         containing properties for:
 //             the book's title (a string)
 //             the book's author (a string)
 //             whether the book has already been read (a boolean true/false)
 // ITERATE through the array
 //     IF book has been read
 //         LOG a string stating the title, the author, and that the book has been read
 //     IF book hasn't been read
 //         LOG a string stating the title, the author, and that the book still needs reading

```

<h3>My code</h3>

```diff-js
 // An array of objects each describing books
 let booksArray = [
    {title: `The Magician's Nephew`, author: `C. S. Lewis`, alreadyRead: true},
    {title: `The Lion, the Witch and the Wardrobev`, author: `C. S. Lewis`, alreadyRead: true},
    {title: `The Horse and His Boy`, author: `C. S. Lewis`, alreadyRead: true},
    {title: `Prince Caspian`, author: `C. S. Lewis`, alreadyRead: true},
    {title: `The Voyage of the Dawn Treader`, author: `C. S. Lewis`, alreadyRead: false},
    {title: `The Silver Chair`, author: `C. S. Lewis`, alreadyRead: false},
    {title: `The Last Battle`, author: `C. S. Lewis`, alreadyRead: false},
 ]

 // ITERATE through the array
 for (let book of booksArray) {
    // IF book has been read
    if (book.alreadyRead) {
        // Log a string stating the title, the author, and that the book has been read
        console.log(`You have already read ${book.title} by ${book.author}.`);
    // IF book hasn't been read    
    } else {
        // LOG a string stating the title, the author, and that the book still needs reading        
        console.log(`You still need to read ${book.title} by ${book.author}.`);
    }
 }
```
<h3>My result</h3>
<img class="books-screenshot" src="/assets/images/pseudocode-comments/books-pseudocode.png" alt="screenshot of result in console">

<h2>Recipe</h2>

<h3>Instructions</h3>

<p>Create an object to hold information on your favourite recipes. It should have properties for:</p>
<ul>
  <li><p>recipeTitle (a string)</p></li>
  <li><p>servings (a number)</p></li>
  <li><p>ingredients (an array of strings)</p></li>
  <li><p>directions (a string)</p></li>
</ul>
<p>List all recipes</p>

<p>Create a loop to list all the ingredients.</p>

<h3>My pseudocode</h3>

```diff-js
 // LET each recipe be stored in an object
 //    LET each object have properties:
 //        LET recipeTitle be a string
 //        LET servings be a number
 //        LET ingredients be an array of strings
 //        LET directions be a string
 //
 // LET each recipe object be stored in an array
 // LOOP through the array of recipes
 //    FOR each recipe
 //        LOG a string containing its title, servings and directions
 //
 // LOOP through the array of recipes
 //    FOR each recipe
 //        LOG its ingredients
```

<h3>My code</h3>

```diff-js
 // 5 recipe objects:
 let recipe1 = {
    recipeTitle: "Pancakes",
    servings: 4,
    ingredients: ["flour", "milk", "egg", "baking powder", "sugar", "salt"],
    directions: "Mix the dry ingredients. Add milk and eggs. Cook on a hot griddle until golden brown."
 };

 let recipe2 = {
    recipeTitle: "Caesar Salad",
    servings: 2,
    ingredients: ["romaine lettuce", "croutons", "parmesan cheese", "Caesar dressing"],
    directions: "Toss the lettuce with dressing. Add croutons and parmesan. Serve immediately."
 };

 let recipe3 = {
    recipeTitle: "Grilled Cheese Sandwich",
    servings: 1,
    ingredients: ["bread", "cheese", "butter"],
    directions: "Butter the bread. Place cheese between slices. Grill until the bread is golden brown and the cheese is melted."
 };

 let recipe4 = {
    recipeTitle: "Chicken Stir Fry",
    servings: 4,
    ingredients: ["chicken breast", "soy sauce", "vegetable oil", "broccoli", "carrot", "bell pepper", "garlic"],
    directions: "Cook the chicken in oil. Add vegetables and stir fry. Add soy sauce and cook until vegetables are tender."
 };

 let recipe5 = {
    recipeTitle: "Chocolate Chip Cookies",
    servings: 24,
    ingredients: ["flour", "baking soda", "salt", "butter", "sugar", "brown sugar", "vanilla extract", "egg", "chocolate chips"],
    directions: "Mix dry ingredients. Cream butter and sugars. Add egg and vanilla. Combine with dry ingredients and stir in chocolate chips. Bake at 350°F for 10-12 minutes."
};

 // array which stores all the recipe objects
 let recipesArray = [recipe1, recipe2, recipe3, recipe4, recipe5];

 // object to hold all the recipes (= the array of multiple recipes)
 let allRecipesObject = {
    recipes: recipesArray
};

 // For each recipe of the array of recipes
 for (let recipe of recipesArray) {
    // Log a string containing its title, servings and directions
    console.log(`Title: ${recipe.recipeTitle}, Servings: ${recipe.servings}, Directions: ${recipe.directions}`);

}
 // For each recipe of the array of recipes
 for (let recipe of recipesArray) {
    // Log its ingredients
    console.log(recipe.ingredients);
}
```
<h3>My result</h3>

<img class="recipes-screenshot" src="/assets/images/pseudocode-comments/recipes-pseudocode.png" alt="screenshot of result in the console">

<h2>Fix Start</h2>

<h3>Instructions</h3>

<p>Create a function called fixStart. It should take a single argument, a string, and return a version where all occurrences of its first character have been replaced with ‘*****’, except for the first character itself. You can assume that the string is at least one character long. For example:
</p>

<ul>
  <li><p>fixStart('babble'): 'ba**le'</p></li>
  <li><p>fixStart('turtle'): 'tur*le'</p></li>
</ul>

<h3>My pseudocode</h3>

```diff-js
 // LET function be named fixStart
 //     LET it take a single argument, a string
 //     LET the result of the function be stored in a variable named result
 //         LET result be assigned the first character of the argument
 //         LET the function add characters to result
 //             FOR each character of the argument from the second charater onwards
 //                 IF the character is identical to the first character of the argument
 //                     add the the string "*" to result
 //                 IF not
 //                     add the character to result
 //     RETURN result
 // LOG function with an argument
```


<h3>My code</h3>

```diff-js
 // LET the function fixStart take a word argument
 function fixStart(word) {
     // LET the result of the function be assigned to a variable which starts with the word argument's first character
     var result = word[0];
     // LOOP through the word argument's characters
     for (let i = 1 ; i < word.length ; i++) {
         // IF the word argument's character is identical to the word argument's first character
         if (word[i] == word[0]) {
             // ADD '*' to the result (in place of the character)
             result += '*'
         // IF the word argument's character is not identical to the word argument's first character
         } else {
             // ADD it to the result
             result += word[i];
         }
     }
     // RETURN the result once the iteration through the word argument has ended
     return result;
 }

 // LOG the function with a string as an argument
 console.log(fixStart("chicken"));
```

<h3>My result</h3>

<img class="fixstart-screenshot" src="/assets/images/pseudocode-comments/fixstart-pseudocode.png" alt="screenshot of result in the console">