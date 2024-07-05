**SOLID** is an acronym for the first five object-oriented design (OOD) principles by Robert C. Martin. These design principles encourage us to create more maintainable, understandable, and flexible software. Consequently, as our applications grow in size, we can reduce their complexity and save ourselves a lot of headaches further down the road

## **S**ingle-Responsibility Principle

A class should have one and only one reason to change, meaning that a class should have only one job, a class should only have one responsibility. 

## **O**pen-Closed Principle

Objects or entities should be open for extension but closed for modification.  In doing so, we stop ourselves from modifying existing code and causing potential new bugs in an otherwise happy application.

## **L**iskov Substitution Principle

 Every subclass or derived class should be substitutable for their base or parent class. If class A is a subtype of class B, we should be able to replace B with A without disrupting the behavior of our program.

 ## **I**nterface Segregation Principle

 A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use. Larger interfaces should be split into smaller ones. By doing so, we can ensure that implementing classes only need to be concerned about the methods that are of interest to them.

 ## **D**ependency Inversion Principle

 Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.