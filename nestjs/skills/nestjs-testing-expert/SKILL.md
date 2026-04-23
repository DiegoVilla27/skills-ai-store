---
description: 'Advanced Unit and Integration Testing with Jest'
author: 'Diego Villanueva'
trigger: 'When implementing tests for controllers, services, or modules in NestJS.'
---

# NestJS Testing Expert

Mastery of the testing ecosystem for robust and bug-free backends.

## ✅ ALWAYS
- Use the `Test.createTestingModule` utility for isolated unit tests.
- Mock dependencies using `jest.fn()` or a dedicated mocking library (e.g., `jest-mock-extended`).
- Implement End-to-End (E2E) tests using `supertest` to validate the full request-response cycle.
- Use `useValue`, `useClass`, or `useFactory` to provide mock implementations during testing.
- Follow the "Testing Pyramid": many unit tests, several integration tests, few E2E tests.

## ❌ NEVER
- Use the real database in unit tests; use an in-memory database or mocks.
- Forget to `close()` the NestJS application instance after E2E tests to avoid memory leaks.
- Test private methods directly; test them through the public API.

## 🛠 Patterns
- **Database Cleaning**: Using a global hook to reset the test database between E2E runs.
- **Custom Matchers**: Creating Jest matchers for specific NestJS response patterns.
