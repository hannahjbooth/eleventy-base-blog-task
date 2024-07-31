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


