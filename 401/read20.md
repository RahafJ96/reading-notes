# Putting it all together

## [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

### 1. How would you break a mock into a component heirarchy?
- The first thing you'll want to do is to draw boxes around every component
- Identified the components in our mock,
- Rerange them into a hierarchy

*Components that appear within another component in the mock should appear as a child in the hierarchy*

### 2. What is the `single responsibility` principle and how does it apply to components?
- Th Component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.


### 3. What does it mean to build a `static` version of your application?
- To build a static version of your app that renders your data model, you'll want to build components that reuse other components and pass data using props


### 4. Once you have a `static` application, what do you need to add?
- **Props** are a way of passing data from parent to child. If you are familiar with the concept of state, don't use state at all to build this static version. 
- **State** is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don't need it.

### 5. What are the three questions you can ask to determine if something is state?
- Is it passed in from a parent via props? If so, it probably isn't state.
- Does it remain unchanged over time? If so, it probably isn't state.
- Can you compute it based on any other state or props in your component? If so, it isn't state.
### 6. How can you identify where state needs to live?
- Identify every component that renders something based on that state.

- Find a common owner component.

- Either the common owner or another component higher up in the hierarchy should own the state.

- If you can't find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
