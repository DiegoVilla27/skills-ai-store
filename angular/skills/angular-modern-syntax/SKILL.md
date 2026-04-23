---
description: 'Control Flow, Deferrable Views, and Modern Template Syntax'
author: 'Diego Villanueva'
trigger: 'When building templates or optimizing UI loading performance.'
---

# Angular Modern Syntax

Mastery of the new template engine features introduced in Angular v17+.

## ✅ ALWAYS
- Use `@if`, `@else if`, `@else` for conditional rendering.
- Use `@for` with a mandatory `track` property for efficient list rendering.
- Use `@switch` for multi-condition templates.
- Leverage **Deferrable Views** (`@defer`) for lazy-loading heavy components.
- Combine `@defer` with `@placeholder`, `@loading`, and `@error` for premium UX.

## ❌ NEVER
- Use `*ngIf`, `*ngFor` or `ngSwitch` (Legacy directives) in new projects.
- Use `@for` without a unique `track` key.
- Forget to set `on` triggers (e.g., `on viewport`, `on idle`) in `@defer` blocks.

## 🛠 Patterns
- **Prefetching**: Using `@defer prefetch on ...` to load code before it is needed.
- **Skeleton Screens**: Using `@placeholder` to show UI shells during loading.
