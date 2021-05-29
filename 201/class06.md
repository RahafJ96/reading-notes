# Problem Domain, Objects, and the DOM

## JavaScript Objects
Objects in JavaScript, just as in many other programming languages, can be compared to objects in real life. The concept of objects in JavaScript can be understood with real life, tangible objects.

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

## Objects and properties
Object properties are basically the same as ordinary JavaScript variables, except for the attachment to objects. 
```javascript
objectName.propertyName
```
 For example, let's create an object named myCar and give it properties named make, model, and year as follows:
 ```javascript
 var myLaptop = new Object();
myLaptop.companyName = 'Toshiba';
myLaptop.coreModel = 'i5';
myLaptop.year = 2018;
```

```javascript
var myLaptop = {
    companyName: 'Toshiba',
    coreModel: 'i5',
    year: 2018
};
```
## Creating new objects
You can create an object using an `object initializer.` Alternatively, you can first create a constructor function and then instantiate an object invoking that function in conjunction with the `new` operator.

- Using object initializers:
```javascript
var obj = { prop_1:   char_1,   // property may be an identifier...
            2:            char_2,   // or a number...
            // ...,
            'property n': char_n }; // or a string
```

## Object initializers
Are expressions, and each object initializer results in a new object being created whenever the statement in which it appears is executed. Identical object initializers create distinct objects that will not compare to each other as equal. Objects are created as if a call to `new Object()` were made; that is, objects made from object literal expressions are instances of `Object`.

The following statement creates an object and assigns it to the variable `x` if and only if the expression `message_x` is true:

```javascript
if (message_x) var x = {greeting: 'hi there'};
```

## Constructor function:
You can create an object with these two steps:

- Define the object type by writing a constructor function. There is a strong convention, with good reason, to use a capital initial letter.
- Create an instance of the object with new.
```javascript
function Laptop(coreModel, model, year) {
  this.coreModel = coreModel;
  this.companyName = companyName;
  this.year = year;
}
```

Now you can create an object called `myLaptop` as follows:
```javascript
var myLaptop = new Laptop('i7', 'Dell', 2018);
```

This statement creates `myLaptop` and assigns it the specified values for its properties. Then the value of `myLaptop.coreModel` is the string `"i7"`, `myLaptop.year` is the integer `2018`, and so on.

You can create any number of `Laptop` objects by calls to `new.` For example:
```java
var hplaptop = new Car('i5', 'HP', 2016);
```
## Defining properties for an object type

You can add a `property` to a previously defined object type by using the `prototype` property. This defines a property that is shared by all objects of the specified type, rather than by just one instance of the object. 
The following code adds a `companyName `property to all objects of type `Laptop`, and then assigns a value to the `companyName` property of the object `laptop1`.

```javascript
Laptop.prototype.companyName = null;
laptop1.companyName = 'black';
```

## Defining methods:

```javascript
objectName.methodname = functionName;

var myObj = {
  myMethod: function(params) {
    // ...do something
  }

  // OR THIS WORKS TOO

  myOtherMethod(params) {
    // ...do something else
  }
};

```

You can then call the method in the context of the object as follows:
```java
object.methodname(params);
```
## Defining getters and setters

When defining getters and setters using object initializers all you need to do is to prefix a getter method with `get` and a `setter` method with set. Of course, the getter method must not expect a parameter, while the setter method expects exactly one parameter (the new value to set). For instance:
```java
var o = {
  a: 7,
  get b() {
    return this.a + 1;
  },
  set c(x) {
    this.a = x / 2;
  }
};

console.log(o.a); // 7
console.log(o.b); // 8 <-- At this point the get b() method is initiated.
o.c = 50;         //   <-- At this point the set c(x) method is initiated
console.log(o.a); // 25
```
`o.a` — a number

`o.b` — a getter that returns o.a plus 1

`o.c` — a setter that sets the value of o.a to half of the value o.c is being set to

___
## Document Object Model (DOM)
![Image](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/742px-DOM-model.svg.png)

**The Document Object Model (DOM)** is the data representation of the objects that comprise the structure and content of a document on the web.

> A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.


## Why called an Object Model?
Documents are modeled using objects, and the model includes not only the structure of a document but also the behavior of a document and the objects of which it is composed of like tag elements with attributes in HTML.
## Properties of DOM:
Let’s see the properties of the document object that can be accessed and modified by the document object. 

![Image2](https://media.geeksforgeeks.org/wp-content/uploads/DOM.png)

- **Window Object:** Window Object is always at top of the hierarchy.
- **Document object:** When an HTML document is loaded into a window, it becomes a document object.
- **Form Object:** It is represented by `form` tags.
- **Link Objects:** It is represented by `link` tags.
- **Anchor Objects:** It is represented by a `href` tags.
- **Form Control Elements:** Form can have many control elements such as text fields, buttons, radio buttons, and checkboxes, etc.

### **Methods of Document Object:**
 

- **write(“string”):** writes the given string on the document.
- **getElementById():** returns the element having the given id value.
- **getElementsByName():** returns all the elements having the given name value.
- **getElementsByTagName():** returns all the elements having the given tag name.
- **getElementsByClassName():** returns all the elements having the given class name.

_example:_

```javascript
<Table>
   <ROWS>
      <TR>
         <TD>Movies</TD>
         <TD>Series</TD>
      </TR>
      <TR>
         <TD>News</TD>
         <TD>Show</TD>
      </TR>
   </ROWS>
</Table>
```