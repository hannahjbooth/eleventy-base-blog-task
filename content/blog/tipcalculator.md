---
title: Tip Calculator
description: This post shows a JavaScript learning exercise I completed.
date: 2024-07-06
tags:
  - JavaScript
---

In our first teaching session on JavaScript, we were introduced to variables and other basic programming concepts, such as data types, arithmetic operators, strings, concatenation and template literals. We were then assigned the following take-away task to complete and upload to our Eleventy blogs.

## Instructions

We’ll make a program to calculate a tip

01. Create variables for the pre-tip total and the tip percentage
02. Calculate the new total
03. Output a sentence to the page - something like: “Your total bill, with tip, is £35.45”. Extension: round the figure to 2 DP and display the tip amount.

## My code and results

{#
```diff-js
 // this is a command
 function myCommand() {
+  let counter = 0;
-  let counter = 1;
   counter++;
 }

 // Test with a line break above this line.
 console.log('Test');
#}

01. Create variables for the pre-tip total and the tip percentage
```diff-js
 // variables --- cost of the food order
 let preTip = 25;

 // variables --- tip percentages
 let tenPcTip = 0.1 * preTip;
 let fifteenPcTip = 0.15 * preTip;
 let twentyPcTip = 0.2 * preTip;
```

02. Calculate the new total
```diff-js
 // variables --- total amounts
 let tenTotal = tenPcTip + preTip;
 let fifteenTotal = fifteenPcTip + preTip;
 let twentyTotal = twentyPcTip + preTip;
```

03. Output a sentence to the page - something like: “Your total bill, with tip, is £35.45”
```diff-js
 // message printed on webpage
 document.write('Your bill (without a tip) is £ ' + preTip.toFixed(2) + '. ')
 document.write('Your total bill  with a 10% tip is £' + tenTotal.toFixed(2) + '. ');
 document.write('Your total bill  with a 15% tip  is £ ' + fifteenTotal.toFixed(2) + '. ');
 document.write('Your total bill  with a 20% tip  is £' + twentyTotal.toFixed(2) + '.');
```
Result on the page:
<div class=row></div>
<img class="col-12" src="/assets/images/page screenshot.png" alt="Screenshot of the result on the webpage">
</div>
<br><br>
Extra: I also displayed the calculator in the console with the following code:

```diff-js
 // console tip calculator
 console.log('Tip calculator');
 console.log(' ');
 console.log('3 options for service charge are 10%, 15% and 20%');
 console.log(' ');
 console.log('Total bill (without service charge) = £ '+ preTip.toFixed(2));
 console.log(' ');
 console.log('10%');
 console.log('Tip = £ '+ tenPcTip.toFixed(2));
 console.log('Total including tip = £' + tenTotal.toFixed(2));
 console.log(' ');
 console.log('15%');
 console.log('Tip = £ ' + fifteenPcTip.toFixed(2));
 console.log('Total including tip = £' + fifteenTotal.toFixed(2));
 console.log(' ');
 console.log('20%');
 console.log('Tip = £ ' + twentyPcTip.toFixed(2));
 console.log('Total including tip = £ '+ twentyTotal.toFixed(2)); 
```
Result in the console:
<div class=row></div>
<img class="col-12" src="/assets/images/console screenshot.png" alt="Screenshot of the result in the console">
</div>
