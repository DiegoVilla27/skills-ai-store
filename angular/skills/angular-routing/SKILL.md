---
description: 'Advanced Declarative Routing and Guards'
author: 'Diego Villanueva'
trigger: 'When implementing navigation, lazy-loaded routes, or route guards.'
---

# Angular Routing & Navigation

Mastery of the Angular Router for scalable, multi-feature applications.

## ✅ ALWAYS
- Use `provideRouter()` and `withComponentInputBinding()` for modern routing.
- Implement **Lazy Loading** for all feature modules using `loadChildren` or `loadComponent`.
- Use **Functional Guards** instead of class-based guards (CanActivateFn).
- Bind route parameters to component inputs using `@Input` (or `input()` in newer versions).
- Use `routerLink` for template-based navigation and `Router.navigate()` for programmatic control.

## ❌ NEVER
- Load all components in the main bundle.
- Put heavy business logic inside Guards or Resolvers.
- Use string-based paths directly in navigation calls; use a constant map.

## 🛠 Patterns
- **Shell Routes**: For layouts shared across multiple feature modules.
- **Data Resolvers**: Fetching critical data before route activation.
