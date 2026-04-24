---
name: nestjs-patterns
description: Design Patterns and Enterprise Architecture in NestJS
author: Diego Villanueva
trigger: When designing complex system logic or choosing architectural patterns.
---

# NestJS Design Patterns

Standardized implementation of GoF and Enterprise patterns in NestJS.

## ✅ ALWAYS
- Use the **Strategy Pattern** for handling multiple algorithms (e.g., different payment gateways).
- Use **Factory Providers** for complex service initialization.
- Implement **Decorators** to add metadata or behavior to classes and methods.
- Use **Interceptors** for the Decorator/Proxy pattern to transform responses.
- Follow **SOLID** principles in every service and controller.

## ❌ NEVER
- Create giant "God Services" that handle everything.
- Hardcode business logic that could be abstracted using a pattern.
- Over-engineer; use patterns only when they solve a real complexity problem.

## 🛠 Patterns
- **Template Method**: Defining the skeleton of an algorithm in a base class.
- **Observer Pattern**: Using the `EventEmitterModule` for internal app events.
