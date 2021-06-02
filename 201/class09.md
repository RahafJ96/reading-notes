# Forms and JS Events

## Forms in HTML & CSS
An HTML form is used to collect user input. The user input is most often sent to a server for processing.
- The `< form>` Element
The HTML `< form>` element is used to create an HTML form for user input:
```javascript
< form>
 . form elements . 
</ form>
```
The `< form>` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

- The `< input>` Element

The HTML `< input>` element is the most used form element.

An `< input>` element can be displayed in many ways, depending on the type attribute.

```javascript
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, the form-data will be sent to a page called "/action_page.php".</p>

```
First name: <input>

Last Name: <input>

<hr>


### Forms:
- `<input type="text">`	Displays a single-line text input field
- `<input type="radio">`	Displays a radio button (for selecting one of many choices)
- `<input type="checkbox">`	Displays a checkbox (for selecting zero or more of many choices)
- `<input type="submit">`	Displays a submit button (for submitting the form)
- `<input type="button">`	Displays a clickable button

### Text Fields
The `<input type="text">` defines a single-line input field for text input.

### The <label> Element
Notice the use of the `<label>` element in the example above.

- The `<label>` tag defines a label for many form elements.
The `<label>` element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element.
The `<label>` element also help users who have difficulty clicking on very small regions- because when the user clicks the text within the `<label>` element, it toggles the radio button/checkbox.
The for attribute of the `<label>` tag should be equal to the id attribute of the `<input>` element to bind them together.

### Checkboxes
The `<input type="checkbox">` defines a checkbox.

<hr>


## CSS Forms

![Image](https://staticresources123.s3.amazonaws.com/site/other/landings/joomla-form/contact-form.png)

### Styling Input Fields
Use the width property to determine the width of the input field, If you only want to style a specific input type, you can use attribute selectors:

- `input[type=text]` - will only select text fields
- `input[type=password]` - will only select password fields
- `input[type=number]` - will only select number fields

### Bordered Inputs
Use the `border` property to change the border size and color, and use the border-radius property to add rounded corners

### Padded Inputs
Use the `padding` property to add space inside the text field.
### Colored Inputs
Use the `background-color` property to add a background color to the input, and the color property to change the text color

ets...
<hr>

## JavaScript Events
HTML events are "things" that happen to HTML elements.

When JavaScript is used in HTML pages, JavaScript can "react" on these events.

An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

- An HTML web page has finished loading
- An HTML input field was changed
- An HTML button was clicked
Often, when events happen, you may want to do something.

JavaScript lets you execute code when events are detected.

HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.


```javascript
//With single quotes:

<element event='some JavaScript'>

//With double quotes:

<element event="some JavaScript">
```