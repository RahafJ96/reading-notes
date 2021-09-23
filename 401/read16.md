# Introduction to React and Components

## Component Based Architecture

### 1. What is a component?
- A component is a software object,
- Intended to interact with other components
- Encapsulating certain functionality or a set of functionalities.
- It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

### 2. What are the charactistics of a component?
- **Reusability:** Components are usually designed to be reused in different situations in different applications However, some components may be designed for a specific task.

- **Replaceable:** Components may be freely substituted with other similar components.Not context specific

- **Encapsulated:** A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

- **Independent:** Components are designed to have minimal dependencies on other components.

- **Extensible:** A component can be extended from existing components to provide new behavior.



### 3. What are the advantages of using component based architecture?
- **Ease of deployment:** As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

- **Reduced cost:** The use of third-party components allows you to spread the cost of development and maintenance.
- **Ease of development:** Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

- **Reusable:** The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

- **Modification of technical complexity:** A component modifies the complexity through the use of a component container and its services.

- **Reliability:** The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

- **System maintenance and evolution:** Easy to change and update the implementation without affecting the rest of the system.

- **Independent:** Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

___
## What is “Props” and how to use it in React?

### 1. What is Props?
**“Props”** is a special keyword in React, which stands for properties

### 2. How are props used in React?
It used for passing data from one component to another.
- Firstly, define an attribute and its value(data)
- Then pass it to child component(s) by using Props
- Finally, render the Props Data

### 3. What is the flow of props?
**uni-directional flow.** one way from parent to child


