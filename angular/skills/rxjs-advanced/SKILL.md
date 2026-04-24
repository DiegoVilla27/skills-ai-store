---
name: rxjs-advanced
description: Mastery of Observables, Streams, and Functional Reactive Programming
author: Diego Villanueva
trigger: When implementing complex data streams, real-time updates, or event orchestration.
---

# Advanced RxJS

Mastery of the power behind Angular's reactivity model.

## ✅ ALWAYS
- Use `pipe()` for combining operators.
- Use `switchMap` for discarding previous requests (e.g., search).
- Use `mergeMap` for parallel independent tasks.
- Use `concatMap` for sequential tasks.
- Use `exhaustMap` for ignoring new requests while one is in progress (e.g., login).
- Always clean up subscriptions using `takeUntilDestroyed()` (Angular 16+) or `take(1)`.

## ❌ NEVER
- Nested `.subscribe()` calls (The "Pyramid of Doom").
- Forget to handle errors with `catchError`.
- Manual unsubscriptions in components if `AsyncPipe` or `toSignal` can be used.

## 🛠 Patterns
- **Action Streams**: Using a `Subject` to trigger complex async flows.
- **Multicasting**: Using `shareReplay(1)` for caching and sharing stream data.
