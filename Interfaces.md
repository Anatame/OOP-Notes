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
-