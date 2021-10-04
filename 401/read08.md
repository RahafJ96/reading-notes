# OO Design

- ***Single-Responsibility Principle***

A class should have one and only one reason to change, meaning that a class should have only one job.

- ***Open-Closed Principle***

Objects or entities should be open for extension but closed for modification.

- ***Liskov Substitution Principle***

Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

- ***Interface Segregation Principle***

A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.

- ***Dependency Inversion Principle***

Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.

## **SOLID :** 
stands for the five principles in OOD that considers maintaining , refactoring , debugging , avoid code smells principles .


### **S - Single-responsiblity Principle :**
- A class should have one reason to change (one functionalitiy) .

- Each class should be concerened about it's own funcionality only .

- In real life imagine important tasks that depends on unrelated tasks .

### **O - Open-closed Principle : Objects or instances should be open for extension and closed for modification .**
- That means we should be able to extend the class without modifiying it .

- To come across Open closed principle Interfaces should be implemented .

- When using interfaces functionality can be extended without modifiying the class itself .

- extending the bilities in phone without having the access to modify it .


### **L - Liskov Substitution Principle : Every derived class can be substituted from it's parent class .**
- The child class should be combatible with it's parent functionality and that what is liskov principle is about .

- Ensures that each child class is able to implement the parents attitude and behavior .


### **I - Interface Segregation Principle :You shouldn't force a user to implement useless methods which he wouldn't use .**
- Making interfaces can divide the task into the classes that needs it .

- Making interfaces serves a specific group or classes .

- Managing the attitude of classes by interfaces .

- It's about depending on smaller useful interface other than one big interface and implementing each method when using it or not .


### **D - Dependency Inversion Principle : Entities should be abstracted and decoupled .**
- both high level and low level modules depends on abstraction .

- This principle is concerned with abstraction and not counting on another class or (sub classes ) .