# Functions in JavaScript

## Defining functions:
JavaScript functions are defined with the function keyword. It can be used as a function declaration or a function expression. 
The construction of the function:
- The name of the function.
- A list of commands to the function, surrounded in parentheses and separated by commas.
- The JavaScript statements that define the function, enclosed in curly brackets, {...}.

_function nameOfTheFuntion(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}_

### Function Declaration:
To create a function we can use a function declaration.

_function funcName(params){
  code
  return output
_}

**To call the function in the Code:**

_funcName(arguments);_

The function keyword goes first, then goes the name of the function, then a list of parameters between the parentheses (comma-separated, empty in the example above) and finally the code of the function, also named “the function body”, between curly braces.

_function showMessage() {
  alert( 'Hello everyone!' );
}_


### Function Expressions:
A JavaScript function can also be defined using an expression. A function expression can be stored in a variable, _as shown in the example: var x = function (a, b) {return a * b};_ 

### Returning a value:
A function can return a value back into the calling code as the result.

###  The () Operator Invokes the Function:
Accessing a function without () will return the function object instead of the function result.

### Local Variables:
A variable declared inside a function is only visible inside that function.

### Naming a function:
Functions are actions. So their name is usually a verb. It should be brief, as accurate as possible and describe what the function does, so that someone reading the code gets an indication of what the function does. It is a widespread practice to start a function with a verbal prefix which vaguely describes the action. There must be an agreement within the team on the meaning of the prefixes.

Function starting with…
- "get…" – return a value,
- "calc…" – calculate something,
- "create…" – create something,
- "check…" – check something and return a boolean, etc.

_for more information [Link](https://www.w3schools.com/js/js_functions.asp)_