# Interfaces Java

- Interfaces stand between classes as a blueprint specifying what a class must do.
- Interfaces can be used to achieve multiple inheritance.
- Interfaces can be used to achieve loose coupling.

## Dependancey Injection

- Constructor Injection
- Setter Injection
- Method injection

## Constructor Injection

- In Constructor Injection the dependency is passed via a constructor. The constructor of the class which needs to use the dependency is used.

## Setter Injection

- In Setter Injection, the dependency is injected via a setter method.
- We can change the dependencies throughout the lifetime of the program.

## Method Injection

- In Method injection, instead of using a setter on constructor, we can pass the dependency in the method itself.
- Every time a method is called, it's possible for it to use different dependencies.

## Interface Segregation Principle

- ISP or Interface Segregation Principle states that no class should be forced to implement methods it does not use.
- ISP reduces coupling in a system.
- Interfaces should be segregated if they have ***different capabilities.***
- Interfaces can use the extend keyword to inherit methods from other interfaces.
- Interfaces can have multiple parents; i.e., **they can extend from multiple interfaces via the extend keyword which only allows one.**

### Fields in Interfaces

- Fields in interfaces are static, final, and constant and cannot be changed in the future.
- **It's a bad practice to use fields in interfaces because once declared, it cannot be changed. Such fields should be defined in implementations and not in interfaces**.
- **If one field is required by only some classes, other classes should not be aware of that field if they don't need it. (Another reason using fields in interfaces is a bad practice)**

## Static methods in Interfaces

- Static methods can be defined in interfaces, they can have logic.
- **Using static methods in Interfaces is bad practice because Interfaces are about what and not hows, defining logic in interfaces adds hows to them.**
- If logic is needed to be reused in all the classes, ***an abstract class*** is used which implements the interface and the logic is ***defined in the abstract class***. The classes that need to use the logic can ***extend the abstract class*** and reuse the logic. This keeps the interfaces clean.

## Private methods in Interfaces

- Private methods can be implemented in interfaces.
- **It's a bad practice to add private methods in interfaces because private methods are implementation detail, they should not be allowed in interfaces.**
- They were added because while writing defined static methods in interfaces, some logic could become repetitive, that repetitive logic can be extracted into separate private methods inside interfaces.
- **Interfaces are contracts, they must not have static methods, no private methods or fields!**

## Difference Between Interfaces and Abstract Classes

- Interfaces are purely contracts, they have no code or implementation. We use them to build loosely coupled, extensible, and testable applications.
- Abstract classes are partially implemented classes and are used to share code between a few classes.

## When to use interfaces?

- Interfaces should be used when you wanna decouple a class from its dependencies.
- You can easily swap one implementation with another with minimal or zero impact on the application.
- Applications can be extended with minimal impact.
- It allows testing in isolation.

# Things to remember:

> **With these new features such as private or static methods, interfaces have lost their meaning and a lot of people are abusing them because they don't understand what interfaces are for**.

> **People are using it as hacks to achieve multiple inheritance but interfaces should not be confused with classes, we should keep them as contracts so we can minimize the impact of changes so we can build loosely coupled applications. So, if we change how we do something, we are not gonna end up with breaking changes or a lot of recompilation of code**.

# Interfaces Quiz

1. Why do we use interfaces? 
2. What is tightly coupled code?
3. What is dependency injection?
4. What are the various types of dependency injections?
5. What is the segregation principle (ISP)?
6. Why we shouldn't declare fields, private or static methods in interfaces?
7. What are the similarities and differences between interfaces and abstract classes?
8. Should we extract an interface from every class? Why?