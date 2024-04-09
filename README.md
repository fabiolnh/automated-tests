### Automated Tests

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
 * E2E: From Frontend, passing through the application until the database or other resource.
 * Integration Test: Commonly, involves external resources or drivers (incoming APIs). Talking about drivers, it communicates with the server (Example: Test a REST Endpoint, checking its HTTP status code). It has resource dependencies. Usually, they are slower than Unit Tests because they interact with IO.
 * Unit Test: Tests pieces of the code in isolation. It can involve more than one class (or more than one method) that collaborate with each other. It will not access the database, external APIs, etc. It has to be fast. It does not guarantee the functionality of the system.
