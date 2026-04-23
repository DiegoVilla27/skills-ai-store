---
description: 'Scaling Complex Backends with Modular Architecture'
author: 'Diego Villanueva'
trigger: 'When designing large-scale applications with multiple domain modules.'
---

# NestJS Modular Monolith

Architectural excellence for scaling without the complexity of microservices.

## ✅ ALWAYS
- Organize the application into **Domain-based Modules**.
- Use `Dynamic Modules` for flexible and configurable integrations.
- Keep the `main.ts` file clean; move configuration to modules.
- Enforce strict boundaries between modules; use `exports` only for shared components.
- Implement a `SharedModule` for truly global utilities and services.

## ❌ NEVER
- Create circular dependencies between modules.
- Reference internal module implementation details from outside; use the public API.
- Create a giant "All-in-one" module.

## 🛠 Patterns
- **Bounded Contexts**: Designing modules based on business domains (DDD).
- **Module Factory**: Using `ConfigService` to dynamically configure modules.
