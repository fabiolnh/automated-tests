### Automated Tests (In Design)

- Given/Arrange -> When/Act -> Then/Assert
- Having 100% unit test coverage does not guarantee 100% correctness.

- FIRST:
  * Fast: Tests must execute quickly.
  * Independent: Each test should be independent of others.
  * Repeatable: Test results should be consistent regardless of how many times they are run.
  * Self-Validating: Tests should validate themselves.
  * Timely: Tests should be written before, during, or shortly after the code.

- TDD (Test-Driven Development): Write tests -> Make the code work -> Eliminate redundancy

Main Tests:
 * E2E: It replicates the experience of the final User. From Frontend (if your product has it. If it does not, can be an API), passing through the application until the database or other resource. (Ex: Selenium, Cypress, etc.)
 * Integration Test: Commonly, involves external resources or drivers (incoming APIs). Talking about drivers, it communicates with the server (Example: Test a REST Endpoint, checking its HTTP status code). It has resource dependencies. Usually, they are slower than Unit Tests because they interact with IO.
 * Unit Test: Tests pieces of the code in isolation. It can involve more than one class (or more than one method) that collaborate with each other. It will not access the database, external APIs, etc. It has to be fast. It does not guarantee the functionality of the system.

OBS: Ensure there isn't excessive redundancy across the three layers. There isn't a single best test; the ideal lies in the combination of all.

## Test Double / Patterns:
 - Stub: An object that returns a predefined answer. It provides a predefined object (the most commonly used). For example, you get the object (or interface) and define what it returns in each method. It overrides the methods, returning what you have defined.
 - Spy: It observes the execution to detect whether something that you wanted to happen has happened. For example, checking the methods in an object to see if they were called with specific parameters that you desired. Another example is verifying if a method was called one or more times. It records all the actions that occurred in the component, allowing you to perform assertions afterward.
 - Mock: Creates an object and programs the expected behavior of this object. For example, it expects that when a method is called, it will be called with certain arguments. It combines features of Stub and Spy by creating expectations within the object itself, typically using the method verify() at the final.
 - Fake: It is a simulated implementation that mimificates the original implementation. For instance, replacing a Postgres Connection Database (Original) with a Fake implementation like a Memory Database.

Note:
 * Dummy: Objects that we create solely to complete the list of parameters required to invoke some method.
