# Lists and Keys in React

### 1. What does .map() return?
It returns a new Array.

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);
```

### 2. If I want to loop through an array and display each value in JSX, how do I do that in React?
- We can build collections of elements and include them in the JSX using curly braces {}.
```javascript
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);
```
- render it to the DOM:
```javascript
ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);
```

### 3. Each list item needs a unique
***“key”*** is a special string attribute you need to include when creating lists of elements


### 4. What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed. 

____

# How to Use the Spread Operator (…) in JavaScript

### 1. What is the spread operator?
- **Spread Operator** is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

- In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

### 2. List 4 things that the spread operator can do.
- Copying an array
- Concatenating or combining arrays
- Using Math functions
- Using an array as arguments
- Adding an item to a list


### 3. Give an example of using the spread operator to combine two arrays.
```java
onst fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
fruits[0] = '🍑'
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍
```


### 4. Give an example of using the spread operator to add a new item to an array.
```java
const myArray = [`🤪`,`🐻`,`🎌`]
const yourArray = [`🙂`,`🤗`,`🤩`]
const ourArray = [...myArray,...yourArray]
console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩
```
### 5. Give an example of using the spread operator to combine two objects into one.
```java
const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂
```