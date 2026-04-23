---
description: 'Dependency Injection Mastery and Service Architecture'
author: 'Diego Villanueva'
trigger: 'When defining services, injection tokens, or complex DI trees.'
---

# Angular Dependency Injection (DI)

Leveraging Angular's hierarchical DI system for modular and testable code.

## ✅ ALWAYS
- Use the `inject()` function for DI instead of constructor injection (Modern Angular).
- Use `providedIn: 'root'` for singleton services.
- Define `InjectionToken` for configuration and abstract interfaces.
- Use `Optional()`, `Self()`, and `SkipSelf()` decorators to control DI resolution.
- Prefer **Functional Interceptors** and **Functional Guards** to reduce class boilerplate.

## ❌ NEVER
- Use constructor injection in new standalone components.
- Manually instantiate classes that should be managed by the DI container.
- Create circular dependencies between services.

## 🛠 Patterns
- **Factory Providers**: For dynamic service initialization.
- **Environment Providers**: Using `provideAppInitializer` for startup logic.
