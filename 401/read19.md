# React and Forms 
## [ React Docs - Forms: ](https://reactjs.org/docs/forms.html)
### 1. What is a "Controlled Component"?

- Is having a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form.

### 2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

- It's updated as soon as they enter, since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

### 3. How do we target what the user is entering if we have an event handler on an input field?

- By controlled input null value, which means specifying the value prop on a controlled component prevents the user from changing the input unless you desire so.

____

## [The Conditional (Ternary) Operator Explained:](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)
### 1. Why would we use a ternary operator?
- Its shorter than the *if* statement
- Redues time
- More cleanr than *if* statement

### 2. Rewrite the following statement using a ternary statement:
  ```java
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }

  ```

  Ternanry statement:
  ```java
  if(x===y)
  { console.log(true); } 
  else 
  { console.log(false); 
  }

    ===> x===y ? (console.log(true)) : (console.log(false))
```
