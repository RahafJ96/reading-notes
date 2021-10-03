# Inheritance and Interfaces

## [Java OO Tutorial](https://docs.oracle.com/javase/tutorial/java/concepts/)

## **What Is Inheritance?**

1. Object-oriented programming allows classes to inherit commonly used state and behavior from other classes.
2. In the Java programming language, each class is allowed to have one direct superclass, and each superclass has the potential for an unlimited number of subclasses
3. To create a subclass use the `extends` keyword at the beginning of your class declaration, followed by the name of the class to inherit from

### **What Is an Interface?**

1. an interface is a group of related methods with empty bodies.
2. To implement this interface, the name of your class would change , and you'd use the `implements` keyword in the class declaration
3. If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.
4. To actually compile a class that uses an interface, you'll need to add the public keyword to the beginning of the implemented interface methods.

### **What Is a Package?**

1. A package is a namespace that organizes a set of related classes and interfaces.
1. Application Programming Interface, or "API": is an enormous class library (a set of packages) suitable for use in your own applications.

## [Interfaces and Inheritance](https://docs.oracle.com/javase/tutorial/java/IandI/index.html)

### Interfaces

**An interface is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.**
- Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces.
- When an instantiable class implements an interface, it provides a method body for each of the methods declared in the interface.
- An interface declaration consists of modifiers, the keyword interface, the interface name, a comma-separated list of parent interfaces (if any), and the interface body.
- An interface can extend other interfaces
- The interface body can contain abstract methods, default methods, and static methods.
- An abstract method within an interface is followed by a semicolon, but no braces
- Default methods are defined with the default modifier
- static methods with the static keyword
- All abstract, default, and static methods in an interface are implicitly public, so you can omit the public modifier.
- All constant values defined in an interface are implicitly public, static, and final. Once again, you can omit these modifiers.

*If you define a reference variable whose type is an interface, any object you assign to it must be an instance of a class that implements the interface.*

``` java
public interface OperateCar {
   // constant declarations, if any
   // method signatures
   // An enum with values RIGHT, LEFT
   int turn(Direction direction,
            double radius,
            double startSpeed,
            double endSpeed);
   int changeLanes(Direction direction,
                   double startSpeed,
                   double endSpeed);
   int signalTurn(Direction direction,
                  boolean signalOn);
   int getRadarFront(double distanceToCar,
                     double speedOfCar);
   int getRadarRear(double distanceToCar,
                    double speedOfCar);
         ......
   // more method signatures
}
```

#### Default Methods

1. Default methods enable you to add new functionality to the interfaces of your libraries and ensure binary compatibility with code written for older versions of those interfaces.
2. To extend an interface that contains a default method, you can do the following:
   - do not mention the default method at all, which lets your extended interface inherit the default method.
   - Redeclare the default method, which makes it abstract.
   - Redefine the default method, which overrides it.
3. Integrating Default Methods into Existing Libraries

### Inheritance

- Every class is implicitly a subclass of Object.
- inheritance is to derive your new class from the existing class.
- The constructor of the superclass can be invoked from the subclass.
- All Classes in the Java Platform are Descendants of Object
- A subclass inherits all of the public and protected members of its parent, no matter what package the subclass is in. If the subclass is in the same package as its parent, it also inherits the package-private members of the parent.
- The inherited fields can be used directly, just like any other fields.
- You can declare a field in the subclass with the same name as the one in the superclass, thus hiding it (not recommended).
- You can declare new fields in the subclass that are not in the superclass.
- The inherited methods can be used directly as they are.
- You can write a new instance method in the subclass that has the same signature as the one in the superclass, thus overriding it.
- You can write a new static method in the subclass that has the same signature as the one in the superclass, thus hiding it.
- You can declare new methods in the subclass that are not in the superclass.
- You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword super.
- A subclass does not inherit the private members of its parent class.

```java
ublic class MountainBike extends Bicycle {
        
    // the MountainBike subclass adds one field
    public int seatHeight;

    // the MountainBike subclass has one constructor
    public MountainBike(int startHeight,
                        int startCadence,
                        int startSpeed,
                        int startGear) {
        super(startCadence, startSpeed, startGear);
        seatHeight = startHeight;
    }   
        
    // the MountainBike subclass adds one method
    public void setHeight(int newValue) {
        seatHeight = newValue;
    }   
}
```
#### Private Members in a Superclass
 A nested class has access to all the private members of its enclosing class—both fields and methods. Therefore, a public or protected nested class inherited by a subclass has indirect access to all of the private members of the superclass.

### Casting Objects

1. an object is of the data type of the class from which it was instantiated, The reverse is not necessarily
2. Casting shows the use of an object of one type in place of another type, among the objects permitted by inheritance and implementations.
3. You can make a logical test as to the type of a particular object using the instanceof operator. This can save you from a runtime error owing to an improper cast
4. You can prevent a class from being subclassed by using the final keyword in the class's declaration.
5. you can prevent a method from being overridden by subclasses by declaring it as a final method.
6. An abstract class can only be subclassed; it cannot be instantiated