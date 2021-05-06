# Expressions and operators
At first we will discuss the JavaScript's expressions and operators, including assignment, comparison, arithmetic, bitwise, logical, string, ternary and more.

## Operators:
There are many types of operators in JavaScript:

**1. Assignment Operators:** In JavaScript assignment operators is included to assign values to variables with less key strokes. The simple assignment operator is equal (=), *for example; x = y assigns the value of y to x*

**2. Comparison Operators:**:that compare two operands and return Boolean value true or false. *for example; Equal(==),Not equal (!=),ets *

**3. Arithmetic Operators:** are used to perform mathematical operations between numeric operands. _for example;(+, -, *, /, %, ++)_

**4.Bitwise operators:**A bitwise operator treats their operands as a set of 32 bits (zeros and ones),_for example;(BitwiseAND; a & b )_

**4. Logical Operators:** are used to combine two or more conditions. JavaScript includes following logical operators._for example;(LogicalAND; a && b)_

**6. String operators:** _for example; It will console logs the string "my string".: console.log('my ' + 'string');_

**7. Conditional Operators:** starts with conditional expression followed by ? operator. Second part ( after ? and before : operator) will be executed if condition turns out to be true. If condition becomes false then third part (after :) will be executed._for example;var status = (age >= 18) ? 'adult' : 'minor';_

**8. Comma operator:** The comma operator (,) evaluates each of its operands (from left to right) and returns the value of the last operand.

**9. Unary operators:** is an operation with only one operand.
- delete: it deletes an object's property.
- typeof: _typeof operand_ or _typeof (operand)_
- void: to evaluate without returning a value. 

**10. Relational operators:** it compares its operands and returns a Boolean value based on whether the comparison is true.
- in: returns true if the specified property is in the specified object.
- instanceof: returns true if the specified object is of the specified object type. 

**11. Operator precedence:** determines the order they are applied when evaluating an expression. [Link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#table)


## Expressions:
An expression is any valid unit of code that resolves to a value.

**1. Primary expressions:**
- **this:** it refers to the calling object in a method.
- **Grouping operator:** ( )

**2. Left-hand-side expressions:** Left values are the destination of an assignment.

- **new:** to create a case of a user-defined object type._var objectName = new objectType([param1, param2, ..., paramN]);_
- **super** to call functions on an object's parent. 
 >_super([arguments]); // calls the parent constructor.
super.functionOnParent([arguments]);_


# Loops and Iteration
Loops are used in JavaScript to perform repeated tasks based on a condition. Conditions typically return **true** or **false** when analysed. A loop will continue running until the defined condition returns **false**. 
_Loops can execute a block of code a number of times._

The three most common types of loops are:
- for
- while
- do while

## for statement:
It repeats until a specified condition evaluates to _**false**_.

- for (variable in object) {
...
}
## while statement:
The while loop starts by evaluating the condition. If the condition is _**true**_, the statement(s) is/are executed. If the condition is _**false**_, the statement(s) is/are not executed. After that, while loop ends.
- while (condition)

  statement

## do while statement:
The **do while loop** is closely related to **while loop**. In the do while loop, the condition is checked at the end of the loop.

 do {

   *Statement(s);*

} while (*condition*);


