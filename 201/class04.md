#  HTML Links, CSS Layout, JS Functions

## HTML Links
The HTML External Resource Link element `(<link>)` specifies relationships between the current document and an external resource.
Links are found in nearly all web pages. Links allow users to click their way from page to page.

### HTML links are hyperlinks.

You can click on a link and jump to another document.
When you move the mouse over a link, the mouse arrow will turn into a little hand.

### HTML Syntax
The HTML `<a>` tag defines a hyperlink. It has the following syntax:
> <a href="url">link text</a>

When you move the mouse over a link, two things will normally happen:

- The mouse arrow will turn into a little hand
- The color of the link element will change

By default, a link will appear like this (in all browsers):
- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red

## HTML links Summary
- Use the HTML `<a>` element to define a link
- Use the HTML href attribute to define the link address
- Use the HTML target attribute to define where to open the linked document
- Use the HTML `<img>` element `(inside <a>)` to use an image as a link
- Use the HTML id attribute `(id="value") `to define bookmarks in a page
- Use the HTML href attribute `(href="#value")` to link to the bookmark

___
## CSS Layout
### Website Layout
A website is often divided into headers, menus, content and a footer:

![Image](https://media.geeksforgeeks.org/wp-content/uploads/website_layout-300x268.png)

### Header Section
The header section is generally placed either at the top of the Website or just below a top navigation menu. It often comprises of the name of the Website or the logo of the Website.

### Navigation Menu
A Navigation Bar/Menu is basically a list of links that allows visitor to navigate through the website comfortably with easy access.

### Content Section
The content section is the main body of the website. The user can divide content section in n-column layout.

### Footer Section 
A footer section is placed at the bottom of the webpage and it generally consists of information like contact info, copyrights, About us etc.

___
# JavaScript Functions
A JavaScript function is a block of code designed to perform a particular task. A JavaScript function is executed when "something" invokes it (calls it).
The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}
```javascript
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```
- Function parameters are listed inside the parentheses () in the function definition.

- Function arguments are the values received by the function when it is invoked.

- Inside the function, the arguments (the parameters) behave as local variables.

**To call the function in the Code:**
```javascript
_funcName(arguments);_
```
The function keyword goes first, then goes the name of the function, then a list of parameters between the parentheses (comma-separated, empty in the example above) and finally the code of the function, also named “the function body”, between curly braces.
```javascript
_function showMessage() {
  alert( 'Hello everyone!' );
}_
```
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