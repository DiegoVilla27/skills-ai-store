---
name: ngrx-signal-store
description: Lightweight and Opinionated State Management with Signals
author: Diego Villanueva
trigger: When implementing global or feature-level state management using NgRx SignalStore.
---

# NgRx SignalStore

Standardized state management using the modern Signal-based NgRx architecture.

## ✅ ALWAYS
- Use `signalStore` for feature/global state and `signalState` for lightweight local state.
- Define `withState` for initial data and `withComputed` for derived state.
- Use `withMethods` to encapsulate state mutations and side effects.
- Leverage `withHooks` for lifecycle logic (`onInit`, `onDestroy`).
- Use `rxMethod` for handling asynchronous streams (RxJS) within the SignalStore.

## ❌ NEVER
- Mutate state directly; always use the updater functions provided by the store.
- Put UI-specific logic inside the Store; keep it focused on state and business logic.
- Forget to handle unsubscriptions in `rxMethod` (although it's often automatic).

## 🛠 Patterns
- **Entity Management**: Using the `@ngrx/signals/entities` plugin for CRUD operations.
- **Deep Signal Selection**: Accessing nested state properties as individual Signals.
