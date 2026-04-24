---
name: angular-signals
description: Modern Reactive State with Angular Signals
author: Diego Villanueva
trigger: When implementing component state, computed values, or fine-grained reactivity.
---

# Angular Signals & Reactivity

Mastering the modern Signal-based reactivity model in Angular (v17+).

## ✅ ALWAYS
- Use `signal()` for mutable state.
- Use `computed()` for derived state to ensure optimal re-computation.
- Use `effect()` for side effects that don't modify other signals.
- Use `input()`, `output()`, and `model()` for component communication.
- Convert RxJS Observables to Signals using `toSignal()` for template usage.
- Follow the **Zoneless** approach by relying exclusively on Signals for change detection.

## ❌ NEVER
- Use `BehaviorSubject` for local component state if a Signal can do it.
- Mutate signals directly inside a template.
- Overuse `effect()`; prefer `computed()` for transforming data.

## 🛠 Patterns
- **Local Store**: Creating a feature-level Service with private `signal` and public `computed` members.
- **RxJS Integration**: Using `toObservable()` when you need to pipe signal changes through RxJS operators.
