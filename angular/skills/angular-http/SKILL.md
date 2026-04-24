---
name: angular-http
description: Type-safe API Communication with HttpClient
author: Diego Villanueva
trigger: When implementing API services, interceptors, or HTTP calls.
---

# Angular HTTP & API Integration

Professional backend communication using `provideHttpClient` and functional interceptors.

## ✅ ALWAYS
- Use `provideHttpClient()` and functional interceptors (`withInterceptors`).
- Define strict TypeScript interfaces for all API responses.
- Implement a global `ErrorInterceptor` for consistent error handling.
- Use `inject(HttpClient)` for dependency injection.
- Use RxJS operators like `retry()`, `catchError()`, and `shareReplay()` for robust data fetching.

## ❌ NEVER
- Subscribe to HTTP calls inside a Service; return the Observable to the component.
- Hardcode API base URLs; use `environment` files or a `basePath` injection token.
- Perform manual JSON parsing; let HttpClient handle the typing.

## 🛠 Patterns
- **Resource Pattern**: Using `rxResource` (Angular 19+) for declarative data fetching.
- **Loading State**: Wrapping Observables in a UI state object `{ data, loading, error }`.
