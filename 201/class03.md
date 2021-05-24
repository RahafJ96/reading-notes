# Class 03 - Read 03

# HTML

## Lists
HTML lists allow web developers to group a set of related items in lists.

### Unordered HTML List
> An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag.


### Ordered HTML List
> An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.

### HTML List Tags
Tag	Description
- `<ul>`	Defines an unordered list
- `<ol>`	Defines an ordered list
- `<li>`	Defines a list item
- `<dl>`	Defines a description list
- `<dt>`	Defines a term in a description list
- `<dd>`	Describes the term in a description list

## Boxes
### All HTML elements can be considered as boxes.
In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

### Explanation of the different parts:

- **Content** - The content of the box, where text and images appear
- **Padding** - Clears an area around the content. The padding is transparent
- **Border** - A border that goes around the padding and content
- **Margin** - Clears an area outside the border. The margin is transparent
The box model allows us to add a border around elements, and to define space between elements. 
> _Example: div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}_

### Width and Height of an Element
- The total width of an element should be calculated like this:
- Total element width = width + left padding + right padding + left border + right border + left margin + right margin
- The total height of an element should be calculated like this:
- Total element height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin

# JavaScript

## Basic JavaScript Instructions
JavaScript includes operators as in other languages. An operator performs some operation on single or multiple operands (data value) and produces a result. For example 1 + 2, where + sign is an operator and 1 is left operand and 2 is right operand. + operator adds two numeric values and produces a result which is 3 in this case.

### JavaScript includes following categories of operators:

**1. Arithmetic Operators:** are used to perform mathematical operations between numeric operands.

**2. Comparison Operators:**:that compare two operands and return Boolean value true or false.

**3. Logical Operators:** are used to combine two or more conditions. JavaScript includes following logical operators.

**4. Assignment Operators:** In JavaScript assignment operators is included to assign values to variables with less key strokes.

**5 Conditional Operators:** starts with conditional expression followed by ? operator. Second part ( after ? and before : operator) will be executed if condition turns out to be true. If condition becomes false then third part (after :) will be executed.


## Decisions and Loops
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


