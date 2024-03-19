# JS-Calculator
A simple calculator programmed with javascript.

This project is purely javascript, run on a simple single html page.
DOM Content Loaded event listener fires off whenever the initial html document has completely loaded.
The next step is to set up variables that will be used to construct the calculator

After the document has loaded, we update the title for the document object: 'JavaScript Project'.

Variables:
const opts - an array containing the keys for the calculator and the values of the numbers
const spec - special function keys

const container - container holding the whole calculator
Add classes for classList and js styling(style), for the width & margin 
Then add the container to the body

construct elements:
const output  - for the screen area 
set text attribute for input and a class classList
style the width, lineHeight, fontSize and textAlign for the variable

Add the variable output to the container object

const main -  container with all the keys for the calculator
Add class classList and styling, width.
add it to the container object.

Add keys from the opts array
use forEach to iterate through all the keys and function to take the value from the array

add function btnMaker with the function to be evoked, addOutput

function addOutput which handles the button clicking event

function btnMaker, with text and myFunction parameters
create element btn. set attribute with type button and style the width, lineHeight, margin, fontSize.
Set the value and text content and event listener
Append the button to main

Output to screen logic
add char variable to addOutput function 
set the value output to the value of character selected. Displays the out put on calculator screen

Add equal sign for evaluation
add btnMaker for equal sign  and clear butons and pass it in the function
creat function for evaluation and clear, evalOutput and clrOutput

function evalOutput
make sure there is a value for evaluation, if no value set border to red
border is black by default
use eval to evaluate the output

function clrOutput
output value is blank ""

BUG FIXES
Decimal Handling
You can do 44.44.444 which is not possible
switches dec and  eva set as a default of false

if character is = decimal value set character as blank to not output another decimal and add red border for error if another decimal is clicked. Switch dec to true to prevent adding any more 
output.value += char; should come after the if else statement to preven clicking of an extra decimal character.

this makes it impossible to add decimal place to other numbers when evaluating...
use eva switch, if eva is true switch back to false allowing the adding of another decimal place
use include to check the character value within the spec array if there, set dec to false

Final Bug Fixes and Code Review
eva switch handles any button that might be clicked
Do not allow evaluation if eva is true: if an evaluation sgn has been clicked it shouldn't allow for evaluation

Function cOutput that takes the color
