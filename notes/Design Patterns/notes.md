


► SOLID Principles:

1. Single Responsibility: Each class should have only one job.
2. Open/Closed: Classes should be extendable without being modified.
3. Liskov Substitution: Subclasses should be replaceable with their parent classes.
4. Interface Segregation: Prefer small, specific interfaces over general ones.
5. Dependency Inversion: Rely on abstractions rather than specific implementations.


### Creational Design Patterns

[https://www.youtube.com/watch?v=vap9ACtc_tU]

 [https://github.com/shabbirdwd53/design_patterns/tree/main/singleton/src/main/java]

#### Singleton  : 
This one’s all about exclusivity. It ensures that a class has just one instance. You can access that instance from anywhere, making it handy for situations where you want a single point of control or coordination in your application.

-> Managing a Database connection
-> Logging system
-> Config manager to store global settings
-> Caching system
-> Session 


We won't allow objects using constructior, we will make private constructor, a static object instance is declared in class and that wil be accessible/created using a method

Lazy Singleton
Eager Singleton
Multithread Singleton
Serializable Singleton
Enum singleton ( to overcome issue with reflection )
 - Enums are static and threadsafe by default


 #### Factory 
  Think of it as a way to make objects with flexibility. It’s like having a blueprint for creating things. You define an interface for creating objects, but the actual creation is left to subclasses. This means different subclasses can create objects of different types using the same method.
  (with abstract class or interface)

 * Factory : As name suggest it is factory where we can create objects.
 * Since it creates object it falls in creational design pattern
 * Factory pattern has  two important element in its design.
 

 * 1. Interface/Abstract class : This is base element for which we are making factory i.e. we are going to get object of this type
 * In this case it is "OperatingSystem" which has type available Windows and Linux.
 
 * 2. Factory : This will have nothing but Object creation logic. Let's say as a library you introduce one more subtype that is

1️⃣ Factory Design Pattern Use Cases
Database Connection
Logger Creation
Dependency Injection
Plugin Systems

 ####  Abstract Factory 
Imagine you’re in charge of a fancy dinner party, and you need matching tableware, cutlery and decorations. The abstract factory is like one-stop for all these related items. It provides a way to create families of objects, ensuring that everything you create fits together seamlessly.

Use Cases
GUI Libraries
Database Access
Game Development
Logging Frameworks


#### Builder
The Builder Design Pattern is a creational pattern used in software design to construct a complex object step by step. It allows the construction of a product in a step-by-step manner, where the construction process can change based on the type of product being built. This pattern separates the construction of a complex object from its representation, allowing the same construction process to create different representations.

#### Prototype
The Prototype Design Pattern is a creational pattern that enables the creation of new objects by copying an existing object. Prototype allows us to hide the complexity of making new instances from the client. The existing object acts as a prototype and contains the state of the object.

### Structural Design patters

#### Adapter
Adapter is a structural design pattern that allows objects with incompatible interfaces to collaborate. It enables the usage of an existing class’s interface as an additional interface is the adapter design pattern. To make two incompatible interfaces function together, it serves as a bridge. This pattern involves a single class, the adapter, responsible for joining functionalities of independent or incompatible interfaces.

Usecases
Different Data Formats
Legacy System Integration

Examples
Legacy printer to new printer
Grocery item to Item (ex in swiggy)


#### Bridge
Bridge is a structural design pattern that lets you split a large class or a set of closely related classes into two separate hierarchies—abstraction and implementation—which can be developed independently of each other.

 * Major components to achieve bridge patterns are :
 * 1. Abstraction : This is main abstract class which client uses.
 * 2. RefinedAbstraction - This is the class which extends abstraction
 * 3. Implementor : Interface for the implementation hierarchy.
 * 4. Concrete Implementor - Implementation of the implementor.


 #### Decorator