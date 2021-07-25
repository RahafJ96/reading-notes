# React State Vs Props

### 1. What types of things can you pass in the props?
In react allows us to pass values from a parent component down to a child component.

### 2. What is the big difference between props and state?
**props** you pass into component *(props handled outside of component )*
**state** is handled inside that component and you can updated inside the component

### 3. When do we re-render our application?
- When we change the state inside of the app.
- Or change the props outside the component.

### 4. What are some examples of things that we could store in state?
There are many examples, such as if we have a counter app like Step counter, and we want to update the count each time you move the phone then we need state to store these updating.

# React lifecycle
![link](https://miro.medium.com/max/1400/1*6X_7HKFdQoh9eXqWgwQuvQ.png)

### 1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
the (render)

### 2. What is the very first thing to happen in the lifecycle of React?
constructor()

### 3. Put the following things in the order that they happen:
- Constructor
- Render
- React Updates
- ComponentWillUnmount
- ComponentDidMount

### 4. What does componentDidMount do?
 Load anything using a network request or initialize the DOM *dom mainplution , network request*