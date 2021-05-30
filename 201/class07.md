# Object-Oriented Programming, HTML Tables

# Domain modeling 
Domain Modelign is your organized and structured knowledge of the problem. The Domain Model should represent the vocabulary and key concepts of the problem domain and it should identify the relationships among all of the entities within the scope of the domain. Also, is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

- using the new keyword creates an object.
- use this to initialize properties inside the object.
- how the object will be stored in a variable for late use.

Most of the time a domain model is illustrated with a set of class diagrams which may show:
- domain objects or conceptual classes
- associations between conceptual classes
- attributes of conceptual classes
To define the same properties between many objects, you’ll want to use a constructor function that will be explained next section.

## HTML Tables:
The HTML `<table>` element represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns of cells containing data.

The process of creating an HTML table is similar to the process that you used to create your web page and any elements that you may have already included in your page, such as links or frames. Coding HTML tables into your web page is fairly easy since you need only understand a few basic table codes.

The basic structure of an HTML table consists of the following tags:

- Table tags: `< TABLE> </ TABLE>`
- Row tags: `< TR> </ TR>`
- Cell tags: `< TD> </ TD>`


```html
<table>
  <tr>
    <td>Rahaf</td>
    <td>Student</td>
  </tr>
  <tr>
    <td>Sara</td>
    <td>Studnet</td>
  </tr>
</table>
```


## Object Constructors
```javascript
function Human(first, last, age, job) { 
    this.firstName = first; 
    this.lastName = last; 
    this.age = age; 
    this.jobDescribtion = job; }
```
## `this` Keyword
In a function definition, this refers to the "owner" of the function.

In the example above, this is the human object that "owns" the fullName function.
In other words, this.firstName means the firstName property of this object.


- Object Types (Blueprints) (Classes) The examples from the previous chapters are limited. They only create single objects.

- Sometimes we need a “blueprint” for creating many objects of the same “type”.

- The way to create an “object type”, is to use an object constructor function.

**In the example above, function Human() is an object constructor function.**
**Objects of the same type are created by calling the constructor function with the new keyword:**
```javascript

let myFriend = new Human(“Sara”, “Nsour”, 26, “student”);

let myTeacher = new Human(“Jack”, “Rally”, 48, “teacher”);
```

The this Keyword In JavaScript, the thing called this is the object that “owns” the code.
The value of this, when used in an object, is the object itself.

In a constructor function this does not have a value. It is a substitute for the new object. The value of this will become the new object when a new object is created.

## Adding a Property to an Object
Adding a new property to an existing object is easy:
```javascript

myFriend.nationality = “Jordanian”;
```
## Adding a Method to an Object
Adding a new method to an existing object is easy:
```javascript

myFriend.name = function () { return this.firstName + “ “ + this.lastName; };
```
## Adding a Property to a Constructor
You cannot add a new property to an object constructor the To add a new property to a constructor, you must add it to the constructor function:
```javascript

function Human(first, last, age, job) { 
    this.firstName = first; 
    this.lastName = last; 
    this.age = age; 
    this.job = job; 
    this.nationality = "Jordan"; }
```
## Adding a Method to a Constructor
Your constructor function can also define methods:
```javascript

function Human(first, last, age, job) { 
    this.firstName = first; 
    this.lastName = last; 
    this.age = age; 
    this.job = job; 
    this.name = function() 
    {return this.firstName + “ “ + this.lastName;}; } 
```
You cannot add a new method to an object constructor the same way you add a new method to an existing object.

## Adding methods to an object constructor must be done inside the constructor function:
```javascript

function Human(firstName, lastName, age, job) { 
    this.firstName = firstName; 
    this.lastName = lastName; 
    this.age = age; 
    this.job = job; 
    this.changeName = function (name) { 
        this.lastName = name; }; 
        }
```

