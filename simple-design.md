# Simple Design

Good design minimizes cost and maximizes benefit over the lifetime of the software. Kent Beck's simple design rules:

### 1. Runs all the tests

The design must produce a system that acts as intended. A system that is comprehensively tested and passes all of its tests is verifiable. Arguably, a system that isn't verifiable shouldn't be deployed.

Writing tests pushes us towards a design where our functions and classes are small and single purpose. Tight coupling makes it difficult to write tests. By applying principles like single responsibility, dependency inversion and tools like interfaces and abstraction, we minimize coupling and make the system more testable.

Writing tests leads to better designs.

### 2. No Duplication (DRY)

Duplication is the primary defect of a well designed system, it represents additional work, additional risk and additional unnecessary complexity. 

Duplication can exist in various forms. Repeated lines of code are unnecessary and should be abstracted to a shared function. Repeated implementation (one or more pieces of code with the same or overlapping functionality) can be eliminated by applying the single responsibility principle, abstracting commonality, and encouraging reuse and composition. By making these abstractions on small pieces of code, we reduce the complexity of the larger system and improve testability.

Everything should be said once and only once.

### 3. Expressive

When working on complex projects, in large teams, over a long period of time, it's critical for us to be able to easily understand what a system does and the problem it solves. If the code is written in a convoluted and confusing way, it is easy to introduce defects when making changes. As a system becomes more complex, it takes more time for a developer to understand, and there is more opportunity for misunderstanding. Code should clearly express the intent of the author.
 
We can keep functions and classes small, and choose good names that clearly define their responsibility. By using standard nomenclature we can communicate common functionality to other developers. Well written unit tests are also expressive, acting as documentation by example.

Spend enough time on, and give sufficient thought to making your code expressive.

Care is a precious resource.

### 4. Fewest elements

In a effort to make our functions and classes small, we may create too many small elements in the code. A balance needs to found. Our goal is to keep our overall system small, whilst also keeping our functions and classes small. This rule is the lowest priority of the four.

Be pragmatic.