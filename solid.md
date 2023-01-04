# SOLID

The SOLID principles provide a pathway to low coupling and high cohesion in OOP.

### Single Responsibility Principle

A class should have a single responsibility, and therefore only have a single reason to change. This results in high cohesion.

Example: a class that mixes both business logic with persistence logic violates the SRP.
An invoice class that calculates an invoice and also handles saving it should
be separated into multiple classes, one that handles the calculation, the other that handles persistence.

### Open-Closed Principle

Classes should be open for extension but closed for modification.

We should avoid modifying the existing functionality of a class, and instead build classes in a way that allows for extension of the functionality. Working with interfaces and abstract classes makes the system more flexible and extendable.

Example: our persistence class that handles saving to a file also needs to handle saving to a database.
Saving to a file and saving to a database can be separated into their own class. Our persistence class can
then expose a single interface which handles saving to either type (via polymorphism). This flexibility means it can be easily
extended to allow for other types of persistence in the future.

### Liskov Substitution Principle

Objects of a base class should be replaceable with objects of its subclasses. 

The subclass should expose all that the base class exposes, extending the behaviour but never
narrowing it down. The subclass should not break the base class behaviour.

### Interface Segregation Principle

This principle states that many client specific interfaces are better than one general purpose interface.

An interface should be as small and simple as possible, only exposing what is needed for a single type of interaction.

Example: A payment interface that includes methods to pay via credit card or bank transfer could be split into 
two interface classes, one for handling credit card payments, the other for bank transfers.

### Dependency Inversion Principle

High level classes should not be dependant on low level classes, both should depend on a standard interface. The interface represents the essential functionality that doesn't change, and removes the need for tight coupling between classes. In this way classes can easily be changed or substituted.

Analogy: a plug socket provides a standard interface for electrical appliances. We do not want to solder our kettle directing into the wiring of the house.