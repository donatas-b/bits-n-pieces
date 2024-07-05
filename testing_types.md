## Unit Tests: Testing in Isolation
Unit tests focus on testing individual units or components of code in isolation. These units can be functions, methods, or classes, typically representing the smallest testable parts of an application. The key principle of unit testing is to isolate each unit from the rest of the codebase and verify its behavior independently.

## Component Tests: Testing Interactions
Component tests, also known as module tests, sit between unit tests and integration tests in terms of scope. While unit tests focus on individual units of code, component tests validate the interactions and integration between multiple units or components within a module or subsystem.

## Integration Tests: Testing the System as a Whole
Integration tests evaluate the interaction and integration of multiple modules or subsystems to ensure that they function correctly when combined. Unlike unit tests and component tests, which focus on isolated parts of the system, integration tests validate the behavior of the system as a whole.

## Regression testing
Tests performed after modifications are made to any software code or structure. It’s done to make sure that the software in question is still functional like it was before the modified or new features were introduced. Most times it’s just old test suits that are run to see if the application passes as it did before. Since this test type is similar to verification and mostly requires the test to be run over and over, it’s almost always automated. 