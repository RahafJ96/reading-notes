#  HTML Links, CSS Layout, JS Functions

## HTML Links
The HTML External Resource Link element `(<link>)` specifies relationships between the current document and an external resource.
Links are found in nearly all web pages. Links allow users to click their way from page to page.

### HTML links are hyperlinks.

You can click on a link and jump to another document.
When you move the mouse over a link, the mouse arrow will turn into a little hand.

### HTML Syntax
The HTML `<a>` tag defines a hyperlink. It has the following syntax:
```html
 <a href="url">link text</a>
```

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


# 6 Reasons for Pair Programming
 Pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard.And the Navigator uses their words to guide the Driver but does not provide any direct input to the computer.
## 1. Greater efficiency
More efficient. Common thinking is that it slows down the project completion time because you are effectively putting two programmers to develop a single program, instead of having them work independently on two different programs.
## 2. Engaged collaboration
Two heads are better than one. If the driver encounters a hitch with the code, there will be two of them who’ll solve the problem.
## 3. Learning from fellow students
Code Fellows talks about how it could help programmers learn from their peers in this blog post. It would allow programmers to get instant face-to-face instruction, which is much better than online tutorials and faster than looking for resources on the Internet. Plus, you can learn things better from your partner, especially in areas that may be unfamiliar to you.
## 4. Social skills
Collaborating on a single project helps your team to appreciate the value of communication and teamwork.
Developers can also pick up best practices and better techniques from more advanced programmers. It can also facilitate mentoring relationships between two programmers.
## 5. Job interview readiness
 The ability to work with and learn from others and stellar communication skills are as (or more!) important to a company than specific technical skills. Pair programming strengthens all of those skills.
 Companies can get a better feel for how an applicant will fit into the team and their collaboration style.
## 6. Work environment readiness
 Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.

