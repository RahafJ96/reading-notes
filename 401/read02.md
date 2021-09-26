# [Packages and Import](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)
## Packages and Import

#### **A Package** is the same as directory
- package declarations must be the first statements
- after importing a package you can specify classes from that package
- For small programs it's common to omit package declaration, although it is not recommended.
- The wildcard character (\*) is used to specify that all classes with that package are available to your program.
- you can specify the exact class that you want to use instead of \*
- **Common imports:**
   - import `java.awt.\*`; Common GUI elements.
   - import `java.awt.event.\*`; The most common GUI event listeners.
   - import `javax.swing.\*`; More common GUI elements. Note "javax".
   - import `java.util.\*`; Data structures (Collections), time, Scanner, etc classes.
   - import `java.io.\*;` Input-output classes.
   - import `java.text.\*;` Some formatting classes.
   - import `java.util.regex.\*;` Regular expression classes.
- imports doesn't make the file larger
- using `\*` in the import prevents accidentally defining classes with names that conflict with the standard library names
- import with` \*` doesn't include any of the subpackages
- Static imports in Java 5 leads to name pollution and confusion about which class constants come from.

## [A Guide to Java Loops](https://www.baeldung.com/java-loops)
### **A Guide to Java Loops**
* Looping in programming langauges is a feature that facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false.
### Types of loops
  - `For loop` - allows you to repeat certain operations by incrementing and evaluating a loop counter
  - `While loop` - repeats a statement or a block of statements while its controlling Boolean-expression is true
  - `Do-While loop` - like a while loop, but the first condition evaluation happens after the first iteration of the loop