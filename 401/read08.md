# **OO Design**


## **Don't repeat yourself (DRY):**
Is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.

***DRY* is a known development mantra which aims to help us to not have the same piece of code copy-pasted in a lot of different places when working on a particular codebase.**

- The idea behind the principle is that repeating yourself is a bad thing to do when coding, because having the same code in different places makes maintainability harder, once changes in the code will have to happen in many places, instead of one.

- Keep in mind that those changes might also require you to change tests to keep them green.
- It’s always a nice idea to extract common logic into functions, so you can reuse them. The trick is to know *WHEN* to do it.

## **You aren't gonna need it (YAGNI)**
Is a principle of extreme programming (XP) that states a programmer should not add functionality until deemed necessary.

- It is meant to be used in combination with several other practices, such as continuous refactoring, continuous automated unit testing, and continuous integration.
- Used without continuous refactoring, it could lead to disorganized code and massive rework, known as technical debt.

## **Minimum Viable Product (MVP)**
Is a version of a product with just enough features to be usable by early customers who can then provide feedback for future product development.

## **Rule of Three**
Is a code refactoring rule of thumb to decide when similar pieces of code should be refactored to avoid duplication. It states that two instances of similar code do not require refactoring, but when similar code is used three times, it should be extracted into a new procedure.

## **SOLID**
stands for the five principles in OOD that considers maintaining , refactoring , debugging , avoid code smells principles .

- ***S**ingle-Responsibility Principle*

A class should have one and only one reason to change, meaning that a class should have only one job.

- ***O**pen-Closed Principle*

Objects or entities should be open for extension but closed for modification.

- ***L**iskov Substitution Principle*

Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

- ***I**nterface Segregation Principle*

A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.

- ***D**ependency Inversion Principle*

Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.