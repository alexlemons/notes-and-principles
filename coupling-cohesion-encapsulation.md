# Coupling, Cohesion and Encapsulation

Low coupling, high cohesion and encapsulation results in a system that is easier to understand and to change.

### Coupling

Coupling is a measure of how interconnected one element (function, class, module) is to another. Tight coupling creates dependencies and ties elements together, making a system harder to understand, test and change. Changes to one element require subsequent changes that can ripple through the system.

We can reduce coupling by defining standard connections or interfaces between elements of a system, removing their knowledge of each other, and allowing interaction with an element only through its defined interface.

Pure functions are inherently decoupled as they are deterministic and don't produce side effects. They can be dependant on other pure functions only. 

A class or module can expose public properties and methods that act as their interface and define their interactions (API).

### Cohesion

Cohesion is measure of how closely related all the data and responsibilities of an element are to each other. It is measure of how well-defined an elements role is. Elements that have a single responsibility and focus are easier to understand and utilize, in isolation and within a larger system. It's important that an elements properties and methods work together to define a sense of purpose. Low cohesion leads to confusing systems that are difficult to change and test, potentially resulting in unwanted defects. 

One of the best ways to improve cohesion in a system is to eliminate duplication.

### Encapsulation

Encapsulation refers to the ability to use an element through its interface alone, and limit direct access to or hide its internal data and implementation. This stops the responsibilities of one element from leaking into another, and protects the internal state from undesirable external access and modification.