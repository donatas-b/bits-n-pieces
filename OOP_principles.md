Object-oriented programming (OOP) is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior.

(CEIPA)

1. **C**lasses and Objects:

 - Class: A blueprint for creating objects. It defines a type of object according to the attributes (data) and methods (functions) that the object can have.
 - Object: An instance of a class. It is a specific realization of a class with actual values.

2. **E**ncapsulation:

 - The bundling of data (attributes) and methods (functions) that operate on the data into a single unit or class. It helps in restricting direct access to some of an object's components, which means the internal representation of an object can't be seen from outside the object’s definition.

3. **I**nheritance:

 - A mechanism where a new class is derived from an existing class. The new class, known as a subclass, inherits attributes and methods from the parent class, allowing for code reusability and the creation of a hierarchy.

4. **P**olymorphism:

- The ability of different classes to be treated as instances of the same class through inheritance. It allows methods to do different things based on the object it is acting upon, even if they share the same name.

5. **A**bstraction:

- The concept of hiding the complex implementation details and showing only the necessary features of an object. It helps in reducing programming complexity and effort.


### Interfaces
An interface is a contract or blueprint that defines a set of methods (and properties) that a class must implement, but does not provide the implementation itself.

1. Method Signatures:

 - An interface specifies what methods a class must implement, including the method names, return types, and parameters, but not the body of the methods.

2. No Implementation:

 - Interfaces do not provide any code for the methods; they only define the method signatures. The actual implementation is provided by the classes that implement the interface.

3. Multiple Inheritance:

 - Unlike classes, which may be limited to single inheritance (a class can inherit from only one superclass), a class can implement multiple interfaces. This allows for a form of multiple inheritance, enhancing flexibility and reuse.

4. Polymorphism:

 - Interfaces allow different classes to be treated as the same type if they implement the same interface. This supports polymorphic behavior, where a single interface type can point to objects of different classes.


### Generics
Generics are a feature that allows you to write classes, methods, and interfaces that operate on types specified as parameters

Imagine a storage box that can hold any type of item. A generic storage box can be used to store books, clothes, or toys without needing to create separate types of boxes for each item. The box’s design remains the same, but the items it holds can vary, similar to how generics allow the same class or method to operate on different data types.
