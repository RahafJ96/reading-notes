# [Java Primitives versus Objects](https://www.baeldung.com/java-primitives-vs-objects)
- Java has two types of data types :
    - Primitive data type : int, boolean , double .
    - references like Integer , Double , String .

- converting primitive type to reference is called autoboxing .
- Choosing which of these type Depends on how much memory available to use and what default values to handle .
- Wrapper classes are immutable .

#### **Primitive size on memory :** 

    - boolean 1 bit .
    - byte 8 bits .
    - short , char 16 bits .
    - int , float 32 bits .
    - double , long 64 bits .


- *Values depend from each JVM .*

####  **Reference types are on heap memory and slower to access with the following sizes :**
    - Boolean , Integer , Float , Short ... : 128 bits .
    - Long , Double : 192 bits .


- The size for array is a little different which occupies 64 bit multiplied by a percentage depending on the type and 128 bit static .

- Running time of a java application depends on the hardware and the jvm and some circumanstances .

- Primitives live on the stack and references lives on heap memory .

- Primitives has an actual value as default but for references null is the default .

- Generics and collections requires using references by default, furthermore the primitives are much faster .

# [Exceptions](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)
## What is an exception? 
- An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions.
- When an error occurs an object is created with the error information about the error and the state of the program .
- this process is called throwing an exception and is handled to the running system .
- when the exception is thrown the compiler start looking for handler to this exception starting from the method where the exception was thrown .
- if a block of code was found to handle that exception that is called catching the error and terminates the program .

## The Catch or Specify Requirement
- Valid java program must appropriatly use try and catch to handle exceptions .

#### **Three types of exceptions :** 
    1. checked exceptions : checked exception where we have to handle exceptions hence their will be terminating the program and all of it's tasks once an exception occurs .
    - All exceptions are checked other than error and runtime exceptions and their sub classes.
    - The only type of exception that the program can recover from.


    2. Error : error throw the running process of the program for example IOError exception .

    3. Runtime exception : this happens when a runtime , logical , mathmatical error occurs for example NullPointerException .

# [Scanning](https://docs.oracle.com/javase/tutorial/essential/io/scanning.html)

-  **Scanner :** an objects of type useful for breaking down formatted input into tokens and translating individual tokens according to their data type.
### Breaking Input into Tokens
  - a scanner uses white space to separate tokens
  - white space characters - blanks, tabs, and line terminators
#### Translating Individual Tokens
  - Scanner supports tokens for all of the Java language's primitive types with the exception of char.
  - Numeric values can use thousands separators.