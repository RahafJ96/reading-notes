# Java Primitives versus Objects

- Java has two types of data types :
    - Primitive data type : int, boolean , double .
    - references like Integer , Double , String .

- converting primitive type to reference is called autoboxing .
- Choosing which of these type Depends on how much memory available to use and what default values to handle .
- Wrapper classes are immutable .

- Primitive size on memory : 
    - boolean 1 bit .
    - byte 8 bits .
    - short , char 16 bits .
    - int , float 32 bits .
    - double , long 64 bits .

- values depend from each JVM .

- Reference types are on heap memory and slower to access with the following sizes : 
    - Boolean , Integer , Float , Short ... : 128 bits .
    - Long , Double : 192 bits .


- The size for array is a little different which occupies 64 bit multiplied by a percentage depending on the type and 128 bit static .

- Running time of a java application depends on the hardware and the jvm and some circumanstances .

- primitives live on the stack and references lives on heap memory .

- Primitives has an actual value as default but for references null is the default .

- Generics and collections requires using references by default, furthermore the primitives are much faster .

# Exceptions
## What is an exception 

- exception is an event that occurs when something stops the normal flow of the program .
- When an error occurs an object is created with the error information about the error and the state of the program .
- this process is called throwing an exception and is handled to the running system .
- when the exception is thrown the compiler start looking for handler to this exception starting from the method where the exception was thrown .
- if a block of code was found to handle that exception that is called catching the error and terminates the program .

## The Catch or Specify Requirement
- Valid java program must appropriatly use try and catch to handle exceptions .

- Three types of exceptions : 
    - checked exceptions : checked exception where we have to handle exceptions hence their will be terminating the program and all of it's tasks once an exception occurs .
    **All exceptions are checked other than error and runtime exceptions and their sub classes.**
    **The only type of exception that the program can recover from.**


    - error : error throw the running process of the program for example IOError exception .

    - Runtime exception : this happens when a runtime , logical , mathmatical error occurs for example NullPointerException .

## Catching and Handling Exceptions

- the blocks to handle exceptions are try , catch and finally .
- checked exception must be caught .

- the unchecked exception can be handled using try , catch and finally blocks .


## Scanning

- Objects of type scanner used for breaking input into tokens .

- by default it uses white spaces to break tokens .

- we Use the bufferedreader class with filereader object passed to it's constructor to read files .
- file reader constructor accept a path as a string .

- the scanner seperates using white space but we can use useDlimiter to specify a regex to seperate tokens .

- Scanner also can read all type of data types and supports integer us locale number seperator .

- we use scanner close method to close the scanner .